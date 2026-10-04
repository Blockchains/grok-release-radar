# Grok Release Radar

A daily digest of new releases across Grok integrations

**Live:** https://blockchains.github.io/grok-release-radar/ · composed by [grokhack-forge](https://github.com/Blockchains/grokhack-forge) · parts: [PARTS.md](PARTS.md) · manifest: [forge.json](forge.json)

- Archetype: `digest` · capabilities: scheduled, structured_output
- Grok via the official `xai-sdk` (gRPC) with structured output, run daily by GitHub Actions
- Default model `grok-4.7`

## Keys
If api.x.ai answers 403 because the xAI account is out of credits or over its spending limit, the app shows an **xAI credits needed** notice; outputs are never faked.

Add the `XAI_API_KEY` repository secret to enable Grok summaries. Without it the page still publishes the real GitHub release data and shows a clear "needs key" notice instead of a summary.

## Run locally
```bash
pip install -r requirements.txt && pytest -q && python -m app.e2e && python -m app.main
```
Never commit keys; use `.env` (git-ignored) or repository secrets.

<!-- blocks:start -->
## Use as a building block

> **For AI agents and builders:** read [`AGENTS.md`](AGENTS.md) (setup, commands, structure, rules), [`llms.txt`](llms.txt) (doc map) and the machine-readable [`blocks.json`](blocks.json) ([schema](https://github.com/Blockchains/.github/blob/main/docs/BLOCKS-SCHEMA.md)). How all Blockchains blocks fit together: **[Build with Blocks](https://github.com/Blockchains/.github/blob/main/docs/BUILD-WITH-BLOCKS.md)** · org catalogue: [https://blockchains.github.io/blocks.json](https://blockchains.github.io/blocks.json).

**What it exports**

| Export | Type | Install / access |
|---|---|---|
| `live app` | web | `https://blockchains.github.io/grok-release-radar/` |
| `forge.json / PARTS.md` | file | `composition manifest: archetype, capabilities, SDK part + commit, default model` |
| `app/` | file | `app/main.py` |

`app/` exports: `collect`, `summarize`, `render`, `FORGE`

**Minimal example** (from the repo README; CI runs the same)

```bash
git clone https://github.com/Blockchains/grok-release-radar && cd grok-release-radar
pip install -r requirements.txt && pytest -q
XAI_API_KEY=... python -m app.main     # without a key it still publishes the real release data with a 'needs key' notice
```

**Inputs → outputs**

- In: `XAI_API_KEY` (secret/env or pasted in the page)
- Out: `Grok output` (web page)

**Composes with**

- [Blockchains/grokhack-forge](https://github.com/Blockchains/grokhack-forge): the composer that generated it; re-compose for variants
- [Blockchains/grokhack-index](https://github.com/Blockchains/grokhack-index): where its SDK part and reference snippets come from
- [Blockchains/blockchainlab-sdk](https://github.com/Blockchains/blockchainlab-sdk): add blockchain data as tools (chat) or inputs (digest)

**Versioning & stability:** `reference`. Generated reference app; versions of the Grok SDK are pinned in package-lock/requirements and recorded in forge.json.
<!-- blocks:end -->

## License
MIT for the generated glue code. Dependencies keep their own licences (see PARTS.md).

## Contributing

Issues and pull requests are welcome. Please read the [contributing guide](https://github.com/Blockchains/.github/blob/main/CONTRIBUTING.md), [code of conduct](https://github.com/Blockchains/.github/blob/main/CODE_OF_CONDUCT.md) and [security policy](https://github.com/Blockchains/.github/blob/main/SECURITY.md) first.

---
Built by Blockchain Lab — [blockchainlab.com](https://blockchainlab.com/?utm_source=github&utm_medium=readme&utm_campaign=grok-release-radar)
