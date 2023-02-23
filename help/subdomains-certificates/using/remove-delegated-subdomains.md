---
product: campaign
solution: Campaign
title: Zuweisung von Subdomains entfernen
description: Erfahren Sie, wie Sie die Zuweisung von Subdomains zu Adobe entfernen.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 5a8c4c4d1c5c527135901cd41f2b0936af8737b4
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 2%

---

# Zuweisung von Subdomains zur Adobe entfernen {#remove-delegated--subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="Zuweisung von Subdomains entfernen"
>abstract="Auf diesem Bildschirm können Sie die Zuweisung einer Subdomain zu Adobe entfernen. Beachten Sie, dass dieser Prozess nach der Übermittlung nicht mehr rückgängig gemacht oder gestoppt werden kann.<br><br>Wenn Sie versuchen, die Zuweisung einer primären Domäne für die ausgewählte Instanz zu entfernen, werden Sie aufgefordert, die Domäne auszuwählen, die sie ersetzen soll."

Mit dem Control Panel können Sie die Zuweisung einer Subdomain entfernen, die an Adobe delegiert wurde, einschließlich der Einrichtung von CNAME.

## Wichtige Hinweise {#important}

Bevor Sie fortfahren, sollten Sie die Auswirkungen sorgfältig prüfen, die nach Auslösung des Entfernungsprozesses auftreten:

* Das Entfernen der Subdomain-Zuweisung kann nicht rückgängig gemacht werden und ist nach dem Start unumkehrbar, bis der Prozess ausgeführt wird.
* Es kann keine andere Subdomain-Zuweisung entfernt werden, wenn ein ähnlicher Vorgang für eine andere Subdomain ausgeführt wird.
* Eine in einer Subdomain entfernte Delegation kann erst 3 Tage nach ihrer Entfernung erneut delegiert werden.

## Entfernen einer Subdomain-Zuweisung {#steps}

Gehen Sie wie folgt vor, um die Zuweisung einer Subdomain zu Adobe zu entfernen:

1. Klicken Sie auf die Suchschaltfläche neben der Domäne, die Sie entfernen möchten, und wählen Sie **[!UICONTROL Delegierte Subdomain entfernen]**.

   ![](assets/undelegate-subdomain.png)

1. Überprüfen Sie den Haftungsausschluss und bestätigen Sie die Entfernung der Domain-Zuweisung zur Adobe.

1. Überprüfen Sie Informationen zur Instanz, mit der die Subdomain verknüpft ist, einschließlich der zugehörigen IP-Affinitäten und Markenkonfigurationen.

   Wenn Sie die Zuweisung der primären Domäne für die ausgewählte Instanz entfernen, müssen Sie die Domäne auswählen, die sie durch die **[!UICONTROL Ersatzdomäne]** Liste.

   Klicken **[!UICONTROL Nächste]** , um mit der Entfernung fortzufahren.

   ![](assets/undelegate-subdomain-details.png)

1. Überprüfen Sie die angezeigte Zusammenfassung. Um das Entfernen zu bestätigen, geben Sie die URL der Domäne ein, für die Sie die Zuweisung entfernen möchten, und klicken Sie auf **[!UICONTROL Einsenden]**.

   ![](assets/undelegate-submit.png)

Nachdem das Entfernen der Zuweisung gestartet wurde, wird der ausstehende Auftrag in den Auftragsprotokollen angezeigt, bis er abgeschlossen ist.

![](assets/undelegate-job.png)

## Fehler-Codes {#FAQ}

In diesem Abschnitt werden die Fehlermeldungen aufgelistet, die auftreten können, wenn Sie versuchen, die Zuweisung einer Subdomain zu entfernen:

| Fehler-code | Nachricht | Beschreibung |
|  ---  |  ---  |  ---  |
| 8002 | Das Entfernen der angeforderten delegierten Domäne kann nicht behoben werden, da eine ähnliche überlappende Anforderung ausgeführt wird. Versuchen Sie es nach 3 Tagen. | Ein Vorgang zum Entfernen einer Subdomain-Zuweisung wird für die ausgewählte Instanz bereits ausgeführt. Warten Sie bis 3 Tage, um einen neuen Löschauftrag zu starten. |
| 8003 | Das angeforderte Delegierte Domänenlöschung wird für diese Instanz nicht unterstützt. | Aufgrund eines technischen Problems wird die Entfernung der Delegation für die ausgewählte Subdomain nicht unterstützt. Wenden Sie sich diesbezüglich an die Kundenunterstützung. |
| 8004 | Das Entfernen der angeforderten delegierten Domäne ist nicht zulässig, da in dieser Instanz nur eine Domäne vorhanden ist. | Für die ausgewählte Instanz wurde nur eine Subdomain zugewiesen. Delegationsentfernungen sind nicht zulässig. |
| 8005 | Das angeforderte Delegierte Domänenlöschung wird für diese Konfiguration nicht unterstützt. | Aufgrund eines technischen Problems wird die Entfernung der Delegation für die ausgewählte Subdomain nicht unterstützt. Wenden Sie sich diesbezüglich an die Kundenunterstützung. |
| 8006 | Das Entfernen angeforderter delegierter Domänen ist aus unbekannten Gründen nicht zulässig. Wenden Sie sich an die Kundenunterstützung. | Aufgrund unbekannter Probleme wird das Entfernen von Delegationen für die ausgewählte Instanz nicht unterstützt. Wenden Sie sich diesbezüglich an die Kundenunterstützung. |
