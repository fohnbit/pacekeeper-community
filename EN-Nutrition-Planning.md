# Nutrition Planning

<!-- screenshot-plan: Mirror the DE nutrition screenshots in English. -->

[← Training planning](EN-Training-Planning) · [Contents](English) · [Next: AI connectors and tokens →](EN-AI-Connectors-and-Tokens)

## Generate nutrition week by week

Nutrition plans should generally be generated **one calendar week at a time**.
This makes it easier to account for working hours, upcoming workouts, shopping,
and short-term changes.

Use **AI actions → Nutrition**, or ask Claude or ChatGPT through an enabled
PaceKeeper connection to create nutrition for a specific week.

Before applying a suggestion, check:

- allergies and intolerances
- nutrition goal and calories
- protein, carbohydrates, and fat
- portion sizes
- ingredients and preparation
- work and training times

## View and edit meals

<!-- code-ref:
  - lib/screens/dashboard/plan/meal_edit_sheet.dart::showMealEditSheet
  - lib/screens/dashboard/plan/meal_recipe_bottom_sheet.dart
-->

Meals appear in the calendar alongside workouts and activities. Open a meal to
view its recipe details. You can edit:

- name and time
- calories
- protein, carbohydrates, and fat
- ingredients
- preparation

Saving synchronises the changes. **Delete** removes the meal after
confirmation. Manual meal creation through Dashboard's plus menu is currently
disabled.

## Shopping list with Bring!

<!-- code-ref:
  - lib/screens/dashboard/plan/calendar_shell_v1.dart::_openAiActionSheet
  - lib/screens/dashboard/plan/calendar_shell_v1.dart::_showBringFallbackDialog
-->

Under **AI actions → Shopping list**, PaceKeeper AI combines the ingredients
for the selected period. On supported devices, the list can be opened through
the external **Bring!** handoff.

If Bring! is unavailable, copy the combined ingredients and paste them into
another shopping-list app manually.

> [!NOTE]
> Integrated nutrition generation uses PaceKeeper AI tokens. Generation
> through Claude or another external connector does not use PaceKeeper AI
> tokens.

[← Training planning](EN-Training-Planning) · [Contents](English) · [Next: AI connectors and tokens →](EN-AI-Connectors-and-Tokens)
