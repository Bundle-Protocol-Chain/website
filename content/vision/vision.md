---
title: "Our Vision"
weight: 1
---
<!--
 Copyright 2023 gpicron
 
 Licensed under the Apache License, Version 2.0 (the "License");
 you may not use this file except in compliance with the License.
 You may obtain a copy of the License at
 
     http://www.apache.org/licenses/LICENSE-2.0
 
 Unless required by applicable law or agreed to in writing, software
 distributed under the License is distributed on an "AS IS" BASIS,
 WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 See the License for the specific language governing permissions and
 limitations under the License.
-->


The purpose of this document is to describe the Bundle Feed Protocol and the applications that can be built on top of it. The network is designed to address the challenges and limitations of centralized services, such as lack of control over personal data and privacy concerns, by providing users with a decentralized, secure and private alternative. We will explain the main concepts and ideas behind the project, its key features and the benefits it can provide to users.

It will also present the technologies used in the project and their advantages, such as P2P distribution, blockchain technology and Scuttlebutt protocol. Furthermore, it will describe the use cases and applications that can be built on this network, covering a wide range of services such as social media, messaging, development platforms, marketplaces, digital currencies, and identity management. Lastly, it will provide an overview of the technical details and implementation considerations, such as security, scalability, and user experience.
## Detailed description of the project

### Network architecture

#### From the blockchain technologies
The Bundle Feed Protocol is based on a P2P data distribution model, where each node owns its data and share it with other nodes. The BPFeed is not a blockchain but  incorporates some blockchain technology in order to ensure the integrity and security of data.

Blockchain technology is a (semi-)decentralized way of storing data in a chain of blocks, where each block contains a number of transactions. The blocks are linked together in a chronological order, creating a chain of blocks, known as the blockchain.

The main principle of blockchain technology is that once a block is added to the chain, it cannot be altered or deleted, creating an immutable record of all transactions. This ensures that data stored on the blockchain is secure and tamper-proof. In order for a new block to be added to the chain, the network participants need to reach a consensus on the new block's validity, this process is known as consensus mechanism. There are different types of consensus mechanisms, the most popular one being the proof of work.

The benefits of blockchain technology include security, transparency, and decentralization. However, it also has some drawbacks, such as low transaction speeds, high energy consumption, and in practice, there is some degree of partial centralization due to the consensus protocols, which implies that only those with the means to put in place powerful infrastructure have significant control over the consensus.

Overall, the Bundle Feed Protocol incorporates some blockchain algorithms to ensure the integrity and security of data, while also addressing potential drawbacks through the use of alternative consensus mechanisms and P2P distribution.

#### From the P2P Secure Scuttlebutt protocol

Secure Scuttlebutt (SSB) is a decentralized, peer-to-peer protocol that allows users to share information and interact with each other in a secure and private way. SSB utilizes a concept of a "feed", which is similar to a blockchain in that it is a chronological sequence of records shared and replicated between peers. However, unlike blockchains, SSB does not rely on a global consensus mechanism and is designed to work in an offline-first environment.

In SSB, each user has a unique feed per device that is identified by a public cryptographic identifier key. This key is not linked to a device or a person, ensuring the anonymity of the user.  Users do not need to provides any information to anybody to get an identifier, they generate it themself.

Users can follow each other's feeds, and when they do, they receive a copy of that feed's data. The feed data is replicated between peers using a gossip protocol, which ensures that the data is distributed to interested users and that authenticity and integrity of the data is verified by as many peers as possible. This replication process is based on the concepts of following and blocking commitments. When a user follows another user's feed, they publicly inform their followers of their interests and make a commitment to accept and replicate that feed's data. When a user blocks another user's feed, they make a commitment to not accept or replicate that feed's data.

There are 2 optionals components of the network that improves its usability and resiliency: the pub servers and the room servers.

