# Claude, ChatGPT, and AI Tokens

<!-- screenshot-plan: Use the corresponding anonymised DE connector captures
     or capture the same views with the English interface. -->

[← Getting started](EN-Getting-Started) · [Contents](English) · [Next: Training planning →](EN-Training-Planning)

## Connecting Claude.ai to PaceKeeper AI

<!-- code-ref:
  - lib/screens/settings/mcp_connect_screen.dart::McpConnectScreen
  - lib/features/pk_state/data/pacekeeper_mcp_link_code_client.dart
-->

The PaceKeeper AI connector lets Claude read authorised data and, after your
confirmation, prepare or modify plans, phases, workouts, and nutrition entries.

1. In PaceKeeper AI, open **Settings → Connect AI assistant**.
2. Generate a one-time six-digit code. It is valid for five minutes.
3. On [claude.ai](https://claude.ai), open **Customize → Connectors**.
4. Select **+ → Add custom connector**.
5. Enter **PaceKeeper AI** as the name.
6. Enter `https://www.pacekeeper.icu/mcp` as the server URL.
7. Select **Add/Connect**, then enter the app's code on PaceKeeper's connection
   page.
8. Enable PaceKeeper AI in the desired chat through **+ → Connectors**.

You can enable or disable the connector per conversation. For Claude Team or
Enterprise, an Owner must first add it to the organisation. Each member can
then connect their own account.

Anthropic currently classifies custom connectors as beta. See the
[official Claude instructions](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp).

> [!CAUTION]
> For write operations, review Claude's tool call and then check the preview or
> change history in PaceKeeper AI. Only connect the server address shown above.

## ChatGPT connector status

The PaceKeeper AI connector has been **submitted to ChatGPT for review**.
During the alpha phase, this does not mean that it is already available to all
users. Use it only when PaceKeeper AI is actually listed in ChatGPT's connected
apps or connectors.

This guide will be updated with the final ChatGPT setup flow after approval.

## Integrated AI or external connector?

<!-- code-ref:
  - lib/features/pk_state/data/pacekeeper_license_client.dart::PaceKeeperLicenseState
  - lib/widgets/pk_header/pk_athlete_sheet.dart
  - lib/screens/settings/subscription_store_screen.dart
-->

| Option | Usage | PaceKeeper AI tokens |
|---|---|---|
| Integrated AI | AI actions directly inside the app, processed through OpenAI | consumed |
| Claude connector | prompt in a Claude conversation with PaceKeeper enabled | not consumed |
| ChatGPT connector | through ChatGPT after approval | not consumed |

> [!IMPORTANT]
> The free tier includes only a small number of tokens for the integrated AI.
> The allowance is renewed every month. The remaining percentage is shown as
> **AI tokens** in the profile menu.

External connectors do not use PaceKeeper AI tokens. The external provider's
own usage limits or charges may still apply. Once PaceKeeper AI is publicly
available, subscriptions with a larger monthly token allowance are planned
through the App Store and Play Store.

[← Getting started](EN-Getting-Started) · [Contents](English) · [Next: Training planning →](EN-Training-Planning)
