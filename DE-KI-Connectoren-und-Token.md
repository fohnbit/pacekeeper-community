# Claude, ChatGPT und KI-Token

<!-- screenshot-plan:
  - Einstellungen > KI-Assistent verbinden mit anonymisiertem Einmalcode
  - Claude > Customize > Connectors mit PaceKeeper AI
-->

[← Ernährungsplanung](DE-Ernaehrungsplanung) · [Inhaltsverzeichnis](Deutsch) · [Weiter: Zugriffe und Einstellungen →](DE-Zugriffe-und-Einstellungen)

## Assistent verbinden

<!-- code-ref:
  - lib/screens/settings/mcp_connect_screen.dart::McpConnectScreen
  - lib/features/pk_state/data/pacekeeper_mcp_link_code_client.dart
-->

- [ChatGPT mit PaceKeeper AI verbinden](DE-ChatGPT-verbinden)
- [Claude.ai mit PaceKeeper AI verbinden](DE-Claude-ai-verbinden)

Beide Anleitungen beschreiben die erste Einrichtung, das erneute Autorisieren
und das Aktualisieren der Verbindung nach Änderungen am Connector.

| ⚠️ **Vorsicht** |
|---|
| Prüfe bei schreibenden Aktionen den Werkzeugaufruf des Assistenten und danach die Vorschau oder den Änderungsverlauf in PaceKeeper AI. Verwende ausschließlich die in den Detailanleitungen genannte Server-Adresse. |

## Verfügbarkeit

Die Verfügbarkeit von Apps und benutzerdefinierten MCP-Verbindungen hängt beim
jeweiligen Anbieter vom Tarif und bei verwalteten Konten zusätzlich von den
Workspace-Einstellungen ab. Die Detailseiten nennen deshalb sowohl den
normalen Verbindungsweg als auch die erforderlichen Admin-Schritte.

## Integrierte KI oder externer Connector?

<!-- code-ref:
  - lib/features/pk_state/data/pacekeeper_license_client.dart::PaceKeeperLicenseState
  - lib/widgets/pk_header/pk_athlete_sheet.dart
  - lib/screens/settings/subscription_store_screen.dart
-->

| Variante | Verwendung | PaceKeeper-AI-Token |
|---|---|---|
| Integrierte KI | KI-Schaltflächen direkt in der App; Verarbeitung über OpenAI | werden verbraucht |
| Claude-Connector | Auftrag in einem Claude-Chat mit aktiviertem PaceKeeper-Connector | werden nicht verbraucht |
| ChatGPT-Connector | Auftrag in einem Chat mit aktivierter PaceKeeper-App | werden nicht verbraucht |

| ❗ **Wichtig** |
|---|
| Die kostenlose Variante enthält nur einige freie Token für die integrierte KI. Das Kontingent wird jeden Monat erneuert. Den verbleibenden Anteil siehst du im Profilmenü unter **AI-Tokens**. |

Externe Connectoren verbrauchen keine PaceKeeper-AI-Token. Es können jedoch
Nutzungsgrenzen oder Kosten beim jeweiligen externen Anbieter entstehen.
Sobald PaceKeeper AI öffentlich verfügbar ist, sollen über App Store und Play
Store Abonnements mit einem größeren monatlichen Token-Kontingent angeboten
werden.

[← Ernährungsplanung](DE-Ernaehrungsplanung) · [Inhaltsverzeichnis](Deutsch) · [Weiter: Zugriffe und Einstellungen →](DE-Zugriffe-und-Einstellungen)
