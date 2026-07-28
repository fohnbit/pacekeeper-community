# ChatGPT mit PaceKeeper AI verbinden

[← KI-Connectoren und Token](DE-KI-Connectoren-und-Token) · [Inhaltsverzeichnis](Deutsch) · [Claude.ai verbinden →](DE-Claude-ai-verbinden)

Diese Anleitung beschreibt, wie du PaceKeeper AI erstmals mit ChatGPT verbindest und die Verbindung nach einem PaceKeeper-Update aktualisierst.

## Voraussetzung

Aktiviere in ChatGPT den Entwicklermodus:

**Einstellungen → Sicherheit und Anmeldung → Entwicklermodus**

Die Verfügbarkeit kann von deinem ChatGPT-Konto und den Regeln deines Workspace abhängen. Wenn die Einstellung fehlt oder gesperrt ist, wende dich an deinen Workspace-Administrator.

## PaceKeeper AI erstmals verbinden

1. Öffne in ChatGPT die Seite [Plugins](https://chatgpt.com/plugins).
2. Klicke rechts oben auf das **Pluszeichen**.
3. Trage folgende Verbindungsdaten ein:

   - Name: `PaceKeeper AI Dev`
   - Beschreibung: `Training, Ernährung und Planung mit PaceKeeper AI`
   - URL: `https://pacekeeper.icu/mcp`

4. Erstelle die Verbindung.
5. Öffne in PaceKeeper AI **Einstellungen → KI-Assistent verbinden**.
6. Erzeuge einen neuen sechsstelligen Einmalcode. Er ist fünf Minuten gültig.
7. Gib den Code auf der geöffneten PaceKeeper-Verbindungsseite ein.
8. Bestätige die Verbindung.
9. Prüfe in ChatGPT, ob bei PaceKeeper AI die Autorisierung `OAuth` und der Status `development` angezeigt werden.
10. Wähle **Im Chat testen**, um eine neue Unterhaltung zu öffnen.

Empfohlener erster Test:

> Verwende PaceKeeper AI Dev und zeige mir mein nächstes geplantes Training.

## Aktuelle Server-Version prüfen

Kopiere diesen Text vollständig in einen neuen Chat:

> Rufe `pacekeeper_get_context` auf.
>
> Enthält die **Beschreibung** dieses Tools eine Zeile `Tool list built <A>`?
>
> **Nein** → Meine Tool-Liste ist **veraltet** und stammt von vor diesem Prüfverfahren. Sag mir, dass ich den Connector trennen und neu verbinden soll.
>
> **Ja** → Vergleiche `<A>` mit `mcp_version` aus der Antwort. Gleich bedeutet aktuell, unterschiedlich bedeutet veraltet und der Connector muss aktualisiert werden.

Aktuell auf dem PaceKeeper-Server läuft `mcp_version`: `{{MCP_VERSION}}`.

Fehlt `<A>` oder unterscheidet sich `<A>` von `mcp_version`, aktualisiere den Connector wie im nächsten Abschnitt beschrieben. Beende danach die ChatGPT-Software vollständig, starte sie neu und öffne einen neuen Chat.

## Verbindung nach einem PaceKeeper-Update aktualisieren

Führe diese Schritte aus, wenn PaceKeeper AI dich nach einem Update dazu auffordert oder neue Funktionen in ChatGPT noch nicht angezeigt werden:

1. Öffne in ChatGPT die Seite [Plugins](https://chatgpt.com/plugins).
2. Wechsle in den Bereich **Persönlich** neben **Öffentlich**.
3. Wähle **PaceKeeper AI** aus.
4. Öffne den **Drei-Punkte-Button** und wähle **Verwalten**.
5. Scrolle auf der Verwaltungsseite ganz nach unten.
6. Klicke auf **Aktualisieren**.
7. Warte, bis die Aktualisierung abgeschlossen ist.
8. Beende die ChatGPT-Software vollständig und starte sie neu.
9. Wähle anschließend **Im Chat testen** und beginne eine neue Unterhaltung.
10. Wiederhole den Versions-Test aus dem vorherigen Abschnitt.

Eine bereits laufende Unterhaltung kann noch den vorherigen Stand verwenden. Öffne deshalb nach einer Aktualisierung immer einen neuen Chat.

## Verbindung erneut autorisieren

Führe diese Schritte aus, wenn ChatGPT einen Anmelde-, Autorisierungs- oder Berechtigungsfehler meldet:

1. Öffne in ChatGPT die Details von **PaceKeeper AI Dev**.
2. Trenne die bisherige PaceKeeper-Verbindung, sofern diese Aktion angeboten wird.
3. Starte die Verbindung erneut.
4. Öffne in PaceKeeper AI **Einstellungen → KI-Assistent verbinden**.
5. Erzeuge einen neuen sechsstelligen Einmalcode.
6. Gib den neuen Code auf der PaceKeeper-Verbindungsseite ein und bestätige die Verbindung.
7. Öffne danach über **Im Chat testen** einen neuen Chat.

Ein abgelaufener oder bereits verwendeter Einmalcode kann nicht erneut verwendet werden.

## Wenn die Verbindung nicht funktioniert

- Prüfe, ob der Entwicklermodus in ChatGPT aktiviert ist.
- Prüfe, ob du exakt `https://pacekeeper.icu/mcp` eingetragen hast.
- Erzeuge einen neuen Code, wenn die fünf Minuten abgelaufen sind.
- Öffne nach einem PaceKeeper-Update unter **Persönlich** bei **PaceKeeper AI** über den Drei-Punkte-Button **Verwalten**, klicke ganz unten auf **Aktualisieren** und starte danach die ChatGPT-Software vollständig neu.
- Trenne und verbinde PaceKeeper AI erneut, wenn ein Autorisierungsfehler bestehen bleibt.
- Aktiviere PaceKeeper AI im neuen Chat, bevor du eine Anfrage stellst.
- Prüfe schreibende Aktionen vor der Bestätigung und kontrolliere das Ergebnis anschließend in PaceKeeper AI.

Quelle: [OpenAI – Connect and test your plugin](https://developers.openai.com/plugins/deploy/connect-chatgpt)

[← KI-Connectoren und Token](DE-KI-Connectoren-und-Token) · [Inhaltsverzeichnis](Deutsch) · [Claude.ai verbinden →](DE-Claude-ai-verbinden)
