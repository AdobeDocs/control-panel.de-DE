---
title: Details der Instanz
description: Erfahren Sie, wie Sie die Details der Instanz im Control Panel überwachen können
translation-type: ht
source-git-commit: a2c19296894ff893987290cb287dc7002ab999e5

---


# Details der Instanz {#instance-details}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_instancedetails"
>title="[!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_instancedetails&quot;
>title=&quot;Über die Details der Instanz&quot;
>abstract=&quot;Zeigen Sie die Details Ihrer Adobe Campaign-Instanzen an: Typen, Namen, Build-Informationen und mögliche Upgrade-Empfehlungen.&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/de-DE/campaign-classic/using/release-notes/latest-release.html&quot; text=&quot;Versionshinweise zu Campaign Classic&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/de-DE/campaign-standard/using/release-notes/release-notes.html&quot; text=&quot;Versionshinweise zu Campaign Standard&quot;"
>abstract="[!IMPORTANT]"
>additional-url="Diese Funktion ist nur für Campaign Classic-Instanzen verfügbar." text="Über die Details der Instanz {#about-instance-details}"
>additional-url="Die Architektur Ihrer Adobe Campaign Classic-Instanz kann mehrere Server umfassen, um flexible Marketing-Aktivitäten zu ermöglichen. So können beispielsweise Marketing-, Echtzeit- (oder Message Center-) und Mid Sourcing-Server Ihre Instanz unterstützen." text="Mit der Funktion &quot;Details der Instanz&quot; können Sie sich die flache Architektur Ihrer Instanz anzeigen lassen. Zusätzlich zu den Server-Informationen erfahren Sie hier auch, ob der Build Ihrer Instanz aktuell ist oder ob ein Upgrade empfohlen wird."

>[!NOTE]
>
>Es ist empfehlenswert, Instanzen mindestens einmal jährlich zu aktualisieren, um ein Nachlassen der Leistung zu verhindern und die neuesten Funktionen und Fehlerkorrekturen von Adobe Campaign Classic zu nutzen.

## **Verwandte Themen:**

[Durchführen eines Build-Upgrades[#$tu14]



>
>
>



* 
* 

## Wählen Sie im linken Fenster die gewünschte Campaign Classic-Instanz aus.{#retrieving-information-about-instances}

[!NOTE]

1. Alle Campaign-Instanzen werden auf der linken Fensterseite aufgelistet. Da die Funktion &quot;Details der Instanz&quot; nur für Campaign Classic-Instanzen unterstützt wird, erscheint bei der Auswahl einer Campaign Standard-Instanz die Meldung &quot;Nicht anwendbare Instanz&quot;.********

   >[!NOTE]Die mit der Instanz verbundenen Server werden angezeigt.
   >
   >![](assets/instance_details.png)

1. Diese Informationen sind verfügbar:

   >**[!UICONTROL Typ:]** der Typ des Servers. Mögliche Werte sind MKT (Marketing), MID (Mid Sourcing) und RT (Message Center-/Echtzeit-Messaging).
   >
   >**[!UICONTROL Name:]** der Name des Servers.

1. **[!UICONTROL Build:]** die auf dem Server installierte Build-Version.

   **[!UICONTROL Aktualisierungsinformationen:]** In dieser Spalte werden für den Server erforderliche Updates aufgeführt.

Grün: Ihr Server ist auf dem neuesten Stand, kein Upgrade ist erforderlich.

* **[!UICONTROL Gelb: Sie sollten ein Upgrade in Erwägung ziehen. Ihnen fehlen die neuesten Funktionen und Fehlerkorrekturen.]**
* **[!UICONTROL Rot: Führen Sie möglichst rasch ein Upgrade durch. Ihnen fehlen neue Funktionen und die Server-Leistung ist möglicherweise nicht optimal.]**
* Informationen zur Aktualisierung von Servern finden Sie in [dieser Dokumentation[#$tu36].]**
* 
   * 
   * 
   * 

If one of your servers requires to be upgraded, refer to [this documentation-ERR:REF-NOT-FOUND- for more details on how to proceed.

## Common questions {#common-questions}

**I do not see the MID server on my instance architecture, does it mean my instances are not functioning correctly? Do I need the RT instance for something I am not able to do today?**

Your own instance can look very different, and it may not have all types of servers, or it can have several of the same server. Not having one type of the server or another does not mean you cannot send a real-time message or perform other kinds of activities. You can request additional server capacity, additional fees will apply.

Please contact Customer Care if you believe some servers are not showing in the &quot;Instance Details&quot; page. Make sure you note the specific instance URL in your message.
