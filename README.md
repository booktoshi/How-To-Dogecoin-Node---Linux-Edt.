
# How to Install Dogecoin Node on Ubuntu 22.04 using VPS
by ~Booktoshi

## Update and Upgrade System
```sh
sudo apt-get update
sudo apt-get upgrade
```
**PRESS Y AND INSTALL MAINTAINER PACKAGES PROVIDED WHEN ASKED.**

## Install Necessary Packages
```sh
sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils
sudo apt-get install libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev
sudo apt install libdb5.3++-dev libdb5.3++ libdb5.3-dev
sudo apt-get install libzmq3-dev
sudo apt-get install libminiupnpc-dev
```

## Download and Install Dogecoin Binaries
```sh
curl -L https://github.com/dogecoin/dogecoin/releases/download/v1.14.7/dogecoin-1.14.7-x86_64-linux-gnu.tar.gz | tar -xz
sudo mv dogecoin-1.14.7/bin/* /usr/local/bin/
```

## Start Dogecoin Node
```sh
dogecoind -daemon
```
**Wait for 1 minute**

```sh
dogecoin-cli stop
```

## Configure Dogecoin
```sh
cd ~/.dogecoin/
nano dogecoin.conf
```

**Add the following configuration:**
```
rpcuser=book
rpcpassword=toshi
rpcallowip=127.0.0.1
maxconnections=50
rpcport=22555
server=1
```

```sh
ls - to check that the file actually saved
cd
dogecoind -daemon
```
**Start node to let it sync.**

# How to Set Up the ApeZord Doginal Inscriboor

## Install Node Version Manager (NVM) and Node.js
```sh
sudo curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
source ~/.bashrc
sudo nvm install stable
node -v
```

## Clone Doginals Repository and Install Dependencies
```sh
git clone https://github.com/booktoshi/doginals.git
cd doginals
sudo npm install
```

## Create .env File
```sh
nano .env
```
**Add the following configuration:**
```
NODE_RPC_URL=http://127.0.0.1:22555
NODE_RPC_USER=user
NODE_RPC_PASS=pass
TESTNET=false
FEE_PER_KB=21000000
```

## Create and Sync Wallet
```sh
node . wallet new
```
**Now send $DOGE to the Doginal Inscription Wallet so that you can Mint.**

```sh
node . wallet sync
```

## Mint Doginals
```sh
node . wallet mint <wallet address> <file path>
```
**Example:**
```sh
node . wallet mint D9Ue4zayx5NP7sTSBMM9uwuzqpHv4HnkaN 1.png
```

## Mint DRC-20 Tokens
```sh
node . drc-20 mint <address> <ticker> <amount>
```
**Example:**
```sh
node . drc-20 mint DESpUq549VHcZTc27cRfE3DNAMfiwyk4W4 $wen 900
```

**WOOF WOOF**

# How to Set Up SirDuney DUNES Etcher

## Clone Dunes Repository and Install Dependencies
```sh
git clone https://github.com/booktoshi/dunes-cli.git
cd dunes-cli
npm install
```

## Create .env File
```sh
nano .env
```
**Add the following configuration:**
```
PROTOCOL_IDENTIFIER=D
NODE_RPC_USER=user
NODE_RPC_PASS=pass
TESTNET=false
FEE_PER_KB=21000000
UNSPENT_API=https://unspent.dogeord.io/api/v1/address/unspent/
ORD=https://wonky-ord.dogeord.io/
```

## Create and Sync Wallet
```sh
node dunes.js wallet new
```
**Now send $DOGE to the DUNES Etching Wallet to start Minting Dunes.**

```sh
node dunes.js wallet sync
```

## Mint Dunes
```sh
node dunes.js mintDune <id> <amount> <to>
```
**Example:**
```sh
node dunes.js mintDune '5088000:50' 100000000 DTZSTXecLmSXpRGSfht4tAMyqra1wsL7xb
```
