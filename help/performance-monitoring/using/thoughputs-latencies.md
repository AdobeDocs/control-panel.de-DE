---
product: campaign
solution: Campaign
title: Überwachen von Durchsätzen und Latenzzeiten
description: Erfahren Sie, wie Sie die Durchsätze und die Latenzzeiten Ihrer Campaign-Instanzen im Control Panel überwachen.
feature: Control Panel
role: Architect
level: Experienced
exl-id: eddef17f-0667-4b43-bc56-2b1aeeae61bb
source-git-commit: a5bd04c4659ae18c4f05934f42e071b209a58fff
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 74%

---

# Überwachen von Durchsätzen und Latenzzeiten {#throughputs-latency-monitoring}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_throughputslatencies"
>title="Über die Überwachung von Durchsätzen und Latenzzeiten "
>abstract="Auf dieser Registerkarte können Sie die Entwicklung der Durchsätze und Latenzzeiten Ihrer Instanzen über einen bestimmten Zeitraum hinweg überwachen. Informationen zu den Sendungen, die zum Durchsatz beitragen, finden Sie in der Tabellenansicht."

Mit dem Control Panel können Sie den Versanddurchsatz und die Latenzzeit für jede Ihrer Instanzen überwachen.

>[!IMPORTANT]
>
>Diese Funktion steht allen Kunden von Campaign Standard und v8 sowie Campaign v7-Kunden mit den Build-Nummern 9032, 9330, 9346 oder 9349 zur Verfügung, die [eigenständige](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/deployment-types-/standalone-deployment.html?lang=de) Bereitstellungen (ohne Mid-Instanz) besitzen.

Die Überwachung der Entwicklung von Versanddurchsatz und Latenz über einen bestimmten Zeitraum ist wichtig, um die Nutzung Ihrer Instanzen zu verstehen und sicherzustellen, dass sie eine gute Leistung erzielen.

Diese Informationen werden im Control Panel für jede Ihrer Campaign-Instanzen auf der Karte **[!UICONTROL Leistungsüberwachung]** auf der Registerkarte **[!UICONTROL Durchsätze und Latenzzeiten]** verfügbar gemacht (beachten Sie, dass es im Control Panel bis zu 1 Stunde dauern kann, bis die Zahlen angezeigt werden).

>[!NOTE]
>
>Alle in diesem Bereich angezeigten Zahlen sind ungefähre Zahlen und dienen nur Informationszwecken.

![](assets/throughput-latencies-overview.png)

Standardmäßig werden Daten für den aktuellen Tag angezeigt. Sie können den angezeigten Zeitraum mithilfe der Schaltflächen **[!UICONTROL 6 Monate]**, **[!UICONTROL 30 Tage]** und **[!UICONTROL 7 Tage]** ändern. Die Daten werden vorgestellt:
* Stündlich für 1 Tag- und 7 Tage-Ansicht,
* 6 stündlich für 30-Tage-Ansicht,
* Täglich für 6 Monate anzeigen.

Sie können diese Informationen auch in tabellarischer Form mit sortierbaren Spalten anstatt mit einem Diagramm visualisieren. Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Visualisierungseinstellungen]** und wählen Sie **[!UICONTROL Tabelle]**.

![](assets/throughput-latencies-table.png)

## Durchsatz überwachen {#throughput}

Der Bereich **[!UICONTROL Durchsatz]** enthält Informationen zur Anzahl der Nachrichten, die pro Stunde von der ausgewählten Campaign-Instanz für alle Kommunikationskanäle gesendet werden, für die Sie eine Berechtigung haben.

>[!NOTE]
>
>Bei Campaign v7/v8 entspricht der angezeigte Durchsatzwert dem Durchsatz, der von MID-Instanzen (Mid-Sourcing) erzielt wurde. Bei eigenständigen Marketing-Bereitstellungen (MKT), d. h. ohne MID-Instanz, wird stattdessen der Durchsatz von der MKT-Instanz angezeigt.

Darüber hinaus ermöglicht Ihnen das Control Panel die Identifizierung der IDs der 5 häufigsten Sendungen, die während des ausgewählten Zeitraums zum Durchsatz beitragen. Diese Informationen sind nur in der Tabellenansicht verfügbar:

![](assets/throughput-latencies-top5.png)

## Überwachen der Latenz {#latency}

Der Bereich **[!UICONTROL Latenz]** enthält Informationen zur Latenzzeit, die in der ausgewählten Instanz beim Versand von Echtzeit-Transaktionsnachrichten auftritt.

>[!NOTE]
>
>Beachten Sie, dass Informationen im Zusammenhang mit **Profillatenz** ist auch verfügbar für [!DNL Campaign Standard] nur Instanzen.

Latenzzeiten werden im 95- und 99-Perzentil erfasst und visualisiert. Das bedeutet, dass 95 % bzw. 99 % der Anfragen schneller als die angegebene Latenzzeit sein sollten.

![](assets/throughput-latencies-latency.png)

Standardmäßig wird die Latenz für alle Kanäle angezeigt. Sie können die Latenz für einen bestimmten Kanal mithilfe der Dropdownliste visualisieren.

![](assets/throughput-latencies-filter.png)

>[!NOTE]
>
>Die Kanalfilterung ist nur für Campaign Classic v7/v8-Instanzen verfügbar.
