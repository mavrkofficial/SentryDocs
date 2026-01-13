# Take Profit (Partial Selling)

The `/tp` command allows you to sell partial amounts of a position, letting you lock in profits while maintaining exposure to the token.

## What is Take Profit?

**Take Profit** lets you sell a percentage of your position (10%, 25%, 50%, 75%, or 100%) instead of selling the entire position. This is useful for:

- Locking in profits while holding some tokens
- Reducing position size gradually
- Testing exit strategies
- Managing risk on large positions

## Command Syntax

```
/tp <token_address>
```

### Parameters
- `<token_address>`: The Solana token address of the position

### Alternative Usage

You can reply to the original `/call` message:
```
/tp
```
(When replying, address is detected automatically)

## How It Works

1. Run `/tp` command
2. Bot shows interactive menu with percentage options
3. Select percentage to sell (10%, 25%, 50%, 75%, 100%)
4. Bot calculates amount to sell
5. Executes partial sell
6. Updates position size
7. Distributes profits (if profitable)

## Percentage Options

When you run `/tp`, you'll see buttons for:

- **10%**: Sell 10% of position
- **25%**: Sell 25% of position  
- **50%**: Sell 50% of position
- **75%**: Sell 75% of position
- **100%**: Sell entire position (same as `/sell`)
- **Cancel**: Cancel the operation

## Example Flow

```
1. Run: /tp 55592jXxdwmCxERy2YmpJMi7MGcqJ6kwYJ2Ztrro7XfX

2. Bot shows menu:
   📉 Take Profit: $SENTRY
   Select percentage to sell:
   [10%] [25%]
   [50%] [75%]
   [Cancel]

3. Click 25%

4. Bot sells 25% of position
5. Position size updated
6. Profits distributed (if profitable)
```

## Position Updates

After a partial sell:

- ✅ Position size is **reduced** by the sold percentage
- ✅ Entry price is **recalculated** (weighted average if DCA was used)
- ✅ Position remains **active** (unless 100% sold)
- ✅ PnL calculations update automatically

### Moonbagging

If you sell more than 50% of a position, it's marked as "moonbagged" - meaning you're holding a smaller amount as a long-term position.

## Profit Distribution

Profits from partial sells are distributed the same way as full sells:

- ✅ Fee deducted (2.5% free tier, 0% premium)
- ✅ Wallet refilled to minimum balance
- ✅ Remaining profit distributed to payout wallets
- ✅ Distribution follows configured reward structure

## When to Use Take Profit

### Use Take Profit When:

- ✅ **Locking in profits**: You're up and want to secure some gains
- ✅ **Reducing risk**: Large position that you want to reduce
- ✅ **Testing exits**: Want to see how partial sell feels
- ✅ **Gradual exit**: Exit strategy that involves multiple sells
- ✅ **Rebalancing**: Adjusting position size based on conditions

### Use Full Sell (`/sell`) When:

- ✅ **Complete exit**: You want to exit the entire position
- ✅ **Clean slate**: Starting fresh with new trades
- ✅ **Cutting losses**: Bad position you want to close completely

## Strategy Examples

### Conservative Strategy
- Sell 25% at 2x
- Sell another 25% at 3x
- Hold remaining 50% for longer term

### Aggressive Strategy
- Sell 50% at 1.5x (take profit quickly)
- Hold 50% for bigger gains

### Balanced Strategy
- Sell 10-25% at reasonable profit levels
- Hold majority for larger moves

## Best Practices

1. **Have a plan** before entering positions
2. **Set profit targets** for different percentages
3. **Don't be greedy** - take profits at reasonable levels
4. **Consider position size** - larger positions benefit more from partial sells
5. **Review after selling** - adjust strategy based on results

## Common Issues

### "Active trade not found"

**Solutions**:
- Verify token address is correct
- Check if position was already sold
- Use `/positions` to see active positions

### Menu doesn't appear

**Solutions**:
- Make sure you're using the command correctly
- Try replying to the original call message
- Verify you're a trader

### Can't select percentage

**Solutions**:
- Use the inline keyboard buttons
- Click the buttons (don't type the percentage)
- Try canceling and running `/tp` again

## Tips

1. **Start small**: Try 10-25% first to test the feature
2. **Monitor results**: See how partial sells affect your strategy
3. **Adjust over time**: Refine your take profit strategy
4. **Coordinate**: Let group know your strategy
5. **Be flexible**: Adjust based on market conditions

---

*Take profit is a powerful tool for managing positions. Use it to lock in gains while maintaining exposure!*
