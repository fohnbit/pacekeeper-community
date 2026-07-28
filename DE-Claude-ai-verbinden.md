# Claude.ai mit PaceKeeper AI verbinden

[← ChatGPT verbinden](DE-ChatGPT-verbinden) · [Inhaltsverzeichnis](Deutsch) · [KI-Connectoren und Token →](DE-KI-Connectoren-und-Token)

Der PaceKeeper-AI-Connector erlaubt Claude, freigegebene PaceKeeper-Daten zu lesen und – nach deiner Prüfung – unterstützte Änderungen vorzubereiten oder auszuführen.

## Voraussetzungen

- Du bist in PaceKeeper AI angemeldet und hast einen Athleten ausgewählt.
- Du verwendest `https://www.pacekeeper.icu/mcp` als Server-Adresse.
- Dein Claude-Tarif erlaubt Custom Connectors. Bei Team oder Enterprise muss ein Owner den Connector gegebenenfalls zuerst für die Organisation hinzufügen.

## Erste Einrichtung für ein persönliches Claude-Konto

1. Öffne PaceKeeper AI und wähle **Einstellungen → KI-Assistent verbinden**.
2. Erzeuge einen neuen sechsstelligen Code. Der Code ist fünf Minuten gültig.
3. Öffne [claude.ai](https://claude.ai).
4. Öffne **Anpassen/Customize → Connectors**.
5. Wähle **+ → Add custom connector**.
6. Trage als Namen **PaceKeeper AI** ein.
7. Trage als Remote-MCP-Server-URL ausschließlich `https://www.pacekeeper.icu/mcp` ein.
8. Wähle **Add** beziehungsweise **Connect**. Eigene OAuth Client ID und Client Secret sind für die normale PaceKeeper-Einrichtung nicht einzutragen.
9. Gib auf der PaceKeeper-Verbindungsseite den sechsstelligen Code aus der App ein und bestätige die Verbindung.
10. Aktiviere PaceKeeper AI im gewünschten Chat über **+ → Connectors**.

## Team und Enterprise

1. Ein Owner fügt PaceKeeper AI unter den Organisations-Connectoren mit `https://www.pacekeeper.icu/mcp` hinzu.
2. Jedes Mitglied öffnet anschließend **Anpassen/Customize → Connectors**.
3. Das Mitglied wählt beim Connector **PaceKeeper AI** die Aktion **Connect**.
4. Das Mitglied erzeugt in seiner eigenen PaceKeeper-App einen sechsstelligen Code und schließt damit seine persönliche Autorisierung ab.

Der Organisations-Connector ersetzt nicht die persönliche Verbindung jedes PaceKeeper-Kontos.

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

Fehlt `<A>` oder unterscheidet sich `<A>` von `mcp_version`, öffne die Verwaltung von **PaceKeeper AI** und klicke auf **Refresh**. Öffne danach einen neuen Chat und wiederhole den Test.

## Verbindung nach einem Update erneuern

Eine erneute Verbindung ist sinnvoll oder erforderlich, wenn:

- PaceKeeper AI ausdrücklich zum erneuten Verbinden auffordert,
- Claude einen Authentifizierungs- oder Berechtigungsfehler meldet,
- neue PaceKeeper-Werkzeuge nach einem Update fehlen,
- der Connector mit einer alten oder falschen Server-Adresse angelegt wurde,
- Anthropic oder PaceKeeper die Connector-Metadaten geändert hat.

Für eine aktualisierte Tool-Liste genügt in Claude normalerweise **Refresh**:

1. Öffne in Claude **Anpassen/Customize → Connectors**.
2. Öffne bei **PaceKeeper AI** das Drei-Punkte-Menü beziehungsweise die Verwaltung.
3. Klicke auf **Refresh** und warte, bis die Aktualisierung abgeschlossen ist.
4. Öffne einen neuen Chat, aktiviere PaceKeeper AI und wiederhole den Versions-Test.

Nur wenn **Refresh** nicht angeboten wird oder ein Autorisierungsfehler bestehen bleibt, entferne den Connector, füge ihn erneut mit `https://www.pacekeeper.icu/mcp` hinzu und autorisiere ihn mit einem neuen Einmalcode aus der PaceKeeper-App.

## Verbindung testen und Fehler beheben

1. Öffne einen neuen Chat und aktiviere PaceKeeper AI unter **+ → Connectors**.
2. Frage beispielsweise: „Was ist mein nächstes Training?“
3. Prüfe bei „Connector nicht verfügbar“, ob er für diesen Chat aktiviert ist.
4. Prüfe bei Autorisierungsfehlern, ob der Einmalcode noch gültig ist; erzeuge andernfalls einen neuen.
5. Klicke auf **Refresh**, wenn Claude weiterhin alte oder fehlende Werkzeuge anzeigt; entferne und verbinde ihn nur dann neu, wenn Refresh nicht hilft.
6. Verbinde niemals eine ähnlich aussehende oder abweichende Server-Adresse.

Prüfe bei schreibenden Aktionen Claudes Werkzeugaufruf und danach die Vorschau oder den Änderungsverlauf in PaceKeeper AI.

Weitere Informationen: [Anthropic-Anleitung für Custom Connectors](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp).

[← ChatGPT verbinden](DE-ChatGPT-verbinden) · [Inhaltsverzeichnis](Deutsch) · [KI-Connectoren und Token →](DE-KI-Connectoren-und-Token)
