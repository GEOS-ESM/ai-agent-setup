# NASA Chat / Ask Sage

## Status

NASA Chat uses a NASA Ask Sage gateway with OpenAI-compatible and Anthropic-compatible APIs. The service supports the client configurations in this repository for authorized users.

## Approved API bases

Use an API base appropriate to the client and protocol. A client adds the operation path itself unless its guide says otherwise.

| Protocol | Base URL |
| --- | --- |
| OpenAI-compatible | `https://api.asksage.ai.nasa.gov/server/openai/v1` |
| Anthropic-compatible for OpenCode | `https://api.asksage.ai.nasa.gov/server/anthropic/v1` |
| Anthropic-compatible for Claude Code | `https://api.asksage.ai.nasa.gov/server/anthropic` |

Claude Code appends `/v1/messages` to `ANTHROPIC_BASE_URL`. Do **not** append `/v1` in its configuration, or requests will use the invalid `/v1/v1/messages` path.

## Obtain before configuring a client

Obtain these through the approved NASA Chat or GMAO service channel:

- Authentication mechanism and secure storage method
- Network, proxy, VPN, certificate, or mTLS requirements
- Permitted data classifications, retention/logging policy, and tool-use restrictions
- A service-owner-approved verification procedure

## Client choice

- [OpenCode](../clients/opencode.md) supports both NASA Chat protocol surfaces.
- [Claude Code](../clients/claude-code.md) uses the Anthropic-compatible surface.
- [Visual Studio Code](../clients/vscode.md) supports both surfaces through custom language models.

## Official references

- [Ask Sage OpenCode integration](https://docs.asksage.ai/integrations/opencode/)
- [Ask Sage Claude Code integration](https://docs.asksage.ai/integrations/claude-code/)
- [Ask Sage OpenAI compatibility](https://docs.asksage.ai/api-documentation/OpenAI-Compatibility-Guide/)
- [Ask Sage Anthropic compatibility](https://docs.asksage.ai/api-documentation/Anthropic-Compatibility-Guide/)
