---
title: Datenbanküberwachung
description: Erfahren Sie, wie Sie Ihre Campaign-Datenbank im Control Panel überwachen können
translation-type: tm+mt
source-git-commit: 3dca1a261c4c92104170f70e6dbd12ba72e61e7d
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 32%

---


# Datenbanküberwachung {#database-monitoring}

## Über Datenbanken von Instanzen {#about-instances-databases}

Gemäß Ihrem Vertrag erhalten alle Ihre Campaign-Instanzen eine bestimmte Menge an Datenbankplatz.

Datenbanken beinhalten alle **Assets**, **Workflows** und **Daten**, die in Adobe Campaign gespeichert werden.

Im Laufe der Zeit können Datenbanken ihre maximale Kapazität erreichen, insbesondere wenn gespeicherte Ressourcen nie aus der Instanz gelöscht werden oder sich viele Workflows in angehaltenem Zustand befinden.

Ein Überlaufen der Datenbank einer Instanz kann zu verschiedenen Problemen führen (Anmeldung nicht möglich, Versand von E-Mails nicht möglich usw.). Daher ist für optimale Leistung eine Überwachung der Datenbanken Ihrer Instanzen unerlässlich.

>[!NOTE]
>
>Wenn der in der Systemsteuerung angegebene verfügbare Speicherplatz nicht dem in Ihrem Vertrag angegebenen Betrag entspricht, wenden Sie sich an den Kundendienst.

## Überwachen der Datenbanknutzung {#monitoring-instances-database}

Mit dem Control Panel können Sie die Datenbanknutzung für jede Ihrer Campaign-Instanzen überwachen. To do this, open the **[!UICONTROL Performance Monitoring]** card, then select the **[!UICONTROL Databases]** tab.

Wählen Sie die gewünschte Instanz aus der **[!UICONTROL Instanz-Liste]** aus, um Informationen zur Datenbankkapazität und zum verwendeten Speicherplatz der Instanz anzuzeigen.

![](assets/databases_dashboard.png)

