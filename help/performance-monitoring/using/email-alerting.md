---
title: E-Mail-Warnung
description: Erfahren Sie, wie Sie E-Mail-Benachrichtigungen erhalten, wenn Probleme mit Ihren Instanzen Ihrer Kampagne auftreten
translation-type: tm+mt
source-git-commit: e79ad202a1d3c3eb8c9944a352cb7d614953bcd4

---


# E-Mail-Warnung {#email-alerting}

## Informationen zu E-Mail-Warnungen {#about-email-alerts}

Um Ihre Arbeit flexibler zu gestalten, verfügt die Systemsteuerung über eine Echtzeit-E-Mail-Warnfunktion.

Gehen Sie wie folgt vor, um diese Warnungen zu abonnieren:

1. Klicken Sie auf die **[!UICONTROL Alerting notifications]** Schaltfläche, die Sie an einer beliebigen Stelle in der Systemsteuerung aufrufen können, und klicken Sie dann auf **[!UICONTROL Subscribe]**.

   ![](assets/subscribing.png)

1. Zur Bestätigung Ihres Abonnements wird eine E-Mail gesendet.

   ![](assets/email_subscription.png)

1. Nach dem Abonnement benachrichtigt die Systemsteuerung über Systemprobleme und empfiehlt die zu ergreifenden Maßnahmen. E-Mail-Warnungen werden an alle Personen gesendet, die sich für **alle Instanzen** angemeldet haben, für die sie Administratoren sind.

   ![](assets/alert_sample.png)


Die Liste der Warnhinweise lautet wie folgt:

* **Nutzung** der SFTP-Datenspeicherung: Einer Ihrer SFTP-Server hat mindestens 80 % seiner Kapazität erreicht. See [SFTP storage management](../../sftp/using/sftp-storage-management.md).

* **Datenbankverwendung**: Eine der Datenbanken Ihrer Instanzen hat mindestens 80 % ihrer Kapazität erreicht. Siehe [Datenbanküberwachung](../../performance-monitoring/using/database-monitoring.md).

* **Ablauf** des SSL-Zertifikats: Eines der SSL-Zertifikate Ihrer Subdomänen ist abgelaufen oder läuft in höchstens 60 Tagen ab. See [Monitoring subdomains&#39; SSL certificates](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

