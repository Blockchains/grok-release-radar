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

## License
MIT for the generated glue code. Dependencies keep their own licences (see PARTS.md).

## Contributing

Issues and pull requests are welcome. Please read the [contributing guide](https://github.com/Blockchains/.github/blob/main/CONTRIBUTING.md), [code of conduct](https://github.com/Blockchains/.github/blob/main/CODE_OF_CONDUCT.md) and [security policy](https://github.com/Blockchains/.github/blob/main/SECURITY.md) first.

---
Built by Blockchain Lab — [blockchainlab.com](https://blockchainlab.com/?utm_source=github&utm_medium=readme&utm_campaign=grok-release-radar)
