---
description: Erweiterung Lager für die Holzwirtschaft.
tags:
- HowTo
prev: ./forestry-base
---
# Forestry Stock
![icons_odoo_forestry_base](assets/icons_odoo_forestry_base.png)

{{ $frontmatter.description }}

Technischer Name: `forestry_stock`\
Repository: <https://github.com/Mint-System/Odoo-Apps-Vertical-Forestry/tree/15.0/forestry_stock>

## Verwendung

### Bewegungen anzeigen

Navigieren Sie nach *Lager > Produkte > Produkte* und öffnen Sie ein *Polter*.

### Lagerbuchungen validieren

Wenn Sie die Zeiterfassungseinträge validieren, wird unter folgenden Bedingungen eine Lagerbuchung erstellt:
* Der Zeiterfassungseintrag ist mit einer Aufgabe verknüpft
* Das verlinkte Produkt ist gelagert
* Die vorhandene Menge ist nicht negativ

Hier ein Bespiel des Prozesses:

![Forestry Stock](assets/Forestry%20Stock.gif)