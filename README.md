Token Smart Contract
This Solidity program implements a simple ERC20-like token contract with basic minting and burning functionalities. It demonstrates the fundamental operations of creating, minting, and burning tokens on the Ethereum blockchain.

Description
The Token contract is a basic smart contract written in Solidity. It allows for the minting of new tokens to an address and the burning of tokens from an address. The contract keeps track of the total supply of tokens and the balance of each address. This program serves as an introductory example for those looking to understand how token contracts work in Solidity.

Getting Started
Executing Program
To run this program, you can use Remix, an online Solidity IDE. Follow the steps below to get started:

Open Remix:
Go to the Remix website at https://remix.ethereum.org/.

Create a New File:
Click on the "+" icon in the left-hand sidebar to create a new file. Save the file with a .sol extension (e.g., Token.sol).



// SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;

contract Token {
   string public nametoken = "etherium";
   string public token_Abbrev = "eth";
   uint public total_supply = 0;

   mapping(address => uint) public balance;

   function mint(address addre, uint value) public {
      total_supply += value;
      balance[addre] += value;
   }

   function burn(address addre, uint value) public {
      if (balance[addre] >= value) {
         total_supply -= value;
         balance[addre] -= value;
      }
   }
}
Compile the Code:
Click on the "Solidity Compiler" tab in the left-hand sidebar. Ensure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile Token.sol" button.

Deploy the Contract:
Once the code is compiled, go to the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the Token contract from the dropdown menu, and click on the "Deploy" button.

Interact with the Contract:
After deploying the contract, you can interact with it by calling the mint and burn functions.

To mint tokens, provide an address and a value, then click on the "mint" button.
To burn tokens, provide an address and a value, then click on the "burn" button.
Authors
suman kumar 
License
This project is licensed under the MIT License - see the LICENSE.md file for details.
