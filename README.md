Create new nodes for blockchain network with passwords:
./geth --datadire node1 account new
./geth --datadire node2 account new

Run puppeth and create a network name
Select the following options:
2 Configure new genesis
1 Create new genesis from scratch
2 Select 2. Clique - Proof-of-Authority

Seal accounts for both nodes and set chain ID

Initiate the network:
./geth --datadir node1 init "network_name.json"
./geth --datadir node2 init "network_name.json"

Open a new command line window for each of the following commands to start the network:
./geth --datadir node1 --unlock "public_key_address_node1" --mine --rpc --allow-insecure-unlock

./geth --datadir node2 --unlock "public_key_address_node2" --mine --port 30304 --bootnodes "enode://node1_P2P_network_address@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock

Configuration:
Chain ID: 888
Port: 30304

Connect to MyCrypto wallet:
Select the appropriate keystore file and enter the password
Create a custom network: set the node and network name, currency = ETH, Chain ID (as noted above)
Once connected, the screen will change to "Send Ether & Tokens"
Enter the recipients public key address and the amount to send, then click Send Transaction
You can check the status of the transaction under TX Status.

