# Mission AI with OpenCode

Use this guide only if you are authorized to use NASA Mission AI. It configures the Mission AI LiteLLM provider only and does not configure NASA Chat.

## Install

Install OpenCode using the current [OpenCode documentation](https://opencode.ai/docs/) and confirm it is available:

```bash
opencode --version
```

## Configure

1. Merge the [Mission AI OpenCode template](../../templates/mission-ai/opencode.jsonc.example) into `~/.config/opencode/opencode.jsonc`. Do not replace unrelated providers, plugins, or preferences.
2. Start OpenCode and run `/connect` for `nasa_mission_ai`.
3. Select an available Mission AI model with `/models`.
4. Run `opencode debug config` to confirm the configuration loaded.

`/connect` stores the credential locally outside the shared configuration. Do not add an `apiKey` to the template or commit local credentials.

Mission AI's documented LiteLLM endpoint is OpenAI-compatible. This repository does not currently provide or validate a Claude Code setup; do not invent one unless the Mission AI service owner explicitly documents a supported interface.

## References

- [OpenCode configuration](https://opencode.ai/docs/config/)
- [OpenCode providers](https://opencode.ai/docs/providers/)
