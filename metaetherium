// SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;
contract Token {

   string public nametoken ="etherium";
   string public token_Abbrev = "eth";
   uint public total_supply = 0;
 
   mapping(address => uint)public balance;
    
   function  mint (address addre, uint value) public {
   total_supply += value;
   balance[addre] += value;
   
   }

    function burn (address addre, uint value) public {
   if (balance[addre] >= value){
      total_supply -= value;
      balance[addre] -= value;
}
}
}
