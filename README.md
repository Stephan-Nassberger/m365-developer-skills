# M365 Developer Skills

Kuratierte Sammlung für Microsoft 365 und SharePoint. Stand: **14.11.2026**. **16 Skills: 6 übernommene Pakete, 10 eigene Ergänzungen.** Kein Microsoft-zertifiziertes Produkt; kein Zugriff auf einen Tenant und keine automatische Bereitstellung.

## Schnellzugriff

- [Alle Skills und Herkunft](CATALOG.md)
- [Recherche, Lizenz- und Qualitätsprüfung](RESEARCH.md)
- [Attribution und Lizenzgrenzen](THIRD_PARTY_NOTICES.md)
- [Commit- und Datei-Nachweise](sources.lock.json)
- [Plugin-Vorbereitung](plugin-preparation/README.md)
- [Ausgeführte Prüfungen und Grenzen](VALIDATION.md)

## Abdeckung

| Thema | Skill |
|---|---|
| PnP PowerShell, Provisionierung, CLI, PnPjs | `martix-sharepoint-pnp` |
| PnP Modern Search v4 | `pnp-modern-search` |
| JSON Column Formatting | `sharepoint-json-column-formatting` |
| JSON View Formatting | `sharepoint-json-view-formatting` |
| SPFx Webparts, Upgrade, React, PnPjs | `spfx` |
| Application Customizer, Field/Command/Form Customizer, HTML | `sharepoint-html-spfx-extensions` + `spfx` |
| Teams Apps, Bots, SSO, Migration | `teams-dev` |
| Adaptive Cards, hostbezogene Aktionen | `adaptive-cards-m365` |
| Power Automate | `power-automate-development` |
| Power Apps und SharePoint-Formulare | `power-apps-development` |
| Power BI/Fabric Semantic Models | `semantic-model-authoring` |
| Microsoft Graph SDK | `msgraph-sdk` |
| Azure Functions für M365 | `azure-functions-m365` |
| Fluent UI | `martix-fluent-ui` |
| Microsoft Forms | `microsoft-forms-integration` |
| Planner | `planner-development` |

Power BI-Berichtsdesign ist noch kein eigenes installiertes Skill-Paket; zusätzliche echte Kandidaten sind in RESEARCH.md verlinkt. Anleitungen ersetzen keine CLI, MCP-Verbindung, Anmeldung, Lizenz oder Berechtigung. Bestehende Architektur und explizite Nutzeranweisungen gehen den Meinungen einzelner Upstream-Skills vor.

## Warum kuratieren statt alles forken?

Die Quellen sind verschieden geschnitten: einzelne Skills, große Plugin-Marktplätze, Produktquellcode oder reine Beispielsammlungen. Ein Sammel-Fork würde diese Unterschiede und Abhängigkeiten nicht lösen. Deshalb gezielte, versionierte Übernahmen samt unterstützenden Dateien und Lizenztexten; keine Forks angelegt. Für spätere Beiträge am Upstream wäre ein gezielter Fork sinnvoll.

## Verwendung

Der gewünschte Ordner `M365 Developer Skills` ist die nachvollziehbare Quelle. Er ist wegen des zusätzlichen Ordnerlevels **kein direkt importierbares ChatGPT-Plugin**. Die Plugin-Vorbereitung erzeugt daraus die portable Struktur `skills/<name>/SKILL.md` und erhält gemeinsame Referenzen und Lizenzen. Noch kein Plugin im Konto angelegt oder installiert.

## Pflege

Neue Quellen erst nach Prüfung von echtem SKILL.md, passendem Anwendungsbereich, Lizenztext, relativen Abhängigkeiten und Tool-Voraussetzungen aufnehmen. Updates gezielt über Branch/PR mit neuem Upstream-Commit, Hashes und Änderungsprüfung; keine automatischen Updates auf ungeprüftes `main`. Ursprungsdateien nicht als eigene Arbeit ausgeben. Keine Tenant-Daten oder Zugangsdaten veröffentlichen.

Originale Inhalte stehen unter MIT; übernommene Pakete behalten ihre jeweiligen MIT-/Apache-2.0-Bedingungen. Siehe THIRD_PARTY_NOTICES.md.