Users do not need to connect to a Pub server to use SSB, but they can choose to connect to existing ones run by other community members or even run their Pub server for their private community. Pub servers are optional components of the SSB network that allow users to share their feeds with others and make them discoverable by others even when they are offline. They act as a relay for the gossip protocol and help to distribute the data across the network more efficiently. However, running a Pub server is not a requirement for using SSB, and users can still participate in the network without running one or connecting to one.

Additionally, Users can also use Room servers to create and manage virtual rooms for group communication. Room servers allow users of a community to know who of that community is currently online and facilitates direct communication between them, increasing the anonymity of communication by allowing users to establish direct connections without intermediaries. Room servers also allow to create some tunnel between peers which allows a even higher degree of anonymisation and to bypass firewalls controls sometime preventing them to connect directly to each others.

The benefits of SSB include its offline-first approach, which allows users to continue to access and share data even when they are not connected to the internet. Additionally, the gossip protocol ensures that data is replicated and verified in a decentralized and efficient way, providing high levels of security and privacy. Additionally, SSB's lack of reliance on a global consensus mechanism makes it less resource-intensive than other secure decentralized protocols.

However, SSB also has some drawbacks. One of the main drawback is that SSB users are responsible for replicating the data of the feeds of the users they follow and the feeds of the users their directly followed users follow. This principle, also known as "The friend of my friend is my friend," helps to make data replication efficient and allows users to form subjective communities around them that collaborate to distribute their content. However, this principle also presents a drawback, as users are required to keep a complete sequence of records of the replicated feeds on their device storage in order to prove their integrity during propagation. This can lead to a significant amount of data storage being taken up by old and potentially unnecessary records, which can be a challenge for users and limit the scalability of the network for some use cases.

Additionally, SSB can be more complex to use and understand than some other decentralized protocols. Users need to run a Pub server to allow others to connect to their feed and replicate their data, and also Room servers can be used to create and manage virtual rooms for group communication. Room servers allow users to know who of a community is currently online and facilitates direct communication between them, increasing the anonymity of communication by allowing users to establish direct connections without intermediaries.

Overall, Secure Scuttlebutt (SSB) is a decentralized, peer-to-peer protocol that offers a variety of excellent features that benefit end-users. Its offline-first approach, decentralized replication, and strong emphasis on security and privacy make it a powerful solution for a variety of use cases. Additionally, SSB's ability to work securely without relying on any provider or centralized authority makes it a highly resilient and adaptable technology. It can work on any type of numeric communication channels, such as USB keys, opportunistic phone-to-phone connections, and even low-power wide-area networks (LoRaWAN).

However, SSB's focus on privacy and security also reduces its value for today's business model that rely on personal data collection and vendor lock-in. This means that the development community has limited funding and the system evolves slowly. Despite this, the network architecture of BPFeed is mainly based on SSB, and if possible, some sort of backward compatibility will be maintained to keep the historical users and developers of SSB on board of this adventure. This will allow for a seamless transition for those already familiar with SSB, while also allowing for new users and developers to benefit from the enhanced features and capabilities offered by BPFeed. This strategy will help in leveraging the strengths of SSB while addressing its limitations, and will allow to grow the user and developer base while keeping the SSB community on board of this adventure.

#### Fediverse/AcitvityPub, Mastodon, PeerTube etc.
Fediverse/ActivityPub, Mastodon, PeerTube, etc are all examples of decentralized, open-source social media platforms that are built on top of the ActivityPub protocol. This protocol allows for the creation of decentralized social networks, where users can communicate and share content with each other without relying on a central authority.

One of the key features of these platforms is the ability for users to interact with each other across different instances, or separate instances of the platform that are run by different organizations or individuals. This allows for a more decentralized and open ecosystem, where users have more control over their data and privacy.

ActivityPub allows for the decentralized distribution of content between instances. When a user posts content on their instance, it is distributed to other instances where the user's followers are located. This allows for a more decentralized and open ecosystem, where users can communicate and share content with each other across different instances without relying on a central authority or intermediary.

