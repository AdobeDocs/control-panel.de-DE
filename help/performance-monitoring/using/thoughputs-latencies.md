---
product: campaign
solution: Campaign
title: Überwachung von Durchsätzen und Latenzzeiten
description: Erfahren Sie, wie Sie die Durchsätze und die Latenzzeiten Ihrer Campaign-Instanzen im Control Panel überwachen.
feature: Control Panel
role: Architect
level: Experienced
exl-id: eddef17f-0667-4b43-bc56-2b1aeeae61bb
source-git-commit: 84fe0aeb10bc5e535a7ab54a3316a51a1a32b3ca
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 74%

---

# Überwachung von Durchsätzen und Latenzzeiten {#throughputs-latency-monitoring}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_throughputslatencies"
>title="Über die Überwachung von Durchsätzen und Latenzzeiten "
>abstract="Auf dieser Registerkarte können Sie die Entwicklung der Durchsätze und Latenzzeiten Ihrer Instanzen über einen bestimmten Zeitraum hinweg überwachen."

Mit dem Control Panel können Sie Versanddurchsatz und Latenz für jede Ihrer Instanzen überwachen.

>[!IMPORTANT]
>
>Diese Funktion steht allen Kunden von Campaign Standard und v8 sowie Campaign V7-Kunden mit den Build-Nummern 9032,9330, 9346 oder 9349 zur Verfügung, die [standalone](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/deployment-types-/standalone-deployment.html) Bereitstellungen (ohne Mid-Instanz).

Um die Nutzung Ihrer Instanzen zu verstehen und sicherzustellen, dass sie eine gute Leistung erzielen, müssen Sie unbedingt überwachen, wie sich die Versanddurchsätze und die Latenzzeiten über einen bestimmten Zeitraum verhalten.

Diese Informationen werden im Control Panel für jede Ihrer Campaign-Instanzen auf der Karte **[!UICONTROL Leistungsüberwachung]** auf der Registerkarte **[!UICONTROL Durchsätze und Latenzzeiten]** verfügbar gemacht (beachten Sie, dass es im Control Panel bis zu 1 Stunde dauern kann, bis die Zahlen angezeigt werden).

* Der Bereich **[!UICONTROL Durchsatz]** enthält Informationen zur Anzahl der Nachrichten, die pro Stunde von der ausgewählten Campaign-Instanz für alle Kommunikationskanäle gesendet werden, für die Sie eine Berechtigung haben.

   >[!NOTE]
   >
   >Bei Campaign v7/v8 entspricht die angezeigte Durchsatznummer dem Durchsatz, der von MID-Instanzen (Mid-Sourcing) erzielt wurde. Bei eigenständigen Marketing-Bereitstellungen (MKT) (ohne MID-Instanz) wird stattdessen der Durchsatz von der MKT-Instanz angezeigt.

* Der Bereich **[!UICONTROL Latenz]** enthält Informationen zur Latenzzeit, die in der ausgewählten Instanz beim Versand von Echtzeit-Transaktionsnachrichten auftritt. Latenzzeiten werden im 95- und 99-Perzentil erfasst und visualisiert. Das bedeutet, dass 95 % bzw. 99 % der Anfragen schneller als die angegebene Latenzzeit sein sollten.

![](assets/throughput-latencies-overview.png)

>[!NOTE]
>
>Alle in diesem Bereich angezeigten Zahlen sind ungefähre Zahlen und dienen nur Informationszwecken.

Standardmäßig werden Daten für den aktuellen Tag angezeigt. Sie können den angezeigten Zeitraum mithilfe der Schaltflächen **[!UICONTROL 6 Monate]**, **[!UICONTROL 30 Tage]** und **[!UICONTROL 7 Tage]** ändern.

Sie können diese Informationen auch in tabellarischer Form mit sortierbaren Spalten anstatt mit einem Diagramm visualisieren. Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Visualisierungseinstellungen]** und wählen Sie **[!UICONTROL Tabelle]**.

![](assets/throughput-latencies-table.png)
