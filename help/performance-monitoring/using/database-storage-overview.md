---
product: campaign
solution: Campaign
title: Speicherübersicht
description: Erfahren Sie, wie Sie im Control Panel die verschiedenen Campaign-Ressourcen überwachen, die in Ihren Instanzen Datenbankspeicherplatz belegen.
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: c52094b8145bdd84aa9e71430a811b8a7b32354d
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 74%

---

# Speicherübersicht {#storage-overview}

>[!CONTEXTUALHELP]
>id="cp_dbdetails_storagedetails"
>title="Über die Speicherübersicht"
>abstract="Auf dieser Registerkarte erhalten Sie detaillierte Informationen zu den verschiedenen Campaign-Ressourcen, die Datenbankspeicherplatz belegen."

Der Bereich **[!UICONTROL Speicherübersicht]** bietet eine grafische Darstellung des belegten Speicherplatzes durch:

* **[!UICONTROL Systemressourcen]**

   Wir empfehlen, sich an die Kundenunterstützung zu wenden, wenn die Systemressourcen einen großen Teil des Datenbankspeichers beanspruchen.

* **[!UICONTROL Native Tabellen]**, die standardmäßig mit den Campaign-Instanzen bereitgestellt werden,
* **[!UICONTROL Temporäre Tabellen]**, die von Workflows und Sendungen erstellt wurden,
* **[!UICONTROL Nicht native Tabellen]**, die nach der Erstellung benutzerdefinierter Ressourcen generiert wurden.

![](assets/database-storage-overview.png)

Klicken Sie auf **[!UICONTROL Details anzeigen]**, um weitere Informationen zu den verschiedenen Assets zu erhalten, die Datenbankspeicher belegen.

Sie können die Dropdown-Liste verwenden, um Ihre Suche zu verfeinern und Tabellen nur aus einem bestimmten Asset-Typ anzuzeigen (Workflows, Sendungen, Empfänger).

![](assets/database-storage-details.png)

Beachten Sie, dass Sie in diesem Bildschirm auch Workflow-Parameter überwachen können, die besondere Aufmerksamkeit erfordern, um Probleme in Ihren Instanzen zu vermeiden. Weiterführende Informationen finden Sie auf [dieser Seite](workflow-monitoring.md).
