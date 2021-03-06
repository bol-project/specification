# Neo Network

_This section is part of the Community Yellow Paper ^[See [Community Yellow Paper](https://github.com/neoresearch/yellowpaper) repository] initiative, a community-driven technical specification for Neo blockchain._

**WARNING:** this section is an **unreleased draft**.
It is expected to be incomplete or even to carry incorrect information, so feel free to contribute with us!

## Blockchain Networks

A Blockchain can be seen and defined differently, depending on the interests around it.
For example, technically speaking, a blockchain can be seen as a data structure capable of handling immutability of records and transparency, however it can also be seen as a **protocol** that allows operations between untrusted agents.
As a network protocol, it is necessary to clearly define how these agents may interact and exchange information.

Blockchain networks are usually composed by full nodes and lightweight nodes.
Full nodes persist and validate the whole blockchain, being able to provide all kinds of information to other nodes, such as lightweight nodes.
Lightweight nodes are usually linked to user wallets, that only have limited blockchain information and depend on full nodes to have access to detailed blockchain information (in order to validate transactions, for example).
A broader view of the topology can be seen as an interaction between agents, forming the pillars of a multi-agent system [@MAS:xxx].
The possibility of deploying agents with different abilities into the network is the core of the Neo Ecosystem.

A special type of node is capable of **generating** new blocks on the blockchain, which is the bookkeeper node^[On Bitcoin network, these nodes are called Miners (due to proof-of-work paradigm), however on Neo no mining process is required to achieve consensus].
On Neo network, these bookkeeper nodes are also called Consensus Nodes, which are elected by means of public voting and are capable of systematically proposing new blocks (by ordering and validating pending network transactions).
Detailed information for Neo Consensus Protocol (called Delegated Byzantine Fault Tolerance) is presented on [Section @Sec:Consensus].

## Communication between nodes

Peer-to-peer (P2P) communication between nodes is the core on fully distributed systems, such as Neo blockchain.

### P2P Protocol Specification

P2P commands can be found on [Neo Project](https://https://github.com/neo-project/neo) repository^[Developers can look directly on _neo/Network/P2P_ folder, while this section is a work on progress].

### Message compression

### Node Capabilities
    TCP, UDP, WS

## Interacting with nodes

A trivial way for interacting with external world can be done by RPC's calls, which are API's natively implemented in the NEO core library.
Detailed documentation regarding these calls can be found in the [API Reference](https://docs.neo.org/en-us/node/cli/apigen.html).

## Plugins

## Interacting with NEO network: transactions, RPC and P2P protocols
