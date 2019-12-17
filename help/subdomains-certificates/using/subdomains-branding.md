---
title: Subdomänen-Branding
description: Weitere Informationen zum Branding von Subdomänen
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Subdomänen-Branding {#subdomains-branding}

## Warum Subdomänen einrichten? {#why-setting-up-subdomains}

Eine Subdomäne ist eine Division Ihrer Domäne, die verwendet werden kann, um Ihre Marken oder verschiedene Arten von Traffic (Transaktionsmeldungen, Marketinginformationen usw.) zu isolieren.

Nehmen wir das Beispiel der Domäne &quot;mybrand.com&quot;, die sowohl transaktionale als auch Marketing-Kommunikation sendet. In diesem Fall können Sie zwei Subdomänen einrichten:

* &quot;info.mybrand.com&quot;-Subdomäne für Ihre Transaktionsbenachrichtigung (Kaufbestätigung, Kennwortrücksetzung usw.),
* &quot;marketing.mybrand.com&quot;-Subdomäne für Ihre E-Mails zum Anzeigen.

Dadurch erhalten Sie den Ruf Ihrer Domäne und anderer Subdomänen. Wenn beispielsweise die Subdomänen &quot;marketing.mybrand.com&quot;aufgrund einer schlechten Zustellbarkeit auf der schwarzen Liste der Internetdienstanbieter standen, würde dies verhindern, dass die gesamte Domäne &quot;mybrand.com&quot;und die Unterdomäne &quot;info.mybrand.com&quot;auf die schwarze Liste gesetzt werden.

## Subdomänendelegationsmethoden {#subdomain-delegation-methods}

Mithilfe der Subdomänendelegation können Sie einen Unterabschnitt Ihrer Domäne (technisch eine &quot;DNS-Zone&quot;) für die Verwendung mit Adobe Campaign delegieren. Verfügbare Setupmethoden sind:

* **Vollständige Subdomänenübertragung an Adobe Campaign** (empfohlen): Die Subdomäne wird vollständig an Adobe delegiert. Adobe ist in der Lage, die Kampagne als verwalteten Dienst bereitzustellen, indem es alle Aspekte von DNS steuert und pflegt, die für die Bereitstellung, Wiedergabe und Verfolgung von E-Mail-Kampagnen erforderlich sind.

* **Verwendung von CNAMEs** (nicht empfohlen und nicht über die Systemsteuerung unterstützt): Erstellen Sie eine Subdomäne und verwenden Sie CNAMEs, um auf Adobe-spezifische Datensätze zu verweisen. Mit diesem Setup teilen sich Adobe und der Kunde die Verantwortung für die Verwaltung des DNS.

Die nachstehende Tabelle gibt einen Überblick über die Funktionsweise dieser Methoden sowie den damit verbundenen Aufwand:

| Delegationsmethode | Funktionsweise | Umfang des Aufwands |
|---|---|---|
| **Vollständige Delegation** | Erstellen Sie den Unterdomäne- und Namespace-Datensatz. Adobe konfiguriert dann alle für Adobe Campaign erforderlichen DNS-Datensätze.<br/><br/>Bei diesem Setup ist Adobe voll verantwortlich für die Verwaltung der Subdomäne und aller DNS-Datensätze. | Niedrig |
| **CNAME, benutzerspezifische Methode** | Erstellen Sie den Unterdomäne- und Namespace-Datensatz. Adobe stellt dann die Datensätze bereit, die auf Ihren DNS-Servern abgelegt werden sollen, und konfiguriert die entsprechenden Werte in den Adobe Campaign-DNS-Servern.<br/><br/>Bei diesem Setup sind Sie und Adobe gemeinsam für die Verwaltung von DNS verantwortlich. | Hoch |

Weitere Informationen zur Domänenübertragung finden Sie[in dieser Dokumentation](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).
