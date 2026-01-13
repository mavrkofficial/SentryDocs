# Selling Positions

The `/sell` command allows you to sell an entire token position, converting it back to SOL and automatically distributing profits if the trade was profitable.

## Command Syntax

```
/sell <token_address>
```

### Parameters
- `<token_address>`: The Solana token address of the position to sell

### Alternative Usage

You can also reply to the original `/call` message:
```
/sell
```
(When replying to the original call message, address is detected automatically)

## How It Works

1. **Position Verification**: Bot checks for active position
2. **Balance Check**: Verifies token balance in Group Wallet
3. **Price Check**: Fetches current price from DexScreener
4. **Swap Execution**: Sells 100% of position via Jupiter or Orca
5. **PnL Calculation**: Calculates profit/loss
6. **Profit Distribution**: If profitable, distributes profits automatically
7. **Position Update**: Marks position as sold in database

## What Happens After Selling

### If Profitable
- ✅ SOL is added to Group Wallet
- ✅ Wallet is refilled to minimum balance (if configured)
- ✅ Profits are distributed to payout wallets
- ✅ Position is marked as sold
- ✅ PnL is recorded for leaderboard/statistics

### If Not Profitable
- ✅ SOL is added to Group Wallet
- ✅ Position is marked as sold
- ✅ Loss is recorded (no distribution)
- ✅ Group wallet balance increases (but less than invested)

## Profit Distribution

When a profitable trade is sold:

1. **Fee Deduction**: 2.5% platform fee (free tier) or 0% (premium)
2. **Refill Wallet**: Group wallet refilled to minimum balance (if set)
3. **Calculate Distributable**: Remaining profit after refill
4. **Distribute**:
   - Top 3 traders get percentages (if configured)
   - Remaining amount split among all payout wallets
5. **Transaction**: SOL sent to payout wallets

See [Profit Distribution Guide](../profit-distribution/overview.md) for details.

## Requirements

Before selling:

- ✅ You must be a **trader**
- ✅ Active position must exist for the token
- ✅ Position must have a token balance

## Example

**Sell by Address**:
```
/sell 55592jXxdwmCxERy2YmpJMi7MGcqJ6kwYJ2Ztrro7XfX
```

**Sell by Reply**:
1. Find the original `/call` message
2. Reply to it with `/sell`
3. Address is detected automatically

## What You'll See

After selling, you'll receive a message showing:

- ✅ Transaction signature
- ✅ Amount sold (SOL received)
- ✅ Entry price vs exit price
- ✅ PnL (profit/loss)
- ✅ ROI percentage
- ✅ Distribution details (if profitable)

### Example Output

```
✅ Sold Position: SENTRY

💰 Amount: 100,000 tokens
💵 Received: 1.25 SOL
📊 Entry: $0.001
📊 Exit: $0.0015
📈 PnL: +$50.00 (+50.0%)
🎯 ROI: +50.0%

💸 Profits distributed to payout wallets
```

## Best Practices

### Before Selling

1. **Check position status**
   ```
   /positions
   ```
   Verify current PnL and price

2. **Review strategy**
   - Is this a good exit point?
   - Should you take partial profit instead? (`/tp`)
   - Consider market conditions

3. **Coordinate with group**
   - Let others know you're selling
   - Check if others want to sell too
   - Consider group strategy

### Selling Strategy

- ✅ **Take profits** when targets are met
- ✅ **Cut losses** if position is bad
- ✅ **Consider partial sells** (`/tp`) for large positions
- ✅ **Don't panic sell** - stick to strategy

### After Selling

- ✅ Verify transaction completed
- ✅ Check Group Wallet balance: `/balance`
- ✅ Verify profits distributed (if profitable)
- ✅ Review performance: `/stats`

## Common Issues

### "Active trade not found for this token"

**Solutions**:
- Verify token address is correct
- Check if position was already sold: `/positions`
- Make sure position exists in this group

### "No balance found"

**Solutions**:
- Position may have already been sold
- Check wallet balance directly
- Use `/cleanup` to verify positions (owner only)

### Transaction Fails

**Possible causes**:
- Insufficient balance for gas fees
- Token has restrictions
- Network congestion
- Liquidity issues

**Solutions**:
- Ensure wallet has SOL for gas (0.01-0.05 SOL)
- Try again later if network is busy
- Check token liquidity on DexScreener

### "Insufficient balance"

**Solutions**:
- Position may have already been sold
- Check actual wallet balance
- Use `/positions` to verify position exists

## Selling vs Take Profit

### Use `/sell` When:
- ✅ You want to exit the entire position
- ✅ Position is at your target
- ✅ You're cutting losses
- ✅ You want to free up capital

### Use `/tp` (Take Profit) When:
- ✅ You want to sell partial amounts
- ✅ Locking in profits while holding some
- ✅ Reducing position size gradually
- ✅ Testing exit strategy

## Tips

1. **Have an exit strategy** before entering positions
2. **Take profits** at reasonable levels
3. **Cut losses** if position turns bad
4. **Consider partial sells** for large positions
5. **Monitor regularly** to catch good exit points

## Example Selling Flow

```
1. Check positions: /positions
2. Review PnL and current price
3. Decide to sell: /sell [address]
4. Verify transaction completed
5. Check balance: /balance
6. Review performance: /stats
```

---

*Ready to sell? Make sure you've reviewed the position and have a strategy. Consider using /tp for partial sells on large positions!*
