---
description: Eine einfache und umfassende Odoo-Dokumentation.
tags:
- HowTo
prev: ./kalender
---
# Kalender Aktionen
![icons_odoo_calendar](assets/icons_odoo_calendar.png)

Kalender-Prozesse automatisieren.

## Aktionen

### Outlook Kalender synchronisieren

Navigieren Sie nach *Einstellungen > Technisch > Server Aktionen* und erstellen Sie einen neuen Eintrag:

Name der Aktion: `Outlook Kalender synchronisieren`\
Modell: `res.users`\
Folgeaktion: `Python-Code ausführen`

Kopieren Sie die folgenden Zeilen in das Feld *Pythoncode*:

```python
for rec in records:
	rec._sync_microsoft_calendar()
```

Die Aktion mit dem Knopf *Kontextuelle Aktion erstellen* bestätigen und dann speichern.

In der Formularansicht der Benutzer wählen Sie *Aktion > Outlook Kalender synchronisieren*.