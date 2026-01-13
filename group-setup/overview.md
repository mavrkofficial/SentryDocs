# Group Setup Overview

Setting up your group correctly is essential for smooth trading operations. This section covers all aspects of group configuration, from initial setup to advanced settings.

## Setup Checklist

- ✅ [Initial Setup](./initial-setup.md) - Initialize the bot and create wallets
- ✅ [Understanding Wallets](./wallets.md) - Learn about Group Wallet and Deployer Wallet
- ✅ [Configuring Traders](./traders.md) - Add and manage traders
- ✅ [Setting Up Payout Wallets](./payout-wallets.md) - Configure profit distribution
- ✅ [Group Settings](./settings.md) - Configure buy amounts, minimum balance, and more

## Quick Reference

### Essential Commands for Group Owners

| Command | Description |
|---------|-------------|
| `/start` | Initialize the bot (owner only) |
| `/addtrader @username` | Add a user as a trader |
| `/removetrader @username` | Remove trader permissions |
| `/traderslist` | View all traders |
| `/settings [amount]` | Set default buy amount (0.1-5.0 SOL) |
| `/setminbal [amount]` | Set minimum reserve balance |
| `/setname [name]` | Set custom group name |
| `/setpfp` | Set group profile picture |
| `/setrewards [1st%] [2nd%] [3rd%]` | Configure profit distribution |

### Essential Commands for Traders

| Command | Description |
|---------|-------------|
| `/payout [address]` | Set your payout wallet |
| `/payoutset` | View all payout wallets |
| `/call [address]` | Buy a token |
| `/sell [address]` | Sell a position |
| `/tp [address]` | Take profit (partial sell) |
| `/dca [address]` | Dollar-cost average |

## Understanding Permissions

Sentry Bot uses a **trader-based permission system**:

- **Group Owner**: Full control, can deploy tokens, manage settings
- **Traders**: Can execute trades, set payout wallets
- **Members**: Can contribute funds, receive profit distributions

**Important**: Trading permissions are separate from Telegram admin status. You don't need to be a Telegram admin to trade - you just need trader permissions.

## What's Next?

Choose a topic to learn more:

1. **[Initial Setup](./initial-setup.md)** - First-time setup steps
2. **[Configuring Traders](./traders.md)** - Add and manage traders
3. **[Group Settings](./settings.md)** - Configure all group options
4. **[Payout Wallets](./payout-wallets.md)** - Set up profit distribution
