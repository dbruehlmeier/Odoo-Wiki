---
description: Eine einfache und umfassende Odoo-Dokumentation.
tags:
- HowTo
prev: ./verkauf
---
# Verkauf Preise
![icons_odoo_sale](assets/icons_odoo_sale.png)

Produkte, Preislisten und Varianten zentral pflegen.

## Konfiguraiton

### Preislisten aktivieren

Navigieren Sie nach *Verkauf > Konfiguration > Preiskalkulation* und aktivieren Sie die Option *Preislisten*. Sie können nun mehrere Peise für ein Produkt erfassen.

### Erweiterte Preisregeln aktivieren

Navigieren Sie nach *Verkauf > Konfiguration > Preiskalkulation* und aktivieren Sie die Option *Preislisten* mit der Unteroption *Erweiterte Preisregeln*.

## Produkte

### Produkte zum Verkauf festlegen

Öffnen Sie ein Produkt via *Verkauf > Produkte > Produkte* und markieren Sie *Kann verkauft werden*. Neue Optionen erscheinen auf der Produktansicht.

![Produkte zum Verkauf deklarieren](assets/Produkte%20zum%20Verkauf%20deklarieren.gif)

### Verkaufspreis auf Produkt festlegen

Wählen Sie das Produkt unter *Verkauf > Produkte > Produkte* aus und legen Sie im Tab *Allgemeine Informationen* im Feld *Verkaufspreis* den Preis fest.  Legen Sie zusätzlich im Feld *Steuern (Verkauf)* die Mehwertsteuer fest. 

### Produktvarianten aktivieren

Navigieren Sie nach *Einstellungen > Verkauf > Produktkatalog* und aktiveren Sie die Option *Varianten*.

### Produktattributte erstellen

Öffnen Sie *Verkäufe > Konfiguration > Produkte > Attribute* und wählen Sie *Anlegen*. Geben den Attributnamen an und legen Sie den Anzeigetyp fest. Für das Feld *Variants Creation Mode* haben Sie diese Optionen:
* **Instantly**: Alle möglichen Produkvarianten werden angelegt.
* **Dynamically**: Produktvarianten werden nur angelegt, wenn diese explizit konfiguriert werden.
* **Niemals**: Mögliche Produktvarianten werden für dieses Attribut nicht angelegt.
Zuletzt tragen Sie Werte für das Attribut ein.

![](assets/Verkauf%20Stammdaten%20Produktattributte.png)

### Produktvarianten konfigurieren

Navigieren Sie nach *Verkauf > Produkte > Produkte* und wählen Sie das Produkt aus für welches Sie Produktvarianten konfigurieren möchten. Zeigen Sie den Tab *Merkmale & Varianten* an und fügen Sie ein Merkmal mit den vefügbaren Varianten hinzu. Klicken Sie anschliessend auf *Konfigurieren* und legen Sie die Preiseaufschläge oder Rabatte im Feld *Value Price Extra* fest.

### Konfigurierierte Produktvarianten anzeigen

Navigieren Sie nach *Verkauf > Produkte > Produktvarianten*. Hier finden Sie alle konfigurierten Produktvarianten.

## Preislisten

### Preisliste anzeigen

Navigieren Sie nach *Verkauf > Produkte > Preislisten* und wählen Sie eine Preisliste aus.

### Preisliste erstellen

Navigieren Sie nach *Verkauf > Produkte > Preislisten* und erstellen Sie einen neuen Eintrag. Legen Sie im Tab *Konfiguration* die Verfügbarkeit gemäss Ländergruppe fest und bestimmen Sie mit der Option *Rabattpolitik*, ob Rabatt im Produkpreis inkludiert ist oder nicht.

### Preisregel für Produktvariante erfassen

Navigieren Sie nach *Verkauf > Produkte > Preislisten* und zeigen Sie eine Preisliste an. Fügen Sie eine neue Zeile hinzu:

