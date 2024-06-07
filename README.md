MyToken Smart Contract
Overview
This smart contract creates a basic cryptocurrency token called "MyToken" with the symbol "MTK". It allows minting (creating) and burning (destroying) of tokens.

Key Components

1. Token Details: 
   - “name”: The name of the token ("MyToken").
   - “symbol”: The abbreviation of the token ("MTK").
   - “totalSupply”: The total number of tokens in circulation.

2. Balances:
   - “balances”: A mapping (similar to a dictionary) that keeps track of how many tokens each address (like a user's account) has.

Functions

1. Minting Tokens:
   - “mint(address _to, uint _amount)”: This function allows creating new tokens.
     - “_to”: The address where the new tokens will be sent.
     - “_amount”: The number of new tokens to create.
     - The function increases the “totalSupply” by “_amount” and also increases the balance of the “_to” address by “_amount”.

2. Burning Tokens:
   - “burn(address _address, uint _amount)”: This function allows destroying tokens.
     - “_address”: The address from which the tokens will be burned.
     - “_amount”: The number of tokens to destroy.
     - The function first checks if the “_address” has enough tokens to burn (“balances[_address] >= _amount”). If true, it decreases the “totalSupply” by “_amount” and also decreases the balance of the “_address” by “_amount”.

Example Use

- Minting: If we call “mint(0xABC..., 100)”, it will create 100 new tokens and add them to the balance of the address “0xABC...”.
- Burning: If we call “burn(0xABC..., 50)”, it will destroy 50 tokens from the balance of the address “0xABC...”, assuming it has at least 50 tokens.

This contract provides a simple way to manage the creation and destruction of tokens, ensuring the total supply and individual balances are updated accordingly.

Author : Aditya Thakur