Benefits of ActivityPub includes the ability to have a decentralized social network where users can communicate and share content with each other without relying on a central authority or intermediary. Additionally, it allows for a more open and decentralized ecosystem, where users have more control over their data and privacy.

One of the main drawbacks of ActivityPub is that it may be more complex to use and understand than centralized social media platforms, while still being simpler than SSB. Additionally, while the platform is decentralized, the individual instances are still run by administrators who have the power to block accounts or content, and there is not verifiable transparency or "democracy" on how these decisions are made. Users also depend on the availability of the instances they choose to use, and there have been scalability concerns with this model during large migrations of users.

Overall, the functioning of the fediverse is not very different that the good old emails servers with the same drawbacks.

In the network of BPFeed, SuperNodes are special nodes that aim to offer the best of both worlds: the security and privacy of SSB and the ease of use of ActivityPub instances. They serve as both Pub servers and Room servers, and also act as archivers by maintaining a full copy of the replicated feeds of the registered users. These SuperNodes also offer query services on the content that is replicated, which allows client apps of the registered users to keep a copy of only the recent and relevant data, while still being able to search for older content.

SuperNodes are not essential for the network to function, and they do not have the power to corrupt or control the network. Even if an entity were to create an enormous number of SuperNodes, it would not be able to prevent the network from functioning or corrupt it in any way. They exist solely to improve the distribution of data, optimize the overall management of resources, and make it easier for users to access the network via lightweight clients such as smartphones or web browsers.

SuperNodes in the network collaborate with each other to optimize the speed and energy cost of data distribution throughout the network. Anyone can deploy and manage a SuperNode, and it may be beneficial for a family or a business to have a small SuperNode running on a raspberry pi at home, similar to a router. Additionally, deploying and managing one or more SuperNodes with high availability can be a business in itself, with the service offered for a fee.
#### Elasped time global consensus
Elapsed time global consensus is a built-in key feature of the network of BPFeed that enables the creation of highly reliable and efficient decentralized applications. Unlike other decentralized protocols, such as blockchain-based systems, this feature does not require a global consensus mechanism to function and instead relies on the collaboration of users to verify the validity of data.

This makes it highly resource-efficient and sustainable, as it does not require a large amount of computational power to maintain.

Examples of applications that could benefit from this feature include supply chain management, where the chronological order of events is crucial for tracking the movement of goods and ensuring the integrity of the supply chain. Another example is voting systems, where the elapsed time consensus can be used to verify the validity of votes and prevent any attempts at voter fraud.

In financial transactions, elapsed time consensus can be used to verify the validity of transactions, making it useful for banking and other business applications.

In comparison to other alternatives available today, such as blockchain-based systems, elapsed time global consensus offers a more sustainable and resource-efficient solution. Blockchain-based systems require a significant amount of computational power and energy to maintain, which is not only costly but also unsustainable. In contrast, elapsed time global consensus only requires the collaboration of users and does not require a large amount of computational power, making it a more sustainable and cost-effective solution for decentralized applications.

In summary, the elapsed time consensus feature of the network of BPFeed enables the creation of highly reliable and efficient decentralized applications, while maintaining a high level of security and privacy for users. It is a highly resource-efficient and sustainable alternative to traditional blockchain-based systems, making it an ideal solution for a wide range of applications, such as supply chain management, voting systems, and financial transactions.
### User control and privacy
In the network of BPFeed, users have full control over their identities and can choose to block or follow other identities for their own reasons. This allows for a high level of privacy and control over one's personal information.
The anonymity of identities on the network makes it difficult to link an identity to a specific person or their personal data. This, combined with the user's control over the information they share, allows for a high level of privacy and security.

One key feature of the network is the ability for users to obfuscate their followings by designating a set of random identities that contains the identity they wish to follow. This allows the user to control how much information they reveal about their followings to others on the network. Additionally, users can choose to ignore and not replicate data from certain feeds without restricting their propagation to their community.

The network also allows for decentralized identity management, where users can create and manage their own identities in a verifiable and secure way. This allows for the creation of community identities and sharing of personal information with designated individuals within those communities.

