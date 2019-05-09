Sucre Core 0.12.2
===============================

To Build Daemon in Ubuntu
---------------------

Build from source below.

```bash
sudo apt -y update && sudo apt -y install build-essential libssl-dev libdb++-dev libboost-all-dev libcrypto++-dev libqrencode-dev libminiupnpc-dev libgmp-dev libgmp3-dev autoconf autogen automake libtool autotools-dev pkg-config bsdmainutils software-properties-common libzmq3-dev libminiupnpc-dev libssl-dev libevent-dev

sudo add-apt-repository ppa:bitcoin/bitcoin
sudo apt-get update
sudo apt-get install libdb4.8-dev libdb4.8++-dev -y

git clone https://github.com/korwinus/SucreCore.git

cd SucreCore
find . -name "*.sh" -exec sudo chmod 755 {} \;
./autogen.sh
./configure # or ./configure --without-gui
make

cd src

strip sucrd
strip sucr-cli
strip sucr-tx

cp sucrd /usr/bin
cp sucr-cli /usr/bin
cp sucr-tx /usr/bin
```


What is Sucre?
----------------

Sucre is an experimental new digital currency that enables anonymous, instant
payments to anyone, anywhere in the world. Sucre uses peer-to-peer technology
to operate with no central authority: managing transactions and issuing money
are carried out collectively by the network. Sucre/Sucr Core is the name of the open
source software which enables the use of this currency.

For more information, as well as an immediately useable, binary version of
the Sucre Core software.


License
-------

Sucre Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.

