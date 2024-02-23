# Node & Mining (Linux)

To mine Won using the POS algorithm, you need to run a Node and mine Won. As Won utilizes the POS algorithm, if you are using Geth version 1.11, please follow the steps below.

**Operating System Requirement:** Linux 22.04 LTS

## Step 1: Install Geth from Ethereum

    ```bash
    sudo add-apt-repository -y ppa:ethereum/ethereum
    sudo apt-get update
    sudo apt-get install Ethereum

## Step 2: Create a directory for Wonchain data

    ```bash
    mkdir wonchaindata

## Step 3: Download the Genesis and Geth files (Version 1.11) from Won Github

```bash
wget https://raw.githubusercontent.com/wondollars/wonchain/main/genesis.json
wget https://github.com/wondollars/wonchain/raw/main/geth

## Step 4: Check the Geth version
```bash
./geth --version


## Step 5: Install the Genesis file
```bash
sudo ./geth init --datadir /wonchaindata genesis.json

## Step 6: Run the Node
```bash
sudo ./geth --gcmode archive --syncmode full --http --miner.etherbase "your Wallet" --networkid 686868 --http.port 6868 --http.corsdomain "*" --http.vhosts "*" --http.addr "0.0.0.0" --datadir ./wonchaindata --mine

## Step 7: Add Peers & Mining
```bash
sudo geth attach --datadir ./wonchaindata
admin.addPeer("enode://277af6386d58c1613f84dbf16ee02a8814f20d68fe1db7c1101e868e7b7d70801c69a9d1993c28653e6b3be9a8f7fd19e0fd2523c7d5369f49bf75f889b12bb5@137.184.178.112:30303")
miner.start()

# Node & Mining (Windows)


**Access Our Github to download**: [WonChain Repository](https://github.com/wondollars/wonchain)

1. Genesis.json
2. Geth.exe (version 1.11 is used for POW)
3. Download it, put it in 1 folder. Example: We call WonChain folder and it is created in Partition D.

### Step 1: Navigate to WonChain directory

Open your terminal, follow the command to move to WonChain:

```bash
cd D:\WonChain
D:\


### Step 2: Install the genesis.json of WonChain
```bash
geth init --datadir /wonchain genesis.json

### Step 3: Run Node
- Change the address 0x312f95F844A1FC20EB91458DB6a44707876f52B6 to your wallet to start mining if you wish.
```bash
geth --gcmode archive --syncmode full --http --miner.etherbase 0x312f95F844A1FC20EB91458DB6a44707876f52B6 --networkid 686868 --http.port 6868 --http.corsdomain "*" --http.vhosts "*" --http.addr "0.0.0.0" --datadir /WonChain --mine


### Step 4: Add Peers & Mining
```bash
sudo geth attach
admin.addPeer("enode://277af6386d58c1613f84dbf16ee02a8814f20d68fe1db7c1101e868e7b7d70801c69a9d1993c28653e6b3be9a8f7fd19e0fd2523c7d5369f49bf75f889b12bb5@137.184.178.112:30303")
miner.setEtherbase('Your Wallet')
miner.start()
- If you already changed your Wallet in Step 3, you can ignore the command miner.setEtherbase('Your Wallet').
