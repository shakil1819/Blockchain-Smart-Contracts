# Smart Contracts Defined (Part 1) (Remix IDE and Greeter Demos)

![[index.mp4]]
Summary:

- Smart contracts are an important component of decentralized applications built on blockchain technology.
- In a smart contract transaction, application-specific conditions need to be verified and validated.
- Smart contracts work with the application-specific semantics and constraints of the transaction, verifying, validating, and executing them.
- Smart contracts leverage the immutable recording and trust model of the blockchain.
- Smart contracts are immutable pieces of code deployed on the blockchain, and once deployed, they cannot be changed.
- Smart contracts can store variables called state variables, and their changes can be tracked over blocks.
- Solidity is a high-level language used to write smart contracts for the Ethereum blockchain.
- Remix is a web-based integrated development environment (IDE) used to create, deploy, and test smart contracts.
- Greeter and Simple Storage are two examples of simple smart contracts explored, demonstrating the structure and functionality of smart contracts.
- The development process of a smart contract involves design, coding, and testing stages.
- Remix IDE provides tools for compiling, running, and debugging smart contracts.
- Through Remix IDE, smart contracts can be deployed and tested on a JavaScript VM, with public variables and functions accessible for interaction.

```solidity
pragma solidity ^0.5.9;

contract Greeter  {

    string public yourName;  // data

    /* This runs when the contract is executed */

    constructor() public {

        yourName = "World";

    }

    function set(string memory name) public {

        yourName = name;

    }

    function hello() view public returns (string memory) {

        return yourName;

    }

}
```
