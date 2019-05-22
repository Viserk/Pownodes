UNIX DAEMON UBUNTU EASY GUIDE
====================
Some notes on how to build Pownodes in Ubuntu.

First add the necessary extra repository and update all packages:
```
sudo add-apt-repository ppa:bitcoin/bitcoin
sudo apt update
sudo apt upgrade
```

Now install the dependencies as described in the installation documentation:

```
sudo apt install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils git libdb4.8-dev libdb4.8++-dev curl
sudo apt install libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev libzmq3-dev
```

Optionally install the Qt dependencies if you want to build the Pownodes GUI:
```
sudo apt install libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools libprotobuf-dev protobuf-compiler
```

Clone Pownodes code

```git clone https://github.com/Viserk/```

Edit permissions

```chmod 755 -R Pownodes```

Build

```
cd Pownodes
./autogen.sh
./configure
make
make install # optional
```
