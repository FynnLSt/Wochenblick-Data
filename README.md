# Wochenblick-Data

Öffentliches Repository für Angebotsdaten und Prüfanfragen. Keine persönlichen Daten, Einkaufslisten, Tokens oder PDFs speichern.

- `status/<slug>.json`: letzte lokale Abrufdiagnose pro Händler.
- `offers/<slug>.json`: nach Originalquelle geprüfte Ergänzungen für einen konkreten Zeitraum.
- `requests/<uuid>.json`: Prüfanfrage ausschließlich im zugehörigen Pull Request. Titel beginnt mit `Wochenblick-Prüfung:`.
- `results/<uuid>.json`: Ergebnis auf main mit schemaVersion:1, id (Anfrage-ID), store (exakte Händlerbezeichnung), status (completed oder failed), start, end (identisch mit Anfrage), checkedAt (ISO-Zeit), message, offers (Array) und removeIds (Array mit ausdrücklich als falsch bestätigten IDs).
- Händler-Slugs: netto, aldi-sued, lidl, edeka, rewe, kaufland.

Nur nach Originalprospekt verifizierte Korrekturen veröffentlichen. Unbekannte Werte bleiben null. `removeIds` dient nur zum Entfernen bestätigter fehlerhafter Positionen. Bei nicht erfolgreicher Prüfung status `failed`, offers und removeIds leer. Keine pauschale Löschung. Korrekturen haben für ihren Gültigkeitszeitraum Vorrang. Anfragen aus unbekannten Forks oder anderer Autorenschaft werden nicht bearbeitet.
