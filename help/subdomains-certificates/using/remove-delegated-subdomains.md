---
product: campaign
solution: Campaign
title: Entfernen der Zuweisung von Subdomains
description: Erfahren Sie, wie Sie die Zuweisung von Subdomains an Adobe entfernen.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 349eb8778a19263b83b70b8c920c401aff7fa24a
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 100%

---

# Entfernen der Zuweisung von Subdomains an Adobe {#remove-delegated--subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="Entfernen der Delegierung einer Subdomain"
>abstract="Auf diesem Bildschirm können Sie die Zuweisung einer Subdomain an Adobe entfernen. Es ist zu beachten, dass dieser Prozess nicht rückgängig gemacht werden kann und unumkehrbar ist, sobald die Ausführung begonnen hat.<br><br>Wenn Sie versuchen, die Zuweisung der primären Domain für die ausgewählte Instanz zu entfernen, müssen Sie die Domain angeben, der sie stattdessen zugewiesen werden soll."

Mit Control Panel können Sie die Delegation einer Adobe delegierten Subdomain entfernen.

>[!NOTE]
>
>Bei Subdomains, die mit CNAME eingerichtet wurden, können Zuweisungen derzeit nicht entfernt werden.

## Wichtige Hinweise {#important}

Bevor Sie fortfahren, sollten Sie sorgfältig prüfen, welche Auswirkungen das Entfernen der Zuweisung haben könnte:

* Sobald der Prozess einmal ausgelöst wurde, kann das Entfernen der Subdomain-Zuweisung nicht mehr rückgängig gemacht werden und bleibt bis zum Abschluss des Prozesses unumkehrbar.
* Es kann keine andere Subdomain-Zuweisung entfernt werden, während ein ähnlicher Vorgang für eine andere Subdomain ausgeführt wird.
* Eine Subdomain, deren Delegation entfernt wurde, kann erst 3 Tage nach der Entfernung erneut delegiert werden.

## Entfernen der Zuweisung einer Subdomain {#steps}

Gehen Sie wie folgt vor, um die Zuweisung einer Subdomain zu Adobe zu entfernen:

1. Klicken Sie neben der Domain, die Sie entfernen möchten, auf die Schaltfläche mit den Auslassungspunkten und wählen Sie **[!UICONTROL Delegierte Subdomain entfernen]** aus.

   ![](assets/undelegate-subdomain.png)

1. Lesen Sie den Haftungsausschluss und bestätigen Sie die Entfernung der Domain-Zuweisung an Adobe.

1. Überprüfen Sie die Informationen zur Instanz, mit der die Subdomain verknüpft ist, einschließlich der zugehörigen IP-Affinitäten und Markenkonfigurationen.

   Wenn Sie die Zuweisung der primären Domain für die ausgewählte Instanz entfernen, müssen Sie mithilfe der Liste **[!UICONTROL Ersetzungs-Domain]** die Domain auswählen, die Sie stattdessen zuweisen.

   Klicken Sie auf **[!UICONTROL Weiter]**, um mit der Entfernung fortzufahren.

   ![](assets/undelegate-subdomain-details.png)

1. Lesen Sie die angezeigte Zusammenfassung. Um die Entfernung zu bestätigen, geben Sie die URL der Domain ein, für die Sie die Zuweisung entfernen möchten, und klicken Sie auf **[!UICONTROL Senden]**.

   ![](assets/undelegate-submit.png)

Nachdem der Entfernungsprozess gestartet wurde, wird der ausstehende Vorgang in den Vorgangslogs angezeigt, bis er abgeschlossen ist.

![](assets/undelegate-job.png)

## Fehler-Codes {#FAQ}

In diesem Abschnitt sind die Fehlermeldungen aufgelistet, die auftreten können, wenn Sie versuchen, die Zuweisung einer Subdomain zu entfernen:

| Fehler-Code | Nachricht | Beschreibung |
|  ---  |  ---  |  ---  |
| 8002 | Die angeforderte Entfernung der delegierten Domain kann nicht angegangen werden, da eine ähnliche, sich damit überlappende Anfrage ausgeführt wird. Bitte in 3 Tagen erneut versuchen | Ein Vorgang zum Entfernen einer Subdomain-Zuweisung wird für die ausgewählte Instanz bereits ausgeführt. Es muss 3 Tage gewartet werden, um einen neuen Entfernungsvorgang zu starten. |
| 8003 | Die angeforderte Entfernung der delegierten Domain wird für diese Instanz nicht unterstützt. | Aufgrund eines technischen Problems wird das Entfernen der Zuweisung für die ausgewählte Subdomain nicht unterstützt. Bitte die Kundenunterstützung kontaktieren. |
| 8004 | Die angeforderte Entfernung der delegierten Domain ist nicht zulässig, da es in dieser Instanz nur eine Domain gibt. | Für die ausgewählte Instanz wurde nur eine Subdomain delegiert. Das Entfernen von Zuweisungen ist nicht erlaubt. |
| 8005 | Die angeforderte Entfernung der delegierten Domain wird für diese Konfiguration nicht unterstützt. | Aufgrund eines technischen Problems wird das Entfernen der Zuweisung für die ausgewählte Subdomain nicht unterstützt. Bitte die Kundenunterstützung kontaktieren. |
| 8006 | Die angeforderte Entfernung der delegierten Domain ist aus unbekannten Gründen nicht zulässig. Bitte die Kundenunterstützung kontaktieren. | Aufgrund unbekannter Probleme wird das Entfernen von Zuweisungen für die ausgewählte Instanz nicht unterstützt. Bitte die Kundenunterstützung kontaktieren. |
