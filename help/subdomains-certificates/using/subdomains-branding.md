---
title: Subdomain-Branding
description: Weitere Informationen zum Branding von Subdomains
translation-type: tm+mt
source-git-commit: 17f51b60310b4fbc89e2106eb4ee9251fd525a59
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 80%

---


# Subdomain-Branding {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="Über Subdomains und SSL-Zertifikate"
>abstract="Überwachen Sie Ihre Subdomains und die zugehörigen SSL-Zertifikate."
>additional-url="https://docs.adobe.com/content/help/de-DE/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="Überwachen der SSL-Zertifikate Ihrer Subdomains"

>[!IMPORTANT]
>
>Die Subdomänenkonfiguration über die Systemsteuerung ist in der Beta-Version verfügbar und unterliegt häufigen Aktualisierungen und Änderungen ohne Vorankündigung.

## Warum sollten Sie Subdomains einrichten? {#why-setting-up-subdomains}

Sie können Ihre Domain in Subdomains unterteilen, um Ihre Marken oder unterschiedlichen Textsorten (Transaktionsnachrichten, Marketing-Informationen usw.) voreinander zu trennen.

Nehmen wir zum Beispiel die Domain &quot;mybrand.com&quot;, die sowohl Transaktions- als auch Marketing-Nachrichten sendet. In diesem Fall können Sie zwei Subdomains einrichten:

* die Subdomain &quot;info.mybrand.com&quot; für Ihre Transaktionsnachrichten (Kaufbestätigung, Passwortzurücksetzung usw.),
* die Subdomain &quot;marketing.mybrand.com&quot; für Ihre Werbe-E-Mails.

Dies hilft Ihnen, die Reputation Ihrer Domain und anderer Subdomains zu schützen. Wenn z. B. die Subdomains &quot;marketing.mybrand.com&quot; aufgrund schlechter Zustellbarkeit von Internetdienstanbietern auf die Blockierungsliste gesetzt werden, würde dies verhindern, dass die gesamte Domain &quot;mybrand.com&quot; und die Subdomain &quot;info.mybrand.com&quot; ebenfalls auf die Blockierungsliste gesetzt werden.

## Subdomänenkonfigurationsmethoden {#subdomain-delegation-methods}

Mit der Subdomänenkonfiguration können Sie einen Unterabschnitt Ihrer Domäne (technisch eine &quot;DNS-Zone&quot;) für die Verwendung mit Adobe Campaign konfigurieren. Verfügbare Einrichtungsmethoden sind:

* **Vollständige Subdomain-Zuweisung an Adobe Campaign** (empfohlen): Die Subdomain wird Adobe vollständig zugewiesen. Adobe kann Campaign als verwalteten Dienst bereitstellen, im Rahmen dessen alle DNS-Bereiche kontrolliert und gewartet werden, die für die Zustellung, das Rendern und das Tracking von E-Mail-Kampagnen erforderlich sind.

* **Verwendung von CNAMEs**: Erstellen Sie eine Subdomäne und verwenden Sie CNAMEs, um auf Adoben-spezifische Datensätze zu verweisen. Mit dieser Konfiguration sind Adobe und der Kunde gleichermaßen für die Wartung des DNS verantwortlich.

Die nachstehende Tabelle gibt einen Überblick über die Funktionsweise dieser Methoden sowie den damit verbundenen Aufwand:

| Konfigurationsmethode | Funktionsweise | Aufwand |
|---|---|---|
| **Vollständige Zuweisung** | Sie erstellen die Subdomain und den Namespace-Eintrag. Adobe konfiguriert dann alle für Adobe Campaign erforderlichen DNS-Einträge.<br/><br/>Bei dieser Konfiguration hat Adobe die volle Verantwortung für die Pflege der Subdomain und aller DNS-Einträge. | Niedrig |
| **CNAME, benutzerspezifische Methode** | Sie erstellen die Subdomain und den Namespace-Eintrag. Adobe stellt dann die Einträge bereit, die auf Ihren DNS-Servern abgelegt werden sollen, und konfiguriert die entsprechenden Werte in den Adobe Campaign-DNS-Servern.<br/><br/>Bei dieser Konfiguration sind Sie und Adobe gemeinsam für die Pflege des DNS verantwortlich. | Hoch |

Additional information on domain configuration is available in [this documentation](https://helpx.adobe.com/de/campaign/kb/domain-name-delegation.html).

Wenden Sie sich bei Fragen zu Subdomänenkonfigurationsmethoden an das Adobe Deliverability Team oder wenden Sie sich an den Kundendienst, um Beratung zur Lieferbarkeit anzufordern.

## Anwendungsfälle von Subdomänen (Campaign Classic) (#subdomains-use-case)

Beim Einrichten von Subdomänen für Campaign Classic-Instanzen müssen Sie den Anwendungsfall auswählen, für den die Subdomäne verwendet werden soll (siehe [](../../subdomains-certificates/using/setting-up-new-subdomain.md)).

Mögliche Anwendungsfälle sind:

* **Marketingnachrichten**: für kommerzielle Zwecke bestimmte Mitteilungen. Beispiel: Vertriebs-E-Mail-Kampagne.

* **Transaktions- und Betriebsnachrichten**: Transaktionsnachrichten enthalten Informationen zum Abschluss eines Prozesses, den der Empfänger mit Ihnen gestartet hat. Beispiel: Kaufbestätigung, E-Mail zum Zurücksetzen des Passworts. Betriebliche Nachrichten beziehen sich auf den Austausch von Informationen, Ideen und Ansichten innerhalb und außerhalb der Organisation ohne kommerziellen Zweck.

**Die Unterteilung Ihrer Subdomains nach Anwendungsfällen ist eine Best Practice für die Zustellbarkeit**. Dadurch wird die Reputation jeder Subdomain isoliert und geschützt. Wenn Ihre Subdomain für Marketing-Nachrichten beispielsweise von Internetdienstanbietern auf die Blockierungsliste gesetzt wird, wird Ihre Subdomain für Transaktionsnachrichten nicht beeinträchtigt und kann weiterhin Nachrichten senden.

**Sie können eine Subdomäne sowohl für Marketing- als auch für Transaktionszwecke** konfigurieren:

* Bei Marketing-Anwendungsfällen werden Subdomains in **MID**-Instanzen (Mid Sourcing) konfiguriert.
* Bei Transaktionsanwendungsfällen werden Subdomains in ALLEN **RT**-Instanzen (Message Center/Real Time Messaging) konfiguriert, um Konnektivität zu gewährleisten. Die Subdomains funktionieren daher mit allen RT-Instanzen.

>[!NOTE]
>
>Wenn Sie Campaign Classic verwenden, können Sie im Control Panel sehen, welche RT/MID-Instanzen mit der Marketing-Instanz verbunden sind, mit der Sie gerade arbeiten. Weitere Informationen hierzu finden Sie im Abschnitt [Details der Instanz](../../instances-settings/using/instance-details.md).

**Verwandte Themen:**

* [Einrichten einer neuen Subdomain](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [Lernvideo](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [Überwachen von Subdomains](../../subdomains-certificates/using/monitoring-subdomains.md)
