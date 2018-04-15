# Cryptocurrency Networks

#### What is a node and what does it do?

A node is a program that stores a cryptocurrency's blockchain and verifies transactions against its copy of the blockchain. A node will connect with other nodes to create a network. This network will then act like a large, democratized, node.

#### How do nodes transfer information?

A node will attempt to connect to other nodes through TCP/IP port 8333. The node will then search a DNS server for any compatible node listed on the DNS server (this can also be manually set.)

After finding adjacent nodes, the node will then request blocks from its adjacent nodes until it has formed its own base blockchain.

Nodes generally have three different modes:

  - Archival Nodes
    - These are full nodes that hold every single transaction that has ever occured
    - They are used to bring a new full node to the network ”up to speed”'
    
  - Full Nodes
    - These are nodes that hold the entire blockchain, and have to have seen every transaction that has ever taken place
      - The blockchain can be reduced to a Merkel Root
    - Subject to concensus rules
    
  - Lightweight Nodes
    - These are nodes that have not seen every transaction on the network and are most often used for hosting wallets
    - They can be tricked into doing things that full nodes would not (ergo, not following consensus rules)
    
#### How the network kicks out attackers.

Since a network consists of multiple nodes, and it is accepting of new nodes, there is the possibility of an attacker hosting a node with false information. The network will detect this false information and compare it to the majority of the nodes in the network. If a majority disagrees with the attacker, than the attacker will be forced to either cooperate or be evicted from the network.

#### The benefit of nodes.

Nodes create a node mesh, and this node mesh is a network of cooperating machines that are in control of different people, under differing governments with different rules. This gives many advantages:

  - Scalability
    - 0 distance between you and the authority
  
  - Security
    - Data redundency beyond what one will ever need
  
  - Transparancy
    - All address information is (generally) available to the public
    
  - Cheap
    - Since the costs are spread to every user in cryptocurrency that runs a node, fees are cheap, if not free
    
[Next we will cover blockchain technology in cryptocurrency](https://github.com/Dadadah/CryptoNotes/blob/master/Blockchain.md)
