---
description: Eine einfache und umfassende Odoo-Dokumentation.
tags:
- HowTo
- Drittanbieter
prev: ./einkauf
---
# Purchase Stock Sale Owner
![icon_oms_box](assets/icon_oms_box.png)

Eigentümer auf Wareneingang aus Verkaufsauftrag zuordnen.

Technischer Name: `purchase_stock_sale_owner`\
Repository: <https://github.com/Mint-System/Odoo-Apps-Purchase-Workflow/tree/15.0/purchase_stock_sale_owner>

## Verwendung

### Eigentümer beim Wareneingang zuordnen

Mit dieser Erweiterung wird bei der Generierung des Wareneingangs aus einer Bestellung geprüft, ob es sich um eine Purchase To Order Bestellung handelt. Wenn die Bestellung mit einem Verkaufsauftrag verknüpft ist, wird der Kontakt aus Lieferadresse als Eigentümer auf dem Wareneingang eingetragen.