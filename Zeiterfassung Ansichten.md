---
description: Eine einfache und umfassende Odoo-Dokumentation.
tags:
- HowTo
prev: ./
---
# Zeiterfassung Ansichten
![icons_odoo_hr_timesheet](assets/icons_odoo_hr_timesheet.png)

Ansichten der Zeiterfassung anpassen.

## Ansichten

### Validierung nach Projekt konfigurieren

Sie möchten die Standardansicht für die Validierung der Zeiterfassungeinträge gemäss folgenden Punkten anpassen:
* Listenansicht als Standardansicht
* Filter *Mein Team* ausschalten

Rufen Sie die Ansicht *Zeiterfassung > Zu validieren > Letzte Woche* auf und führen Sie [Aktuelle Aktion bearbeiten](Entwicklung%20Aktionen.md#Aktuelle%20Aktion%20bearbeiten) aus. Erstellen Sie im Abschnitt *Ansichten* einen  Eintrag vom Typ *Baum*.

Als nächstes entfernen Sie den Filter *Mein Team* und fügen den Filter *Gruppieren nach > Projekt* hinzu, speichern Sie die Filter als neuen Favoriten *Gruppiert nach Projekt* mit der Option Standardfilter. Anschliessend führen Sie [Benutzerdefinierter Filter für alle Benutzer freigeben](Entwicklung%20Ansichten.md#Benutzerdefinierter%20Filter%20für%20alle%20Benutzer%20freigeben) aus.