---
name: test-node-mcp
description: "Test Node.js MCP server with echo tool"
version: "0.1.0"
author: "Plugin Store Team"
tags: [test]
---
# Test Node.js MCP
## Overview
Minimal Node.js MCP server distributed as npm package.
## Pre-flight Checks
1. onchainos CLI installed
2. Node.js 18+
## Commands
### Echo (MCP Tool)
Call MCP tool `echo` with message.
### Token Search
```bash
onchainos token search --query "ETH"
```
**Ask user to confirm** before executing.
## Error Handling
| Error | Cause | Resolution |
|-------|-------|------------|
| Connection failed | Not running | Check install |
## Skill Routing
- For swaps → use `okx-dex-swap`
