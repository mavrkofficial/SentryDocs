# Initial Setup

This guide walks you through the initial setup process for Sentry Bot in your Telegram group.

## Prerequisites

Before starting, make sure you have:

- ✅ A Telegram **private group** or **supergroup** (not a public channel)
- ✅ Group owner/creator permissions (only the owner can initialize)
- ✅ Ability to promote the bot to admin

## Step-by-Step Setup

### Step 1: Add the Bot

1. Open your Telegram group
2. Go to group settings → "Add Members"
3. Search for `@SentryBot` (or your bot's username)
4. Add the bot to the group

### Step 2: Promote to Admin

**This is essential** - the bot cannot function without admin permissions.

1. Go to group settings → "Administrators"
2. Find Sentry Bot in the list
3. Click "Promote to Admin"
4. Enable "Read Messages" permission (required)
5. Optional: Enable "Delete Messages" and "Pin Messages"

**Why is this needed?** The bot needs to read all messages to:
- Detect token addresses in chat
- Respond to commands
- Track trading activity
- Provide token information

### Step 3: Run /start Command

As the group owner, type:
```
/start
```

The bot will:
1. Prompt you for a **group name** (first time only)
2. Create a unique **Group Wallet** for trading
3. Create a **Deployer Wallet** for token deployments
4. Initialize all necessary settings

### Step 4: Save Your Wallet Addresses

After running `/start`, you'll receive a message with:
- **Group Wallet Address**: Send SOL here to fund trading
- **Deployer Wallet Address**: Send SOL here for token deployments

**Important**: Save these addresses! You'll need them to fund your wallets.

### Step 5: Fund Your Wallets

#### Fund Group Wallet (Required for Trading)

1. Copy the **Group Wallet** address
2. Send SOL from any Solana wallet (Phantom, Solflare, etc.)
3. Minimum recommended: 0.1 SOL to start trading

**Tip**: Anyone in the group can contribute to the Group Wallet!

#### Fund Deployer Wallet (Optional - for Token Deployments)

1. Copy the **Deployer Wallet** address
2. Send SOL for token deployments
3. Recommended: ~0.1 SOL per deployment

**Note**: Deployer Wallet is only needed if you plan to deploy tokens.

## Verification

After setup, verify everything is working:

1. **Check initialization**:
   ```
   /balance
   ```
   Should show your wallet balance (may be 0 if not funded yet)

2. **View settings**:
   ```
   /settings
   ```
   Should show current buy amount (default: 0.1 SOL)

3. **Test bot response**:
   ```
   /info
   ```
   Should display the command guide

## Next Steps

Once initialized, you can:

1. **[Add Traders](./traders.md)** - Give users trading permissions
2. **[Configure Settings](./settings.md)** - Set buy amounts, minimum balance, etc.
3. **[Set Up Payout Wallets](./payout-wallets.md)** - Configure profit distribution
4. **[Start Trading](../trading/overview.md)** - Make your first trade!

## Common Setup Issues

### "Only group owner can initialize"

**Solution**: Make sure you're the group creator/owner. Only the original group creator can run `/start`.

### Bot doesn't respond

**Solutions**:
- ✅ Verify bot is an admin
- ✅ Check "Read Messages" permission is enabled
- ✅ Ensure group is private (not a public channel)

### "Bot not initialized" errors

**Solution**: Run `/start` command as the group owner.

### Wallet addresses not showing

**Solution**: 
- Check that `/start` completed successfully
- Try running `/wallet` to view wallet addresses
- Verify you're the group owner

## Migration from Old System

If you're an existing group, your setup may have been automatically migrated:

- ✅ Existing admins may have been converted to traders
- ✅ Existing settings are preserved
- ✅ Wallet addresses remain the same

Use `/traderslist` to see who has trader permissions.

---

*Having issues? Make sure the bot is an admin and try `/start` again. Use `/info` to see all available commands.*
