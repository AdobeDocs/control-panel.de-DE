---
title: Grundlagen zu Subdomänen
description: Weitere Informationen zu Subdomänen
translation-type: tm+mt
source-git-commit: c2ef995d49118943bdd77e6d3c14ef7ec643e672

---


# Über Subdomäne {#about-subdomains}

## Warum Subdomänen einrichten? {#why-setting-up-subdomains}

Eine Subdomäne ist eine Division Ihrer Domäne, die zur Isolierung verschiedener Traffic-Typen (Unternehmens-, Marketing-Informationen usw.) verwendet werden kann.

Nehmen wir das Beispiel der Domäne &quot;mybrand.com&quot;, die sowohl Informations- als auch Marketingkommunikation sendet:

* info.mybrand.com für interne Kommunikation
* marketing.mybrand.com für Ihre Prospekt-E-Mails.

In diesem Fall können Sie die Subdomäne &quot;marketing.mybrand.com&quot;an Adobe Campaign delegieren. Dadurch erhalten Sie den Ruf Ihrer Domäne und anderer Subdomänen. Wenn beispielsweise die Subdomänen &quot;marketing.mybrand.com&quot;aufgrund einer schlechten Zustellbarkeit auf der schwarzen Liste der Internetdienstanbieter standen, würde dies verhindern, dass die gesamte Domäne &quot;mybrand.com&quot;und &quot;info.mybrand.com&quot;blockiert wird.

## Subdomänendelegationsmethoden {#subdomain-delegation-methods}

Mithilfe der Subdomänendelegation können Sie einen Unterabschnitt Ihrer Domäne (technisch eine &quot;DNS-Zone&quot;) für die Verwendung mit Adobe Campaign delegieren. Verfügbare Setupmethoden sind:

* **Vollständige Subdomänenübertragung an Adobe Campaign** (empfohlen)

   Die Subdomäne wird vollständig an Adobe delegiert. Adobe ist in der Lage, die Kampagne als verwalteten Dienst bereitzustellen, indem es alle Aspekte von DNS steuert und pflegt, die für die Bereitstellung, Wiedergabe und Verfolgung von E-Mail-Kampagnen erforderlich sind.

* **Verwendung von CNAMEs** (nicht empfohlen und nicht in der Systemsteuerung unterstützt):

   Erstellen Sie eine Subdomäne und verwenden Sie CNAMEs, um auf Adobe-spezifische Datensätze zu verweisen. Mit diesem Setup teilen sich Adobe und der Kunde die Verantwortung für die Verwaltung des DNS.

Weitere Informationen zu diesen Methoden (implizite Verantwortung, Anforderungen usw.) finden Sie in [dieser Dokumentation](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).