>[!NOTE]
>
>Beachten Sie, dass die Daten aus diesem Dashboard basierend auf dem technischen Arbeitsablauf für die **[!UICONTROL Datenbankbereinigung]** aktualisiert werden, der auf Ihrer Kampagne ausgeführt wird (siehe Dokumentation zu [Campaign Standard](https://docs.adobe.com/help/de-DE/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) und [Campaign Classic](https://docs.adobe.com/help/de-DE/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html) ).
>
>Sie können überprüfen, wann der Workflow zuletzt unter den Metriken &quot; **[!UICONTROL Gebrauchter Speicherplatz]** &quot;und &quot; **[!UICONTROL Bereitgestellter Speicherplatz]** &quot;ausgeführt wurde. Beachten Sie, dass, wenn der Workflow seit mehr als 3 Tagen nicht ausgeführt wird, es empfohlen wird, sich an die Kundenunterstützung der Adobe zu wenden, damit sie herausfinden, warum der Workflow nicht ausgeführt wird.

In diesem Dashboard stehen zusätzliche Metriken zur Verfügung, die Ihnen bei der Analyse der Nutzung der Instanzdatenbank helfen:

* [Datenbankauslastung](../../performance-monitoring/using/database-monitoring.md#database-utilization)
* [Speicherübersicht](../../performance-monitoring/using/database-monitoring.md#storage-overview)
* [Die 10 wichtigsten temporären Ressourcen](../../performance-monitoring/using/database-monitoring.md#top-10)

### Database utilization {#database-utilization}

The **[!UICONTROL Database utilization]** area provides a graphical representation of the minimum, average and maximum database utilization over the last 7 days as well as the 90% database utilization threshold represented by a red dotted curve.

Um den Zeitraum zu ändern, verwenden Sie die Filter in der oberen rechten Ecke des Diagramms.

Zur besseren Lesbarkeit können Sie auch eine oder mehrere Kurven im Diagramm hervorheben. Wählen Sie diese dazu aus der Legende **[!UICONTROL Aggregationstyp]** aus.

Wenn Sie weitere Details zu einem bestimmten Zeitraum anzeigen möchten, halten Sie den Mauszeiger über das Diagramm, um Informationen zur Datenbanknutzung anzuzeigen, die zu diesem Zeitpunkt vorgenommen wurde.

![](assets/databases_dashboard_detail.png)

### Speicherübersicht {#storage-overview}

Der **[!UICONTROL Übersichtsbereich]** für die Datenspeicherung bietet eine grafische Darstellung des belegten Raumes:

* **[!UICONTROL Systemressourcen]**

   Beachten Sie, dass, wenn Systemressourcen einen Großteil des Datenbankplatzes verbrauchen, wir empfehlen, sich an die Kundenunterstützung zu wenden.

* **[!UICONTROL Standardmäßige Tabellen]** , die standardmäßig mit den Instanzen Ihrer Kampagne bereitgestellt werden,
* **[!UICONTROL Temporäre Tabellen]** , die von Workflows und Versänden erstellt wurden,
* **[!UICONTROL Nicht-Out-of-the-Box-Tabellen]** , die nach der Erstellung benutzerdefinierter Ressourcen generiert wurden.

![](assets/database-storage-overview.png)

Klicken Sie auf die Schaltfläche **[!UICONTROL Ansicht Details]** , um weitere Informationen zu den verschiedenen Assets zu erhalten, die Speicherplatz in der Datenbank benötigen.

![](assets/database-storage-details.png)

Verwenden Sie den Filter, um die Suche zu verfeinern und Tabellen nur aus einem bestimmten Asset-Typ anzuzeigen.

![](assets/database-storage-overview-filter.png)

### Die 10 wichtigsten temporären Ressourcen {#top-10}

Der **[!UICONTROL Top 10-Bereich für temporäre Ressourcen]** Liste die 10 größten temporären Ressourcen, die von Workflows und Versänden erzeugt werden.

Die Überwachung von Workflows und Versänden, die große temporäre Ressourcen erstellen, ist ein wichtiger Schritt zur Überwachung Ihrer Datenbank. Wenn eine temporäre Ressource zu viel Speicherplatz in der Datenbank beansprucht, stellen Sie sicher, dass dieser Workflow oder Versand erforderlich ist, und navigieren Sie schließlich zu Ihrer Instanz, um sie zu beenden.

>[!IMPORTANT]
>
>Die allgemeine Empfehlung ist, zu vermeiden, dass **mehr als 40 Spalten** nicht sofort verfügbar sind.

![](assets/database-top10.png)

>[!NOTE]
>
>Wenn festgestellt wird, dass ein Workflow eine große Anzahl von Tabellenwerten oder Datenbankgrößen aufweist, sollten Sie den Workflow überprüfen, um zu prüfen, warum er so viele Daten generiert.
>
>Campaign Standard- und Classic-Ressourcen stehen am Ende dieser Seite ebenfalls zur Verfügung, um eine Überlastung der Datenbank zu verhindern.

Über die Schaltfläche &quot; **[!UICONTROL Ansicht alle]** &quot;können Sie auf detaillierte Informationen zu diesen temporären Ressourcen zugreifen.

![](assets/database-top10-view.png)

>[!NOTE]
>
>Der Wert in der Spalte Zwischenergebnisse **** beibehalten gibt an, ob die Option in Kampagne aktiviert (&quot;1&quot;) oder deaktiviert (&quot;0&quot;) ist. Die Option &quot;Zwischenergebnisse **** beibehalten&quot;steht in den Eigenschaften der Workflows zur Verfügung. Sie können die Ergebnisse der Transitionen zwischen den verschiedenen Aktivitäten eines Workflows speichern (siehe Dokumentation zu [Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/executing-a-workflow/managing-execution-options.html) und [Campaign Classic](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/workflow-best-practices.html#logs) ).
>
>Wenn die Option für eine Ihrer Workflows aktiviert ist, kann der Arbeitsablauf für die Datenbankbereinigung nicht den durch Zwischenergebnisse belegten Speicherplatz zurückgewinnen. Wir empfehlen daher, den Workflow zu überprüfen, um zu prüfen, ob die Option deaktiviert werden kann.

## Verhindern einer Überbelegung von Datenbanken {#preventing-database-overload}

Campaign Standard und Classic bieten verschiedene Möglichkeiten, um eine Überbelegung von Speicherplatz in Datenbanken zu verhindern.

Im folgenden Abschnitt finden Sie nützliche Ressourcen aus Campaign-Dokumentationen, die Ihnen bei der Optimierung der Datenbanknutzung helfen:

**Workflow-Überwachung**

* [Workflow-Best Practices](https://docs.adobe.com/content/help/de-DE/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.htmls) (Campaign Standard)
* [Überwachung der Workflow-Ausführung](https://docs.adobe.com/help/de-DE/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html) (Campaign Classic)

**Wartung der Datenbank**

* Database cleanup technical workflow ([Campaign Standard](https://docs.adobe.com/help/de-DE/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) / [Campaign Classic](https://docs.adobe.com/help/de-DE/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html))
* [Handbuch zur Datenbankwartung](https://docs.adobe.com/content/help/de-DE/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html) (Campaign Classic)
* [Behebung von Problemen mit der Datenbankleistung](https://docs.adobe.com/content/help/de-DE/campaign-classic/using/monitoring-campaign-classic/troubleshooting/database-performances.html) (Campaign Classic)
* [Datenbankbezogene Optionen](https://docs.adobe.com/help/de-DE/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html#database) (Campaign Classic)
* Datenaufbewahrung ([Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/data-retention.html) / [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/configuring-campaign-classic/data-model/data-model-best-practices.html#data-retention))

>[!NOTE]
>
>Außerdem können Sie Benachrichtigungen erhalten, wenn eine Ihrer Datenbanken ihre Kapazität erreicht. To do this, subscribe to [email alerts](../../performance-monitoring/using/email-alerting.md).