Decentralized identity management is a concept that allows individuals to have full control and ownership over their own digital identity and personal information. This means that users have the ability to create, manage, and control multiple identities within the network, and can choose to share certain personal information with specific individuals or groups.

Unlike centralized identity management systems, where a single entity controls and manages the identities of users, decentralized systems are distributed among multiple nodes and users. This means that there is no central point of failure and users have more control over their own data.

In the context of the network of BPFeed, decentralized identity management allows users to create a verifiable community identity within the network, while maintaining anonymity and privacy. This means that users can share certain personal information with some members of their community, while keeping their personal information private from the rest of the network.

This feature allows for a wide range of use cases, such as creating verifiable and trustworthy online identities, facilitating secure transactions and data sharing, and enabling secure communication and collaboration within a community. Overall, decentralized identity management empowers users to have more control over their online identities, and allows for a more secure and private online experience. 

Overall, the network of BPFeed allows for a high degree of user control and privacy, with features such as obfuscation of followings, decentralized identity management, and anonymity of identities. This allows for a more secure and private digital experience for users.
### Key features of the network
1. **Decentralized architecture and protocols**, such as SSB and ActivityPub, that allow for a more open and secure ecosystem where users have control over their data and privacy.
2. **Elapsed time global consensus**, which enables users to verify the validity of events based on the time since they occurred, ensuring data integrity and preventing false data attacks.
3. **User control and privacy**, where users have full control over their identities and can choose to block or follow other identities while remaining anonymous.
4. **Supernodes**: These nodes act as Pub servers and Room servers for SSB, maintaining full copies of replicated feeds and providing query services for archived content. This improves data distribution and resource management within the network. Supernodes can be run by anyone, whether for personal or business use, and they provide an easy entry point for users to start using the network and applications running on it. Additionally, the network does not rely on the presence of Supernodes to function, it can work even without internet and using alternative communication channels and opportunistic data transfer, providing a high level of resiliency and accessibility.
5. **Decentralized identity management**: The network allows for the creation of decentralized identity management applications, where users can create verifiable community identities and share personal information with designated individuals.
6. **High resource-efficiency**: The network is highly resource-efficient and does not require global consensus to function, making it more sustainable compared to other alternatives.
7. **Resilience**: The network designed to be highly resilient and does not rely on a central authority or intermediary to function. It can continue to operate even in the absence of internet connectivity, by using alternative communication channels and opportunistic data transfer. This is achieved through the use of peer-to-peer protocols and the decentralized architecture of the network. Supernodes, while helpful for improving data distribution and resource management, are not necessary for the network to function. This means that even if a large number of supernodes were to become unavailable, the network would still be able to operate and ensure data integrity for its users. This feature makes it highly suitable for use in areas with poor or unreliable internet connectivity.
8. **Interoperability**: The network allows for interoperability with other protocols such as ActivityPub, which allows for communication and content sharing across different instances and platforms.
# Current Challenges and Limitations
## Analysis of the challenges and limitations of centralized or semi-centralized services
### Data privacy
Data privacy is a major concern for users of centralized or semi-centralized social media platforms. These platforms often collect and share personal data with third parties for advertising or other purposes, without the user's knowledge or consent.

The network of BPFeed addresses this issue by providing a decentralized architecture and protocols, such as SSB and ActivityPub, that allow for a more open and secure ecosystem where users have control over their data and privacy. With the use of decentralized identity management, users can create verifiable community identities and share personal information with designated individuals, rather than having their data collected and shared without their consent.

In addition, the elapsed time global consensus mechanism ensures the integrity of data on the network and prevents false data attacks, further protecting user's personal information.

