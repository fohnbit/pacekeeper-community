# Claude, ChatGPT, and AI Tokens

<!-- screenshot-plan: Use the corresponding anonymised DE connector captures
     or capture the same views with the English interface. -->

[← Nutrition planning](EN-Nutrition-Planning) · [Contents](English) · [Next: Access and settings →](EN-Access-and-Settings)

## Connect an assistant

<!-- code-ref:
  - lib/screens/settings/mcp_connect_screen.dart::McpConnectScreen
  - lib/features/pk_state/data/pacekeeper_mcp_link_code_client.dart
-->

- [Connect ChatGPT to PaceKeeper AI](EN-Connect-ChatGPT)
- [Connect Claude.ai to PaceKeeper AI](EN-Connect-Claude-ai)

Both guides cover first-time setup, refreshing after an update, authorising
the connection again, and user-facing troubleshooting.

> [!CAUTION]
> For write operations, review the assistant's action and then check the
> preview or change history in PaceKeeper AI. Use only the address shown in
> the relevant setup guide.

## Availability

Availability depends on the external provider's plan and, for managed
accounts, workspace settings. The individual guides include the setup and
administrator requirements relevant to users.

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
| ChatGPT connector | prompt in a chat with PaceKeeper AI enabled | not consumed |

> [!IMPORTANT]
> The free tier includes only a small number of tokens for the integrated AI.
> The allowance is renewed every month. The remaining percentage is shown as
> **AI tokens** in the profile menu.

External connectors do not use PaceKeeper AI tokens. The external provider's
own usage limits or charges may still apply. Once PaceKeeper AI is publicly
available, subscriptions with a larger monthly token allowance are planned
through the App Store and Play Store.

[← Nutrition planning](EN-Nutrition-Planning) · [Contents](English) · [Next: Access and settings →](EN-Access-and-Settings)
