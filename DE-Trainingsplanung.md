# Trainingsplanung

<!-- screenshot-plan:
  - Meine Pläne und Neuer Plan
  - Planeditor: Plan Daten, Events und Struktur
  - Phasenliste mit Aktionen Phasen und Trainings
-->

[← Dashboard und Bedienung](DE-App-Bedienung) · [Inhaltsverzeichnis](Deutsch) · [Weiter: Ernährungsplanung →](DE-Ernaehrungsplanung)

## Richtige Reihenfolge

Ein vollständiger Trainingsplan entsteht in drei Schritten:

1. **Planrahmen und Events anlegen**
2. **Phasen erzeugen**
3. **Trainings für jede Phase erzeugen**

Phasen allein enthalten noch keine konkreten Trainingseinheiten.

## Den ersten Plan anlegen

<!-- code-ref:
  - lib/features/plans/ui/my_plans_screen.dart::MyPlansScreen
  - lib/features/plans/ui/plan_project_editor_dialog.dart::showPlanProjectEditorDialog
  - lib/features/plans/model/plan_project_draft.dart::PlanProjectDraft
-->

1. Öffne **Plan** und über das Kalendersymbol **Meine Pläne**.
2. Wähle **Neuer Plan**.
3. Lege den **Plan-Typ** fest: Ernährung, Training oder Training mit
   abgestimmter Ernährung.
4. Trage Start- und Enddatum des gesamten Plans ein.
5. Definiere das Hauptziel als A-Rennen mit Name, Datum, Zielvorgabe und
   Sportart. Ergänze bei Bedarf B- und C-Rennen.
6. Wähle unter **Struktur** die Sportarten und möglichen Wochentage
   beziehungsweise Tageszeiten je Sportart.
7. Ergänze unter **Events** alle bekannten Einschränkungen und besonderen
   Zeiträume.
8. Speichere zunächst diese Rahmendaten.

## Events vor der Phasenplanung erfassen

<!-- code-ref:
  - lib/features/plans/model/plan_event_type.dart::PlanEventType
  - lib/features/plans/ui/plan_event_type_ui.dart
-->

Zur Auswahl stehen:

- B- und C-Rennen
- Urlaub
- Krankheit
- Verletzung
- Trainingslager
- Dienstreise
- Erholungsblock
- Andere

Gib einen aussagekräftigen Namen, ein Datum oder einen Zeitraum und bei
**Andere** eine Beschreibung an. Nur so kann die KI diese Zeit bei Belastung,
Erholung und Trainingsverteilung berücksichtigen.

Kommt später ein Urlaub oder anderes wichtiges Ereignis hinzu, ergänze es im
Plan und lass die betroffenen Phasen und Trainings erneut prüfen oder
optimieren.

## Phasen erzeugen

Nach dem Speichern des Planrahmens wählst du beim Plan **✨ Phasen**. PaceKeeper
AI erstellt über die integrierte OpenAI-Anbindung einen Vorschlag für die
Periodisierung.

Prüfe vor dem Übernehmen:

- Ist der gesamte Planzeitraum ohne Lücken abgedeckt?
- Werden A-, B- und C-Ziele richtig berücksichtigt?
- Sind Urlaub, Krankheit, Dienstreisen und andere Events berücksichtigt?
- Sind Belastungsaufbau, Erholung, Peak und Wettkampfwoche sinnvoll verteilt?

Alternativ kannst du Claude über den Connector beauftragen, die Phasen des
vorhandenen Plans zu erstellen oder zu überarbeiten. Beispiel:

> Prüfe meinen Plan, berücksichtige alle Events und erstelle passende
> Trainingsphasen bis zu meinem A-Ziel.

Nach der Freigabe ist derselbe externe Ablauf auch mit ChatGPT vorgesehen.

## Trainings je Phase erzeugen

Wähle bei **jeder Phase** die Aktion **✨ Trainings**. Kontrolliere danach:

- Sportart und Trainingsinhalt
- Datum, Uhrzeit und Dauer
- Intensität und Belastungsverteilung
- Erholungstage
- Vereinbarkeit mit Arbeit und privaten Events
- Urlaub, Krankheit, Verletzung und Wettkämpfe

Wiederhole den Vorgang, bis alle Phasen mit konkreten Trainingseinheiten
gefüllt sind. Trainings können durch die integrierte KI oder extern durch
Claude – später auch ChatGPT – erstellt und angepasst werden.

## Änderungen prüfen

KI-Vorschläge werden vor dem Übernehmen als Vorschau angezeigt. **Übernehmen**
schreibt die vorgeschlagenen Änderungen, **Verwerfen** lässt den bestehenden
Plan unverändert. Falls angeboten, macht **Rückgängig** die zuletzt angewendete
Änderung rückgängig. Der Verlauf ist über das Verlaufssymbol erreichbar.

[← Dashboard und Bedienung](DE-App-Bedienung) · [Inhaltsverzeichnis](Deutsch) · [Weiter: Ernährungsplanung →](DE-Ernaehrungsplanung)