Overall, the network of BPFeed prioritizes user privacy by giving them control over their personal data and ensuring it is protected from unauthorized access or sharing.
### Data security
Data security is another major challenge with centralized and semi-centralized services. With a centralized architecture, all data is stored on a single server or a small number of servers, making it a prime target for hackers and cyber attacks. Even Blockchains are exposed to some sort attacks related to the facts a relatively limited set of servers maintain the all history of the network and that one that could achieve to create and/or control a sufficiencitly large number may disturb the network or even rewrite the history. Additionally, centralized services often rely on third-party providers for security measures, which can be vulnerable to breaches and other security issues.

The network of BPFeed addresses these challenges by its decentralized architecture which allows for the distribution of data across all the nodes in the network, including end-users, making it much more difficult for hackers to target and compromise the entire system. Additionally, the network utilizes state-of-the-art encryption and security protocols to ensure the protection of personal data and is designed to evolve as those will be subject to be broken (thing about quantum computers that are yet know to be able to break RSA protocol in minutes when they will become a reality).

Furthermore, the use of supernodes in the network allows for the creation of multiple entry points for users to access the network, reducing the risk of a single point of failure. The network also allows for the use of alternative communication channels, such as Bluetooth or LoRaWAN, which can provide additional security and privacy measures in the event of a loss of internet connectivity.

In summary, the network of BPFeed addresses the challenges of data security by its decentralized architecture, use of cutting-edge encryption and security protocols, and the use of supernodes and alternative communication channels. These measures provide a robust and secure platform for users to share and access information. It also provides a more resilient network that can continue to operate even in the event of a loss of internet connectivity. The network is designed to be adaptable to new security challenges as they arise, making it a secure and reliable option for users concerned about the security of their personal data.

### Centralized Services
Centralized services, such as traditional social media platforms and online marketplaces, have become ubiquitous in our daily lives. These services offer convenience and ease of use, but they also come with significant limitations and challenges.

One of the main challenges with centralized services is the lack of control and ownership over personal data. Users are often required to give up their personal information, including their browsing history, location data, and other sensitive information, in exchange for access to the service. This information is then collected, analyzed, and used by the central authority for various purposes, such as targeted advertising and data mining.

Another major challenge with centralized services is the lack of data security and privacy. As all the data is stored on a single server or a small number of servers, it is vulnerable to hacking and cyber attacks. Additionally, centralized services often rely on third-party providers for security measures, which can be compromised.

Blockchain technologies, while decentralized, also present limitations in terms of user control and privacy. Transactions on a blockchain are recorded on a public ledger, and while user identities may be pseudonymous, they can still be linked to real-world identities through various means such as IP tracking. Additionally, the use of smart contracts and decentralized applications on a blockchain can still result in the collection and analysis of personal data by the developers or operators of those applications.

Furthermore, the fact that blockchain technologies are de facto more or less centralized due to large investment needed to setup profitable nodes, it doesn't solve the issue of centralization, it just shift it to another point.

In summary, while centralized services and blockchain technologies offer some level of decentralization, they still come with limitations and challenges in terms of user control and privacy, and data security and ownership.

Centralized services, such as traditional social media platforms, are often plagued by scalability issues. As the number of users and amount of data increase, these platforms are often unable to handle the load and may experience slowdowns or crashes. Additionally, centralized services typically require large amounts of energy to run and maintain, leading to a significant environmental impact.

Blockchain technologies, while decentralized in terms of their architecture, also suffer from scalability issues due to their consensus mechanism and the high computational power required for mining. The environmental impact of blockchains is also significant, as the energy consumption required for mining has been shown to be substantial. While some blockchain projects have implemented solutions that try to address these issues, such as proof-of-stake consensus mechanisms, they are still a concern for the long-term sustainability of the technology and their actual degree of centralization.
### Federated Services
Federated services, such as ActivityPub, offer a more decentralized approach compared to centralized services, but still retain a level of centralization as the majority of control is held by the administrators of the instances. These instances are essentially separate networks that communicate with each other, but the owners of the instances have the ability to control what content and users are allowed on their network. This can lead to a lack of user control and censorship concerns, as users may be limited in what they can see and publish based on the policies of the instance they are registered on. Additionally, personal data stored on these instances may be at risk of being mishandled or misused by the administrators.

