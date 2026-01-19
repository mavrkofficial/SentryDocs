# Initial Setup

This guide walks you through the first-time setup using the Sentry Menu interface.

## Prerequisites

- A Telegram private group or supergroup
- Group owner permissions (owner must initialize)
- Ability to promote the bot to admin

## Step-by-Step Setup

### Step 1: Add the Bot

1. Open your Telegram group
2. Group Settings -> Add Members
3. Search for `@Sentry_Trading_Bot`
4. Add the bot to the group

### Step 2: Promote to Admin

The bot must be an admin to read messages and respond to menu flows.

1. Group Settings -> Administrators
2. Promote Sentry Bot
3. Enable Read Messages (required)
4. Optional: Delete Messages, Pin Messages

### Step 3: Initialize the Bot (Owner Only)

The owner initializes the bot in the group. The bot will:

1. Ask for a group name (first time only)
2. Create a Group Wallet for trading
3. Create a Deployer Wallet for token launches
4. Initialize settings

### Step 4: Fund Your Wallets

Group Wallet (required for trading):

1. Copy the Group Wallet address from the initialization message
2. Send SOL from any wallet
3. Keep a SOL buffer for fees

Deployer Wallet (optional for launches):

1. Copy the Deployer Wallet address
2. Fund when you plan to deploy tokens

## Verification

Open the Sentry Menu and confirm:

- Balance shows the Group Wallet balance
- Settings -> Group Call/DCA Amount is visible
- Positions opens without errors

## Next Steps

1. [Add Traders](./traders.md)
2. [Configure Settings](./settings.md)
3. [Set Up Payout Wallets](./payout-wallets.md)
4. [Start Trading](../trading/overview.md)

## Common Setup Issues

### "Only group owner can initialize"
- Only the original group owner can initialize the bot

### Bot does not respond
- Bot is admin
- Read Messages permission is enabled
- Group is private

### Wallet addresses not showing
- Initialization completed successfully
- Owner is running the flow

---

If the menu button is not visible, reopen the chat and check the menu button again.
