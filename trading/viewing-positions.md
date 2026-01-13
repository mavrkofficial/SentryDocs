# Viewing Positions

The `/positions` command shows all active token positions, their current value, PnL, and performance metrics.

## Command Syntax

```
/positions [@username]
```

### Parameters
- `[@username]`: Optional - filter to show only one user's positions
- If no username: Shows all active positions in the group

### Examples

**View All Positions**:
```
/positions
```

**View Specific User's Positions**:
```
/positions @johndoe
```

## What You'll See

The `/positions` command displays:

- **All active positions** for the group (or user)
- **Token information**: Name, symbol, address
- **Entry price**: Price when position was opened
- **Current price**: Real-time price from DexScreener
- **Position size**: Amount of tokens held
- **Invested amount**: Total SOL invested
- **Current value**: Current USD value of position
- **PnL**: Profit/Loss in USD
- **ROI**: Return on Investment percentage
- **DCA history**: All buy points (Entry, DCA 1, DCA 2, etc.)
- **Quick actions**: Links to sell or take profit

## Position Details

For each position, you'll see:

### Basic Information
- Token name and symbol
- Token address
- Caller username
- Position ID

### Price Information
- Entry price (USD)
- Current price (USD)
- Price change since entry

### Financial Metrics
- Amount invested (SOL)
- Current value (USD)
- PnL (Profit/Loss in USD)
- ROI (Return on Investment %)

### Position Size
- Total tokens held
- Average entry price (if DCA was used)

### DCA History
If DCA was used, you'll see:
- Entry: Original purchase
- DCA 1: First additional purchase
- DCA 2: Second additional purchase
- etc.

### Quick Actions
- Links to `/tp` (take profit)
- Links to `/sell` (sell position)

## Example Output

```
📊 Active Positions

🪙 Token: SENTRY ($SENTRY)
📍 Address: 55592jXxdwmCxERy2YmpJMi7MGcqJ6kwYJ2Ztrro7XfX
👤 Caller: @johndoe
💰 Invested: 0.5 SOL ($75.00)
💵 Current Value: $112.50
📈 PnL: +$37.50
🎯 ROI: +50.0%
📊 Entry: $0.001
📊 Current: $0.0015

🔄 DCA History:
  • Entry: $0.001 (50,000 tokens)
  • DCA 1: $0.0008 (62,500 tokens)

[Take Profit] [Sell]
```

## Portfolio Summary

At the bottom, you'll see a summary:

- **Total Invested**: Sum of all positions
- **Total Current Value**: Current value of all positions
- **Total PnL**: Combined profit/loss
- **Number of positions**: Count of active trades

## Using Position Information

### Making Decisions

Use position data to:

- ✅ **Monitor performance**: See how positions are doing
- ✅ **Make exit decisions**: Decide when to sell or take profit
- ✅ **Plan DCA**: See if averaging down makes sense
- ✅ **Track strategy**: Review your trading performance
- ✅ **Coordinate with group**: Share information with traders

### Quick Actions

From the positions list, you can:

- Click **Take Profit** buttons to sell partial amounts
- Click **Sell** buttons to sell entire positions
- Use position IDs for quick commands: `/tp_[id]` or `/sell_[id]`

## Best Practices

### Regular Monitoring

- ✅ Check positions regularly: `/positions`
- ✅ Monitor price movements
- ✅ Review PnL trends
- ✅ Track entry prices

### Analysis

- ✅ Review ROI on each position
- ✅ Compare performance across positions
- ✅ Identify best/worst performers
- ✅ Learn from your trades

### Decision Making

- ✅ Use data to make exit decisions
- ✅ Set profit targets based on ROI
- ✅ Identify positions that need attention
- ✅ Plan DCA strategies

## Filtering by User

To see only one user's positions:

```
/positions @username
```

This is useful for:
- ✅ Checking your own positions
- ✅ Reviewing another trader's performance
- ✅ Coordinating with specific traders
- ✅ Analyzing individual strategies

## Common Questions

### Why don't I see a position?

**Possible reasons**:
- Position was already sold
- You're filtering by username and it's not your position
- Position doesn't exist (check token address)

### Price seems wrong

**Note**: Prices are from DexScreener and update in real-time. There may be slight delays or differences from other sources.

### How do I use the quick action buttons?

Click the inline keyboard buttons (Take Profit, Sell) that appear below each position in the message.

## Related Commands

- `/balance` - View wallet balance and portfolio value
- `/stats` - View personal trading statistics
- `/pnl` - Comprehensive P&L report
- `/leaderboard` - See top performers

---

*Use `/positions` regularly to monitor your trades and make informed decisions. Check it before making exit decisions!*
