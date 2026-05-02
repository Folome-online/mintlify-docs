# Quick Install (Claude Code)

If you are on Claude Code, both pieces install in two commands.

## 1. Install the OpenFinance skills (recommended)

```bash
npx skills add openfinance-tech/skills -y
```

## 2. Add the MCP server

No key is needed for public market data:

```bash
claude mcp add openfinance-tech \
  --transport http "https://api.openfinance.tech/agent/mcp"
```

## Want wallet-scoped tools too?

Add your API key as a header:

```bash
claude mcp add openfinance-tech \
  --transport http "https://api.openfinance.tech/agent/mcp" \
  --header "x-api-key: open_xxxxx"
```

Restart Claude Code and you are done.

## Next steps

* Learn the difference between [Skills and MCP](skills-vs-mcp.md).
* Understand when you need an [API Key](api-keys.md).
* For other editors, see the **Installation** sections.
