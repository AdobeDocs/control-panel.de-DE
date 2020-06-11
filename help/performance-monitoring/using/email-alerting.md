---
title: Warnungen per E-Mail
description: Erfahren Sie, wie Sie E-Mail-Benachrichtigungen erhalten, wenn Probleme mit Ihren Campaign-Instanzen auftreten.
translation-type: tm+mt
source-git-commit: e2ee8badd9fffdfadabbe6c659aef8504ee62e9d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 100%

---


# Warnungen per E-Mail {#email-alerting}

Um Ihre Arbeit flexibler zu gestalten, verfügt das Control Panel über eine Funktion mit echtzeitbasierten E-Mail-Warnungen.

Gehen Sie wie folgt vor, um diese Warnungen zu abonnieren:

1. Klicken Sie an einer beliebigen Stelle im Control Panel auf die Schaltfläche **[!UICONTROL Warnbenachrichtigungen]** und dann auf **[!UICONTROL Abonnieren]**.

   ![](assets/subscribing.png)

1. Sie erhalten eine E-Mail zur Bestätigung Ihres Abonnements.

   ![](assets/email_subscription.png)

1. Nach dem Abonnieren benachrichtigt Sie das Control Panel über Systemprobleme und empfiehlt zu ergreifende Maßnahmen. E-Mail-Warnungen werden an alle Personen gesendet, die sich für **alle Instanzen** angemeldet haben, bei denen sie Administratoren sind.

   ![](assets/alert_sample.png)


Die Liste der Warnungen lautet wie folgt:

* **Nutzung des SFTP-Speichers**: Einer Ihrer SFTP-Server hat mindestens 80 % seiner Kapazität erreicht. Siehe [SFTP-Speicherverwaltung](../../sftp/using/sftp-storage-management.md).

* **Datenbanknutzung**: Eine der Datenbanken Ihrer Instanzen hat mindestens 80 % ihrer Kapazität erreicht. Siehe [Datenbanküberwachung](../../performance-monitoring/using/database-monitoring.md).

* **Ablauf des SSL-Zertifikats**: Eines der SSL-Zertifikate Ihrer Subdomains ist abgelaufen oder läuft in 60 Tagen oder weniger ab. Siehe [Überwachen von SSL-Zertifikaten der Subdomains](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

