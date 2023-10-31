---
product: campaign
solution: Campaign
title: Überwachen von Subdomains
description: Überwachen Sie Ihre Subdomains, um sicherzustellen, dass sie alle ordnungsgemäß für die Verwendung mit Adobe Campaign konfiguriert sind.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '154'
ht-degree: 100%

---


# Überwachen Ihrer Subdomains {#monitoring-subdomains}

Sie müssen Ihre Subdomains unbedingt überwachen, um sicherzustellen, dass alle ordnungsgemäß für die Verwendung mit Adobe Campaign konfiguriert sind.

Die Liste der Subdomains für jede Ihrer Produktionsinstanzen ist direkt verfügbar, wenn Sie die Karte **[!UICONTROL Subdomains &amp; Zertifikate]** auswählen.

Die Spalte **[!UICONTROL Letzte Verifizierung]** gibt an, wann eine Subdomain zum letzten Mal verifiziert wurde. Sie können eine Verifizierung jederzeit starten, indem Sie die Schaltfläche **...** / **[!UICONTROL Subdomain verifizieren]** auswählen.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe rät von der Verwendung von Subdomains ohne Zertifikatsdatum ab, da diese Subdomains Probleme mit der Zustellbarkeit haben können.

Beim Starten einer Verifizierung werden mehrere Vorgänge ausgeführt, um zu überprüfen, ob die Subdomain korrekt konfiguriert ist (Prüfung des Instanzmandanten, E-Mail-Versand-Test usw.) Wenn die Verifizierung der Subdomain fehlschlägt, wenden Sie sich für weitere Informationen an die Adobe-Kundenunterstützung.

**Verwandte Themen:**

* [Verlängern des SSL-Zertifikats einer Subdomain](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Subdomain-Branding](../../subdomains-certificates/using/subdomains-branding.md)
