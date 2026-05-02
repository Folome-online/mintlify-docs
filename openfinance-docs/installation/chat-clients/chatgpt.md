# ChatGPT

ChatGPT supports remote MCP servers, so OpenFinance works here too.

## Steps

1. Open ChatGPT → **Settings** → **Connectors**.
2. Click **Create** under custom connectors.
3. Fill in:
   * **Name**: `OpenFinance`
   * **MCP Server URL**: `https://api.openfinance.tech/agent/mcp`
   * **Authentication** (only if you need wallet tools): Custom header → name `x-api-key`, value `open_xxxxx`
4. Save and enable the connector.
5. In a new chat, select **OpenFinance** from the connector picker. Tools are now available.

{% hint style="info" %}
Custom MCP connectors require a ChatGPT Plus, Pro, Business, or Enterprise plan.
{% endhint %}
