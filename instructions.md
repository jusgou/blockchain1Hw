Instructions: 

node1_public = 0xaeEa900e06cC9387A5EF487C4d5d54A7387cB7a5
node1_secret_key_path = node1\keystore\UTC--2021-07-11T22-39-04.598977300Z--aeea900e06cc9387a5ef487c4d5d54a7387cb7a5

node2_public = 0x76002E5d130008e56bCE23401D93964036f98964
node2_secret_key_path = node2\keystore\UTC--2021-07-11T22-39-37.234486000Z--76002e5d130008e56bce23401d93964036f98964

Chain_ID = 47538

Step 1) Initialize:

Initialize each node with the following commands: 

node1: ./geth init homework.json --datadir node1

node2: ./geth init homework.json --datadir node2


Step 2) Start Node 1

Start node1 with the following command: 

./geth --datadir node1 --unlock "aeEa900e06cC9387A5EF487C4d5d54A7387cB7a5" --mine --rpc --allow-insecure-unlock

[Make note of the node1 enode: "enode://0b447b8f49a2cd946efaeddfae9097572d923ede7ae38f0b1cb75612e8c40140cc70a8a9f3270e6707a6f5568056da886c4c2dd950a46d03d6fa3390b979b883@127.0.0.1:30303"

Enter password to unlock chain.


Step 3) Start Node 2

Start node2 with the following command:

./geth --datadir node2 --unlock "76002E5d130008e56bCE23401D93964036f98964" --mine --port 30304 --bootnodes "enode://0b447b8f49a2cd946efaeddfae9097572d923ede7ae38f0b1cb75612e8c40140cc70a8a9f3270e6707a6f5568056da886c4c2dd950a46d03d6fa3390b979b883@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock

Enter password to unlock chain.
