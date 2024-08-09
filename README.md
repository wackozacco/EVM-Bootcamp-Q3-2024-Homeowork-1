# EVM-Bootcamp-Q3-2024-Homework-1

Assignment: 

* Interact with “HelloWorld.sol” within your group to change message strings and change owners
* Write a report with each function execution and the transaction hash, if successful, or the revert reason, if failed
* Submit your weekend project by filling the form provided in Discord

Code reference from Lesson 4 for HelloWorld.sol:

    // SPDX-License-Identifier: GPL-3.0
    pragma solidity >=0.7.0 <0.9.0;
      
    contract HelloWorld {
      string private text;
      address public owner;
        
      modifier onlyOwner()
      {
          require (msg.sender == owner, "Caller is not the owner");
          _;
      }
    
      constructor() {
        text = "Hello World";
        owner = msg.sender;
      }
    
      function helloWorld() public view returns (string memory) {
        return text;
      }
    
      function setText(string calldata newText) public onlyOwner {
        text = newText;
      }
    
      function transferOwnership(address newOwner) public onlyOwner {
        owner = newOwner;
      }
    }

https://sepolia.etherscan.io/address/0x2a48af6a3733ccde8fab2d5149357f73f8e4a753
