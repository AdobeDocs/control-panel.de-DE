---
title: Einrichten einer neuen Subdomäne
description: Erfahren Sie, wie Sie eine neue Subdomäne für Ihre Kampagneninstanzen einrichten.
translation-type: tm+mt
source-git-commit: 52f155bbbecec9edabc66cbc28756f9579b81f04

---


# Einrichten einer neuen Subdomäne {#setting-up-subdomain}

>[!NOTE]
>
>Die Subdomänenübertragung von der Systemsteuerung befindet sich derzeit in der Betaphase und unterliegt häufigen Aktualisierungen und Änderungen ohne Benachrichtigung.

## Vollständige Subdomäne-Übertragung {#full-subdomain-delegation}

Über die Systemsteuerung können Sie eine Subdomäne vollständig an Adobe Campaign delegieren. Gehen Sie dazu wie folgt vor:

1. Wählen Sie auf der Karte &quot; **[!UICONTROL Subdomänen und Zertifikate]**&quot;die gewünschte Produktionsinstanz und klicken Sie dann auf Neue Subdomäne**[!UICONTROL  einrichten]**.

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >Die Subdoman-Delegation ist nur für **Produktionsinstanzen** verfügbar.

1. Klicken Sie auf **[!UICONTROL Weiter]**, um die vollständige Delegationsmethode zu bestätigen.

   ![](assets/subdomain3.png)

   >[!NOTE]
   >
   >[CNAME](#use-cnames) und benutzerdefinierte Methoden werden derzeit nicht von der Systemsteuerung unterstützt.

1. Erstellen Sie die gewünschte Subdomäne und Nameserver in der von Ihrem Unternehmen verwendeten Hostinglösung. Kopieren Sie dazu die im Assistenten angezeigten Adobe Nameserver-Informationen und fügen Sie sie ein. Weitere Informationen zum Erstellen einer Subdomäne in einer Hostinglösung finden Sie im [Lernvideo](https://video.tv.adobe.com/v/30175?captions=ger).

   >[!CAUTION]
   >
   >Achten Sie beim Konfigurieren von Nameservers darauf, Ihre Stammteildomäne **nie an Adobe** zu delegieren. Andernfalls kann die Domäne nur mit Adobe verwendet werden. Jegliche andere Verwendung ist nicht möglich, z. B. das Senden interner E-Mails an Mitarbeiter Ihrer Organisation.

   ![](assets/subdomain4.png)

   Beachten Sie, dass bei einer nicht konfigurierten Subdomäne die von Ihnen eingerichtete Subdomäne als **primäre Subdomäne** gilt. Die Posteingänge (Sender, Fehler, Antwortadressen) bleiben für alle Subdomänen, die später in dieser Subdomäne konfiguriert werden, gleich.

   Nachdem die Subdomäne mit den entsprechenden Adobe-Serverinformationen erstellt wurde, klicken Sie auf **[!UICONTROL Weiter]**.

1. Wählen Sie die gewünschte Verwendungsart für die Subdomäne aus:

   * **Marketingkommunikation**: für kommerzielle Zwecke bestimmte Mitteilungen. Beispiel: Vertriebs-E-Mail-Kampagne.
   * **Transaktions- und Betriebskommunikation**: Transaktionskommunikation enthält Informationen zum Abschluss eines Prozesses, den der Empfänger mit Ihnen gestartet hat. Beispiel: Kaufbestätigung, E-Mail zum Zurücksetzen des Kennworts. Organisatorische Kommunikation bezieht sich auf den Austausch von Informationen, Ideen und Ansichten innerhalb und außerhalb der Organisation ohne kommerziellen Zweck.
   >[!NOTE]
   >
   >Die Unterteilung Ihrer Subdomänen nach Anwendungsfällen ist eine Best Practice für die Bereitstellung. Dadurch wird der Ruf jeder Subdomäne isoliert und geschützt.
   >
   >Wenn Ihre Subdomäne für Marketingkommunikation beispielsweise letztendlich von Internet Service Providern auf die schwarze Liste gesetzt wird, wird Ihre Subdomäne für Transaktionskommunikation nicht beeinträchtigt und kann weiterhin Nachrichten senden.

   ![](assets/subdomain5.png)

1. Geben Sie die von Ihnen erstellte Subdomäne in Ihre Hostinglösung ein und klicken Sie dann auf **[!UICONTROL Senden]**.

   >[!NOTE]
   >
   > Vergewissern Sie sich, dass Sie den **vollständigen Namen** der zu delegierenden Subdomäne eingeben. Um beispielsweise die Subdomäne &quot;usoffer.email.weretail.com&quot;zu delegieren, geben Sie &quot;usoffer.email.weretail.com&quot;ein.

   ![](assets/subdomain6.png)

1. Sobald die Subdomäne übermittelt wurde, prüft die Systemsteuerung, ob sie korrekt auf Adobe NS-Datensätze verweist und ob der SOA-Datensatz (Start of Authority) für diese Subdomäne nicht vorhanden ist.

1. Wenn die Prüfungen erfolgreich sind, beginnt die Systemsteuerung mit der Einrichtung der Subdomäne mit DNS-Datensätzen, zusätzlichen URLs, Postfächern usw. Weitere Informationen zum Konfigurationsstatus erhalten Sie, wenn Sie auf die Schaltfläche **[!UICONTROL Prozessdetails]**klicken.

   ![](assets/subdomain7.png)

   >[!NOTE]
   >
   >In einigen Fällen erfolgt die Übertragung durch, aber die Subdomäne wird möglicherweise nicht erfolgreich überprüft. Die Subdomäne wird direkt in die Liste der **[!UICONTROL verifizierten Subdomänen]**mit dem Status &quot;**[!UICONTROL  Nicht verifiziert]** &quot;und einem Auftragsprotokoll mit Informationen zum Fehler geleitet. Wenden Sie sich an den Kundendienst, wenn Sie Probleme bei der Lösung des Problems haben.
   >
   >Beachten Sie, dass während der Ausführung von Subdomänendelegationen andere Anfragen über die Systemsteuerung in eine Warteschlange eingegeben und erst nach Abschluss der Subdomänendelegation ausgeführt werden, um Leistungsprobleme zu vermeiden.

Am Ende des Prozesses werden die Subdomänen für die Verwendung mit Ihrer Adobe Campaign-Instanz konfiguriert und die folgenden Elemente werden erstellt:

* **Die Subdomäne** mit den folgenden **DNS-Datensätzen**: SOA, MX, CNAME(s), DKIM, SPF, TXT,
* **Zusätzliche Subdomänen** zum Hosten von Mirror, Ressource, Verfolgungsseiten und domainkey,
* **Postfächer**: Sender, Fehler, Antwort.

Sie können weitere Details zur Subdomäne abrufen, indem Sie auf die Schaltfläche &quot; **[!UICONTROL Subdomänendetails]**&quot;klicken.

![](assets/subdomain_details_general.png)

![](assets/subdomains_details_senderinfo.png)

>[!NOTE]
>
>Zusätzlich zur Verarbeitungsstufe benachrichtigt Adobe das Bereitstellungsteam über die neue Subdomäne, um die erstellte Subdomäne zu prüfen. Das Audit-Verfahren kann bis zu 3 Tage nach der Übertragung der Subdomäne dauern.
>
>Zu den durchgeführten Überprüfungen gehören Feedback-Schleifen und Spam-Reklamationsschleifen-Tests. Daher empfehlen wir nicht, die Subdomäne vor Abschluss der Prüfung zu verwenden, da dies zu einem schlechten Ruf der Subdomäne führen könnte.

## Verwendung von CNAMEs {#use-cnames}

Die Verwendung von CNAMEs für die Übertragung von Subdomänen wird von Adobe nicht empfohlen und wird nicht über die Systemsteuerung unterstützt. Wenden Sie sich zur Verwendung dieser Methode an den Adobe-Kundendienst.
