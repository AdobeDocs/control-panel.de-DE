---
title: URL-Genehmigungen
description: Erfahren Sie, wie Sie URL-Genehmigungen im Control Panel verwalten.
translation-type: ht
source-git-commit: a2c19296894ff893987290cb287dc7002ab999e5

---


# URL-Genehmigungen {#url-permissions}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_urlpermissions"
>title="[!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_urlpermissions&quot;
>title=&quot;Über URL-Genehmigungen&quot;
>abstract=&quot;Verwalten Sie die URLs, mit denen Ihre Adobe Campaign-Instanzen eine Verbindung herstellen können.&quot;
>additional-url=&quot;https://images-tv.adobe.com/mpcv3/91206a19-d9af-4b6a-8197-0d2810a78941_1563488165.1920x1080at3000_h264.mp4&quot; text=&quot;Demovideo ansehen&quot;"
>abstract="[!IMPORTANT]"
>additional-url="Diese Funktion ist nur für Campaign Classic-Instanzen verfügbar." text="Über URL-Genehmigungen {#about-url-permissions}"

>[!IMPORTANT]Die Liste der URLs, die standardmäßig von JavaScript-Codes (Workflows usw.) über Ihre Campaign Classic-Instanzen aufgerufen werden können, ist begrenzt. Diese URLs ermöglichen das ordnungsgemäße Funktionieren der Instanzen.
>
>Standardmäßig sind Instanzen nicht berechtigt, eine Verbindung zu externen URLs herzustellen. Über das Control Panel haben Sie die Möglichkeit, externe URLs zur Liste der berechtigten URLs hinzufügen, sodass sich Ihre Instanz mit ihnen verbinden kann. Dadurch können Sie zwischen Ihren Campaign-Instanzen und externen Systemen, wie z. B. SFTP-Servern oder Websites, eine Verbindung herstellen, um den Datei- und/oder Datentransfer zu ermöglichen.

## Nach dem Hinzufügen einer URL wird sie in der Konfigurationsdatei der Instanz referenziert (serverConf.xml).{#about-url-permissions}

**Verwandte Themen:**

[Campaign-Server konfigurieren[#$tu13]





* 
* 
* 

## Das Control Panel unterstützt die Protokolle **HTTP**, **HTTPS** und **SFTP**. Die Eingabe ungültiger URLs oder Protokolle hat Fehler zur Folge.

* Verwaltung von URL-Genehmigungen {#managing-url-permissions}
* [!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_url_add&quot;
>title=&quot;Hinzufügen neuer URLs&quot;
>abstract=&quot;Fügen Sie URLs hinzu, um Verbindungen zu Ihrer Campaign-Instanz zuzulassen.&quot;
* Gehen Sie wie folgt vor, um eine URL hinzuzufügen, mit der sich Ihre Instanz verbinden kann:************

## Öffnen Sie die Karte **[!UICONTROL Instanzeinstellungen]**, um auf die Registerkarte **[!UICONTROL URL-Genehmigungen]** zuzugreifen.

>[!CONTEXTUALHELP]
>id="cp_instancesettings_url_add"
>title="[!NOTE]"
>abstract="Wenn die Karte &quot;Instanzeinstellungen&quot; nicht auf der Startseite des Control Panels sichtbar ist, bedeutet das, dass Ihre IMS-ORG-Kennung mit keiner Adobe Campaign Classic-Instanz verknüpft ist."

Auf der Registerkarte <b><span class="uicontrol">URL-Genehmigungen</span></b> werden alle externen URLs aufgelistet, mit denen Ihre Instanz eine Verbindung herstellen kann. Diese Liste enthält jedoch nicht die URLs, die für das Funktionieren von Campaign erforderlich sind (z. B. Verbindungen zwischen Infrastrukturelementen).

1. Wählen Sie auf der linken Seite die gewünschte Instanz aus und danach die Schaltfläche **[!UICONTROL Neue URL hinzufügen]**.****

   >![](assets/add_url1.png)
   >
   >[!NOTE]
   >
   >Alle Campaign-Instanzen werden auf der linken Fensterseite aufgelistet.<b><span class="uicontrol"></span></b>

1. Da die Verwaltung der URL-Genehmigungen nur für Campaign Classic-Instanzen möglich ist, erscheint bei der Auswahl einer Campaign Standard-Instanz die Meldung &quot;Nicht anwendbare Instanz&quot;.****

   ![](assets/add_url1.png)Geben Sie die URL ein, die genehmigt werden soll, einschließlich des mit ihr verknüpften Protokolls (HTTP, HTTPS oder SFTP).

   >[!NOTE]
   >
   >Es ist auch möglich, die Verbindung von mehreren Instanzen mit der URL zu genehmigen. Fügen Sie die Instanzen direkt im Feld Instanz(en) ein, indem Sie den ersten Buchstaben tippen.
   >
   >![](assets/add_url2.png)

1. Die URL wird der Liste hinzugefügt und Sie können sich jetzt damit verbinden.

   >[!NOTE]
   >
   >Nach der Validierung werden am Ende der eingegebenen URL automatisch die Zeichen &quot;/.*&quot; hinzugefügt, damit auch alle Unterseiten eingeschlossen sind.

   ![](assets/add_url_listnew.png)

1. Sie können eine URL jederzeit löschen, indem Sie sie selektieren und danach die Schaltfläche **[!UICONTROL URL löschen]** auswählen.

   >[!NOTE]Beachten Sie, dass eine gelöschte URL von Ihrer Instanz nicht mehr aufgerufen werden kann.
   >
   >Häufige Fragen {#common-questions}

   **Ich habe eine neue URL hinzugefügt, meine Instanz kann aber noch immer keine Verbindung mit ihr herstellen. Warum passiert das?**

In manchen Fällen ist es nötig, dass URLs auf die Whitelist gesetzt werden, ein Passwort eingegeben wird oder eine andere Form der Authentifizierung durchgeführt wird, um eine Verbindung mit URLs herzustellen. Das Control Panel unterstützt keine zusätzlichen Formen der Authentifizierung.****

Keep in mind that, if you delete a URL, your instance will not be able to call it again.

## Common questions {#common-questions}

**I added a new URL, but my instance is still unable to connect to that URL. Why is that?**

In some cases, URLs you try to connect to require whitelisting, password entry or another form of authentication. The Control Panel does not manage additional authentication.
