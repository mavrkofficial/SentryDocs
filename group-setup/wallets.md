# Understanding Wallets

Sentry Bot uses two separate Solana wallets for different purposes. Understanding the difference is important for proper group management.

## Group Wallet

The **Group Wallet** is the main trading wallet that holds your group's trading capital.

### Purpose
- Stores SOL for executing trades
- Holds token positions purchased by the group
- Receives profits from sold positions
- Used for all `/call`, `/sell`, `/dca`, and `/tp` commands

### Funding
- **Anyone can contribute**: Send SOL to the Group Wallet address
- **No minimum required**: But you need at least 0.1 SOL to execute trades
- **Recommended starting amount**: 0.5 - 1.0 SOL

### Viewing Balance
```
/balance
```
Shows:
- SOL balance
- USD value
- Portfolio value (including token positions)

### Wallet Address
View the address with:
```
/wallet
```
Or check the message you received after `/start`.

### Important Notes
- ⚠️ **Don't send tokens directly** - Only send SOL
- ⚠️ **Keep some SOL for gas fees** - Reserve 0.01-0.05 SOL
- ⚠️ **Monitor balance** - Use `/balance` regularly

## Deployer Wallet

The **Deployer Wallet** is used exclusively for token deployments.

### Purpose
- Pays for token deployment transactions
- Funds bundle buys (if enabled during deployment)
- Used for the `/deploy` command

### Funding
- **Only needed for deployments**: Fund only if you plan to deploy tokens
- **Cost per deployment**: ~0.045 SOL (gas fees)
- **Bundle buy funding**: Additional SOL if you enable bundle buys

### Viewing Balance
```
/wallet
```
Shows both Group Wallet and Deployer Wallet balances.

### When to Fund

Fund the Deployer Wallet when:
- ✅ You're about to deploy a token (`/deploy`)
- ✅ You want to enable bundle buys on deployment
- ✅ You plan to use the "first buyer" feature

**Don't fund if**: You only want to trade existing tokens (use Group Wallet instead).

## Wallet Management

### Checking Both Wallets
```
/wallet
```

This command shows:
- Group Wallet address and balance (SOL & USD)
- Deployer Wallet address and balance (SOL & USD)
- Quick access to both addresses

### Funding Tips

**Group Wallet**:
- Start with 0.5-1.0 SOL
- Add more as your group grows
- Multiple members can contribute
- Keep at least 0.1 SOL for trading

**Deployer Wallet**:
- Fund only when needed
- ~0.1 SOL per deployment is usually sufficient
- Add extra if using bundle buys
- Can be funded by the owner only

### Security Notes

- 🔒 **Private keys are encrypted** and stored securely by the bot
- 🔒 **Only the bot can access wallets** - you can't export private keys
- 🔒 **Group owner controls settings** - but can't directly control wallet funds
- 🔒 **Traders can only execute trades** - they can't withdraw funds directly

### Withdrawing Funds

To withdraw from Group Wallet:
```
/withdraw [amount] [address]
```

**Note**: This requires multi-sig approval from admins (2/3 approval needed).

To withdraw from Deployer Wallet:
```
/deployerwithdraw [amount]
```

**Note**: Owner only, withdraws to harvest wallet if set.

## Best Practices

1. **Separate funding**: Keep Group Wallet and Deployer Wallet funded separately
2. **Monitor balances**: Check `/balance` and `/wallet` regularly
3. **Reserve SOL**: Always keep some SOL for gas fees
4. **Group contributions**: Encourage members to contribute to Group Wallet
5. **Deployer funding**: Only fund Deployer Wallet when deploying tokens

## Common Questions

### Can I use the same wallet for both?
No, they're separate wallets by design for security and organization.

### Who controls the wallets?
The bot controls the wallets. The group owner controls settings, but funds are managed by the bot's smart contract logic.

### Can traders withdraw funds?
No, traders can only execute trades. Withdrawals require multi-sig approval or owner-only commands.

### What happens if I lose access to the group?
Contact support immediately. Wallet recovery is possible but requires verification.

---

*Use `/wallet` anytime to view your wallet addresses and balances. Use `/balance` for a quick Group Wallet check.*
