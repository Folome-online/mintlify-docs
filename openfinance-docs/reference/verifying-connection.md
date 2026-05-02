# Verifying the Connection

Hit the endpoint directly to confirm it responds.

## Public tools, no auth needed

No auth header is needed for `tools/list`:

```bash
curl -i https://api.openfinance.tech/agent/mcp \
  -H "Accept: application/json, text/event-stream" \
  -H "Content-Type: application/json" \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/list"}'
```

A `200 OK` with a JSON-RPC payload listing tools means you are good to go.

## Wallet-scoped tools

To verify a wallet-scoped tool, add the header and call one that requires it:

```bash
curl -i https://api.openfinance.tech/agent/mcp \
  -H "x-api-key: open_xxxxx" \
  -H "Accept: application/json, text/event-stream" \
  -H "Content-Type: application/json" \
  -d '{"jsonrpc":"2.0","id":2,"method":"tools/call","params":{"name":"getPositions","arguments":{}}}'
```

A `401` on this call means the key is missing or invalid.
