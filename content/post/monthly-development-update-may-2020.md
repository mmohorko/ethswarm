+++
authors = []
date = 2020-06-04T22:00:00Z
excerpt = "Swarm’s Dev Team made great progress in the last month, here is the gist"
hero = "/images/screenshot-2020-07-14-at-13-46-01.png"
timeToRead = 7
title = "Monthly Development Update — May 2020"

+++
**Highlight of the month**

We are happy to share the first public pre-release of the [**Book Of Swarm**](https://swarm-gateways.net/bzz:/latest.bookofswarm.eth/the-book-of-swarm-viktor-tron-v0.1-pre-release.pdf)(hosted on Swarm), which is now available for your reading pleasure. Feedback and suggestions on the book are more than welcome. Please reach out via [bookofswarm@ethswarm.org](mailto:bookofswarm@ethswarm.org) if you would like to participate in the peer review.

## **Core Track** 

**Bee project**

* [Implemented forwarding Kademlia](https://github.com/ethersphere/bee/pull/155) topology driver and integrated with libp2p service
* Added [signing](https://github.com/ethersphere/bee/pull/196) of underlay address and overlay address validation in the handshake protocol.
* Implemented [local pinning](https://github.com/ethersphere/bee/pull/187) on the chunk level.
* [Improvements on push syncing](https://github.com/ethersphere/bee/pull/171) protocol implementation.
* File [chunking](https://github.com/ethersphere/bee/pull/186) and [joining](https://github.com/ethersphere/bee/pull/189) implemented.
* Improved overlay address generation by including [network id](https://github.com/ethersphere/bee/pull/190) to comply with the Book of Swarm.

**Incentives / Research / Persistence**

* Research on external signer integration
* [Global pinning](https://github.com/ethersphere/swarm/issues/2173) experimental implementation on phase 3 (testing)
* Finalized BZZ token parameters in collaboration with partners

## **DevOps**

Released [Bee Helm chart v0.3.1](https://github.com/ethersphere/helm/tree/master/charts/bee) with the option to set an update strategy for the Bee cluster.

Implemented [automatic integration tests](https://github.com/ethersphere/bee/actions?query=workflow%3ABeekeeper) using Beekeeper and Github Actions for Bee.

Added new integration tests into Beekeeper:

* full connectivity — checks if every node has connectivity to all other nodes in the cluster
* ping pong — executes ping from all nodes to all other nodes in the cluster, and prints round-trip time (RTT) of each ping
* push sync — uploads given number of chunks to given number of nodes, and checks if chunks are synced to their closest nodes

Released [Beekeeper v0.2.1](https://github.com/ethersphere/beekeeper) with the option to use insecure TLS for both, Bee API and debug API, independently of one another.

## **Events**

May is traditionally marked with the brightest orange in our calendar since this is the time of the most anticipated annual Swarm Orange Summit. 2020 mixed up our event plans a bit, but we are happy to announce that you can expect some serious swarming on June 29. More details coming soon.

## **Let’s stay in touch!**

* The Swarm team is reachable on [**Mattermost.**](http://beehive.ethswarm.org/)
* Follow us on [**Twitter**](https://twitter.com/ethswarm).
* Discussions about Swarm on [**/r/ethswarm**](https://www.reddit.com/r/ethswarm) and [**/r/ethereum**](https://www.reddit.com/r/ethereum)subreddits.
* Please feel free to reach out via [**info@ethswarm.org**](mailto:info@ethswarm.org)
* Swarm up your inbox with our monthly newsletter! [**Subscribe here.**](https://mailchi.mp/3871b41953e3/swarm-newsletter-signup)