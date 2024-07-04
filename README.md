
# How to Install Dogecoin Node on Ubuntu 22.04 using VPS
by ~Booktoshi

## Update and Upgrade System
```sh
sudo apt-get update
```
```sh 
sudo apt-get upgrade
```
## Download and Install Dogecoin Binaries
```sh
curl -L https://github.com/dogecoin/dogecoin/releases/download/v1.14.7/dogecoin-1.14.7-x86_64-linux-gnu.tar.gz | tar -xz
```
```sh
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
```
```sh
nano dogecoin.conf
```
**Add the following configuration:**
```
rpcuser=your
rpcpassword=pass
rpcallowip=127.0.0.1
maxconnections=50
rpcport=22555
server=1
txindex=1
```
```sh
ls
```
to check that the file actually saved
```sh
cd
```
```sh
dogecoind -daemon
```
**Start node to let it sync.**

# How to Set Up the ApeZord Doginal Inscriboor

## Install Node Version Manager (NVM) and Node.js

```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh
```
```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```
```sh
source ~/.bashrc
```
```sh
nvm list-remote
```
```sh
nvm install stable
```
```sh
node -v
```
```sh
sudo apt install npm
```
## Clone Doginals Repository and Install Dependencies
```sh
git clone https://github.com/booktoshi/doginals.git
```
```sh
cd doginals
```
```sh
sudo npm install
```

## Create .env File
```sh
nano .env
```
**Add the following configuration:**
```
NODE_RPC_URL=http://127.0.0.1:22555
NODE_RPC_USER=your
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
```
```sh
cd dunes-cli
```
```sh
npm install
```

## Create .env File
```sh
nano .env
```
**Add the following configuration:**

```sh
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
