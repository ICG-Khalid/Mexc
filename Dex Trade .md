# DEX Trading Guide

![ICG Logo](https://raw.githubusercontent.com/icgio/brandkit/main/logo/dark690x175nobg.png)

**Complete guide to automated decentralized exchange trading**

---

## Welcome to DEX Trading

The ICG Trading platform provides a comprehensive decentralized exchange (DEX) trading suite with automated bot capabilities across multiple blockchains. This guide will walk you through all features and help you get started with automated DEX trading.

### ⚠️ Access Requirements

DEX trading requires the **dex_access** permission on your account. Contact support if you need access enabled.

---

## Multi-Chain Support

Trade across 6 major blockchain networks with support for the most popular DEXes:

| Chain | Native Token | Supported DEXes |
|-------|--------------|-----------------|
| Ethereum | ETH | Uniswap V2, Uniswap V3, PancakeSwap |
| BSC | BNB | PancakeSwap |
| Arbitrum | ETH | Uniswap V2, Uniswap V3, PancakeSwap |
| Base | ETH | Uniswap V2, Uniswap V3, PancakeSwap |
| Polygon | MATIC | Uniswap V2, Uniswap V3 |
| Solana | SOL | Raydium, Pumpswap |

Select your desired chain from the dropdown in the top right corner. All three tabs (Wallets, Trading, Monitor) will automatically filter to show only data for the selected chain.

![Screenshot 1: Multi-Chain Interface](https://raw.githubusercontent.com/ICG-Khalid/Mexc/a642db0595bd768f0fff7ba5cab9ba2b62b75b26/Screenshot%201.png)

---

## Wallet Management

The Wallets tab provides complete control over your on-chain wallet infrastructure. This is where you'll create, manage, and distribute funds across your trading wallets.

### Key Features

#### 🔐 Seed Creation
Generate secure 24-word mnemonic seeds. All seeds are encrypted at rest with AES-256-GCM. Private keys are derived on-the-fly and never stored.

#### 👛 Wallet Derivation
Derive up to 100 wallets per seed using standard derivation paths. The master wallet (index 0) is your primary wallet for receiving funds.

#### 💰 Balance Tracking
Real-time balance monitoring for native tokens and configured trading tokens. Auto-refresh every 30-60 seconds.

#### 🪙 Token Configuration
Add any token by contract address. The system automatically detects symbol and decimals for seamless trading.

#### 📤 Fund Distribution
Distribute native tokens or trading tokens from master wallet to multiple derived wallets in one transaction.

#### 📥 Fund Collection
Collect funds from multiple derived wallets back to the master wallet. Essential for consolidating profits.

![Screenshot 2: Wallet Management Interface](https://raw.githubusercontent.com/ICG-Khalid/Mexc/a642db0595bd768f0fff7ba5cab9ba2b62b75b26/Screenshot%202.png)

### Wallet Operations

- **Derive:** Create new wallets from your seed (up to index 99)
- **Distribute:** Send native or trading tokens to multiple wallets at once
- **Collect:** Gather funds from derived wallets back to master
- **Sell All Tokens:** Quickly liquidate trading tokens across all wallets
- **Withdraw:** Send funds to external addresses

> 💡 **Best Practice**  
> Always keep sufficient native tokens (ETH, BNB, SOL, etc.) in each wallet for gas fees. The platform will warn you if balances are too low to execute trades.

---

## Automated Trading

The Trading tab is where you configure and execute automated DEX trading strategies.

### Creating a Trading Configuration

#### 1. Set Token Address
Enter the contract address of the token you want to trade. The system will auto-detect the token details.

#### 2. Configure Trade Parameters
Set min/max trade amounts, intervals between trades, slippage tolerance, and total amount target. Use randomization to make bot activity less detectable.

#### 3. Select Wallets & DEXes
Choose which wallets to use and which DEXes to trade on. You can distribute trades across multiple DEXes for better execution.

#### 4. Configure Advanced Settings
**For Solana:** Enable JITO bundles and set tip amounts.  
**For EVM chains:** Adjust gas settings and priority fees.

#### 5. Start Trading
Save your configuration and click Start. The bot will execute trades according to your parameters until the total target is reached or you stop it manually.

![Screenshot 3: Trading Configuration](https://raw.githubusercontent.com/ICG-Khalid/Mexc/a642db0595bd768f0fff7ba5cab9ba2b62b75b26/Screenshot%203.png)

### Smart Execution Flow

The trading bot uses intelligent execution logic:

- Randomly selects wallet and DEX from your configuration
- Calculates trade amount within your min/max range
- Checks wallet balance and adjusts if insufficient
- Executes swap with your slippage tolerance
- Waits random interval before next trade
- Continues until total target reached or manually stopped

### Trading Features

#### ⚡ Multi-Config Support
Run multiple trading configurations simultaneously across different tokens and chains.

#### 📊 Progress Tracking
Monitor real-time progress for each config: trades executed, total volume, success rate, and time elapsed.

#### 🎯 Flexible Targeting
Set total amount targets or let the bot run indefinitely until you manually stop it.

#### 🔀 Randomization
Randomize trade amounts and intervals to mimic organic trading behavior and avoid detection.

---

## Trade Monitoring

The Monitor tab provides comprehensive visibility into all your trading activity.

### 24-Hour Statistics

#### 📈 Total Trades
Count of all trades executed in the last 24 hours across all configurations.

#### ✅ Successful
Number of trades that completed successfully on-chain.

#### ❌ Failed
Trades that failed due to slippage, insufficient balance, or network issues.

#### ⏳ Pending
Trades currently being processed on-chain.

#### 📊 Success Rate
Percentage of successful trades. Aim for 95%+ success rate.

![Screenshot 4: Monitor Statistics](https://raw.githubusercontent.com/ICG-Khalid/Mexc/a642db0595bd768f0fff7ba5cab9ba2b62b75b26/Screenshot%204.png)

### Trade History

View detailed history of all trades with the following information:

- **Timestamp:** Exact time the trade was executed
- **DEX:** Which decentralized exchange processed the swap
- **Wallet:** Which wallet executed the trade
- **In Amount:** Amount and token sent
- **Out Amount:** Amount and token received
- **Status:** Success, Failed, or Pending
- **Transaction Hash:** Clickable link to blockchain explorer

![Screenshot 5: Trade History](https://raw.githubusercontent.com/ICG-Khalid/Mexc/a642db0595bd768f0fff7ba5cab9ba2b62b75b26/Screenshot%205.png)

> 🔄 **Auto-Refresh**  
> The Monitor tab automatically refreshes every 10 seconds to show the latest trade data and statistics.

---

## Architecture & Security

### Client Isolation
Every client operates in a completely isolated environment. Your seeds, wallets, and trading data are never visible to other users or clients.

### Encrypted Seeds
All mnemonic seeds are encrypted at rest using AES-256-GCM with client-specific keys. Seeds are only decrypted in memory when needed to derive keys for transactions.

### On-the-Fly Key Derivation
Private keys are never stored anywhere. They are derived on-demand from your encrypted seed when needed to sign transactions, then immediately discarded from memory.

### Secure Communication
All API communication uses HTTPS with proper authentication. Transaction signing happens server-side in isolated, secure environments.

---

## Getting Started

### Quick Start Checklist

1. **Create a Seed**  
   Go to Wallets tab and create your first seed. Back up the 24-word mnemonic securely.

2. **Derive Wallets**  
   Generate multiple wallets (recommend 5-20) for distributing trades.

3. **Fund Master Wallet**  
   Send native tokens (ETH, BNB, SOL, etc.) to your master wallet (index 0).

4. **Distribute Funds**  
   Use the Distribute function to send native tokens to your derived wallets for gas fees.

5. **Add Trading Token**  
   Configure the token you want to trade by adding its contract address.

6. **Create Trading Config**  
   Go to Trading tab, create a configuration with your desired parameters.

7. **Start Trading**  
   Click Start and monitor progress in real-time. Switch to Monitor tab to view detailed statistics.

---

© 2026 ICG Trading. All rights reserved. | [clients.icg.io](https://clients.icg.io/)

