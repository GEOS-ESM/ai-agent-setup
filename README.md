# AI Agent Setup for GMAO

Private, credential-safe guidance for using coding-agent clients and Visual Studio Code with GMAO AI services.

## Start here

1. Read [Security](SECURITY.md) before configuring a client.
2. Confirm that your intended data and repository are approved for the service.
3. Select only the service you are authorized to use.
4. Follow its client-specific instructions. Do not install a configuration for the other service.
5. Obtain service access and configuration values through the approved GMAO channel. Do not request or add credentials in GitHub issues, pull requests, or chat.

## Services

### NASA Chat

NASA Chat is available through [OpenCode](docs/nasa-chat/opencode.md), [Claude Code](docs/nasa-chat/claude-code.md), and [Visual Studio Code](docs/nasa-chat/vscode.md).

### Mission AI

Mission AI setup is currently documented for [OpenCode](docs/mission-ai/opencode.md) and [Visual Studio Code](docs/mission-ai/vscode.md). A Claude Code setup has not been tested or documented here.

## Scope

This repository provides client configuration patterns and redacted templates. It does not contain API keys, tokens, certificates, private keys, or prompt and source data.

The NASA Chat and Mission AI endpoint and model information here is for GMAO users of the approved NASA services. It is not for public distribution. Service owners remain authoritative for access, models, data handling, and network policy.

## Templates

- [NASA Chat OpenCode](templates/nasa-chat/opencode.jsonc.example)
- [NASA Chat Claude Code](templates/nasa-chat/claude-code-settings.json.example)
- [NASA Chat VS Code](templates/nasa-chat/chatLanguageModels.json.example)
- [Mission AI OpenCode](templates/mission-ai/opencode.jsonc.example)
- [Mission AI VS Code](templates/mission-ai/chatLanguageModels.json.example)

Copy a template to the client configuration location documented in its guide. Keep credentials in the approved local secret store or environment; never put a secret in the copied configuration.

## References

- [OpenCode configuration](https://opencode.ai/docs/config/)
- [OpenCode providers](https://opencode.ai/docs/providers/)
- [Claude Code settings](https://code.claude.com/docs/en/settings)
- [Claude Code LLM gateways](https://code.claude.com/docs/en/llm-gateway)
- [NASA Chat OpenCode integration reference](https://docs.asksage.ai/integrations/opencode/)
- [NASA Chat Claude Code integration reference](https://docs.asksage.ai/integrations/claude-code/)
