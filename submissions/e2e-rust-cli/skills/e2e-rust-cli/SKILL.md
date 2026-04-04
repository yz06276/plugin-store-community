---
name: e2e-rust-cli
description: "Rust echo CLI for E2E testing"
version: "1.0.0"
author: "yz06276"
tags: [e2e-test, rust]
---
# e2e-rust-cli
## Overview
A simple Rust CLI that echoes back its arguments.
## Pre-flight Checks
1. The `e2e-rust-cli` binary is installed
2. Verify: `which e2e-rust-cli`
## Commands
### Echo
```bash
e2e-rust-cli hello
```
**When to use**: Test the e2e-rust-cli plugin.
**Output**: Prints "hello".
