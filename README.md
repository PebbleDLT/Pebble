![Pebble Logo1](pebblelogo_red.svg) ![Pebble Logo2](Pebble.svg)
# Pebble Distributed Ledger Technology
## Live Network
##### NOTE: Currently the Pebble network is in active development, hence we are not sharing the codebase and the live network is maintained by us.The network is not fully stable yet.
We have launched a testnet for development,outreach and awareness purposes, tests on scalability and decentralisation is done on regular basis. We currently use modified ethereum smart contracts engine for smart contract
execution.

For more information about how the technology works, the team behind it, and the roadmap visit www.pebbledlt.com

For Queries and trying Pebble, reach out at team@pebbledlt.com
## Installation
### Pebble Peer Discovery

The discovery go program helps in connecting new peer to network,
and finding other peers in the Pebble Network.

`Service Available at PORT : 5000`

`GRPC Function: AddPeer(PublicKeyHex,PeerIP)`

### Pebble Peer Node Testnet Configuration

Modify the `Config.txt` for pointing to Discovery Node
Place `Config.txt` in the same directory as the Pebble Binary.


### Pebble APIs

Connect to Pebble GRPC Server at `PORT 5001`

#### APIs Calls for testnet
1) `send_transaction(toAddr,fromAddr,amount,data,signature)`
2) `get_balance(address)`
3) `create_contract(bin,abi,fromAddr)`

    _creates the new smart contract and initializes it,returns the newly created smart contract Address._
4) `call_method(method,contractAddr,input,fromAddr,signature)`

    _calls the specified method of smart contract with given input and context, returns the output if present._
5) `get_ledger()`

    _returns the the whole state of the network, as a grpc stream_
