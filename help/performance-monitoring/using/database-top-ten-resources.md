---
product: campaign
solution: Campaign
title: Die zehn wichtigsten temporären Ressourcen
description: Erfahren Sie, wie Sie im Control Panel die zehn größten temporären Ressourcen überwachen, die durch Workflows und Sendungen in Ihrer Campaign-Datenbank generiert wurden.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: 2fa2ffbb-102b-42c4-8feb-b0263ee9c930
TQID: 'https://experienceleague.adobe.com/HeAm1BE6NkD-6rtbBXrHlJ-5KpgipvlH7UsHmPw2M-E'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: ae9127b0-c11d-467b-903d-a84cef43f6ed
    internal-label: Control Panel
  - id: c5474392-5419-4296-9e41-f6f4ce4f6e9b
    internal-label: Administration
subfeature_v2:
  - id: e519a22f-a06a-42fc-9d09-d78a3ab2c434
    internal-label: Monitoring guidelines
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: b2723b0683a305a992b710a37a3e47927e1fb65e
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
