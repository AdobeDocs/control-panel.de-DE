---
title: Einrichten einer neuen Subdomäne
description: Erfahren Sie, wie Sie eine neue Subdomäne für Ihre Kampagneninstanzen einrichten.
translation-type: tm+mt
source-git-commit: cde5b58c1cf65d23b68c5fa6b1a484fc6db40325

---


# Einrichten einer Subdomäne {#setting-up-subdomain}

Über die Systemsteuerung können Sie eine Subdomäne vollständig an Adobe Campaign delegieren. Gehen Sie dazu wie unten beschrieben vor.

>[!NOTE]
>
>Die Verwendung von CNAMEs für Subdomänendelegationen wird nicht über die Systemsteuerung unterstützt. For more on this method, refer to [this page](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).

1. Wählen Sie auf der Karte &quot; **[!UICONTROL Subdomänen und Zertifikate]**&quot;die gewünschte Instanz aus und klicken Sie dann auf die Schaltfläche Neue Subdomäne**[!UICONTROL  einrichten]** .

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >Die Schaltfläche **[!UICONTROL Neue Subdomäne]**einrichten steht nur für Produktionsinstanzen zur Verfügung.

1. Wählen Sie die Methode **[!UICONTROL Delegation bei Adobe]**und klicken Sie dann auf**[!UICONTROL  Weiter]**.

   ![](assets/subdomain3.png)

1. Erstellen Sie die gewünschte Subdomäne in der von Ihrem Unternehmen verwendeten Hostinglösung. Kopieren Sie dazu die im Assistenten angezeigten Adobe Nameserver-Informationen und fügen Sie sie dann in Ihre Hostinglösung ein.

   Weitere Informationen zum Erstellen einer Subdomäne in einer Hostinglösung finden Sie im Lernvideo, auf das über den Assistenten zugegriffen werden kann.

   ![](assets/subdomain4.png)

   Nachdem die Subdomäne mit den entsprechenden Adobe-Serverinformationen erstellt wurde, klicken Sie auf **[!UICONTROL Weiter]**.

1. Wählen Sie die gewünschte Verwendungsart für die Subdomäne aus:

   * **Marketingkommunikation**: für kommerzielle Zwecke bestimmte Mitteilungen. Beispiel: Vertriebs-E-Mail-Kampagne.
   * **Transaktions- und Betriebskommunikation**: Transaktionskommunikation enthält Informationen zum Abschluss eines Prozesses, den der Empfänger mit Ihnen gestartet hat. Beispiel: Kaufbestätigung, E-Mail zum Zurücksetzen des Kennworts. Organisatorische Kommunikation bezieht sich auf den Austausch von Informationen, Ideen und Ansichten innerhalb und außerhalb der Organisation ohne kommerziellen Zweck.
   Eine solche Unterteilung Ihrer Subdomänen ist eine Best Practice für die Bereitstellung. Dadurch wird der Ruf jeder Subdomäne isoliert und geschützt. Wenn Ihre Subdomäne für Marketingkommunikation beispielsweise letztendlich von Internet Service Providern auf die schwarze Liste gesetzt wird, wird Ihre Subdomäne für Transaktionskommunikation nicht beeinträchtigt und kann weiterhin Nachrichten senden.

   ![](assets/subdomain5.png)

   >[!NOTE]
   >
   >Sie können nur einen Anwendungsfall auswählen, der für Ihre Instanz konfiguriert wurde. Wenn die Instanz nur für &quot;Marketing-Kommunikation&quot;konfiguriert wurde, können Sie den Anwendungsfall &quot;Transaktions- und Vorgangskommunikation&quot;nicht auswählen.

1. Geben Sie die von Ihnen erstellte Subdomäne mit den Adobe Nameserver-Informationen in Ihre Hostinglösung ein und klicken Sie dann auf **[Senden]**.

   >[!NOTE]
   >
   > Achten Sie darauf, die **vollständige** Subdomäne zum Delegieren auszufüllen. Um beispielsweise die Subdomäne &quot;usoffer.email.weretail.com&quot;zu delegieren, geben Sie &quot;usoffer.email.weretail.com&quot;ein.

   ![](assets/subdomain6.png)

1. Sobald die Subdomäne gesendet wurde, führt die Systemsteuerung verschiedene Vorgänge aus, um die Subdomäne zu konfigurieren und sicherzustellen, dass sie korrekt auf die Kampagneninstanz verweist (Erstellung von Namespacedatensätzen, Konfiguration der Kampagneninstanz, Überprüfung des Datensatzes am Anfang der Behörde usw.).

   Sie können jederzeit weitere Details zum Konfigurationsstatus abrufen, indem Sie auf die Schaltfläche **[!UICONTROL Prozessdetails]**klicken.

   ![](assets/subdomain7.png)

Was bekommen Sie am Ende des Prozesses?
* Subdomäne mit den folgenden DNS-Datensätzen - SOA, MX, CNAME(s), DKIM, SPF, TXT.
* Zusätzliche Subdomänen zum Hosten von Mirror, Ressource, Verfolgungsseiten und domainkey
* Postfächer - Sender, Fehler, Antwort
* Letztlich werden die Subdomänen für die Verwendung mit Ihrer Adobe Campaign-Instanz konfiguriert