* **Produkt**: Wählen Sie hier die Produktvorlage aus
* **Variante**: Und hier die entsprechende Produktvariante
* **Preis**: Legen Sie den Preis der Produktvariante fest

### Preisliste mit Rabatt erstellen

Wenn Sie die [Erweiterte Preisregeln aktivieren](#Erweiterte%20Preisregeln%20aktivieren) können Sie eine Preisliste erstellen, die auf einer bestehenden Preisliste Rabatt gewährt.

Navigieren Sie nach *Verkauf > Produkte > Preislisten* und erstellen Sie einen neuen Eintrag mit dem Prozentsatz im Namen. Fügen Sie im Tab *Preisregeln* folgende Regeln hinzu:

* **Anzuwenden auf**: Alle Produkte
* **Startdatum**: Gemäss Laufzeit
* **Enddatum**: Gemäss Laufzeit
* **Ermittle Preis**: Formel
* **Basiert auf**: Andere Preisliste
* **Stardatum**: Preisliste auswählen
* **Rabatt**: Rabatt in Prozent

Dazu ein Beispiel:

![](assets/Verkauf%20Preisregel%20Rabat.png)

Beim Auswahl der Preisliste im Angebot wird anschliessend der Preis mit Rabatt berechnet und eingetragen.

### Preisliste mit Rabatt für eine bestimmte Periode einrichten

Wenn Sie die [Erweiterte Preisregeln aktivieren](#Erweiterte%20Preisregeln%20aktivieren) können Sie eine Preisliste erstellen, die auf einer bestehenden Preisliste Rabatt gewährt.

Wenn Sie auf eine bestehenden Preisliste in einem bestimmten Zeitraum Rabatt gewähren möchten, müssen Sie eine neue Preisliste mit zwei Preisregeln einrichten. Navigieren Sie nach *Verkauf > Produkte > Preislisten* und erstellen Sie einen neuen Eintrag mit dem Prozentsatz im Namen. Erstellen Sie eine für den Rabatt:

* **Anzuwenden auf**: Alle Produkte
* **Enddatum**: Ende der Kampange
* **Ermittle Preis**: Formel
* **Basiert auf**: Andere Preisliste
* **Andere Preisliste**: Preisliste auswählen
* **Rabatt**: Rabatt in Prozent

Erstellen Sie eine zweite Preisregel für den normalen Preis:

* **Anzuwenden auf**: Alle Produkte
* **Startdatum**: Ende der Kampange
* **Ermittle Preis**: Formel
* **Basiert auf**: Andere Preisliste
* **Andere Preisliste**: Preisliste auswählen

Dazu ein Beispiel:

![](assets/Verkauf%20Stammdaten%20Preisliste%20mit%20Rabatt.png)

### Preisliste mit Staffelpreisen

Um für ein Produkt in Abhängigkeit zu unterschiedlichen Mengen eine Preisstaffelung einzurichten, muss die entsprechende Option *Preislisten / Mehrere Preise pro Produkt* unter *Einstellungen > Verkauf  > Preiskalkulation* eingeschaltet werden.

![](assets/Verkauf%20Stammdaten%20Staffelpreise.png)

Ein Beispiel könnte so aussehen:

![](assets/Verkauf%20Stammdaten%20Staffelpreise%20Beispiel.png)

In einem *Angebot / Verkaufsauftrag* werden die Preise entsprechend unterschiedlich angezeigt. Dazu das folgende Beispiel:

![](assets/Verkauf%20Stammdaten%20Staffelpreise%20Verkaufsauftrag%20Beispiel.png)

### Preisregeln anzeigen

Damit Sie eine Übersicht der Preisregeln erhalten, folgen Sie dem HowTo [Menüeintrag erstellen](Entwicklung.md#Menüeintrag%20erstellen) und verwenden diese Werte:

Menü: `Preisregeln`\
Obermenü: `Verkauf/Produkte`\
Aktion: `ir.actions.act_window` `Preisregeln`\
Nummernfolge: `5`


