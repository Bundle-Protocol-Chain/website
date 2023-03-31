---
title: "The Genesis..."
weight: 1
---

# The Genesis of the project

The main concepts and ideas behind the project are centered around providing users with a decentralized, secure and private alternative to centralized services. By utilizing the best algorithms and ideas coming from blockchain technology, Secure Scuttlebutt, IPFS, and Fediverse/Mastodon technologies, the Bundle Feed Protocol (BPFeed) aims to empower users by giving them control over their personal data and privacy.

The BPFeed aims to be a decentralized protocol for various applications, where users can interact with each other without relying on a central authority. This will enable users to communicate, share and transact with each other without the need of intermediaries, providing a more secure, private, and efficient way of doing so.

The project also puts a strong emphasis on scalability, security, and user experience. This will be achieved through a combination of various technologies, such as data encryption, access control, network security, and user-friendly interfaces.

Furthermore, the project aims to create an ecosystem of various applications, which will be built on top of the Bundle Feed Protocol, providing users with a wide range of services such as social media, messaging, development platforms, marketplaces, digital currencies, and identity management.

The project is based on the philosophy of creating Commons, where the technology is available to all to build new applications, similar to how HTTP, HTML, and CSS are available to all today. The goal is to foster collaboration between all parties, and to create a decentralized network that is open and accessible to everyone. The project gouvernance will be based on principles of Holocracy and Sociocracy, and will be adapted as needed to fit the purpose and scale of the organization.

Overall, the main concepts and ideas behind the project are centered around creating a decentralized network that empowers users by giving them control over their personal data and privacy, providing a secure and private alternative to centralized services, and enabling the creation of a wide range of services and applications, while being inspired by the latest technologies such as Secure Scuttlebutt and fostering a culture of collaboration, openness, and accessibility.

**Why restarting from scratch and not evolving Secure Scuttlebutt ?**

In the vast and ever-evolving world of the internet, I see the SSB protocol as an unidentified flying object (UFO). It's different from centralized social networks and has the potential to be a game-changer, forming the foundation of a "new HTTP."

Socially, I find SSB to be a "slow food" alternative to the "fast food" social networks like Facebook and Twitter. It encourages deeper connections and more meaningful interactions between users. However, I've noticed that currently, SSB can be challenging for non-technical users to adopt. The current community of SSB users can be difficult to reach, and newcomers who aren't tech-savvy may struggle to find support.

Despite these challenges, I believe that the SSB protocol has reached the minimum viable product (MVP) level technologically, and it offers many capabilities that allow for experimentation and testing. However, it still falls short in terms of energy efficiency and ease of adoption for new developers.

To address these issues, I propose building on the existing SSB protocol with an established standard like BP7. This will enable us to create a new API that is user-friendly and accessible to developers while allowing the protocol to evolve without breaking backward compatibility.

In conclusion, SSB is a fascinating and innovative technology that has the potential to revolutionize the way we connect and interact online. With the right approach, I believe we can overcome the challenges and make SSB accessible to a wider audience, creating a more inclusive and meaningful online community.

**Why not using IPFS and LibP2P ?**

Because IPFS and LibP2P are designed to operate on top of an IP network, they may not be able to adapt well to disconnected environments. They assume that IP connectivity is available everywhere, which is not always the case. On the other hand, BP7 assumes unreliable connectivity and can adapt to any communication channel, making BPFeed more efficient, scalable, and unstoppable.

While IPFS and LibP2P have provided guidance on building similar projects and establishing new standards, the API model needs to be easy to learn and portable, and the protocol should be implemented in every supported language. I chose to implement BPFeed in Nim because it's easy to learn and most of the code produced will run on various devices, including microcontroller devices, browsers, mobile devices, and large computers. Nim is also a language that can easily interoperate with other languages, making it possible to expose the APIs to those languages without significant overhead.

**Why not using the Fediverse ?**

While the activity stream protocol offers a robust vocabulary, it lacks efficiency and scalability. In comparison, the pull gossip mechanism of SSB is more efficient and scalable. By basing BPFeed on the established standard BP7, we can abstract the data distribution model and offer a choice between the two models and many others, including those used by the Fediverse.

BPFeed can provide a stack that improves the activity stream implementation and supports Fediverse initiatives while offering a more efficient and scalable solution. By leveraging the advantages of BP7 and the pull gossip mechanism, BPFeed can offer a better alternative to the activity stream protocol and improve the overall performance of the Fediverse.

[The long version](vision)