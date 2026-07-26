# Access, Settings, and Troubleshooting

[← App controls](EN-App-Controls) · [Contents](English)

## Managed athletes and sharing

<!-- code-ref:
  - lib/screens/managed/managed_athletes_screen.dart::ManagedAthletesScreen
  - lib/features/pk_state/data/pacekeeper_connected_athlete_client.dart
  - lib/widgets/pk_header/pk_athlete_sheet.dart
-->

Through the profile picture and **Access & sharing**, athletes can share
selected data with a coach or another person managing them.

1. The person who needs access selects **Request access**.
2. They enter the data owner's intervals.icu athlete ID.
3. They select the requested permissions.
4. The data owner reviews the incoming request, adjusts permissions if needed,
   and approves or rejects it.
5. After approval, the managed athlete can be selected from the profile menu.

Permissions are granted separately for **Profile, Calendar, Workouts,
Wellness, and Nutrition**. Read and write permissions are independent. Write
access permits changes to the corresponding data, so only grant what is
needed.

The data owner can end sharing at any time. The other person can also end their
access or withdraw a pending request.

## Important settings

<!-- code-ref:
  - lib/screens/settings/settings_screen.dart::SettingsContent
  - lib/features/pk_state/pk_state_controller.dart::PkStateController
-->

- **Sync now:** fetch data again and update trends.
- **Background sync:** keeps data current for other devices and authorised
  access while the app is closed.
- **Health sync:** reads health values on supported mobile devices and can
  optionally upload them to intervals.icu.
- **Refresh profile:** clears local profile caches and downloads the data
  again.
- **Connect AI assistant:** connects Claude or, later, ChatGPT.
- **AI settings:** customises integrated AI actions.
- **Trend, Appearance, and Chart settings:** changes time ranges, the interface,
  and custom charts.
- **Tools & data:** contains utilities and local data management.
- **Debug info:** collects details for a support request.

## If data is missing or out of date

1. Check the internet connection and selected athlete.
2. Select **Settings → Sync now**.
3. Check the intervals.icu connection and, for managed athletes, the stored API
   key or sharing permission.
4. Use **Refresh profile** if profile or wellness data is still missing.
5. For a support request, open **Settings → Debug info**.

Never share passwords, private API keys, or complete access tokens.

[← App controls](EN-App-Controls) · [Contents](English)

