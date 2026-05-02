# Skills vs MCP

OpenFinance ships two things, and they do different jobs.

## MCP server, the live tool layer

The MCP server is what lets the agent fetch real prices, simulate a trade, or build a transaction. Without it, the agent has no hands.

## Skills, the static playbooks

Skills teach the agent **how** to use OpenFinance well, when to use isolated vs cross margin, how to size a Hyperliquid perp, how to interpret a Polymarket order book, how to chain `previewTrade` before `buildTransaction`. Without them, the agent has hands but no judgement.

## Which should I install?

You can install either independently. For the best experience, install both.

| Component  | Purpose                              | Install with                          |
| ---------- | ------------------------------------ | ------------------------------------- |
| MCP server | Live tools and data access           | Editor or chat-client config          |
| Skills     | Playbooks for using tools correctly  | `npx skills add openfinance-tech/skills` |

## Next

* [Get an API Key](api-keys.md) if you need wallet-scoped tools.
* [Install the Skills](installing-skills.md) to give your agent context.
