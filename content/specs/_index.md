---
title: "Specifications"
weight: 1
---

## Introduction

So far, this page mainly points to a series of feature proposals / specifications / ideas in the context of my contributions to Secure Scuttlebutt ecosystem.

This is to keep track of various ideas and proposals that I plan to implement in the future as part of the Bundle Feed Protocol project.

The Bundle Feed Protocol is an extension of the Bundle Protocol 7 derived from and compatible with the Secure Scuttlebutt protocol.  The main issue with the Secure Scuttlebutt protocol is that it is not designed to be used as a general purpose protocol for decentralized applications and some initial design decisions make it difficult to evolve without breaking the backward compatibility.  The Bundle Feed Protocol is designed to be used as a general purpose protocol for decentralized applications.  Moreover SSB ecosystem is lacking a easy tu use API to build applications on top of it.  
The current project will implements a new API using the Nim programming language and offer bindings for other languages. The choose of the Nim programming language is due to its simplicity, performance, security and the fact that it is designed for interoperability with other languages.

## Proposed features

### SSB archive

https://github.com/gpicron/ssb-archive

This is the first project that I am implementing actively. While it will be implemented initially for SSB protocol, the principle and the design will be identical in the Bundle Feed Protocol.  The sole difference will be the use of different message formats and that the concept will be extended later to a more generic event sourcing snapshot model to cope with various use cases.

This sub-project is used to implement and demonstrate the capability to build components in Nim that are easy to integrate in other languages.  

Leveraging the SSB BIPF format for implementing the archives bundles that meet more interest from the SSB communnity than the proposed format in initial proposal.  Still some evolution of the BIPF spec is needed to improve https://github.com/ssbc/bipf-spec

Roadmap:

- update the specification with feed backs received from the community and at P2P Basel
- Improve the BIPF spec to support the use case of the SSB archive
- implement the first version of the API using the Nim programming language
- integrate the API in the SSB JS reference implementation and in Manyverse
- integrate the API in the SSB Go reference implementation and in Planetary

### Gossip protocol and Elapsed Time consensus

https://github.com/gpicron/ssb-clock-spec

This is a specification for a gossip data distribution protocol. It will derive to a mechanism allowing to establish local consensuses of Elapsed Time.

### Various ideas

- https://github.com/gpicron/ssb-code-of-conduct
- https://github.com/ssbc/ssb2-discussion-forum/issues/17
- https://github.com/ssbc/ssb2-discussion-forum/issues/16






