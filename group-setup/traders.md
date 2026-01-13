# Configuring Traders

Traders are users who have permission to execute trades on behalf of the group. This guide explains how to manage trader permissions.

## What is a Trader?

A **trader** is a user who can:
- ✅ Execute `/call` commands (buy tokens)
- ✅ Execute `/sell` commands (sell positions)
- ✅ Use `/tp` command (take profit)
- ✅ Use `/dca` command (dollar-cost average)
- ✅ Set payout wallets with `/payout`

**Important**: Trading permissions are **separate** from Telegram admin status. Users don't need to be Telegram admins to trade - they just need trader permissions.

## Adding Traders

Only the **group owner** can add traders.

### Command
```
/addtrader @username
```

Replace `@username` with the Telegram username (without the @ symbol in the command).

### Example
```
/addtrader johndoe
```

This gives `@johndoe` permission to execute trades.

### What Happens
- ✅ User is added to the traders list
- ✅ User can now use all trading commands
- ✅ User can set a payout wallet
- ✅ User appears in `/traderslist`

## Removing Traders

To remove trading permissions:

### Command
```
/removetrader @username
```

### Example
```
/removetrader johndoe
```

### What Happens
- ✅ User loses trading permissions
- ✅ User can no longer use `/call`, `/sell`, `/tp`, `/dca`
- ✅ User is removed from traders list
- ⚠️ User's payout wallet setting is preserved (in case they're re-added)

## Viewing All Traders

### Command
```
/traderslist
```

### What You'll See
- List of all users with trader permissions
- Usernames and user IDs
- Status indicators

This is useful for:
- Checking who can trade
- Verifying trader status
- Managing permissions

## Automatic Trader Addition

Users are automatically added as traders in these cases:

1. **Setting a payout wallet**: When a user runs `/payout [address]`, they're automatically added as a trader
2. **Migration**: Existing users who had trading access before may have been automatically migrated

**Note**: The group owner is always a trader and cannot be removed.

## Trader Permissions Explained

### What Traders CAN Do
- ✅ Execute all trading commands (`/call`, `/sell`, `/tp`, `/dca`)
- ✅ Set their payout wallet (`/payout`)
- ✅ View positions and analytics
- ✅ Use all analytics commands

### What Traders CANNOT Do
- ❌ Add or remove other traders (owner only)
- ❌ Change group settings (`/settings`, `/setminbal`, etc.)
- ❌ Deploy tokens (`/deploy` - owner only)
- ❌ Withdraw funds directly
- ❌ Configure bundle wallets (owner only)
- ❌ Set harvest wallet (owner only)

## Best Practices

### Managing Traders

1. **Start small**: Begin with 2-3 trusted traders
2. **Verify users**: Make sure you trust users before adding them
3. **Regular reviews**: Use `/traderslist` to review who has access
4. **Remove inactive traders**: Clean up traders who are no longer active
5. **Clear communication**: Let traders know their responsibilities

### Security Tips

- 🔒 Only add trusted users as traders
- 🔒 Regularly review your traders list
- 🔒 Remove traders who leave the group
- 🔒 Don't give trader permissions to new/unverified members
- 🔒 Monitor trading activity with `/positions` and `/stats`

### Trader Responsibilities

Traders should:
- ✅ Execute trades in the group's best interest
- ✅ Set payout wallets to receive distributions
- ✅ Coordinate with other traders
- ✅ Follow group trading strategies (if any)
- ✅ Be active and responsive

## Common Scenarios

### Adding a New Member as Trader
1. Verify the user is legitimate
2. Confirm they understand trading responsibilities
3. Run `/addtrader @username`
4. Ask them to set payout wallet: `/payout [address]`

### Removing an Inactive Trader
1. Check if they're still active: `/traderslist`
2. Review their recent activity: `/stats @username`
3. Remove if inactive: `/removetrader @username`

### Temporarily Disabling Trading
If you need to pause trading temporarily:
1. Remove all traders except yourself: `/removetrader @username` (repeat)
2. Re-add traders when ready: `/addtrader @username`

**Note**: You cannot remove yourself (group owner always has trader permissions).

## Troubleshooting

### "User not found" error
- ✅ Check the username is correct (case-sensitive)
- ✅ Make sure the user is in the group
- ✅ Verify the username format (without @ in command)

### User says they can't trade
- ✅ Check if they're in `/traderslist`
- ✅ Verify they're using commands correctly
- ✅ Try removing and re-adding them

### "Only group owners can use this command"
- ✅ Only the group owner/creator can add/remove traders
- ✅ Admins cannot add traders (only owners)

---

*Use `/traderslist` regularly to manage your traders. Remember: trader permissions are separate from Telegram admin status!*
