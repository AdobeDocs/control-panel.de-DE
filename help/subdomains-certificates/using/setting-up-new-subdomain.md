---
title: Einrichten einer neuen Subdomain
description: Erfahren Sie, wie Sie eine neue Subdomain für Ihre Campaign-Instanz einrichten.
translation-type: tm+mt
source-git-commit: b27c6c8db765bc61b4e2afcadf446b28b15d3a93
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 94%

---


# Einrichten einer neuen Subdomain {#setting-up-subdomain}

>[!CONTEXTUALHELP]
>id="cp_subdomain_management"
>title="Einrichten neuer Subdomains und Verwalten von Zertifikaten"
>abstract="Sie müssen eine neue Subdomain einrichten und die SSL-Zertifikate Ihrer Subdomains verwalten, um mit Adobe Campaign E-Mails senden oder Landingpages veröffentlichen zu können."
>additional-url="https://docs.adobe.com/content/help/de-DE/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="Überwachen der SSL-Zertifikate Ihrer Subdomains"

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

1. Wählen Sie auf der Karte **[!UICONTROL Subdomains &amp; Zertifikate]** die gewünschte Produktionsinstanz und danach **[!UICONTROL Neue Subdomain einrichten]** aus.

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >Die Zuweisung von Subdomains ist nur für **Produktionsinstanzen** verfügbar.

