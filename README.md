# QuorumDemo
Using this demo you'll be able to setup a blockchain network (using Quorum Maker), deploy a smart contract and interact with it

Step by setp guide: 

First we need to setup a test/development Quorum network with two nodes through [Quorum Maker](https://github.com/synechron-finlabs/quorum-maker/wiki#setting-up-quorum-testdevelopment-network):

1. Clone quorum maker from [Quorum Maker github repository](https://github.com/synechron-finlabs/quorum-maker.git) 

2. Run the following command to create a Quorum development network with two nodes and tessera as privacy layer:
    * `./setup.sh dev --tessera --project <projectName> --nodecount 2`
    * Make sure to over wirte projectName


3. Quorum maker will print to the cmd the following, we will need them later:
    * Node public keys
    * RPC/Node manager ports 

4. Navigate to the directory created and run the network in docker:   
    * `cd <projectName>`
    * `docker-compose up`




Now you can access NodeManager UI through:
  - node1: http://localhost:20104 
  - node1: http://localhost:20204

** Note: Above URLs are valid if you’re using OSX, otherwise change the port according to the NodeManager ports printed by QuorumMaker to the cmd 




Through NodeManager UI, compile and deploy your contract.
  - Click on “Compile & Deploy Contract”
  - Choose your solidity file
  - Choose the other node to be “privateFor” 



After the contract has been deployed, you’re able to start interacting with it. See the code in this repo.


