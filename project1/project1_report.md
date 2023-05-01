HelloWorld.sol
```
// SPDX-License-Identifier: GPL-3.0

pragma solidity >=0.7.0 <0.9.0;

  

contract HelloWorld {

    string private text;

    address public owner;

  

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

  

    function everyoneSetText(string calldata newText) public {

        text = newText;

    }

  

    function transferOwnership(address newOwner) public onlyOwner {

        owner = newOwner;

    }

  

    modifier onlyOwner()

    {

        require (msg.sender == owner, "Caller is not the owner");

        _;

    }

}
```
- Contract Address: [0x29fd1AC7c72bb7d7c16e06b381a98940210903E0]

Function: constructor()

Transaction hash: [0x99f4a3cf42b660a1d955c16f01364e5b2432c7bff84f6c83a308c1694e9a00b6]

Status: Successful

Function: everyoneSetText(string)
Transaction hash: [0x9c2884f955f12fd3b778cfe423bf0b62640495dd3a5371ba0383faae8c0abb03]

Status: Successful

Function: setText(string)
Transaction hash: [0x2537bf6d647782a4719268fec1de4ee655f612895718c8db4e562a6b797cf414]

Status: Successful

Function: transferOwnership(address)
Transaction hash: [0x571f8256eef813b5e2b0d5bb1b290fe3b3cf02d38a4ee8fd4c25b6ccdb90ba2e]

Status: Successful
