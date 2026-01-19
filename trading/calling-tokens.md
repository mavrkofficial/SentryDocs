# Calling Tokens (Buying)

The Call button is the primary way to buy tokens for your group.

## What is a Call?

A call is a buy order executed from the Group Wallet. The bot buys at the current market price and tracks the position.

## How to Call a Token (Menu Flow)

1. Open Sentry Menu -> Call
2. Paste the token address when prompted
3. The bot executes the buy and posts a confirmation

## Requirements

- You must be a trader
- Group Wallet must have sufficient SOL
- Token must be on DexScreener
- Only one active position per token

## Buy Amount

The buy amount comes from:

Settings -> Group Call/DCA Amount

## What Happens After a Call

- Transaction signature and links
- Token details (name, symbol, price)
- Amount purchased
- Entry price recorded
- Position added to Positions

You can then manage the position with DCA, Take Profit, or Sell.

## Platform Fees

- Free Tier: 2.5 percent fee from the buy amount
- Premium Tier: 0 percent fee

## Smart Routing

- Sentry-deployed tokens: Orca
- Other tokens: Jupiter

## Common Issues

### "You must be a trader"
- Ask the owner to add you in Settings -> Traders
- Set a payout wallet in Settings -> Payouts

### "Insufficient SOL"
- Fund the Group Wallet
- Reduce buy amount in Settings

### "Token not found"
- Check the address
- Wait for DexScreener indexing

## Best Practices

1. Research the token before calling
2. Check balance in Balance
3. Coordinate with the group
4. Monitor in Positions

---

Call is the entry point for every position. Keep your buy amount reasonable and stay coordinated with the group.
