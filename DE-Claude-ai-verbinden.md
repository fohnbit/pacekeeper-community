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

Die aktuell auf dem PaceKeeper-Server laufende MCP-Version wird oben im Web-Wiki angezeigt. Um zu prüfen, welchen Server dein aktueller Chat tatsächlich erreicht, sende in Claude:

Aktueller Wert im Web-Wiki: `{{MCP_SERVER_BUILD_UTC}}`

> Ruf `pacekeeper_get_context` ab und zeig mir `server_build_utc`.

Vergleiche den zurückgegebenen Wert mit dem Zeitstempel der oben angezeigten MCP-Version. Stimmen beide überein, erreicht der Werkzeugaufruf den aktuellen PaceKeeper-Server. Fehlt `server_build_utc` oder weicht der Wert ab, erneuere die Verbindung wie im nächsten Abschnitt beschrieben und öffne danach einen neuen Chat.

Ein übereinstimmender Wert bestätigt den aktuellen Backend-Stand. Wenn trotzdem neue Werkzeuge fehlen, kann Claude noch eine ältere Werkzeugliste gespeichert haben; entferne den Connector dann wie unten beschrieben, füge ihn erneut hinzu und verwende einen neuen Chat.

## Verbindung nach einem Update erneuern

Eine erneute Verbindung ist sinnvoll oder erforderlich, wenn:

- PaceKeeper AI ausdrücklich zum erneuten Verbinden auffordert,
- Claude einen Authentifizierungs- oder Berechtigungsfehler meldet,
- neue PaceKeeper-Werkzeuge nach einem Update fehlen,
- der Connector mit einer alten oder falschen Server-Adresse angelegt wurde,
- Anthropic oder PaceKeeper die Connector-Metadaten geändert hat.

Anthropic bietet für Custom Connectors derzeit keine allgemeine Bearbeitung vorhandener Connector-Einstellungen an. Zum Aktualisieren wird der Connector entfernt und neu hinzugefügt:

1. Öffne in Claude **Anpassen/Customize → Connectors**.
2. Öffne bei **PaceKeeper AI** das Drei-Punkte-Menü und wähle **Remove/Entfernen**.
3. Bei Team oder Enterprise entfernt beziehungsweise aktualisiert der Owner zuerst den Organisations-Connector, wenn dessen Server-Konfiguration betroffen ist.
4. Füge PaceKeeper AI erneut mit `https://www.pacekeeper.icu/mcp` hinzu.
5. Öffne PaceKeeper AI unter **Einstellungen → KI-Assistent verbinden** und erzeuge einen neuen sechsstelligen Code.
6. Schließe die neue Autorisierung mit diesem Code ab.
7. Aktiviere den Connector in einem neuen Claude-Chat und teste zunächst eine lesende Anfrage.

Ein alter Code oder eine alte Autorisierung soll nicht wiederverwendet werden. Ist nur die persönliche Anmeldung abgelaufen, kann je nach Claude-Oberfläche bereits **Connect** genügen; sobald Werkzeuge oder Connector-Metadaten veraltet sind, ist Entfernen und erneutes Hinzufügen der sichere Weg.

## Verbindung testen und Fehler beheben

1. Öffne einen neuen Chat und aktiviere PaceKeeper AI unter **+ → Connectors**.
2. Frage beispielsweise: „Was ist mein nächstes Training?“
3. Prüfe bei „Connector nicht verfügbar“, ob er für diesen Chat aktiviert ist.
4. Prüfe bei Autorisierungsfehlern, ob der Einmalcode noch gültig ist; erzeuge andernfalls einen neuen.
5. Entferne den Connector und füge ihn erneut hinzu, wenn Claude weiterhin alte oder fehlende Werkzeuge anzeigt.
6. Verbinde niemals eine ähnlich aussehende oder abweichende Server-Adresse.

Prüfe bei schreibenden Aktionen Claudes Werkzeugaufruf und danach die Vorschau oder den Änderungsverlauf in PaceKeeper AI.

Weitere Informationen: [Anthropic-Anleitung für Custom Connectors](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp).

[← ChatGPT verbinden](DE-ChatGPT-verbinden) · [Inhaltsverzeichnis](Deutsch) · [KI-Connectoren und Token →](DE-KI-Connectoren-und-Token)
