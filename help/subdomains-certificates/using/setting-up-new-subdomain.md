---
title: Einrichten einer neuen Subdomain
description: Erfahren Sie, wie Sie eine neue Subdomain für Ihre Campaign-Instanz einrichten.
translation-type: tm+mt
source-git-commit: 43d5d522c29586b9898d924dd164435ee8fbb614

---


# Einrichten einer neuen Subdomain {#setting-up-subdomain}

>[!CONTEXTUALHELP]
>id=&quot;cp_subdomain_management&quot;
>title=&quot;Einrichten neuer Subdomains und Verwalten von Zertifikaten&quot;
>abstract=&quot;Sie müssen eine neue Subdomain einrichten und die SSL-Zertifikate Ihrer Subdomains verwalten, um mit Adobe Campaign E-Mails senden oder Landingpages veröffentlichen zu können.&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/de-DE/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html&quot; text=&quot;Überwachen von SSL-Zertifikaten der Subdomains&quot;

>[!IMPORTANT]
>
>Die Subdomain-Zuweisung über das Control Panel befindet sich in der Beta-Phase und unterliegt häufigen Aktualisierungen und Änderungen ohne Vorankündigung.

## Vollständige Subdomain-Zuweisung {#full-subdomain-delegation}

Über das Control Panel können Sie Adobe Campaign eine Subdomain vollständig zuweisen. Gehen Sie dazu wie folgt vor:

>[!NOTE]
>
>Wenn die ausgewählte Instanz keine zuvor konfigurierten Subdomains hat, wird die erste Subdomain, die Adobe zugewiesen wird, zur **primären Subdomain** für diese Instanz. Sie werden dies später nicht mehr ändern können.
>
>Mithilfe dieser primären Subdomain werden Reverse-DNS-Einträge für andere Subdomains erstellt. Außerdem werden über die primäre Subdomain Antwort- und Bounce-Adressen für andere Subdomains generiert.

1. Wählen Sie auf der **[!UICONTROL Subdomains & Certificates]** Karte die gewünschte Produktionsinstanz aus und klicken Sie dann auf **[!UICONTROL Setup new subdomain]**.

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >Die Zuweisung von Subdomains ist nur für **Produktionsinstanzen** verfügbar.