1. Wählen Sie **[!UICONTROL Weiter]** aus, um die Methode der vollständigen Zuweisung zu bestätigen.

   ![](assets/subdomain3.png)

   >[!NOTE]
   >
   >[CNAME](#use-cnames) und benutzerdefinierte Methoden werden derzeit vom Control Panel nicht unterstützt.

1. Erstellen Sie die gewünschte Subdomain und die gewünschten Nameserver in der von Ihrem Unternehmen verwendeten Hosting-Lösung. Kopieren Sie dazu die im Assistenten angezeigten Adobe-Nameserver-Informationen und fügen Sie sie ein. Weitere Informationen zum Erstellen einer Subdomain in einer Hosting-Lösung finden Sie in diesem [Tutorial-Video](https://video.tv.adobe.com/v/30175?captions=ger).

   >[!IMPORTANT]
   >
   >Achten Sie beim Konfigurieren von Nameservern darauf, **Adobe nie Ihre Stamm-Subdomain zuzuweisen**. Andernfalls kann die Domain nur mit Adobe verwendet werden. Eine andere Verwendung ist dann nicht möglich, wie z. B. das Senden interner E-Mails an die Mitarbeiter Ihrer Organisation.
   >
   >Erstellen Sie außerdem **keine separate Zonendatei** für diese neue Subdomain.

   ![](assets/subdomain4.png)

   Nachdem die Subdomain mit den entsprechenden Adobe-Nameserver-Informationen erstellt wurde, wählen Sie **[!UICONTROL Weiter]** aus.

1. Wählen Sie den gewünschten Anwendungsfall für die Subdomain aus:

   * **Marketingnachrichten**: für kommerzielle Zwecke bestimmte Mitteilungen. Beispiel: Vertriebs-E-Mail-Kampagne.
   * **Transaktions- und Betriebsnachrichten**: Transaktionsnachrichten enthalten Informationen zum Abschluss eines Prozesses, den der Empfänger mit Ihnen gestartet hat. Beispiel: Kaufbestätigung, E-Mail zum Zurücksetzen des Passworts. Betriebliche Nachrichten beziehen sich auf den Austausch von Informationen, Ideen und Ansichten innerhalb und außerhalb der Organisation ohne kommerziellen Zweck.
   ![](assets/subdomain5.png)

   **Die Unterteilung Ihrer Subdomains nach Anwendungsfällen ist eine Best Practice für die Zustellbarkeit**. Dadurch wird die Reputation jeder Subdomain isoliert und geschützt. Wenn Ihre Subdomain für Marketing-Nachrichten beispielsweise von Internetdienstanbietern auf die Blacklist gesetzt wird, wird Ihre Subdomain für Transaktionsnachrichten nicht beeinträchtigt und kann weiterhin Nachrichten senden.

   **Sie können Subdomains für sowohl Marketing- als auch Transaktionsanwendungsfälle delegieren**:

   * Bei Marketing-Anwendungsfällen werden Subdomains in **MID**-Instanzen (Mid Sourcing) konfiguriert.
   * Bei Transaktionsanwendungsfällen werden Subdomains in ALLEN **RT**-Instanzen (Message Center/Real Time Messaging) konfiguriert, um Konnektivität zu gewährleisten. Die Subdomains funktionieren daher mit allen RT-Instanzen.
   >[!NOTE]
   >
   >Wenn Sie Campaign Classic verwenden, können Sie im Control Panel sehen, welche RT/MID-Instanzen mit der Marketing-Instanz verbunden sind, mit der Sie gerade arbeiten. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../instances-settings/using/instance-details.md).

1. Geben Sie die von Ihnen erstellte Subdomain in Ihre Hosting-Lösung ein und wählen Sie dann **[!UICONTROL Senden]** aus.

   Vergewissern Sie sich, dass Sie den **vollständigen Namen** der zuzuweisenden Subdomain eingeben. Um beispielsweise die Subdomain &quot;usoffer.email.weretail.com&quot; zuzuweisen, geben Sie &quot;usoffer.email.weretail.com&quot; ein.

   ![](assets/subdomain6.png)

1. Nachdem die Subdomain übermittelt wurde, prüft das Control Panel, ob sie korrekt auf Adobe-NS-Einträge verweist. Zusätzlich wird sichergestellt, dass für diese Subdomain kein SOA-Datensatz (Start of Authority) existiert.

   >[!NOTE]
   >
   >Beachten Sie, dass während der Ausführung der Subdomain-Zuweisung andere Anfragen über das Control Panel in eine Warteschlange eingegeben und erst nach Abschluss der Subdomain-Zuweisung ausgeführt werden, um Leistungsprobleme zu vermeiden.

1. Wenn die Prüfungen erfolgreich sind, beginnt das Control Panel mit der Einrichtung der Subdomain mit DNS-Einträgen, zusätzlichen URLs, Postfächern usw.

   Schließlich wird das Bereitstellbarkeitsteam über die neue Subdomäne informiert, um sie zu prüfen. Der Prüfungsprozess kann bis zu 3-10 Werktage nach der Übertragung der Subdomäne dauern. Die durchgeführten Überprüfungen umfassen das Testen von Feedback-Schleifen und Spam-Beschwerdeschleifen. Daher empfehlen wir nicht, die Subdomain vor Abschluss der Prüfung zu verwenden, da dies zu einer schlechten Reputation der Subdomain führen kann.

   Wählen Sie **[!UICONTROL Prozessdetails]** aus, um weitere Informationen zum Konfigurationsfortschritt zu erhalten.

   ![](assets/subdomain7.png)

   >[!NOTE]
   >
   >In einigen Fällen wird die Zuweisung durchgeführt, die Subdomain wird jedoch möglicherweise nicht erfolgreich verifiziert. Die Subdomäne bleibt mit einem Auftragsprotokoll, das Informationen zum Fehler enthält, in der Liste **[!UICONTROL Verarbeitung]** . Wenden Sie sich an die Kundenunterstützung, wenn Sie Probleme bei der Lösung des Problems haben.

Am Ende des Prozesses werden die Subdomains für die Verwendung mit Ihrer Adobe Campaign-Instanz konfiguriert und die folgenden Elemente erstellt:

* **Die Subdomain mit den folgenden DNS-Einträgen**: SOA, MX, CNAME(s), DKIM, SPF, TXT,
* **Zusätzliche Subdomains** zum Hosten von Mirror-, Ressourcen- und Tracking-Seiten sowie von Domain-Schlüsseln,
* **Postfächer**: Absender, Fehler, Antwort.

   Standardmäßig ist das „Antwort“-Postfach über das Control Panel so konfiguriert, dass E-Mails gelöscht werden, und kann nicht überprüft werden. Verwenden Sie diese Adresse nicht, wenn Sie Ihr „Antwort“-Postfach für Ihre Marketingkampagnen überwachen möchten.

Klicken Sie auf **[!UICONTROL Details der Subdomain]** und **[!UICONTROL Absenderdetails]**, um weitere Informationen zur Subdomain zu erhalten.

![](assets/detail_buttons.png)

![](assets/subdomain_details.png)

![](assets/sender_info.png)

## Verwenden von CNAME {#use-cnames}

Die Verwendung von CNAME für die Subdomain-Zuweisung wird über das Control Panel nicht unterstützt. Kontaktieren Sie zur Verwendung dieser Methode die Adobe-Kundenunterstützung.

**Verwandte Themen:**

* [Zuweisen von Subdomains (Tutorial-Video)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [Subdomain-Branding](../../subdomains-certificates/using/subdomains-branding.md)
* [Überwachen von Subdomains](../../subdomains-certificates/using/monitoring-subdomains.md)