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

<br>

Contract: https://sepolia.etherscan.io/address/0x2a48af6a3733ccde8fab2d5149357f73f8e4a753

<br>

Contract created\
&ensp;TxHash: 0xd2ccb8a03539f64b4f262e5b992f011092dc364963a22849fa1be59368aaafa0

Set Text\
&ensp;TxHash: 0x550d8247724c4666894f919468116049da96a4f37bcb88d3be01368afc81b6d3

Transfer Ownership\
&ensp;TxHash: 0x2070cf133c2beb1d03128a3a28f8a95b1cf844409aec0942659c9cdf285e9b0c
     
Set Text (FAILED) 'Caller is not the owner'\
&ensp;TxHash: 0x15fe5ae7014cdcf173dde6ea7b6f2a5afb0714b0bc10dbc1f2dd2f9cb5a1285d

Set Text\
&ensp;TxHash: 0xae6a3663995ccc71ba69b5fd8f2d1d583e856d71b5596adc68bd6071c4b446b3

Transfer Ownership\
&ensp;TxHash: 0xb2472bcf52e13f26e89ead3bb803182d771675d760b8496283aeea7875fedacd

Transfer Ownership\
&ensp;TxHash: 0x4b4725b420af51a2c5f6862d2fbd112a2ee242d749fa69a706e2356b8cf1089d

Transfer Ownership (FAILED) 'Caller is not the owner'\
&ensp;TxHash: 0xdc549be6b921c6ca352cff6ad2d9d6302512cf44e8d2dc72001883f3225c1e1a

Transfer Ownership (FAILED) 'Caller is not the owner'\
&ensp;TxHash: 0xe15b5de935a757fda9cc942b8b66b52f8b0727442299c28ce7662d2049a24c23

Transfer Ownership (FAILED) 'Caller is not the owner'\
&ensp;TxHash: 0x660bcdd56f054a5c115481a46d5b9359dd957246a2c6dee1ba2ebd1dd15a6b89

Set Text\
&ensp;TxHash: 0x850525ba8b0eb2077511d701ec3187b30ff593721baf4b135a6da7481cdadb6e

Transfer Ownership\
&ensp;TxHash: 0x4e5729bfc128b0d75674de2dd558b45b03bd17e2b74ae3c2459577d4322e8110

Set Text\
&ensp;TxHash: 0x8a3c0afe6830b7dec66d553627d3622ffc154903cb5d869dd2f6b85cdafbec54
     
Set Text (FAILED) 'Caller is not the owner'\
&ensp;TxHash: 0xa8ff1f56dafed376946b28c15fc2ffb8b4242d851bcc59ea8fe01da4ad10d6a5

Transfer Ownership\
&ensp;TxHash: 0x00a0a8f4c21eda0b2cd3b673a1483cb1f5e6d18c0e760b096d042c2e32090183

Set Text\
&ensp;TxHash: 0x31beaa9dc566ca7168993ec5c6b3fd3bc6a74ac325a6b83c8a7a7528dd23844f

Transfer Ownership\
&ensp;TxHash: 0xe6bdcc6f69df39137b0b5e5ceb9bfb9a86113a244efb6b0fd2ac24df67d6f34c

Set Text\
&ensp;TxHash: 0x8cba232131f5dc77a74e031011a8152f08a69a76197e0f7904a0b0ddfc807113

Set Text\
&ensp;TxHash: 0xe50b172b75ebe989b46f78df1b2598482487fe31d779630d13ee3ffe41c5f2d6

Transfer Ownership\
&ensp;TxHash: 0xb80255155b7275a0fe414cc8c34180e374f83b54fb41733fea96d98aaf8b68c7

Set Text\
&ensp;TxHash: 0x45e63fb06f81a31624b7048a69bb0468b27b967f0078a19b5f43f1925b56ebf0
