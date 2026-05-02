# Cursor

## Steps

1. Open Cursor.
2. Press **Cmd+Shift+P** (Mac) or **Ctrl+Shift+P** (Windows) to open the Command Palette.
3. Type `MCP` and select **Cursor Settings: Open MCP Settings**.
4. This opens a JSON file. Add the OpenFinance server inside the `mcpServers` object:

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

Drop the `headers` object if you only need public tools.

5. Save the file.
6. Open the Command Palette again (Cmd/Ctrl+Shift+P), type `MCP` and select **Reload MCP Servers**.
7. OpenFinance tools are now available in Cursor's AI chat.
