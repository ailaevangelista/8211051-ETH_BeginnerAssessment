# 8211051-ETH_BeginnerAssessment

# Token
The main objective of this Solidity project is to implement a token contract that enables users to create and burn tokens. In order to ensure that specific actions are only taken when possible, the program also uses conditional expressions. Additionally, it makes it possible to track balances connected to specific addresses.

## Description
This application is a straightforward contract that counts the number of tokens owned by each address using a mapping data structure. The software offers two operations: one to add tokens and the other to remove them. Overall, this application serves as a helpful simulation, illuminating the creation and destruction of tokens.

### Executing Program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., myToken.sol). Copy and paste the following code into the file:


CODES

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {
    // public variables here
        string public name = "OMNI";
        string public abbreviation = "NAMI";
        uint public supply = 0;

    // mapping variable here
        mapping(address => uint) public balance;

    // mint function
        function mint(address add, uint value) public{
            supply += value;
            balance[add] += value;
        }
    // burn function
        function burn(address add, uint value) public{
            if(balance[add] >= value){
                supply -= value;
                balance[add] -= value;
            }
        }
}`

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile myToken.sol" button.

To deploy the contract, click on the "Deploy and Run Transactions" button. This will open a new window that allows you to deploy the contract. Do not forget to select the “MyToken” contract before deploying.

In the deployment window “Deployed Contracts”, set the parameters for the balance, mint, and burn functions.

To mint new tokens, input the address of the recipient and the number of tokens you want to mint and click transact.

To burn tokens, input the address of the recipient and the number of tokens you want to burn and click transact.

To see current balances of the address, input the address of the recipient and the number of tokens you want to mint and click call. You can also see the total supply by clicking the “totalSupply” button.

#### Authors
NTCIAN Aila Marie Evangelista Discord @8211051@NTC.EDU.PH

##### License
This project is licensed under the MIT License - see the LICENSE.md file for details.
