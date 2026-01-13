# Quick Start Guide

Get your Telegram group trading with Sentry Bot in just a few minutes!

## Step 1: Add the Bot to Your Group

1. Open your Telegram group (must be a **private group** or **supergroup**)
2. Add the Sentry Bot as a member
   - Search for `@SentryBot` (or the bot's username)
   - Click "Add to Group"
3. **Important**: The bot must be in a private group (not public channels)

## Step 2: Promote the Bot to Admin

This step is **essential** - the bot needs admin permissions to read messages and function correctly.

1. Open your group settings
2. Go to "Administrators"
3. Find Sentry Bot in the member list
4. Click "Promote to Admin"
5. Grant the bot permission to:
   - Read messages ✅
   - Delete messages (optional)
   - Pin messages (optional)

**Why is this needed?** The bot needs to read messages to detect token addresses, respond to commands, and track trading activity.

## Step 3: Initialize the Bot

1. In your group, type:
   ```
   /start
   ```
2. The bot will prompt you for a **group name** (if this is the first time)
3. The bot will create two wallets:
   - **Group Wallet**: For trading (main wallet)
   - **Deployer Wallet**: For token deployments (created automatically)

You'll see a message like this:

```
🛡️ Sentry Bot Initialized

📊 Group Name: Your Group Name
🆔 Chat ID: [number]
💳 Group Wallet: [address]
🚀 Deployer Wallet: [address]

⚠️ IMPORTANT:
1. Deposit SOL to Group Wallet to trade.
2. Deposit SOL to Deployer Wallet for token deployments (~0.1 SOL per deployment).
3. Make Sentry an Admin to function correctly.
4. Current Plan: Free (2.5% Fee on Profits).
```

## Step 4: Fund Your Group Wallet

The group wallet needs SOL to execute trades. Anyone can contribute!

1. Copy the **Group Wallet** address from the `/start` message
2. Send SOL to this address from any Solana wallet (Phantom, Solflare, etc.)
3. The bot requires a minimum balance (default 0.1 SOL) to trade

**Tip**: You can check your wallet balance anytime with `/balance`

## Step 5: Set Up Traders

Only users with "trader" permissions can execute trades. As the group owner:

1. **Add traders** with:
   ```
   /addtrader @username
   ```
2. **View all traders** with:
   ```
   /traderslist
   ```

**Note**: The group owner is automatically a trader. Previous admins may have been automatically migrated as traders.

## Step 6: Configure Settings (Optional)

### Set Buy Amount

Set the default SOL amount for each trade:
```
/settings 0.5
```
This sets the buy amount to 0.5 SOL per `/call` command.

**Range**: 0.1 - 5.0 SOL  
**Default**: 0.1 SOL

### Set Minimum Balance

Set how much SOL must remain in the wallet before profit distribution:
```
/setminbal 1.0
```
This ensures at least 1.0 SOL stays in the wallet.

## Step 7: Make Your First Trade!

Now you're ready to trade! Here's how:

1. **Call a token** (buy):
   ```
   /call 55592jXxdwmCxERy2YmpJMi7MGcqJ6kwYJ2Ztrro7XfX
   ```
   Replace the address with any Solana token address.

2. **Check your positions**:
   ```
   /positions
   ```

3. **Sell when ready**:
   ```
   /sell [token_address]
   ```
   Or reply to the original `/call` message with `/sell`

## Next Steps

Congratulations! Your group is now set up. Learn more about:

- **[Trading Commands](../trading/overview.md)** - Master all trading features
- **[Setting Up Traders](../group-setup/traders.md)** - Manage trader permissions
- **[Profit Distribution](../profit-distribution/overview.md)** - Understand how profits are shared
- **[Token Deployment](../deployment/overview.md)** - Launch your own tokens

## Common Issues

### Bot doesn't respond to commands
- ✅ Make sure the bot is an **admin**
- ✅ Check that the group is **private** (not a public channel)
- ✅ Verify you've run `/start` to initialize

### "Bot not initialized" error
- ✅ Run `/start` command (group owner only)
- ✅ Make sure you're the group owner/creator

### "You must be a trader" error
- ✅ Ask the group owner to add you: `/addtrader @yourusername`
- ✅ Or set a payout wallet: `/payout [your_wallet_address]`

---

*Need help? Use `/info` to see all available commands, or `/howto` for a quick reference guide.*
