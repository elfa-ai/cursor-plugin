# Elfa AI for Cursor

Crypto social intelligence from X and Telegram, plus **Auto**, a condition engine that watches the market and fires an action when your conditions are met.

One plugin, two parts:

- **MCP server** — 11 tools covering mentions, trending tokens and contract addresses, narratives, smart account stats, market chat, and the full Auto query lifecycle
- **Skill** — workflow guidance for the Elfa API and for writing EQL, so the agent knows which tool to reach for and what a query costs before it runs

## Install

Get an API key at [dev.elfa.ai](https://dev.elfa.ai), install the plugin, and paste the key when Cursor asks for it.

| Variable | Required | Purpose |
| --- | --- | --- |
| `ELFA_API_KEY` | yes | Authenticates every request |
| `ELFA_HMAC_SECRET` | no | Signs Auto mutations when signing is required. Notification-only query mutations do not need it |

The MCP server is fetched from npm on demand as [`@elfa-ai/mcp`](https://www.npmjs.com/package/@elfa-ai/mcp); nothing is vendored here.

Ask *"what's trending in crypto right now?"* to confirm it works.

## Contents

```
.cursor-plugin/plugin.json   plugin manifest
mcp.json                     MCP server configuration
skills/elfa-ai/              the Elfa API skill
assets/icon.png              plugin logo
```

## Source of truth

`skills/elfa-ai/` mirrors the same directory in [`elfa-ai/skills`](https://github.com/elfa-ai/skills), minus `scripts/build-skill.sh`, which is packaging tooling specific to that repository. Edit the skill there, not here.

The MCP server lives in [`elfa-ai/mcp`](https://github.com/elfa-ai/mcp). Both track [docs.elfa.ai](https://docs.elfa.ai).

## License

MIT. Covers this repository's contents only — not access to the Elfa API, and not the Elfa name or logo.
