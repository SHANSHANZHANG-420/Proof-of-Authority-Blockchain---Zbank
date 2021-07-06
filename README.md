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

Create accounts for two nodes for the network with a separate datadir for each using geth: 

./geth --datadir node1 account new
./geth --datadir node2 account new


