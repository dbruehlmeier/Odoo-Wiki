---
description: Aktivieren Trigram-Index auf Datenbank-Felder.
tags:
- HowTo
- OCA
prev: ./datenbank
---
# Base Search Fuzzy
![icon_oca_app](assets/icon_oca_app.png)

{{ $frontmatter.description }}

Technischer Name: `base_search_fuzzy`\
Repository: <https://github.com/OCA/server-tools/tree/16.0/auditlog>

## Verwendung

Mit der Trigramm-Indexierung können Sie sog. *Fuzzy Search* ausführen. 

### Trigram-Indexierung für ausgewähltes Feld aktivieren

Navigieren Sie nach *Einstellungen > Technisch > Datenbankstruktur > Trigram Index* und erstellen Sie einen neuen Eintrag:

* **Feld**: Wählen Sie das Feld aus für welches ein Trigram-Index erstellt werden soll.
* **Index Name**: Vergeben Sie optional einen Indexnamen.
* **Index Typ**: Wählen Sie den Index-Typ aus.

::: tip
Damit eine *Fuzzy Search* funktioniert muss auf der Suchmaske der Suchfilter  angepasst werden. Statt den Operator `ilike`, gibt es neu den Operator `%`. Mit einer *Fuzzy Search* werden Suchergebnisse zuverlässiger gefliefert. Hier ein Beispiel mit einem Rechtschreibefehler:

![](assets/Base%20Search%20Fuzzy.png)
:::