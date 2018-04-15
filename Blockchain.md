# Blockchain Technology in Cryptocurrencies

### Cryptographic Functions

Before covering how the blockchain works, you should have a basic understanding of a cryptographic function.

A cryptographic function is basically a function that is one way. It is easy to solve but hard to reverse. For example:

  - f(x) = 7\*x + 3
    - This is not a cryptographic function because we can find x with f(x)
    - x = (f(x) - 3)/7
  
  - f(x) = x%7 + 3
    - This is a cryptographic function because there is an infinite number of possibilities for x with any f(x)

### Blocks and Blockchains

Now that we know what a cryptographic function is, we can cover their application with cryptocurrency.

#### What is a block?

A block is a data structure that stores many details about the network at a certain time, such as:

  - Block Header
    - Currency Version
    - Cryptographic hash of previous block
    - Its Merkel Root
    - When it was created as a timestamp
  
  - Magic Number
  
  - Block Size
  
  - Transaction Count
  
  - Transaction List
  
#### How are blocks immutable?

Blocks are immutable because one small change the a block leads to a large change in future blocks due to the Merkel Root. This makes it where if a block change is detected, the network will reject the change as long as the majority does not support it.

#### What is a Merkel Root?

![Merkel Root Diagram](https://upload.wikimedia.org/wikipedia/commons/9/95/Hash_Tree.svg)
  
A Merkel Root is the root of a Hash Tree. A Hash Tree is a special tree data structure where each parent is the sum hash of all of its children. This means that only the leaves are actual data.

We can apply this data structure to cryptocurrencies. If we assume each transaction is a leaf on the hash tree, we can assume that any change to any transaction completely changes the Merkel Root.

This means that any change to transactions, previous blocks, address amounts, timestamps, or anything stored on the blockchain will change the Merkel Root, creating essentially an immutable data structure.
