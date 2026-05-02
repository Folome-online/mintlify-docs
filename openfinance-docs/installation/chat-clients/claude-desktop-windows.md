# Claude Desktop (Windows)

## Steps

1. Open Claude Desktop → **Settings** → **Developer**.
2. Click **Edit Config**.
3. Find `claude_desktop_config.json` and open it with Notepad or any text editor.
4. You will see something like this:

```json
{
  "preferences": {
    "coworkScheduledTasksEnabled": true,
    "sidebarMode": "task"
  }
}
```

5. Add a comma after the `preferences` closing brace, then paste the `mcpServers` block. The full file should look like:

```json
{
  "preferences": {
    "coworkScheduledTasksEnabled": true,
    "sidebarMode": "task"
  },
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

If you only need public tools, drop the `headers` object entirely.

6. Save the file.
7. Right-click Claude Desktop in the taskbar → **Close window**, or press Alt+F4.

{% hint style="warning" %}
Make sure the app is fully closed, not just minimized.
{% endhint %}

8. Reopen Claude Desktop.
9. Start a new conversation. You should see a hammer icon in the chat input area, that means OpenFinance MCP is connected.
