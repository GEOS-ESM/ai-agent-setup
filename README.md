# SI Agent Setup for GMAO

Private, credential-safe guidance for using coding-agent clients and Visual Studio Code with GMAO SI services.

## Start here

1. Read [Security](SECURITY.md) before configuring a client.
2. Confirm that your intended data and repository are approved for the service.
3. Select only the service you are authorized to use.
4. Follow its client-specific instructions. Do not install a configuration for the other service.
5. Obtain service access and configuration values through the approved GMAO channel. Do not request or add credentials in GitHub issues, pull requests, or chat.

## NAS restriction

SI agent harnesses, including the clients documented in this repository, are not allowed on [NASA Advanced Supercomputing (NAS)](https://www.nas.nasa.gov/) systems. Do not install or configure them there.

## Services

OpenCode and Visual Studio Code are the SI Team's primary clients for these services, so their guides are the main paths through this repository. Secondary CLI guides cover Claude Code for NASA Chat and Codex for both services. The presence of a guide does not change the service or system restrictions above.

### NASA Chat

First [get a NASA Chat API key](docs/nasa-chat/api-key.md). Start with [OpenCode](docs/nasa-chat/opencode.md) or [Visual Studio Code](docs/nasa-chat/vscode.md); CLI alternatives are [Claude Code](docs/nasa-chat/claude-code.md) and [Codex](docs/nasa-chat/codex.md).

### Mission AI

Start with [OpenCode](docs/mission-ai/opencode.md) or [Visual Studio Code](docs/mission-ai/vscode.md). A [Codex CLI trial](docs/mission-ai/codex.md) is also documented, but the Mission AI gateway's Responses API compatibility remains unverified. A Claude Code setup has not been tested or documented here. If you do not already have a Mission AI API key, contact the SI Team for more information.

## Scope

This repository provides client configuration patterns and redacted templates. It does not contain API keys, tokens, certificates, private keys, or prompt and source data.

The NASA Chat and Mission AI endpoint and model information here is for GMAO users of the approved NASA services. It is not for public distribution. Service owners remain authoritative for access, models, data handling, and network policy.

## Templates

- [NASA Chat OpenCode](templates/nasa-chat/opencode.jsonc.example)
- [NASA Chat VS Code](templates/nasa-chat/chatLanguageModels.json.example)
- [NASA Chat Claude Code](templates/nasa-chat/claude-code-settings.json.example)
- [NASA Chat Codex](templates/nasa-chat/codex.config.toml.example)
- [Mission AI OpenCode](templates/mission-ai/opencode.jsonc.example)
- [Mission AI VS Code](templates/mission-ai/chatLanguageModels.json.example)
- [Mission AI Codex](templates/mission-ai/codex.config.toml.example)

Copy a template to the client configuration location documented in its guide. Keep credentials in the approved local secret store or environment; never put a secret in the copied configuration.

## References

- [OpenCode configuration](https://opencode.ai/docs/config/)
- [OpenCode providers](https://opencode.ai/docs/providers/)
- [Claude Code settings](https://code.claude.com/docs/en/settings)
- [Claude Code LLM gateways](https://code.claude.com/docs/en/llm-gateway)
- [NASA Chat OpenCode integration reference](https://docs.asksage.ai/integrations/opencode/)
- [NASA Chat Claude Code integration reference](https://docs.asksage.ai/integrations/claude-code/)
- [Codex custom model providers](https://developers.openai.com/codex/config-file/config-advanced#custom-model-providers)
- [NASA Chat Codex integration reference](https://docs.asksage.ai/integrations/codex/)
