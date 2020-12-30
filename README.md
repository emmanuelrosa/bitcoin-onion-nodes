# bitcoin-onion-nodes
A list of bitcoin validating nodes running as Tor onion services.

The nodes can be added to `bitcoind.conf`, like this:

```
addnode=2l2u6mrojvm6zypx.onion
addnode=34jtv2p5pw4e5bp3.onion
addnode=35yncj7et6k3koqy.onion
```

You can use the AWK script `mknodes.awk` to generate a list reading to be inserted into `bitcoind.conf`:

```
awk -f mknodes.awk < nodes.txt
```
