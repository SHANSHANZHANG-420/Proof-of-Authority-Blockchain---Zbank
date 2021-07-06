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



### Initialize the nodes 
Using geth, initialize each node with the new networkname.json.

./geth --datadir node1 init zbank/zbank.json

./geth --datadir node2 init zbank/zbank.json


### Unlock the node 1 and node 2 - staring mining blocks

Run the nodes in separate terminal windows with the commands:

./geth --datadir node1 --unlock "SEALER_ONE_ADDRESS" --mine --rpc --allow-insecure-unlock

./geth --datadir node2 --unlock "SEALER_TWO_ADDRESS" --mine --port 30304 --bootnodes "enode://SEALER_ONE_ENODE_ADDRESS@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock



Unlock my  node 1 
./geth --datadir node1 --unlock "519a7994b5C45b7b2850Bd1C81d714b44C26D479" --mine --rpc --allow-insecure-unlock
<img width="766" alt="Node 1 mining" src="https://user-images.githubusercontent.com/76719561/124563900-d163e900-de83-11eb-9ae4-fac1a55fd885.png">


Unlock my node 2 
./geth --datadir node2 --unlock "5c361d4d6CD12D545a6e5B3C49CF6c077aDF5f91" --mine --port 30304 --bootnodes "enode://a034092680fce7b35044e658276443196cc6996f78f72308a897a67a6b718c21b13439a34aa0c7a61fa89eabdf90747f9dd12c77e27beb805f08702e504679ae@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock
<img width="640" alt="Node 2 mining" src="https://user-images.githubusercontent.com/76719561/124563916-d5900680-de83-11eb-9290-d92526c195f0.png">


### Go to myCrypto App 
Create custom network 
<img width="578" alt="Custom network" src="https://user-images.githubusercontent.com/76719561/124564465-7252a400-de84-11eb-9b70-08a62980834f.png">


After connecting to the custom network in MyCrypto, it can be tested by sending money between accounts.

Select the View & Send option from the left menu pane, then click Keystore file (node 1) 
On the next screen, click Select Wallet File, then navigate to the keystore directory inside your Node1 directory, select the file located there, provide your password when prompted and then click Unlock.

View your account balance 
<img width="1201" alt="Account balance" src="https://user-images.githubusercontent.com/76719561/124564719-b04fc800-de84-11eb-8cde-dd1505c205fe.png">


### make Transaction 
<img width="852" alt="Screen Shot 2021-07-06 at 5 19 59 pm" src="https://user-images.githubusercontent.com/76719561/124564859-d2e1e100-de84-11eb-9166-978c190d06a1.png">
<img width="1036" alt="Transcation" src="https://user-images.githubusercontent.com/76719561/124564874-d6756800-de84-11eb-807c-999f72fb7330.png">

