# smart-contract--using-solidity

A smart contract is a self-executing agreement implemented on a blockchain platform, typically using a programming language called Solidity. Solidity is a high-level language designed specifically for writing smart contracts on the Ethereum blockchain, although it can also be used on other blockchain platforms.
In Solidity, you can define smart contracts by writing code that specifies the contract's functionality, rules, and interactions with other contracts and users.

# Error Handling in Solidity - Module1

In Solidity, you can define smart contracts by writing code that specifies the contract's functionality, rules, and interactions with other contracts and users.
This Solidity smart contract demonstrates error handling techniques using the `require`, `assert`, and `revert` statements. Let's explore how error handling is implemented in the code!

# Getting Started


# Executing Program
# The project will involve the following steps:

# Setting up Remix:


1.Open the Remix IDE in your web browser.
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

2.Creating the smart contract:
Start a new file in the code editor within Remix. Copy and paste the following code into the file:

''' // SPDX-License-Identifier: MIT pragma solidity 0.8.18;

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;contract SmartContract {
    uint public value;
    
    function setValue(uint _value) public {
        // require statement
        require(_value > 0, "Value must be greater than zero");
        
        // assert statement
        assert(_value != 42);
        
        // set the value
        value = _value;
    }
    
    function setValueWithRevert(uint _value) public {
        if (_value == 0) { // revert statement
            revert("Value cannot be zero");
        }
        
        value = _value;
    }
}



# Purpose


 It's important to note that require(), assert(), and revert() are used for different 
 
1.require() is typically used to validate input conditions or contract preconditions. It throws an error and reverts the transaction if the condition is not met.
2assert() is used to check for internal errors in the contract. It should only be used for conditions that should never be false. If the condition is false, it indicates a 
 bug in the contract.
 
3.revert() is used to explicitly revert the transaction, usually due to a requirement violation or an exceptional condition.
 These error handling mechanisms help ensure the contract's integrity and provide meaningful feedback to users interacting with the contract.

# Compiling the Contract:


.Use the Remix compiler panel to compile your smart contract.
.Select the appropriate compiler version pragma solidity ^0.8.0;


# Deploying the Contract:
1.Switch to the "Deploy & run transactions" tab in Remix.

2.Deploy the compiled contract by clicking the "Deploy" button.


# Interacting with the smart contract:

1.Utilize the Remix IDE to interact with the deployed contract create.

2.In the above smart contract, there are two functions: setValue() and setValueWithRevert(). Both functions take an input _value and set the value variable of the contract 
 to that input value. However, they use different error handling mechanisms.
 
3.Input the adress and value and click on the corresponding function buttons to execute our contract.
## Author

Pragya
@https://www.linkedin.com/in/pragya-299103231///pragyathakur092002@gmail.com

## License

his project is licensed under the MIT License - see the LICENSE.md file for details.This code is licensed under the MIT License. You can find the license text in the SPDX-License-Identifier comment at the beginning of the contract.
