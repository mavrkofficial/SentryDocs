# Sentry Bot - GitBook Documentation Structure

This document outlines the complete structure for user-facing documentation. Each section should be written in clear, simple language for end-users (not developers).

## Table of Contents

```
📚 Sentry Bot User Guide
├── 🚀 Getting Started
│   ├── Introduction
│   ├── What is Sentry Bot?
│   ├── Key Features
│   └── Quick Start Guide
│
├── 🏁 Group Setup
│   ├── Initial Setup
│   │   ├── Adding the Bot to Your Group
│   │   ├── Promoting the Bot to Admin
│   │   └── Running /start Command
│   ├── Understanding Wallets
│   │   ├── Group Wallet
│   │   ├── Deployer Wallet
│   │   └── Funding Your Wallets
│   ├── Configuring Traders
│   │   ├── Adding Traders (/addtrader)
│   │   ├── Removing Traders (/removetrader)
│   │   ├── Viewing Traders List (/traderslist)
│   │   └── Trader Permissions Explained
│   ├── Setting Up Payout Wallets
│   │   ├── What is a Payout Wallet?
│   │   ├── Setting Your Payout Wallet (/payout)
│   │   ├── Viewing All Payout Wallets (/payoutset)
│   │   └── Why You Need a Payout Wallet
│   └── Group Settings
│       ├── Setting Group Name (/setname)
│       ├── Setting Group Profile Picture (/setpfp)
│       ├── Configuring Buy Amount (/settings)
│       ├── Setting Minimum Balance (/setminbal)
│       └── Customizing Reward Distribution (/setrewards)
│
├── 💸 Trading Guide
│   ├── Making Your First Trade
│   │   ├── Understanding /call Command
│   │   ├── How to Call a Token
│   │   ├── Checking Token Information
│   │   └── What Happens When You Call
│   ├── Managing Positions
│   │   ├── Viewing Active Positions (/positions)
│   │   ├── Selling Positions (/sell)
│   │   ├── Using Take Profit (/tp)
│   │   │   ├── Partial Selling (10%, 25%, 50%, 75%)
│   │   ├── Dollar-Cost Averaging (/dca)
│   │   │   ├── What is DCA?
│   │   │   ├── When to Use DCA
│   │   │   └── How DCA Affects Your Entry Price
│   │   └── Quick Sell Options
│   ├── Trading Strategies
│   │   ├── Best Practices
│   │   ├── Risk Management
│   │   ├── Reading Token Scans
│   │   └── Understanding Slippage
│   └── Trading Commands Reference
│       └── Complete Command List with Examples
│
├── 📊 Analytics & Performance
│   ├── Viewing Your Performance
│   │   ├── Personal Stats (/stats)
│   │   ├── Understanding PnL (Profit & Loss)
│   │   ├── Win Rate Explained
│   │   └── Best Trades Tracking
│   ├── Group Analytics
│   │   ├── Group PnL Report (/pnl)
│   │   ├── Wallet Balance (/balance)
│   │   ├── Wallet Details (/wallet)
│   │   └── Portfolio Overview
│   ├── Leaderboards
│   │   ├── Group Leaderboard (/leaderboard)
│   │   ├── How Rankings Work
│   │   ├── Understanding ROI
│   │   └── Top Traders Metrics
│   └── Data Interpretation
│       ├── Reading Performance Metrics
│       ├── Understanding Returns
│       └── Tracking Progress Over Time
│
├── 🚀 Token Deployment
│   ├── Overview
│   │   ├── What is Token Deployment?
│   │   ├── Zero Capital Requirements
│   │   ├── Vanity Addresses (555 prefix)
│   │   └── Deployment Costs
│   ├── Deployment Wizard (/deploy)
│   │   ├── Step 1: Token Name
│   │   ├── Step 2: Token Symbol
│   │   ├── Step 3: Token Logo
│   │   ├── Step 4: Deployment Options
│   │   │   ├── Bundle Buy Setup
│   │   │   ├── First Buyer Option
│   │   │   └── Final Deployment
│   │   └── What Happens After Deployment
│   ├── Bundle Wallets
│   │   ├── What are Bundle Wallets?
│   │   ├── Setting Up Bundle Wallets (/bundlewallets)
│   │   │   ├── How Many Wallets?
│   │   │   ├── Wallet Format
│   │   │   └── Best Practices
│   │   └── Managing Bundle Wallets
│   ├── Bundle Buy Feature
│   │   ├── Understanding Bundle Buy
│   │   ├── How Bundle Buy Works
│   │   ├── Setting Bundle Buy Amount
│   │   ├── Token Distribution
│   │   └── When to Use Bundle Buy
│   ├── Deployment Flow
│   │   ├── Complete Deployment Process
│   │   ├── Timeline
│   │   ├── What to Expect
│   │   └── Troubleshooting
│   └── Post-Deployment
│       ├── Trading Your Deployed Token
│       ├── Managing Liquidity
│       └── Monitoring Your Token
│
├── 💰 Profit Distribution
│   ├── How Profit Distribution Works
│   │   ├── When Profits Are Distributed
│   │   ├── Profit Calculation
│   │   ├── Fee Structure (Free vs Premium)
│   │   └── Refill Mechanism
│   ├── Reward Structure
│   │   ├── Default Distribution (Even Split)
│   │   ├── Custom Distribution (/setrewards)
│   │   │   ├── Top 3 Traders (25%/15%/10%)
│   │   │   ├── Group Pool (50%)
│   │   │   └── Setting Custom Percentages
│   │   └── Eligibility Requirements
│   ├── Receiving Dividends
│   │   ├── Payout Wallet Setup
│   │   ├── Distribution Timeline
│   │   ├── Checking Your Rewards
│   │   └── Common Issues
│   └── Understanding Fees
│       ├── Platform Fees (2.5% Free Tier)
│       ├── Premium Membership (0% Fees)
│       └── Fee Processing
│
├── 🌾 Harvesting LP Trading Fees
│   ├── Overview
│   │   ├── What is Fee Harvesting?
│   │   ├── How LP Fees Work
│   │   └── Benefits of Harvesting
│   ├── Setting Up Harvest Wallet
│   │   ├── What is a Harvest Wallet?
│   │   ├── Setting Your Harvest Wallet (/harvestwallet)
│   │   ├── Viewing Current Harvest Wallet
│   │   └── Why You Need a Harvest Wallet
│   ├── Harvesting Fees (/harvest)
│   │   ├── How to Harvest
│   │   ├── What Gets Harvested
│   │   ├── SOL vs Token Distribution
│   │   ├── Multiple Positions
│   │   └── Harvesting Frequency
│   ├── Deployer Wallet Withdrawal
│   │   ├── Understanding Deployer Wallet Balance
│   │   ├── Withdrawing from Deployer Wallet (/deployerwithdraw)
│   │   ├── Reserve Amounts
│   │   └── Transfer to Harvest Wallet
│   └── Best Practices
│       ├── When to Harvest
│       ├── Managing Harvested Funds
│       └── Tax Considerations
│
├── 🛠️ Advanced Features
│   ├── Token Scanning
│   │   ├── Automatic Token Detection
│   │   ├── Understanding Scan Results
│   │   └── Using Scan Information
│   ├── Wallet Management
│   │   ├── Group Wallet Operations
│   │   ├── Deployer Wallet Operations
│   │   └── Multi-Wallet Strategy
│   ├── Withdrawal System
│   │   ├── Multi-Sig Withdrawals (/withdraw)
│   │   ├── Approval Process
│   │   └── Security Features
│   └── Premium Features
│       ├── Lifetime Membership (/upgrade)
│       ├── Zero Fee Trading
│       └── Benefits
│
├── 📋 Command Reference
│   ├── Essentials
│   │   ├── /start
│   │   ├── /info
│   │   ├── /howto
│   │   ├── /rules
│   │   └── /upgrade
│   ├── Trading Commands
│   │   ├── /call
│   │   ├── /sell
│   │   ├── /dca
│   │   ├── /tp
│   │   └── /positions
│   ├── Analytics Commands
│   │   ├── /balance
│   │   ├── /wallet
│   │   ├── /pnl
│   │   ├── /stats
│   │   └── /leaderboard
│   ├── Setup Commands
│   │   ├── /settings
│   │   ├── /payout
│   │   ├── /payoutset
│   │   ├── /addtrader
│   │   ├── /removetrader
│   │   └── /traderslist
│   ├── Owner Commands
│   │   ├── /setname
│   │   ├── /setpfp
│   │   ├── /setminbal
│   │   ├── /setrewards
│   │   ├── /bundlewallets
│   │   └── /harvestwallet
│   ├── Deployment Commands
│   │   ├── /deploy
│   │   └── /deployerwithdraw
│   └── Utility Commands
│       ├── /harvest
│       └── /withdraw
│
├── ❓ Frequently Asked Questions
│   ├── Setup Questions
│   ├── Trading Questions
│   ├── Deployment Questions
│   ├── Profit Distribution Questions
│   ├── Harvest Questions
│   └── Troubleshooting
│
├── 🔒 Security & Best Practices
│   ├── Wallet Security
│   ├── Group Management
│   ├── Trader Permissions
│   ├── Safe Trading Practices
│   └── Scam Prevention
│
└── 📞 Support & Resources
    ├── Getting Help
    ├── Community Resources
    ├── Official Links
    └── Updates & Announcements
```

