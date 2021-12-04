# bitcoin-onion-nodes
A list of bitcoin validating nodes running as Tor v3 onion services. This can be useful as a list of onion-only seed nodes, to get a new bitcoind instance connected. There's now also a list of validating nodes running as I2P hidden services. There's no guarantee of node availability. These nodes are simply known to have existed at a moment in time.

There are currently *1676* nodes in this collection.

Note: Previous versions of this list also contained v2 onion services. But as of Jun 1 2021, only v3 onion services are now listed. This is in anticipation for the deprecation of v2 addresses in July 2021.

## Why?

When I initiallt set up a bitcoind node to use Tor exclusively, the node had difficulty making outbound connections; It could not find peers to connect with. Over time, the node continued to identify more and more peers, so I began to build my own seed list. That list is now in this repo. 

Now, anyone can set up a new Tor-only bitcoind node and use this node list (or realistically, just a small portion of it) to seed the node.

## How?

I got the nodes from `bitcoin-cli getpeerinfo`. Nothing special, just periodic quering.

## Usage

The nodes can be added to `bitcoind.conf`, like this:

```
addnode=26dclk7xbzy4f6gaspbxzsmhhb332ozcjhaaksyq4x66ia5ckfdsryad.onion:8333
addnode=2it222nsdjr6xeamcynu2ddsctbovdgfgy5dcstw6u6k44pnxjcttmad.onion:8333
addnode=2jmtxvyup3ijr7u6uvu7ijtnojx4g5wodvaedivbv74w4vzntxbrhvad.onion:8333
```
