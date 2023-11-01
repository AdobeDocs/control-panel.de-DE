---
product: campaign
solution: Campaign
title: Delegieren von SSL-Zertifikaten von Subdomains an Adobe
description: Erfahren Sie, wie Sie die SSL-Zertifikate Ihrer Subdomains an Adobe delegieren
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: a2b3d409-704b-4e81-ae40-b734f755b598
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 100%

---

# Delegieren von SSL-Zertifikaten von Subdomains an Adobe {#delegate-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_managed_ssl"
>title="Delegieren von SSL-Zertifikaten von Subdomains an Adobe"
>abstract="Mit dem Control Panel können Sie die SSL-Zertifikate Ihrer Subdomains von Adobe verwalten lassen. Wenn Sie CNAMEs zum Einrichten Ihrer Subdomain verwenden, werden automatisch Zertifikatdatensätze generiert und bereitgestellt, um ein Zertifikat in Ihrer Domain-Hosting-Lösung zu generieren."

Es wird dringend empfohlen, die Verwaltung der SSL-Zertifikate Ihrer Subdomains an Adobe zu delegieren, da Adobe das Zertifikat automatisch ausstellt und jedes Jahr vor Ablauf erneuert.

Wenn Sie CNAMEs zum Einrichten einer Subdomain-Delegierung verwenden, stellt Adobe Zertifikatdatensätze bereit, die in Ihrer Domain-Hosting-Lösung zum Generieren Ihres Zertifikats verwendet werden.

Die Delegierung von SSL-Zertifikaten an Adobe kann beim Einrichten einer neuen Subdomain oder für bereits delegierte Subdomains durchgeführt werden.

>[!NOTE]
>
>Adobe Managed SSL ist eine kostenlose Funktion, die Benutzenden gebührenfrei zur Verfügung steht. Das Delegieren des Zertifikats einer Subdomain an Adobe ist transparent und hat keinen Einfluss auf Ihre Kampagnen und die Zustellbarkeit. [Erfahren Sie mehr über die Verwaltung von SSL-Zertifikaten](monitoring-ssl-certificates.md#management)


## Delegieren von SSL-Zertifikaten neuer Subdomains {#new}

Um SSL-Zertifikate beim Einrichten einer neuen Subdomain zu delegieren, aktivieren Sie die Option **[!UICONTROL Für von Adobe verwaltetes SSL für Subdomains registrieren]** im Konfigurationsassistenten für Subdomains. Zertifikatsdatensätze, die in Ihre Hosting-Lösung kopiert werden sollen, werden später im Konfigurationsassistenten bereitgestellt. Detaillierte Schritte sind in [diesem Abschnitt](setting-up-new-subdomain.md) dokumentiert.

![](assets/cname-adobe-managed.png){width="70%" align="left"}

## Delegieren von SSL-Zertifikaten für bereits delegierte Subdomains {#delegated}

Um SSL-Zertifikate für eine bereits delegierte Subdomain zu delegieren, klicken Sie auf die Ellipsen-Schaltfläche neben der gewünschten Subdomain und klicken Sie auf **[!UICONTROL Zu verwaltetem SSL wechseln]**.

![](assets/delegate-ssl-list.png){width="70%" align="left"}

Es wird ein Dialogfeld mit den Zertifikatsdatensätzen angezeigt, die automatisch von Adobe generiert wurden. Kopieren Sie diese Einträge entweder einzeln oder durch Herunterladen einer CSV-Datei, und navigieren Sie dann zu Ihrer Domain-Hosting-Lösung, um die passenden Zertifikate zu generieren.

Stellen Sie sicher, dass alle Zertifikate aus den vorherigen Schritten in Ihrer Domain-Hosting-Lösung generiert wurden. Wenn alles ordnungsgemäß konfiguriert ist, bestätigen Sie die Erstellung der Datensätze und klicken Sie auf **[!UICONTROL Senden]**.

![](assets/delegate-ssl.png){width="70%" align="left"}
