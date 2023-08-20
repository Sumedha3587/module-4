# DegenToken Smart Contract
Version: 1.0.0
License: MIT License
SPDX-License-Identifier: MIT

#  Description
The DegenToken smart contract is an ERC20 token contract that allows for the creation, management, and interaction with a custom token called "Degen" (symbol: DGN). The contract includes functionality to mint new tokens, transfer tokens, burn tokens, redeem tokens for specific choices, and store location data.

# Prerequisites
Solidity Compiler v0.8.18
OpenZeppelin Contracts v4.3.2 (ERC20.sol, Ownable.sol)
# Usage
Deploy the DegenToken smart contract to the Ethereum network.
The contract owner has the exclusive ability to mint new Degen tokens using the mint function.
Users can transfer their Degen tokens to other addresses using the transferTokens function.
Users can burn (destroy) their Degen tokens using the burnTokens function.
The store function provides a hardcoded location data representation.
The redeemTokens function allows users to redeem their Degen tokens for specific choices (locations) as indicated in the store function.
Choices range from 1 to 5, each corresponding to a location.
The contract checks the user's balance before redemption and transfers tokens to the contract owner while recording the redeemed location.
# Functions
mint(address to, uint256 amount) public onlyOwner
Mints a specified amount of Degen tokens and assigns them to the provided address.
transferTokens(address to, uint256 amount) external
Transfers a specified amount of Degen tokens from the sender's account to the target address.
burnTokens(uint256 amount) external
Burns (destroys) a specified amount of Degen tokens from the sender's account.
store() public pure returns (string memory)
Returns a hardcoded string representing location data.
redeemTokens(uint256 choice) external payable
Allows users to redeem Degen tokens for a specific choice (location).
Requires a valid choice (1-5) and checks the user's balance before redemption.
Transfers tokens to the contract owner and records the redeemed location.
# Deployment
Compile the contract using the Solidity compiler v0.8.18.
Deploy the compiled contract to the Ethereum network.
Interact with the contract functions using an Ethereum wallet or a dApp browser.
# Disclaimer
This smart contract is provided as-is, without any warranty or guarantee. Use at your own risk. The contract's functionality and behavior are subject to the Solidity version and external dependencies used during deployment.