Despite these limitations, federated services do offer some benefits such as a decentralized user base and the ability for users to move between instances. However, it is important to note that the level of decentralization can vary greatly between instances and ultimately, the level of control and privacy protection is determined by the policies and actions of the instance administrators.

Furthermore, Federated services also suffer from scalability issues, and the fact that a large number of instances are required to form a truly decentralized network. This results in a large number of servers, which increases the environmental impact of the network.

In summary, while federated services offer a more decentralized approach compared to centralized services, they still retain a level of centralization and can suffer from issues related to user control, censorship, data privacy and scalability.
### The Network of BPFeed
#### Data privacy and security
The Network of BPFeed addresses the challenges of data privacy and security by its decentralized architecture and protocols, such as SSB and ActivityPub. This allows for a more open and secure ecosystem where users have control over their data and privacy.
By distributing data across all the nodes in the network, including end-users, it becomes much more difficult for hackers to target and compromise the entire system. Additionally, the network utilizes state-of-the-art encryption and security protocols to ensure the protection of personal data.
Furthermore, users have full control over their identities and can choose to block or follow other identities while remaining anonymous. This allows for a higher level of privacy and control over personal data.
Decentralized identity management is also possible on the network, where users can create verifiable community identities and share personal information with designated individuals. This allows for a more secure and private way to manage personal information.
In summary, The Network of BPFeed addresses the challenges of data privacy and security through its decentralized architecture, use of cutting-edge encryption and security protocols, and the ability for users to have full control over their identities and personal information.
#### Control over personal data
The Network of BPFeed addresses the issue of control over personal data in both centralized and federated services. In centralized services, all data is controlled by a single entity, giving them complete control over the data and how it is used. This lack of control by the users can lead to privacy violations, data breaches, and other security issues. Federated services, while offering more control than centralized services, still rely on the control of the instance owner, who has the power to block or censor content, and access or use personal data.

Censorship is another major challenge with centralized and semi-centralized services, as the centralized authority or administrator has the power to control and limit the information and content that is shared and accessed on the platform. This can lead to a lack of diversity in viewpoints and can stifle free speech. Federated services based on protocols like ActivityPub also have this weakness as the instances administrators can also decide what its users can see or not, publish or not, based on their personal criteria.

The network of BPFeed addresses these challenges by its decentralized architecture, which promotes the distribution of data and control over the network to all its users. The use of supernodes and alternative communication channels, such as Bluetooth or LoRaWAN, also provide multiple entry points for users to access the network, making it much more difficult for any one entity to control or censor the information being shared. Additionally, the network utilizes state-of-the-art encryption and security protocols to ensure the protection of personal data and the freedom of speech. In this way, the network of BPFeed provides a robust and secure platform for users to share and access information without the fear of censorship.

The Network of BPFeed, through its decentralized architecture and protocols, gives users complete control over their data and identities. Users can choose to block or follow other identities, and decide who they share their personal data with.

Furthermore, the use of cutting-edge encryption and security protocols ensures the protection of personal data and the network is designed to evolve as technology advances. The use of alternative communication channels, such as Bluetooth or LoRaWAN, can provide additional security and privacy measures in the event of a loss of internet connectivity.

In summary, the Network of BPFeed addresses the issue of control over personal data by giving users complete control over their data and identities, providing multiple entry points for access, and utilizing state-of-the-art encryption and security protocols, making it a robust and secure platform for users to share and access information.
The network of BPFeed also addresses the scalability and environmental issues of both centralized and federated services by its offline-first nature. This allows for the network to operate in areas with limited or intermittent internet connectivity, reducing the energy consumption required to maintain a constant connection. Additionally, the decentralized architecture and use of supernodes allows for the distribution of data and processing power, reducing the energy consumption required to maintain and update the network. Furthermore, by allowing the network to operate on intermittent energy sources, such as solar or wind power, it reduces the environmental impact of the network compared to centralized or semi-centralized services and and making it more sustainable in the long-term..

