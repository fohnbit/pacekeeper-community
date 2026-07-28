# Connect Claude.ai to PaceKeeper AI

[← Connect ChatGPT](EN-Connect-ChatGPT) · [Contents](English) · [AI connectors and tokens →](EN-AI-Connectors-and-Tokens)

The PaceKeeper AI connector lets Claude read authorised PaceKeeper data and, after your review, perform supported actions.

## Requirements

- You are signed in to PaceKeeper AI and have selected an athlete.
- You use `https://www.pacekeeper.icu/mcp` as the server address.
- Your Claude plan supports custom connectors. With Team or Enterprise, an Owner might need to add the connector for the organisation first.

## First setup for a personal Claude account

1. In PaceKeeper AI, open **Settings → Connect AI assistant**.
2. Generate a new six-digit one-time code. It is valid for five minutes.
3. Open [claude.ai](https://claude.ai).
4. Open **Customize → Connectors**.
5. Select **+ → Add custom connector**.
6. Enter **PaceKeeper AI** as the name.
7. Enter only `https://www.pacekeeper.icu/mcp` as the remote server URL.
8. Select **Add** or **Connect**. Do not enter a custom OAuth Client ID or Client Secret for the normal PaceKeeper setup.
9. Enter the six-digit code from the app on the PaceKeeper connection page and confirm.
10. Enable PaceKeeper AI in the desired chat through **+ → Connectors**.

## Team and Enterprise

1. An Owner adds PaceKeeper AI to the organisation's connectors using `https://www.pacekeeper.icu/mcp`.
2. Each member then opens **Customize → Connectors**.
3. The member selects **Connect** for **PaceKeeper AI**.
4. The member generates a six-digit code in their own PaceKeeper app and uses it to complete their personal authorisation.

The organisation connector does not replace the personal connection for each PaceKeeper account.

## Reconnect after an update

Reconnect when:

- PaceKeeper AI asks you to connect again,
- Claude reports an authentication or permission error,
- new PaceKeeper functions are missing after an update,
- the connector was added with an old or incorrect address.

To refresh the custom connector, remove it and add it again:

1. In Claude, open **Customize → Connectors**.
2. Open the three-dot menu for **PaceKeeper AI** and select **Remove**.
3. With Team or Enterprise, the Owner first updates the organisation connector if necessary.
4. Add PaceKeeper AI again using `https://www.pacekeeper.icu/mcp`.
5. In PaceKeeper AI, open **Settings → Connect AI assistant** and generate a new six-digit code.
6. Complete the new authorisation with this code.
7. Enable the connector in a new Claude chat and begin with a read request.

An old one-time code cannot be reused. If only your personal sign-in has expired, selecting **Connect** again might be sufficient. If new functions remain unavailable, removing and adding the connector again is the reliable refresh process.

## If the connection does not work

- Check that PaceKeeper AI is enabled for the current conversation.
- Generate a new code if the five-minute validity period has expired.
- Remove and add the connector again if Claude continues to show outdated or missing functions.
- Use only `https://www.pacekeeper.icu/mcp` as the server address.
- Review Claude's action before confirming a write, then verify the result in PaceKeeper AI.

Further information: [Anthropic's custom connector guide](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp).

[← Connect ChatGPT](EN-Connect-ChatGPT) · [Contents](English) · [AI connectors and tokens →](EN-AI-Connectors-and-Tokens)
