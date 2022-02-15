---
product: campaign
solution: Campaign
title: Überwachen aktiver Abfragen
description: Erfahren Sie, wie Sie aktive Abfragen auf Ihren Campaign-Instanzen im Control Panel überwachen.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 34af1000aeb444b273ade358eb35096bd3365fc7
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 100%

---

# Überwachen aktiver Abfragen {#long-running-queries}

Im Bereich **[!UICONTROL Aktive Abfragen]** auf der Registerkarte **[!UICONTROL Datenbanken]** werden die fünf Abfragen aufgelistet, die schon am längsten auf der ausgewählten Instanz ausgeführt werden.

![](assets/active-queries.png)

Die Spalte **[!UICONTROL Dauer]** gibt an, wie lange eine Abfrage schon auf der Instanz ausgeführt wird. Die Dauer wird in folgendem Format angezeigt: `hh:mm:ss.ms`.

>[!IMPORTANT]
>
>Wenn eine der Abfragen seit mehr als 24 Stunden aktiv ist, wenden Sie sich an die Kundenunterstützung, damit diese das Problem erkennt und behebt. In diesem Fall müssen Sie den Wert der Spalte **[!UICONTROL PID]** angeben, der eine eindeutige Kennung für die Abfrage darstellt.
