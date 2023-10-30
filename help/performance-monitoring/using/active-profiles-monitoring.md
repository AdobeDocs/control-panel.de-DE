---
product: campaign
solution: Campaign
title: Überwachen aktiver Profile
description: Erfahren Sie, wie Sie Informationen über die aktuelle und historische Nutzung und Entwicklung aktiver Profile für jede Ihrer Campaign-Instanzen in Echtzeit abrufen.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: a157cc27-577f-490f-8c4f-0f203219cfb5
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 51%

---

# Aktive Profile überwachen {#active-profiles-monitoring}

## Über aktive Profile {#about-active-profiles}

>[!IMPORTANT]
>
>Die Überwachung aktiver Profile über das Control Panel befindet sich in der Beta-Phase und unterliegt häufigen Aktualisierungen und Änderungen ohne Vorankündigung. Diese Funktion ist ab Campaign Standard-Build 10368 verfügbar.

Gemäß Ihrem Vertrag erhalten alle Ihre Campaign-Instanzen eine bestimmte Anzahl aktiver Profile, die zu Abrechnungszwecken gezählt werden. Informationen zur Anzahl der gekauften aktiven Profile finden Sie in Ihrem aktuellen Vertrag.

Profil bezeichnet einen Datensatz, der einen Endkunden, einen Prospect oder Lead repräsentiert. Bei diesen Daten kann es sich z. B. um einen Datensatz in der nmsRecipient-Tabelle oder einer externen Tabelle handeln, die die Kennung eines Cookies, eines Kunden oder eines Mobiltelefons oder andere für einen bestimmten Kanal relevante Informationen enthält.

Profile gelten als aktiv, wenn sie in den letzten 12 Monaten über einen beliebigen Kanal angesprochen wurden oder über einen beliebigen Kanal mit ihnen kommuniziert wurde.

>[!NOTE]
>
>Die Kanäle Facebook und Twitter werden nicht berücksichtigt.

Weitere Informationen zu aktiven Profilen finden Sie in den Dokumentationen zu [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html?lang=de) und [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html?lang=de#active-profiles).

## Überwachen der Verwendung aktiver Profile {#monitoring-active-profiles}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_active_profile"
>title="Über die Überwachung aktiver Profile"
>abstract="Auf diesem Tab erhalten Sie Echtzeitinformationen über die aktuelle und historische Nutzung und Entwicklung aktiver Profile für jede Instanz in Ihren Campaign-Instanzen und in Ihrer Organisation."

Die Informationen zur Verwendung aktiver Profile werden im Control Panel auf der Grundlage des dedizierten [!DNL Campaign] technische Workflows, die täglich auf Ihren Instanzen ausgeführt werden:
* Der Workflow „[Abrechnung](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=de)“ für Campaign Standard,
* Der Workflow [Anzahl aktiver Abrechnungsprofile](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html?lang=de) für Campaign v7/v8.


Um die aktive Profilnutzung im Control Panel zu überwachen, navigieren Sie zum **[!UICONTROL Leistungsüberwachung]** card > **[!UICONTROL Aktive Profile]** und wählen Sie die gewünschte Instanz aus dem **[!UICONTROL Instanzliste]**.

Es werden Informationen zu Ihrer Verwendung aktiver Profile angezeigt.

![](assets/active-profiles-graph.png)

Im oberen Abschnitt werden die folgenden Informationen angezeigt:

* Die Anzahl der aktiven Profile, die derzeit in der ausgewählten Instanz verwendet werden, sowie der Zeitstempel der letzten Ausführung des Abrechnungs-Workflows für Ihre Instanz.

* Die Gesamtzahl der aktiven Profile, die in Ihrer Organisation in allen Instanzen verwendet werden.

  >[!NOTE]
  >
  >Dieser Abschnitt ist nur sichtbar, wenn Ihrem Unternehmen mehrere Instanzen zugeordnet sind.

* Die Gesamtzahl der aktiven Profile, die Ihrer Organisation zugewiesen sind.

Der untere Abschnitt bietet eine visuelle Darstellung der aktiven Profilnutzung in den letzten 30 Tagen. Mit dem Filter oben rechts können Sie diesen Zeitraum auf 1 Jahr ändern. Wenn Sie den Mauszeiger über das Diagramm bewegen, erhalten Sie die genaue Anzahl der im ausgewählten Zeitraum verwendeten aktiven Profile.
