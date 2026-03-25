---
name: test-go-mcp
description: "Test Go MCP server with echo tool"
version: "0.1.0"
author: "Plugin Store Team"
tags: [test]
---
# Test Go MCP
## Overview
Minimal Go MCP server for build pipeline testing. Provides echo tool.
## Pre-flight Checks
1. onchainos CLI installed
## Commands
### Echo (MCP Tool)
Call MCP tool `echo` with message parameter.
### Token Search (onchainos)
```bash
onchainos token search --query "ETH"
```
**Ask user to confirm** the query before executing.
## Error Handling
| Error | Cause | Resolution |
|-------|-------|------------|
| Connection failed | Server not running | Verify installation |
## Skill Routing
- For swaps → use `okx-dex-swap`
