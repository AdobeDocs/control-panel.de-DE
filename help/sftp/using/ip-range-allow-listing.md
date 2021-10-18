---
product: campaign
solution: Campaign
title: Zulassungsauflistung von IP-Bereichen
description: Erfahren Sie, wie Sie der Zulassungsliste IP-Bereiche für den Zugriff auf SFTP-Server hinzufügen.
feature: Control Panel
role: Architect
level: Experienced
exl-id: 45a3bfcd-500c-4139-b610-d39989260ab7
source-git-commit: 99861c898c216d2589f23bd52779db328ea47256
workflow-type: tm+mt
source-wordcount: '1081'
ht-degree: 36%

---

# Zulassungsauflistung von IP-Bereichen {#ip-range-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_ip_whitelist"
>title="Über die Zulassungsauflistung von IP-Bereichen"
>abstract="Auf dieser Registerkarte können Sie der Zulassungsliste IP-Bereiche hinzufügen, um eine Verbindung zu Ihren SFTP-Servern herzustellen. Hier werden nur SFTP-Server aufgeführt, auf die Sie Zugriff haben. Wenn Sie Zugriff auf andere SFTP-Server wünschen, kontaktieren Sie Ihren Administrator."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=98" text="Demovideo ansehen"

SFTP-Server sind geschützt. Um auf sie zugreifen zu können, um Dateien anzuzeigen oder neue zu schreiben, müssen Sie die öffentliche IP-Adresse des Systems oder des Clients, über das bzw. den auf die Server zugegriffen wird, zur Zulassungsliste hinzufügen.

