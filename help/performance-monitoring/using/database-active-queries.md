---
product: campaign
solution: Campaign
title: Überwachen aktiver Abfragen
description: Erfahren Sie, wie Sie aktive Abfragen auf Ihren Campaign-Instanzen im Control Panel überwachen.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 12e9326ba220776874654705587152bf3978949c
workflow-type: ht
source-wordcount: '123'
ht-degree: 100%

---

# Überwachen aktiver Abfragen {#long-running-queries}

Im Bereich **[!UICONTROL Aktive Abfragen]** auf der Registerkarte **[!UICONTROL Datenbanken]** werden die fünf Abfragen aufgelistet, die schon am längsten auf der ausgewählten Instanz ausgeführt werden.

![](assets/active-queries.png)

Die Spalte **[!UICONTROL Dauer]** gibt an, wie lange eine Abfrage schon auf der Instanz ausgeführt wird. Die Dauer wird in folgendem Format angezeigt: `hh:mm:ss.ms`.

>[!IMPORTANT]
>
>Wenn eine der Abfragen schon länger als 24 Stunden aktiv ist, werden Sie per E-Mail benachrichtigt, wenn Sie [Benachrichtigungen per E-Mail](email-alerting.md) abonniert haben.
>
>Wenden Sie sich in diesem Fall an die Kundenunterstützung, damit diese das Problem identifizieren und beheben kann. In diesem Fall müssen Sie den Wert der Spalte **[!UICONTROL PID]** angeben, der eine eindeutige Kennung für die Abfrage darstellt.
