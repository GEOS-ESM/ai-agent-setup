# AI Agent Setup for GMAO

Private, credential-safe guidance for using coding-agent clients and Visual Studio Code with GMAO AI services.

## Start here

1. Read [Security](SECURITY.md) before configuring a client.
2. Confirm that your intended data and repository are approved for the service.
3. Select a client: [OpenCode](docs/clients/opencode.md), [Claude Code](docs/clients/claude-code.md), or [Visual Studio Code](docs/clients/vscode.md).
4. Select the approved service: [NASA Chat / Ask Sage](docs/providers/nasa-chat-asksage.md) or [Mission AI](docs/providers/mission-ai.md).
5. Obtain service access and configuration values through the approved GMAO channel. Do not request or add credentials in GitHub issues, pull requests, or chat.

## Scope

This repository provides client configuration patterns and redacted templates. It does not contain API keys, tokens, certificates, private keys, or prompt and source data.

The NASA Chat and Mission AI endpoint and model information here is for GMAO users of the approved NASA services. It is not for public distribution. Service owners remain authoritative for access, models, data handling, and network policy.

## Templates

- [OpenCode configuration](templates/opencode/opencode.jsonc.example)
- [Claude Code settings template](templates/claude-code/settings.json.example)
- [VS Code language-model configuration](templates/vscode/chatLanguageModels.json.example)

Copy a template to the client configuration location documented in its guide. Keep credentials in the approved local secret store or environment; never put a secret in the copied configuration.

## References

- [OpenCode configuration](https://opencode.ai/docs/config/)
- [OpenCode providers](https://opencode.ai/docs/providers/)
- [Claude Code settings](https://code.claude.com/docs/en/settings)
- [Claude Code LLM gateways](https://code.claude.com/docs/en/llm-gateway)
- [Ask Sage OpenCode integration](https://docs.asksage.ai/integrations/opencode/)
- [Ask Sage Claude Code integration](https://docs.asksage.ai/integrations/claude-code/)
