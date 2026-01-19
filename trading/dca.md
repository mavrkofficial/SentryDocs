# Dollar-Cost Averaging (DCA)

The DCA button lets you add to an existing position, lowering your average entry price or increasing size.

## How to DCA (Menu Flow)

1. Open Sentry Menu -> DCA
2. Paste the token address when prompted
3. The bot executes the buy and updates the position

## Requirements

- You must be a trader
- An active position must exist
- Group Wallet has sufficient SOL

## How It Works

1. Bot finds the active position
2. Uses the Group Call/DCA Amount
3. Buys more at the current price
4. Recalculates weighted average entry

## When to Use DCA

Use DCA when:

- Averaging down on dips
- Adding to a winning position
- Building a position gradually

Avoid DCA when:

- No active position exists
- You are adding without a plan

## Where to See the Impact

Check Positions to review:

- Updated entry price
- Position size
- DCA history

## Common Issues

### "No active position found"
- Call the token first
- Verify the address

### "Insufficient SOL"
- Fund the Group Wallet
- Reduce the Call/DCA amount

## Best Practices

1. Set a max position size
2. DCA on dips, not pumps
3. Track updated entry in Positions

---

DCA is a powerful tool when used with a strategy. Plan your entries and stay disciplined.