1. Click **[!UICONTROL Next]** to confirm the full delegation method.

   ![](assets/subdomain3.png)

   >[!NOTE]
   >
   >[CNAME](#use-cnames) und benutzerdefinierte Methoden werden derzeit vom Control Panel nicht unterstützt.

1. Erstellen Sie die gewünschte Subdomain und die gewünschten Nameserver in der von Ihrem Unternehmen verwendeten Hosting-Lösung. Kopieren Sie dazu die im Assistenten angezeigten Adobe-Nameserver-Informationen und fügen Sie sie ein. Weitere Informationen zum Erstellen einer Subdomain in einer Hosting-Lösung finden Sie in diesem [Tutorial-Video](https://video.tv.adobe.com/v/30175?captions=ger).

   >[!IMPORTANT]
   >
   >Achten Sie beim Konfigurieren von Nameservern darauf, **Adobe nie Ihre Stamm-Subdomain zuzuweisen**. Andernfalls kann die Domain nur mit Adobe verwendet werden. Eine andere Verwendung ist dann nicht möglich, wie z. B. das Senden interner E-Mails an die Mitarbeiter Ihrer Organisation.
   >
   >Erstellen Sie **keine separate Zonendatei** für diese neue Subdomäne.

   ![](assets/subdomain4.png)

   Once the subdomain is created with the corresponding Adobe nameserver information, click **[!UICONTROL Next]**.

1. Wählen Sie den gewünschten Anwendungsfall für die Subdomain aus:

   * **Marketingnachrichten**: für kommerzielle Zwecke bestimmte Mitteilungen. Beispiel: Vertriebs-E-Mail-Kampagne.
   * **Transaktions- und Betriebsnachrichten**: Transaktionsnachrichten enthalten Informationen zum Abschluss eines Prozesses, den der Empfänger mit Ihnen gestartet hat. Beispiel: Kaufbestätigung, E-Mail zum Zurücksetzen des Passworts. Betriebliche Nachrichten beziehen sich auf den Austausch von Informationen, Ideen und Ansichten innerhalb und außerhalb der Organisation ohne kommerziellen Zweck.
   ![](assets/subdomain5.png)

   **Die Unterteilung Ihrer Subdomains nach Anwendungsfällen ist eine Best Practice für die Zustellbarkeit**. Dadurch wird die Reputation jeder Subdomain isoliert und geschützt. Wenn Ihre Subdomain für Marketingnachrichten beispielsweise von Internetdienstanbietern auf die Blacklist gesetzt wird, wird Ihre Subdomain für Transaktionsnachrichten nicht beeinträchtigt und kann weiterhin Nachrichten senden.

   **Sie können Subdomänen für Marketing- und Transaktionszwecke** delegieren:

   * Für Marketing-Anwendungsfälle werden Subdomänen auf **MID** -Instanzen (Mid Sourcing) konfiguriert.
   * Bei Transaktionen werden Subdomänen für ALLE **RT** -Instanzen (Message Center/Echtzeit-Nachrichten) konfiguriert, um die Konnektivität sicherzustellen. Die Subdomänen funktionieren daher mit allen RT-Instanzen.
   >[!NOTE]
   >
   >Wenn Sie Campaign Classic verwenden, können Sie in der Systemsteuerung sehen, welche RT/MID-Instanzen mit der Marketing-Instanz verbunden sind, mit der Sie arbeiten. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../instances-settings/using/instance-details.md).

1. Enter the subdomain that you created into your hosting solution, then click **[!UICONTROL Submit]**.

   Vergewissern Sie sich, dass Sie den **vollständigen Namen** der zuzuweisenden Subdomain eingeben. Um beispielsweise die Subdomain &quot;usoffer.email.weretail.com&quot; zuzuweisen, geben Sie &quot;usoffer.email.weretail.com&quot; ein.

   ![](assets/subdomain6.png)

1. Nachdem die Subdomain übermittelt wurde, prüft das Control Panel, ob sie korrekt auf Adobe-NS-Einträge verweist. Zusätzlich wird sichergestellt, dass für diese Subdomain kein SOA-Datensatz (Start of Authority) existiert.

1. Wenn die Prüfungen erfolgreich sind, beginnt das Control Panel mit der Einrichtung der Subdomain mit DNS-Einträgen, zusätzlichen URLs, Postfächern usw. You can get more details on the configuration progress by clicking the **[!UICONTROL Process details]** button.

   ![](assets/subdomain7.png)

   >[!NOTE]
   >
   >In einigen Fällen wird die Zuweisung durchgeführt, die Subdomain wird jedoch möglicherweise nicht erfolgreich verifiziert. The subdomain will go directly into the **[!UICONTROL Verified subdomains]** list with the **[!UICONTROL Unverified]** status and a job log providing information on the error. Wenden Sie sich an die Kundenunterstützung, wenn Sie Probleme bei der Lösung des Problems haben.
   >
   >Beachten Sie, dass während der Ausführung der Subdomain-Zuweisung andere Anfragen über das Control Panel in eine Warteschlange eingegeben und erst nach Abschluss der Subdomain-Zuweisung ausgeführt werden, um Leistungsprobleme zu vermeiden.

Am Ende des Prozesses werden die Subdomains für die Verwendung mit Ihrer Adobe Campaign-Instanz konfiguriert und die folgenden Elemente erstellt:

* **Die Subdomain** mit den folgenden **DNS-Einträgen**: SOA, MX, CNAME(s), DKIM, SPF, TXT,
* **Zusätzliche Subdomains** zum Hosten von Mirror-, Ressourcen- und Tracking-Seiten sowie von Domain-Schlüsseln,
* **Postfächer**: Absender, Fehler, Antwort.

>[!NOTE]
>
>Standardmäßig ist das „Antwort“-Postfach über das Control Panel so konfiguriert, dass E-Mails gelöscht werden, und kann nicht überprüft werden. Verwenden Sie diese Adresse nicht, wenn Sie Ihr „Antwort“-Postfach für Ihre Marketingkampagnen überwachen möchten.

You can get more details on the subdomain by clicking the **[!UICONTROL Subdomain details]** and **[!UICONTROL Sender info]** buttons.

![](assets/detail_buttons.png)

![](assets/subdomain_details.png)

![](assets/sender_info.png)

>[!IMPORTANT]
>
>Fragen Sie nach der Verarbeitungsphase bei der Adobe-Kundenunterstützung nach, ob eine Prüfanfrage für das Zustellbarkeits-Team eingereicht wurde, um die neu erstellte Subdomain zu überprüfen. Der Prüfvorgang kann drei bis zehn Werktage dauern, nachdem die Subdomain zugewiesen wurde.
>
>Die durchgeführten Überprüfungen umfassen das Testen von Feedback-Schleifen und Spam-Beschwerdeschleifen. Daher empfehlen wir nicht, die Subdomain vor Abschluss der Prüfung zu verwenden, da dies zu einer schlechten Reputation der Subdomain führen kann.

## Verwenden von CNAME {#use-cnames}

Die Verwendung von CNAME für die Subdomain-Zuweisung wird über das Control Panel nicht unterstützt. Kontaktieren Sie zur Verwendung dieser Methode die Adobe-Kundenunterstützung.

**Verwandte Themen:**

* [Zuweisen von Subdomains (Tutorial-Video)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [Subdomain-Branding](../../subdomains-certificates/using/subdomains-branding.md)
* [Überwachen von Subdomains](../../subdomains-certificates/using/monitoring-subdomains.md)