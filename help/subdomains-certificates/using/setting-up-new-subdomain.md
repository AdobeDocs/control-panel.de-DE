---
title: Einrichten einer neuen Subdomain
description: Erfahren Sie, wie Sie eine neue Subdomain für Ihre Campaign-Instanz einrichten.
translation-type: tm+mt
source-git-commit: 766ff590d83929eeddb69113904643517c1475ad

---


# Einrichten einer neuen Subdomain {#setting-up-subdomain}

>[!NOTE]
>
>Die Subdomänenübertragung von der Systemsteuerung befindet sich derzeit in der Betaphase und unterliegt häufigen Aktualisierungen und Änderungen ohne Benachrichtigung.

## Vollständige Subdomain-Zuweisung {#full-subdomain-delegation}

Über das Control Panel können Sie Adobe Campaign eine Subdomain vollständig zuweisen. Gehen Sie dazu wie folgt vor:

>[!NOTE]
>
>Wenn Sie keine Subdomäne für Adobe konfiguriert haben, gilt die erste von Ihnen eingerichtete Subdomäne als **primäre Subdomäne**.
>Ein **umgekehrter DNS-Datensatz** wird erstellt und als Standard-Subdomäne für Postfächer (Sender, Antwort, Fehler-E-Mail-Adressen) festgelegt.

1. Wählen Sie auf der Karte **[!UICONTROL Subdomains &amp; Zertifikate]**die gewünschte Produktionsinstanz und danach**[!UICONTROL  Neue Subdomain einrichten]** aus.

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >Subdomain delegation is available for **production** instances only.

