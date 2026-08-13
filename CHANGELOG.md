# Changelog

All notable changes to this plugin will be documented here.

## 1.1.0

- Synced the bundled `elfa-ai` skill with docs.elfa.ai: Auto no longer accepts order actions, exchange connections are no longer documented, and the skill gains the Telegram channel and SEC filing condition sources.
- `ELFA_HMAC_SECRET` is now described as signing Auto mutations that are not plain notifications, in both the plugin variable prompt and the README.
- The MCP server ships eleven tools, down from twelve.

## 1.0.0 — initial release

- Added the `elfa` MCP server, launched via `npx -y @elfa-ai/mcp`, with `ELFA_API_KEY` and optional `ELFA_HMAC_SECRET` supplied as plugin variables.
- Added the `elfa-ai` skill covering Elfa API workflows and EQL authoring for Auto.
