---
product: campaign
solution: Campaign
title: Datenbanküberwachung
description: Erfahren Sie, wie Sie Ihre Campaign-Datenbank im Control Panel überwachen können
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: cca04cd965c00a9e2bc496de632ee41ce53a166a
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 87%

---

# Datenbanküberwachung {#database-monitoring}

## Über Datenbanken von Instanzen {#about-instances-databases}

Gemäß Ihrem Vertrag erhalten alle Ihre Campaign-Instanzen eine bestimmte Menge an Datenbankplatz.

Datenbanken beinhalten alle **Assets**, **Workflows** und **Daten**, die in Adobe Campaign gespeichert werden.

Im Laufe der Zeit können Datenbanken ihre maximale Kapazität erreichen, insbesondere wenn gespeicherte Ressourcen nie aus der Instanz gelöscht werden oder sich viele Workflows in angehaltenem Zustand befinden.

Ein Überlaufen der Datenbank einer Instanz kann zu verschiedenen Problemen führen (Anmeldung nicht möglich, Versand von E-Mails nicht möglich usw.). Daher ist für optimale Leistung eine Überwachung der Datenbanken Ihrer Instanzen unerlässlich.

>[!NOTE]
>
>Wenn die im Control Panel angegebene Menge an verfügbarem Datenbankspeicherplatz nicht der in Ihrem Vertrag angegebenen Menge entspricht, wenden Sie sich an die Kundenunterstützung.

## Überwachen der Datenbanknutzung {#monitoring-instances-database}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_database"
>title="Über die Datenbanküberwachung"
>abstract="Auf diesem Tab erhalten Sie Echtzeitinformationen über die aktuelle und historische Datenbanknutzung und -entwicklung für jede Ihrer Campaign-Instanzen."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=de" text="Über die Leistungsüberwachung"

