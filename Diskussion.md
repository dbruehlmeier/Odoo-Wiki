---
description: In alle Module integrierter privater Chat und Gruppen-Chat.
tags:
- HowTo
prev: ./
---
# Diskussion
![icons_odoo_mail](assets/icons_odoo_mail.png)

{{ $frontmatter.description }}

Website: <https://www.odoo.com/de_DE/app/discuss>

## Bereiche

| Bereich                                               | Beschreibung                         |
| ----------------------------------------------------- | ------------------------------------ |
| [Diskussion Aktivitäten](Diskussion%20Aktivitäten.md) | Arbeitsplanung mit Odoo Aktivitäten. |
| [Diskussion E-Mail](Diskussion%20E-Mail.md)           | E-Mail mit Odoo versenden.           |

## Erweiterungen

| Erweiterung                                                                         | Beschreibung                                                           |
| ----------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| [Account Move Mail Thread](Account%20Move%20Mail%20Thread.md)                       | Verhindert das versenden von Nachrichten beim Erstellen einer Buchung. |
| [Account Move Send Unsubscribe](Account%20Move%20Send%20Unsubscribe.md)             | Alle Abonnenten nach Versenden der Rechnung entfernen.                 |
| [Account Move Unsubscribe](Account%20Move%20Unsubscribe.md)                         | Alle Abonnenten nach Buchung eines Buchungssatzes entfernen.           |
| [Mail Composer Default Template](Mail%20Composer%20Default%20Template.md)           | Standardvorlage für Mail-Dialog festlegen.                             |
| [Mail No Autofollow](Mail%20No%20Autofollow.md)                                     | Beim Erstellen von Nachrichten erfolgt keine automatische Abonnierung. |
| [Mail Optional Follower Notification](Mail%20Optional%20Follower%20Notification.md) | Auswahl Nachrichen an Abonnenten verschicken.                          |
| [Mail Thread Context](Mail%20Thread%20Context.md)                                   | Automatisches Abonnieren deaktiveren.                                  |
| [Mail Unsubscribe](Mail%20Unsubscribe.md)                                           | Automatische Abmeldung der Follower vor dem Versand einer Nachricht.   |
| [Purchase Order Send Unsubscribe](Purchase%20Order%20Send%20Unsubscribe.md)         | Alle Abonnenten nach Versenden der Bestellung entfernen.               |
| [Purchase Order Unsubscribe](Purchase%20Order%20Unsubscribe.md)                     | Alle Abonnenten nach Bestätigung der Bestellung entfernen.             |
| [Sale Order Send Unsubscribe](Sale%20Order%20Send%20Unsubscribe.md)                 | Alle Abonnenten nach Versenden des Angebots entfernen.                 |
| [Sale Order Unsubscribe](Sale%20Order%20Unsubscribe.md)                             | Alle Abonnenten nach Bestätigung des Angebots entfernen.               |
| [URL Attachment](URL%20Attachment.md)                                               | Url als Dokument anhängen.                                             |

## Auswertung

### Versendete Nachrichten betrachten

Nachrichten, die von Odoo versendet werden, werden zentral gespeichert. Im Entwicklermodus sehen Sie diese unter *Einstellungen > Technisch > E-Mail > Nachrichten*. Hier sehen Sie alle versendeten Nachrichten aufgelistet. In der Detailansicht sieht man den *Nachrichtentext* und die Metadaten.

![](assets/Diskussion%20Detailansicht.png)

Jede versendete Nachricht erhält eine eindeutige *Nachrichten-ID*.

![](assets/Diskussion%20Nachrichten-ID.png)

Wurde die Nachricht als Mail versendet, können Sie im Tab *Empfänger* die Kontakte sehen.

![](assets/Diskussion%20Empfänger.png)

### Nachrichten abrufen

Führen Sie folgendes aus  *Einstellungen > Diskussion > Externe E-Mail-Server > Eintrag auswählen*. Führen Sie die Aktion *Nachrichten abrufen* aus. Im Feld *Letztes Abholdatum* sehen ob die E-Mails abgerufen werden konnten.

## Abonnieren

### Eigenes Abonnement hinzufügen

Wenn Sie einen Chatter zum Odoo-Geschäftsobjekt sehen, können Sie mit einem Klick auf *Abonnieren*, das eigene Abonnement hinzufügen.

### Abonnement hinzufügen

Fügen Sie einen Abonnent dem Odoo-Objekt hinzu indem Sie rechts von *Abonnieren* auf das Icon klicken und *Followers hinzufügen* wählen.

![Diskussion Abonnent hinzufügen](assets/Diskussion%20Abonnent%20hinzufügen.gif)

### Abonnement bearbeiten

Wählen Sie ein Abonnement auf dem Odoo-Gschäftsobjekts aus, indem Sie rechts von *Abonnieren* auf das Icon klicken und ein Abonnement auswählen.

### Abonnement entfernen

Entfernen Sie einen Abonnent vom Odoo-Objekt indem Sie rechts von *Abonnieren* auf das Icon klicken.

![Diskussion Abonnent entfernen](assets/Diskussion%20Abonnent%20entfernen.gif)

## Benachrichtigungen

### Benachrichtigungen anzeigen

Wenn Odoo Nachrichten versendet, werden abonnierte Benutzer benachrichtigt. Diese Benachrichtigungen können via *Einstellungen > Technisch > Benachrichtigungen* angezeigt werden.

### Subtypen verwalten

Navigieren Sie nach *Einstellungen > Technisch > Subtypen* und zeigen Sie beispielsweise den Subtyp *Bestätigt* an.

![](assets/Diskussion%20Subtyp%20Bestätigt.png)

Konfigurieren Sie den Subtypen gemäss Anforderungen:

* **Standard**: Wird beim Abonnieren automatisch ausgewählt.
* **Nur interne**: Nur für interne Benutzer sichtbar.
* **Versteckt**: Subtyp wird auf Abonnement-Formular ausgeblendet.

### Subtyp auf Abonnement aktivieren

Zeigen Sie ein Odoo Dokument an und beareiten Sie ein Abonnement.

![](assets/Diskussion%20Abonnement%20bearbeiten.png)

Wählen Sie die Subtypen aus, welche für das Abonnement aktiv sein sollen.

## Kanäle

### Kanal löschen

Um einen Kanal zu löschen navigieren Sie nach *Einstellungen > Technisch > Kanäle*, wechseln in die Listenansicht und wählen die Kanäle die gelöscht werden sollen. Klicken Sie auf *Aktion > Löschen*.

::: warning
Alle mit dem Kanal verknüpften Nachrichten werden mit dieser Aktion gelöscht.
:::