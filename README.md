# Aurion AIOS Plugin Marketplace

Shared Plugin marketplace for Aurion AIOS customers.

**One private GitHub repository** (`Kevin-aurion/aurion-aios-plugin-marketplace`) supports **ChatGPT Desktop Plugins**, **Codex CLI**, and **Claude**. Claude reads `.claude-plugin/marketplace.json`; ChatGPT Desktop and Codex CLI read `.agents/plugins/marketplace.json`. Both catalogs install the same plugin: `aurion-aios-builder`.

## Install — ChatGPT Desktop Plugins / Codex CLI

### Codex CLI

```bash
codex plugin marketplace add Kevin-aurion/aurion-aios-plugin-marketplace
codex plugin add aurion-aios-builder@aurion-aios-plugin-marketplace
```

### ChatGPT Desktop Plugins

1. Open **Plugins**.
2. Import / add a marketplace from a **GitHub repository**.
3. Use the same repository: `Kevin-aurion/aurion-aios-plugin-marketplace`.
4. Install `aurion-aios-builder` when prompted.

## Install — Claude

In Claude Cowork, open **Customize → Plugins → Add marketplace** and add:

`Kevin-aurion/aurion-aios-plugin-marketplace`

In Claude Code:

`/plugin marketplace add Kevin-aurion/aurion-aios-plugin-marketplace`

`/plugin install aurion-aios-builder@aurion-aios-plugin-marketplace`

## Update

Cowork users click **Update** on the marketplace. Claude Code users run:

`/plugin marketplace update aurion-aios-plugin-marketplace`

Codex CLI users re-add or update the marketplace, then reinstall/update the plugin as needed:

```bash
codex plugin marketplace add Kevin-aurion/aurion-aios-plugin-marketplace
codex plugin add aurion-aios-builder@aurion-aios-plugin-marketplace
```

The Plugin connects only to https://aios-mcp.lazyoffice.app/mcp. Installation does not grant AIOS access; every user must still authenticate with an enabled AIOS account through OAuth.

Version: 1.5.1
