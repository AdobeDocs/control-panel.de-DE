---
title: IP-Bereiche auf die Whitelist setzen
description: Erfahren Sie, wie Sie IP-Bereiche für den Zugriff auf SFTP-Server auf die Whitelist auflisten
translation-type: tm+mt
source-git-commit: e080a86cc598581b75cffd622b2109e10355130a

---


# IP-Bereiche auf die Whitelist setzen {#ip-range-whitelisting}

SFTP-Server sind geschützt. Damit Sie darauf zugreifen und Dateien anzeigen oder neue erstellen können, müssen Sie die öffentliche IP-Adresse des Systems oder des Clients, über das bzw. den der Zugriff auf die Server erfolgt, auf die Whitelist setzen.

## Über das CIDR-Format {#about-cidr-format}

IP-Bereiche werden über das Control Panel im CIDR-Format (Classless Inter-Domain Routing) hinzugefügt.

Die Syntax besteht aus einer IP-Adresse, gefolgt vom Zeichen / und einer Dezimalzahl. Format und Syntax sind in [diesem Artikel](https://whatismyipaddress.com/cidr) ausführlich beschrieben.

Sie können im Internet nach kostenlosen Online-Tools suchen, mit denen Sie Ihren IP-Bereich in das CIDR-Format konvertieren können.

## Best Practices {#best-practices}

Beachten Sie unbedingt die folgenden Empfehlungen und Einschränkungen, wenn Sie IP-Adressen über das Control Panel auf die Whitelist setzen.

* **Setzen Sie IP-Bereiche** statt einzelner IP-Adressen auf die Whitelist. Um eine einzelne IP-Adresse auf die Whitelist zu setzen, fügen Sie "/32" an sie an, um zu kennzeichnen, dass der Bereich nur eine einzelne IP-Adresse enthält.
* **Setzen Sie keine extrem großen Bereiche auf die Whitelist**, z. B. über 265 IP-Adressen. Das Control Panel lehnt Bereiche im CIDR-Format ab, die zwischen /0 und /23 liegen.
* Only **public IP addresses** can be whitelisted.
* Make sure to **regularly delete whitelisted IP addresses** that you don't need anymore.

## IP-Adressen auf die Whitelist setzen {#whitelisting-ip-addresses}

Gehen Sie wie folgt vor, um einen IP-Bereich auf die weiße Liste zu setzen:

1. Öffnen Sie die Karte **[!UICONTROL SFTP]** und wählen Sie dann die Registerkarte **[!UICONTROL IP-Whitelisting]**.
1. Für jede Instanz wird die Liste der auf der Whitelist befindlichen IP-Adressen angezeigt. Wählen Sie die gewünschte Instanz auf der linken Liste und danach die Schaltfläche **[!UICONTROL Neuen IP-Bereich hinzufügen]aus.**

   ![](assets/control_panel_add_range.png)

1. Definieren Sie den IP-Bereich, den Sie auf die Whitelist setzen möchten, im CIDR-Format und geben Sie dann den Titel ein, der in der Liste angezeigt werden soll.

   >[!NOTE]
   >
   >Diese Sonderzeichen sind im Feld Titel erlaubt:
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

   ![](assets/control_panel_add_range2.png)

   >[!CAUTION]
   >
   >Ein IP-Bereich darf sich nicht mit einem bereits auf der Whitelist vorhandenen Bereich überschneiden. Löschen Sie in diesem Fall zunächst den Bereich, der die überlappende IP enthält.
   >
   >Es ist möglich, einen Bereich für mehrere Instanzen auf die Whitelist zu setzen. Verwenden Sie dazu die Abwärtspfeiltaste oder geben Sie die ersten Buchstaben der gewünschten Instanz ein und wählen Sie sie dann aus der Liste aus.

   ![](assets/control_panel_add_range3.png)

1. Wählen Sie die Schaltfläche **[!UICONTROL Speichern]aus.** Das Hinzufügen der IP-Adresse zur Whitelist wird als "Ausstehend" gekennzeichnet, bis die Anfrage vollständig verarbeitet wurde. Dies dauert nur einige Sekunden.

To delete whitelisted IP ranges, select them then click the **[!UICONTROL Delete IP range]** button.

![](assets/control_panel_delete_range2.png)

>[!NOTE]
>
>Es ist derzeit nicht möglich, einen auf der Whitelist befindlichen Bereich zu bearbeiten. Um einen IP-Bereich zu ändern, löschen Sie ihn und erstellen Sie danach einen, der Ihren Anforderungen entspricht.

## Überwachung von Änderungen {#monitoring-changes}

The **[!UICONTROL Job Logs]** in the Control Panel home page let you monitor all changes that have been made to whitelisted IP addresses.

Weitere Informationen zur Benutzeroberfläche des Control Panels finden Sie in [diesem Abschnitt](../../discover/using/discovering-the-interface.md).

![](assets/control_panel_ip_logNEW.png)
