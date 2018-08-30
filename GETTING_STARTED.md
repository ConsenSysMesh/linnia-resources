# Getting started

Interacting with the Linnia requires a connection to the Ethereum network and a storage solution of your choice. If you follow this tutorial, you will be able to use the library to store files in either IPFS, a decentralized storage solution, or AWS S3.

#### Choosing an Ethereum Network to Use

[Ethereum](https://www.ethereum.org/) is a blockchain-based platform that allows for the operation of decentralized applications. Since the Linnia protocol is still a work in progress, we can test it by either connecting to the Ropsten Ethereum Testnet or use an application called Ganache to simulate an Ethereum network locally. You choose which network to connect to when you pass in the `web3` argument to the library constructor, like so:

```javascript
// local connection, since HttpProvider points to localhost
let web3 = new Web3(new Web3.providers.HttpProvider('http://localhost:7545'))
```

We strongly recommend starting your development locally with Ganache, then moving to Ropsten when you are ready to go live.

#### Using Ganache

The other option we have for testing is to simulate an ethereum network locally. Our sister project Truffle has created a great tool called [Ganache](http://truffleframework.com/ganache) that allows us to do this. We will use the [CLI version](https://github.com/trufflesuite/ganache-cli).

Our main repository, [https://github.com/ConsenSys/Linnia-Smart-Contracts](https://github.com/ConsenSys/Linnia-Smart-Contracts) includes a stable version of the CLI and a task to run it

To install it, use:
```bash
git clone https://github.com/ConsenSys/Linnia-Smart-Contracts
npm install
```

Now you can navigate to that repo and run:

```bash
npm run start
```
To run your own simulated blockchain locally on port 7545!

Now, to connect to the local blockchain, create this web3 object and pass it as the first argument to the linnia-js constructor:

```javascript
// local connection, since HttpProvider points to localhost
let web3 = new Web3(new Web3.providers.HttpProvider('http://localhost:7545'))
```

#### Ropsten Testnet

The Ropsten Testnet is a clone of the Ethereum Testnet that allows us to deploy and test out our decentralized applications with no risk before deploying them on the Ethereum Mainnet. The Linnia team has already deployed a version of the Linnia Protocol smart contracts on this Testnet, so if you choose to use it, you already have half of the work done for you. On the flip side, **all interactions with these contracts are liable to be wiped out at any moment if the Linnia team redeploys.**

#### Registering for an Infura to connect to Ropsten

[Infura](https://infura.io/about) is a service that allows you to connect to the ethereum network locally without having to run a node. All you need to do to get started with Infura is [sign up here](https://infura.io/signup).

Once you do, Infura will send you an email with links to use to connect to Infura in this format:

```
https://ropsten.infura.io/${YOUR_ACCESS_TOKEN}
```

To connect to Ropsten when using linnia-js, create this web3 object and pass it as the first argument to the linnia-js constructor:

```javascript
// ropsten connection, since HttpProvider points to authenticated ropsten infura link
let web3 = new Web3(new Web3.providers.HttpProvider('https://ropsten.infura.io/${YOUR_ACCESS_TOKEN}'))
```

#### Storing files on IPFS

[IPFS](https://ipfs.io), short for InterPlanetary File System, is a peer-to-peer storage solution for files. As with Ethereum, we have the option to either connect to the IPFS network, or run one locally ourselves.

#### Connecting to IPFS through Infura

If you wish to use Infura to connect to IPFS, congratulations, you are already done!

You can just use the Infura url when connecting, like so:

```javascript
const IPFS = require('ipfs-api');
const ipfs = new IPFS({
  host: 'ipfs.infura.io',
  port: 5001,
  protocol: 'https'
});
```

To install it locally, head over to the [IPFS install page](https://ipfs.io/docs/install/) and download the binary. Once done, run:

```bash
sudo mv ipfs /usr/local/bin/ipfs
```

Then, to start the service, run:

```bash
ipfs init
ipfs daemon
```

#### Storing files on AWS S3

[S3](https://aws.amazon.com/s3/) is a popular cloud storage service provided by Amazon Web services. We recommend using IPFS or another decentralized storage solution in most use cases, since AWS infastructure will add a point of centralization to your application, but if you feel more comfortable developing with it, or if you want to use some of the services provided by AWS to interact with your records, it is completely acceptable to use it.

Unlike IPFS, we do not have the option to run a node locally. To use it, we need to [sign up for an AWS account](https://aws.amazon.com/free/). 

Next, you will need to issue a pair of access keys for your application to use. You will need to create a pair of access keys. If you are unfamiliar with how to do this, the `Access Keys` section of [this page](https://docs.aws.amazon.com/general/latest/gr/aws-sec-cred-types.html).

You will also need to create a bucket to put your files in. This can be done by following [this](https://docs.aws.amazon.com/AmazonS3/latest/gsg/CreatingABucket.html) tutorial.

Once you have an account set up, you will need to install and configure the AWS JS SDK. Instructions for how to do so can be found [here](https://aws.amazon.com/sdk-for-node-js/).

Now, you should be able to get started coding!

You can import the sdk and instantiate an S3 client instance like so:

```javascript
const AWS = require('aws-sdk');

const s3 = new AWS.S3({ region: YOUR_ACOUNT_REGION });
```

Next, you can form your `object` to put into S3:

```javascript
const params = {
	Body: YOUR_ENCRYPTED_DATA, 
	Bucket: YOUR_BUCKET_NAME, 
	Key: dataHash, // the dataHash of your data
	ServerSideEncryption: "AES256", // (optional): extra encryption at rest if you choose
	ACL: 'public-read', // public read so anyone with decryption keys can read
	Tagging: metaData // (optional): and metaData you wish to 
};
```
And then put the object into S3:

```javascript
const response = await new Promise((resolve, reject) => {
	s3.putObject(params, function(err, data) {
	    err ? reject(err) : resolve(data);
	});
});
```

If the request is successful, you then form the dataUri and create the Linnia record:

```javascript
const dataUri = `https://${bucketName}.s3.amazonaws.com/${dataHash}`;

await records.addRecord(dataHash, metaData, dataUri, {
	from: OWNER_ADDRESS
	gas: YOUR_GAS_LIMIT
});
```

And you're all set!




