+++
authors = []
date = 2020-03-03T23:00:00Z
excerpt = "Earlier this month, we published a blog post on how developers can start creating unstoppable DApps on Swarm. But how do you know it is not unicorn poop? In order to better inform you how Swarm is happening (soon), we are publishing this monthly development update to keep you updated and keep us accountable. Here, we only list what was done. Let’s go."
hero = "/images/1-nq9ax4pxcsycsst9idt2yw.png"
timeToRead = 5
title = "Swarm Development Update — February 2020"

+++
##### Earlier this month, we published a [blog post](https://medium.com/ethereum-swarm/get-ready-for-unstoppable-dapp-development-with-swarm-mvp-852933e32676?source=friends_link&sk=8c649f6ab35bae6c25a3ed7469cbea19) on how developers can start creating unstoppable DApps on Swarm. But how do you know it is not unicorn poop? In order to better inform you how Swarm is happening (soon), we are publishing this monthly development update to keep you updated and keep us accountable. Here, we only list what was done. Let’s go.

The **Bee, reference libp2p Swarm client**, received significant development attention and it quickly grew to be a minimal but functional product including most basic things:

* modern CLI interface,
* P2P and HTTP APIs,
* automated build and testing,
* basic instrumentation.
* for now, the underlay transport layer is set and Swarm Handshake protocol is implemented, as well as the Retrieval protocol.
* the Hive protocol is actively worked on, while we are adding new internal components as needed.
* Check out the progress on [github](https://github.com/ethersphere/bee).

**Commits to master**: The 0.5.5. and 0.5.6. brought the following upgrades:

* introduced load balanced retrieve requests across different peers
* improved retrieval performance meaning you’ll get the data fast(er)
* improved internal devp2p protocol messages handling
* supporting new ENS contract, so one less thing to worry for the devs
* added RNS name resolution (why RNS? Read more [here](https://medium.com/ethereum-swarm/partnership-between-swarm-and-rsk-infrastructure-framework-rif-to-develop-a-breakthrough-storage-3901734fdd41?source=friends_link&sk=b6f428ff463e15d3427f771bb58d322e) and [here](https://www.reddit.com/r/ethswarm/comments/ew4xje/swarm_055_release_is_out/)).

Code base consolidation. This is an ongoing task.

You might also start to miss some bugs. They left the building.

# DevOps

**TL;DR; First step towards Swarm client developer testnet — one testnet, many clients**

Since Swarm is matured as a project, a significant effort was made to improve infrastructure orchestration and migrate all production systems behind [swarm-gateways.net](http://swarm-gateways.net/). This effort also includes internal staging and testing infrastructure. This is the basis of the upcoming more robust testing infrastructure and improved release process.

Swarm, as a P2P network has to be able to validate implemented functionalities in close to real world scenarios, and that is what the new infrastructure will provide in both manual and automated fashion. This will be an important and pretty big task in the near future, that will ensure the quality of multiple Swarm implementations in the same network.

# Incentives track

**TL;DR; The incentives track has been primarily focused on hardening the implementation of the Swarm Accounting Protocol (SWAP).**

**Expanded APIs** enable you to engage in SWAP:

* peerbalance: get SWAP balance with a specific peer
* balances: get SWAP balances with all known peers
* peercheques: get last sent and received cheques for a given peer
* cheques: get last sent and received cheques for all known peers
* availablebalance: get current balance against which new cheques can be written

Deploying of chequebooks now happens via a **factory contract**. As it should.

A **simulation for the SWAP** package was setup that runs now automatically by the Swarm Continuous Integration. It’s quite real and begs the question: do we live in a simulation?

**Incentives testnet upgrade**: from now on any release, we run a series of tests against this network, to verify the correct functioning of bandwidth incentives

We added **batch support to the underlying database**. This is good as it reduces many SWAP edge-cases.

**Refactored the cash-out (of cheques) logic** from the SWAP business logic.

One known attack vector was where a malicious peer could send a too-high cheque. It was causing the balance to tilt in his favor and an honest node to respond with a cheque in return. The attack is now impossible by not allowing to receive cheques that would put a node into significant debt. So, yes, no flash SWAP trickery here.

**The working of SWAP is now documented best ever**, so if you’re missing weekend project ideas or spending some time at the beach, well…, we recommend this funky [reading](https://swarm-guide.readthedocs.io/en/latest/incentivization.html). If you’re next level, you can also start your own incentivized node. Old wisdom says, that every cloud, no matter how big it is, starts with the first node.

Added support for running SWAP with a chequebook that writes cheques for receiving ERC-20 tokens. This work was done to preliminary test how a Swarm token would behave under SWAP.

This track is done and made possible through partnership with cool people at [IOV Labs](https://www.iovlabs.org/). Thank you!

# Research track

**TL;DR; It’s complicated. That’s why Swarm needs a book.**

**Book of Swarm** structure and chapters are written. Once we have nice and shiny diagrams, we’ll share it. The book brings together all the research that was done on Swarm while the climax is reached in specs that give developers superpowers which they can use to develop their own Swarm clients.

**The push-sync incentives were inspected** and it was concluded that push-sync incentives are in many ways analogous to retrieval incentives. We expect the work which is happening at the moment to facilitate bandwidth incentives for retrieval to be highly applicable for facilitating bandwidth incentives for upload.

During the Swarm hackweek in Madrid, a plan was presented to facilitate flexible pricing for bandwidth incentives. It was agreed upon to develop a minimal approach, including support for the needed protocol messages and basic economic reasoning of the node. Flexible pricing for bandwidth allows any node to set their price for providing bandwidth to Swarm, therefore enabling competition between nodes. **This ultimately benefits end-users of Swarm with a better service for a lower price.**

# Organizational changes

There are many organisational changes as Swarm is essentially growing from dev team into a fully fledged organisation.

* **New organisational structure based** on decentralised and holacratic principles. There’s three new teams: Leet squad (Legal Entities Executive Team), Swarm Ops and Swarm Comms
* **New team members** who are not devs. However, they still bring gifts in the form of this blog post. [Or this.](https://medium.com/ethereum-swarm/la-vie-en-orange-paris-we-love-you-2c1fae6ff6f6?source=friends_link&sk=a7865e9e34d0cc3dac1d5ee99e9526a9)
* A plan for product releases is done. **Alpha, beta, ready, go!**
* **Legal incorporation is in progress.** If you wonder where, it’s the land of cheese. For the French people: “It’s Switzerland.”

# What’s next?

Quite a lot is planned next but we promised no promises here (did we break the promise with this?). So, please, just check our next development update.

One more thing… There’s a big and very important section missing, called **Ecosystem**. Let us know what you’re working on and we’ll make you famous in the Swarm universe. We might even help with dev related questions ;)

PLUR!

# Let’s stay in touch!

The Swarm team is reachable on [**Mattermost.**](http://beehive.ethswarm.org/)

Discussions about Swarm on [**/r/ethswarm**](https://www.reddit.com/r/ethswarm) and [**/r/ethereum**](https://www.reddit.com/r/ethereum) subreddits.

Please feel free to reach out via [**info@ethswarm.org**](mailto:info@ethswarm.org)

Swarm up your inbox with our monthly newsletter! [**Subscribe here.**](https://mailchi.mp/3871b41953e3/swarm-newsletter-signup)

[Meet us at EthCC!](https://medium.com/ethereum-swarm/la-vie-en-orange-paris-we-love-you-2c1fae6ff6f6?source=friends_link&sk=a7865e9e34d0cc3dac1d5ee99e9526a9)