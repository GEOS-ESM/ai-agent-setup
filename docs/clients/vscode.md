# Visual Studio Code

Visual Studio Code Chat can use custom language models for NASA Chat / Ask Sage and NASA Mission AI LiteLLM. The shared configuration contains model metadata and endpoint URLs but no API key.

## Configure

1. In VS Code, run **Chat: Manage Language Models** from the Command Palette.
2. Open `chatLanguageModels.json` from that view. On macOS, the usual location is `~/Library/Application Support/Code/User/chatLanguageModels.json`.
3. Merge the entries in the [VS Code template](../../templates/vscode/chatLanguageModels.json.example) into the existing JSON array. Do not replace any other custom providers.
4. Run **Developer: Reload Window**.
5. Return to **Chat: Manage Language Models**, choose a NASA provider's settings, select **Update API Key**, and enter your service-specific key.

VS Code stores the key in local secret storage. It may add an `apiKey` value such as `${input:chat.lm.secret.1234abcd}` to your local configuration. That is a local secret reference, not the key itself. Do not replace it with a literal credential or commit it.

## Available services

- **NASA Ask Sage (OpenAI):** GPT model IDs through the OpenAI-compatible Chat Completions API.
- **NASA Ask Sage (Anthropic):** Claude model IDs through the Anthropic Messages API.
- **NASA Mission AI LiteLLM:** Claude, GPT, and Gemini model IDs through the OpenAI-compatible Chat Completions API.

Available models and limits can change by entitlement and service policy. A model listed in the template may not be available to every user.
