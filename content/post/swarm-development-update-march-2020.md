+++
authors = []
date = 2020-04-02T22:00:00Z
draft = true
excerpt = "Here is what we’ve been up to in the last month. The Book of Swarm was announced and we are maintaining a strong pace to move Swarm from the MVP phase through to the Alpha release. More details on this are coming soon."
hero = "/images/screenshot-2020-07-14-at-13-46-01.png"
timeToRead = 4
title = "Swarm Development Update — March 2020"

+++
Here is what we’ve been up to in the last month. The [Book of Swarm](https://medium.com/ethereum-swarm/the-book-of-swarm-4922c2b40423) was announced and we are maintaining a strong pace to move Swarm from the [MVP phase](https://medium.com/ethereum-swarm/get-ready-for-unstoppable-dapp-development-with-swarm-mvp-852933e32676) through to the Alpha release. More details on this are coming soon.

We have divided the update into different tracks so that you can quickly scan and read the parts that you are interested in. Let’s dive in!

### Core Track 

* Swarm’s quarterly hackweek that was planned to take place in Mallorca was held online because of the world pandemic situation. Important decisions for the whole Swarm project were made. It was decided that all efforts will be focused on the recently started [Bee project](https://github.com/ethersphere/bee), with the goal for it to be the reference implementation of the Swarm.
* This online hackweek was used constructively to give updates and discuss with the team about the state of Swarm and Bee projects.
* Storage layer implementation testing was continued and a new approach with using only BadgerDB is being actively worked on. Results are yet to be finalized.
* Bee project received significant additions in protocols area, such as initial Hive protocol implementation and improvements in protocol handling.
* Distributed tracing over libp2p is ready for bee.

**Recorded sessions of the online hackweek will be soon  
available online.** [Subscribe to our Youtube channel](https://www.youtube.com/channel/UCu6ywn9MTqdREuE6xuRkskA) **to be notified.**

### Incentives Track

* Migration of the incentivized testnet to the new cluster.
* Transaction queue PR, which ensures that all interaction of Swarm with the blockchain can be handled and is reliable in all situations (even across restarts!) This PR resolves many edge cases and will make future development of the incentivized protocols much easier and of higher quality.
* Creating Solidity-like variable types in Golang, such that the Swarm code already handles all variables as if they were Solidity variables and ensures we are not sending unexpected variables to the blockchain.
* The quality of logging has improved in the SWAP package. Now, logs from SWAP can be written to a file (needed for audit purposes) and filtering can be done more efficiently.

### Research Track

* Research has iterated on the full solution for positive incentivization of chunk storage based on the redistribution of postage stamp income among storers in return of a proof of their engagement in storage. See[swarmresear.ch](https://swarmresear.ch/t/race-positive-incentivization-of-chunk-storage/48).
* The missing chunk notification protocol has been revisited and a much simpler scheme has been proposed to solve on demand data recovery. This underlies the much anticipated product feature of global pinning.
* Chunk recovery uses the trojan chunk-based new pss. The prototype implementation is starting first week of April.
* Using Trojan chunks and single owner chunks,, research finalised a few update notification constructs.
* The vision of a new API design was presented. We decided to take a 2 week feasibility research whether the switch would speed up release 1.0

**DevOps Track**

* Production Swarm cluster was stabilized and optimized.
* All the websites were migrated from Ethereum to the Swarm infrastructure.
* Swarm-staging and swap-staging clusters were deployed.
* Core cluster was put in use and teams were familiarized with it and the tooling.
* DevOps Overview presentation was held online, as Mallorca hack week has been canceled and moved online.
* It has been decided that all infrastructure improvement plans made for the Swarm project are transferred to the Bee project.
* Changed ELK stack with Loki for logs aggregation
* Swarm was enabled to expose Prometheus metrics

### Ecosystem Track

* Filter persistence in Swarm was unveiled at EthCC in Paris, [Fairdrop](https://fairdrop.xyz/), a file sharing and storage platform built entirely using the Ethereum Web3 decentralized stack and leveraging Swarm as it’s storage layer.

### News

**Book of Swarm — The blueprint for the web 3.0**

Read the [blog post here](https://medium.com/ethereum-swarm/the-book-of-swarm-4922c2b40423).

We will share some interesting excerpts and concepts from the book in the upcoming days, so make sure you follow us on [Twitter](https://twitter.com/ethswarm) to hear about the latest news.

### Events

* Two important talks by Viktor and Gregor will be broadcasted from [Noncon](https://noncon.org/) on 4th April from 20:30 CET. Follow us on [Twitter](https://twitter.com/ethswarm) for links to the talks.

### MISC

* We are BUIDLing the future of storing files one code line at a time. Show some love and donate and/or share our [Gitcoin](https://gitcoin.co/grants/540/ethereum-swarm?tab=description) campaign. Thanks ❤

### Let's Stay In Touch

* The Swarm team is reachable on [Mattermost.](http://beehive.ethswarm.org/)
* Discussions about Swarm on [/r/ethswarm](https://www.reddit.com/r/ethswarm) and [/r/ethereum](https://www.reddit.com/r/ethereum) subreddits.
* Please feel free to reach out via [info@ethswarm.org](https://us3.admin.mailchimp.com/campaigns/info@ethswarm.org)