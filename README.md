TOKEN
This Solidity program is a  program that demonstrates the basic syntax and functionality of the Solidity programming language. It is is a Solidity contract that implements a basic token contract with minting and burning functions
Description
This program is a  contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. It is is a Solidity contract that implements a basic token contract with minting and burning functions.It defines a simple token contract with the ability to mint and burn tokens while keeping track of balances.
Getting Started
Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., project.sol). Copy and paste the following code into the file:

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

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile project.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Project" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the 'burn', 'mint'  function. Click on the "project" contract in the left-hand sidebar, and then click on the desired function. Finally, click on the "transact" button to execute the function and retrieve the output by providing token values a sinput.

Authors
Rais@
Ahmad Raza
License
This project is licensed under the MIT License - see the LICENSE.md file for details
