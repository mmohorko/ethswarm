+++
authors = []
date = 2020-07-05T22:00:00Z
draft = true
excerpt = "It is here! After months of relentless developments on June 29 we proudly released the alpha version of Swarm’s new Bee client."
hero = "/images/0-at6ksupodifghfhk.png"
timeToRead = 10
title = "Monthly Development Update — June 2020"

+++
###### It is here! After months of relentless developments on June 29 we proudly released the alpha version of Swarm’s new Bee client.
<br>
We marked this long-awaited milestone, that brings us one step closer to a fully working Swarm ecosystem, [with an online event](https://www.youtube.com/watch?v=BHDfzzWVVK0&list=PL6fQnFAjtuY9TfTMm5GYqgscQ_6a7LE8A) that featured some of the best minds in the Ethereum and wider blockchain space. 

In the event we showcased how developers can become part of the Swarm ecosystem and start using [our client](https://swarm-gateways.net/bzz:/docs.swarm.eth/) to build a different breed of software. Software that is rooted in an immutable, decentralized and censorship-resistant data storage and that can bring forth real digital sovereignty. For the really enthusiastic ones we have also [prepared grants](https://swarmgrants.typeform.com/to/SbrJiiiL) so keep reading if you want to learn more.

**Core Track**

* Bee version [0.1.0](https://github.com/ethersphere/bee/releases/tag/v0.1.0) released
* Implement [file](https://github.com/ethersphere/bee/pull/266) [upload](https://github.com/ethersphere/bee/pull/306) with [file entry](https://github.com/ethersphere/bee/pull/242) containing meta information in HTTP API
* Implemented [pull syncing](https://github.com/ethersphere/bee/pull/254)
* Improved the retrieval protocol with [retries to different peers](https://github.com/ethersphere/bee/pull/338)
* Implemented [copy on write](https://github.com/ethersphere/bee/pull/350) in Kademlia PSlice structure
* Implemented [recursive DNS discovery](https://github.com/ethersphere/bee/pull/276) and setting the [public bootnodes DNS address](https://github.com/ethersphere/bee/pull/315) as default
* Improved Kademlia [saturation function](https://github.com/ethersphere/bee/pull/374) and [many](https://github.com/ethersphere/bee/pull/384) [other](https://github.com/ethersphere/bee/pull/364) [Kademlia](https://github.com/ethersphere/bee/pull/356)[improvements](https://github.com/ethersphere/bee/pull/353) in [various](https://github.com/ethersphere/bee/pull/352) [places](https://github.com/ethersphere/bee/pull/232)
* Added a [welcome message](https://github.com/ethersphere/bee/pull/312) to the handshake protocol to greet a newly connected nodes with specific log messages
* Added [DB capacity flag](https://github.com/ethersphere/bee/pull/250)
* Cleaned up the HTTP API which now include /chunks, /bytes and /files endpoints
* Added [optional CORS headers](https://github.com/ethersphere/bee/pull/358) to HTTP API
* Added [OpenAPI specifications](https://github.com/ethersphere/bee/pull/289) for bee APIs
* Improved the handshake protocol [underlay address discoverability](https://github.com/ethersphere/bee/pull/257)
* Implemented [signed Bzz address in Hive](https://github.com/ethersphere/bee/pull/227)
* Allow setting a [static NAT address](https://github.com/ethersphere/bee/pull/311) with configuration options
* [Clean addressbook](https://github.com/ethersphere/bee/pull/309) after failed connection attempts
* Improve the bee Node [service shutdown](https://github.com/ethersphere/bee/pull/287)
* A lot of smaller but significant connectivity improvements in libp2p networking layer

**Incentives Track**

Consensus on [architecture of swap/accounting implementation](https://hackmd.io/@ethswarm/H1qvBIjC8)  
Global pinning on swarm [post-mortem and bee howto](https://hackmd.io/ph1bogFISdiW89icRoFUaQ?view)

**DevOps Track**

Launched Bee Alpha Release [public cluster](http://gateway.ethswarm.org/)  
Created public bootnodes DNS zone: bootnode.ethswarm.org  
Released several versions of [Bee Helm Chart](https://github.com/ethersphere/helm/tree/master/charts/bee) (latest v0.4.5) with following improvements:

* speed up pods starting/stopping
* update libp2p key version (1->3)
* add support to preset libp2p keys per pod
* add support for p2p fixed nodePorts
* add db_capacity, p2p-enable-quic, p2p-enable-ws and welcome-message config options
* use ethersphere/bee:0.1.0 image

Released [Beekeeper Helm Chart](https://github.com/ethersphere/helm/tree/master/charts/beekeeper) v0.1.3  
Released several versions of [Beekeeper](https://github.com/ethersphere/beekeeper) (latest v0.2.11) with following improvements:  
Added new integration tests into Beekeeper:

* fileretrieval
* kademlia
* pullsync
* retrieval

Added new features into Beekeeper:

* print command
* chaos mesh integration
* metrics

Created [bee-local](https://github.com/ethersphere/bee-local) repository with all the definitions for the Bee local cluster development  
Updated Bee and Beekeeper Grafana dashboards  
Configured CI/CD for [documentation](https://swarm-gateways.net/bzz:/docs.swarm.eth/) and [book of swarm](https://swarm-gateways.net/bzz:/latest.bookofswarm.eth/) publishing

**Research Track**

Iterated through Stage #1 of the BZZ token bonding curve design with Linum labs  
Further explored and specified deletion of content from Swarm:

* protocol violations and their associated costs
* self-deleting content retrieval and its possible applications
* possible APIs for deletable content
* paper about deletion in Swarm in progress

**Ecosystem Track**

At the Swarm Alpha online event we announced grants for dApp developers. Apply for grants [here](https://swarmgrants.typeform.com/to/SbrJiiiL).

dApps on Swarm:

* [Instaswarm](https://github.com/wendydv1989/insta-swarm) (mobile social/commerce),
* [Vyzion](https://vizyon.ai/) (radiology network)
* [Swapchat](https://github.com/felfele/swapchat) (zero leak private comms app)
* [Fairdrop](https://fairdrop.xyz/) (decentralized file transfer)

**Events Track**

In case you missed the event or you want to re-watch the talks and panels, [here is the link to the recording of the event.](https://www.youtube.com/watch?v=BHDfzzWVVK0&list=PL6fQnFAjtuY9TfTMm5GYqgscQ_6a7LE8A)