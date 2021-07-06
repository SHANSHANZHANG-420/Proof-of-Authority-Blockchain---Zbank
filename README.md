# Proof-of-Authority-Blockchain---Zbank

This is a PoA Chain and this private network is running on the Ethereum network.

## Preparation 
1. python 3.7 virtual ethereum environment 
2. MyCrypto App https://download.mycrypto.com/.
3. Go Ethereum Tools download page at https://geth.ethereum.org/downloads/



## Instructions
First step, ppen a terminal activate ethereum environment: 
 conda activate ethereum 

Next, navigate to the go ethereum-Tools folder and type the following command:

./puppeth

### Creating two nodes with accounts
The Proof of Authority (PoA) algorithm is typically used for private blockchain networks as it requires pre-approval of, or voting in of, the account addresses that can approve transactions (seal blocks).
Because the accounts must be approved, we will generate two new nodes with new account addresses that will serve as our pre-approved sealer addresses.

Create accounts for two nodes for the network with a separate datadir for each using geth: 

./geth --datadir node1 account new

./geth --datadir node2 account new

Saving the node 1 and node 2 Public address of the key and Path of the secret key file


### Creating a Genesis Block
<img width="826" alt="Create a genesis block " src="https://user-images.githubusercontent.com/76719561/124562773-c3619880-de82-11eb-8501-37597355d861.png">

