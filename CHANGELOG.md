# Changelog

All notable changes to this plugin will be documented here.

## 1.2.0

- **Removed the `ELFA_HMAC_SECRET` plugin variable.** Elfa no longer documents HMAC signing for `/v2/auto/*` — the API key alone authenticates every route, including mutations. Cursor no longer prompts for it, and it is no longer passed to the MCP server in `mcp.json`. `ELFA_API_KEY` remains the only variable.
- Synced the bundled `elfa-ai` skill with docs.elfa.ai: request signing is gone from the guidance and from `elfa_call.sh`, a credit is now $0.0145 with a $20 minimum PAYG top-up, and the skill gains the account-follow condition source.
- Refreshed the bundled API spec to `2.6.3`, which also drops `hmacEnabled` from the key-status schema and `pacifica` from the symbol-validation venues.

## 1.1.0

- Synced the bundled `elfa-ai` skill with docs.elfa.ai: Auto no longer accepts order actions, exchange connections are no longer documented, and the skill gains the Telegram channel and SEC filing condition sources.
- `ELFA_HMAC_SECRET` is now described as signing Auto mutations that are not plain notifications, in both the plugin variable prompt and the README.
- The MCP server ships eleven tools, down from twelve.

## 1.0.0 — initial release

- Added the `elfa` MCP server, launched via `npx -y @elfa-ai/mcp`, with `ELFA_API_KEY` and optional `ELFA_HMAC_SECRET` supplied as plugin variables.
- Added the `elfa-ai` skill covering Elfa API workflows and EQL authoring for Auto.
