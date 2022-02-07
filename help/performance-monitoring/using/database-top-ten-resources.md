---
product: campaign
solution: Campaign
title: Die zehn wichtigsten temporären Ressourcen
description: Erfahren Sie, wie Sie im Control Panel die zehn größten temporären Ressourcen überwachen, die durch Workflows und Sendungen in Ihrer Campaign-Datenbank generiert wurden.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 12e9326ba220776874654705587152bf3978949c
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 100%

---

# Die zehn wichtigsten temporären Ressourcen {#top-10}

Im Bereich **[!UICONTROL Die zehn wichtigsten temporären Ressourcen]** werden die 10 größten temporären Ressourcen aufgelistet, die durch Workflows und Sendungen generiert wurden.

Die Überwachung von Workflows und Sendungen, die große temporäre Ressourcen erzeugen, ist ein wichtiger Schritt zur Überwachung Ihrer Datenbank. Wenn eine temporäre Ressource zu viel Datenbankspeicherplatz beansprucht, prüfen Sie, ob dieser Workflow oder dieser Versand erforderlich ist, und navigieren Sie schließlich zu Ihrer Instanz, um sie zu stoppen.

>[!IMPORTANT]
>
>Es wird allgemein empfohlen, zu vermeiden, **mehr als 40 Spalten** nicht nativer Ressourcen zu haben.

![](assets/database-top10.png)

>[!NOTE]
>
>Wenn festgestellt wird, dass ein Workflow eine große Anzahl von Tabellenzahlen oder Datenbankgrößen aufweist, empfehlen wir, den Workflow zu überprüfen und zu untersuchen, warum so viele Daten generiert werden.
>
>Am Ende dieser Seite finden Sie auch Ressourcen für Campaign Standard und Campaign Classic, mit denen Sie eine Überlastung der Datenbank verhindern können.

Über **[!UICONTROL Alle anzeigen]** können Sie auf detaillierte Informationen zu diesen temporären Ressourcen zugreifen.

![](assets/database-top10-view.png)

Der Wert in der Spalte **[!UICONTROL Zwischenergebnisse behalten]** gibt an, ob die Option in Campaign aktiviert („1“) oder deaktiviert („0“) ist. Mit dieser Option können Sie die Ergebnisse der Transitionen zwischen den verschiedenen Aktivitäten eines Workflows speichern (siehe die Dokumentationen zu [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/executing-a-workflow/managing-execution-options.html?lang=de) und [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/introduction/workflow-best-practices.html?lang=de#logs)).

>[!IMPORTANT]
>
>Diese Option darf in einem Produktions-Workflow niemals aktiviert sein. Sie wird zur Analyse der Ergebnisse verwendet und ist nur für Testzwecke konzipiert und darf daher nur in Entwicklungs- oder Staging-Umgebungen verwendet werden.
>
>Wenn der Wert im Control Panel anzeigt, dass die Option für einen Ihrer Workflows aktiviert ist, empfehlen wir dringend, sie in Campaign zu deaktivieren.
