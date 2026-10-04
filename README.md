# Grok Release Radar

A daily digest of new releases across Grok integrations

**Live:** https://blockchains.github.io/grok-release-radar/ · composed by [grokhack.com /forge](https://grokhack.com/forge) · parts: [PARTS.md](PARTS.md) · manifest: [forge.json](forge.json)

- Archetype: `digest` · capabilities: scheduled, structured_output
- Grok via the official `xai-sdk` (gRPC) with structured output, run daily by GitHub Actions
- Default model `grok-4.6`

## Keys
Add the `XAI_API_KEY` repository secret to enable Grok summaries. Without it the page still publishes the real GitHub release data and shows a clear "needs key" notice instead of a summary.

## Run locally
```bash
pip install -r requirements.txt && pytest -q && python -m app.e2e && python -m app.main
```
Never commit keys; use `.env` (git-ignored) or repository secrets.

## License
MIT for the generated glue code. Dependencies keep their own licences (see PARTS.md).
