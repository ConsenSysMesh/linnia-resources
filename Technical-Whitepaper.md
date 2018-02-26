# Linnia Technical Paper

# Introduction

## From Web 2.0 to Web 3.0

Our current web (Web 2.0) is siloed and centralized. The Internet was meant to be a network technology enabling data to flow freely without bottlenecks or monopolies. In the past decade and a half we have noticed that this vision has turned into a digital world dominated by few main players.

We believe that these players, such as Facebook, Google, Instagram, Twitter and YouTube, were instrumental in bringing the web to its current stage. The transition from Web 1.0 to Web 2.0 involved arrival of incredible applications and services, from the emergence of social networks, content-sharing platforms and extremely clever user experiences. However, in the process, we lost something very important  - sovereignty over our digital selves. Today, we neither control our digital identity nor do we control our data because nearly everything is based on single sign-on, enabling third-parties to freely share and monetize our information with no possibility of control from the actual owner: us.

We believe that Web 2.0 has served its purpose and that we should now prepare to enter Web 3.0. The paradigm where we surrender our data and all control over it in exchange for a service has come to an end. We also believe that if we don't provide a better User Experience (UX) that is more simple and efficient than the existing ones, we will fail to create the impulse needed to move people from Web 2.0 to Web 3.0.

Finally, we w to achieve our ideals and create the web many of us want, blockchains and decentralized technologies need to be considered as a mean, not as an end in itself. The real shift will happen when non-blockchain developers, regular users, entrepreneurs and governments will feel empowered enough to start using these technologies as their own. It starts here, with the help of the whole community.

*[future footnotes] Simple in the sense that using this UX does not require any deep technical understanding. Efficient in the sense that the user won't spend more time using a Web 3.0 dApp than it would have using a Web 2.0 application. That includes respecting best practices of visibility and navigability.*

**Our relationship with the Web  - its applications and its service providers - needs to evolve into a more mature stage and be more respectful to one's privacy and sovereignty.**

