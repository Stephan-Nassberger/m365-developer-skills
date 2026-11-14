# Plugin 0.2.0: Microsoft Learn

Das bestehende private Plugin wird um den offiziellen Microsoft-Learn-MCP-Dienst und einen eigenen Dokumentations-Skill ergänzt. Die 16 bisherigen Skills bleiben erhalten; insgesamt 17. Name, private Sichtbarkeit und Benutzerzuordnung bleiben gleich.

- Endpunkt: https://learn.microsoft.com/api/mcp
- Transport: Streamable HTTP
- Anmeldung: keine
- Fähigkeiten laut Microsoft: Dokumentationssuche, Artikelabruf, Codebeispielsuche. Tools und Schemas beim Verbindungsaufbau dynamisch ermitteln.
- Keine M365-Tenant-Berechtigungen, kein Graph-/SharePoint-Schreibzugriff.

Konfiguration: `mcp.json` in diesem Ordner; beim Paketbau liegt sie am Plugin-Wurzelverzeichnis. Nicht als gewöhnliche Webadresse im Browser testen.

```text
python scripts/validate_collection.py
python scripts/build_plugin.py --output ../m365-developer-skills-plugin.zip
```

Der Paketbau erhält Referenzen, Lizenzen und Herkunftsnachweise. Die Originale liegen weiterhin im Ordner `M365 Developer Skills`. Der Agent-Plugins-Importer kann zusätzliche Kompatibilitätsdateien erzeugen.

Ein gespeichertes Update ist noch kein Nachweis, dass der Host den neuen MCP-Dienst verbunden hat. Verbindungs- und Funktionstests getrennt dokumentieren; bei Bedarf Plugin im Host aktualisieren und einen neuen Chat öffnen. Zugang zu weiteren Power-Platform-/M365-Tools bleibt separat.
