# Dashboard, Athlete, and App Controls

<!-- screenshot-plan: Mirror the DE dashboard and athlete screenshots in English. -->

[← Nutrition planning](EN-Nutrition-Planning) · [Contents](English) · [Next: Access and settings →](EN-Access-and-Settings)

## Main navigation

<!-- code-ref:
  - lib/widgets/dashboard_bottom_nav.dart::DashboardBottomNav
  - lib/screens/dashboard_screen.dart::_sidebarNavItems
  - lib/screens/dashboard_screen.dart::_onNavTabChange
-->

| Icon | Section | Purpose |
|---|---|---|
| 🚩 | **Plan** | Calendar for workouts, activities, and meals |
| 👤 | **Athlete** | Performance, wellness, history, and custom charts |
| ▣ | **Dashboard** | Daily view with previous and upcoming days |
| ⚙️ | **Settings** | Synchronisation, AI, appearance, data, and diagnostics |

On phones, navigation is shown at the bottom. In landscape or on larger
screens, it may appear in a sidebar.

## Header and readiness

<!-- code-ref:
  - lib/widgets/pk_header/pk_gradient_header.dart
  - lib/widgets/pk_header/pk_header_theme.dart::PkHeaderMetricStyle
  - lib/widgets/pk_header/pk_metric_detail_sheet.dart
  - lib/widgets/pk_header/pk_athlete_sheet.dart::showPkAthleteSheet
-->

The coloured ring around your profile picture shows your current
**readiness**. Tap the picture to switch athlete, view licence and AI tokens,
manage sharing, or sign out.

Swipe the header sideways to see readiness reasons and additional wellness
values. Tap a metric for an explanation and its seven-day history.

| Abbreviation | Meaning |
|---|---|
| HR | Resting heart rate |
| HRV | Heart-rate variability |
| CTL | Long-term training load or fitness |
| ATL | Short-term training load or fatigue |
| TSB | Form; relationship between long- and short-term load |
| ↑ / ↓ / → | Value is rising, falling, or stable |

Green, red, and grey indicate favourable, unfavourable, or no material change.
The exact interpretation depends on the metric.

## Dashboard

<!-- code-ref:
  - lib/screens/dashboard/today/today_detail_mobile.dart
  - lib/widgets/today_create_action_sheet.dart::TodayCreateActionSheet
-->

Dashboard always opens on **Today**. Swipe horizontally between the previous
seven days, today, and the next seven days. Pull down to restore the header if
it disappears while scrolling.

Use **+** to:

- create a workout,
- import a FIT or TCX activity,
- import an activity from Bosch eBike Connect.

## Plan and calendar

In the calendar, switch between month, week, and day, navigate with the arrows,
return to **Today**, and filter workouts, meals, or activities. Depending on
the view, totals may include time, TSS, calories, and elevation.

## Athlete

The **Athlete** section shows development across selectable time ranges.
Depending on connected data sources, it may contain resting HR, HRV, sleep,
blood pressure, steps, weight, body fat, VO₂max, and custom charts.

## Common icons

| Icon | Action |
|---|---|
| ＋ | create a new entry or action |
| ✎ | edit |
| 🗑 | delete |
| ↻ | refresh or synchronise |
| ★ / Pin | pin content to Dashboard |
| ⧉ | copy data or text |
| ⤢ | open detail or full view |
| ‹ / › | previous or next period |
| ⋮ | more actions |
| History icon | open change history |
| Bell | open AI queue status |

Icons may vary slightly between iOS, macOS, and Android.

[← Nutrition planning](EN-Nutrition-Planning) · [Contents](English) · [Next: Access and settings →](EN-Access-and-Settings)
