---
title: Produktdokumentation
description: Dokumentation für Control Panel.
feature: Control Panel
role: Architect
level: Beginner
exl-id: 2b2cfaed-e42e-4c3a-a8d8-224b936890ab
source-git-commit: 6a4db9712d3a92d8057758eb134b0178213f5ff8
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 62%

---

# Hilfe {#control-panel-documentation}

>[!CONTEXTUALHELP]
>id="cp_overview"
>title="Über das Control Panel"
>abstract="Auf der Startseite des Control Panels haben Sie Zugriff auf alle Aktionen, die auf Ihren Campaign-Instanzen ausgeführt werden können."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/accessing-control-panel.html?lang=de" text="Zugriff auf das Control Panel"

![](assets/do-not-localize/banner.png)

Das Control Panel von Campaign hilft Produktadministratoren von Campaign Standard und v7/v8, effizienter zu arbeiten, indem sie Einstellungen verwalten und die Nutzung der Instanzen überwachen können.

## Neue Funktionen

**Benutzeroberfläche**

* Das Control Panel ist jetzt in zusätzlichen Sprachen verfügbar. [Weitere Informationen](discover/using/discovering-the-interface.md#supported-languages-languages)

**Überwachen aktiver Profile**

* Sie können jetzt die Anzahl der aktiven Profile überwachen, die Sie für Ihr Unternehmen berechtigt sind, sowie die Gesamtzahl der in Ihrem Unternehmen verwendeten Profile in allen Instanzen, wenn Sie mehrere Instanzen verwenden. [Weitere Informationen](performance-monitoring/using/active-profiles-monitoring.md)

**DMARC-Einträge**

* Mehrere E-Mail-Adressen können jetzt E-Mails zu aggregierten Berichten und Fehlerberichten erhalten. [Weitere Informationen](subdomains-certificates/using/dmarc.md)
* Änderungen wurden vorgenommen, wenn sowohl DMARC- als auch BIMI-Datensätze für eine Subdomain vorhanden sind:

   * DMARC-Datensätze können nicht gelöscht werden. Wenn Sie einen Eintrag löschen möchten, müssen Sie zuerst den BIMI-Datensatz löschen.
   * DMARC-Einträge können bearbeitet werden, aber das Downgrade der Richtlinie auf &quot;Keine&quot;ist nicht zulässig und der Prozentwert muss 100 betragen.

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
