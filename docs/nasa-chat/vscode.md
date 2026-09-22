# NASA Chat with Visual Studio Code

Use this guide only if you are authorized to use NASA Chat. The template configures NASA Chat's OpenAI-compatible and Anthropic-compatible custom language models, but does not configure Mission AI.

Before configuring Visual Studio Code, [request NASA Chat access and create an API key](api-key.md).

1. In VS Code, run **Chat: Manage Language Models** from the Command Palette.
2. Open `chatLanguageModels.json` from that view. On macOS, the usual location is `~/Library/Application Support/Code/User/chatLanguageModels.json`.
3. Merge entries from the [NASA Chat VS Code template](../../templates/nasa-chat/chatLanguageModels.json.example) into the existing JSON array.
4. Run **Developer: Reload Window**.
5. Return to **Chat: Manage Language Models**, choose a NASA Chat provider's settings, select **Update API Key**, and enter your NASA Chat key.

VS Code stores the key in local secret storage. It may add a local reference such as `${input:chat.lm.secret.1234abcd}`; this is not the credential itself. Do not replace it with a literal key or commit it.
