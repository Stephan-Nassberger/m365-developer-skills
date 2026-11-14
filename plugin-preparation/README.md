# Vorbereitung des späteren ChatGPT-Plugins

Vorbereitet ist ein **Skills-only Plugin**, nicht bereits ein verbundenes M365-Werkzeug. Das Entwurfsmanifest verwendet Agent Plugins 1.0. Noch kein Plugin im Konto angelegt, installiert oder öffentlich eingereicht.

## Reproduzierbarer Paketbau

Mit Python 3 und PyYAML (nur für die Validierung):

```text
python scripts/validate_collection.py
python scripts/build_plugin.py --output ../m365-developer-skills-plugin.zip
```

Der Paketbau erzeugt `m365-developer-skills/plugin.json`, `skills/<name>/SKILL.md`, `common/`, Attribution, Lizenztexte und Quellen-Lock. Er ändert die kuratierten Skill-Dateien nicht. Er übernimmt unterstützende Referenzen, Regeln und Templates, lässt aber fremde verschachtelte Plugin-Manifeste und Eval-Pakete aus. Original-Hashes im Lock beziehen sich auf die Sammlung; `package-files.json` weist die tatsächlich gepackten Dateien aus.

## Vor der Installation zu prüfen

- Mit dem tatsächlichen ChatGPT-/Codex-Importer validieren: unbekannte Upstream-Frontmatterfelder können hostabhängig sein. Keine bestätigte Import-Kompatibilität behaupten.
- Reale Aufgaben pro Skill testen: insbesondere Schema/Host für JSON und Cards, Cmdlet/CLI-Versionen, SPFx-Build, Graph-Rechte und Power-BI-MCP/TMDL-Pfade. Keine bloßen Text-Matching-Evals als Qualitätsnachweis.
- Routing-Konflikte prüfen: PnPjs-/v9-Defaults von SPFx, breite Teams-Trigger und optionale MartiX-Geschwisterskills. Bestehende Projekte nicht auf diese Defaults migrieren.
- Nur tatsächlich benötigte MCP-Verbindungen ergänzen. Für Power Apps/Automate die offiziellen Microsoft-Plugins mit ihren vollständigen Laufzeitabhängigkeiten gesondert evaluieren.

## Spätere Werkzeugebene

Ein Skill ist Wissen/Arbeitsanweisung. Für Zugriff braucht es separat echte Tools, z. B. lokale PnP-/M365-/PAC-/Azure-CLIs oder unterstützte MCP-Dienste. Berechtigungen und Authentifizierung am jeweiligen Dienst prüfen. Keine erfundenen Endpoints oder vorab leeren Zugangsdaten in `mcp.json`; deshalb existiert noch keine solche Datei.

Lesen, Quellcodeerstellung, Tenant-Änderungen und Deployment sind unterschiedliche Fähigkeiten. Für ein späteres Tool-Plugin zunächst Identität, Zieltenant/-umgebung, zulässige Operationen und Credential-Verwaltung festlegen, danach read-only integrieren und gezielt Schreiboperationen ergänzen. Keine automatische Vergabe von Adminrechten. Das Paket enthält keine Zugangsdaten, Kundendaten oder internen novato-Quellen.

Die portable Ordnerstruktur folgt den im Arbeitsumfeld verfügbaren Plugin-Paketanweisungen. Eine Installation oder öffentliche Freigabe ist noch nicht Teil dieser Vorbereitung.

