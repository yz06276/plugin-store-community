---
name: e2e-rust-cli
description: "Rust CLI with onchainos integration for E2E testing"
version: "1.0.3"
author: "yz06276"
tags: [e2e-test, rust, onchainos]
---

# e2e-rust-cli

## Overview

A Rust CLI that echoes arguments and queries token prices via onchainos.

## Pre-flight Checks

1. The `e2e-rust-cli` binary is installed (via plugin-store or pre-flight download)
2. `onchainos` CLI is installed and authenticated: `onchainos wallet status`

## Commands

### Echo Arguments

```bash
e2e-rust-cli hello world
```

**When to use**: When the user asks to test basic echo functionality.
**Output**: Prints "hello world".

### Query ETH Price (via CLI binary)

```bash
e2e-rust-cli price ethereum 0xeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee
```

**When to use**: When the user asks to query ETH price using the Rust CLI.
**Output**: JSON with ETH price from onchainos market API.

### Query BTC Price (via onchainos directly)

```bash
onchainos market price --address "0x2260fac5e5542a773aa44fbcfedf7c193bc2c599" --chain ethereum
```

**When to use**: When the user asks for BTC (WBTC) price.
**Output**: JSON with WBTC price on Ethereum.

## Error Handling

| Error | Cause | Resolution |
|-------|-------|------------|
| `Failed to run onchainos` | onchainos not installed | Install via `onchainos upgrade` |
| TLS/certificate error | Local proxy interference | Run with `ALL_PROXY="" onchainos ...` |
