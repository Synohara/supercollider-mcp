# SuperCollider MCP Server

[![smithery badge](https://smithery.ai/badge/@Synohara/supercollider-mcp)](https://smithery.ai/server/@Synohara/supercollider-mcp)

The SuperCollider MCP Server is a [Model Context Protocol (MCP)](https://modelcontextprotocol.io/introduction) server for the SuperCollider programming language that allows to execute synth using supercolliderjs.

## Prerequisites

1. Install [SuperCollider](https://supercollider.github.io/downloads) on your machine.
2. Node.js and npm should be installed on your machine. You can download it from [Node.js official website](https://nodejs.org/).

## Compatibility

This project has been tested and confirmed to work only on macOS with Apple Silicon (M1) processors. Compatibility with other operating systems or processor architectures has not been verified.

## Installation

### Installing via Smithery

To install SuperCollider Synth Executor for Claude Desktop automatically via [Smithery](https://smithery.ai/server/@Synohara/supercollider-mcp):

```bash
npx -y @smithery/cli install @Synohara/supercollider-mcp --client claude
```

### Usage with Claude Desktop

Add this to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "mcp-supercollider": {
      "command": [
        "npx", 
        "-y",
        "@makotyo/mcp-supercollider"]
    }
  }
}
```


### Usage with VS Code

Add the following JSON block to your User Settings (JSON) file in VS Code. You can do this by pressing Ctrl + Shift + P and typing Preferences: Open User Settings (JSON).

Optionally, you can add it to a file called .vscode/mcp.json in your workspace. This will allow you to share the configuration with others.

> Note that the mcp key is not needed in the .vscode/mcp.json file.

```json
{
  "mcp": {
    "servers": {
      "mcp-supercollider": {
        "command": "npx",
        "args": [
          "-y",
          "@makotyo/mcp-supercollider"
        ]
      }
    }
  }
}
```
