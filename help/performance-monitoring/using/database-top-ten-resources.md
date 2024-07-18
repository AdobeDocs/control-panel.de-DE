---
product: campaign
solution: Campaign
title: Die zehn wichtigsten temporären Ressourcen
description: Erfahren Sie, wie Sie im Control Panel die zehn größten temporären Ressourcen überwachen, die durch Workflows und Sendungen in Ihrer Campaign-Datenbank generiert wurden.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: 2fa2ffbb-102b-42c4-8feb-b0263ee9c930
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 100%

---

# Die zehn wichtigsten temporären Ressourcen {#top-10}

Im Bereich **[!UICONTROL Die zehn wichtigsten temporären Ressourcen]** werden die 10 größten temporären Ressourcen aufgelistet, die durch Workflows und Sendungen generiert wurden.

Die Überwachung von Workflows und Sendungen, die große temporäre Ressourcen erzeugen, ist ein wichtiger Schritt zur Überwachung Ihrer Datenbank. Wenn eine temporäre Ressource zu viel Datenbankspeicherplatz beansprucht, prüfen Sie, ob dieser Workflow oder dieser Versand erforderlich ist, und navigieren Sie schließlich zu Ihrer Instanz, um sie zu stoppen.

>[!IMPORTANT]
>
>Es wird allgemein empfohlen zu vermeiden, **mehr als 40 Spalten** nicht vorkonfigurierter Ressourcen zu haben. Wenn ein Workflow eine große Anzahl von Tabellen oder eine hohe Datenbankgröße aufweist, empfehlen wir, den Workflow zu überprüfen, um herauszufinden, warum er so viele Daten erzeugt.
>
>Die Richtlinien für Campaign Standard und Classic sind auch auf [dieser Seite](database-preventing-overload.md) verfügbar. Sie helfen Ihnen, eine Überlastung der Datenbank zu vermeiden.

![](assets/database-top10.png)

Über die Schaltfläche **[!UICONTROL Alles anzeigen]** können Sie auf die Details der **[!UICONTROL Speicherübersicht]** zugreifen, um detaillierte Informationen zu diesen temporären Ressourcen zu erhalten. Weitere Informationen hierzu finden Sie auf [dieser Seite](database-storage-overview.md).
