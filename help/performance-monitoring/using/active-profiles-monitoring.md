---
title: Überwachung aktiver Profil
description: Erfahren Sie, wie Sie Echtzeit-Informationen über die neueste und historische Nutzung und Entwicklung aktiver Profil für jede Ihrer Instanzen in der Kampagne erhalten.
translation-type: tm+mt
source-git-commit: 024eb750021ff2446b34d648b5abfb016eabc289
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 17%

---


# Überwachung aktiver Profil {#active-profiles-monitoring}

>[!IMPORTANT]
>
>Die Überwachung aktiver Profil über die Systemsteuerung ist in der Beta-Version verfügbar und kann mit häufigen Aktualisierungen und Änderungen ohne Vorankündigung durchgeführt werden.
>
>Die Funktion steht für Kunden zur Verfügung, die ab dem Build von Campaign Standard 10368 und dem Campaign Classic 8931 auf AWS gehostet werden. Wenn Sie einen früheren Build verwenden, müssen Sie ein Upgrade durchführen, um diese Funktion zu verwenden.

## Informationen zu aktiven Profilen {#about-active-profiles}

Gemäß Ihrem Vertrag erhalten alle Instanzen Ihrer Kampagne eine bestimmte Anzahl aktiver Profil, die zu Rechnungszwecken gezählt werden. Bitte beachten Sie die Anzahl der erworbenen aktiven Profil in Ihrem aktuellen Vertrag.

Profil bezeichnet einen Datensatz, der einen Endkunden, einen Prospect oder Lead repräsentiert. Bei diesen Daten kann es sich z. B. um einen Datensatz in der nmsRecipient-Tabelle oder einer externen Tabelle handeln, die die Kennung eines Cookies, eines Kunden oder eines Mobiltelefons oder andere für einen bestimmten Kanal relevante Informationen enthält.

Profile gelten als aktiv, wenn sie in den letzten 12 Monaten über einen Kanal anvisiert oder mit ihnen kommuniziert wurden.

>[!NOTE]
>
>Die Kanäle Facebook und Twitter werden nicht berücksichtigt.

Weitere Informationen zu aktiven Profilen finden Sie in den [Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) - und [Campaign Classic](https://docs.adobe.com/content/help/en/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles) -Dokumentationen.

## Überwachen aktiver Profil {#monitoring-active-profiles}

Über die Systemsteuerung können Sie die Verwendung der aktiven Profil für jede Ihrer Instanzen der Kampagne überwachen.

Gehen Sie dazu wie folgt vor:

1. Open the **[!UICONTROL Performance Monitoring]** card, then select the **[!UICONTROL Active Profiles]** tab.

1. Wählen Sie die gewünschte Instanz aus der **[!UICONTROL Instanzenliste]** aus.

1. Die Anzahl der aktiven Profil, die von der Instanz verwendet werden, sowie das letzte Mal, wenn der Abrechnungs-Workflow auf Ihrer Instanz ausgeführt wurde, werden angezeigt.

![](assets/active-profiles-graph.png)

>[!NOTE]
>
>Aktive Profil werden auf der Grundlage spezieller Technischen Workflows gezählt, die täglich in Ihren Instanzen ausgeführt werden:
>
>* Der [&quot;Rechnungsstellungsarbeitsablauf&quot;](https://docs.adobe.com/help/de-DE/campaign-standard/using/administrating/application-settings/technical-workflows.html) für Campaign Standard,
>* Der Arbeitsablauf [&quot;Anzahl der aktiven Profile&quot;](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/technical-workflows/deliveries.html) zum Campaign Classic.


Der untere Bereich bietet eine grafische Darstellung der aktiven Profil der letzten 30 Tage. Sie können den angezeigten Zeitraum mithilfe der verfügbaren Filter oben rechts auf 1 Jahr ändern.

Wenn Sie den Mauszeiger über eine der Diagrammleisten halten, können Sie die exakte Anzahl der aktiven Profil abrufen, die im ausgewählten Zeitraum verwendet wurden.