In summary, the network of BPFeed addresses scalability and environmental issues by its offline-first nature, decentralized architecture, and the use of supernodes and intermittent energy sources. These measures provide a sustainable and eco-friendly platform for users to share and access information.

The Network of BPFeed addresses the scalability issues of both centralized and federated services by utilizing a decentralized architecture and protocols dervied from SSB. This allows for a distributed network where data is stored across all nodes, including end-users, reducing the load on a single server or a small group of servers. This not only improves the scalability of the network, but also increases its resiliency as there is no single point of failure.

Additionally, the use of supernodes in the network allows for improved data distribution and resource management, allowing for a more efficient use of resources. Supernodes also act as entry points for users to access the network, reducing the risk of a single point of failure and increasing the overall scalability of the network.

Another challenge with centralized and federated services is limited innovation. With centralized services, all decision making and control over the network lies in the hands of a single entity or a small group of entities. This can stifle innovation and limit the potential for new and exciting applications to be developed on the network.

The Network of BPFeed addresses this challenge by its truly decentralized nature and the use of open-source protocols such as SSB. The network is open to contributions and developments from anyone, allowing for a wider range of ideas and perspectives to be brought to the table. It is designed to reduce the risk of stifled innovation and to activelly promote experimentation.

Overall, the network of BPFeed promotes an environment of open innovation, encouraging the development of new and exciting applications.
# Use Cases and Applications
## Distributed Identity management
Decentralized Identity Management (DID) is a type of digital identity management system that is based on blockchain or distributed ledger technology. It allows individuals or organizations to have control over their own digital identities, rather than relying on centralized organizations to manage them. This includes the ability to create, update, and revoke digital identities without the need for a central authority.

DID standards are a set of technical specifications that define how DIDs should be created, managed, and used. They include specifications for data formats, protocols, and APIs. Some examples of DID standards include the W3C's DID specification and the Decentralized Identity Foundation's (DIF) DID specifications.

DID can also be connected to Verifiable Credentials (VC) which are digital representations of claims made about an individual or organization by a trusted third party. Verifiable Credentials can be used to verify an individual's identity, age, qualifications, and more.

DID can be used in various use-cases such as identity verification, access control, and secure sharing of personal information. It can also be used to create self-sovereign identity systems that allow individuals to have more control over their personal data and how it is used.

The Distributed Identity Management app is creating a self-sovereign identity system on top of the network of BPFeed. It allows users to create, manage and control their own identities, and share verifiable information with other users.

This is made possible by using Decentralized Identifiers (DIDs) as the foundation of the system. DIDs are unique identifiers that are created and controlled by the user, rather than a centralized authority. They are a key component of the W3C's Decentralized Identity Management standards and are designed to be interoperable with other systems and blockchains.

With the Distributed Identity Management app, users can create multiple identities for different purposes and contexts, such as personal, professional, or community-based identities. They can also link these identities to existing social media accounts or other online identities, providing a unified view of their digital identity.

The app also allows users to share verifiable information, such as qualifications, certifications, and other credentials, with other users in the network. This can be done through the use of Verifiable Credentials, which are digital representations of information that can be independently verified by other users.

In addition to providing users with control over their own identities and information, the Distributed Identity Management app also offers significant benefits for businesses and organizations. It allows them to verify the identities of their customers and partners in a secure and decentralized way, while also reducing the need for costly and time-consuming identity verification processes.

A self-sovereign identity system is based on the idea that individuals should have control over their own personal data and identities, rather than relying on centralized authorities to manage and verify their identities. The W3C's Decentralized Identity (DID) standard is a key component of this system, as it allows for the creation of unique and verifiable digital identities that are anchored to the blockchain.

