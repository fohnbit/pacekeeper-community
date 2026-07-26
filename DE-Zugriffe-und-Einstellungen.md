# Zugriffe, Einstellungen und Fehlerbehebung

<!-- screenshot-plan:
  - Zugriffe & Freigaben ausschließlich mit anonymisierten Athletendaten
  - wichtigste Einstellungen
-->

[← App-Bedienung](DE-App-Bedienung) · [Inhaltsverzeichnis](Deutsch)

## Betreute Athleten und Freigaben

<!-- code-ref:
  - lib/screens/managed/managed_athletes_screen.dart::ManagedAthletesScreen
  - lib/features/pk_state/data/pacekeeper_connected_athlete_client.dart
  - lib/widgets/pk_header/pk_athlete_sheet.dart
-->

Über das Profilbild und **Zugriffe & Freigaben** können Athleten Daten gezielt
mit Trainern oder anderen betreuenden Personen teilen.

1. Die Person, die Zugriff erhalten soll, wählt **Zugriff anfragen**.
2. Sie trägt die intervals.icu-Athlet-ID des Dateninhabers ein.
3. Sie wählt die gewünschten Rechte.
4. Der Dateninhaber prüft die eingehende Anfrage, passt Rechte bei Bedarf an
   und gibt sie frei oder lehnt sie ab.
5. Nach der Freigabe kann der betreute Athlet über das Profilmenü ausgewählt
   werden.

Rechte werden getrennt für **Profil, Kalender, Training, Wellness und
Ernährung** vergeben. Lese- und Schreibrechte sind eigenständig. Schreibrechte
erlauben Änderungen an den entsprechenden Daten. Gewähre daher nur notwendige
Rechte.

Der Dateninhaber kann eine Freigabe jederzeit beenden. Die betreuende Person
kann ihren Zugriff ebenfalls beenden oder eine offene Anfrage zurückziehen.

## Wichtige Einstellungen

<!-- code-ref:
  - lib/screens/settings/settings_screen.dart::SettingsContent
  - lib/features/pk_state/pk_state_controller.dart::PkStateController
-->

- **Jetzt synchronisieren:** Daten und Trends neu abrufen.
- **Hintergrund-Synchronisierung:** hält Daten bei geschlossener App für andere
  Geräte und berechtigte Zugriffe aktuell.
- **Health Sync:** liest auf unterstützten Mobilgeräten Gesundheitswerte und
  kann sie optional zu intervals.icu übertragen.
- **Profil aktualisieren:** leert lokale Profil-Zwischenspeicher und lädt die
  Daten neu.
- **KI-Assistent verbinden:** verbindet Claude oder später ChatGPT.
- **KI-Einstellungen:** passt integrierte KI-Aktionen an.
- **Trend, Darstellung und Chart-Einstellungen:** verändert Zeiträume,
  Oberfläche und eigene Diagramme.
- **Tools & Daten:** enthält Hilfswerkzeuge und lokale Datenverwaltung.
- **Debug-Infos:** sammelt Angaben für eine Supportanfrage.

## Wenn Daten fehlen oder veraltet sind

1. Prüfe Internetverbindung und ausgewählten Athleten.
2. Wähle **Einstellungen → Jetzt synchronisieren**.
3. Prüfe die intervals.icu-Verbindung und bei betreuten Athleten den
   hinterlegten API-Key beziehungsweise die Freigabe.
4. Nutze **Profil aktualisieren**, wenn Profil- oder Wellness-Daten weiterhin
   fehlen.
5. Öffne für eine Supportanfrage **Einstellungen → Debug-Infos**.

Teile niemals Passwörter, private API-Schlüssel oder vollständige
Zugangstoken.

[← App-Bedienung](DE-App-Bedienung) · [Inhaltsverzeichnis](Deutsch)
