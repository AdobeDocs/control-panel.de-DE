---
product: campaign
solution: Campaign
title: Zuweisung von Subdomains entfernen
description: Erfahren Sie, wie Sie die Zuweisung von Subdomains zu Adobe entfernen.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: deb99ceb789f40c905de1a76cca8deca6b979765
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 16%

---

# Zuweisung von Subdomains zur Adobe entfernen {#remove-delegated--subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="Entfernen der Delegierung einer Subdomain"
>abstract="Auf diesem Bildschirm können Sie die Zuweisung einer Subdomain zu Adobe entfernen. Beachten Sie, dass dieser Prozess nicht rückgängig gemacht werden kann und erst nach seiner Ausführung wieder rückgängig gemacht werden kann.<br><br>Wenn Sie versuchen, die Zuweisung einer primären Domäne für die ausgewählte Instanz zu entfernen, werden Sie aufgefordert, die Domäne auszuwählen, die sie ersetzen soll."

Mit dem Control Panel können Sie die Zuweisung einer Subdomain entfernen, die an Adobe delegiert wurde, einschließlich der Einrichtung von CNAME.

## Wichtige Hinweise {#important}

Bevor Sie fortfahren, sollten Sie die Auswirkungen sorgfältig prüfen, die nach Auslösung des Entfernungsprozesses auftreten:

* Sobald der Prozess ausgelöst wurde, kann das Entfernen der Subdomain-Zuweisung nicht mehr rückgängig gemacht werden und ist so lange unumkehrbar, bis die Prozessausführung abgeschlossen ist.
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
| 8002 | Die angeforderte Entfernung der delegierten Domain kann nicht angegangen werden, da eine ähnliche überlappende Anfrage ausgeführt wird. Bitte nach 3 Tagen erneut versuchen | Ein Vorgang zum Entfernen einer Subdomain-Zuweisung wird für die ausgewählte Instanz bereits ausgeführt. Warten Sie bis 3 Tage, um einen neuen Löschauftrag zu starten. |
| 8003 | Die angeforderte Entfernung der delegierten Domain wird für diese Instanz nicht unterstützt. | Aufgrund eines technischen Problems wird die Entfernung der Delegation für die ausgewählte Subdomain nicht unterstützt. Wenden Sie sich diesbezüglich an die Kundenunterstützung. |
| 8004 | Die angeforderte Entfernung der delegierten Domain ist nicht zulässig, da es in dieser Instanz nur eine Domain gibt. | Für die ausgewählte Instanz wurde nur eine Subdomain zugewiesen. Delegationsentfernungen sind nicht zulässig. |
| 8005 | Die angeforderte Entfernung der delegierten Domain wird für diese Konfiguration nicht unterstützt. | Aufgrund eines technischen Problems wird die Entfernung der Delegation für die ausgewählte Subdomain nicht unterstützt. Wenden Sie sich diesbezüglich an die Kundenunterstützung. |
| 8006 | Die angeforderte Entfernung der delegierten Domain ist aus unbekannten Gründen nicht zulässig. Bitte die Kundenunterstützung kontaktieren. | Aufgrund unbekannter Probleme wird das Entfernen von Delegationen für die ausgewählte Instanz nicht unterstützt. Wenden Sie sich diesbezüglich an die Kundenunterstützung. |
