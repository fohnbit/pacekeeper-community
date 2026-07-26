# Dashboard, Athlet und Bedienung

<!-- screenshot-plan:
  - Dashboard mit Bereitschaftsring und Kennzahlen
  - Plan-Kalender mit Ansichtsumschaltung
  - Athletenansicht mit anonymisierten Charts
-->

[← Erste Schritte](DE-Erste-Schritte) · [Inhaltsverzeichnis](Deutsch) · [Weiter: Trainingsplanung →](DE-Trainingsplanung)

## Hauptnavigation

<!-- code-ref:
  - lib/widgets/dashboard_bottom_nav.dart::DashboardBottomNav
  - lib/screens/dashboard_screen.dart::_sidebarNavItems
  - lib/screens/dashboard_screen.dart::_onNavTabChange
-->

| Symbol | Bereich | Bedeutung |
|---|---|---|
| ![Plan](images/icons/plan.png) | **Plan** | Kalender für Trainings, Aktivitäten und Mahlzeiten |
| ![Athlet](images/icons/athlete.png) | **Athlet** | Leistungs-, Wellness- und Verlaufsdaten sowie eigene Charts |
| ![Dashboard](images/icons/dashboard.png) | **Dashboard** | Tagesansicht mit vergangenen und kommenden Tagen |
| ![Einstellungen](images/icons/settings.png) | **Einstellungen** | Synchronisierung, KI, Darstellung, Daten und Diagnose |

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

| Symbol | Kürzel | Bedeutung |
|---|---|---|
| ![Herzfrequenz](images/icons/heart-rate.png) | HF | Ruhe-Herzfrequenz |
| ![HRV](images/icons/hrv.png) | HRV | Herzratenvariabilität |
| ![CTL](images/icons/ctl.png) | CTL | längerfristige Trainingsbelastung bzw. Fitness |
| ![ATL](images/icons/atl.png) | ATL | kurzfristige Trainingsbelastung bzw. Ermüdung |
| ![TSB](images/icons/tsb.png) | TSB | Form; Verhältnis langfristiger zu kurzfristiger Belastung |
|  | ↑ / ↓ / → | Wert steigt, fällt oder bleibt stabil |

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
| ![Hinzufügen](images/icons/add.png) | neuen Eintrag oder neue Aktion anlegen |
| ![Bearbeiten](images/icons/edit.png) | bearbeiten |
| ![Löschen](images/icons/delete.png) | löschen |
| ![Synchronisieren](images/icons/sync.png) | aktualisieren oder synchronisieren |
| ![Anheften](images/icons/pin.png) | Inhalt im Dashboard anheften |
| ![Kopieren](images/icons/copy.png) | Daten oder Text kopieren |
| ![Vollansicht](images/icons/full-view.png) | Detail- oder Vollansicht öffnen |
| ![Zurück](images/icons/previous.png) / ![Weiter](images/icons/next.png) | vorheriger oder nächster Zeitraum |
| ![Weitere Aktionen](images/icons/more.png) | weitere Aktionen |
| ![Verlauf](images/icons/history.png) | Änderungsverlauf öffnen |
| ![KI-Warteschlange](images/icons/ai-queue.png) | Status der KI-Warteschlange öffnen |

Die Symbole können sich zwischen iOS, macOS und Android geringfügig
unterscheiden.

[← Erste Schritte](DE-Erste-Schritte) · [Inhaltsverzeichnis](Deutsch) · [Weiter: Trainingsplanung →](DE-Trainingsplanung)
