---
product: campaign
solution: Campaign
title: Entfernen der Zuweisung von Subdomains
description: Erfahren Sie, wie Sie die Zuweisung von Subdomains an Adobe entfernen.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: 517818c9-8557-49fd-b49c-b98b60e48f1c
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '831'
ht-degree: 100%

---

# Entfernen der Zuweisung von Subdomains an Adobe {#remove-delegated--subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="Entfernen der Delegierung einer Subdomain"
>abstract="Auf diesem Bildschirm kann die Delegierung einer Subdomain an Adobe entfernt werden. Es ist zu beachten, dass dieser Prozess nicht rückgängig gemacht werden kann und unumkehrbar ist, sobald die Ausführung begonnen hat.<br><br>Beim Versuch, die Delegierung der primären Domain für die ausgewählte Instanz zu entfernen, muss die Domain angegeben werden, der sie stattdessen zugewiesen werden soll."

Mit dem Control Panel können Sie die Delegation einer Subdomain entfernen, die vollständig an Adobe oder mithilfe von CNAME-Einträgen delegiert wurde.

## Wichtige Hinweise {#important}

Bevor Sie fortfahren, sollten Sie sorgfältig prüfen, welche Auswirkungen das Entfernen der Zuweisung haben könnte:

* Sobald der Prozess einmal ausgelöst wurde, kann das Entfernen der Subdomain-Zuweisung nicht mehr rückgängig gemacht werden und bleibt bis zum Abschluss des Prozesses unumkehrbar.
* Es kann keine andere Subdomain-Zuweisung entfernt werden, während ein ähnlicher Vorgang für eine andere Subdomain ausgeführt wird.
* Eine Subdomain, deren Delegation entfernt wurde, kann erst 3 Tage nach der Entfernung erneut delegiert werden.

## Entfernen der Zuweisung einer Subdomain {#steps}

Gehen Sie wie folgt vor, um die Zuweisung einer Subdomain zu Adobe zu entfernen:

1. Klicken Sie neben der Domain-Delegierung, die Sie entfernen möchten, auf die Schaltfläche mit den Auslassungspunkten und wählen Sie **[!UICONTROL Delegierung entfernen]** aus.

   ![](assets/undelegate-subdomain.png)

1. Lesen Sie den Haftungsausschluss und bestätigen Sie die Entfernung der Domain-Zuweisung an Adobe.

1. Überprüfen Sie die Informationen zur Instanz, mit der die Subdomain verknüpft ist, einschließlich der zugehörigen IP-Affinitäten und Markenkonfigurationen.

   Wenn Sie die Zuweisung der primären Domain für die ausgewählte Instanz entfernen, müssen Sie mithilfe der Liste **[!UICONTROL Ersetzungs-Domain]** die Domain auswählen, die Sie stattdessen zuweisen.

   Klicken Sie auf **[!UICONTROL Weiter]**, um mit der Entfernung fortzufahren.

   ![](assets/undelegate-subdomain-details.png)

