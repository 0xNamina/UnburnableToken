# UnburnableToken

Simple token implementation with claim mechanism and safe transfer functionality.

## Description

This contract implements a basic token system without ERC-20 compliance, featuring a one-time claim mechanism and safe transfer functions. The token has a fixed supply of 100 million tokens with no decimal places, and each address can claim exactly 1,000 tokens once.

## Features

- **Fixed Supply**: 100,000,000 tokens total (no decimals)
- **One-time Claim**: Each address can claim 1,000 tokens exactly once
- **Safe Transfers**: Enhanced transfer safety with recipient validation
- **Custom Errors**: Gas-efficient error handling

## Safety Mechanisms

- **Zero Address Check**: Prevents transfers to zero address
- **ETH Balance Check**: Recipients must have > 0 Base Sepolia ETH
- **Sufficient Balance Check**: Validates sender has enough tokens
- **Claim Validation**: Prevents double claims and over-claiming

## Token Economics

- Total Supply: 100,000,000 tokens
- Claim Amount: 1,000 tokens per address
- Decimals: 0 (whole numbers only)
- Maximum Claims: 100,000 unique addresses

## Deployment Instructions

1. Open [Remix IDE](https://remix.ethereum.org/)
2. Create a new file and copy-paste the contract code
3. Compile the contract using Solidity ^0.8.0
4. Deploy on **Base Sepolia Testnet**
5. Interact with the functions:
   - `claim()` - Claim your 1,000 tokens (once per address)
   - `safeTransfer(address _to, uint256 _amount)` - Transfer tokens safely
   - `balances(address)` - Check token balance
   - `hasClaimed(address)` - Check if address has claimed

## Submit Exercise

[📖 Submit Minimal Tokens Exercise](https://docs.base.org/learn/token-development/minimal-tokens/minimal-tokens-exercise)
