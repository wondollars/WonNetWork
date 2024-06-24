# Node & Mining (Linux)

To mine Won using the POS algorithm, you need to run a Node and mine Won. As Won utilizes the POS algorithm, if you are using Geth version 1.11, please follow the steps below.
  
**Operating System Requirement:** Linux 22.04 LTS

  

### 1 - Install Geth from Ethereum
    sudo  add-apt-repository  -y  ppa:ethereum/ethereum
    sudo  apt-get  update
    sudo  apt-get  install  Ethereum
### 2- Create a directory for Wonchain data
    mkdir wonchaindata
### 3- Download the Genesis and Geth files (Version 1.11) from Won Github

    wget  https://raw.githubusercontent.com/wondollars/wonchain/main/genesis.json
    wget  https://github.com/wondollars/wonchain/raw/main/geth

### 4- Check the Geth version

    ./geth  --version

### 5- Install the Genesis file

    sudo  ./geth  init  --datadir  /wonchaindata  genesis.json

### 6- Run the Node

    sudo ./geth --gcmode archive --syncmode full --http  --miner.etherbase "your Wallet" --networkid  686868  --http.port  6868  --http.corsdomain "*" --http.vhosts "*" --http.addr "0.0.0.0" --datadir ./wonchaindata --mine

### 7- Add Peers & Mining

    sudo  geth  attach  --datadir  ./wonchaindata
    admin.addPeer("enode://7ab49c1ce4d7800412f8793eeb08febf0b2797531561cb292385f7127a5f7210acdbd8ae4302c7f5e4da0d443d5189a2c608a13eb40ab576e127d0223c4c6709@137.184.178.112:30303")
    miner.start()

# Node & Mining (Window)
**Access Our Github to download**: [WonChain Repository](https://github.com/wondollars/wonchain)

 1. Genesis.json
 2. Geth.exe (version 1.11  is  used  for  POW)

 

> Download  it,  put  it  in  1  folder.  Example:  We  call  WonChain  folder  and  it  is  created  in  Partition  D
### 1 - Navigate to WonChain directory
> Open  your  terminal,  follow  the  command  to  move  to  WonChain:

    cd D:\WonChain
    D:\

### 2 - Install the genesis.json of WonChain

    geth  init  --datadir  /wonchain  genesis.json

### 3 - Run Node

    geth  --gcmode archive --syncmode full --http  --miner.etherbase  0x312f95F844A1FC20EB91458DB6a44707876f52B6  --networkid  686868  --http.port  6868  --http.corsdomain "*" --http.vhosts "*" --http.addr "0.0.0.0" --datadir /WonChain --mine
    

> Change  the  address  0x312f95F844A1FC20EB91458DB6a44707876f52B6  to  your  wallet  to  start  mining  if  you  wish.

### 4 - Add Peers & Mining

> Open other Terminal, move to D:\WonChain and run the follow command

    geth  attach
    admin.addPeer("enode://277af6386d58c1613f84dbf16ee02a8814f20d68fe1db7c1101e868e7b7d70801c69a9d1993c28653e6b3be9a8f7fd19e0fd2523c7d5369f49bf75f889b12bb5@137.184.178.112:30303")
    miner.setEtherbase('Your Wallet')
    miner.start()

> if you already Changing your Wallet in Step 3, you can ignore the command "miner.setEtherbase('Your Wallet')"
