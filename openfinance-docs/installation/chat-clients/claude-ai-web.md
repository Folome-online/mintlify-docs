# Claude.ai (Web)

Because OpenFinance MCP runs over Streamable HTTP, it works directly with Claude.ai's custom connectors.

## Steps

1. Open Claude.ai → **Settings** → **Connectors**.
2. Click **Add custom connector**.
3. Fill in the fields:
   * **Name**: `OpenFinance`
   * **URL**: `https://api.openfinance.tech/agent/mcp`
   * **Custom header** (only if you need wallet tools): name `x-api-key`, value `open_xxxxx`
4. Click **Add**.
5. Open any chat and click the **tools menu**. OpenFinance should appear in the list, toggle it on for the conversation.

{% hint style="info" %}
Custom connectors are available on Pro, Max, Team, and Enterprise plans. Skills installed via `npx skills add` only apply to local editors, not Claude.ai web.
{% endhint %}
