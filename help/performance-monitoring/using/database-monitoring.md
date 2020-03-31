---
title: Datenbanküberwachung
description: Erfahren Sie, wie Sie Ihre Kampagne-Datenbank in der Systemsteuerung überwachen.
translation-type: tm+mt
source-git-commit: f995e0dc51fd95d00fdcaa2eb347b2aedfdef60d

---


# Datenbanküberwachung {#database-monitoring}

## Grundlagen zu Instanzdatenbanken {#about-instances-databases}

Gemäß Ihrem Vertrag erhalten alle Instanzen Ihrer Kampagne eine bestimmte Menge an Datenbankplatz.

Datenbanken umfassen alle **Assets**, **Workflows** und **Daten** , die in Adobe Campaign gespeichert werden.

Im Laufe der Zeit können Datenbanken ihre maximale Kapazität erreichen, insbesondere wenn die gespeicherten Ressourcen nie aus der Instanz gelöscht werden oder wenn viele Workflows angehalten sind.

Das Überlaufen einer Instanzdatenbank kann zu mehreren Problemen führen (Unmöglichkeit der Anmeldung, des Versands von E-Mails usw.). Die Überwachung der Datenbanken Ihrer Instanzen ist daher für eine optimale Leistung unerlässlich.

>[!NOTE]
>
>Beachten Sie, dass es einige Diskrepanzen zwischen Ihrer aktuellen Datenbankspeicherkapazität und der im Vertrag angegebenen Menge für bestimmte Zeiträume geben kann, um eine höhere Leistung sicherzustellen.

## Überwachen der Datenbanknutzung {#monitoring-instances-database}

1. Öffnen Sie die **[!UICONTROL Health Monitoring]** Karte und wählen Sie die **[!UICONTROL Databases]** Registerkarte aus.

1. Wählen Sie die gewünschte Instanz aus dem **[!UICONTROL Instance List]**.

   Der obere Bereich enthält Informationen zur Datenbankkapazität der Instanz und zum verwendeten Platz.

   ![](assets/databases_dashboard.png)

   Der untere Bereich bietet eine grafische Darstellung der Datenbanknutzung in den letzten 7 Tagen. Sie können den angezeigten Zeitraum mithilfe der verfügbaren Filter oben rechts ändern.

   Wenn Sie den Mauszeiger über das Diagramm bewegen, erhalten Sie detaillierte Informationen zum ausgewählten Zeitraum.

   ![](assets/databases_dashboard_detail.png)

## Überladen von Datenbanken verhindern {#preventing-database-overload}

Campaign Standard und Classic Angebot verschiedene Möglichkeiten, eine Überbelegung des Datenbankspeicherplatzes zu verhindern.

Im folgenden Abschnitt finden Sie nützliche Ressourcen aus Kampagnen-Dokumentationen, die Ihnen bei der Optimierung Ihrer Datenbanknutzung helfen:

**Workflows**

* [Workflows Best Practices](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.html) (Campaign Standard)
* [Überwachung der Workflow-Ausführung](https://docs.adobe.com/help/en/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html) (Campaign Classic)

**Bereinigung der Datenbank**

* Technischer Arbeitsablauf für die Datenbankbereinigung ([Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflowshtml#list-of-technical-workflows) / [Kampagnenklassiker](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html))
* [Handbuch](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html) zur Datenbankwartung (Campaign Classic)
* [Fehlerbehebung](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/troubleshooting/database-performances.html) der Datenbankleistung (Campaign Classic)
* [Datenbankbezogene Optionen](https://docs.adobe.com/help/en/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html#database) (Campaign Classic)
