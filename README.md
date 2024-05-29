
# MyToken Smart Contract: Token Implementation & Creation

this is a Solidity Project "Token Implementation & Creation"
program.





## Description

With the sign MTK, this smart contract introduces MyToken, a unique ERC20 token. The contract has features for keeping a balance ledger current in addition to minting and burning tokens.
## Getting Started
## Executing Program

First to open any Browser and to open Remix IDE, it's an online Solidity Platform.
link - https://remix.ethereum.org/.

then create a new file and file extension is .sol and save it. then copy and paste the code into the file:

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;
contract MyToken {

    // public variables here
    string public tokenName = "sonu";
    string public tokenAbbrs = "svm";
    uint public totalSupply = 0;


    // mapping variable here

    mapping (address => uint) public balance;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balance[_address] += _value;

    }

    // burn function

    function burn(address _address, uint _value) public {
        if (balance[_address] >= _value) {
             totalSupply -= _value;
            balance[_address] -= _value;
    
        }
    }

}

## Authors

Sonu kumar Saw


## License

This project is licensed under the MIT License- see the LICENSE.md file for details.

