# Dashboard, Athlet und Bedienung

[← Ernährungsplanung](DE-Ernaehrungsplanung) · [Inhaltsverzeichnis](Deutsch) · [Weiter: Zugriffe und Einstellungen →](DE-Zugriffe-und-Einstellungen)

## Hauptnavigation

<!-- code-ref:
  - lib/widgets/dashboard_bottom_nav.dart::DashboardBottomNav
  - lib/screens/dashboard_screen.dart::_sidebarNavItems
  - lib/screens/dashboard_screen.dart::_onNavTabChange
-->

| Symbol | Bereich | Bedeutung |
|---|---|---|
| 🚩 | **Plan** | Kalender für Trainings, Aktivitäten und Mahlzeiten |
| 👤 | **Athlet** | Leistungs-, Wellness- und Verlaufsdaten sowie eigene Charts |
| ▣ | **Dashboard** | Tagesansicht mit vergangenen und kommenden Tagen |
| ⚙️ | **Einstellungen** | Synchronisierung, KI, Darstellung, Daten und Diagnose |

Auf Mobilgeräten befindet sich die Navigation unten. Im Querformat oder auf
größeren Bildschirmen kann sie als Seitenleiste erscheinen.

## Kopfbereich und Bereitschaft

<!-- code-ref:
  - lib/widgets/pk_header/pk_gradient_header.dart
  - lib/widgets/pk_header/pk_header_theme.dart::PkHeaderMetricStyle
  - lib/widgets/pk_header/pk_metric_detail_sheet.dart
  - lib/widgets/pk_header/pk_athlete_sheet.dart::showPkAthleteSheet
-->

Der farbige Ring um dein Profilbild zeigt deine aktuelle **Bereitschaft**.
Tippe auf das Profilbild, um Athleten zu wechseln, Lizenz und AI-Token zu sehen,
Freigaben zu verwalten oder dich abzumelden.

Wische den Kopfbereich seitwärts, um Bereitschaftsgründe und weitere
Wellness-Werte zu sehen. Ein Tipp auf eine Kennzahl öffnet ihre Erklärung und
den 7-Tage-Verlauf.

| Kürzel | Bedeutung |
|---|---|
| HF | Ruhe-Herzfrequenz |
| HRV | Herzratenvariabilität |
| CTL | längerfristige Trainingsbelastung bzw. Fitness |
| ATL | kurzfristige Trainingsbelastung bzw. Ermüdung |
| TSB | Form; Verhältnis langfristiger zu kurzfristiger Belastung |
| ↑ / ↓ / → | Wert steigt, fällt oder bleibt stabil |

Grün, Rot und Grau bedeuten günstig, ungünstig oder keine wesentliche
Änderung. Die genaue Interpretation hängt von der Kennzahl ab.

## Dashboard

<!-- code-ref:
  - lib/screens/dashboard/today/today_detail_mobile.dart
  - lib/widgets/today_create_action_sheet.dart::TodayCreateActionSheet
-->

Das Dashboard öffnet immer bei **Heute**. Wische horizontal zwischen den
vergangenen sieben Tagen, heute und den kommenden sieben Tagen. Ziehe die Seite
nach unten, um einen beim Scrollen ausgeblendeten Kopfbereich zurückzuholen.

Über **+** kannst du:

- ein Training anlegen,
- eine FIT- oder TCX-Aktivität importieren,
- eine Aktivität aus Bosch eBike Connect importieren.

## Plan und Kalender

Im Kalender kannst du zwischen Monat, Woche und Tag wechseln, mit den Pfeilen
navigieren, zu **Heute** springen und Trainings, Mahlzeiten oder Aktivitäten
filtern. Je nach Ansicht werden Zeit, TSS, Kalorien, Höhenmeter und weitere
Summen angezeigt.

## Athlet

Der Bereich **Athlet** zeigt deine Entwicklung über auswählbare Zeiträume. Je
nach Datenquelle können Ruhe-HF, HRV, Schlaf, Blutdruck, Schritte, Gewicht,
Körperfett, VO₂max und eigene Diagramme erscheinen.

## Häufige Symbole

| Symbol | Aktion |
|---|---|
| ＋ | neuen Eintrag oder neue Aktion anlegen |
| ✎ | bearbeiten |
| 🗑 | löschen |
| ↻ | aktualisieren oder synchronisieren |
| ★ / Pin | Inhalt im Dashboard anheften |
| ⧉ | Daten oder Text kopieren |
| ⤢ | Detail- oder Vollansicht öffnen |
| ‹ / › | vorheriger oder nächster Zeitraum |
| ⋮ | weitere Aktionen |
| Verlaufssymbol | Änderungsverlauf öffnen |
| Glocke | Status der KI-Warteschlange öffnen |

Die Symbole können sich zwischen iOS, macOS und Android geringfügig
unterscheiden.

[← Ernährungsplanung](DE-Ernaehrungsplanung) · [Inhaltsverzeichnis](Deutsch) · [Weiter: Zugriffe und Einstellungen →](DE-Zugriffe-und-Einstellungen)

