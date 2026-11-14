# Ausgeführte Validierung

Stand 14.11.2026.

- Sammlung: 16 eindeutige Skill-Namen und gültige YAML-Einstiegsmetadaten; alle 138 im Quellen-Lock erfassten Dateien stimmen mit ihren SHA-256-Werten überein.
- Alle lokalen Markdown-Dateiverweise in den Skill-Paketen und gemeinsamen Referenzen aufgelöst. URL-Erreichbarkeit und inhaltliche Richtigkeit sämtlicher externer Links sind damit nicht bewiesen.
- Zehn eigene Skills einzeln mit dem installierten skill-creator/quick_validate.py geprüft: 10 bestanden. Upstream-Skills unverändert behalten ihre zusätzlichen Frontmatterfelder; keine vollständige hostübergreifende Validator-Kompatibilität behauptet.
- Alle JSON-Dateien der Sammlung geparst; Manifest-Schema-ID und Untertitellänge geprüft. Das ist keine vollständige Validierung gegen das entfernte Plugin-Schema und kein Importtest.
- Plugin-Archiv erzeugt und wieder geöffnet: 16 SKILL.md-Einstiege auf portabler Ebene, 135 Dateien, ZIP-Integrität und lokale Dateiverweise geprüft.
- Bei der ersten Archivprüfung fehlte eine von MartiX referenzierte metadata.json. Der Paketfilter wurde korrigiert; erneuter Paketbau und Verweisprüfung bestanden. Die Prüfung ist jetzt Bestandteil von build_plugin.py.

## Noch ausstehend

ChatGPT-/Codex-Import, Skill-Routing-Evaluation, M365-/SharePoint-Tenant-Tests, SPFx-Build eines Zielprojekts, CLI-/MCP-Laufzeitprüfungen, Power-BI-Modelltests und produktive Deploymentprüfungen wurden nicht ausgeführt. Vorhandene Upstream-evals wurden nicht ausgeführt. Keine Aussage über funktionierende Tenant-Verbindungen, Berechtigungen, Premium-Lizenzen oder produktive Eignung.

## Wiederholen

```text
python scripts/validate_collection.py
python scripts/build_plugin.py --output ../m365-developer-skills-plugin.zip
```

Die Sammlung wurde statisch untersucht; die mitgelieferten Fremdskripte und Templates wurden nicht ausgeführt. Keine Geheimnisse oder Tenant-Inhalte wurden absichtlich aufgenommen.
