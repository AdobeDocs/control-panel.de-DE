---
product: campaign
solution: Campaign
title: Überwachen aktiver Abfragen
description: Erfahren Sie, wie Sie aktive Abfragen auf Ihren Campaign-Instanzen im Control Panel überwachen.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: a1ea14f9-ec1d-4e10-89ef-846065512e8c
TQID: 'https://experienceleague.adobe.com/9lSAwCefSWAZ37fBHpu-1rUWppKTrnXcBSACJ3JthQg'
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
source-wordcount: '109'
ht-degree: 100%
---
# Überwachen aktiver Abfragen {#long-running-queries}

Im Bereich **[!UICONTROL Aktive Abfragen]** auf der Registerkarte **[!UICONTROL Datenbanken]** werden die fünf Abfragen aufgelistet, die schon am längsten auf der ausgewählten Instanz ausgeführt werden.

![](assets/active-queries.png)

Die Spalte **[!UICONTROL Dauer]** gibt an, wie lange eine Abfrage schon auf der Instanz ausgeführt wird. Die Dauer wird in folgendem Format angezeigt: `hh:mm:ss.ms`.

>[!IMPORTANT]
>
>Wenn eine der Abfragen seit mehr als 24 Stunden aktiv ist, wenden Sie sich an die Kundenunterstützung, damit diese das Problem erkennt und behebt. Sie müssen dabei den Wert in der Spalte **[!UICONTROL PID]** angeben, der eine eindeutige Kennung für die Abfrage ist.
