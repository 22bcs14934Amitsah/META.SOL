**Contract Details**
Token Name: MYMINING
Token Abbreviation: MINING
Initial Total Supply: 0
**Contract Structure**
The contract MyToken is written in Solidity version 0.8.18 and includes the following key components:

**State Variables**:

tokenName: Public variable storing the name of the token.
tokenAbbrvi: Public variable storing the abbreviation or symbol of the token.
totalSupply: Public variable tracking the total supply of tokens minted.
Mapping:

balance: Mapping from addresses to uint, storing the balance of tokens for each address.
Functions:

mint: Function to mint new tokens and assign them to a specified address. Increases totalSupply and updates the balance of the recipient.
burn: Function to burn tokens from a specified address. Reduces totalSupply and updates the balance of the address, if the address has sufficient tokens.
License
This project is licensed under the MIT License. See SPDX-License-Identifier in the contract file for details.

**CODE**
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;
contract MyToken {

    // public variables here
    string public tokenName = "MYMINING";
    string public tokenAbbrvi = "MINING";
    uint public totalSupply = 0;
    // mapping variable here
    mapping (address => uint) public balance;
    // mint function
    function mint( address _address, uint _value) public {
        totalSupply += _value;
        balance[_address] += _value;
    }
    // burn function
    function burn(address _address, uint _value) public {
        if(balance[_address] >= _value){
            totalSupply -= _value;
            balance[_address] -= _value;
        }
    }
}

**Usage**
To use this contract:

Deploy MyToken contract to an Ethereum-compatible blockchain.
Interact with the contract using Ethereum wallets or scripts.
Call mint to create new tokens for addresses.
Call burn to destroy tokens from addresses.
Compile the contract using Solidity 0.8.18.
Deploy the compiled bytecode to an Ethereum address.
Interact with the deployed contract using tools like Remix.

**Contact**
For questions or support, contact the project maintainer at muthimar@amitsah.com.

**Author** :Amit Kumar Sah
