---
title: Datenbanküberwachung
description: Erfahren Sie, wie Sie Ihre Campaign-Datenbank im Control Panel überwachen können
translation-type: ht
source-git-commit: b2447b30314f4bd46b2b6e144f7f713ff2f1ec59
workflow-type: ht
source-wordcount: '450'
ht-degree: 100%

---


# Datenbanküberwachung {#database-monitoring}

## Über Datenbanken von Instanzen {#about-instances-databases}

Gemäß Ihrem Vertrag erhalten alle Ihre Campaign-Instanzen eine bestimmte Menge an Datenbankplatz.

Datenbanken beinhalten alle **Assets**, **Workflows** und **Daten**, die in Adobe Campaign gespeichert werden.

Im Laufe der Zeit können Datenbanken ihre maximale Kapazität erreichen, insbesondere wenn gespeicherte Ressourcen nie aus der Instanz gelöscht werden oder sich viele Workflows in angehaltenem Zustand befinden.

Ein Überlaufen der Datenbank einer Instanz kann zu verschiedenen Problemen führen (Anmeldung nicht möglich, Versand von E-Mails nicht möglich usw.). Daher ist für optimale Leistung eine Überwachung der Datenbanken Ihrer Instanzen unerlässlich.

>[!NOTE]
>
>Die im Control Panel angezeigte Menge an Datenbankspeicherplatz entspricht möglicherweise nicht der in Ihrem Vertrag angegebenen Menge an Datenbankspeicherplatz. In den meisten Fällen wird Ihnen vorübergehend ein größerer Datenbankspeicherplatz zur Verfügung gestellt, um die Leistung Ihres Systems sicherzustellen.

## Überwachen der Datenbanknutzung {#monitoring-instances-database}

Mit dem Control Panel können Sie die Datenbanknutzung für jede Ihrer Campaign-Instanzen überwachen. Gehen Sie dazu wie folgt vor:

1. Öffnen Sie die Karte **[!UICONTROL Leistungsüberwachung]** und wählen Sie dann den Tab **[!UICONTROL Datenbanken]** aus.

1. Wählen Sie die gewünschte Instanz aus der **[!UICONTROL Instanzenliste]** aus.

   Der obere Bereich enthält Informationen zur Datenbankkapazität der Instanz sowie zum verwendeten Speicherplatz.

   ![](assets/databases_dashboard.png)

   Der untere Bereich bietet eine grafische Darstellung der minimalen, durchschnittlichen und maximalen Datenbankauslastung über die letzten sieben Tage sowie des Schwellenwerts von 90 % Datenbankauslastung, gekennzeichnet durch eine rot gepunktete Kurve.

   Sie können den angezeigten Zeitraum mithilfe der oben rechts verfügbaren Filter ändern.

   Zur besseren Lesbarkeit können Sie auch eine oder mehrere Kurven im Diagramm hervorheben. Wählen Sie diese dazu aus der Legende **[!UICONTROL Aggregationstyp]** aus.

   Wenn Sie den Mauszeiger über das Diagramm bewegen, erhalten Sie genaue Informationen zum ausgewählten Zeitraum.

   ![](assets/databases_dashboard_detail.png)

>[!NOTE]
>
>Zusätzlich zu diesem Dashboard stehen Ihnen auch Benachrichtigungen zur Verfügung, die an Sie gesendet werden, wenn eine Ihrer Datenbanken ihre Kapazitätsgrenze erreicht. Abonnieren Sie dazu [Warnungen per E-Mail](../../performance-monitoring/using/email-alerting.md).

## Verhindern einer Überbelegung von Datenbanken {#preventing-database-overload}

Campaign Standard und Classic bieten verschiedene Möglichkeiten, um eine Überbelegung von Speicherplatz in Datenbanken zu verhindern.

Im folgenden Abschnitt finden Sie nützliche Ressourcen aus Campaign-Dokumentationen, die Ihnen bei der Optimierung der Datenbanknutzung helfen:

**Workflow-Überwachung**

* [Workflow-Best Practices](https://docs.adobe.com/content/help/de-DE/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.htmls) (Campaign Standard)
* [Überwachung der Workflow-Ausführung](https://docs.adobe.com/help/de-DE/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html) (Campaign Classic)

**Wartung der Datenbank**

* Technischer Workflow für die Datenbankbereinigung ([Campaign Standard](https://docs.adobe.com/help/de-DE/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) / [Campaign Classic](https://docs.adobe.com/help/de-DE/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html))
* [Handbuch zur Datenbankwartung](https://docs.adobe.com/content/help/de-DE/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html) (Campaign Classic)
* [Behebung von Problemen mit der Datenbankleistung](https://docs.adobe.com/content/help/de-DE/campaign-classic/using/monitoring-campaign-classic/troubleshooting/database-performances.html) (Campaign Classic)
* [Datenbankbezogene Optionen](https://docs.adobe.com/help/de-DE/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html#database) (Campaign Classic)
