---
name: test-python-mcp
description: "Test Python MCP server with echo tool"
version: "0.1.0"
author: "Plugin Store Team"
tags: [test]
---
# Test Python MCP
## Overview
Minimal Python MCP server packaged with PyInstaller.
## Pre-flight Checks
1. onchainos CLI installed
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
