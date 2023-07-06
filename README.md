# Token Coin

This is a solidity program in which I am creating a token coin program. This program will take the input from the user and then give the total supply and the remaining balance as the output. The syntax used in this code is simple solidity syntax and uses the basic concept of the solidity program such as if-else condition, function creation, etc.  

# Description

This is the simple code that uses solidity programming. Solidity, a programming language for creating smart contracts for the Ethereum network, this program is a straightforward contract. The program contains two functions and some variables containing two string types, one of the uint type and the last is the mapping variable. The mapping variable is mapped from the address to the uint type. And about the functions: One is the mint function which incremented the balances and the other one is the burn function which is the opposite of the mint but the burn function also contains the if condition. 

# Getting Start

To get started with this programming type, you should first open up the solidity compiler that is Remix online IDE: https://remix.ethereum.org/. 
Now, when the IDE opens you first have to create a file in which you can write the code, so first click on the new file which is given at the left-hand sidebar. Name the file of your wish and save the file with an extension .sol. For example, firstcode.sol.
Now, write the given code in your file

    pragma solidity 0.8.18;
    
    contract MyToken {
    
        string public tokenName = "CHANDIGARH UNIVERSITY";
        string public tokenAbbrv = "CU";
        uint public totalSupply = 0;
    
        mapping (address => uint) public balances;
        function mint (address _address, uint _value) public {
            totalSupply += _value;
            balances [_address] += _value;    
        }
        function bur (address _address, uint _value) public { 
            if (balances[_address] >= _value){
            totalSupply -= _value;
            balances [_address] -= _value;  
            }   
        }   
    }

# Explanation 

Now, I will explain my code. 

First I have created the contract MyToken. Inside the contract, I made two string-type public variables tokenNmae and tokenAbbrv, and give them a name CHANDIGARH UNIVERSITY and CU respectively. 

Next, I created a uint type public variable totalSupply and initialize it with 0. 

In the next part, I created a mapping variable (address => uint). This state that the address is mapped to uint and assigns its values balances. 

After that, the first function is created a mint function which contains two parameters value and address. Inside a mint function, the total supply is added to the value, and balances of addresses are also added to the value. 

At last, the function bur is created which will work opposite of the mint function. In this function, an if condition is used which state that if the balance of address is greater than or equal to the value then, the value is decreased from the total supply and the balances of address. 


# Compilaion

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18", and then click on the "Compile firstcode.sol" button.

Once the code is compiled, you can deploy the contract.  When you deploy the contract you will see the 6 buttons of which 2 are orange color and 4 are Steal Blue color. The orange color ones represent the function and the Steal Blue ones represent the variables. 

When you click on totenName it will show you "CHANDIGARH UNIVERSITY". When you click on tokenAbbrv it will show you "CU". The one is totalSupply which is showing 0 now and the last one is a balance which is showing nothing.

Now, if you select any random address from the account displayed above the deploy button. Choose any random address from there and now copy that to the clipboard.

Once, you have done that now just paste that address to the mint function and put any random value let's say 1000 in the context of the value. Now, after doing that just again check for total supply. It has changed from 0 to 1000. Do the same with the bur function, but the value will get decreased this time not going to increase.

You can also check the balance in the same manner.


# License 

This project is licensed under the MIT License - see the LICENSE.md file for details


