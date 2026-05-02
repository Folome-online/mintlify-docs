# VS Code (GitHub Copilot)

Requires the GitHub Copilot extension installed and an active Copilot subscription.

## Steps

1. Open VS Code.
2. Press **Cmd+Shift+P** (Mac) or **Ctrl+Shift+P** (Windows) to open the Command Palette.
3. Type `MCP` and select **MCP: Add Server**.
4. Choose **Workspace** (adds to this project) or **Global** (available in all projects).
5. This creates or opens an `mcp.json` file. Add the OpenFinance server inside the `servers` object:

```json
{
  "servers": {
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

{% hint style="warning" %}
VS Code uses `"servers"`, not `"mcpServers"`. This is different from Claude.
{% endhint %}

6. Save the file.
7. A **Start** button appears at the top of the file. Click it to start the MCP server.
8. Open Copilot Chat (Ctrl+Alt+I / Cmd+Ctrl+I), select **Agent** mode, and OpenFinance tools are available.
