---
name: test-rust-mcp
description: "Test MCP server that echoes messages — for build pipeline verification"
version: "0.1.0"
author: "Plugin Store Team"
tags:
  - test
---

# Test Rust MCP Server

## Overview

This is a minimal MCP server written in Rust, used to verify the build pipeline. It provides a single `echo` tool that returns the input message.

## Pre-flight Checks

1. The `onchainos` CLI is installed
2. The test-rust-mcp MCP server is installed via plugin-store

## Commands

### Echo a Message (MCP Tool)

Call MCP tool `echo` with a message parameter.

**When to use**: When the user wants to test that the MCP server is working.
**Output**: The same message echoed back with "Echo: " prefix.

### Search for Tokens (onchainos)

```bash
onchainos token search --query "ETH"
```

**When to use**: When the user asks to find a token.
**Ask user to confirm** the search query before executing.

## Error Handling

| Error | Cause | Resolution |
|-------|-------|------------|
| MCP connection failed | Server not running | Verify plugin is installed |
| Empty response | No message provided | Provide a message parameter |

## Skill Routing

- For real token operations → use `okx-dex-token` skill
- For swap operations → use `okx-dex-swap` skill
