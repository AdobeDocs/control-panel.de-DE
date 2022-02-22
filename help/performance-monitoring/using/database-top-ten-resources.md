---
product: campaign
solution: Campaign
title: Die zehn wichtigsten temporären Ressourcen
description: Erfahren Sie, wie Sie im Control Panel die zehn größten temporären Ressourcen überwachen, die durch Workflows und Sendungen in Ihrer Campaign-Datenbank generiert wurden.
feature: Control Panel
role: Architect
level: Experienced
exl-id: 2fa2ffbb-102b-42c4-8feb-b0263ee9c930
source-git-commit: b17abddf6bad7e58cb7bd825cd97322427a0b21f
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 79%

---

# Die zehn wichtigsten temporären Ressourcen {#top-10}

Im Bereich **[!UICONTROL Die zehn wichtigsten temporären Ressourcen]** werden die 10 größten temporären Ressourcen aufgelistet, die durch Workflows und Sendungen generiert wurden.

Die Überwachung von Workflows und Sendungen, die große temporäre Ressourcen erzeugen, ist ein wichtiger Schritt zur Überwachung Ihrer Datenbank. Wenn eine temporäre Ressource zu viel Datenbankspeicherplatz beansprucht, prüfen Sie, ob dieser Workflow oder dieser Versand erforderlich ist, und navigieren Sie schließlich zu Ihrer Instanz, um sie zu stoppen.

>[!IMPORTANT]
>
>Es wird allgemein empfohlen, zu vermeiden, **mehr als 40 Spalten** nicht nativer Ressourcen zu haben. Wenn festgestellt wird, dass ein Workflow eine große Anzahl von Tabellenzahlen oder Datenbankgrößen aufweist, empfehlen wir, den Workflow zu überprüfen und zu untersuchen, warum so viele Daten generiert werden.
>
>Campaign Standard- und Classic-Richtlinien sind auch in [diese Seite](database-preventing-overload.md) um eine Überlastung der Datenbank zu verhindern.

![](assets/database-top10.png)

Die **[!UICONTROL Alle anzeigen]** -Schaltfläche können Sie auf die **[!UICONTROL Speicherübersicht]** Details, um detaillierte Informationen zu diesen temporären Ressourcen zu erhalten. Weitere Informationen hierzu finden Sie auf [dieser Seite](database-storage-overview.md).
