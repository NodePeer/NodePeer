# NodePeer

NodePeer is a client that will provide the bleeding edge of security improvements to the Peercoin protocol. These improvements are experimental, but highly necessary to preserve a functioning network. There will be provided no binaries, so this is a client meant for the technical community that knows how to build software. Due to the recent huge amount of vulnerabilities found by AI, we need another client to preserve the healthy fork if the chain splits.

Repo: [https://github.com/NodePeer/NodePeer](https://github.com/NodePeer/NodePeer)

How to build on Ubuntu:

```
sudo apt-get -y install build-essential autotools-dev automake autoconf libprotobuf-dev protobuf-compiler libminiupnpc-dev libzmq3-dev libqrencode-dev libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools libtool pkg-config libdb-dev libdb++-dev libboost-all-dev libssl-dev libevent-dev bsdmainutils libsqlite3-dev git
```

```
sudo apt-get -y update && sudo apt-get -y upgrade
```

```
mkdir -p ~/.peercoin
```

```
echo "rpcuser=username" >>~/.peercoin/peercoin.conf
```

```
echo "rpcpassword=`head -c 32 /dev/urandom | base64`" >>~/.peercoin/peercoin.conf
```

```
git clone https://github.com/NodePeer/NodePeer
```

```
cd NodePeer
```

```
./autogen.sh
```

```
./configure --with-gui=qt5 --with-incompatible-bdb
```

```
make
```

