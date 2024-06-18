This Solidity contract provides a basic implementation of a token system on the Ethereum blockchain.

Overview
The Token contract supports minting and burning tokens, as well as tracking balances for different addresses.

License and Solidity Version
solidity
Copy code
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;
Contract Structure
State Variables
solidity
Copy code
contract Token {

   string public nametoken = "etherium";
   string public token_Abbrev = "eth";
   uint public total_supply = 0;
   mapping(address => uint) public balance;
nametoken: The name of the token ("etherium").
token_Abbrev: The token's abbreviation ("eth").
total_supply: The total supply of the token.
balance: A mapping to track the balance of each address.
a. Mint Function
solidity
Copy code
function mint(address addre, uint value) public {
   total_supply += value;
   balance[addre] += value;
}
This function increases the total supply of the token and credits the specified address with the minted tokens.
b. Burn Function
solidity
Copy code
function burn(address addre, uint value) public {
   if (balance[addre] >= value) {
      total_supply -= value;
      balance[addre] -= value;
   }
}
This function decreases the total supply of the token and deducts the specified amount from the given address, provided that the address has enough tokens.






