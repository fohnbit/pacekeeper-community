# Claude, ChatGPT und KI-Token

<!-- screenshot-plan:
  - Einstellungen > KI-Assistent verbinden mit anonymisiertem Einmalcode
  - Claude > Customize > Connectors mit PaceKeeper AI
-->

[← Ernährungsplanung](DE-Ernaehrungsplanung) · [Inhaltsverzeichnis](Deutsch) · [Weiter: Zugriffe und Einstellungen →](DE-Zugriffe-und-Einstellungen)

## Claude.ai mit PaceKeeper AI verbinden

<!-- code-ref:
  - lib/screens/settings/mcp_connect_screen.dart::McpConnectScreen
  - lib/features/pk_state/data/pacekeeper_mcp_link_code_client.dart
-->

Der PaceKeeper-AI-Connector erlaubt Claude, freigegebene Daten zu lesen und –
nach deiner Bestätigung – Pläne, Phasen, Trainings oder Ernährungseinträge
vorzubereiten beziehungsweise zu ändern.

1. Öffne in PaceKeeper AI **Einstellungen → KI-Assistent verbinden**.
2. Lass einen einmaligen sechsstelligen Code erzeugen. Er ist fünf Minuten
   gültig.
3. Öffne auf [claude.ai](https://claude.ai) **Anpassen/Customize →
   Connectors**.
4. Wähle **+ → Add custom connector**.
5. Trage als Namen **PaceKeeper AI** ein.
6. Trage als Server-URL `https://www.pacekeeper.icu/mcp` ein.
7. Wähle **Add/Connect** und gib auf der PaceKeeper-Verbindungsseite den Code
   aus der App ein.
8. Aktiviere PaceKeeper AI im gewünschten Chat über **+ → Connectors**.

Der Connector lässt sich pro Unterhaltung ein- oder ausschalten. Bei Claude
Team oder Enterprise muss ein Owner ihn zuerst für die Organisation
hinzufügen. Danach verbindet jedes Mitglied sein eigenes Konto.

Benutzerdefinierte Claude-Connectoren befinden sich laut Anthropic derzeit in
einer Beta-Phase. Weitere Details stehen in der
[offiziellen Claude-Anleitung](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp).

> [!CAUTION]
> Prüfe bei schreibenden Aktionen Claudes Werkzeugaufruf und danach die
> Vorschau oder den Änderungsverlauf in PaceKeeper AI. Verbinde ausschließlich
> die oben genannte Server-Adresse.

## Status des ChatGPT-Connectors

Der PaceKeeper-AI-Connector wurde bei **ChatGPT zur Prüfung eingereicht**.
Während der Alpha-Phase bedeutet das noch nicht, dass er bereits für alle
Nutzer verfügbar ist. Verwende ihn erst, wenn PaceKeeper AI in ChatGPT
tatsächlich unter den verbundenen Apps beziehungsweise Connectoren angeboten
wird.

Nach der Freigabe wird diese Dokumentation um den endgültigen
ChatGPT-Einrichtungsablauf ergänzt.

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
| ChatGPT-Connector | nach Freigabe über ChatGPT | werden nicht verbraucht |

> [!IMPORTANT]
> Die kostenlose Variante enthält nur einige freie Token für die integrierte
> KI. Das Kontingent wird jeden Monat erneuert. Den verbleibenden Anteil siehst
> du im Profilmenü unter **AI-Tokens**.

Externe Connectoren verbrauchen keine PaceKeeper-AI-Token. Es können jedoch
Nutzungsgrenzen oder Kosten beim jeweiligen externen Anbieter entstehen.
Sobald PaceKeeper AI öffentlich verfügbar ist, sollen über App Store und Play
Store Abonnements mit einem größeren monatlichen Token-Kontingent angeboten
werden.

[← Ernährungsplanung](DE-Ernaehrungsplanung) · [Inhaltsverzeichnis](Deutsch) · [Weiter: Zugriffe und Einstellungen →](DE-Zugriffe-und-Einstellungen)
