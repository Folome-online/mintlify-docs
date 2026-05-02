# API Keys

## Do I need an API key?

Most of OpenFinance MCP works without authentication. Public market data, prices, funding rates, order books, market metadata, and trade previews, is open. Point your agent at the endpoint and start querying.

You only need an API key for **wallet-scoped tools**, which include anything that:

* Builds a transaction tied to a specific wallet
* Places, modifies, or cancels an order
* Reads a wallet's positions, balances, or order history
* Signs or submits anything on-chain

If your agent is doing research, monitoring, or analysis, you can skip the key entirely. If it is going to act on a wallet, you need one.

## Get an API Key

Only follow these steps if you need wallet tools.

1. Sign in at [openfinance.tech](https://openfinance.tech).
2. Open **Settings → API Keys**.
3. Click **Create Key**, give it a name, and copy the value (it starts with `open_`).

{% hint style="warning" %}
**Treat your API key like a password.** It carries the same permissions as your account, including the ability to build and sign trade transactions on connected wallets. Do not commit it to git or paste it into shared chats.
{% endhint %}

## How the key is used

The key is passed as `x-api-key: open_xxxxx` in any of the editor or chat-client configs. Leave the `headers` object out entirely if you only want public tools.

## Next

* Pick your editor or chat client from the **Installation** sections.
