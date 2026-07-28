# Connect ChatGPT to PaceKeeper AI

[← AI connectors and tokens](EN-AI-Connectors-and-Tokens) · [Contents](English) · [Connect Claude.ai →](EN-Connect-Claude-ai)

This guide explains how to connect PaceKeeper AI to ChatGPT for the first time and refresh the connection after a PaceKeeper update.

## Requirement

Enable developer mode in ChatGPT:

**Settings → Security and login → Developer mode**

Availability can depend on your ChatGPT account and workspace policy. If this setting is missing or locked, contact your workspace administrator.

## Connect PaceKeeper AI for the first time

1. Open the [Plugins](https://chatgpt.com/plugins) page in ChatGPT.
2. Select the **plus button** in the top-right corner.
3. Enter these connection details:

   - Name: `PaceKeeper AI Dev`
   - Description: `Training, nutrition, and planning with PaceKeeper AI`
   - URL: `https://pacekeeper.icu/mcp`

4. Create the connection.
5. In PaceKeeper AI, open **Settings → Connect AI assistant**.
6. Generate a new six-digit one-time code. It is valid for five minutes.
7. Enter the code on the PaceKeeper connection page that opens.
8. Confirm the connection.
9. In ChatGPT, check that PaceKeeper AI shows `OAuth` authorisation and the `development` status.
10. Select **Test in chat** to open a new conversation.

Recommended first test:

> Use PaceKeeper AI Dev and show me my next planned workout.

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

If `<A>` is missing or differs from `mcp_version`, refresh the connector as described below. Then fully quit and restart the ChatGPT application and open a new chat.

## Refresh the connection after a PaceKeeper update

Follow these steps when PaceKeeper AI asks you to refresh after an update or new functions are not yet shown in ChatGPT:

1. Open the [Plugins](https://chatgpt.com/plugins) page in ChatGPT.
2. Select **PaceKeeper AI Dev**.
3. Open the plugin details.
4. Scroll to the **Info** section.
5. Select **Refresh**.
6. Wait for the refresh to finish.
7. Fully quit and restart the ChatGPT application.
8. Select **Test in chat** and start a new conversation.
9. Repeat the version check from the previous section.

An existing conversation might continue to use the previous version. Always start a new chat after refreshing.

## Authorise the connection again

Follow these steps if ChatGPT reports a sign-in, authorisation, or permission error:

1. Open the details for **PaceKeeper AI Dev** in ChatGPT.
2. Disconnect the existing PaceKeeper connection if this option is available.
3. Start the connection again.
4. In PaceKeeper AI, open **Settings → Connect AI assistant**.
5. Generate a new six-digit one-time code.
6. Enter the new code on the PaceKeeper connection page and confirm.
7. Select **Test in chat** to open a new conversation.

An expired or previously used one-time code cannot be reused.

## If the connection does not work

- Check that developer mode is enabled in ChatGPT.
- Check that you entered exactly `https://pacekeeper.icu/mcp`.
- Generate a new code if the five-minute validity period has expired.
- After a PaceKeeper update, select **Refresh** in the plugin details and then fully restart the ChatGPT application.
- Disconnect and reconnect PaceKeeper AI if an authorisation error remains.
- Enable PaceKeeper AI in the new chat before submitting a request.
- Review write actions before confirming them, then verify the result in PaceKeeper AI.

Source: [OpenAI – Connect and test your plugin](https://developers.openai.com/plugins/deploy/connect-chatgpt)

[← AI connectors and tokens](EN-AI-Connectors-and-Tokens) · [Contents](English) · [Connect Claude.ai →](EN-Connect-Claude-ai)
