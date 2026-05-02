# Claude Desktop (macOS)

Claude Desktop supports remote MCP servers either through the Connectors UI or by editing the config file directly. The config file approach is shown here for parity with other editors.

## Steps

1. Open Claude Desktop → **Settings** → **Developer**.
2. Click **Edit Config**.
3. Find `claude_desktop_config.json` and open it with a text editor (right-click → Open With → TextEdit, or VS Code).
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
7. Go back to Claude Desktop. Click **Claude** in the menu bar → **Quit Claude** (or press Cmd+Q).

{% hint style="warning" %}
Closing the window is not enough, you must fully quit the app.
{% endhint %}

8. Reopen Claude Desktop.
9. Start a new conversation. You should see a hammer icon in the chat input area, that means OpenFinance MCP is connected.
