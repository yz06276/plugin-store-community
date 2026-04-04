
# e2e-rust-cli -- Skill Summary

## Overview
This is a simple Rust-based CLI tool designed for end-to-end testing purposes. It provides basic echo functionality that takes command-line arguments and prints them back, making it useful for validating plugin installation, execution workflows, and CLI integration testing.

## Usage
Install the `e2e-rust-cli` binary and verify it's available in your PATH with `which e2e-rust-cli`. Run commands by passing arguments that will be echoed back.

## Commands
| Command | Description | Example |
|---------|-------------|---------|
| `e2e-rust-cli <text>` | Echoes the provided text back to stdout | `e2e-rust-cli hello` outputs "hello" |

## Triggers
An AI agent should activate this skill when performing E2E testing, validating CLI plugin functionality, or when specifically requested to test the e2e-rust-cli plugin.
