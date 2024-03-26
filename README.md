# General

Won Network emerges as a pioneering blockchain venture committed to providing a haven for asset storage, with a focus on anonymity, gas-free transactions, and a suite of enduring utilities. 
    Our platform encompasses a diverse range of services, including a versatile wallet app, a decentralized exchange (DEX), an array of engaging games, and a launchpad for budding projects.

    At the core of Won Network's ethos is the belief in democratizing access to financial resources. We envision a world where individuals can safeguard their assets without sacrificing their privacy or incurring unnecessary transaction fees. To this end, Won Network operates on a gas-free model, ensuring that users can execute transactions seamlessly, without being burdened by the costs typically associated with blockchain operations.

    Moreover, Won Network is committed to fostering community engagement and empowerment. Through our unique distribution system, we distribute WON tokens at no cost to users, thereby ensuring widespread accessibility and inclusivity within our ecosystem.

    Looking ahead, Won Network aspires to become a hub of interoperability, connecting seamlessly with other blockchains to enhance convenience and utility for our users. By forging strategic partnerships and embracing collaboration, we are poised to realize our vision of a sustainable and inclusive blockchain community.

    Join us on this journey as we redefine the landscape of decentralized finance, one innovative solution at a time. Together, let's build a future where financial sovereignty is a reality for all.
  
**Operating System Requirement:** Linux 22.04 LTS

  

### 1 - URL
    Homepage: https://wonnetwork.org/ 
    WonDollars: https://wondollars.org (Free Distribution)
    Faucet: https://faucet.wondollars.org/ 
    Bridge: https://test-bridge.wondollars.org
    Documents: https://docs.wonnetwork.org/
   
    
### 2- Blockchain Information
    Name: WonChain
    Chain ID: 686868
    RPC URL: https://rpc.wonnetwork.org/
    SYMBOL: WON
    EXPLORER: https://scan.wonnetwork.org/
    EXPLORER-2 : https://explorer.wonnetwork.org/
    
### 3- Token Information
    
    - Contract-Address-Celo: "0xE517f64B5668eAa0AF4316c6b7386aEBAEC23B22"
 
    - Contract-Address-Bnb: "0xC05e4d0E570E5C0Be901Bbf36D6a27819a24F6c9"
 
### 4- Check the Geth version

    ./geth  --version

### 5- Install the Genesis file

    sudo  ./geth  init  --datadir  /wonchaindata  genesis.json

### 6- Run the Node

    sudo ./geth --gcmode archive --syncmode full --http  --miner.etherbase "your Wallet" --networkid  686868  --http.port  6868  --http.corsdomain "*" --http.vhosts "*" --http.addr "0.0.0.0" --datadir ./wonchaindata --mine

### 7- Add Peers & Mining

    sudo  geth  attach  --datadir  ./wonchaindata
    admin.addPeer("enode://277af6386d58c1613f84dbf16ee02a8814f20d68fe1db7c1101e868e7b7d70801c69a9d1993c28653e6b3be9a8f7fd19e0fd2523c7d5369f49bf75f889b12bb5@137.184.178.112:30303")
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
