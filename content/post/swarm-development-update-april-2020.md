+++
authors = []
date = 2020-05-04T22:00:00Z
draft = true
excerpt = "Here is the latest update on the work that was done in April 2020. The team is working on the development of the Bee client and there is a good progress on global pinning too."
hero = "/images/screenshot-2020-07-14-at-13-46-01.png"
timeToRead = 0
title = "Swarm Development Update — April 2020"

+++
#### Here is the latest update on the work that was done in April 2020. The team is working on the development of the Bee client and there is a good progress on global pinning too.

### Core Track

**Bee project:**

* Added low-level chunk upload and download endpoints to HTTP API.
* Added chunk persistence by porting existing solutions, localstore and shed packages, from the swarm project and adjusting to the new code organization.
* Added a connection breaker component that makes the node more resilient to a large number of potential connectivity related problems.
* Improving connections handling to the bootnodes when the node starts. As well adding more error-resilient connectivity strategies on libp2p level.
* Added addressbook persistence. Addressbook is a component that stores underlay addresses about known peers.
* Added the first and simple netstore implementation. Netstore is a component that fetches the chunk from the p2p network if the chunk is not found in the node’s localstore.
* Added simple file joiner implementation and integrated to the codebase. This is the first step to have file operations on the exposed HTTP API.
* Added a general purpose state store, mostly ported from the swarm codebase.
* Progressing in replacing LevelDB with BadgerDB for chunk storage, but the effort is still on-going. A proper performance testing is planned to be performed when more chunk and file related functionalities are added to the codebase.
* Added more functionalities to the debug API to be used by integration tests, such as node addressing information and whether the chunk is stored by the node.
* Connected tracing identifiers with log messages to correlate events.
* Added explicit coding guidelines in the project repository.
* A number of improvements related to unit testing.

**Incentives/persisence:**

* Huge progress on global pinning.
* PSS is redesigned, initial stage curtailed for global pinning requirements.
* Implemented trojan chunks.
* Add PSS monitoring capabilities to monitor the state of the sent trojan chunk.

### DevOps Track

* Completed observability stack for Bee project (prometheus, loki, jaeger and grafana)
* Had presentation/demo — How to use observability stack for debugging purposes
* Released new version of Bee Helm chart
* Setup bee-staging project for easier Bee deployments and testing
* Had presentation/demo — How to use bee-staging
* Started Beekeeper project for Bee integration testing
* Released Beekeeper v0.1.0 with peer count test available
* Setup static code analysis tool for Bee project ([deepsource.io](http://deepsource.io/))
* Create eks-local-disk-provisioner for better utilization of NVME SSD disks in EKS cluster
* Extended registration of ENS domains
* Created DevOps Roadmap

### Research Track

* Designed the bonding curve for the emission of Swarm token (BZZ)
* Did some numerical stress-tests in gnu bc
* Discussed and validated the design with experts in the field
* Finished the design and architecture part of the Book of Swarm, specs are in the making

### Events Track

Viktor announced the Book of Swarm at Noncon 2020. [Watch his talk here.](https://www.youtube.com/watch?v=4tVvMhDqxX0&feature=youtu.be)

### Let's Stay In Touch

* The Swarm team is reachable on [**Mattermost.**](http://beehive.ethswarm.org/)
* Discussions about Swarm on [**/r/ethswarm**](https://www.reddit.com/r/ethswarm) and [**/r/ethereum**](https://www.reddit.com/r/ethereum)subreddits.
* Please feel free to reach out via [**info@ethswarm.org**](mailto:info@ethswarm.org)
* Swarm up your inbox with our monthly newsletter! [**Subscribe here.**](https://mailchi.mp/3871b41953e3/swarm-newsletter-signup)