# Trading Guide Overview

This section covers everything you need to know about trading with Sentry Bot. Learn how to buy tokens, manage positions, and execute profitable trades.

## Trading Basics

Sentry Bot allows authorized traders to execute trades on behalf of the group using the Group Wallet. All trades are tracked, and profits are automatically distributed to group members.

## Trading Commands

| Command | Description | Quick Reference |
|---------|-------------|-----------------|
| `/call <address>` | Buy a token | [Call Guide](./calling-tokens.md) |
| `/sell <address>` | Sell entire position | [Selling Guide](./selling-positions.md) |
| `/tp <address>` | Take profit (partial sell) | [Take Profit Guide](./take-profit.md) |
| `/dca <address>` | Dollar-cost average | [DCA Guide](./dca.md) |
| `/positions` | View active positions | [Positions Guide](./viewing-positions.md) |

## Trading Workflow

1. **Call a Token** (`/call`)
   - Buy a token using group funds
   - Amount set by `/settings` command
   - Creates a tracked position

2. **Monitor Position** (`/positions`)
   - Check current price, PnL, ROI
   - View all active trades

3. **Manage Position**
   - **Take Profit** (`/tp`): Sell partial amounts (10%, 25%, 50%, 75%)
   - **DCA** (`/dca`): Buy more at current price
   - **Sell** (`/sell`): Sell entire position

4. **Profit Distribution**
   - Automatic when position is sold for profit
   - Distributed to payout wallets
   - See [Profit Distribution Guide](../profit-distribution/overview.md)

## Key Concepts

### Entry Price
The price at which you bought the token. Used to calculate PnL and ROI.

### Current Price
The real-time price of the token from DexScreener.

### PnL (Profit and Loss)
The difference between entry price and current/exit price, multiplied by position size.

### ROI (Return on Investment)
The percentage gain or loss: `(Current Price - Entry Price) / Entry Price * 100`

### Position Size
The amount of tokens you hold in the position.

## Trading Requirements

Before trading, make sure:

- ✅ You're a **trader** (ask owner to add you with `/addtrader @username`)
- ✅ Group Wallet has sufficient SOL (check with `/balance`)
- ✅ You've set a payout wallet (`/payout [address]`)
- ✅ Buy amount is configured (`/settings` - default 0.1 SOL)

## Trading Best Practices

1. **Research tokens** before calling
2. **Check wallet balance** before trading
3. **Set take profits** strategically
4. **Use DCA** to average down if needed
5. **Monitor positions** regularly
6. **Coordinate with other traders**

## What's Next?

Choose a topic to learn more:

1. **[Calling Tokens](./calling-tokens.md)** - How to buy tokens
2. **[Selling Positions](./selling-positions.md)** - How to sell
3. **[Take Profit](./take-profit.md)** - Partial selling strategies
4. **[Dollar-Cost Averaging](./dca.md)** - Adding to positions
5. **[Viewing Positions](./viewing-positions.md)** - Monitoring trades

---

*Ready to trade? Make sure you're a trader and your payout wallet is set! Use `/positions` to see all active trades.*
