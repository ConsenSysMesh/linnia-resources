# Keys

The Linnia protocol need 4 different keys to work: (Ethereum Private Key, Ethereum Address, Encryption Private Key, Encryption Public key)



### Ethereum Keys

In order to add data to the Linnia Smart Contracts, the user needs an ethereum wallet to be able to sign transaction and add them to the ethereum blockchain. (We recommend to download Metamask https://metamask.io/ to create the **Ethereum Keys** and sign the transaction)

There are 2 different Ethereum Keys, the first one is your **Ethereum Private Key**: this has to be private, nobody should have access to this but you. With this key you can sign transactions and add them to the blockchain. This is you authentication key, to prove your identity.

The second one is your **Ethereum Address**: this is public and is how external users refer to yourself. If someone want's to share data with you using Linnia they will need your Ethereum Address.



### Encryption Keys

In order to add data to the Linnia Protocol, the data has to be encrypted. That means that the data will look like a bunch of random letters and numbers. When you encrypt some data you are hiding the real content so nobody can understand. In order to recover the original data you need to decrypt. There are also 2 **Encryption Keys**

This first one is the **Encryption Private Key**: similar to the **Ethereum Private Key** this key has to be private too and the owner is the only one that should have access to. You need this key in order to decrypt the data, so after you retrieve the hidden random looking data, with this key you will be able to convert that into the readable original content.

The second one is your **Encryption Public Key**: this is public and is how external users can share data with you. If you want to share data with Bob, you can encrypt (hide) using Bob's **Encryption Public Key** and then the only one that will be able to decrypt and read the original content will be Bob.