1. Wenn Sie eine Delegation vom Typ CNAME entfernen oder eine primäre Domain durch eine mithilfe von CNAME-Einträgen delegierte Domain ersetzen, wird ein zusätzlicher **[!UICONTROL Aktionsschritt]** zur Verwaltung von DNS-Einträgen angezeigt. [Weitere Informationen finden Sie in diesem Abschnitt](#dns)

1. Lesen Sie die angezeigte Zusammenfassung. Um die Entfernung zu bestätigen, geben Sie die URL der Domain ein, für die Sie die Zuweisung entfernen möchten, und klicken Sie auf **[!UICONTROL Senden]**.

   ![](assets/undelegate-submit.png)

Nachdem der Entfernungsprozess gestartet wurde, wird der ausstehende Vorgang in den Vorgangslogs angezeigt, bis er abgeschlossen ist.

![](assets/undelegate-job.png)

## Verwaltung von DNS-Einträgen {#dns}

Um eine Domain-Delegation mithilfe von CNAME-Einträgen zu konfigurieren, erfordert das Control Panel, dass Sie bestimmte Einträge zu Ihrem DNS-Server hinzufügen. [Erfahren Sie, wie Sie Subdomains mithilfe von CNAME-Einträgen einrichten](setting-up-new-subdomain.md#use-cnames)

Beim Entfernen einer Delegation vom Typ CNAME müssen Sie **diese DNS-Einträge** von Ihrem Server entfernen, um Probleme zu vermeiden. Wenn Sie außerdem die Delegation einer primären Subdomain entfernen und sie durch eine mithilfe von CNAME-Einträgen delegierte Domain ersetzen möchten, müssen Sie möglicherweise **DNS-Einträge** auf Ihrem Server hinzufügen, abhängig von den für die Subdomain festgelegten IP-Affinitäten.

In der folgenden Tabelle ist(sind) die auszuführende(n) Aktion(en) aufgeführt, abhängig von der Art der Delegation, die Sie entfernen, und der Art der Delegation, die zur Einrichtung der Ersatz-Domain verwendet wurde.

| Entfernte Delegation | Delegation der Ersatz-Domain | Aktion erforderlich |
|  ---  |  ---  |  ---  |
| CNAME | Keine Ersatz-Domain | DNS-Einträge löschen |
| CNAME | CNAME | DNS-Einträge löschen<br/>DNS-Einträge hinzufügen *(optional, je nach IP-Affinitäten)* |
| CNAME | Vollständig | DNS-Einträge löschen |
| Vollständig | Keine Ersatz-Domain | Keine Aktion erforderlich |
| Vollständig | CNAME | DNS-Einträge hinzufügen *(optional, je nach IP-Affinitäten)* |
| Vollständig | Vollständig | Keine Aktion erforderlich |

{style="table-layout:auto"}

Wenn eine dieser Aktionen zum Entfernen der Delegierung erforderlich ist, wird ein zusätzlicher **[!DNL Action]**-Schritt vor der Löschbestätigung für die Delegierung angezeigt. In diesem Bildschirm werden je nach Kontext die zu entfernenden oder hinzuzufügenden DNS-Einträge aufgelistet.

![](assets/action-step.png)

### DNS-Einträge löschen

1. Navigieren Sie zu Ihrem DNS-Server und entfernen Sie die im Control Panel aufgelisteten Einträge.
1. Gehen Sie zurück zum Control Panel und klicken Sie auf **[!UICONTROL Weiter]**, um mit der Entfernung der Delegation fortzufahren.

### DNS-Einträge hinzufügen

1. Navigieren Sie zu Ihrem DNS-Server und fügen Sie die im Control Panel aufgelisteten Einträge hinzu.
1. Warten Sie, bis das Hinzufügen des DNS wirksam ist.
1. Gehen Sie zurück zum Control Panel und klicken Sie auf **[!UICONTROL Überprüfen]**.
1. Nachdem das Hinzufügen der Einträge erfolgreich überprüft wurde, klicken Sie auf **[!UICONTROL Weiter]**, um mit dem Entfernen der Delegation fortzufahren.

## Fehler-Codes {#FAQ}

In diesem Abschnitt sind die Fehlermeldungen aufgelistet, die auftreten können, wenn Sie versuchen, die Zuweisung einer Subdomain zu entfernen:

| Fehler-Code | Nachricht | Beschreibung |
|  ---  |  ---  |  ---  |
| 8002 | Die angeforderte Entfernung der delegierten Domain kann nicht angegangen werden, da eine ähnliche, sich damit überlappende Anfrage ausgeführt wird. Bitte in 3 Tagen erneut versuchen | Ein Vorgang zum Entfernen einer Subdomain-Zuweisung wird für die ausgewählte Instanz bereits ausgeführt. Es muss 3 Tage gewartet werden, um einen neuen Entfernungsvorgang zu starten. |
| 8003 | Die angeforderte Entfernung der delegierten Domain wird für diese Instanz nicht unterstützt. | Aufgrund eines technischen Problems wird das Entfernen der Delegierung für die ausgewählte Subdomain nicht unterstützt. Bitte die Kundenunterstützung kontaktieren. |
| 8004 | Die angeforderte Entfernung der delegierten Domain ist nicht zulässig, da es in dieser Instanz nur eine Domain gibt. | Für die ausgewählte Instanz wurde nur eine Subdomain delegiert. Das Entfernen von Delegierungen ist nicht erlaubt. |
| 8005 | Die angeforderte Entfernung der delegierten Domain wird für diese Konfiguration nicht unterstützt. | Aufgrund eines technischen Problems wird das Entfernen der Delegierung für die ausgewählte Subdomain nicht unterstützt. Bitte die Kundenunterstützung kontaktieren. |
| 8006 | Die angeforderte Entfernung der delegierten Domain ist aus unbekannten Gründen nicht zulässig. Bitte die Kundenunterstützung kontaktieren. | Aufgrund unbekannter Probleme wird das Entfernen von Delegierungen für die ausgewählte Instanz nicht unterstützt. Bitte die Kundenunterstützung kontaktieren. |
