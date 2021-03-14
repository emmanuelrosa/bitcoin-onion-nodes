# bitcoin-onion-nodes
A list of bitcoin validating nodes running as Tor onion services. This can be useful as a list of onion-only seed nodes, to get a new bitcoind instance connected. There's no guarantee of node availability. These nodes are simply known to have existed at a moment in time.

There are currently *151* nodes in this collection.

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

## Contributions

If you would like to this list, simply submit a pull request. You should sort the nodes so that the Git diffs are easier to comprehend.

```
cp nodes.txt orig.txt
echo SOMENODE.onion >> orig.txt
cat orig.txt | sort | uniq > nodes.txt
rm orig.txt
git add nodes.txt
git commit -m "add some nodes"
```
