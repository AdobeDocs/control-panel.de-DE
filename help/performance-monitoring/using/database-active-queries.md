---
product: campaign
solution: Campaign
title: Überwachen aktiver Abfragen
description: Erfahren Sie, wie Sie aktive Abfragen auf Ihren Campaign-Instanzen im Control Panel überwachen.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 12e9326ba220776874654705587152bf3978949c
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 52%

---

# Überwachen aktiver Abfragen {#long-running-queries}

Im Bereich **[!UICONTROL Aktive Abfragen]** auf der Registerkarte **[!UICONTROL Datenbanken]** werden die fünf Abfragen aufgelistet, die schon am längsten auf der ausgewählten Instanz ausgeführt werden.

![](assets/active-queries.png)

Die Spalte **[!UICONTROL Dauer]** gibt an, wie lange eine Abfrage schon auf der Instanz ausgeführt wird. Die Dauer wird in folgendem Format angezeigt: `hh:mm:ss.ms`.

>[!IMPORTANT]
>
>Wenn eine der Abfragen länger als 24 Stunden aktiv ist, werden Sie per E-Mail benachrichtigt, wenn Sie sich für [E-Mail-Benachrichtigung](email-alerting.md).
>
>Wenden Sie sich in diesem Fall an die Kundenunterstützung , damit diese das Problem identifiziert und beheben kann. Sie müssen ihnen die Variable **[!UICONTROL PID]** column -Wert, der eine eindeutige Kennung für die Abfrage darstellt.
