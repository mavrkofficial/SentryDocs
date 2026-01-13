# Setting Up Payout Wallets

Payout wallets are your personal Solana wallet addresses where you receive profit distributions and dividends from group trading.

## What is a Payout Wallet?

A **payout wallet** is your personal Solana wallet address that:
- ✅ Receives profit distributions when trades are sold for profit
- ✅ Receives dividends from the group pool
- ✅ Receives bundle distributions (if applicable)
- ✅ Is used for all profit-sharing mechanisms

**Important**: You must set a payout wallet to receive any profit distributions!

## Who Can Set a Payout Wallet?

- ✅ **Traders**: All users with trader permissions can set payout wallets
- ✅ **Auto-addition**: Setting a payout wallet automatically adds you as a trader (if not already)

## Setting Your Payout Wallet

### Command
```
/payout [your_wallet_address]
```

Replace `[your_wallet_address]` with your Solana wallet address (base58 format, 32-44 characters).

### Example
```
/payout 7xKXtg2CW87d97TXJSDpbD5jBkheTqA83TZRuJosgAsU
```

### What Happens
- ✅ Your payout wallet is saved
- ✅ You're automatically added as a trader (if not already)
- ✅ You'll receive profit distributions to this address
- ✅ You appear in `/payoutset` list

## Viewing All Payout Wallets

### Command
```
/payoutset
```

This shows all traders who have set payout wallets and are eligible to receive distributions.

### What You'll See
- List of all users with payout wallets configured
- Usernames and wallet addresses
- Status indicators

## Wallet Address Format

Your payout wallet address should be:
- **Format**: Base58 encoded Solana address
- **Length**: 32-44 characters
- **Example**: `7xKXtg2CW87d97TXJSDpbD5jBkheTqA83TZRuJosgAsU`

### Valid Wallet Types
- ✅ Phantom wallet addresses
- ✅ Solflare wallet addresses
- ✅ Any standard Solana wallet (SPL-compatible)

## Changing Your Payout Wallet

To update your payout wallet address:

1. Run the `/payout` command again with your new address
2. Your old address will be replaced with the new one
3. All future distributions will go to the new address

**Note**: Previous distributions cannot be redirected to a new address.

## Why You Need a Payout Wallet

Without a payout wallet:
- ❌ You won't receive profit distributions
- ❌ You won't receive dividends from group pool
- ❌ You won't receive bundle distributions
- ✅ You can still trade, but profits go to others

**Always set your payout wallet before trading!**

## Profit Distribution Flow

When a profitable trade is sold:

1. **Profit Calculation**: Net profit is calculated (after fees)
2. **Refill Wallet**: Group wallet is refilled to minimum balance
3. **Distribution**: Remaining profit is distributed to payout wallets
4. **Top Traders**: Top 3 traders (by PnL) receive percentages (if configured)
5. **Group Pool**: Remaining amount split among all payout wallets

### Distribution Structure

**Default (Even Distribution)**:
- All payout wallets receive equal shares

**Custom Distribution** (if `/setrewards` is configured):
- 🥇 1st place: Custom percentage (e.g., 25%)
- 🥈 2nd place: Custom percentage (e.g., 15%)
- 🥉 3rd place: Custom percentage (e.g., 10%)
- 👥 Group Pool: Remaining amount split evenly

## Security Best Practices

### Protecting Your Wallet

1. **Use a secure wallet**: Use a reputable wallet (Phantom, Solflare)
2. **Keep private keys safe**: Never share your private key
3. **Verify address**: Double-check your address before setting it
4. **Use a separate wallet**: Consider using a separate wallet for group distributions
5. **Regular checks**: Verify you're receiving distributions correctly

### Common Mistakes

- ❌ Using an exchange address (may not support SPL tokens)
- ❌ Typos in wallet address (always verify)
- ❌ Using the Group Wallet address (won't work)
- ❌ Forgetting to set payout wallet before trading

## Troubleshooting

### "Invalid Solana address" error

**Solutions**:
- ✅ Check the address is correct (32-44 characters)
- ✅ Verify it's a valid Solana address format
- ✅ Make sure there are no extra spaces
- ✅ Copy the address directly from your wallet

### Not receiving distributions

**Check**:
- ✅ Verify payout wallet is set: Check `/payoutset` list
- ✅ Confirm you're a trader: Use `/traderslist`
- ✅ Check wallet address is correct: Verify with `/payoutset`
- ✅ Verify you've made trades: Check `/stats`
- ✅ Check wallet on Solana explorer: Verify address exists

### "You must be a trader" error

**Solutions**:
- ✅ Ask group owner to add you: `/addtrader @username`
- ✅ Setting payout wallet auto-adds you as trader
- ✅ Verify you're in the group

## FAQ

### Can I use multiple payout wallets?
No, you can only have one payout wallet per user. Update it with `/payout` if you need to change it.

### Do I need to set a payout wallet for each group?
Yes, payout wallets are set per group. Set it once per group you trade in.

### Can I use an exchange address?
Not recommended. Exchange addresses may not support all token types. Use a proper Solana wallet.

### When do I receive distributions?
Distributions are sent automatically when profitable trades are sold.

### How do I verify my payout wallet?
Use `/payoutset` to see your address in the list, or check your wallet for incoming transactions.

---

*Always set your payout wallet before making trades to ensure you receive profit distributions! Use `/payoutset` to verify all payout wallets are configured.*
