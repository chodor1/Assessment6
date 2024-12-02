# DegenToken Smart Contract

## Overview
DegenToken is a custom ERC20 token built for gamified environments. This smart contract combines the standard ERC20 functionality with features like token redemption for in-game items and inventory management. It is written in Solidity and leverages the OpenZeppelin library for secure and robust implementation.

## Features
- **ERC20 Token**:
  - Token Name: `Degen`
  - Token Symbol: `DGN`
  - Decimals: `0` (non-fractional tokens)
- **Minting and Burning**:
  - The owner can mint new tokens.
  - Users can burn tokens from their balance.
- **In-Game Economy**:
  - Redeem tokens for predefined in-game items.
  - Track owned items through inventory functions.
- **Secure and Transparent**:
  - Utilizes OpenZeppelin's `Ownable` for access control.
  - Includes events for tracking significant actions like item redemption.

## Contract Details
- **Solidity Version**: ^0.8.18
- **License**: MIT

## Functions

### Token Management
| Function       | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| `mint(address to, uint256 amount)` | Allows the owner to mint tokens to a specific address. |
| `burnTokens(uint256 amount)`      | Users can burn tokens from their balance.              |
| `transferTokens(address recipient, uint256 amount)` | Enables users to transfer tokens to others. |

### Game Item Functions
| Function        | Description                                                                 |
|-----------------|-----------------------------------------------------------------------------|
| `redeem(uint256 itemId)` | Redeem tokens for a predefined game item.                         |
| `getGameItems()` | Fetches the list of all available game items.                             |
| `getOwnedItems()` | Retrieves the list of items owned by the caller.                        |

### Utility Functions
| Function        | Description                                                                 |
|-----------------|-----------------------------------------------------------------------------|
| `decimals()`    | Returns the number of decimals (set to 0 for non-fractional tokens).        |
| `getBalance()`  | Returns the token balance of the caller.                                   |
