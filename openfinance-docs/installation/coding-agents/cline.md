# Cline (VS Code Extension)

## Steps

1. Open VS Code with the Cline extension installed.
2. Click the **Cline** icon in the sidebar.
3. Click the **MCP Servers** button (gear icon) in the Cline panel.
4. Click **Configure MCP Servers**, this opens the Cline MCP settings file.
5. Add the OpenFinance server:

```json
{
  "mcpServers": {
    "openfinance-tech": {
      "type": "streamableHttp",
      "url": "https://api.openfinance.tech/agent/mcp",
      "headers": {
        "x-api-key": "open_xxxxx"
      }
    }
  }
}
```

Drop the `headers` object if you only need public tools.

6. Save the file.
7. Back in the Cline MCP panel, OpenFinance should appear. Toggle it on if needed.
8. OpenFinance tools are now available in Cline conversations.
