# NASA Chat with OpenCode

Use this guide only if you are authorized to use NASA Chat. It configures both the OpenAI-compatible and Anthropic-compatible NASA Chat providers, but does not configure Mission AI.

## Install

Install OpenCode using the current [OpenCode documentation](https://opencode.ai/docs/) and confirm it is available:

```bash
opencode --version
```

## Configure

1. Merge the [NASA Chat OpenCode template](../../templates/nasa-chat/opencode.jsonc.example) into `~/.config/opencode/opencode.jsonc`. Do not replace unrelated providers, plugins, or preferences.
2. Start OpenCode and run `/connect` for `nasa_chat_anthropic` or `nasa_chat_openai`.
3. Select an available NASA Chat model with `/models`.
4. Run `opencode debug config` to confirm the configuration loaded.

`/connect` stores the credential locally outside the shared configuration. Do not add an `apiKey` to the template or commit local credentials.

## References

- [OpenCode configuration](https://opencode.ai/docs/config/)
- [OpenCode providers](https://opencode.ai/docs/providers/)
- [NASA Chat OpenCode integration reference](https://docs.asksage.ai/integrations/opencode/)
