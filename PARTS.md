# Integration parts used by Grok Release Radar

Composed by [grokhack.com /forge](https://grokhack.com/forge) from [Blockchains/grokhack-index](https://github.com/Blockchains/grokhack-index) (index generated 2026-10-04T14:56:15Z).

**Idea:** A daily digest of new releases across Grok integrations

**Archetype:** `digest` · **Capabilities detected:** scheduled, structured_output

## Runtime dependency (installed, pinned to the indexed fork commit)

- `xai-sdk`  from [Blockchains/xai-sdk-python](https://github.com/Blockchains/xai-sdk-python/tree/1d9e1dffc9a0521ede0e6bc7f2b906177b940d34/) (upstream xai-org/xai-sdk-python, licence Apache-2.0)

Default model `grok-4.6`: newest general `grok-N.M` model referenced in [Blockchains/xai-sdk-python@1d9e1df](https://github.com/Blockchains/xai-sdk-python/tree/1d9e1dffc9a0521ede0e6bc7f2b906177b940d34). Override with `XAI_MODEL` (digest) or the model picker (chat, live list from `GET /v1/language-models`).

## Reference implementations consulted (not copied; links pinned to the indexed commit)

- [Blockchains/langchain `libs/partners/openai/langchain_openai/chat_models/base.py` L1381-1404](https://github.com/Blockchains/langchain/blob/57236d55d9ffc8634bda987861e6fce460aff268/libs/partners/openai/langchain_openai/chat_models/base.py#L1381-L1404) · MIT · 147434 stars · capabilities: embeddings, image_generation, live_search, mcp, openai_compatible, reasoning, streaming, structured_output, tool_calling, vision, voice_realtime
- [Blockchains/TradingAgents `tradingagents/llm_clients/openai_client.py` L208-231](https://github.com/Blockchains/TradingAgents/blob/8b22d43d01d9ddda5d686d093d5385884622f3de/tradingagents/llm_clients/openai_client.py#L208-L231) · Apache-2.0 · 109719 stars · capabilities: openai_compatible, reasoning, structured_output, tool_calling
- [Blockchains/mem0 `mem0/llms/xai.py` L33-56](https://github.com/Blockchains/mem0/blob/abb81c88e1f738a8117d8293530fbc31a5ef8fd9/mem0/llms/xai.py#L33-L56) · Apache-2.0 · 66558 stars · capabilities: openai_compatible, structured_output, tool_calling
