# Mission AI with Visual Studio Code

Use this guide only if you are authorized to use NASA Mission AI. The template configures the Mission AI LiteLLM custom language model only and does not configure NASA Chat.

1. In VS Code, run **Chat: Manage Language Models** from the Command Palette.
2. Open `chatLanguageModels.json` from that view. On macOS, the usual location is `~/Library/Application Support/Code/User/chatLanguageModels.json`.
3. Merge entries from the [Mission AI VS Code template](../../templates/mission-ai/chatLanguageModels.json.example) into the existing JSON array.
4. Run **Developer: Reload Window**.
5. Return to **Chat: Manage Language Models**, choose the Mission AI provider settings, select **Update API Key**, and enter your Mission AI key.

VS Code stores the key in local secret storage. It may add a local reference such as `${input:chat.lm.secret.1234abcd}`; this is not the credential itself. Do not replace it with a literal key or commit it.
