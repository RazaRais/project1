# TOKEN CONTRACT
This Solidity program is a  program that demonstrates the basic syntax and functionality of the Solidity programming language. It is is a Solidity contract that implements a basic token contract with minting and burning functions.
# Description
This program is a  contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. It is is a Solidity contract that implements a basic token contract with minting and burning functions. This contract provides a basic token implementation with minting and burning capabilities, allowing for the creation and destruction of tokens while maintaining balances and total supply
# Getting Started
## Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., project.sol). Copy and paste the following code into the file:
```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;
contract MyToken {
string public tokenName = "META";
string public tokenAbbrv = "MTA";
uint public totalSupply = 0;
    
mapping(address => uint) public balances;
   
function mint (address _address, uint _value) public {
   totalSupply += _value;
   balances[_address] += _value;
}

    function burn (address _address, uint _value) public {
       if (balances[_address] >= _value)
       {
   totalSupply -= _value;
   balances[_address] -= _value;
}}

}
```

The mint function works by increasing the total supply of tokens by the specified amount and then increasing the balance of the recipient by the same amount. The burn function works by decreasing the total supply of tokens by the specified amount and then decreasing the balance of the sender by the same amount.
The burn function also has a conditional statement that ensures that the balance of the sender is greater than or equal to the amount that is being burned. This is to prevent users from burning tokens that they don't own.

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile project.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Project" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the 'burn'and 'mint'  function. Click on the "project" contract in the left-hand sidebar, and then click on the desired function. Finally, click on the "transact" button to execute the function and retrieve the output by providing token values a sinput.

# Authors
@RazaRais
Ahmad Raza
# License
This project is licensed under the MIT License - see the LICENSE.md file for details
