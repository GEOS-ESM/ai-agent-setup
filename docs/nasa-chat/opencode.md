# NASA Chat with OpenCode

Use this guide only if you are authorized to use NASA Chat. It configures the Anthropic-compatible, OpenAI-compatible, xAI (Grok), and Google Gemini NASA Chat providers, but does not configure Mission AI.

Before configuring OpenCode, [request NASA Chat access and create an API key](api-key.md).

## Install

Install OpenCode using the current [OpenCode documentation](https://opencode.ai/docs/) and confirm it is available:

```bash
opencode --version
```

## Configure

1. Merge the [NASA Chat OpenCode template](../../templates/nasa-chat/opencode.jsonc.example) into `~/.config/opencode/opencode.jsonc`. Do not replace unrelated providers, plugins, or preferences.
2. Choose an approved credential method for your service and device. If local OpenCode credential storage is approved, start OpenCode and run `/connect` for each NASA Chat provider you intend to use (`nasa_chat_anthropic`, `nasa_chat_openai`, `nasa_chat_grok`, and/or `nasa_chat_google`). Otherwise, add an `options.apiKey` reference such as `"{env:NASA_CHAT_API_KEY}"` to each relevant provider block in your local config, and supply that variable through an approved mechanism before starting OpenCode. The Google provider also sends `NASA_CHAT_API_KEY` in the `x-access-tokens` header, which the template already sets; Ask Sage requires that header for Gemini.
3. Start (or restart) OpenCode, then select an available NASA Chat model with `/models`.
4. Run `opencode debug config` to confirm the configuration loaded. Its output may include resolved credentials; do not share it without redacting secrets.

The template does not set a default model; choose the provider and model you want in `/models`.

OpenCode's NASA Chat base URLs include `/v1`. The [Claude Code guide](claude-code.md) uses a shorter Anthropic base URL because Claude Code appends `/v1/messages` itself. If an existing local OpenCode provider has a different ID, use that ID in your model selections and authenticate the corresponding provider.

`/connect` stores credentials in `~/.local/share/opencode/auth.json`, outside the shared configuration. An `apiKey` environment reference contains no credential itself. Never put a literal key in the template or commit credentials. Restart OpenCode after editing its configuration.

## References

- [OpenCode configuration](https://opencode.ai/docs/config/)
- [OpenCode providers](https://opencode.ai/docs/providers/)
- [NASA Chat OpenCode integration reference](https://docs.asksage.ai/integrations/opencode/)
