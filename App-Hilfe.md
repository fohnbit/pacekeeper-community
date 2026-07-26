# PaceKeeper AI – App-Hilfe · App Help

[🇩🇪 Deutsch](#deutsch) · [🇬🇧 English](#english)

> Die verfügbaren Funktionen können je nach Plattform, Konto, Lizenz und verbundenen Diensten abweichen.  
> Available features may vary by platform, account, licence, and connected services.

> [!WARNING]
> **Alpha-Version:** PaceKeeper AI befindet sich noch in aktiver Entwicklung.
> Funktionen, Symbole und Abläufe können sich ändern. Prüfe insbesondere
> KI-Vorschläge vor dem Übernehmen und melde unerwartetes Verhalten mit den
> Debug-Infos aus der App.  
> **Alpha version:** PaceKeeper AI is under active development. Features,
> icons, and workflows may change. Review AI suggestions before applying them
> and include the app's debug information when reporting unexpected behaviour.

---

## Deutsch

### Wofür ist PaceKeeper AI gedacht?

PaceKeeper AI verbindet Trainingsplanung, absolvierte Aktivitäten, Wellness- und
Leistungsdaten in einer Ansicht. Die App synchronisiert sich mit
**intervals.icu** und unterstützt dich dabei, deinen aktuellen Zustand zu
verstehen, Training und Ernährung zu planen und Änderungen mit KI-Unterstützung
vorzubereiten.

### Erster Start

<!-- code-ref:
  - lib/features/auth/auth_controller.dart::AuthController
  - lib/features/onboarding/profile_onboarding_screen.dart::ProfileOnboardingScreen
  - lib/features/onboarding/dashboard_tutorial.dart::buildDashboardTutorial
-->

1. Melde dich über **intervals.icu** an.
2. PaceKeeper AI übernimmt verfügbare Stammdaten aus intervals.icu.
3. Prüfe und ergänze diese Daten im automatisch gestarteten
   Einrichtungsassistenten. Unvollständige Angaben verschlechtern die Qualität
   späterer Trainings- und Ernährungsvorschläge.
4. Warte auf die erste Synchronisierung.
5. Prüfe im **Dashboard** deine Tagesübersicht und unter **Plan** deinen
   Kalender.

Der Assistent fragt – abhängig davon, ob du Training, Ernährung oder beides
gewählt hast – folgende Informationen ab:

- Name, Geschlecht, Geburtsdatum, Größe und Gewicht,
- automatische Gewichtssynchronisierung,
- Arbeitstage, Arbeitszeiten oder Schichtarbeit,
- tatsächlich ausgeübte Sportarten und Trainingsziel,
- Ernährungsziel, Ernährungsform und zusätzliche Schwerpunkte,
- Fleisch-/Fischhäufigkeit, Küchen- und Zubereitungsstil,
- Allergien, Unverträglichkeiten, Abneigungen und Vorlieben,
- gewünschte Mahlzeiten und deren übliche Uhrzeiten.

> **Wichtig:** Übernommene intervals.icu-Daten sind eine Ausgangsbasis, keine
> Bestätigung ihrer Richtigkeit. Kontrolliere insbesondere Körperdaten,
> Sportarten und Trainingsziel, bevor du speicherst.

Den Einrichtungsassistenten kannst du später unter **Einstellungen →
Einrichtungsassistent** erneut öffnen. Die kurze Einführung lässt sich über
**Einstellungen → Tutorial erneut anzeigen** wiederholen.

### Claude.ai mit PaceKeeper AI verbinden

<!-- code-ref:
  - lib/screens/settings/mcp_connect_screen.dart::McpConnectScreen
  - lib/features/pk_state/data/pacekeeper_mcp_link_code_client.dart
-->

Mit dem PaceKeeper-AI-Connector kann Claude deine freigegebenen Daten lesen und
– nach deiner Bestätigung – Pläne, Phasen, Trainings oder Ernährungseinträge
vorbereiten beziehungsweise ändern.

1. Öffne in PaceKeeper AI **Einstellungen → KI-Assistent verbinden**.
2. Lass einen einmaligen sechsstelligen Code erzeugen. Er ist fünf Minuten
   gültig; ein abgelaufener Code kann jederzeit neu erzeugt werden.
3. Öffne auf [claude.ai](https://claude.ai) **Anpassen/Customize →
   Connectors**.
4. Wähle **+ → Add custom connector** und trage als Namen **PaceKeeper AI**
   sowie als Server-URL `https://www.pacekeeper.icu/mcp` ein.
5. Wähle **Add/Connect**. Gib auf der PaceKeeper-Verbindungsseite den Code aus
   der App ein und bestätige die Verbindung.
6. Aktiviere PaceKeeper AI in einem Chat über **+ → Connectors**. Der
   Connector kann pro Unterhaltung ein- oder ausgeschaltet werden.

Bei Claude Team oder Enterprise muss ein Owner den benutzerdefinierten
Connector zuerst für die Organisation hinzufügen. Danach verbindet jedes
Mitglied sein eigenes Konto. Benutzerdefinierte Claude-Connectoren befinden
sich laut Anthropic derzeit ebenfalls in einer Beta-Phase. Sieh dazu die
[offizielle Claude-Anleitung](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp).

Prüfe bei schreibenden Aktionen immer Claudes Werkzeugaufruf und anschließend
die Vorschau beziehungsweise den Änderungsverlauf in PaceKeeper AI. Verbinde
nur die oben genannte Server-Adresse.

### ChatGPT-Connector

Der PaceKeeper-AI-Connector wurde auch bei **ChatGPT zur Prüfung eingereicht**.
Während der Alpha-Phase bedeutet das noch nicht, dass er für alle Nutzer
verfügbar ist. Verwende ihn erst, wenn PaceKeeper AI in ChatGPT tatsächlich
unter den verbundenen Apps beziehungsweise Connectoren angeboten wird. Die
Dokumentation wird nach der Freigabe um den endgültigen ChatGPT-Ablauf ergänzt.

### Den ersten Plan erstellen

<!-- code-ref:
  - lib/features/plans/ui/my_plans_screen.dart::MyPlansScreen
  - lib/features/plans/ui/plan_project_editor_dialog.dart::showPlanProjectEditorDialog
  - lib/features/plans/model/plan_project_draft.dart::PlanProjectDraft
-->

1. Öffne **Plan** und danach über das Kalendersymbol **Meine Pläne**.
2. Wähle **Neuer Plan**.
3. Lege den **Plan-Typ** fest: Ernährung, Training oder Training mit
   abgestimmter Ernährung.
4. Trage Start- und Enddatum des gesamten Plans ein.
5. Erfasse bei einem Trainingsplan das Hauptziel als A-Rennen mit Name, Datum,
   Zielvorgabe und Sportart. Ergänze bei Bedarf B- und C-Rennen.
6. Wähle unter **Struktur** die Sportarten und die möglichen Wochentage bzw.
   Tageszeiten je Sportart.
7. Ergänze unter **Events** alle bereits bekannten Einschränkungen und
   besonderen Zeiträume.
8. Speichere zunächst nur diese Rahmendaten.

#### Events unbedingt vor der Phasenplanung erfassen

Zur Auswahl stehen B-/C-Rennen, **Urlaub, Krankheit, Verletzung,
Trainingslager, Dienstreise, Erholungsblock** und **Andere**. Gib einen
aussagekräftigen Namen, Datum oder Zeitraum und bei „Andere“ eine Beschreibung
an. Nur dann kann die KI diese Zeiten bei Belastung, Erholung und
Trainingsverteilung berücksichtigen.

Wenn später ein Urlaub oder anderes wichtiges Ereignis hinzukommt, ergänze es
im Plan und lass die betroffenen Phasen beziehungsweise Trainings erneut prüfen
oder optimieren.

#### 1. Phasen erzeugen

Nach dem Speichern des Planrahmens wählst du beim Plan **✨ Phasen**. PaceKeeper
AI erstellt mit der integrierten OpenAI-Anbindung einen Vorschlag für die
Periodisierung. Prüfe, ob der gesamte Planzeitraum ohne Lücken abgedeckt ist und
Ziele, Events, Belastungsaufbau, Erholung, Peak und Wettkampfwoche sinnvoll
berücksichtigt sind. Übernimm den Vorschlag erst danach.

Alternativ kannst du Claude über den verbundenen Connector beauftragen, die
Phasen für den vorhandenen Plan zu erstellen oder zu überarbeiten, zum
Beispiel: „Prüfe meinen Plan, berücksichtige alle Events und erstelle passende
Trainingsphasen bis zu meinem A-Ziel.“ Nach der ChatGPT-Freigabe ist derselbe
externe Ablauf auch dort vorgesehen.

#### 2. Trainings je Phase erzeugen

Phasen allein enthalten noch keine konkreten Einheiten. Wähle deshalb bei
**jeder Phase** die Aktion **✨ Trainings**. Prüfe anschließend Sportart, Datum,
Dauer, Intensität, Erholungstage und die Vereinbarkeit mit Arbeit, Urlaub und
anderen Events. Wiederhole dies, bis alle Phasen mit Trainings gefüllt sind.

Auch diese Einheiten können entweder durch die integrierte KI oder extern über
Claude – später auch ChatGPT – erstellt beziehungsweise angepasst werden.

#### 3. Ernährung wochenweise erzeugen

Ernährungspläne sollten in der Regel **wochenweise** erzeugt werden. Dadurch
lassen sich Arbeitszeiten, anstehende Trainings, Einkauf und kurzfristige
Änderungen besser berücksichtigen. Nutze dafür **KI-Aktionen → Ernährung** oder
bitte Claude über den Connector, die Ernährung für eine konkrete Kalenderwoche
zu erstellen. Prüfe Allergien, Unverträglichkeiten, Kalorien, Makronährstoffe,
Portionen und Zutaten vor dem Übernehmen. Nach der Freigabe ist dieser Ablauf
auch mit ChatGPT vorgesehen.

### KI-Token und externe Connectoren

<!-- code-ref:
  - lib/features/pk_state/data/pacekeeper_license_client.dart::PaceKeeperLicenseState
  - lib/widgets/pk_header/pk_athlete_sheet.dart
  - lib/screens/settings/subscription_store_screen.dart
-->

> [!IMPORTANT]
> Die **integrierte KI** von PaceKeeper AI verwendet das monatliche
> KI-Token-Kontingent der App. In der kostenlosen Variante stehen nur einige
> freie Token zur Verfügung. Das Kontingent wird jeden Monat erneuert; den
> verbleibenden Anteil siehst du im Profilmenü bei **AI-Tokens**.

Aufrufe über einen **externen Connector**, beispielsweise Claude, verbrauchen
keine PaceKeeper-AI-Token. Es können jedoch die Nutzungsgrenzen oder Kosten des
jeweiligen externen Anbieters gelten. Sobald PaceKeeper AI öffentlich
verfügbar ist, sollen Abonnements mit einem größeren monatlichen
Token-Kontingent über den App Store beziehungsweise Play Store angeboten
werden.

### Hauptnavigation

<!-- code-ref:
  - lib/widgets/dashboard_bottom_nav.dart::DashboardBottomNav
  - lib/screens/dashboard_screen.dart::_sidebarNavItems
  - lib/screens/dashboard_screen.dart::_onNavTabChange
-->

| Symbol | Bereich | Bedeutung |
|---|---|---|
| 🚩 | **Plan** | Kalender für geplante Trainings, absolvierte Aktivitäten und Mahlzeiten. Die Ansicht kann zwischen Monat, Woche und Tag wechseln. |
| 👤 | **Athlet** | Persönliche Leistungs-, Wellness- und Verlaufsdaten sowie eigene Charts. |
| ▣ | **Dashboard** | Tagesansicht. Wische zwischen den vergangenen sieben Tagen, heute und den nächsten sieben Tagen. |
| ⚙️ | **Einstellungen** | Synchronisierung, KI, Darstellung, Werkzeuge, Daten, Hilfe und Diagnose. |

Auf Mobilgeräten befindet sich die Navigation unten. Auf Geräten im
Querformat oder mit größerem Bildschirm kann sie als Seitenleiste erscheinen.

### Kopfbereich und Bereitschaft

<!-- code-ref:
  - lib/widgets/pk_header/pk_gradient_header.dart
  - lib/widgets/pk_header/pk_header_theme.dart::PkHeaderMetricStyle
  - lib/widgets/pk_header/pk_metric_detail_sheet.dart
  - lib/widgets/pk_header/pk_athlete_sheet.dart::showPkAthleteSheet
-->

Der farbige Ring um dein Profilbild zeigt deine aktuelle **Bereitschaft**.
Tippe auf das Profilbild, um den aktiven Athleten zu wechseln, Lizenz und
KI-Token anzusehen, Zugriffe und Freigaben zu verwalten, die
Athleten-Einstellungen zu öffnen oder dich abzumelden.

Wische den Kopfbereich seitwärts, um Gründe für die Bereitschaft und weitere
Wellness-Werte zu sehen. Ein Tipp auf eine Kennzahl öffnet eine kurze Erklärung
und ihren 7-Tage-Verlauf.

| Kürzel/Symbol | Bedeutung |
|---|---|
| ♥ **HF** | Ruhe-Herzfrequenz |
| Herzmonitor **HRV** | Herzratenvariabilität |
| ⚡ **CTL** | längerfristige Trainingsbelastung bzw. Fitness |
| 🔥 **ATL** | kurzfristige Trainingsbelastung bzw. Ermüdung |
| Blatt **TSB** | Form; Verhältnis von langfristiger zu kurzfristiger Belastung |
| ↑ / ↓ / → | Wert steigt, fällt oder bleibt stabil |
| Grün / Rot / Grau | günstig, ungünstig oder keine wesentliche Änderung; die genaue Wertung hängt von der Kennzahl ab |

### Dashboard verwenden

<!-- code-ref:
  - lib/screens/dashboard/today/today_detail_mobile.dart
  - lib/widgets/today_create_action_sheet.dart::TodayCreateActionSheet
-->

Das Dashboard öffnet immer bei **Heute**. Wische horizontal, um die
vergangenen oder kommenden sieben Tage zu sehen. Wenn der Kopfbereich beim
Scrollen verschwindet, ziehe die Seite nach unten, um ihn wieder einzublenden.

Tippe auf einen Eintrag, um Details zu einem Training oder einer Aktivität zu
öffnen. Je nach Eintrag kannst du Daten ansehen, bearbeiten, erneut von
intervals.icu laden oder speichern und synchronisieren.

Über **+** kannst du derzeit:

- ein Training anlegen,
- eine Aktivität als FIT- oder TCX-Datei importieren,
- eine Aktivität aus Bosch eBike Connect importieren.

Das manuelle Anlegen einer Mahlzeit ist in diesem Menü derzeit deaktiviert.

### Plan und Kalender

<!-- code-ref:
  - lib/screens/dashboard/plan/calendar_shell_v1.dart::CalendarShellV1
  - lib/screens/dashboard/plan/parts/calendar_shell_widgets.dart
-->

Im Bereich **Plan** kannst du:

- zwischen Monats-, Wochen- und Tagesansicht wechseln,
- mit den Pfeilen zum vorherigen oder nächsten Zeitraum springen,
- mit **Heute** zum aktuellen Datum zurückkehren,
- Trainings, Mahlzeiten und Aktivitäten filtern,
- Einträge öffnen und – sofern unterstützt – bearbeiten,
- Wochen- und Aktivitätssummen wie Zeit, TSS, Kalorien und Höhenmeter ansehen,
- Trainings- und Ernährungspläne sowie KI-Aktionen öffnen.

KI-Vorschläge werden vor dem Übernehmen als Vorschau angezeigt. Prüfe Inhalt,
Datum und betroffenen Zeitraum sorgfältig. Erst **Übernehmen** schreibt die
vorgeschlagenen Änderungen; **Verwerfen** lässt den bestehenden Plan
unverändert. Falls angeboten, macht **Rückgängig** die zuletzt angewendete
Änderung wieder rückgängig.

### Athlet

<!-- code-ref:
  - lib/screens/dashboard_screen.dart::_buildAthleteTab
  - lib/screens/dashboard/athlete/athlete_info_chip.dart::_AthleteInfoChip
  - lib/features/settings/ui_settings_store.dart
-->

Der Bereich **Athlet** zeigt deine Entwicklung über auswählbare Zeiträume. Dazu
können Trainings- und Wellness-Werte, eigene Diagramme sowie Werte wie
Ruhe-HF, HRV, Schlaf, Blutdruck, Schritte, Gewicht, Körperfett und VO₂max
gehören. Welche Daten erscheinen, hängt von den angeschlossenen Quellen ab.

### Zugriffe, Freigaben und betreute Athleten

<!-- code-ref:
  - lib/screens/managed/managed_athletes_screen.dart::ManagedAthletesScreen
  - lib/features/pk_state/data/pacekeeper_connected_athlete_client.dart
  - lib/widgets/pk_header/pk_athlete_sheet.dart
-->

Über das Profilbild und **Zugriffe & Freigaben** können Athleten ihre Daten
gezielt mit einer anderen Person teilen. Das ist beispielsweise für Trainer
oder gemeinsam betreute Athleten gedacht.

So wird ein Zugriff eingerichtet:

1. Die Person, die Zugriff erhalten soll, wählt **Zugriff anfragen**.
2. Sie trägt die intervals.icu-Athlet-ID des Dateninhabers (Owner) ein.
3. Sie wählt die gewünschten Rechte. Standardmäßig sind alle Leserechte
   aktiviert.
4. Der Owner sieht die Anfrage unter **Eingehende Zugriffsanfragen**, prüft die
   Rechte und gibt sie frei oder lehnt sie ab.
5. Nach der Freigabe erscheint der Athlet unter **Aktive Zugriffe** und kann
   über das Profilmenü ausgewählt werden.

Rechte lassen sich getrennt für **Profil, Kalender, Training, Wellness und
Ernährung** vergeben. Lese- und Schreibrechte sind eigenständig. Gewähre nur
die Rechte, die tatsächlich benötigt werden: Schreibrechte erlauben Änderungen
an den entsprechenden Daten. Der Owner kann eine Freigabe jederzeit beenden;
die andere Person kann ihren Zugriff ebenfalls beenden. Eine noch offene
Anfrage kann zurückgezogen werden.

Freigegebene Daten können auch verarbeitet werden, wenn die App des Owners
nicht geöffnet ist. Dafür muss die notwendige Server- und
Hintergrund-Synchronisierung eingerichtet sein.

### Ernährung und Einkaufsliste

<!-- code-ref:
  - lib/screens/dashboard/plan/calendar_shell_v1.dart::_openAiActionSheet
  - lib/screens/dashboard/plan/meal_edit_sheet.dart::showMealEditSheet
  - lib/screens/dashboard/plan/meal_recipe_bottom_sheet.dart
-->

Im Kalender werden Mahlzeiten gemeinsam mit Trainings und Aktivitäten
angezeigt. Öffne eine Mahlzeit, um Rezeptdetails zu sehen. Vorhandene
Mahlzeiten lassen sich bearbeiten; dazu gehören Name, Uhrzeit, Kalorien,
Protein, Kohlenhydrate, Fett, Zutaten und Zubereitung. Beim Speichern werden
die Änderungen synchronisiert. **Löschen** entfernt die Mahlzeit nach einer
Bestätigung.

Über **KI-Aktionen → Ernährung** kann PaceKeeper AI Ernährungsvorschläge für
den gewählten Zeitraum vorbereiten. Prüfe Wochenmenü, Mengen, Allergien und
persönliche Vorgaben in der Vorschau, bevor du die Daten übernimmst.

Unter **KI-Aktionen → Einkaufsliste** werden die Zutaten des gewählten
Zeitraums zusammengeführt. Auf unterstützten Geräten kann die Liste über die
externe **Bring!**-Übergabe geöffnet werden. Falls Bring! nicht verfügbar ist,
kannst du die zusammengefassten Zutaten kopieren und manuell in eine andere
Einkaufsliste einfügen.

### Wichtige Symbole

<!-- code-ref:
  - lib/widgets/dashboard_bottom_nav.dart
  - lib/widgets/pk_header
  - lib/screens/dashboard/plan/calendar_shell_v1.dart
  - lib/screens/dashboard/today/today_detail_mobile.dart
-->

| Symbol | Aktion |
|---|---|
| ＋ | neuen Eintrag oder neue Aktion anlegen |
| ✎ | Eintrag bearbeiten |
| 🗑 | Eintrag löschen; eine Bestätigung kann erforderlich sein |
| ↻ / Sync | Daten aktualisieren oder synchronisieren |
| ★ / Pin | Chart oder Inhalt im Dashboard anheften |
| ⧉ | Daten oder Text kopieren |
| ⤢ | Detail- oder Vollansicht öffnen |
| ‹ / › | vorheriger bzw. nächster Zeitraum |
| ⋮ | weitere Aktionen |
| Verlaufssymbol | Änderungsverlauf öffnen |
| Glocke | Status der KI-Warteschlange öffnen; sie ist keine allgemeine Nachrichten-Glocke |
| › | Unterseite oder weitere Einstellungen öffnen |

Die konkrete Darstellung eines Symbols kann sich zwischen iOS, macOS und
Android geringfügig unterscheiden. Halte den Mauszeiger über ein Symbol oder
drücke es länger, wenn die Plattform einen Hinweistext unterstützt.

### Einstellungen und Synchronisierung

<!-- code-ref:
  - lib/screens/settings/settings_screen.dart::SettingsContent
  - lib/features/pk_state/pk_state_controller.dart::PkStateController
-->

Unter **Einstellungen** findest du insbesondere:

- **Jetzt synchronisieren:** Daten und Trends neu abrufen.
- **Hintergrund-Synchronisierung:** hält Daten auch ohne geöffnete App für
  andere Geräte aktuell. Dabei wird ein verschlüsselter intervals.icu-Token am
  Server hinterlegt.
- **Health Sync:** liest auf unterstützten Mobilgeräten Gesundheitswerte und
  kann sie optional zu intervals.icu übertragen.
- **Profil aktualisieren:** löscht lokal zwischengespeicherte Profildaten und
  lädt sie vollständig neu.
- **KI-Assistent verbinden / KI-Einstellungen:** verbindet unterstützte
  KI-Apps und konfiguriert KI-Aktionen.
- **Trend, Darstellung und Chart-Einstellungen:** passt Zeiträume, Oberfläche
  und eigene Diagramme an.
- **Tools & Daten:** enthält Hilfswerkzeuge, intervals.icu-Werkzeuge und die
  Verwaltung lokal gespeicherter Daten.
- **Debug-Infos:** sammelt App-, Geräte- und Profilinformationen für den
  Support.

### Wenn Daten fehlen oder veraltet sind

1. Prüfe deine Internetverbindung und den aktuell gewählten Athleten.
2. Wähle **Einstellungen → Jetzt synchronisieren**.
3. Prüfe die Verbindung zu intervals.icu und bei betreuten Athleten den
   hinterlegten API-Key.
4. Nutze **Profil aktualisieren**, wenn Profil- oder Wellness-Daten weiterhin
   fehlen. Beachte, dass dabei lokale Zwischenspeicher neu aufgebaut werden.
5. Öffne für eine Supportanfrage **Einstellungen → Debug-Infos** und kopiere
   die dort angebotenen Angaben. Teile keine Passwörter oder privaten
   API-Schlüssel.

[Nach oben](#pacekeeper-ai--app-hilfe--app-help)

---

## English

<!-- translation-of: #deutsch
     Keep both language sections structurally aligned. -->

### What is PaceKeeper AI for?

PaceKeeper AI combines training plans, completed activities, wellness data, and
performance metrics in one place. It synchronises with **intervals.icu** and
helps you understand your current condition, plan training and nutrition, and
prepare changes with AI assistance.

### First start

1. Sign in through **intervals.icu**.
2. PaceKeeper AI imports available profile information from intervals.icu.
3. Review and complete it in the setup assistant that opens automatically.
   Missing information reduces the quality of later training and nutrition
   suggestions.
4. Wait for the first synchronisation to finish.
5. Review your day in **Dashboard** and your calendar under **Plan**.

Depending on whether you selected training, nutrition, or both, the assistant
asks for:

- name, gender, date of birth, height, and weight,
- automatic weight synchronisation,
- work days, working hours, or shift work,
- sports you actually practise and your training goal,
- nutrition goal, diet type, and additional focus areas,
- meat/fish frequency, cuisine, and preparation style,
- allergies, intolerances, dislikes, and preferences,
- meals you want to plan and their usual times.

> **Important:** Imported intervals.icu values are a starting point, not a
> guarantee that they are correct. Check body data, sports, and your training
> goal in particular before saving.

You can reopen the assistant under **Settings → Setup assistant** and replay
the short introduction with **Settings → Replay tutorial**.

### Connecting Claude.ai to PaceKeeper AI

The PaceKeeper AI connector lets Claude read the data you authorise and, after
your confirmation, prepare or modify plans, phases, workouts, and nutrition
entries.

1. In PaceKeeper AI, open **Settings → Connect AI assistant**.
2. Generate a one-time six-digit code. It is valid for five minutes; generate
   a new one if it expires.
3. On [claude.ai](https://claude.ai), open **Customize → Connectors**.
4. Select **+ → Add custom connector**. Use **PaceKeeper AI** as its name and
   `https://www.pacekeeper.icu/mcp` as the server URL.
5. Select **Add/Connect**. Enter the code from the app on PaceKeeper's
   connection page and confirm.
6. Enable PaceKeeper AI in a conversation through **+ → Connectors**. You can
   enable or disable it separately for each conversation.

For Claude Team or Enterprise, an Owner must first add the custom connector to
the organisation. Each member can then connect their own account. Anthropic
currently also classifies custom connectors as beta. See the
[official Claude instructions](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp).

For write operations, always review Claude's tool call and then check the
preview or change history in PaceKeeper AI. Only connect the server address
shown above.

### ChatGPT connector

The PaceKeeper AI connector has also been **submitted to ChatGPT for review**.
During the alpha phase, this does not mean that it is already available to all
users. Use it only once PaceKeeper AI is actually listed in ChatGPT's connected
apps or connectors. This guide will be updated with the final setup flow after
approval.

### Creating your first plan

1. Open **Plan**, then use the calendar icon to open **My plans**.
2. Select **New plan**.
3. Choose the **plan type**: nutrition, training, or training with coordinated
   nutrition.
4. Enter the start and end date for the complete plan.
5. For a training plan, define the main goal as an A race with its name, date,
   target, and sport. Add B and C races where appropriate.
6. Under **Structure**, select the sports and available weekdays or times of
   day for each sport.
7. Under **Events**, add all known restrictions and special periods.
8. Save these plan parameters first.

#### Add events before generating phases

Available events include B/C races, **vacation, illness, injury, training
camp, work travel, recovery block**, and **other**. Enter a meaningful name,
date or period and, for “Other,” a description. This allows the AI to account
for these periods when distributing load, recovery, and workouts.

If a vacation or another important event is added later, update the plan and
have the affected phases and workouts reviewed or optimised again.

#### 1. Generate phases

After saving the plan parameters, select **✨ Phases** on the plan. PaceKeeper
AI uses its integrated OpenAI connection to propose a periodisation. Verify
that it covers the entire plan without gaps and appropriately considers goals,
events, progressive load, recovery, peak, and race week before applying it.

Alternatively, ask Claude through the connected connector to create or revise
the phases of the existing plan. For example: “Review my plan, consider every
event, and create suitable training phases through my A goal.” The same
external workflow is intended for ChatGPT after approval.

#### 2. Generate workouts for every phase

Phases do not yet contain individual sessions. Select **✨ Trainings** on
**each phase**, then check sport, date, duration, intensity, recovery days, and
compatibility with work, vacation, and other events. Repeat until every phase
contains its workouts.

These sessions can be created or adjusted either by the integrated AI or
externally through Claude and, later, ChatGPT.

#### 3. Generate nutrition week by week

Nutrition plans should generally be generated **one week at a time**. This
makes it easier to account for working hours, upcoming workouts, shopping, and
short-term changes. Use **AI actions → Nutrition**, or ask Claude through the
connector to create nutrition for a specific calendar week. Review allergies,
intolerances, calories, macronutrients, portions, and ingredients before
applying it. This workflow is also intended for ChatGPT after approval.

### AI tokens and external connectors

> [!IMPORTANT]
> PaceKeeper AI's **integrated AI** uses the app's monthly AI-token allowance.
> The free tier only includes a small number of free tokens. The allowance is
> renewed each month; the remaining percentage is shown as **AI tokens** in the
> profile menu.

Requests made through an **external connector**, such as Claude, do not use
PaceKeeper AI tokens. The external provider's own usage limits or charges may
still apply. Once PaceKeeper AI is publicly available, subscriptions with a
larger monthly token allowance are planned through the App Store and Play
Store.

### Main navigation

| Icon | Section | Purpose |
|---|---|---|
| 🚩 | **Plan** | Calendar for planned workouts, completed activities, and meals. Switch between month, week, and day. |
| 👤 | **Athlete** | Personal performance, wellness, history, and custom charts. |
| ▣ | **Dashboard** | Daily view. Swipe between the previous seven days, today, and the next seven days. |
| ⚙️ | **Settings** | Synchronisation, AI, appearance, tools, data, help, and diagnostics. |

On phones, navigation is shown at the bottom. In landscape or on larger
screens, it may appear in a sidebar.

### Header and readiness

The coloured ring around your profile picture shows your current
**readiness**. Tap the picture to switch athlete, view your licence and AI
tokens, manage access and sharing, open athlete settings, or sign out.

Swipe the header sideways to see readiness reasons and additional wellness
values. Tap a metric for a short explanation and its seven-day history.

| Abbreviation/icon | Meaning |
|---|---|
| ♥ **HR** | Resting heart rate |
| Heart monitor **HRV** | Heart-rate variability |
| ⚡ **CTL** | Long-term training load or fitness |
| 🔥 **ATL** | Short-term training load or fatigue |
| Leaf **TSB** | Form; relationship between long- and short-term load |
| ↑ / ↓ / → | Value is rising, falling, or stable |
| Green / red / grey | favourable, unfavourable, or no material change; exact interpretation depends on the metric |

### Using the Dashboard

Dashboard always opens on **Today**. Swipe horizontally to see the previous or
next seven days. If the header disappears while scrolling, pull down to show it
again.

Tap an entry to open workout or activity details. Depending on the entry, you
can view or edit data, reload it from intervals.icu, or save and synchronise it.

Use **+** to:

- create a workout,
- import an activity from a FIT or TCX file,
- import an activity from Bosch eBike Connect.

Manual meal creation is currently disabled in this menu.

### Plan and calendar

In **Plan**, you can:

- switch between month, week, and day,
- use the arrows to move to the previous or next period,
- return to the current date with **Today**,
- filter workouts, meals, and activities,
- open and, where supported, edit entries,
- review weekly and activity totals such as time, TSS, calories, and elevation,
- open training plans, nutrition planning, and AI actions.

AI suggestions are shown as a preview before they are applied. Carefully check
the content, date, and affected period. **Apply** writes the suggested changes;
**Discard** leaves the current plan unchanged. Where available, **Undo**
reverts the most recently applied change.

### Athlete

The **Athlete** section shows your development across selectable time ranges.
It may contain training and wellness metrics, custom charts, and values such as
resting heart rate, HRV, sleep, blood pressure, steps, weight, body fat, and
VO₂max. The available data depends on your connected sources.

### Access, sharing, and managed athletes

Use the profile picture and **Access & sharing** to share selected athlete data
with another person, such as a coach or someone managing an athlete.

To set up access:

1. The person who needs access selects **Request access**.
2. They enter the data owner's intervals.icu athlete ID.
3. They select the requested permissions. All read permissions are enabled by
   default.
4. The owner reviews the item under **Incoming requests**, adjusts the
   permissions if necessary, and approves or rejects it.
5. Once approved, the athlete appears under **Active connections** and can be
   selected from the profile menu.

Permissions are granted separately for **Profile, Calendar, Workouts,
Wellness, and Nutrition**. Read and write permissions are independent. Grant
only what is needed: write access permits changes to the corresponding data.
The owner can end sharing at any time, and the other person can end their
access. A pending request can be withdrawn.

Shared data can also be processed while the owner's app is closed, provided
the required server and background synchronisation are configured.

### Nutrition and shopping list

Meals appear in the calendar alongside workouts and activities. Open a meal to
view its recipe details. Existing meals can be edited, including name, time,
calories, protein, carbohydrates, fat, ingredients, and preparation. Saving
synchronises the changes. **Delete** removes the meal after confirmation.

Use **AI actions → Nutrition** to let PaceKeeper AI prepare nutrition
suggestions for the selected period. Review the weekly menu, quantities,
allergies, and personal requirements in the preview before applying it.

Under **AI actions → Shopping list**, ingredients for the selected period are
combined. On supported devices, the list can be opened through the external
**Bring!** handoff. If Bring! is unavailable, copy the combined ingredients
and paste them into another shopping-list app manually.

### Important icons

| Icon | Action |
|---|---|
| ＋ | create a new entry or action |
| ✎ | edit an entry |
| 🗑 | delete an entry; confirmation may be required |
| ↻ / Sync | refresh or synchronise data |
| ★ / Pin | pin a chart or content to Dashboard |
| ⧉ | copy data or text |
| ⤢ | open details or full view |
| ‹ / › | previous or next period |
| ⋮ | more actions |
| History icon | open change history |
| Bell | open AI queue status; this is not a general notification inbox |
| › | open a subpage or further settings |

An icon's exact appearance can vary slightly between iOS, macOS, and Android.
Hover over it or press and hold it where the platform supports help text.

### Settings and synchronisation

Important options under **Settings** include:

- **Sync now:** fetch data again and update trends.
- **Background sync:** keeps data current for other devices while the app is
  closed. An encrypted intervals.icu token is stored on the server.
- **Health sync:** reads health values on supported mobile devices and can
  optionally upload them to intervals.icu.
- **Refresh profile:** clears locally cached profile information and downloads
  it again.
- **Connect AI assistant / AI settings:** connects supported AI apps and
  configures AI actions.
- **Trend, Appearance, and Chart settings:** customise time ranges, the user
  interface, and personal charts.
- **Tools & data:** provides utilities, intervals.icu tools, and local data
  management.
- **Debug info:** collects app, device, and profile details for support.

### If data is missing or out of date

1. Check your internet connection and the selected athlete.
2. Select **Settings → Sync now**.
3. Check the intervals.icu connection and, for managed athletes, the stored API
   key.
4. Use **Refresh profile** if profile or wellness information is still
   missing. Local caches will be rebuilt.
5. For a support request, open **Settings → Debug info** and copy the details
   provided there. Never share passwords or private API keys.

[Back to top](#pacekeeper-ai--app-hilfe--app-help)

<!-- screenshot-plan:
  Capture the same five views in German and English where practical:
  1. Dashboard with readiness ring and metric labels
  2. Plan calendar with view switcher and action buttons
  3. Athlete view with charts and time-range controls
  4. Access & sharing with anonymised athlete data
  5. Nutrition preview and Bring! shopping-list action
  Store assets under images/app-help/ and add short alt text.
-->
