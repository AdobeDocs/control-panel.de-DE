---
product: campaign
solution: Campaign
title: Speicherübersicht
description: Erfahren Sie, wie Sie im Control Panel die verschiedenen Campaign-Ressourcen überwachen, die in Ihren Instanzen Datenbankspeicherplatz belegen.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
TQID: 'https://experienceleague.adobe.com/3zcScy61C5LHsWM86WWWuy0uic-pdNQGKc0qY7ewwOQ'
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
source-wordcount: '180'
ht-degree: 100%
---
# Speicherübersicht {#storage-overview}

>[!CONTEXTUALHELP]
>id="cp_dbdetails_storagedetails"
>title="Über die Speicherübersicht"
>abstract="Auf dieser Registerkarte befinden sich detaillierte Informationen zu den verschiedenen Campaign-Ressourcen, die Datenbankspeicherplatz belegen."

Der Bereich **[!UICONTROL Speicherübersicht]** bietet eine grafische Darstellung des belegten Speicherplatzes durch:

* **[!UICONTROL Systemressourcen]**

  Wir empfehlen, sich an die Kundenunterstützung zu wenden, wenn die Systemressourcen einen großen Teil des Datenbankspeichers beanspruchen.

* **[!UICONTROL Native Tabellen]**, die standardmäßig mit den Campaign-Instanzen bereitgestellt werden,
* **[!UICONTROL Temporäre Tabellen]**, die von Workflows und Sendungen erstellt wurden,
* **[!UICONTROL Nicht native Tabellen]**, die nach der Erstellung benutzerdefinierter Ressourcen generiert wurden.

![](assets/database-storage-overview.png)

Klicken Sie auf **[!UICONTROL Details anzeigen]**, um weitere Informationen zu den verschiedenen Assets zu erhalten, die Datenbankspeicher belegen.

Sie können die Dropdown-Liste verwenden, um Ihre Suche zu verfeinern und nur Tabellen aus einem bestimmten Asset-Typ anzuzeigen (Workflows, Sendungen, Empfänger).

![](assets/database-storage-details.png)

Beachten Sie, dass Sie in diesem Bildschirm auch Workflow-Parameter überwachen können, die besondere Aufmerksamkeit erfordern, um Probleme in Ihren Instanzen zu vermeiden. Weitere Informationen finden Sie auf [dieser Seite](workflow-monitoring.md).
