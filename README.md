# bitcoin-onion-nodes
A list of bitcoin validating nodes running as Tor v3 onion services. This can be useful as a list of onion-only seed nodes, to get a new bitcoind instance connected. There's no guarantee of node availability. These nodes are simply known to have existed at a moment in time.

There are currently *208* nodes in this collection.

Note: Previous versions of this list also contained v2 onion services. But as of Jun 1 2021, only v3 onion services are now listed. This is in anticipation for the deprecation of v2 addresses in July 2021.

## Usage

The nodes can be added to `bitcoind.conf`, like this:

```
addnode=26dclk7xbzy4f6gaspbxzsmhhb332ozcjhaaksyq4x66ia5ckfdsryad.onion:8333
addnode=2it222nsdjr6xeamcynu2ddsctbovdgfgy5dcstw6u6k44pnxjcttmad.onion:8333
addnode=2jmtxvyup3ijr7u6uvu7ijtnojx4g5wodvaedivbv74w4vzntxbrhvad.onion:8333
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
