---
title: SFTP-Speicherverwaltung
description: Erfahren Sie, wie Sie den Speicher des SFTP-Servers überwachen und verwalten.
translation-type: ht
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# SFTP-Speicherverwaltung {#sftp-storage-management}

Abhängig von Ihrem Vertrag kann Ihr SFTP-Server eine andere Speicherkapazität aufweisen.

Es ist wichtig, dass Sie laufend den verfügbaren Speicherplatz eines jeden SFTP-Servers überwachen. Andernfalls könnte es passieren, dass keine weiteren Dateien mehr auf dem Server gespeichert oder keine Workflows mehr erfolgreich ausgeführt werden können, die auf die Aktualisierung dieses Servers angewiesen sind.

**Verwandte Themen:**

* [Tutorial für Campaign Standard](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/monitoring-server-capacity-whitelisting-adding-ssh-key.html)
* [Tutorial für Campaign Classic](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/managing-sftp-servers.html)

## Zugriff auf Informationen zur Speicherkapazität {#accessing-storage-capacity-information}

Der Bereich **[!UICONTROL Die am meisten genutzten SFTP-Server]**im Header enthält die drei am häufigsten genutzten Server, die mit den Instanzen verbunden sind, auf die Sie Administratorzugriff haben. Diese Informationen sind auf jeder Registerkarte der SFTP-Karte verfügbar.

![](assets/control_panel_topspace.png)

Informationen zum Speicherplatz, der von allen Instanzen verwendet wird, auf die Sie zugreifen können, finden Sie auf der Registerkarte **[!UICONTROL Speicher]**der SFTP-Karte. Dieser Wert wird bei jeder Seitenaktualisierung neu berechnet.

![](assets/control_panel_space.png)

Eine visuelle Warnung wird für jede Instanz angezeigt, bei der die Speicherkapazität ausgeschöpft ist:

* **Orange**: Mehr als 80 % der Kapazität der Instanz sind ausgelastet,
* **Rot**: Mehr als 90 % der Kapazität der Instanz sind ausgelastet.

Außerdem erfahren Sie, wie Sie vorgehen sollten, wenn die Server-Kapazität nahezu erschöpft ist.

## Best Practices, wenn die Speicherkapazität erschöpft ist {#best-practices-when-capacity-runs-out}

1. **Entfernen Sie vom SFTP-Server alte oder unnötige Dateien**. Weitere Informationen zum Zugriff auf Ihren SFTP-Server-Ordner finden Sie in [diesem Abschnitt](../../sftp/using/logging-into-sftp-server.md).
1. Stellen Sie sicher, dass die **Workflows**, die Ihre SFTP-Server bereinigen, ordnungsgemäß ausgeführt werden. Weitere Informationen zu technischen Workflows in Adobe Campaign finden Sie in den Dokumentationen zu [Campaign Classic](https://docs.campaign.adobe.com/doc/AC/de/WKF_Allgemeine_Funktionsweise_Workflow_erstellen.html#Technische_Workflows) und [Campaign Standard](https://helpx.adobe.com/de/campaign/standard/administration/using/technical-workflows.html).
1. Wenden Sie sich an Ihr Account-Team, um **mehr Speicherplatz anzufordern** (möglicherweise fallen zusätzliche Gebühren an).
1. Wenden Sie sich an die **Kundenunterstützung**, wenn Sie glauben, dass ein Problem vorliegt.
