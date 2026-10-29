# mindlist for Claude and Codex

One install connects Claude or Codex to your mindlist saves and adds a skill that finds, cites and summarizes them. What it reads and never writes: [plugins/mindlist/README.md](plugins/mindlist/README.md).

## Claude (web and desktop, paid plans)

1. Open https://claude.ai/customize/plugins, click Add, choose Add marketplace, paste `mindlistai/mindlist`, confirm.
2. In Discover, choose mindlist, click Add.
3. Open mindlist, then its Connectors tab. Click Add, then Connect, and sign in with the email code mindlist sends.
4. Ask: "What did I save about onboarding?"

## Claude Code

If you added the plugin in Claude and sign Claude Code in with the same Claude account, it is already there. Otherwise, in your shell:

```
claude plugin marketplace add mindlistai/mindlist && claude plugin install mindlist@mindlist
```

Then start Claude Code and sign in through `/mcp` when it asks.

## Codex

In your shell:

```
codex plugin marketplace add mindlistai/mindlist && codex plugin add mindlist@mindlist && codex mcp login mindlist
```

Then start a new Codex session.

## Other ways

- **Claude, Free plan:** add the connector at https://claude.ai/customize/connectors (Add custom connector, the address `https://mindlist.ai/api/v1/mcp`), then upload the skill: download `mindlist-skill.zip` from https://github.com/mindlistai/mindlist/releases/latest and choose Customize, Skills, +, Create skill, Upload a skill (code execution must be on).
- **Codex in an editor:** `codex mcp add mindlist --url https://mindlist.ai/api/v1/mcp`, then copy `plugins/mindlist/skills/mindlist` to `~/.agents/skills/mindlist`.
- **Any other AI tool:** the connector's address is `https://mindlist.ai/api/v1/mcp`.

## Updates

Claude updates plugins from this catalog by itself. Claude Code: `/plugin marketplace update mindlist`. Codex: `codex plugin marketplace upgrade`. The changes are in [CHANGELOG.md](CHANGELOG.md).