![](assets/do-not-localize/how-to-video.png) Entdecken Sie diese Funktion im Video mit [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/performance-monitoring/monitoring-databases.html#performance-monitoring) oder [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/performance-monitoring/monitoring-databases.html#performance-monitoring).

Mit dem Control Panel können Sie die Datenbanknutzung für jede Ihrer Campaign-Instanzen überwachen. Öffnen Sie dazu die Karte **[!UICONTROL Leistungsüberwachung]** und wählen Sie dann den Tab **[!UICONTROL Datenbanken]** aus.

Wählen Sie die gewünschte Instanz aus der **[!UICONTROL Instanzenliste]** aus, um Informationen zur Datenbankkapazität und zum verwendeten Speicherplatz der Instanz anzuzeigen.

![](assets/databases_dashboard.png)

>[!NOTE]
>
>Beachten Sie, dass die Daten in diesem Dashboard basierend auf dem **[!UICONTROL technischen Workflow für die Datenbankbereinigung]** aktualisiert werden, der in Ihrer Campaign-Instanz ausgeführt wird (siehe die Dokumentationen zu [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) und [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html)).
>
>Zusätzlich können Sie Benachrichtigungen erhalten, wenn für eine Ihrer Datenbanken der Workflow unterhalb der Metriken **[!UICONTROL Verwendeter Speicherplatz]** und **[!UICONTROL Bereitgestellter Speicherplatz]** ausgeführt wurde. Wenn der Workflow seit mehr als drei Tagen nicht mehr ausgeführt wird, empfehlen wir, sich an die Adobe-Kundenunterstützung zu wenden, um zu untersuchen, warum der Workflow nicht ausgeführt wird.

In diesem Dashboard stehen zusätzliche Metriken (weiter unten erklärt) zur Verfügung, mit denen Sie die Verwendung der Datenbank der Instanz analysieren können.

### Datenbankauslastung {#database-utilization}

Der Bereich **[!UICONTROL Datenbankauslastung]** bietet eine grafische Darstellung der minimalen, durchschnittlichen und maximalen Datenbankauslastung über die letzten sieben Tage sowie des Schwellenwerts von 90 % Datenbankauslastung, gekennzeichnet durch eine rot gepunktete Kurve.

Um den Zeitraum zu ändern, verwenden Sie die Filter oben rechts im Diagramm.

Zur besseren Lesbarkeit können Sie auch eine oder mehrere Kurven im Diagramm hervorheben. Wählen Sie diese dazu aus der Legende **[!UICONTROL Aggregationstyp]** aus.

Bewegen Sie den Mauszeiger über das Diagramm, um weitere Informationen zu einem bestimmten Zeitraum anzuzeigen und Informationen über die zu diesem Zeitpunkt erfolgte Datenbanknutzung anzuzeigen.

![](assets/databases_dashboard_detail.png)

### Speicherübersicht {#storage-overview}

>[!CONTEXTUALHELP]
>id="cp_dbdetails_storagedetails"
>title="Über Speicherübersicht"
>abstract="Auf diesem Tab erhalten Sie detaillierte Informationen zu den verschiedenen Campaign-Ressourcen, die Datenbankspeicherplatz belegen."

Der Bereich **[!UICONTROL Speicherübersicht]** bietet eine grafische Darstellung des belegten Speicherplatzes durch:

* **[!UICONTROL Systemressourcen]**

   Wir empfehlen, sich an die Kundenunterstützung zu wenden, wenn die Systemressourcen einen großen Teil des Datenbankspeichers beanspruchen.

* **[!UICONTROL Native Tabellen]**, die standardmäßig mit den Campaign-Instanzen bereitgestellt werden,
* **[!UICONTROL Temporäre Tabellen]**, die von Workflows und Sendungen erstellt wurden,
* **[!UICONTROL Nicht native Tabellen]**, die nach der Erstellung benutzerdefinierter Ressourcen generiert wurden.

![](assets/database-storage-overview.png)

Klicken Sie auf **[!UICONTROL Details anzeigen]**, um weitere Informationen zu den verschiedenen Assets zu erhalten, die Datenbankspeicher belegen.

![](assets/database-storage-details.png)

Verwenden Sie den Filter, um die Suche zu verfeinern und Tabellen nur für einen bestimmten Asset-Typ anzuzeigen.

![](assets/database-storage-overview-filter.png)

### Die 10 wichtigsten temporären Ressourcen {#top-10}

Im Bereich **[!UICONTROL Die 10 wichtigsten temporären Ressourcen]** werden die 10 größten temporären Ressourcen aufgelistet, die durch Workflows und Sendungen generiert wurden.

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

Der Wert in der Spalte **[!UICONTROL Zwischenergebnisse behalten]** gibt an, ob die Option in Campaign aktiviert („1“) oder deaktiviert („0“) ist. Mit dieser Option können Sie die Ergebnisse der Transitionen zwischen den verschiedenen Aktivitäten eines Workflows speichern (siehe die Dokumentationen zu [Campaign Standard](://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/executing-a-workflow/managing-execution-options.html?lang=de) und [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/introduction/workflow-best-practices.html#logs)).

>[!IMPORTANT]
>
>Diese Option darf in einem Produktions-Workflow niemals aktiviert sein. Sie wird zur Analyse der Ergebnisse verwendet und ist nur für Testzwecke konzipiert und darf daher nur in Entwicklungs- oder Staging-Umgebungen verwendet werden.
>
>Wenn der Wert im Control Panel anzeigt, dass die Option für einen Ihrer Workflows aktiviert ist, empfehlen wir dringend, sie in Campaign zu deaktivieren.

## Verhindern einer Überbelegung von Datenbanken {#preventing-database-overload}

Campaign Standard und Classic bieten verschiedene Möglichkeiten, um eine Überbelegung von Speicherplatz in Datenbanken zu verhindern.

Im folgenden Abschnitt finden Sie nützliche Ressourcen aus Campaign-Dokumentationen, die Ihnen bei der Optimierung der Datenbanknutzung helfen:

**Workflow-Überwachung**

* [Workflow-Best Practices](://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.html?lang=de) (Campaign Standard)
* [Überwachung der Workflow-Ausführung](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html?lang=de) (Campaign Classic)

**Wartung der Datenbank**

* Technischer Workflow für die Datenbankbereinigung: [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) / [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html)
* [Handbuch zur Datenbankwartung](://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html?lang=de) (Campaign Classic)
* [Behebung von Problemen mit der Datenbankleistung](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/troubleshooting-toc/database-issues-toc/database-performances.html?lang=de) (Campaign Classic)
* [Datenbankbezogene Optionen](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html#database) (Campaign Classic)
* Datenaufbewahrung: [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/data-retention.html) / [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/configuring-campaign-classic/data-model/data-model-best-practices.html#data-retention)

>[!NOTE]
>
>Zusätzlich stehen Ihnen auch Benachrichtigungen zur Verfügung, die an Sie gesendet werden, wenn eine Ihrer Datenbanken ihre Kapazitätsgrenze erreicht. Abonnieren Sie dazu [Warnungen per E-Mail](../../performance-monitoring/using/email-alerting.md).
