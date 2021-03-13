# bitcoin-onion-nodes
A list of bitcoin validating nodes running as Tor onion services. This can be useful as a list of onion-only seed nodes, to get a new bitcoind instance connected. There's no guarantee of node availability. These nodes are simply known to have existed at a moment in time.

There are currently *131* nodes in this collection.

## Usage

The nodes can be added to `bitcoind.conf`, like this:

```
addnode=2l2u6mrojvm6zypx.onion
addnode=34jtv2p5pw4e5bp3.onion
addnode=35yncj7et6k3koqy.onion
```

Alternatively, you can use the AWK script `mknodes.awk` to generate a list ready to be inserted into `bitcoind.conf`:

```
awk -f mknodes.awk < nodes.txt
```
