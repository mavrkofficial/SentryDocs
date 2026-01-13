# Group Settings

This guide covers all configurable settings for your trading group. These settings help you customize how Sentry Bot operates in your group.

## Available Settings

### Buy Amount (`/settings`)

Sets the default SOL amount used for each `/call` command.

#### Command
```
/settings [amount]
```

#### Parameters
- `[amount]`: SOL amount (0.1 to 5.0)
- If no amount specified, shows current setting

#### Examples
```
/settings 0.5
```
Sets buy amount to 0.5 SOL per trade.

```
/settings
```
Shows current buy amount setting.

#### Default Value
- **Default**: 0.1 SOL
- **Minimum**: 0.1 SOL
- **Maximum**: 5.0 SOL

#### Who Can Change
- **Owner only**: Only the group owner can change this setting

#### Best Practices
- Start with 0.1-0.5 SOL for testing
- Adjust based on group size and capital
- Consider your Group Wallet balance
- Larger amounts = larger positions = higher risk/reward

### Minimum Balance (`/setminbal`)

Sets how much SOL must remain in the Group Wallet before profit distributions.

#### Command
```
/setminbal [amount]
```

#### Parameters
- `[amount]`: SOL amount to reserve
- Default: 0 SOL (no reserve)

#### Example
```
/setminbal 1.0
```
Ensures at least 1.0 SOL stays in the wallet before distributions.

#### Purpose
- Prevents wallet from being completely drained
- Maintains liquidity for future trades
- Ensures gas fees are available

#### Who Can Change
- **Owner only**: Only the group owner can change this

#### How It Works
When a trade is sold for profit:
1. Wallet is refilled to the minimum balance
2. Only profits above this amount are distributed
3. Ensures wallet always has the reserve amount

### Group Name (`/setname`)

Sets a custom name for your group (used in leaderboards and alpha channel alerts).

#### Command
```
/setname [name]
```

#### Parameters
- `[name]`: Custom group name (text)

#### Example
```
/setname Alpha Traders
```

#### Where It's Used
- Leaderboard displays
- Alpha channel notifications
- Analytics and reporting

#### Who Can Change
- **Owner only**: Only the group owner can change this

### Group Profile Picture (`/setpfp`)

Sets a custom profile picture for your group.

#### Command
```
/setpfp
```

#### How to Use
1. Run `/setpfp` command
2. Bot will prompt you to send an image
3. Send your image (photo or file)
4. Bot will save it as the group profile picture

#### Supported Formats
- PNG
- JPEG/JPG
- Other common image formats

#### Who Can Change
- **Owner only**: Only the group owner can change this

### Reward Distribution (`/setrewards`)

Configures custom profit distribution percentages for top traders.

#### Command
```
/setrewards [1st%] [2nd%] [3rd%]
```

#### Parameters
- `[1st%]`: Percentage for 1st place trader
- `[2nd%]`: Percentage for 2nd place trader
- `[3rd%]`: Percentage for 3rd place trader
- Use `reset` to return to default (even distribution)

#### Examples

**Custom Distribution**:
```
/setrewards 25 15 10
```
- 1st place: 25%
- 2nd place: 15%
- 3rd place: 10%
- Group pool: 50% (remaining, split evenly)

**Reset to Default**:
```
/setrewards reset
```
Returns to even distribution (all payout wallets get equal shares).

#### Default Behavior
- **Default**: Even distribution (all payout wallets receive equal shares)
- **Custom**: Set percentages for top 3, remainder split evenly

#### Who Can Change
- **Owner only**: Only the group owner can change this

#### Important Notes
- Percentages should total less than 100% (remainder goes to group pool)
- Rankings are based on realized PnL (closed trades)
- If fewer than 3 traders, unused percentages return to group wallet

## Viewing Current Settings

### Check Buy Amount
```
/settings
```
(Without amount parameter)

### Check All Settings
Use these commands to verify settings:
- `/settings` - Buy amount
- `/wallet` - Wallet balances (includes minimum balance info)
- `/info` - General information

## Settings Best Practices

### Buy Amount
- ✅ Start conservative (0.1-0.5 SOL)
- ✅ Adjust based on Group Wallet balance
- ✅ Consider group size and risk tolerance
- ✅ Monitor performance before increasing

### Minimum Balance
- ✅ Set a reserve (0.5-1.0 SOL recommended)
- ✅ Ensures you can always trade
- ✅ Prevents wallet depletion
- ✅ Adjust based on trading frequency

### Reward Distribution
- ✅ Start with default (even distribution)
- ✅ Switch to custom if you want to reward top performers
- ✅ Use percentages that total < 100%
- ✅ Consider group culture and goals

### Group Identity
- ✅ Set a clear, memorable group name
- ✅ Use a professional profile picture
- ✅ Keep branding consistent

## Common Settings Combinations

### Conservative Setup
```
/settings 0.1
/setminbal 0.5
/setrewards reset
```
- Small buy amounts
- Safety reserve
- Even distribution

### Aggressive Setup
```
/settings 1.0
/setminbal 0.1
/setrewards 25 15 10
```
- Larger positions
- Minimal reserve
- Rewards top performers

### Balanced Setup
```
/settings 0.5
/setminbal 1.0
/setrewards reset
```
- Medium positions
- Good reserve
- Fair distribution

## Troubleshooting

### "Only group owners can use this command"
- ✅ Only the group owner/creator can change settings
- ✅ Admins cannot change settings
- ✅ Verify you're the group owner

### Settings not saving
- ✅ Check command syntax
- ✅ Verify parameter ranges (e.g., 0.1-5.0 for buy amount)
- ✅ Try the command again
- ✅ Check bot is responding (may need to be admin)

### Want to reset to defaults
- **Buy amount**: `/settings 0.1`
- **Minimum balance**: `/setminbal 0`
- **Rewards**: `/setrewards reset`

---

*Settings are owner-only. Choose settings that match your group's goals and risk tolerance. Start conservative and adjust as you learn!*
