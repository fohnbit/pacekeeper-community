# Ernährungsplanung

<!-- screenshot-plan:
  - KI-Ernährungsvorschau einer anonymisierten Woche
  - Bring!-Einkaufslistenaktion ohne private Zutaten
-->

[← Trainingsplanung](DE-Trainingsplanung) · [Inhaltsverzeichnis](Deutsch) · [Weiter: App-Bedienung →](DE-App-Bedienung)

## Ernährung wochenweise erzeugen

Ernährungspläne sollten in der Regel **für jeweils eine Kalenderwoche** erzeugt
werden. Dadurch lassen sich Arbeitszeiten, anstehende Trainings, Einkauf und
kurzfristige Änderungen besser berücksichtigen.

Nutze **KI-Aktionen → Ernährung** oder bitte Claude über den Connector, die
Ernährung für eine konkrete Kalenderwoche zu erstellen. Nach der Freigabe ist
dies auch mit ChatGPT vorgesehen.

Prüfe vor dem Übernehmen insbesondere:

- Allergien und Unverträglichkeiten
- Ernährungsziel und Kalorien
- Protein, Kohlenhydrate und Fett
- Portionsgrößen
- Zutaten und Zubereitung
- Arbeits- und Trainingszeiten

## Mahlzeiten ansehen und bearbeiten

<!-- code-ref:
  - lib/screens/dashboard/plan/meal_edit_sheet.dart::showMealEditSheet
  - lib/screens/dashboard/plan/meal_recipe_bottom_sheet.dart
-->

Mahlzeiten erscheinen im Kalender gemeinsam mit Trainings und Aktivitäten.
Öffne eine Mahlzeit, um Rezeptdetails zu sehen. Bearbeitet werden können:

- Name und Uhrzeit
- Kalorien
- Protein, Kohlenhydrate und Fett
- Zutaten
- Zubereitung

Beim Speichern werden die Änderungen synchronisiert. **Löschen** entfernt die
Mahlzeit nach einer Bestätigung. Das manuelle Anlegen einer Mahlzeit über das
Plus-Menü im Dashboard ist derzeit noch deaktiviert.

## Einkaufsliste mit Bring!

<!-- code-ref:
  - lib/screens/dashboard/plan/calendar_shell_v1.dart::_openAiActionSheet
  - lib/screens/dashboard/plan/calendar_shell_v1.dart::_showBringFallbackDialog
-->

Unter **KI-Aktionen → Einkaufsliste** fasst PaceKeeper AI die Zutaten des
gewählten Zeitraums zusammen. Auf unterstützten Geräten kann die Liste über
die externe **Bring!**-Übergabe geöffnet werden.

Falls Bring! nicht verfügbar ist, kannst du die zusammengefassten Zutaten
kopieren und manuell in eine andere Einkaufsliste einfügen.

> [!NOTE]
> Für die integrierte Ernährungserstellung werden PaceKeeper-AI-Token
> verbraucht. Eine Erstellung über Claude oder einen anderen externen Connector
> verbraucht keine PaceKeeper-AI-Token.

[← Trainingsplanung](DE-Trainingsplanung) · [Inhaltsverzeichnis](Deutsch) · [Weiter: App-Bedienung →](DE-App-Bedienung)
