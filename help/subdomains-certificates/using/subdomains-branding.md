---
title: Subdomain-Branding
description: Weitere Informationen zum Branding von Subdomains
translation-type: ht
source-git-commit: 80b35e82116b064a7b141d957ab79ecfc9a99026
workflow-type: ht
source-wordcount: '467'
ht-degree: 100%

---


# Subdomain-Branding {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="Über Subdomains und SSL-Zertifikate"
>abstract="Überwachen Sie Ihre Subdomains und die zugehörigen SSL-Zertifikate."
>additional-url="https://docs.adobe.com/content/help/de-DE/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="Überwachen der SSL-Zertifikate Ihrer Subdomains"

>[!IMPORTANT]
>
>Die Subdomain-Zuweisung über das Control Panel befindet sich in der Beta-Phase und unterliegt häufigen Aktualisierungen und Änderungen ohne Vorankündigung.

## Warum sollten Sie Subdomains einrichten? {#why-setting-up-subdomains}

Sie können Ihre Domain in Subdomains unterteilen, um Ihre Marken oder unterschiedlichen Textsorten (Transaktionsnachrichten, Marketing-Informationen usw.) voreinander zu trennen.

Nehmen wir zum Beispiel die Domain &quot;mybrand.com&quot;, die sowohl Transaktions- als auch Marketing-Nachrichten sendet. In diesem Fall können Sie zwei Subdomains einrichten:

* die Subdomain &quot;info.mybrand.com&quot; für Ihre Transaktionsnachrichten (Kaufbestätigung, Passwortzurücksetzung usw.),
* die Subdomain &quot;marketing.mybrand.com&quot; für Ihre Werbe-E-Mails.

Dies hilft Ihnen, die Reputation Ihrer Domain und anderer Subdomains zu schützen. Wenn z. B. die Subdomains &quot;marketing.mybrand.com&quot; aufgrund schlechter Zustellbarkeit von Internetdienstanbietern auf die Blockierungsliste gesetzt werden, würde dies verhindern, dass die gesamte Domain &quot;mybrand.com&quot; und die Subdomain &quot;info.mybrand.com&quot; ebenfalls auf die Blockierungsliste gesetzt werden.

## Methoden der Subdomain-Zuweisung {#subdomain-delegation-methods}

Mithilfe der Subdomain-Zuweisung können Sie einen Teil Ihrer Domain (technisch eine &quot;DNS-Zone&quot;) Adobe Campaign zuweisen. Verfügbare Einrichtungsmethoden sind:

* **Vollständige Subdomain-Zuweisung an Adobe Campaign** (empfohlen): Die Subdomain wird Adobe vollständig zugewiesen. Adobe kann Campaign als verwalteten Dienst bereitstellen, im Rahmen dessen alle DNS-Bereiche kontrolliert und gewartet werden, die für die Zustellung, das Rendern und das Tracking von E-Mail-Kampagnen erforderlich sind.

* **Verwenden von CNAME** (nicht empfohlen und vom Control Panel nicht unterstützt): Erstellen Sie eine Subdomain und verwenden Sie CNAME, um auf Adobe-spezifische Einträge zu verweisen. Mit dieser Konfiguration sind Adobe und der Kunde gleichermaßen für die Wartung des DNS verantwortlich.

Die nachstehende Tabelle gibt einen Überblick über die Funktionsweise dieser Methoden sowie den damit verbundenen Aufwand:

| Zuweisungsmethode | Funktionsweise | Aufwand |
|---|---|---|
| **Vollständige Zuweisung** | Sie erstellen die Subdomain und den Namespace-Eintrag. Adobe konfiguriert dann alle für Adobe Campaign erforderlichen DNS-Einträge.<br/><br/>Bei dieser Konfiguration hat Adobe die volle Verantwortung für die Pflege der Subdomain und aller DNS-Einträge. | Niedrig |
| **CNAME, benutzerspezifische Methode** | Sie erstellen die Subdomain und den Namespace-Eintrag. Adobe stellt dann die Einträge bereit, die auf Ihren DNS-Servern abgelegt werden sollen, und konfiguriert die entsprechenden Werte in den Adobe Campaign-DNS-Servern.<br/><br/>Bei dieser Konfiguration sind Sie und Adobe gemeinsam für die Pflege des DNS verantwortlich. | Hoch |

Weitere Informationen zur Domain-Zuweisung finden Sie [in dieser Dokumentation](https://helpx.adobe.com/de/campaign/kb/domain-name-delegation.html).

Wenden Sie sich bei Fragen zu den Methoden der Subdomain-Zuweisung an das Zustellbarkeits-Team von Adobe oder an die Kundenunterstützung, um eine Beratung zu Fragen der Zustellbarkeit anzufordern.

**Verwandte Themen:**

* [Einrichten einer neuen Subdomain](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [Zuweisen von Subdomains (Tutorial-Video)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [Überwachen von Subdomains](../../subdomains-certificates/using/monitoring-subdomains.md)
