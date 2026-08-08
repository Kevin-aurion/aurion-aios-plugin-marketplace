# Aurion AIOS Plugin Marketplace

Private Claude Plugin marketplace for Aurion AIOS customers.

## Install

In Claude Cowork, open **Customize → Plugins → Add marketplace** and add:

`Kevin-aurion/aurion-aios-plugin-marketplace`

In Claude Code:

`/plugin marketplace add Kevin-aurion/aurion-aios-plugin-marketplace`

`/plugin install aurion-aios-builder@aurion-aios`

## Update

Cowork users click **Update** on the marketplace. Claude Code users run:

`/plugin marketplace update aurion-aios`

The Plugin connects only to https://aurion-aios-mcp.lazyoffice.app/mcp. Installation does not grant AIOS access; every user must still authenticate with an enabled AIOS account through OAuth.

Version: 1.2.1
