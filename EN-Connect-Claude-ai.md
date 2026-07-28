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

## Check the current server version

Copy this complete text into a new chat:

> Call `pacekeeper_get_context`.
>
> Does this tool's **description** contain a line `Tool list built <A>`?
>
> **No** → My tool list is **outdated** and predates this check. Tell me to disconnect and reconnect the connector.
>
> **Yes** → Compare `<A>` with `mcp_version` in the response. Equal means current; different means outdated and the connector must be refreshed.

The PaceKeeper server currently reports `mcp_version`: `{{MCP_VERSION}}`.

If `<A>` is missing or differs from `mcp_version`, open the **PaceKeeper AI** connector management and click **Refresh**. Then open a new chat and repeat the check.

## Reconnect after an update

Reconnect when:

- PaceKeeper AI asks you to connect again,
- Claude reports an authentication or permission error,
- new PaceKeeper functions are missing after an update,
- the connector was added with an old or incorrect address.

To refresh the tool list, Claude normally only needs **Refresh**:

1. In Claude, open **Customize → Connectors**.
2. Open the three-dot menu or management view for **PaceKeeper AI**.
3. Click **Refresh** and wait for it to finish.
4. Open a new chat, enable PaceKeeper AI, and repeat the version check.

Only if **Refresh** is unavailable or an authorisation error remains, remove the connector, add it again with `https://www.pacekeeper.icu/mcp`, and authorise it using a new one-time code from the PaceKeeper app.

## If the connection does not work

- Check that PaceKeeper AI is enabled for the current conversation.
- Generate a new code if the five-minute validity period has expired.
- Click **Refresh** if Claude continues to show outdated or missing functions; remove and reconnect it only if Refresh does not help.
- Use only `https://www.pacekeeper.icu/mcp` as the server address.
- Review Claude's action before confirming a write, then verify the result in PaceKeeper AI.

Further information: [Anthropic's custom connector guide](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp).

[← Connect ChatGPT](EN-Connect-ChatGPT) · [Contents](English) · [AI connectors and tokens →](EN-AI-Connectors-and-Tokens)