## Content Guidelines for Each Section

### Writing Style
- **User-friendly language**: Avoid technical jargon when possible
- **Step-by-step instructions**: Clear, numbered steps
- **Examples**: Include real-world examples
- **Screenshots**: Visual guides where helpful
- **Warnings**: Highlight important warnings/cautions
- **Tips**: Include helpful tips and best practices

### Each Page Should Include
1. **Clear title** and introduction
2. **Step-by-step instructions** (if applicable)
3. **Command syntax** with examples
4. **What to expect** (output/results)
5. **Common issues** or troubleshooting
6. **Related topics** (links to other pages)

### Example Page Structure

```markdown
# [Page Title]

[Brief introduction explaining what this feature does]

## What is [Feature Name]?

[Detailed explanation in simple terms]

## How to Use

### Step 1: [Action]
[Detailed instructions]

### Step 2: [Action]
[Detailed instructions]

## Command Syntax

\`\`\`
/command <parameter>
\`\`\`

### Parameters
- `<parameter>`: Description

## Examples

**Example 1:**
\`\`\`
/call 55592jXxdwmCxERy2YmpJMi7MGcqJ6kwYJ2Ztrro7XfX
\`\`\`

## What to Expect

[Describe what users will see/experience]

## Common Issues

- **Issue 1**: Solution
- **Issue 2**: Solution

## Tips

- Tip 1
- Tip 2

## Related Topics

- [Link to related page]
- [Link to related page]
```

## Next Steps

1. Create this folder structure in your GitBook space or `/docs` folder
2. Start with "Getting Started" section
3. Fill in content section by section
4. Add screenshots and examples as you go
5. Review and refine based on user feedback
