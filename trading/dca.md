# Dollar-Cost Averaging (DCA)

The `/dca` command allows you to add more tokens to an existing position, effectively lowering your average entry price or increasing position size.

## What is DCA?

**Dollar-Cost Averaging (DCA)** means buying more of a token you already hold. In Sentry Bot, this:

- Adds to your existing position
- Calculates a new weighted average entry price
- Increases your total position size
- Maintains a history of all buy points

## Command Syntax

```
/dca <token_address>
```

### Parameters
- `<token_address>`: The Solana token address of your existing position

## How It Works

1. **Finds Active Position**: Bot locates your existing position for the token
2. **Uses Buy Amount**: Spends the amount set by `/settings` command
3. **Executes Buy**: Purchases more tokens at current market price
4. **Calculates Average**: Computes new weighted average entry price
5. **Updates Position**: Increases position size and updates entry price
6. **Records History**: Tracks all DCA points ("DCA 1", "DCA 2", etc.)

## Requirements

Before using DCA:

- ✅ You must be a **trader**
- ✅ Active position must exist for the token
- ✅ Group Wallet must have sufficient SOL
- ✅ Cannot DCA if no active position exists

## When to Use DCA

### Use DCA When:

- ✅ **Averaging down**: Token price dropped, want to lower average entry
- ✅ **Adding to winners**: Token is performing well, want more exposure
- ✅ **Building position**: Gradually increasing position size
- ✅ **Price action**: Buying more at favorable prices

### Don't Use DCA When:

- ❌ **No position exists**: Use `/call` to create a new position first
- ❌ **Bad fundamentals**: Don't throw good money after bad
- ❌ **Panic buying**: Have a strategy, don't DCA emotionally

## Example Scenario

**Initial Call**:
- Buy: 0.5 SOL worth at $0.01
- Position: 50,000 tokens
- Entry Price: $0.01

**DCA 1** (price dropped to $0.008):
- Buy: 0.5 SOL worth at $0.008
- Additional: 62,500 tokens
- New Position: 112,500 tokens
- **New Average Entry**: ~$0.0089 (weighted average)

**DCA 2** (price dropped to $0.007):
- Buy: 0.5 SOL worth at $0.007
- Additional: ~71,429 tokens
- New Position: ~183,929 tokens
- **New Average Entry**: ~$0.0082 (weighted average)

## Entry Price Calculation

DCA uses **weighted average** to calculate the new entry price:

```
New Average = (Old Position Value + New Purchase Value) / Total Tokens
```

This means:
- ✅ Your average entry price decreases if buying at lower prices
- ✅ Your average entry price increases if buying at higher prices
- ✅ Position size always increases
- ✅ All buy points are tracked in history

## DCA History

All DCA points are tracked with labels:

- **Entry**: Original `/call` purchase
- **DCA 1**: First DCA purchase
- **DCA 2**: Second DCA purchase
- **DCA 3**: Third DCA purchase
- etc.

You can see this history in `/positions` command.

## Best Practices

### Strategy Tips

1. **Have a plan**: Know why you're DCAing
2. **Set limits**: Don't DCA indefinitely
3. **Consider price**: Better to DCA on dips than pumps
4. **Monitor position**: Keep track of your average entry
5. **Know when to stop**: Don't keep adding to losing positions

### Risk Management

- ✅ **Set maximum position size**: Don't over-concentrate
- ✅ **Use for strategy, not emotion**: Have a plan
- ✅ **Monitor wallet balance**: Don't drain the Group Wallet
- ✅ **Coordinate with group**: Let others know your strategy

### When to Stop DCAing

- ⚠️ Position size becomes too large
- ⚠️ Token fundamentals changed for worse
- ⚠️ Wallet balance getting low
- ⚠️ Reached your position size limit

## Common Issues

### "No active position found"

**Solutions**:
- You must have an active position first (use `/call`)
- Verify token address is correct
- Check `/positions` to see active trades

### "Insufficient SOL"

**Solutions**:
- Fund the Group Wallet
- Check balance: `/balance`
- Reduce buy amount if needed: `/settings [amount]`

### "You must be a trader"

**Solutions**:
- Ask owner to add you: `/addtrader @username`
- Or set payout wallet: `/payout [address]`

## DCA vs New Call

### Use DCA When:
- ✅ You already have a position
- ✅ You want to average your entry price
- ✅ You want to increase position size

### Use `/call` When:
- ✅ Starting a new position
- ✅ You don't have this token yet
- ✅ Creating a fresh entry

## Tips for Success

1. **DCA on dips**: Better entry prices
2. **Have limits**: Set max position size
3. **Track your average**: Monitor entry price changes
4. **Use strategically**: Not just because price moved
5. **Coordinate**: Work with other traders

## Example DCA Strategy

```
1. Initial Call: /call [address] at $0.01
2. Price drops to $0.008: /dca [address] (average down)
3. Price drops to $0.007: /dca [address] again
4. Monitor average entry price
5. Take profit when price recovers above average
```

---

*DCA is a powerful tool for managing entries. Use it strategically to build positions and lower your average cost!*
