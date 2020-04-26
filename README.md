# Idchain

Idchain is a fork of the [official Golang implementation of the Ethereum protocol](https://github.com/ethereum/go-ethereum) with a small change to burn gas fees instead of awarding them to the block sealers.

## Joining the Idchain Network

### Building on Ubuntu

```shell
$ sudo snap install go --classic
$ sudo apt-get install -y build-essential
$ git clone https://github.com/BrightID/idchain.git
$ cd idchain
$ make geth
$ sudo ln -sf $PWD/build/bin/geth /usr/bin/geth
```

### Running a Node


```shell
$ mkdir node
$ cd node
# Initializing the node by genesis file
$ wget http://idchain.brightid.org/files/idchain.json
$ geth --datadir . init idchain.json
# Setting static peers
$ wget http://idchain.brightid.org/files/static-nodes.json
# Running the node
$ geth --datadir . --networkid 74
```
