---
title: IP-Listen zulassen
description: Erfahren Sie, wie Sie der zulassungsliste in der Systemsteuerung IP-Adressen hinzufügen, z. B. den Zugriff auf die Systemsteuerung.
translation-type: tm+mt
source-git-commit: d8fe1c2e847fa25919f81bf0a4195de5ad0b2781
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 47%

---


# IP-Listen zulassen {#ip-whitelisting}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange"
>title="Info zur IP-Listen zulassen"
>abstract="Hinzufügen IP-Adressen an die zulassungsliste, um auf Ihre Instanzen zuzugreifen."
>additional-url="https://images-tv.adobe.com/mpcv3/045cac99-f948-478e-ae04-f8c161dcb9e2_1568132508.1920x1080at3000_h264.mp4" text="Demovideo ansehen"

>[!IMPORTANT]
>
>Diese Funktion ist nur für Campaign Classic-Instanzen verfügbar.

## Info zur IP-Listen zulassen {#about-ip-whitelisting}

Standardmäßig kann nicht über verschiedene IP-Adressen auf Ihre Adobe Campaign Classic-Instanz zugegriffen werden.

Wenn Ihre IP-Adresse nicht zur zulassungsliste hinzugefügt wurde, können Sie sich nicht von dieser Adresse aus bei der Instanz anmelden. Auf dieselbe Weise können Sie eine API möglicherweise nicht mit Ihrem Message Center oder Ihrer Marketing-Instanz verbinden, wenn die IP-Adresse nicht explizit mit der Instanz zur zulassungsliste hinzugefügt wurde.

Über die Systemsteuerung können Sie neue Verbindungen zu Ihren Instanzen einrichten, indem Sie IP-Adressbereiche zur zulassungsliste hinzufügen. Folgen Sie dazu den weiter unten beschriebenen Schritten.

Sobald sich die IP-Adressen auf der zulassungsliste befinden, können Sie Operatoren für die Kampagne erstellen und mit ihnen verknüpfen, damit die Benutzer auf die Instanz zugreifen können.

## Best Practices {#best-practices}

Beachten Sie beim Hinzufügen von IP-Adressen zur zulassungsliste in der Systemsteuerung die unten stehenden Empfehlungen und Einschränkungen.

* **Aktivieren Sie nicht den IP-Zugriff für alle Zugriffstypen**, wenn Sie nicht möchten, dass sich die IP-Adresse mit Ihren RT-Servern oder der AEM-Sicherheitszone verbindet.
* **Wenn Sie vorübergehend den Zugriff auf Ihre Instanz für eine IP-Adresse** aktiviert haben, müssen Sie die IP-Adressen aus der zulassungsliste entfernen, sobald Sie keine Verbindung mehr zu Ihrer Instanz herstellen müssen.
* **Es wird nicht empfohlen, der zulassungsliste IP-Adressen öffentlicher Orte (Flughäfen, Hotels usw.) hinzuzufügen** . Verwenden Sie Ihre unternehmenseigene VPN-Adresse, um jederzeit die Sicherheit Ihrer Instanz zu gewährleisten.

## Hinzufügen von IP-Adressen zur zulassungsliste für den Instanzzugriff {#whistelisting-ip-addresses}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange_add"
>title="Hinzufügen neuer IP-Bereich"
>abstract="Definieren Sie den IP-Bereich, den Sie der zulassungsliste hinzufügen möchten, um eine Verbindung zu Ihrer Instanz herzustellen."

Gehen Sie wie folgt vor, um der zulassungsliste IP-Adressen hinzuzufügen:

1. Open the **[!UICONTROL Instances Settings card]** to access the IP allow listing tab, then click **[!UICONTROL Add new IP Range]**.

   >[!NOTE]
   >
   >Wenn die Karte &quot;Instanzeinstellungen&quot; nicht auf der Startseite des Control Panels sichtbar ist, bedeutet das, dass Ihre IMS-ORG-Kennung mit keiner Adobe Campaign Classic-Instanz verknüpft ist.

   ![](assets/ip_whitelist_list1.png)

1. Füllen Sie die Informationen für den IP-Bereich aus, den Sie der zulassungsliste hinzufügen möchten, wie nachfolgend beschrieben.

   ![](assets/ip_whitelist_add1.png)

   * **[!UICONTROL Instanz(en)]**: Die Instanzen, mit denen sich die IP-Adressen verbinden können. Mehrere Instanzen können gleichzeitig bearbeitet werden. Beispielsweise kann eine IP-Listen-Listen-Auflistung sowohl für Produktions- als auch für Stage-Instanzen im selben Schritt durchgeführt werden.
   * **[!UICONTROL IP-Bereich]**: Der IP-Bereich, den Sie der zulassungsliste im CIDR-Format hinzufügen möchten. Beachten Sie, dass ein IP-Bereich keinen vorhandenen Bereich auf der zulassungsliste überlappen kann. Löschen Sie in diesem Fall zunächst den Bereich, der die überlappende IP enthält.

   >[!NOTE]
   >
   >IP-Bereiche werden über das Control Panel im CIDR-Format (Classless Inter-Domain Routing) hinzugefügt. Die Syntax besteht aus einer IP-Adresse, gefolgt vom Zeichen / und einer Dezimalzahl. Format und Syntax sind in [diesem Artikel](https://whatismyipaddress.com/cidr) ausführlich beschrieben.
   >
   >Sie können im Internet nach kostenlosen Online-Tools suchen, mit denen Sie Ihren IP-Bereich in das CIDR-Format konvertieren können.

   * **[!UICONTROL Beschriftung]**: Die Beschriftung, die in der zulassungsliste angezeigt wird.
   * **[!UICONTROL Name]**: Der Name muss für den Zugriffstyp, die Instanz (im Fall einer externen API-Verbindung) und die IP-Adresse eindeutig sein.


1. Geben Sie die Art des Zugriffs an, den Sie den IP-Adressen gewähren möchten:

   * **[!UICONTROL Zugriff auf die Campaign-Konsole]**: Die IP-Adressen können sich mit der Campaign Classic-Konsole verbinden. Beachten Sie, dass der Konsolenzugriff nur für Marketing-Instanzen möglich ist. Der Zugriff auf MID- und RT-Instanzen ist nicht erlaubt und deshalb auch nicht aktiviert.
   * **[!UICONTROL AEM-Verbindung]**: Die angegebenen AEM-IP-Adressen können sich mit der Marketing-Instanz verbinden.
   * **[!UICONTROL Externe API-Verbindung]**: Externe APIs mit den angegebenen IP-Adressen können sich mit der Marketing- und/oder Message Center (RT)-Instanz verbinden. Beachten Sie, dass die Verbindung mit der Konsole für RT-Instanzen nicht aktiviert ist.

   ![](assets/ip_whitelist_acesstype.png)

1. Wählen Sie die Schaltfläche **[!UICONTROL Speichern]** aus. Der IP-Bereich wird der zulassungsliste hinzugefügt.

   ![](assets/ip_whitelist_added.png)

Um IP-Bereiche aus der zulassungsliste zu löschen, wählen Sie sie aus und klicken Sie dann auf die Schaltfläche IP-Bereich **[!UICONTROL löschen]** .

**Verwandte Themen:**
* [IP-Listen zulassen (Tutorial-Video)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/ip-allow-listing.html)
* [Sicherheitszone mit einem Benutzer verknüpfen](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html#Linking_a_security_zone_to_an_operator)
