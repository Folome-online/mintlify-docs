# Claude Code (Manual MCP Setup)

If you skipped the [Quick Install](../../getting-started/quick-install.md), you can wire the MCP server up by hand. Choose one of the two options below.

## Option A, Project-level

Available in one project only.

1. `cd` into your project folder.
2. Create `.mcp.json` in the project root.

## Option B, Global

Available in all projects.

1. Edit `~/.claude.json` (create it if it does not exist).

## Configuration

Then paste this block.

### Public-only setup

```json
{
  "mcpServers": {
    "openfinance-tech": {
      "type": "http",
      "url": "https://api.openfinance.tech/agent/mcp"
    }
  }
}
```

### With wallet tools enabled

Add the `headers` block:

```json
{
  "mcpServers": {
    "openfinance-tech": {
      "type": "http",
      "url": "https://api.openfinance.tech/agent/mcp",
      "headers": {
        "x-api-key": "open_xxxxx"
      }
    }
  }
}
```

{% hint style="info" %}
If `~/.claude.json` already has a `mcpServers` object, add the `"openfinance-tech": { ... }` entry inside it rather than replacing the whole file.
{% endhint %}

Restart Claude Code, OpenFinance tools are now available.
