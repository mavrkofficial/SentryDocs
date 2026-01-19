# Understanding Wallets

Sentry Bot uses two separate Solana wallets. Both are visible from the Sentry Menu.

## Group Wallet (Trading Wallet)

The Group Wallet holds the group's trading capital.

### Purpose
- Executes all trades (Call, DCA, Sell, Take Profit)
- Holds active positions
- Receives proceeds from sells

### Funding
- Anyone in the group can send SOL
- Recommended: 0.5 to 1.0 SOL to start
- Keep a small SOL buffer for gas fees

### Viewing Balance
Open Balance in the Sentry Menu to see:
- SOL balance
- USD value
- Portfolio value (positions included)

### Important Notes
- Only send SOL to the Group Wallet
- Keep extra SOL for gas (0.01 to 0.05 SOL)

## Deployer Wallet (Launch Wallet)

The Deployer Wallet is used for token launches and bundle operations.

### Purpose
- Pays deployment fees
- Funds bundle buys (if enabled)
- Supports Deployer tools in the menu

### When to Fund
Fund the Deployer Wallet only if you plan to deploy a token or run bundle actions.

## Where to Find Wallet Addresses

You can view both wallet addresses in:

- The initialization message
- The Sentry Menu header (shows wallet details and balances)

## Security Notes

- Private keys are encrypted and stored by the bot
- Traders can trade but cannot withdraw funds directly
- Owner controls settings, not private keys

## Best Practices

1. Keep Group and Deployer wallets funded separately
2. Monitor balances in Balance
3. Always leave a small SOL reserve for fees

---

Use the Balance button anytime for a quick view of wallet balances and portfolio value.