The full vision behind Linnia is explained in detail in the[Introductory Linnia White Paper](https://consensys.quip.com/uvpXAabk3xOh/INTRODUCTION-TO-LINNIA).

In this paper, we introduce Linnia as a protocol using the Ethereum blockchain to bring the power of decentralization to secure longitudinal personal data management. Linnia's technical core contribution relies on a Protocol and User Experience research efforts.

We will first discuss the technical context of the project by comparing Linnia and other initiatives that may seem similar or related. We will then reveal our technical approach and the tools we aim to provide to the ecosystem. We finally conclude with more information on our roadmap and the perspectives.


## A Singleton has more than one face

undefined

[source](https://www.pinterest.fr/pin/535013630709742486/)

**What is Identity for Linnia? A dual concept**

The *Singleton* is a technical term used to describe an object that only has **one **instance of itself.

The concept of *identity* conveys a sense of *uniqueness*. The same way a person only exists as one instance of itself in the real world, so will it be in the digital world. This is where the term *Singleton* is powerful to describe identity.

However, the digital world also needs to convey the idea that a person's identity might be used and revealed in different ways depending on the context. In real life, Alice might be a doctor, a Tesla car owner, and a diabetic. Depending on the context, she might be interacting with Tesla customer support, accessing her patient's file in the database of the hospital or joining a group of discussions for diabetic individuals. Each time, she will have to expose different facets of her identity. In the real world, it is simple, as no one can (yet) read one's mind. One must choose to only disclose the information one feels is relevant. To support these claims, we can often provide a physical document (a professional card, a medical certificate or a car registration document). To express the contextual nature of identity in the digital world, we use the term **facets**. Unique and manifold, just like our real life identity, each Singleton will have an infinite number of facets.

Linnia will be a bridge between a user *Singleton *(stored in a decentralized identity platform for self-sovereignty) and its data files (stored in a decentralized storage platform for self-management).


## The Landscape of Data Privacy-oriented Initiatives

All the projects presented in this section have similar goals related to data security (Linnia included).
The originality of each of these projects relies on the breadth of their technical approaches. We believe that it is very interesting to have multiple projects in the ecosystem trying to solve major technical challenges with different methods. We also believe that a collaboration framework can emerge from this research effort, allowing our organizations to explore this space together and share knowledge without compromising the diversity of our solutions or moving toward technical homogeneity.

**Rockchain**
Rockchain is an infrastructure project that interacts with the Ethereum blockchain. Their infrastructure provides access rights to control distributed data and computation results.  Rockchain is not a UX-oriented project and will probably focus on its infrastructure for the next few years. Linnia is a binder, an enabler for interoperability and a UX-oriented project. For these reasons, we believe that Linnia could use Rockchain in its lower layers as a storage and computing component in order to increase the diversity of the Linnia Mesh with vetted outside support. We will discuss the Linnia Mesh in the last part of this paper. 

**Keep network**
Keep is an off-chain container for private data which allows contracts to manage and use private data without exposing it the public blockchain in order to execute operations over this data. The data is published encrypted on the blockchain and computation will be delegated to keep network, the result afterwards will be published again to be reviewed on the blockchain.
Keep focuses on executing calculation over encrypted data, Linnia on the other hand has a broader approach where the computation represents only one part of the project and it would be interesting if Linnia could use Keep as its computation network.

**Enigma**
Enigma is a decentralized computation platform connected to an existing blockchain. Its goal is to enable to build privacy by design without the need of a third party using private smart contracts. Unlike blockchains, computations and data storage are not replicated by every node in the network. Only a small subset performs each computation over different parts of the data.
Linnia uses smart contracts in order to allow users to share their data, control access permission from outside applications and do calculation over their encrypted data. The smart contracts platform used by Enigma could be very useful for Linnia  to protect user privacy.


**Two major differences between Enigma and Keep:**

Keep is working on a narrow approach rather than build a grand approach to “private smart contracts”. Keep focuses on mitigating attacks such as Sybil attacks while Enigma risks of having a large attack surface because of the private smart contracts platform which creates bigger attack surface. 
On the other hand, Enigma's unique technology of private smart contracts allows the code itself to be run off-chain when it needs to be private and the nodes running these private contracts to prove they have executed correctly the contract.
On the technical side, Keep is building on-chain Random Number Generators (RNG) while both Enigma and Keep use SMPC (Secure MultiParty Computation) to query data and compute over it in a distributed way. Data will be stored using decentralized solutions for both of these projects.



**Ocean**
*[WIP Carlos Buendia]*
The Ocean Protocol includes a protocol that makes use of curation markets to categorize the value of encrypted data in order to enable a decentralized data marketplace. 



|	|UX focus	|Identity Centric	|Data Privacy	|Permissions & Policies 	|Interoperability focus	|
|---	|---	|---	|---	|---	|---	|
|	|(Developers and Users experience research effort)	|(Attestions - link between decentralized identity and data files)	|(Blind computation)	|(Self-managed data files, compliance with user's regulatory framework)	|(Enabler for Web 3.0 ecosystem, interoperability effort)	|
|LINNIA	|yes	|yes	|yes	|yes	|yes	|
|KEEP	|no	|no	|yes	|no	|no	|
|ROCKCHAIN	|	|	|yes	|yes	|	|
|ENIGMA	|yes	|no	|yes	|no	|no	|
|OCEAN	|no	|no	|yes	|yes	|yes	|
|UPORT	|yes (?)	|yes	|no	|	|yes	|

Figure X - A few points of comparisons for Linnia


# Technical overview

## Linnia, an enabler of Web 3.0

The goal of this paper is to lay out Linnia's technical approach to facilitate the transition from Web 2.0 to Web 3.0.

Linnia is not a decentralized identity platform (e.g. uPort, Civic, YouBase etc.), nor is it a decentralized storage platform (e.g. IPFS, SWARM etc.), nor a decentralized cloud platform (e.g. iExec). Instead, Linnia aims to work with all the above and many others to bring Web 3.0 to life.

**Linnia offers a protocol that will interact with a blockchain (e.g. Ethereum), decentralized platforms (e.g. uPort, IPFS, iExec), connected devices (e.g. Fitbit) and browser extensions (e.g. Metamask).*** **[footnote: a more comprehensive list of the projects we aim at collaborating with will be provided in the future, every projects in the community is welcome to contact us to discuss about working on an integration effort]***
Linnia's goal is to bind these powerful technologies to design a service-oriented architecture and offer great UX for the developers who want to build Web 3.0-based applications. **
**Linnia is also a research-oriented project which aims at tackling some of the most interesting challenges related to reconciling transparency with confidentiality.**


## Overview of the architecture

[INSERT FIGURE, this doodle will be turned into a figure by Carlos Buendia ]

undefined

undefined


Figure X - Overview of the Linnia Architecture

Mains components:

* User and its local client (with storage capabilities)
* Applications interface (front-end)
* *(optional)* Application DB if not a dApp 
* Blockchain & smart contracts 
* Decentralized Storage
* Computation mesh



# **Linnia Core Components**

## Attaching the problem: Seven Verticals 


As an integration protocol, Linnia will leverage some of the technologies that several projects are already working on. In order to provide the previous functionalities, the problem is divided into the core modules: 


1. **Decentralized Identity:** One of the core aims of the Linnia protocol is to bring back the control of data to the user by linking its data files to its decentralized identity. 
2. **Decentralized storage:** It wouldn't be possible to let users own their data if it's  stored on a third-party server. With Linnia, the usage of decentralized storage solutions (IPFS, Swarm), will play a major role. 
3. **Contextual attestations**: Attestations (either on-chain or off-chain) are a powerful tool which enables any Ethereum account to endorse any other piece of data. However, usability varies depending on the context. Linnia will provide a way to contextualize these attestations and make them useful to third party applications.
4. **Permissions and Policies**: In order to build a user-centric architecture, every critical step in terms of data governance (data acquisition, sharing, storage, computation) needs to be compliant with the user's preferences.
5. **Data and Metadata:** In the same way that the semantic web enabled the creation of linked data structures between completely different web applications, decentralized applications will need to provide common data formats that enable intercommunication between DApps and data reuse.  
6. **Quality scoring (IRIS): **By creating an algorithm to calculate the underlying value of the data uploaded by the user, the protocol will enable to incentivize the users to contribute with more content to increase their IRIS score.
7. **Data Computation:  **Applications need to execute calculation over data to run their services. However, the computation is not done locally by the data owner; instead, it is done by untrusted parties. Blind computation is a way to improve usability of data while preserving its privacy. 
    *[Footnote : Computation on encrypted data will be more extensively addressed in the last part of the document “Linnia Blind Computation Mesh”.]*

All of these verticals will be explained in details in the following sections.


## 1. Decentralized Identity

Current Web 2.0 users create numerous accounts in different apps and websites. Each Web 2.0 context results in a new identity facet. This collection includes an identity facet for email, a shopping site, a car-sharing application and so on. Ethereum provides a single decentralized database, wherein singleton data structures can be shared among all the blockchain network participants [?]. The Linnia protocol’s reliable identity singleton solves this** identity challenge** faced by the developers of third-party apps.

Linnia is an **identity-centric protocol**. Identity is unique and manifold. Each user should only interact with Linnia protocol based apps with a single identity. Once claimed via Linnia, your singleton (persistent ID) will anchor and bind your self-sovereign identity to your self-managed data files via Facets (using child keys).

In order for Linnia to work and offer a new experience to Web 3.0 user, Identity appears as a cornerstone. Several projects are currently working on solving the self-sovereign identity issue, we can name these following initiatives:

1. OneName [ *]* started using the NameCoin protocol [ *]* in the early days of Bitcoin [ ];
2. the W F [ *]* has created an initiative to provide a common standard;
3. BIP32, HDWallets Hierarchical Deterministic wallets; and
4. uPort [ *]* provides today one of the most advanced running pilots of a digital identity solution.

To create a sense of ownership around user's data, Linnia is going to use self-sovereign identity to build a bridge with self-managed data files.

**HD wallets - A bridge between the Singleton and its Facets**

Since all the data files (decentralized storage instances) must be linked to the facets of the user's singleton (decentralized identity instance), we will introduce here a preliminary approach to designing this system.

**HDWallets** (Hierarchical Deterministic wallets) can play a significant role by creating a unique but multifaceted identity. HDWallets were created in Bitcoin (BIP32) [ *]** *as a tool to generate wallets derived from a known seed. Child keys are derived from this known parent seed. HD wallets can also be a very useful tool for identity schemes, as identity facets can be generated as child keys. 
Our digital identities have many identity **facets. **A facet is a contextualized identity which is why each child key will be used in a different context.
This further protects the privacy of other facets. Additionally, HDwallets enable revocation of child keys by just using the seed only known by the master key. The following figure illustrates the usage of HDWallets in many facets, all of them deriving from a common parent key. This provides practical source for child keys, which are created for specific temporary user experiences. In this scenario, if any child key is leaked or lost, the parent key is still safe, and the user's singleton is not compromised.
undefined

*Figure X. Example with 3 facets: health, mobility and photos.*



## **2. Decentralized Storage**

**IPFS** and **Swarm**** **decentralized storage solutions will play a major role in the Linnia Protocol. Here the Linnia protocol solves the limiting Web 2.0 dependency of centralized data storage infrastructure. Long-standing BitTorrent protocols introduced peer-to-peer solutions to avoid centralization and possible content censorship. However, BitTorrent’s architecture was oriented to providing a way to share already packed resources, and not addressing problems like duplicity and granularity on content discovery.
In the Web 3.0 decentralized era, different services are working on solving these storage issues: IPFS was one of the first movers, providing a persistent content addressed storage layer for the decentralized web.
Also, Ethereum with its vision of providing a full decentralized stack for the web of trust started the development of **Swarm. **Swarm is a storage layer integrated with the Ethereum blockchain to provide economic incentives. Swarm's core storage component is an immutable content addressed chunkstore [] rather than a generic DHT (distributed hash table),  IPFS combines a distributed hashtable.
We will need DHT for the computation part in order to divide and send data to be computed in an easy way. However, there is no native search function provided by either Swarm nor IPFS. Furthermore, data disclosure over decentralized storage is usually covered via encryption schemes. In this context, we find the same dilemma between privacy and data utility for third-parties: the less data you store in plain text, the harder it is to find any utility for the uploaded data.

When a user will push its data files on Linnia, the data will be processed this way:

1. Metadata analysis and storage (creation of a metadata structure) in an easily searchable database (e.g. PostgreSQL),
2. Quality scoring computation (IRIS) either on-chain or off-chain with proof of computation,
3. Permissions setting (none, by default),
4. Encrypted file and its metadata are stored, for example, on IPFS,
5. Update of the mapping table of the database in (1.) with the corresponding IPFS hash newly generated.



## **3. Contextual Attestations**

Attestations are used in the uPort system to prove that a certain identity's claim about another one is valid. []
Attestations, either *on-chain* or *off-chain*, are a powerful tool which enables any Ethereum account to endorse any other piece of data.
We consider that their usability in a specific context can be increased with the right attributes. 
Linnia will provide a way to contextualize these attestations by working on a general data structure (JSON file) with some relevant attributes for Linnia based applications.

Our attestations will then be able to have a “weight” depending on the signatures they carry. This “weight” will be influenced by the number of signatures and also by their provenance. The provenance will be retrieved by verifying if the identity facet that was used to sign correspond to an “expert agent” facet.
For example, if a doctor signs an attestation in a medical context, the doctor's signature will have more weight since she/he can display a “medical facet”.
Here the confirmation by a specific expert agent such as a Healthcare Provider may certify the provenance* *of the specific data (e.g. a Continuity of Care Document [[source](https://web.archive.org/web/20120320190602/http://www.corepointhealth.com/whitepapers/continuity-care-document-ccd-changing-landscape-healthcare-information-exchange)]).

The Linnia-based application will have the information that this attestation has been verified by an “**expert agent” **which can trigger an action at the application level (validation of a pharmaceutical prescription, bounty claim, instant access to a specific area etc.).

We can also imagine more complex scheme of attestations (with multisig) where N differents types of “expert agent” are needed to verify (sign) a certain *claim *in a specific order*.*


## 4. Permissions and Policies

The Linnia protocol enables data acquisition, search, computation, and display.
Every function of this protocol needs to be fully compliant with users' preferences.
Linnia's Policies and Permissions are a set of records used to make permanent a user’s preferences for sharing data (via P*ermissions) *and for managing its data when handled by Linnia or third-parties (via *Policies*).
For example, a user can create a permission to share its data with an application A and if its *Singleton *reveals that the user is a EU citizen, a GPDR policy will be set so that the user's data are stored in a compliant way regarding the user's country regulatory framework.
In order to let the data flow as freely as possible, the user will be able to easily set up and manage its permissions toward third parties. Each Linnia based application needs permissions to access the user’s data expression and these permissions can be revoked at all time.

The following scenario is an example of a use case of Linnia permissionning component:

Let’s say that Alice decides to download Linnia based app **A**.
*Initial condition*: Alice has already connected to Linnia her identity singleton through an attestation.

1. Alice agrees to let the application access some of her data by setting a permission for App “A”.
2. App “A” send a query to fetch Alice’s data.
3. The permissions are checked to see if the query is valid. If yes, then:

4.A Case 1: 

    1. Alice's files are fetched from the decentralized storage to her local client.
    2. These files are decrypted by Alice's client and encrypted with App “A” public key.
    3. The files are sent via an encrypted tunnel to App “A”.
    4. App “A” decrypt the files and can run its algorithm.


4.B Case 2:  

    1. App “A” computes on Alice’s data using the Linnia Mesh.

5. App “A” offers Alice interesting insights and beautiful data visualizations.


## **5. Data and Metadata**

Linnia must play the role of **data market maker**. An efficient data market requires data discovery and thus search. Since all user data is encrypted by default once uploaded, search is not possible unless the user makes public some standard information that we call *metadata*. Linnia will introduce contextual metadata models and might consider technologies like IPLD [ ] to connect different data sources.

Data discovery requires the classification and the differentiation of data. A service must be able to discover and make use of the necessary part of a dataset. Current decentralized storage solutions like Swarm and IPFS link their resources via a Merkle DAG. This type of schemas search is not possible, because it is necessary to know either the resource's content or its hash in order to identify the file.
This dilemma brings out the following different solutions: **Encrypted computation** and **Linked Metadata based indexing**.

Linnia’s search infrastructure for these decentralized data storage systems includes the following types of metadata:

1. **Contextual metadata** that describes the characteristics of the object behind a hash identifier
2. **Quality metadata** needed to compute the IRIS Score without revealing the data.

## 6. Quality Scoring with IRIS

*IRIS stands for InfoRmation Integrity Score.*

**The IRIS Score** enables different actors to determine the value of a given set of data without accessing its content. *[footnote/attempt to link the name : It is also the name of the Rainbow goddess in Greek mythology. **Just as a rainbow has many colors, data's value relies on several components.]*

The value of a precious gem (e.g. a diamond) is estimated through the concept of CARAT. Then, depending on the market, a certain amount of CARAT will be worth a certain amount in dollars.
By analogy, Linnia aims to create a “value unit” for data. This requires a specific model for each domain (social data, health data, mobility data, home data etc.) but the main criteria are always the same. These criteria are chosen after consensus from the domain experts, together they create a scale that is voted by the community. The voted scale is stored on-chain to prevent any tampering and to ensure that in the future, all data that are pushed into the system will have their IRIS score calculated in the same way - Linnia doesn't decide anyone's data value.
Every time a user pushes data through Linnia, its IRIS score will go up proportionally to the value of its data, the interface will display that information thus creating a basis for a gamified relationship between the user and its IRIS. This will further impact in a positive way the user experience. 

To illustrate the concept of IRIS, let's take an example in Healthcare involving two main criteria: data type and data provenance.
If a data “blood-lab measurement” is sent by a medical* *laboratory* *for a user, that data will have a good provenance score - the laboratory being a certified source or "expert agent" -  and thus a higher IRIS than if the user had self-declared the same data. 
Additionally, a “blood-lab measurement” will be worth more than “pedometer measurements” because the first data type is harder to get and more valuable in the healthcare community.
These decisions will be based on a public scale built by expert discussions and consensus. 

**Connected devices can also be a source of data**
For connected devices such as fitness trackers, a scale is going to be set depending on how easy it will be to cheat a particular device and generate fake data, but ultimately some certified devices will appear with various provenance scores.

**Gaming the IRIS score**
User's self-declared data will have a lower medical provenance score but are still meaningful to draw an activity profile that other applications running on top of Linnia will leverage. These informations will be used by applications to feed their algorithms, to create insightful visualization tools or for scientific research that needs multiple factors search (a specific age range, correlated with a specific treatment, a disease or a specific environment).
This way, there is an incentive for the user to keep pushing its data but no incentive for the user to lie about their data. Indeed, they can't gain much from pushing fake data as the provenance source is low (and so will be the IRIS), but they can lose a lot because they will be feeding their own applications with bad data - rendering their applications useless.

## **7. Data computation**

Given the computational costs and privacy restrictions in order to characterize and score each user's data we need to run expensive algorithms. In these situation, using the current Ethereum blockchain for computation is not appropriate. As a need to protect the user's privacy, Linnia will use protocols like sMPC in order to do all sorts of computation on encrypted data. Deterministic off-chain computation is a current field of research in the Ethereum community. Linnia dedicates an off-chain network connected to the Main Ethereum blockchain to do all sorts of computation, this network is known as **Linnia Computation Mesh. **The computation Mesh  is composed of multiple nodes that are either third-party or Linnia vetted nodes (based on their reputation and computation capability). Collectively these nodes are responsible for handling all types of arithmetic computation and delivering the result to the user in exchange for a payment. Linnia's goal is to both preserve privacy and optimize computation time for the user via blind computation.

**Blind data computation**
The limited computation power of user devices and the growing number of computationally intensive tasks makes the delegation of data computation to large data centers a desirable solution. This delegation, however, creates confidentiality and privacy issues when sharing data with untrusted data centers for computation purposes. To solve these issues and preserve user privacy, the data must be hidden via encryption using Blind Computation which allows limited computational functions over encrypted data without leaking information data to third parties.

Linnia allows users to perform blind computation over their data upon their request or on a Linnia-based application request. This means that data is never shared with these applications only the result of the computation done by the computation mesh is shared.
Since this network consumes computation power in order to conduct these calculations, whoever requests the result will have to pay it. For example, a Linnia-based application needs to apply a matching algorithm for kidney transplants, this algorithm must access the donor and recipient's data to find the match. Linnia's approach would be to run the matching algorithm on encrypted data without any disclosure of private data.
Linnia Mesh allows a user and an application to communicate off-chain and only the final state is logged on the blockchain. If for some reason a dispute occurs, for example,  the user claims that it didn't give permission to the application, then the series of signed off-chain transactions can be uploaded to the blockchain for verification or dispute resolution.

**Encryption Protocols**
Blind computation means that the data will be encrypted/obfuscated and calculation will be done over this encrypted data. There exists different cryptographic protocols which allow us to operate over encrypted data, Homomorphic encryption (HE) protocols are the most famous ones, yet the least practical ones. The problem with Homomorphic Encryption can be summarized in: 

* First, some protocols support only one of both operations (addition/multiplication) on the ciphertext. We call these protocols  SomeWhat Homomorphic Schemes (SHE) such as RSA (multiplicatively homomorphic) and Paillier cryptosystem (additively homomorphic).
* Second, those which support both operations known by Fully Homomorphic Encryption (FHE)  protocols ( for example the Ideal Lattices protocol designed by Graig Gentry) are very costly in terms of complexity. 

Secure MultiParty Computation (SMPC) is another example of cryptographic schemes which handle Blind Computation using a different approach, the data (secret) will not be encrypted. Instead, it will be divided between multiple untrusted parties in a way that makes it unreadable, each one of those parties will do computation on their share of the data and send it back to the owner in order to reconstruct it.  Shamir Secret Sharing (SSS) is an example of such schemes. Zero Knowledge Protocols (ZKP) as well give the possibility to parties to communicate, perform computation and verify the correctness of this computation without sharing the secret like ZK-SNARKS for example.

The protocols listed above are all explored by Linnia in order to solve the Blind computation challenge while preserving user privacy and optimize the computation complexity. The details of  Linnia's approach will be published in future articles where research work will be discussed. 


# Linnia Blind Computation Mesh

## **Computation incentive algorithm **

Linnia uses the following consensus model to incentivize the mesh nodes to participate in the computation process by using their computation power, staying online and computing correct results.


1. **Choose:** Linnia runs a smart contract which allows to solicit the nodes who have a good reputation profile (i.e reputation will be measured according to the level of credibility of computation they have done before) and have enough computation power for the operation wanted since nodes differ in resources.  Each time the node misbehaves, the reputation decreases as well the probability that the node will be chosen for the next round.
2. **Participate: **The chosen nodes will be notified when there is a request for computation, the request will contain the proposed price for each operation.
3. **Commit: **The nodes which agree on the price will notify back the user by sending a response via Linnia application. The user confirms to continue the process, nodes will have to prove their commitment by putting up a security deposit in an escrow smart contract. The value of the security deposit will be set according to how much the operation is expensive in terms of previously price and computation power.
4. **Prove: **Linnia will run a verification process on the blockchain in order to verify the computation correctness. The verification process will permit Linnia to distinguish between honest and dishonest nodes, the reason why it's done on and not off-chain is to keep a permanent proof in case nodes complain about being misjudged.
5. **Reward/Punishment: **After the verification process is done, the security deposit will be given back to honest nodes and taken away from malicious ones to be distributed all over the network participating in the computation.

***Who controls the escrow contract? ***No one, the contract is filled with the fulfillment of the conditions which the user/application and the mesh nodes agreed upon and will then run automatically.
***Who has the right to rewards/punish?* **Since the audit will be done on-chain by all the network, neither the user nor Linnia will have an upper hand to change the result and improperly hold the security deposit.
***Who owns the Linnia mesh?  ***It's definitely not Linnia, these nodes volunteer to use their resources for computation, Linnia will accept them and creates a reputation profile for each one of these nodes. Each time there is a computation request, nodes will be chosen according to the smart contract policies, this choice however is not up to Linnia to control.


## **Tokens for data exchange and computation**

In order to provide a peer-to-peer network dedicated to performing computation on encrypted data, we need to find a way to incentivize the nodes. These nodes will be paid for the computation power in Linnia tokens (as mentioned in the Linnia White Paper). Depending on who orders the computation, the payer will be different. If the user wants Linnia to provide computation results, then the payer is the user, and it needs to send a token transaction to Linnia. If the payer is a third-party that is computing on user's data, the payer will need to send a token transaction to the user to pay for data usage (before that, verification is done to ensure that these users have already accepted that their data are going to be used but not disclosed to the third-party) and to pay the Linnia peers for the computation as well. 
If the third-party is paying for the access to the plaintext data, then the only tokens that are sent are meant to pay the user for sharing their data. In this case, no computation needed and no payment for the Linnia mesh nodes is made.


# Roadmap and Ecosystem

## Linnia and the Ecosystem

### APIs & LIBRARIES

The Linnia protocol will nurture an ecosystem of developers tools and libraries.  With these tools, it becomes simple to handle self-managed data. Linnia strives to achieve a wide range of data interoperability including the following:

1. Personal wearable devices such as fitness trackers;
2. Electronic Health Records (EHR), Health Information Exchanges (HIEs) and Fast Healthcare Interoperability Resources (FHIR) server; and

These tools and libraries will allow fast and secure import of hierarchical JSON data files.
The Linnia team will implement and provide code for the research concepts that are introduced in the protocol (singleton, facets, contextual attestations etc.).

### Research papers

The Linnia team will provide update of its research effort on data privacy management and user experience research and development effort around dApp user interfaces and interactions to the dApp developpers community.

### Workshops and events

This technical stack will be open for decentralized applications in multiple spheres to build upon, especially the ones dealing with personal data.
To test the protocol and identifies the priorities in terms of development, discussions with the community (Q&As) will be scheduled and when the first stable protocol version will be released, a dApp Hackathon will be hosted.


## Roadmap

undefined* * *

# **Conclusion and perspectives**

Web 2.0 was a brief interlude between the birth of the Internet and the arrival of our self- sovereignty. Web 3.0 is the future. A future in which individuals can control their data to act in their own interest.
Linnia aims at enabling all emerging decentralized technologies to interoperate in a way that will allow the collaboration around Web 3.0 to increase, with a specific focus over user's self-managed data files.

This technical paper aimed at explaining the approach that the Linnia team is taking to solve majors challenges related to these goals, especially :

* A decentralized** data exchange protocol,**
* A user **experience research and development effort.**

## **Challenges facing Linnia**

The R&D effort is long-term oriented and aims at creating an open protocol that can be leveraged by app developers, institutions, associations and user communities to create better self-sovereign apps and dApps. However, technical obstacles make this a difficult mission to accomplish, some of the challenges that Linnia is focusing on solving in the futur are:  

1. **Confidentiality challenges: **When sharing data with untrusted data centers for computation purposes, the data must be hidden via encryption in order to maintain confidentiality and preserve user privacy. However, the task of computation on encrypted data creates other issues like the ones specified just below.
2. **Verified computation:  **Verifiable computation is required when dealing with untrusted data centers. A malicious external server is always a risk making the problem of verifying the correctness of computation on data stored on external servers even more difficult to solve.** **
3. **Complexity challenges:  **Previously mentioned protocols, like Homomorphic encryption (HE) solve some confidentiality/privacy issues. However, they suffer from large computational costs. Also, when using protocols like Secret Sharing, the secret needs to be reconstructed by a certain number **t (**security parameter**)** of computation entities and other participants may disappear without compromising data availability. The drawback of this solution is that it needs a large volume of shares (multiplication of the initial data volume by the number of participants). ** **
4. **Scalability challenges:** Ethereum (and many other blockchain based systems today) need validation from all the network participants in order to ensure correctness on every state change. As a result, the computational cost for every state change is considerably high compared with computational cost of a single computer. Additionally, as stated in the verifier's dilemma, it is not possible to increase the number of transactions per second without risking the possibility of inclusion of an invalid transaction inside a block. The Linnia Mesh acts as an external consensus layer, where state changes are only committed to the main consensus computer (Ethereum) as a final adjudication layer, following the direction pointed by protocols like Plasma, Lighting network, or TrueBit. 


The Linnia team (us) has been in contact with the projects cited in this paper and is eager to discuss our ideas with other projects in the Ethereum ecosystem.
We believe that eventually the combination of all Ethereum-based projects, that aims at solving different parts of the same puzzle in different manners, will lead to a successful transition to Web 3.0.

To that end, we encourage you to reach out to us if:

* you are working on a project that will fit with the Linnia protocol (whether a decentralized identity platform, a decentralized application that would benefit from querying aggregate user data, or something entirely different)
* you want to contribute to the Linnia community (through protocol implementation, research, UX, providing feedback on this paper or other involvement)


We have made our resources available on GitHub (our code and papers) and we will continue to do so for each release.

This soft release provides:

* Smart contract for medical patient and medical provider registration (created to illustrate a potential medical use case for Linnia)
* Smart contract for metadata indexing and record attestations
* Smart contract for data permissioning

The first Protocol implementation will be introduced in version 1.0.

You can contact us and get updates on the project through:

* twitter: @LinniaProject
* website: [www.Linnia.com](http://www.linnia.com/) 

* * *


## Sources


[] Social networks (Instgram, Facebook, etc..)
[ ]
[ ]; Keep network https://backend.keep.network/whitepaper
[ ]: Enigma https://www.enigma.co/enigma_full.pdf
[ ]: Swarm http://swarm-guide.readthedocs.io/en/latest/ 
[ ]: IPFS https://github.com/ipfs/ipfs
[ ]: Swarm Whitepapaer http://swarm-gateways.net/b :/theswarm.eth/ethersphere/ orange-papers/ /sw% E .pdf
[ ]: Proof Of Stake https://en.bitcoin.it/wiki/Proof_of_Stake
[ ] :uPort white paper, https://whitepaper.uport.me/uPort_whitepaper_DRAFT .pdf
[ ]: IPLD https://ipld.io/
[ ]: OneName https://onename.com/
[ ]: NameCoin https://namecoin.org/
[ ]: Bitcoin Whitepaper https://bitcoin.org/bitcoin.pdf
[ ]: Web Foundation: https://web .foundation/
[ ]: Ethereum Yellow Paper http://gavwood.com/paper.pdf
[ ]: Bitcoin BIP Protocol https://github.com/bitcoin/bips/blob/master/ bip- .mediawiki
[ ] Orange Paper Swarm http://swarm-gateways.net/b :/theswarm.eth/ethersphere/ orange-papers/ /sw% E .pdf
[ ]: Homomorphic Encryption https://en.wikipedia.org/wiki/Homomorphic_encryption
[ ]: Garbled Circuits https://en.wikipedia.org/wiki/Garbled_circuit
[ ]: Secure MultyParty Computations https://en.wikipedia.org/wiki/ Secure_multi-party_computation
[ ]: Scaling Bitcoin with Secure Hardware http://hackingdistributed.com/ / / / scaling-bitcoin-with-secure-hardware/
[ ]: Private contact discovery for Signal https://signal.org/blog/contact-discovery/
[ ]: Shamir Secret Sharing https://en.wikipedia.org/wiki/Shamir% s_Secret_Sharing
[
