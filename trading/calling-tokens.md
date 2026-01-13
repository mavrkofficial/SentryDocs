# Calling Tokens (Buying)

The `/call` command is the primary way to buy tokens for your group. This guide explains how to use it effectively.

## What is a Call?

A **call** is when a trader executes a buy order for a token using the Group Wallet. The bot purchases tokens at the current market price and tracks the position.

## Command Syntax

```
/call <token_address>
```

### Parameters
- `<token_address>`: The Solana token address (base58 format, 32-44 characters)

### Examples

**Basic Call**:
```
/call 55592jXxdwmCxERy2YmpJMi7MGcqJ6kwYJ2Ztrro7XfX
```

**Call by Replying**:
You can also reply to a message containing a token address:
```
/call
```
(When replying to a message with a token address)

## How It Works

1. **Token Validation**: Bot fetches token data from DexScreener
2. **Balance Check**: Verifies Group Wallet has sufficient SOL
3. **Buy Execution**: Executes swap via Jupiter or Orca (depending on token)
4. **Position Tracking**: Records entry price, amount, and caller info
5. **Confirmation**: Shows transaction details and position info

## Requirements

Before calling a token:

- ✅ You must be a **trader** (set by group owner)
- ✅ Group Wallet must have sufficient SOL
- ✅ Token must be listed on DexScreener
- ✅ No active position for this token (one position per token)

## Buy Amount

The amount spent per call is determined by the `/settings` command:

- **Default**: 0.1 SOL
- **Range**: 0.1 - 5.0 SOL
- **Set by**: Group owner only
- **Check current**: Run `/settings` without parameters

**Example**: If `/settings 0.5` is set, each `/call` spends 0.5 SOL.

## What Happens After a Call

After executing a call, you'll see:

- ✅ Transaction signature (on-chain confirmation)
- ✅ Token information (name, symbol, price)
- ✅ Amount purchased
- ✅ Entry price recorded
- ✅ Position added to `/positions`

The position is now tracked, and you can:
- Monitor it with `/positions`
- Take profit with `/tp`
- Add to it with `/dca`
- Sell it with `/sell`

## Platform Fees

- **Free Tier**: 2.5% fee deducted from buy amount
- **Premium Tier**: 0% fee

**Example**: If buy amount is 1.0 SOL and you're on free tier:
- Fee: 0.025 SOL
- Amount spent: 0.975 SOL worth of tokens

## Smart Routing

Sentry Bot uses intelligent routing:

- **Sentry-deployed tokens**: Routes through Orca directly (lower fees)
- **Other tokens**: Routes through Jupiter aggregator (best prices)

This happens automatically - you don't need to choose.

## Restrictions

### One Position Per Token

You can only have **one active position** per token. If you try to call a token that already has an active position, you'll see:

```
⚠️ Active Trade Exists

This token was already called by @username.
Sell the current position before calling again.
```

**Solution**: Sell the existing position first with `/sell <address>`

### Balance Requirements

If the Group Wallet doesn't have enough SOL:

```
❌ Insufficient SOL in Group Wallet.

Req: 0.5 SOL
Address: [wallet_address]
```

**Solution**: Fund the Group Wallet with SOL

## Best Practices

### Before Calling

1. **Research the token**
   - Check DexScreener for price, liquidity, market cap
   - Verify it's a legitimate token
   - Check trading volume

2. **Check wallet balance**
   ```
   /balance
   ```
   Ensure you have enough SOL for the trade

3. **Verify token address**
   - Double-check the address is correct
   - Use DexScreener links when possible
   - Be careful of typos

4. **Coordinate with group**
   - Check if others are planning trades
   - Avoid duplicate positions
   - Consider group strategy

### During Trading

- ✅ Use clear token addresses
- ✅ Reply to messages with addresses when possible
- ✅ Monitor transaction confirmations
- ✅ Verify position was created

### After Calling

- ✅ Check `/positions` to verify position
- ✅ Monitor price movement
- ✅ Set strategy (take profit, hold, DCA)
- ✅ Coordinate with other traders

## Common Issues

### "You must be a trader to use this command"

**Solution**:
- Ask group owner to add you: `/addtrader @username`
- Or set a payout wallet: `/payout [address]` (auto-adds as trader)

### "Bot not initialized"

**Solution**:
- Group owner must run `/start` first
- Verify bot is set up correctly

### "Could not fetch data for token"

**Solutions**:
- Token may not be listed on DexScreener yet
- Check token address is correct
- Try again in a few moments
- Verify token exists on Solana

### "Insufficient SOL in Group Wallet"

**Solutions**:
- Fund the Group Wallet with SOL
- Check current balance: `/balance`
- Reduce buy amount if needed: `/settings [lower_amount]`

### Transaction Fails

**Possible causes**:
- Insufficient balance for gas fees
- Token has restrictions
- Network congestion
- Invalid token address

**Solutions**:
- Ensure wallet has extra SOL for gas (0.01-0.05 SOL)
- Verify token is tradeable
- Try again later if network is busy

## Tips for Success

1. **Start small**: Use default buy amounts when learning
2. **Research first**: Always check tokens before calling
3. **Coordinate**: Work with other traders
4. **Monitor**: Check positions regularly
5. **Be strategic**: Have an exit plan before calling

## Example Trading Flow

```
1. Research token on DexScreener
2. Check group wallet: /balance
3. Call the token: /call [address]
4. Verify position: /positions
5. Monitor price movement
6. Take profit or sell when ready: /tp [address] or /sell [address]
```

---

*Ready to call your first token? Make sure you're a trader, check your balance, and research the token first!*
