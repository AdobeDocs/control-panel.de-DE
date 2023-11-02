---
product: campaign
solution: Campaign
title: Benachrichtigungen per E-Mail
description: Erfahren Sie, wie Sie E-Mail-Benachrichtigungen erhalten, wenn Probleme mit Ihren Campaign-Instanzen auftreten.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: 7942d2b1-d28f-4760-aa25-5ba94a627fd0
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---

# Benachrichtigungen per E-Mail {#email-alerting}

Das Control Panel verfügt über eine Funktion mit echtzeitbasierten E-Mail-Warnungen, damit Sie Ihre Arbeit flexibler gestalten können.

## Liste der Warnhinweise {#list}

Die Liste der Warnungen lautet wie folgt:

* **Nutzung des SFTP-Speichers**: Einer Ihrer SFTP-Server hat mindestens 80 % seiner Kapazität erreicht. Siehe [SFTP-Speicherverwaltung](../../sftp/using/sftp-storage-management.md).

* **Datenbanknutzung**: Eine der Datenbanken Ihrer Instanzen hat mindestens 80 % ihrer Kapazität erreicht. Siehe [Datenbanküberwachung](../../performance-monitoring/using/database-monitoring.md).

* **Gültigkeit der SFTP-IP-Zulassungsauflistung**: Einer der von Ihnen definierten IP-Bereiche ist abgelaufen oder läuft in spätestens 10 Tagen ab. Weitere Informationen finden Sie unter [IP-Bereich-Zulassungsauflistung](../../sftp/using/ip-range-allow-listing.md).

* **Gültigkeit des öffentlichen SFTP-Schlüssels**: Einer der von Ihnen definierten öffentlichen Schlüssel ist abgelaufen oder läuft in spätestens 10 Tagen ab. Weitere Informationen finden Sie unter [Schlüsselverwaltung](../../sftp/using/key-management.md).

* **Gültigkeit des SSL-Zertifikats**: Eines der SSL-Zertifikate Ihrer Subdomains ist abgelaufen oder läuft in 30 Tagen oder weniger ab. Siehe [Überwachen von SSL-Zertifikaten der Subdomains](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

<!--* **Long running Queries**: A query has been running for more than 24 hours on one of your instances. See [Monitoring active queries](database-active-queries.md).-->

>[!NOTE]
>
>Darüber hinaus ermöglicht Ihnen das Control Panel, **Erinnerungen festzulegen**, um per E-Mail benachrichtigt zu werden, bevor ein Ereignis auf Ihren Instanzen eintritt (Versionen und Service-Reviews).
>
>Dazu müssen Sie E-Mail-Warnungen abonniert und eine Erinnerung an die gewünschten anstehenden Ereignisse eingerichtet haben. [Erfahren Sie, wie Sie Erinnerungen für anstehende Ereignisse festlegen.](../../service-events/service-events.md#reminders)

## Warnhinweise abonnieren {#subscribe}

Gehen Sie wie folgt vor, um diese Warnhinweise zu abonnieren:

1. Klicken Sie an einer beliebigen Stelle im Control Panel auf die Schaltfläche **[!UICONTROL Warnbenachrichtigungen]** und dann auf **[!UICONTROL Abonnieren]**.

   ![](assets/subscribing.png)

1. Sie erhalten eine E-Mail zur Bestätigung Ihres Abonnements.

   ![](assets/email_subscription.png)

1. Nach dem Abonnieren benachrichtigt Sie das Control Panel über Systemprobleme und empfiehlt zu ergreifende Maßnahmen. E-Mail-Warnungen werden an alle Personen gesendet, die sich für **alle Instanzen** angemeldet haben, bei denen sie Administratoren sind.

   ![](assets/alert_sample.png)
