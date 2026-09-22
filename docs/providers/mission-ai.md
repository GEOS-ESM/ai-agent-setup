# Mission AI

## Status

Mission AI provides a NASA LiteLLM proxy with an OpenAI-compatible Chat Completions API for authorized users.

## Approved API base

```text
https://proxy.fast.luna.nasa.gov
```

OpenCode's OpenAI-compatible adapter uses this base directly. VS Code uses the complete Chat Completions URL:

```text
https://proxy.fast.luna.nasa.gov/v1/chat/completions
```

Mission AI is currently documented here for OpenCode and VS Code. Claude Code requires an Anthropic-compatible gateway, and this LiteLLM configuration should not be assumed to provide one.

## Required service-owner information

Obtain these through the approved Mission AI or GMAO service channel:

- Authentication issuance, storage, rotation, and revocation process
- Network and certificate requirements
- Data handling, retention, telemetry, and audit policy
- A non-production verification procedure

Use [OpenCode](../clients/opencode.md) or [Visual Studio Code](../clients/vscode.md). Do not substitute a personal account or a different service endpoint.
