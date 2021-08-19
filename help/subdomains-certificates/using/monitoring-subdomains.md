---
product: campaign
solution: Campaign
title: Überwachen von SSL-Zertifikaten der Subdomains
description: Erfahren Sie, wie Sie die SSL-Zertifikate Ihrer Subdomains überwachen.
feature: Control Panel
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: 3bd3dcc0e09d887cab7d810d43f2c72bb4251ac9
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 94%

---

# Überwachen von Subdomains {#monitoring-subdomains}

>[!AVAILABILITY]
>
>Diese Funktion ist für Campaign v8 nicht verfügbar.

Sie müssen Ihre Subdomains unbedingt überwachen, um sicherzustellen, dass alle ordnungsgemäß für die Verwendung mit Adobe Campaign konfiguriert sind.

Die Liste der Subdomains für jede Ihrer Produktionsinstanzen ist direkt verfügbar, wenn Sie die Karte **[!UICONTROL Subdomains &amp; Zertifikate]** auswählen.

Die Spalte **[!UICONTROL Letzte Verifizierung]** gibt an, wann eine Subdomain zum letzten Mal verifiziert wurde. Sie können eine Verifizierung jederzeit starten, indem Sie die Schaltfläche **...** / **[!UICONTROL Subdomain verifizieren]** auswählen.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe rät von der Verwendung von Subdomains ohne Zertifikatsdatum ab, da diese Subdomains Probleme mit der Zustellbarkeit haben können.

Beim Starten einer Verifizierung werden mehrere Vorgänge ausgeführt, um zu überprüfen, ob die Subdomain korrekt konfiguriert ist (Prüfung des Instanzmandanten, E-Mail-Versand-Test usw.)

Wenn die Verifizierung der Subdomain fehlschlägt, wenden Sie sich für weitere Informationen an die Adobe-Kundenunterstützung.

**Verwandte Themen:**

* [Verlängern des SSL-Zertifikats einer Subdomain](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Subdomain-Branding](../../subdomains-certificates/using/subdomains-branding.md)