1. Wählen Sie **[!UICONTROL Weiter]**aus, um die Methode der vollständigen Zuweisung zu bestätigen.

   ![](assets/subdomain3.png)

   >[!NOTE]
   >
   >[CNAME](#use-cnames) und benutzerdefinierte Methoden werden derzeit vom Control Panel nicht unterstützt.

1. Erstellen Sie die gewünschte Subdomain und die gewünschten Nameserver in der von Ihrem Unternehmen verwendeten Hosting-Lösung. Kopieren Sie dazu die im Assistenten angezeigten Adobe-Nameserver-Informationen und fügen Sie sie ein. For more on how to create a subdomain in a hosting solution, refer to the [tutorial video](https://video.tv.adobe.com/v/30175?captions=ger).

   >[!CAUTION]
   >
   >Achten Sie beim Konfigurieren von Nameservers darauf, Ihre Stammteildomäne **nie an Adobe** zu delegieren. Andernfalls kann die Domäne nur mit Adobe verwendet werden. Jegliche andere Verwendung ist nicht möglich, z. B. das Senden interner E-Mails an Mitarbeiter Ihrer Organisation.

   ![](assets/subdomain4.png)

   Nachdem die Subdomain mit den entsprechenden Adobe-Nameserver-Informationen erstellt wurde, wählen Sie **[!UICONTROL Weiter]**aus.

1. Wählen Sie den gewünschten Anwendungsfall für die Subdomain aus:

   * **Marketingnachrichten**: für kommerzielle Zwecke bestimmte Mitteilungen. Beispiel: Vertriebs-E-Mail-Kampagne.
   * **Transaktions- und Betriebskommunikation**: Transaktionskommunikation enthält Informationen zum Abschluss eines Prozesses, den der Empfänger mit Ihnen begonnen hat. Beispiel: Kaufbestätigung, E-Mail zum Zurücksetzen des Passworts. Organisatorische Kommunikation bezieht sich auf den Austausch von Informationen, Ideen und Ansichten innerhalb und außerhalb der Organisation ohne kommerziellen Zweck.
   >[!NOTE]
   >
   >Die Unterteilung Ihrer Subdomains nach Anwendungsfällen ist eine Best Practice für die Zustellbarkeit. Dadurch wird die Reputation jeder Subdomain isoliert und geschützt.
   >
   >Wenn Ihre Subdomain für Marketingnachrichten beispielsweise von Internetdienstanbietern auf die Blacklist gesetzt wird, wird Ihre Subdomain für Transaktionsnachrichten nicht beeinträchtigt und kann weiterhin Nachrichten senden.

   ![](assets/subdomain5.png)

1. Geben Sie die von Ihnen erstellte Subdomain in Ihre Hosting-Lösung ein und wählen Sie dann **[!UICONTROL Senden]**aus.

   >[!NOTE]
   >
   > Vergewissern Sie sich, dass Sie den **vollständigen Namen** der zuzuweisenden Subdomain eingeben. Um beispielsweise die Subdomain &quot;usoffer.email.weretail.com&quot; zuzuweisen, geben Sie &quot;usoffer.email.weretail.com&quot; ein.

   ![](assets/subdomain6.png)

1. Sobald die Subdomäne übermittelt wurde, prüft die Systemsteuerung, ob sie korrekt auf Adobe NS-Datensätze verweist und ob der SOA-Datensatz (Start of Authority) für diese Subdomäne nicht vorhanden ist.

1. Wenn die Prüfungen erfolgreich sind, beginnt die Systemsteuerung mit der Einrichtung der Subdomäne mit DNS-Datensätzen, zusätzlichen URLs, Inboxes usw. Wählen Sie **[!UICONTROL Prozessdetails]**aus, um weitere Informationen zum Konfigurationsfortschritt zu erhalten.

   ![](assets/subdomain7.png)

   >[!NOTE]
   >
   >In einigen Fällen erfolgt die Übertragung durch, aber die Subdomäne wird möglicherweise nicht erfolgreich überprüft. Die Subdomäne wird direkt in die Liste der **[!UICONTROL verifizierten Subdomänen]**mit dem Status &quot;**[!UICONTROL  Nicht verifiziert]** &quot;und einem Auftragsprotokoll mit Informationen zum Fehler aufgenommen. Wenden Sie sich an den Kundendienst, wenn Sie Probleme bei der Lösung des Problems haben.
   >
   >Beachten Sie, dass während der Ausführung von Subdomänendelegationen andere Anfragen über die Systemsteuerung in eine Warteschlange eingegeben und erst nach Abschluss der Subdomänendelegation ausgeführt werden, um Leistungsprobleme zu vermeiden.

Am Ende des Prozesses werden die Subdomänen für die Verwendung mit Ihrer Adobe Campaign-Instanz konfiguriert und die folgenden Elemente werden erstellt:

* **Die Subdomain** mit den folgenden **DNS-Einträgen**: SOA, MX, CNAME(s), DKIM, SPF, TXT,
* **Zusätzliche Subdomänen** zum Hosten von Spiegeln, Ressourcen, Verfolgungsseiten und Domänenschlüssel,
* **Postfächer**: Absender, Fehler, Antwort.

>[!NOTE]
>
>Standardmäßig ist der Posteingang &quot;Antwort auf&quot;in der Systemsteuerung so konfiguriert, dass E-Mails gelöscht werden, und kann nicht überprüft werden. Verwenden Sie diese Adresse nicht, wenn Sie Ihren Posteingang &quot;Antwort auf&quot;für Ihre Marketingkampagnen überwachen möchten.


You can get more details on the subdomain by clicking the **[!UICONTROL Subdomain Details]**button.

![](assets/subdomain_details_general.png)

![](assets/subdomains_details_senderinfo.png)

>[!NOTE]
>
>Zusätzlich zur Verarbeitungsstufe benachrichtigt Adobe das Bereitstellungsteam über die neue Subdomäne, um die erstellte Subdomäne zu prüfen. Das Audit-Verfahren kann bis zu 3 Tage nach der Übertragung der Subdomäne dauern.
>
>Zu den durchgeführten Überprüfungen gehören Feedback-Schleifen und Spam-Reklamationsschleifen-Tests. Daher empfehlen wir nicht, die Subdomäne vor Abschluss der Prüfung zu verwenden, da dies zu einem schlechten Ruf der Subdomäne führen könnte.

## Verwenden von CNAME {#use-cnames}

Die Verwendung von CNAME für die Zuweisung von Subdomains wird von Adobe nicht empfohlen und vom Control Panel nicht unterstützt. Wenden Sie sich zur Verwendung dieser Methode an den Adobe-Kundendienst.
