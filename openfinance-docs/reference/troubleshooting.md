# Troubleshooting

## 401 Unauthorized

A wallet-scoped tool was called without a valid `x-api-key` header. Either you forgot the header, or the key is wrong. Re-copy from the dashboard and make sure the value starts with `open_`.

{% hint style="info" %}
Public market-data tools should never return 401. If they do, check the request URL.
{% endhint %}

## Tools do not appear after editing config

Most clients only read the MCP config on startup. Fully quit and relaunch the app, or use the client's "Reload MCP servers" command.

## Skills do not appear after `npx skills add`

Run `npx skills list` to confirm the install location. If installed globally, restart your editor. If installed to a project, make sure you opened that project root.

## 429 Too Many Requests

You hit the rate limit. Public tools have a per-IP limit, wallet tools have a per-key limit. Throttle your agent or request a higher tier from the dashboard.

## Still stuck?

Full tool reference and changelog: [docs.openfinance.tech](https://docs.openfinance.tech).
