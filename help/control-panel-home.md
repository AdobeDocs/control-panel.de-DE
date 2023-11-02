---
title: Produktdokumentation
description: Dokumentation für Control Panel.
feature: Control Panel
role: Admin
level: Experienced
exl-id: 2b2cfaed-e42e-4c3a-a8d8-224b936890ab
source-git-commit: e8bffd8e7f571fd85c725adf837c2997f7615fcd
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---

# Hilfe {#control-panel-documentation}

>[!CONTEXTUALHELP]
>id="cp_overview"
>title="Über das Control Panel"
>abstract="Auf der Startseite des Control Panels haben Sie Zugriff auf alle Aktionen, die auf Ihren Campaign-Instanzen ausgeführt werden können."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/accessing-control-panel.html?lang=de" text="Zugriff auf das Control Panel"

Das Control Panel von Campaign hilft Produktadministratoren von Campaign Standard und v7/v8, effizienter zu arbeiten, indem sie Einstellungen verwalten und die Nutzung der Instanzen überwachen können.

## Neue Funktionen

**Benutzeroberfläche**

* Control Panel ist jetzt in weiteren Sprachen verfügbar. [Weitere Informationen](discover/using/discovering-the-interface.md#supported-languages-languages)

**Überwachung aktiver Profile**

* Sie können jetzt die Anzahl der aktiven Profile überwachen, die Ihnen für Ihre Organisation zustehen, sowie die Gesamtzahl der in Ihrer Organisation verwendeten Profile in allen Instanzen, wenn Sie mehrere Instanzen verwenden. [Weitere Informationen](performance-monitoring/using/active-profiles-monitoring.md)

**DMARC-Einträge**

* Mehrere E-Mail-Adressen können jetzt E-Mails zu aggregierten Berichten und Fehlerberichten erhalten. [Weitere Informationen](subdomains-certificates/using/dmarc.md)
* Es wurden Änderungen für den Fall vorgenommen, dass sowohl DMARC- als auch BIMI-Einträge für eine Subdomain vorhanden sind:

   * DMARC-Einträge können nicht gelöscht werden. Wenn Sie einen Eintrag löschen möchten, müssen Sie zuerst den BIMI-Eintrag löschen.
   * DMARC-Einträge können bearbeitet werden, aber das Herunterstufen der Richtlinie auf „Keine“ ist nicht zulässig und der Prozentwert muss 100 betragen.

>[!CAUTION]
>
>* Das Control Panel steht nur Administratoren zur Verfügung. [Weitere Informationen](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=de#discover-control-panel)   
>
>* Für Campaign v7 gelten Bereitstellungsbeschränkungen. [Weitere Informationen](faq.md#v7-restrictions)

## Zusätzliche Ressourcen {#additional-resources}

<table>
    <tr>
        <td><b>Campaign Standard</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/control-panel-overview.html?lang=de">Tutorial-Videos zum Control Panel</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-standard/using/campaign-standard-home.html?lang=de">Produktdokumentation zu Campaign Standard</a></li>
        </ul>
        </td>
        <td><b>Campaign v7</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/control-panel-overview.html?lang=de">Tutorial-Videos zum Control Panel</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-classic/using/campaign-classic-home.html?lang=de">Produktdokumentation zu Campaign v7</a></li>
        </ul>
        </td>
        <td><b>Campaign v8</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-learn/control-panel/control-panel-overview.html?lang=de">Tutorial-Videos zum Control Panel</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign/campaign-v8/campaign-home.html?lang=de">Produktdokumentation zu Campaign v8</a></li>
        </ul>
        </td>
    </tr>
</table>
