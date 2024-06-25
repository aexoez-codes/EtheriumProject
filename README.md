# Welcome to EthereumProject
This Ethereum Project is a simple implementation of a cryptocurrency token using the Ethereum blockchain. This contract includes basic functionalities such as minting new tokens and burning existing tokens. It also maintains a record of the total supply of tokens and the balance of each address.

# Features
1. **Public Variables**: The contract has public variables that store the token details:
* Token Name: "META"
* Token Abbreviation: "MTA"
* Total Supply of Tokens

2. **Address to Balance Mapping**: The contract maintains a mapping of addresses to their respective token balances.
  
3. **Minting Function**: The contract includes a function to mint new tokens. This function increases the total supply and the balance of the specified address.

4. **Burning Function**: The contract includes a function to burn tokens. This function decreases the total supply and the balance of the specified address. It also ensures that the balance of the address is sufficient to burn the specified amount of tokens.

5. **Owner Restriction**: Only the owner of the contract can call the mint and burn functions.

# Requirements
* Solidity version: ^0.8.26
* SPDX License Identifier: MIT

# Contract Details
**Variables**

* ```tokenName```: The name of the token (META).

* ```tokenAbbrv```: The abbreviation of the token (MTA).

* ```totalSupply```: The total supply of the token.

* ```balances```: A mapping that stores the balance of each address.

* ```owner```: The address of the contract owner.

# Constructor
The constructor sets the contract owner to the address that deploys the contract.

# Modifiers

```onlyOwner```: This modifier restricts access to certain functions, allowing only the owner to call them.

# Functions
```mint(address _address, uint _value)```: This function mints new tokens. It takes an address and a value as parameters, increases the total supply by the given value, and adds the value to the balance of the specified address. Only the owner can call this function.

```burn(address _address, uint _value)```: This function burns tokens. It takes an address and a value as parameters, ensures that the address has sufficient balance to burn the specified value, decreases the total supply by the given value, and subtracts the value from the balance of the specified address. Only the owner can call this function.

# Execution Process
To deploy and interact with the MyToken contract using Remix IDE, follow these steps:

1. **Open Remix IDE**: Navigate to Remix IDE.

2. **Create a New File**: In the Remix file explorer, create a new file named MyToken.sol.

3. **Copy the Contract Code**: Copy the MyToken contract code above into the new file.

4. **Compile the Contract**: Select the appropriate Solidity compiler version (^0.8.26) and compile the contract.

5. **Deploy the Contract**:

* Navigate to the "Deploy & Run Transactions" tab.
* Select the ```MyToken``` contract from the dropdown menu.
* Click the "Deploy" button.
* Confirm the transaction in your Ethereum wallet

6. **Interact with the Contract**:

* Once deployed, you can interact with the contract using the functions available in the Remix interface.
* Use the ```mint``` function to mint new tokens by providing the recipient's address and the amount.
* Use the ```burn``` function to burn tokens by providing the address and the amount to be burned.

7. **View Balances**:

* You can check the balance of any address by entering the address in the ```balances``` mapping field.
