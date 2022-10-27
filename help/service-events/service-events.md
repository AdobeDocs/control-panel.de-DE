---
product: campaign
solution: Campaign
title: Überwachung wichtiger Kontakte und Ereignisse
description: Erfahren Sie, wie Sie Ereignisse auf Ihren Instanzen und wichtige Ansprechpartner bei Adobe finden können.
feature: Control Panel
role: Architect
level: Intermediate
exl-id: d230aae6-4f0e-4201-bb3c-0e3f83a7c1b8
source-git-commit: 80a96152ffcfa184fbeb6fc5cddcb119655ffab1
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 95%

---

# Überwachung wichtiger Kontakte und Ereignisse {#keycontacts-events}

>[!CONTEXTUALHELP]
>id="cp_servicecalendar_serviceevents"
>title="Service-Kalender"
>abstract="Im Abschnitt „Wichtige Kontakte“ finden Sie eine Liste der Ansprechpartner bei Adobe, an die Sie sich bei Anfragen oder Problemen mit Ihren Instanzen wenden können. Im Abschnitt „Service-Ereignis-Kalender“ können Sie Versionen und Service-Überprüfungen für die ausgewählte Instanz ermitteln und Erinnerungen für künftige Ereignisse einrichten."

>[!IMPORTANT]
>
>Der Service-Kalender ist als Beta-Version verfügbar und unterliegt häufigen Aktualisierungen und Änderungen ohne Vorankündigung.

Die Identifizierung von Ereignissen, die auf Ihren Instanzen geplant sind, ist für die Überwachung Ihrer Campaign-Instanzen unerlässlich.

Mit dem Control Panel können Sie Releases und Service-Reviews auf Ihren Instanzen überwachen und auf eine Liste der wichtigsten Ansprechpartner bei Adobe zugreifen, wenn Sie eine Anfrage oder ein Problem haben.

Diese Informationen sind über die Karte **[!UICONTROL Service-Kalender]** auf der Startseite des Control Panels zugänglich.

## Wichtige Kontakte {#key-contacts}

Im Abschnitt **[!UICONTROL Wichtige Kontakte]** sind die Personen bei Adobe aufgeführt, an die Sie sich bei allen Anfragen oder Problemen mit Ihren Instanzen wenden können.

>[!NOTE]
>
>In diesem Abschnitt werden Informationen nur für Managed Service-Konten angezeigt.

![](assets/service-events-contacts.png)

Zu den wichtigen Kontakten gehören die folgenden Rollen:

* **[!UICONTROL TAM]**: technischer Kundenbetreuer,
* **[!UICONTROL CSM]**: Customer Success Manager,
* **[!UICONTROL Zustellbarkeit]**: Ansprechpartner für Zustellvorgänge,
* **[!UICONTROL Transition Manager]**: Managed Services Transition Manager (nur Managed Services-Konto),
* **[!UICONTROL Onboarding-Spezialist]**: Dem Konto zugewiesener Spezialist, der Sie beim Einstieg in Campaign Classic unterstützt (nur Managed Services-Konto).

## Ereignisse {#events}

### Ereignisse überwachen {#monitor-events}

Der Abschnitt **[!UICONTROL Kalender der Service-Ereignisse]** enthält alle früheren und künftigen Releases und Service-Reviews für die ausgewählte Instanz.

![](assets/service-events-calendar.png)

Die Spalte **[!UICONTROL Hinweise]** enthält Informationen zum Status jeder Version:

* **[!UICONTROL Allgemeine Verfügbarkeit]**: Neuester verfügbarer stabiler Build.
* **[!UICONTROL Eingeschränkte Verfügbarkeit]**: Implementierung nur auf Anfrage.
* **[!UICONTROL Release-Kandidat]**: technisch validiert. Fertigstellung für die Produktion ist ausstehend.
* **[!UICONTROL Vorabversion]**: Frühere Verfügbarkeit für spezifische Kundenanforderungen.
* **[!UICONTROL Nicht mehr verfügbar]**: Mit diesem Build bestehen zwar keine größeren Probleme, aber es ist ein neuerer Build mit zusätzlichen Fehlerkorrekturen verfügbar. Ein Upgrade ist erforderlich.
* **[!UICONTROL Veraltet]**: Ein Build, der bekannte Regressionen enthält.
Der Build wird nicht mehr unterstützt. Ein Upgrade ist unbedingt erforderlich.

Sie können einem oder mehreren kommenden Ereignissen eine Markierung zuweisen, um sie zu verfolgen. Klicken Sie dazu auf die Schaltfläche mit den Auslassungspunkten neben dem Ereignisnamen.

![](assets/service-events-flag.png)

### Erinnerungen einstellen {#reminders}

Mit Service-Kalender können Sie Erinnerungen festlegen, um vor einem Ereignis per E-Mail benachrichtigt zu werden.

>[!NOTE]
>
>Um über bevorstehende Ereignisse benachrichtigt zu werden, müssen Sie im Control Panel E-Mail-Benachrichtigungen abonniert haben. [Weitere Informationen](../performance-monitoring/using/email-alerting.md)

Gehen Sie wie folgt vor, um eine Benachrichtigung für ein Ereignis einzurichten:

1. Klicken Sie auf die Schaltfläche mit den Auslassungspunkten neben dem Ereignis, an das Sie erinnert werden möchten, und wählen Sie dann **[!UICONTROL Erinnerung festlegen]**.

1. Geben Sie der Erinnerung einen Titel und wählen Sie dann das Datum, an dem Sie vor dem Ereignis benachrichtigt werden möchten.

   ![](assets/service-events-set-reminder.png)

   >[!NOTE]
   >
   >Wenn Sie keine Warnhinweise vom Control Panel abonniert haben, wird eine Meldung angezeigt, mit der Sie sich für den Erhalt von E-Mail-Benachrichtigungen anmelden können.

1. Die Erinnerung ist jetzt für das ausgewählte Ereignis eingerichtet. Wenn Sie den Mauszeiger darüber bewegen, wird der Titel angezeigt.

   ![](assets/service-events-reminder.png)

   >[!NOTE]
   >
   >Sie können für jedes Ereignis bis zu 2 Erinnerungen einrichten.

1. An dem in der Erinnerung angegebenen Datum wird eine E-Mail gesendet, um Sie über das bevorstehende Ereignis zu informieren, und die Erinnerung wird automatisch aus der Liste **[!UICONTROL Erinnerungen]** im Service-Kalender-Menü entfernt.