A self-sovereign identity system is composed of several key components that interact to build trust. These include:
1. Identifiers: Unique identifiers, such as DIDs (Decentralized Identifiers) as specified by the W3C, are used to identify entities within the system. The feed identifiers in our network are compliant with the W3C standard.
2. Claims: Claims are statements about an entity, such as their name or age, that are made by other entities within the system. These claims are cryptographically signed and can be used to build trust.
3. Verifiable Credentials: Verifiable Credentials are a collection of claims that are cryptographically signed by an issuer and can be used to prove the authenticity of an entity's claims.
4. Trust Anchors: Trust Anchors are entities within the system that are trusted to verify the authenticity of claims and credentials.
5. DID Resolution: DID Resolution is the process by which a DID is mapped to a location where the corresponding public key and other information can be found, allowing entities to verify the authenticity of claims and credentials.

In a self-sovereign identity system, users have control over their own identities and can choose which other entities they trust to verify their claims and credentials. This creates a web of trust where each user is its own authority and decide which other authorities to trust and to what extent.

This approach allows for a more decentralized and secure identity management system compared to traditional hierarchical PKI systems.
The Distributed Identity Management app on the network of BPFeed aims to create a self-sovereign identity system for users, where they have full control over their personal data and identities. Unlike traditional centralized systems, or even federated systems, the network utilizes a web of trust where each user is an authority and can choose which authorities they trust.
When a user invokes a service, the app will attempt to find a path through the web of trust to establish a sufficient level of confidence between the two parties. This allows for a more open and secure ecosystem, where users can share personal information with designated individuals and organizations, while remaining anonymous to those they choose not to share with.
The app also provides a variety of services such as Identification, Authentication, Confirmation, Qualified Electronic Signature, and more. These services are designed to make the user's experience convenient and secure, while also providing businesses and legal authorities with a way to verify users' identities.
Overall, the Distributed Identity Management app on the network of BPFeed provides users with a way to take control of their personal data, identities, and the trust relationships they establish, while also addressing the challenges and limitations present in traditional centralized and federated systems.

The Distributed Identity Management app on the Network of BPFeed provides several benefits for different groups of users.
For end-users, the app offers a self-sovereign identity system where they have full control over their personal data and can choose who they trust to manage and verify their identity. This eliminates the need for a centralized authority, such as a government or corporation, to hold and manage personal data. The app also offers a convenient and secure way for users to identify themselves using an international NFC ID document, such as a passport or driving license.
For organizations, the app provides a way to easily verify the identity of their customers, partners and employees without relying on a central authority. This can improve the efficiency of various processes such as onboarding, transactions and document signing. It also increases the security of these processes by using a web of trust to establish trust levels instead of a centralized trust anchor.
For legal authorities, the app provides a secure and verifiable way to confirm the identity of individuals, which can be useful in various legal processes such as voting and court proceedings. It also provides a way to validate the authenticity of documents and signatures, which can be used to improve the efficiency of legal processes.
Overall, the Distributed Identity Management app on the Network of BPFeed provides a more secure, efficient and decentralized way to manage and verify identity, which can benefit all parties involved.

## Social media
TODO
    * Messaging and micro-blogging
        * Allow public posting
        * Allow private groups micro-blogging
        * Allow private encrypted messaging end to end to individuals and groups
        * Trust enabled by Distributed Identity
            * Certified identities (subjective because this is only if the user tells the app that he trust some authority that he will trust the cerficates emitted by this authority)
            * Allows for instance Parent Control on minimum requirements to allow their childs to connect to unknown peoples and see content from others.
        * Can allow entreprises to implements secure professional messagings and collaboration tools with complex access control but off-line caps without depending on a centralised service/vendor locking solution/e.

## Development platforms
TODO

## Marketplaces
TODO

## Digital currencies
TODO

# Technical Details and Implementation Considerations
* Security and privacy concerns
    * Data encryption
    * Access control
    * Network security
* Scalability
    * Network topology
    * Data storage
* User experience
    * User interface
    * Interoperability
# Conclusion
* Summary of the key takeaways
* Next steps for the project
* Call to action for feedback and participation
# Feedback, questions and next steps