![](assets/do-not-localize/how-to-video.png) Entdecken Sie diese Funktion im Video mit [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/adding-ip-range-to-allow-list.html#sftp-management) oder [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/adding-ip-range-to-allow-list.html#sftp-management).

## Über das CIDR-Format {#about-cidr-format}

IP-Bereiche werden über das Control Panel im CIDR-Format (Classless Inter-Domain Routing) hinzugefügt.

Die Syntax besteht aus einer IP-Adresse, gefolgt vom Zeichen / und einer Dezimalzahl. Format und Syntax werden in [diesem Artikel](https://whatismyipaddress.com/cidr){target=&quot;_blank&quot;} ausführlich beschrieben.

Sie können im Internet nach kostenlosen Online-Tools suchen, die Ihnen helfen, den vorhandenen IP-Bereich in das CIDR-Format zu konvertieren.

## Best Practices {#best-practices}

Beachten Sie unbedingt die folgenden Empfehlungen und Einschränkungen, wenn Sie IP-Adressen über das Control Panel auf die Zulassungsliste setzen.

* **Fügen Sie der Zulassungsliste IP-Bereiche** anstelle einzelner IP-Adressen hinzu. Um eine einzelne IP-Adresse auf die Zulassungsliste zu setzen, fügen Sie &quot;/32&quot; an sie an, um zu kennzeichnen, dass der Bereich nur eine einzelne IP-Adresse enthält.
* **Fügen Sie der Zulassungsliste keine sehr großen Bereiche hinzu**, z. B. mehr als 265 IP-Adressen. Das Control Panel lehnt Bereiche im CIDR-Format ab, die zwischen /0 und /23 liegen.
* Der Zulassungsliste können nur **öffentliche IP-Adressen** hinzugefügt werden.
* Stellen Sie sicher, dass **regelmäßig IP-Adressen** löschen, dass Sie nicht mehr von der Zulassungsliste benötigen.

## Hinzufügen von IP-Adressen zur Zulassungsliste {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_add"
>title="IP-Bereichskonfiguration"
>abstract="Definieren Sie IP-Bereiche, die Sie auf die Zulassungsliste setzen möchten, um sich mit Ihren SFTP-Servern zu verbinden."

Gehen Sie wie folgt vor, um einen IP-Bereich auf die Zulassungsliste zu setzen:

1. Öffnen Sie die Karte **[!UICONTROL SFTP]** und wählen Sie dann die Registerkarte **[!UICONTROL IP-Zulassungsauflistung]** aus.
1. Die Liste der IP-Adressen auf der Zulassungsliste wird für jede Instanz angezeigt. Wählen Sie in der linken Liste die gewünschte Instanz und danach die Schaltfläche **[!UICONTROL Neuen IP-Bereich hinzufügen]** aus.

   ![](assets/control_panel_add_range.png)

1. Definieren Sie den IP-Bereich, den Sie der Zulassungsliste hinzufügen möchten. Dieses Feld akzeptiert nur IP-Bereiche im CIDR-Format, z. B. *192.150.5.0/24*.

   ![](assets/control_panel_add_range4.png)

   >[!IMPORTANT]
   >
   >Ein IP-Bereich darf sich nicht mit einem bereits auf der Zulassungsliste vorhandenen Bereich überschneiden. Löschen Sie in diesem Fall zunächst den Bereich, der die überlappende IP enthält.

1. Es ist möglich, der Zulassungsliste einen Bereich für mehrere Instanzen hinzuzufügen. Verwenden Sie dazu die Abwärtspfeiltaste oder geben Sie die ersten Buchstaben der gewünschten Instanz ein und wählen Sie sie dann aus der Liste aus.

   ![](assets/control_panel_add_range3.png)

1. Definieren Sie den Titel, der für diesen IP-Bereich in der Liste angezeigt wird.

   ![](assets/control_panel_add_range2.png)

   >[!NOTE]
   >
   >Die folgenden Sonderzeichen sind im Feld **[!UICONTROL Beschriftung]** zulässig:
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

1. Um Ihre IP-Zulassungsliste besser zu verwalten, können Sie eine Dauer für die Verfügbarkeit der einzelnen IP-Bereiche festlegen. Wählen Sie dazu eine Einheit in der Dropdown-Liste **[!UICONTROL Typ]** aus und legen Sie eine Dauer im entsprechenden Feld fest. Weitere Informationen zum Ablauf von IP-Bereichen finden Sie in [diesem Abschnitt](#expiry).

   ![](assets/control_panel_add_range5.png)

   >[!NOTE]
   >
   >Standardmäßig ist das Feld **[!UICONTROL Typ]** auf **[!UICONTROL Unlimited]** gesetzt, was bedeutet, dass der IP-Bereich nie abläuft.

1. Im Feld **[!UICONTROL Kommentar]** können Sie einen Grund angeben, warum Sie diesen IP-Bereich zulassen möchten (warum, für wen usw.).

1. Wählen Sie die Schaltfläche **[!UICONTROL Speichern]** aus. Der zur Zulassungsliste hinzugefügte IP-Bereich wird als **[!UICONTROL Ausstehend]** angezeigt, bis die Anfrage vollständig verarbeitet wurde. Dies sollte nur einige Sekunden dauern.

   ![](assets/control_panel_add_range6.png)

>[!IMPORTANT]
>
>Wenn Sie versuchen, Ihre SFTP-Server mit einem neuen System zu verbinden und so der Zulassungsliste neue IP-Bereiche hinzufügen, müssen Sie möglicherweise neue öffentliche Schlüssel eingeben, um die Verbindung abzuschließen. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](key-management.md).

## Verwalten von IP-Bereichen {#managing-ip-ranges}

Die von Ihnen erstellten IP-Bereiche werden auf der Registerkarte **[!UICONTROL IP-Zulassungsauflistung]** angezeigt.

Sie können die Elemente nach Erstellungsdatum oder Bearbeitungsdatum, nach dem Benutzer, der sie erstellt oder bearbeitet hat, und nach dem Ablauf des IP-Bereichs sortieren.

Sie können auch einen IP-Bereich durchsuchen, indem Sie eine Bezeichnung, einen Bereich, einen Namen oder einen Kommentar eingeben.

![](assets/control_panel_allow_list_sort.png)

Informationen zum Bearbeiten eines oder mehrerer IP-Bereiche finden Sie in [diesem Abschnitt](#editing-ip-ranges).

Um einen oder mehrere IP-Bereiche aus der Zulassungsliste zu löschen, wählen Sie sie aus und klicken Sie dann auf die Schaltfläche **[!UICONTROL IP-Bereich löschen]** .

![](assets/control_panel_delete_range.png)

### Ablauf {#expiry}

Die Spalte **[!UICONTROL Läuft ab]** gibt an, wie viele Tage bis zum Ablauf des IP-Bereichs verstreichen.

Wenn Sie sich für [E-Mail-Warnungen](../../performance-monitoring/using/email-alerting.md) angemeldet haben, erhalten Sie Benachrichtigungen per E-Mail 10 Tage und 5 Tage, bevor ein IP-Bereich abläuft und an dem Tag, an dem er abläuft. Nach Erhalt des Warnhinweises können Sie [den IP-Bereich](#editing-ip-ranges) bearbeiten, um den Gültigkeitszeitraum bei Bedarf zu verlängern.

Ein abgelaufener IP-Bereich wird nach 7 Tagen automatisch gelöscht. Sie wird als **[!UICONTROL Abgelaufen]** in der Spalte **[!UICONTROL Läuft ab]** angezeigt. Innerhalb dieses 7-tägigen Zeitraums:

* Für den Zugriff auf die SFTP-Server kann kein abgelaufener IP-Bereich mehr verwendet werden.

* Sie können keinen weiteren IP-Bereich erstellen, der einen abgelaufenen Bereich überschneidet. Sie müssen zunächst den abgelaufenen IP-Bereich löschen, bevor Sie den neuen erstellen.

* Sie können [einen abgelaufenen IP-Bereich bearbeiten](#editing-ip-ranges) und seine Dauer aktualisieren, um ihn wieder verfügbar zu machen.

* Sie können sie aus der Zulassungsliste löschen.

## Bearbeiten von IP-Bereichen {#editing-ip-ranges}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_update"
>title="Aktualisieren von IP-Bereichen"
>abstract="Aktualisieren Sie die ausgewählten IP-Bereiche, die eine Verbindung zu Ihrem SFTP-Server herstellen dürfen."

Gehen Sie wie folgt vor, um IP-Bereiche zu bearbeiten.

>[!NOTE]
>
>Sie können nur IP-Bereiche bearbeiten, die seit der Control Panel-Version vom Oktober 2021 erstellt wurden.

<!--Edition is not available for IP ranges that have been created before the Control Panel October 2021 release.-->

1. Wählen Sie einen oder mehrere IP-Bereiche aus der Liste **[!UICONTROL IP-Zulassungsauflistung]** aus.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL IP-Bereich aktualisieren]** .

   ![](assets/control_panel_edit_range.png)

1. Sie können nur den Ablauf des IP-Bereichs bearbeiten und/oder einen neuen Kommentar hinzufügen.

   >[!NOTE]
   >
   >Um das CIDR-Format, seinen Titel oder die zugehörigen Instanzen zu ändern, müssen Sie zunächst den IP-Bereich löschen und einen neuen erstellen, der Ihren Anforderungen entspricht.

   ![](assets/control_panel_edit_range2.png)

1. Speichern Sie Ihre Änderungen.

## Änderungen überwachen {#monitoring-changes}

Auf der Startseite des Control Panels können Sie mit **[!UICONTROL Vorgangslogs]** alle Änderungen verfolgen und überwachen, die an IP-Adressen auf der Zulassungsliste vorgenommen wurden.

Weitere Informationen zur Benutzeroberfläche des Control Panels finden Sie in [diesem Abschnitt](../../discover/using/discovering-the-interface.md).

![](assets/control_panel_ip_log.png)
