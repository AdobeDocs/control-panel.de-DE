---
product: campaign
solution: Campaign
title: Subdomain-Branding
description: Weitere Informationen zum Branding von Subdomains
feature: Control Panel
role: Architect
level: Intermediate
exl-id: a489d051-fb95-45cf-bb6d-33aef10b7795
source-git-commit: f1f6388bd32927cb13359f8975748ca4a158e660
workflow-type: ht
source-wordcount: '729'
ht-degree: 100%

---

# Subdomain-Branding {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="Über Subdomains und SSL-Zertifikate"
>abstract="Überwachen Sie Ihre Subdomains und die zugehörigen SSL-Zertifikate."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html?lang=de" text="Überwachen von SSL-Zertifikaten"

## Warum sollten Sie Subdomains einrichten? {#why-setting-up-subdomains}

Sie können Ihre Domain in Subdomains unterteilen, um Ihre Marken oder unterschiedlichen Textsorten (Transaktionsnachrichten, Marketing-Informationen usw.) voreinander zu trennen.

Nehmen wir zum Beispiel die Domain &quot;mybrand.com&quot;, die sowohl Transaktions- als auch Marketing-Nachrichten sendet. In diesem Fall können Sie zwei Subdomains einrichten:

* die Subdomain &quot;info.mybrand.com&quot; für Ihre Transaktionsnachrichten (Kaufbestätigung, Passwortzurücksetzung usw.),
* die Subdomain &quot;marketing.mybrand.com&quot; für Ihre Werbe-E-Mails.

Dies hilft Ihnen, die Reputation Ihrer Domain und anderer Subdomains zu schützen. Wenn z. B. die Subdomain &quot;marketing.mybrand.com&quot; aufgrund schlechter Zustellbarkeit von Internetdienstanbietern auf die Blockierungsliste gesetzt wird, würde dies verhindern, dass die gesamte Domain &quot;mybrand.com&quot; und die Subdomain &quot;info.mybrand.com&quot; ebenfalls auf die Blockierungsliste gesetzt werden.

## Methoden der Subdomain-Konfiguration {#subdomain-delegation-methods}

Mithilfe der Subdomain-Konfiguration können Sie einen Teil Ihrer Domain (technisch eine „DNS-Zone“) für die Verwendung mit Adobe Campaign konfigurieren. Verfügbare Einrichtungsmethoden sind:

* **Vollständige Subdomain-Zuweisung an Adobe Campaign** (empfohlen): Die Subdomain wird Adobe vollständig zugewiesen. Adobe kann Campaign als verwalteten Dienst bereitstellen, im Rahmen dessen alle DNS-Bereiche kontrolliert und gewartet werden, die für die Zustellung, die korrekte Darstellung und das Tracking von E-Mail-Kampagnen erforderlich sind.

* **Verwenden von CNAME**: Erstellen Sie eine Subdomain und verwenden Sie CNAME, um auf Adobe-spezifische Einträge zu verweisen. Mit dieser Konfiguration sind Adobe und der Kunde gleichermaßen für die Wartung des DNS verantwortlich.

Die nachstehende Tabelle gibt einen Überblick über die Funktionsweise dieser Methoden sowie den damit verbundenen Aufwand:

| Konfigurationsmethode | Funktionsweise | Aufwand |
|---|---|---|
| **Vollständige Zuweisung** | Sie erstellen die Subdomain und den Namespace-Eintrag. Adobe konfiguriert dann alle für Adobe Campaign erforderlichen DNS-Einträge.<br/><br/>Bei dieser Konfiguration hat Adobe die volle Verantwortung für die Pflege der Subdomain und aller DNS-Einträge. | Niedrig |
| **CNAME, benutzerspezifische Methode** | Sie erstellen die Subdomain und den Namespace-Eintrag. Adobe stellt dann die Einträge bereit, die auf Ihren DNS-Servern abgelegt werden sollen, und konfiguriert die entsprechenden Werte in den Adobe Campaign-DNS-Servern.<br/><br/>Bei dieser Konfiguration sind Sie und Adobe gemeinsam für die Pflege des DNS verantwortlich. | Hoch |

Weitere Informationen zur Domain-Konfiguration finden Sie in [dieser Dokumentation](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=de).

Wenden Sie sich bei Fragen zu den Methoden der Subdomain-Konfiguration an das Zustellbarkeitsteam von Adobe oder an die Kundenunterstützung, um eine Beratung zu Fragen der Zustellbarkeit anzufordern.

## Anwendungsfälle von Subdomains (Campaign v7/v8){#subdomains-use-cases}

>[!CONTEXTUALHELP]
>id="cp_add_subdomain_usecase_selection"
>title="Anwendungsfall für Ihre Subdomain auswählen"
>abstract="Die Unterteilung Ihrer Subdomains nach Anwendungsfällen ist eine Best Practice für die Zustellbarkeit. Dadurch wird die Reputation jeder Subdomain isoliert und geschützt."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=de" text="Einrichten einer neuen Subdomain"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/subdomains-branding.html?lang=de" text="Subdomain-Branding"

Beim Einrichten von Subdomains für Campaign v7/v8-Instanzen müssen Sie den Anwendungsfall auswählen, für den die Subdomain verwendet werden soll (siehe [Einrichten einer neuen Subdomain](../../subdomains-certificates/using/setting-up-new-subdomain.md)).

Mögliche Anwendungsfälle sind:

* **Marketingnachrichten**: für kommerzielle Zwecke bestimmte Mitteilungen. Beispiel: Vertriebs-E-Mail-Kampagne.

* **Transaktions- und Betriebsnachrichten**: Transaktionsnachrichten enthalten Informationen zum Abschluss eines Prozesses, den der Empfänger mit Ihnen gestartet hat. Beispiel: Kaufbestätigung, E-Mail zum Zurücksetzen des Passworts. Betriebliche Nachrichten beziehen sich auf den Austausch von Informationen, Ideen und Ansichten innerhalb und außerhalb der Organisation ohne kommerziellen Zweck.

**Die Unterteilung Ihrer Subdomains nach Anwendungsfällen ist eine Best Practice für die Zustellbarkeit**. Dadurch wird die Reputation jeder Subdomain isoliert und geschützt. Wenn Ihre Subdomain für Marketing-Nachrichten beispielsweise von Internetdienstanbietern auf die Blockierungsliste gesetzt wird, wird Ihre Subdomain für Transaktionsnachrichten nicht beeinträchtigt und kann weiterhin Nachrichten senden.

**Sie können Subdomains für sowohl Marketing- als auch Transaktionsanwendungsfälle konfigurieren**:

* Bei Marketing-Anwendungsfällen werden Subdomains in **MID**-Instanzen (Mid Sourcing) konfiguriert.
* Bei Transaktionsanwendungsfällen werden Subdomains in ALLEN **RT**-Instanzen (Message Center/Real Time Messaging) konfiguriert, um Konnektivität zu gewährleisten. Die Subdomains funktionieren daher mit allen RT-Instanzen.

>[!NOTE]
>
>Wenn Sie Campaign v7/v8 verwenden, können Sie im Control Panel sehen, welche RT/MID-Instanzen mit der Marketing-Instanz verbunden sind, mit der Sie gerade arbeiten. Weitere Informationen hierzu finden Sie im Abschnitt [Details der Instanz](../../instances-settings/using/instance-details.md).

**Verwandte Themen:**

* [Einrichten einer neuen Subdomain](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [Überwachen von Subdomains](../../subdomains-certificates/using/monitoring-subdomains.md)
