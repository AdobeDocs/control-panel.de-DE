---
title: URL-Genehmigungen
description: Informationen zum Verwalten von URL-Berechtigungen in der Systemsteuerung
translation-type: tm+mt
source-git-commit: 8ee999b89af88a1a59956838d5722ce8fc6b3955

---


# URL-Genehmigungen {#url-permissions}

>[!CAUTION]
>
>Diese Funktion ist nur für Campaign Classic-Instanzen verfügbar.

## Über URL-Genehmigungen {#about-url-permissions}

Die Liste der URLs, die standardmäßig von JavaScript-Codes (Workflows usw.) über Ihre Campaign Classic-Instanzen aufgerufen werden können, ist begrenzt. Diese URLs ermöglichen das ordnungsgemäße Funktionieren der Instanzen.

Standardmäßig sind Instanzen nicht berechtigt, eine Verbindung zu externen URLs herzustellen. Über das Control Panel haben Sie die Möglichkeit, externe URLs zur Liste der berechtigten URLs hinzufügen, sodass sich Ihre Instanz mit ihnen verbinden kann. Dadurch können Sie zwischen Ihren Campaign-Instanzen und externen Systemen, wie z. B. SFTP-Servern oder Websites, eine Verbindung herstellen, um den Datei- und/oder Datentransfer zu ermöglichen.

Nach dem Hinzufügen einer URL wird sie in der Konfigurationsdatei der Instanz referenziert (serverConf.xml).

**Verwandte Themen:**

* [Campaign-Server konfigurieren](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html)
* [Schutz der ausgehenden Verbindung](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html#Outgoing_connection_protection)
* [Adding URL Permissions (Video-Tutorial)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/adding-url-permissions.html)

## Best Practices {#best-practices}

* Verbinden Sie Ihre Campaign-Instanz nicht mit Websites/Servern, zu denen Sie keine Verbindung benötigen.
* Löschen Sie URLs, die Sie nicht mehr benötigen. Beachten Sie jedoch, dass für andere Abteilungen Ihres Unternehmens, die die von Ihnen gelöschte URL weiterhin benötigen, keine Verbindung mehr zu dieser URL möglich ist.
* The Control Panel supports **http**, **https**, and **sftp** protocols. Die Eingabe ungültiger URLs oder Protokolle hat Fehler zur Folge.

## URL-Genehmigungen verwalten {#managing-url-permissions}

Gehen Sie wie folgt vor, um eine URL hinzuzufügen, mit der Ihre Instanz eine Verbindung herstellen kann:

1. Öffnen Sie die Karte **[!UICONTROL Instanzeinstellungen]**, um auf die Registerkarte **[!UICONTROL URL-Genehmigungen]** zuzugreifen.

   >[!NOTE]
   >
   >Wenn die Karte Instanzeneinstellungen nicht auf der Startseite des Control Panels sichtbar ist, bedeutet das, dass Ihre IMS-ORG-Kennung mit keiner Adobe Campaign Classic-Instanz verknüpft ist.
   >
   >The <b><span class="uicontrol">URL permissions</span></b> tab lists all outside URLs that your instance can connect to. Diese Liste enthält jedoch nicht die URLs, die für das Funktionieren von Campaign erforderlich sind (z. B. Verbindungen zwischen Infrastrukturelementen).

1. Wählen Sie auf der linken Seite die gewünschte Instanz aus und danach die Schaltfläche **[!UICONTROL Neue URL hinzufügen].**

   ![](assets/add_url1.png)

   >[!NOTE]
   >
   >Alle Campaign-Instanzen werden auf der linken Fensterseite aufgelistet.
   >
   >Da die Verwaltung der URL-Berechtigungen ausschließlich Kampagnen-Classic-Instanzen gewidmet ist, wird die Meldung "Nicht zutreffende Instanz"angezeigt, wenn Sie eine Campaign Standard-Instanz auswählen.

1. Geben Sie die URL ein, die genehmigt werden soll, einschließlich des mit ihr verknüpften Protokolls (http, https oder sftp).

   >[!NOTE]
   >
   >Es ist auch möglich, die Verbindung von mehreren Instanzen mit der URL zu genehmigen. Fügen Sie die Instanzen direkt im Feld Instanz(en) ein, indem Sie den ersten Buchstaben tippen.

   ![](assets/add_url2.png)

1. Die URL wurde hiermit der Liste hinzugefügt und Sie können sich jetzt damit verbinden.

   >[!NOTE]
   >
   >Nach der Validierung werden am Ende der eingegebenen URL automatisch die Zeichen "/.*" hinzugefügt, damit auch alle Unterseiten eingeschlossen sind.

   ![](assets/add_url_listnew.png)

You can delete a URL at any time by selecting it and clicking the **[!UICONTROL Delete URL]** button.

Beachten Sie, dass eine gelöschte URL von Ihrer Instanz nicht mehr aufgerufen werden kann.

## Häufige Fragen {#common-questions}

**Ich habe eine neue URL hinzugefügt, meine Instanz kann aber noch immer keine Verbindung mit ihr herstellen. Warum passiert das?**

In manchen Fällen ist es nötig, dass URLs auf die Whitelist gesetzt werden, ein Passwort eingegeben wird oder eine andere Form der Authentifizierung durchgeführt wird, um eine Verbindung mit URLs herzustellen. Das Control Panel unterstützt keine zusätzlichen Formen der Authentifizierung.
