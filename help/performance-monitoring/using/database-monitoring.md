---
title: Datenbanküberwachung
description: Erfahren Sie, wie Sie Ihre Campaign-Datenbank im Control Panel überwachen können
translation-type: tm+mt
source-git-commit: 77165e3f408f75dfb57434111b07b20ad9caab5e

---


# Datenbanküberwachung {#database-monitoring}

>[!IMPORTANT]
>
>Die Datenbanküberwachung über die Systemsteuerung wird Ende April verfügbar sein.

## Über Datenbanken von Instanzen {#about-instances-databases}

Gemäß Ihrem Vertrag erhalten alle Ihre Campaign-Instanzen eine bestimmte Menge an Datenbankplatz.

Datenbanken beinhalten alle **Assets**, **Workflows** und **Daten**, die in Adobe Campaign gespeichert werden.

Im Laufe der Zeit können Datenbanken ihre maximale Kapazität erreichen, insbesondere wenn gespeicherte Ressourcen nie aus der Instanz gelöscht werden oder sich viele Workflows in angehaltenem Zustand befinden.

Ein Überlaufen der Datenbank einer Instanz kann zu verschiedenen Problemen führen (Anmeldung nicht möglich, Versand von E-Mails nicht möglich usw.). Daher ist für optimale Leistung eine Überwachung der Datenbanken Ihrer Instanzen unerlässlich.

>[!NOTE]
>
>Der in der Systemsteuerung angezeigte Speicherplatz in der Datenbank spiegelt möglicherweise nicht die in Ihrem Vertrag angegebene Menge an Datenbankspeicherplatz wider. In den meisten Fällen wird Ihnen vorübergehend ein größerer Datenbankraum zur Verfügung gestellt, um die Leistung Ihres Systems sicherzustellen.

## Überwachen der Datenbanknutzung {#monitoring-instances-database}

Über die Systemsteuerung können Sie die Datenbanknutzung für jede Ihrer Instanzen der Kampagne überwachen. Gehen Sie dazu wie folgt vor:

1. Öffnen Sie die **[!UICONTROL Performance Monitoring]** Karte und wählen Sie die **[!UICONTROL Databases]** Registerkarte aus.

1. Select the desired instance from the **[!UICONTROL Instance List]**.

   Der obere Bereich enthält Informationen zur Datenbankkapazität der Instanz sowie zum verwendeten Speicherplatz.

   ![](assets/databases_dashboard.png)

   Der untere Bereich bietet eine grafische Darstellung der minimalen, durchschnittlichen und maximalen Datenbankauslastung während der letzten 7 Tage sowie der 90%igen Datenbankauslastungsschwelle, dargestellt durch eine rote Punktkurve.

   Sie können den angezeigten Zeitraum mithilfe der oben rechts verfügbaren Filter ändern.

   Zur besseren Lesbarkeit können Sie auch eine oder mehrere Kurven im Diagramm hervorheben. Wählen Sie dazu aus der **[!UICONTROL Aggregation Type]** Legende aus.

   Wenn Sie den Mauszeiger über das Diagramm bewegen, erhalten Sie genaue Informationen zum ausgewählten Zeitraum.

   ![](assets/databases_dashboard_detail.png)

>[!NOTE]
>
>Zusätzlich zu diesem Dashboard können Sie Benachrichtigungen erhalten, wenn eine Ihrer Datenbanken ihre Kapazität erreicht. Um dies zu tun, abonnieren Sie [E-Mail-Warnungen](../../performance-monitoring/using/email-alerting.md)

## Verhindern einer Überbelegung von Datenbanken {#preventing-database-overload}

Campaign Standard und Classic bieten verschiedene Möglichkeiten, um eine Überbelegung von Speicherplatz in Datenbanken zu verhindern.

Im folgenden Abschnitt finden Sie nützliche Ressourcen aus Campaign-Dokumentationen, die Ihnen bei der Optimierung der Datenbanknutzung helfen:

**Workflow-Überwachung**

* [Workflow-Best Practices](https://docs.adobe.com/content/help/de-DE/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.htmls) (Campaign Standard)
* [Überwachung der Workflow-Ausführung](https://docs.adobe.com/help/de-DE/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html) (Campaign Classic)

**Wartung der Datenbank**

* Technischer Workflow für die Datenbankbereinigung ([Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) / [Campaign Classic](https://docs.adobe.com/help/de-DE/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html))
* [Handbuch zur Datenbankwartung](https://docs.adobe.com/content/help/de-DE/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html) (Campaign Classic)
* [Behebung von Problemen mit der Datenbankleistung](https://docs.adobe.com/content/help/de-DE/campaign-classic/using/monitoring-campaign-classic/troubleshooting/database-performances.html) (Campaign Classic)
* [Datenbankbezogene Optionen](https://docs.adobe.com/help/de-DE/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html#database) (Campaign Classic)
