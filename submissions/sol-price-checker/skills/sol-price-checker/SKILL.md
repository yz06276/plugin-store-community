---
name: sol-price-checker
description: "Query real-time token prices on Solana with market data and trend analysis"
version: "1.0.0"
author: "Demo Developer"
tags:
  - solana
  - price
  - analytics
---

# Solana Price Checker

## Overview

This skill enables the AI agent to query real-time token prices, view candlestick charts, and discover trending tokens on the Solana blockchain.

## Pre-flight Checks

Before using this skill, ensure:

1. The `onchainos` CLI is installed and configured
2. Network connectivity is available for API calls

## Commands

### Search for a Token

```bash
onchainos token search --query "SOL" --chain solana
```

**When to use**: When the user asks to find a token by name, symbol, or contract address on Solana.
**Output**: Token name, symbol, contract address, chain, current price.

### Get Token Details

```bash
onchainos token info --address <TOKEN_ADDRESS> --chain solana
```

**When to use**: When the user has a specific token address and wants detailed information.
**Output**: Token metadata, supply, holder count, social links.

### Get Market Price

```bash
onchainos market price --address <TOKEN_ADDRESS> --chain solana
```

**When to use**: When the user asks for the current price of a specific Solana token.
**Output**: Current price in USD, 24h price change, 24h volume, market cap.

### View Price Chart (Kline)

```bash
onchainos market kline --address <TOKEN_ADDRESS> --chain solana --bar 1H --limit 24
```

**When to use**: When the user wants to see price history or a chart.
**Output**: OHLCV candlestick data. Present as a summary (open, high, low, close, trend direction).

### Discover Trending Tokens

```bash
onchainos token trending --chains solana --sort-by 5 --time-frame 4
```

**When to use**: When the user asks "what's hot on Solana" or wants trending tokens.
**Output**: Top tokens ranked by 24h volume. Show name, symbol, price, and 24h change.

## Error Handling

| Error | Cause | Resolution |
|-------|-------|------------|
| "Token not found" | Invalid symbol or address | Ask user to verify the token name or contract address |
| "Rate limited" | Too many API requests | Wait 10 seconds and retry once |
| "Chain not supported" | Wrong chain parameter | Ensure `--chain solana` is specified |
| Empty response | Token may be delisted or very new | Inform user the token data is unavailable |

## Skill Routing

- For token swaps → use `okx-dex-swap` skill
- For wallet balances → use `okx-wallet-portfolio` skill
- For security scanning → use `okx-security` skill
- For smart money signals → use `okx-dex-signal` skill
- For meme token analysis → use `okx-dex-trenches` skill
