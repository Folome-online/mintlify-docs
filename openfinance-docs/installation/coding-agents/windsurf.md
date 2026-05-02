# Windsurf

## Steps

1. Open Windsurf.
2. Click the **Cascade** icon (the AI assistant panel).
3. Click the **hammer icon** at the top of the Cascade panel.
4. Click **Configure** to open the MCP config file.
5. Add the OpenFinance server inside the `mcpServers` object:

```json
{
  "mcpServers": {
    "openfinance-tech": {
      "serverUrl": "https://api.openfinance.tech/agent/mcp",
      "headers": {
        "x-api-key": "open_xxxxx"
      }
    }
  }
}
```

Drop the `headers` object if you only need public tools.

6. Save the file.
7. Click the **Refresh** button next to the MCP server list, or restart Windsurf.
8. OpenFinance should appear in the server list as connected.
