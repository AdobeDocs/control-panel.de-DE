---
title: IP-Whitelisting
description: Erfahren Sie mehr über IP-Whitelisting im Control Panel für den Zugriff auf Instanzen
translation-type: ht
source-git-commit: a2c19296894ff893987290cb287dc7002ab999e5

---


# IP-Whitelisting {#ip-whitelisting}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange"
>title="[!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_iprange&quot;
>title=&quot;Über IP-Whitelisting&quot;
>abstract=&quot;Verwalten Sie IP-Whitelisting, um auf Ihre Instanzen zuzugreifen.&quot;
>additional-url=&quot;https://images-tv.adobe.com/mpcv3/045cac99-f948-478e-ae04-f8c161dcb9e2_1568132508.1920x1080at3000_h264.mp4&quot; text=&quot;Demovideo ansehen&quot;"
>abstract="[!IMPORTANT]"
>additional-url="Diese Funktion ist nur für Campaign Classic-Instanzen verfügbar." text="Über IP-Whitelisting {#about-ip-whitelisting}"

>[!IMPORTANT]Standardmäßig kann nicht über verschiedene IP-Adressen auf Ihre Adobe Campaign Classic-Instanz zugegriffen werden.
>
>Wenn Ihre IP-Adresse nicht auf der Whitelist steht, können Sie sich nicht von dieser Adresse aus bei der Instanz anmelden. Ebenso können Sie keine API mit Ihrer Message Center- oder Marketing-Instanz verbinden, wenn die IP-Adresse nicht speziell für die Instanz auf die Whitelist gesetzt wurde.

## Im Control Panel können Sie neue Verbindungen mit Ihren Instanzen einrichten, indem Sie IP-Adressbereiche auf die Whitelist setzen. Folgen Sie dazu den weiter unten beschriebenen Schritten.{#about-ip-whitelisting}

Nachdem IP-Adressen auf die Whitelist gesetzt wurden, können Sie Campaign-Benutzer erstellen und mit den Adressen verknüpfen, sodass die Benutzer auf die Instanz zugreifen können.

Best Practices {#best-practices}

Beachten Sie unbedingt die folgenden Empfehlungen und Einschränkungen, wenn Sie IP-Adressen über das Control Panel auf die Whitelist setzen.

**Aktivieren Sie nicht den IP-Zugriff für alle Zugriffstypen**, wenn Sie nicht möchten, dass sich die IP-Adresse mit Ihren RT-Servern oder der AEM-Sicherheitszone verbindet.

## **Wenn Sie einer IP-Adresse einen temporären Zugriff auf Ihre Instanz gewährt haben**, entfernen Sie die IP-Adresse wieder aus der Whitelist, wenn diese keine Verbindung mehr mit Ihrer Instanz herstellen muss.

**Wir empfehlen, keine IP-Adressen öffentlicher Orte auf die Whitelist zu setzen** (Flughäfen, Hotels etc.). Verwenden Sie Ihre unternehmenseigene VPN-Adresse, um jederzeit die Sicherheit Ihrer Instanz zu gewährleisten.

* IP-Adressen für den Zugriff auf eine Instanz auf die Whitelist setzen {#whistelisting-ip-addresses}**
* [!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_iprange_add&quot;
>title=&quot;Hinzufügen eines neuen IP-Bereichs&quot;
>abstract=&quot;Definieren Sie den IP-Bereich, den Sie auf die Whitelist setzen möchten, um eine Verbindung zu Ihrer Instanz herzustellen.&quot;**
* **Gehen Sie wie folgt vor, um IP-Adressen auf die Whitelist zu setzen:**

## Öffnen Sie die Karte **[!UICONTROL Instanzeinstellungen]**, um auf die Registerkarte &quot;IP-Whitelisting&quot; zuzugreifen, und wählen Sie dann **[!UICONTROL Neuen IP-Bereich hinzufügen]** aus.

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange_add"
>title="[!NOTE]"
>abstract="Wenn die Karte &quot;Instanzeinstellungen&quot; nicht auf der Startseite des Control Panels sichtbar ist, bedeutet das, dass Ihre IMS-ORG-Kennung mit keiner Adobe Campaign Classic-Instanz verknüpft ist."

![](assets/ip_whitelist_list1.png)

1. Füllen Sie wie unten angegeben die Informationen für den IP-Bereich aus, den Sie auf die Whitelist setzen möchten.********

   >![](assets/ip_whitelist_add1.png)
   >
   >**[!UICONTROL Instanz(en)]**: Die Instanzen, mit denen sich die IP-Adressen verbinden können. Mehrere Instanzen können gleichzeitig bearbeitet werden. Beispielsweise kann IP-Whitelisting im selben Schritt sowohl für Produktions- als auch für Staging-Instanzen ausgeführt werden.

   **[!UICONTROL IP-Bereich]**: Der IP-Bereich, der auf die Whitelist gesetzt werden soll (im CIDR-Format). Beachten Sie, dass sich ein IP-Bereich nicht mit einem bereits auf der Whitelist vorhandenen Bereich überschneiden darf. Löschen Sie in diesem Fall zunächst den Bereich, der die überlappende IP enthält.

1. [!NOTE]

   IP-Bereiche werden über das Control Panel im CIDR-Format (Classless Inter-Domain Routing) hinzugefügt. Die Syntax besteht aus einer IP-Adresse, gefolgt vom Zeichen / und einer Dezimalzahl. Format und Syntax sind in [diesem Artikel[#$tu30] ausführlich beschrieben.

   * 
   * 
   >
   >
   >
   >
   >**[!UICONTROL Zugriff auf die Campaign-Konsole]**: Die IP-Adressen können sich mit der Campaign Classic-Konsole verbinden. Beachten Sie, dass der Konsolenzugriff nur für Marketing-Instanzen möglich ist. Der Zugriff auf MID- und RT-Instanzen ist nicht erlaubt und deshalb auch nicht aktiviert.

   * **[!UICONTROL AEM-Verbindung]**: Die angegebenen AEM-IP-Adressen können sich mit der Marketing-Instanz verbinden.
   * **[!UICONTROL Externe API-Verbindung]**: Externe APIs mit den angegebenen IP-Adressen können sich mit der Marketing- und/oder Message Center (RT)-Instanz verbinden. Beachten Sie, dass die Verbindung mit der Konsole für RT-Instanzen nicht aktiviert ist.


1. ![](assets/ip_whitelist_acesstype.png)

   * Wählen Sie die Schaltfläche **[!UICONTROL Speichern]** aus. Der IP-Bereich wird zur Liste der auf der Whitelist befindlichen IP-Adressen hinzugefügt.
   * ![](assets/ip_whitelist_added.png)]**
   * Um IP-Bereiche aus der Whitelist zu löschen, selektieren Sie sie und wählen Sie dann die Schaltfläche **[!UICONTROL IP-Bereiche löschen]** aus.
   **Verwandte Themen:**

1. [IP Whitelisting (Video-Tutorial)[#$tu44]]**

   

To delete whitelisted IP ranges, select them then click the **[!UICONTROL Delete IP range]** button.

**Related topics:**
* [IP whitelisting (tutorial video)-ERR:REF-NOT-FOUND-
* [Linking a security zone to an operator-ERR:REF-NOT-FOUND-
