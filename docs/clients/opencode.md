# OpenCode

OpenCode supports custom providers through `opencode.json` or `opencode.jsonc`. The shared configuration has NASA Chat providers for OpenAI and Anthropic models and a Mission AI LiteLLM provider.

## Install

Use the current [OpenCode installation documentation](https://opencode.ai/docs/). Confirm the installed version with:

```bash
opencode --version
```

## Configure

1. Copy the shared [OpenCode configuration](../../templates/opencode/opencode.jsonc.example) into `~/.config/opencode/opencode.jsonc`, merging it with existing configuration. Do not replace unrelated providers, plugins, or preferences.
2. Start OpenCode and run `/connect` for the provider you need. It stores the credential locally, outside the shared configuration. Do not add `apiKey` values to the file.
3. Select a configured model with `/models`.
4. Use `opencode debug config` to confirm the configuration loaded.

The current provider IDs are `nasa_asksage_anthropic`, `nasa_asksage_openai`, and `nasa_mission_ai`. Use the model IDs returned by the service. The template provides the currently approved shared catalog as a convenience, not a guarantee of entitlement.

## Traffic controls

The templates disable the built-in OpenCode provider, sharing, automatic updates, and mDNS discovery. These controls reduce non-inference traffic but do not govern package installers, editor extensions, plugins, or every client feature. Follow the service owner's network requirements.

Use the least-privilege agent/tool permissions allowed by the service policy. Review a proposed command or edit before approving it.

## Templates

- [GMAO OpenCode configuration](../../templates/opencode/opencode.jsonc.example)

## References

- [OpenCode providers](https://opencode.ai/docs/providers/)
- [OpenCode configuration](https://opencode.ai/docs/config/)
