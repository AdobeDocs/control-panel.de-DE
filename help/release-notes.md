---
product: campaign
solution: Campaign
title: Control Panel-Versionen
description: Auf dieser Seite werden alle neuen Funktionen und Verbesserungen für das Control Panel aufgeführt.
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: 35b849725711bfee9852cf8f503bc599f6d8eaff
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 86%

---

# Control Panel-Versionen {#control-panel-releases}

Auf dieser Seite werden alle neuen Funktionen und Verbesserungen für das Control Panel aufgeführt.

>[!NOTE]
>
>Das Control Panel ist nur für Administratoren zugänglich. Weiterführende Informationen zu Berechtigungen finden Sie in [diesem Abschnitt](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=de#discover-control-panel).
>
>Für Campaign v7 muss Ihre Instanz auf Amazon Web Services (AWS) gehostet und auf den neuesten [stabilen Campaign-Build](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=de#rn-statuses) (oder auf Build 9032 oder höher) aktualisiert werden. Erfahren Sie in [diesem Abschnitt](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=de#getting-your-campaign-version), wie Sie Ihre Version überprüfen. Um zu überprüfen, ob Ihre Instanz auf AWS gehostet wird, folgen Sie den Schritten auf [dieser Seite](faq.md#hosted-aws).

## März 2022 {#march-2022}

<table>
<thead>
<tr>
<th><strong>Durchsätze und Verfügbarkeit der Latenzüberwachung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Durchsätze und Latenzüberwachung sind jetzt für alle Campaign Standard- und v8-Kunden sowie für Campaign V7-Kunden mit den Build-Nummern 9032,9330, 9346 oder 9349 verfügbar, die eigenständige Bereitstellungen (ohne Zwischeninstanz) aufweisen.</p><p>Weitere Informationen finden Sie in der <a href="performance-monitoring/using/thoughputs-latencies.md">entsprechenden Dokumentation.</a></p>
</td>
</tr>
</tbody>
</table>

## Februar 2022 {#february-2022}

<table>
<thead>
<tr>
<th><strong>Überwachung von Workflow-Parametern</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Workflow-Parameter überwachen, die möglicherweise besondere Aufmerksamkeit erfordern, um Probleme in Ihren Instanzen zu vermeiden. </p><p>Weitere Informationen finden Sie in der <a href="performance-monitoring/using/workflow-monitoring.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

## Januar 2022 {#january-2022}

<table>
<thead>
<tr>
<th><strong>Überwachung aktiver Abfragen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mit dem Control Panel können Sie jetzt diejenigen Abfragen überwachen, die auf Ihren Instanzen am längsten ausgeführt werden.</p><p>Weitere Informationen finden Sie in der <a href="performance-monitoring/using/database-active-queries.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Überwachung von Durchsätzen und Latenzzeiten</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt die Entwicklung der Durchsätze und Latenzzeiten Ihrer Instanzen über einen bestimmten Zeitraum hinweg überwachen.</p><p>Weitere Informationen finden Sie in der <a href="performance-monitoring/using/thoughputs-latencies.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Vorgänge von SSL-Zertifikaten auf neuen Subdomains</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vorgänge von SSL-Zertifikaten können jetzt auf einer neu eingerichteten Subdomain ausgeführt werden, auch wenn die Zustellbarkeitsprüfung noch läuft.</p><p>Weitere Informationen finden Sie in der <a href="subdomains-certificates/using/renewing-subdomain-certificate.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

## Oktober 2021 {#october-2021}

<table>
<thead>
<tr>
<th><strong>IP-Bereich und Gültigkeitszeitraum des öffentlichen Schlüssels</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Es ist jetzt möglich, eine Dauer für die Verfügbarkeit von IP-Bereichen und öffentlichen Schlüsseln festzulegen. </p><p>Weitere Informationen finden Sie im Abschnitt <a href="sftp/using/ip-range-allow-listing.md#adding-ip-addresses-allow-list">Zulassungsauflistung von IP-Bereichen</a> und <a href="sftp/using/key-management.md#installing-ssh-key">Schlüsselverwaltung</a> Abschnitte.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>IP-Bereich und Ausgabe öffentlicher Schlüssel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt die <a href="sftp/using/ip-range-allow-listing.md#editing-ip-ranges">IP-Bereiche</a> und die <a href="sftp/using/key-management.md#editing-public-keys">öffentlichen Schlüssel</a> bearbeiten, die Sie erstellen. Beachten Sie, dass diese Funktion nicht für die Elemente verfügbar ist, die vor der aktuellen Control Panel-Version erstellt wurden.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Benachrichtigung zum SFTP-IP-Bereich und zum Ablauf öffentlicher Schlüssel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die E-Mail-Warnfunktion enthält jetzt Warnhinweise zum Verfall der SFTP-IP-Zulassungsauflistung und der öffentlichen SFTP-Schlüssel.
</p><p>Weitere Informationen finden Sie in der <a href="performance-monitoring/using/email-alerting.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Vollständige Unterstützung in Campaign v8</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die Vewaltungsfunktionen <strong>Subdomain</strong> und <strong>Zertifikat</strong> werden jetzt vom Control Panel in Adobe Campaign v8 unterstützt.</a>.</p>
</td>
</tr>
</tbody>
</table>

## August 2021 {#august-2021}

<table>
<thead>
<tr>
<th><strong>Unterstützung in Campaign v8</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Das Control Panel ist jetzt für Adobe Campaign v8 verfügbar, mit Ausnahme der Verwaltungsfunktionen <strong>Subdomain</strong> und <strong>Zertifikat</strong>, die noch nicht unterstützt werden.</p><p>Weitere Informationen finden Sie im Abschnitt <a href="https://experienceleague.adobe.com/docs/campaign/campaign-v8/deploy/self-service.html?lang=de" target="blank">Dokumentation zu Campaign v8</a>.</p>
</td>
</tr>
</tbody>
</table>

## Oktober 2020 {#october-2020}

<table>
<thead>
<tr>
<th><strong>Subdomain-Konfiguration mit CNAME</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Im Control Panel können Sie jetzt mit CNAME eine Subdomain für die Verwendung mit Adobe direkt über die Benutzeroberfläche konfigurieren.</p><p>Weitere Informationen finden Sie in der <a href="subdomains-certificates/using/setting-up-new-subdomain.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Verbesserungen bei der Datenbanküberwachung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die Datenbanküberwachung wurde um zusätzliche Metriken erweitert, sodass Sie detaillierte Informationen zu den Ressourcen erhalten können, die Speicherplatz in Ihrer Datenbank belegen.</p><p>Weitere Informationen finden Sie in der <a href="performance-monitoring/using/database-monitoring.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

## Juni 2020 {#june-2020}

<table>
<thead>
<tr>
<th><strong>Prüfung der Subdomain-Zustellbarkeit</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nachdem Sie eine neue Subdomain zugewiesen haben, können Sie nun mit dem Control Panel die vom Zustellbarkeitsteam durchgeführte Prüfung verfolgen.</p><p>Weitere Informationen finden Sie in der <a href="subdomains-certificates/using/setting-up-new-subdomain.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>GPG-Schlüsselverwaltung</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Im Control Panel können Sie jetzt ein GPG-Schlüsselpaar generieren, sodass Sie in Campaign eingehende externe Daten problemlos entschlüsseln können. Darüber hinaus können Sie einen öffentlichen GPG-Schlüssel installieren, um von Campaign ausgehende Daten zu verschlüsseln.</p><p>Weitere Informationen finden Sie in der <a href="instances-settings/using/gpg-keys-management.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Überwachung aktiver Profile</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Im Control Panel können Sie jetzt die Anzahl der aktiven Profile überwachen, die von Ihren Instanzen verwendet und für Abrechnungszwecke gezählt werden.</p><p>Weitere Informationen finden Sie in der <a href="performance-monitoring/using/active-profiles-monitoring.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

>[!IMPORTANT]
>
>Die Überwachung aktiver Profile über das Control Panel befindet sich in der Beta-Phase und unterliegt häufigen Aktualisierungen und Änderungen ohne Vorankündigung.

## Mai 2020 {#may-2020}

<table>
<thead>
<tr>
<th><strong>Zertifikatverwaltung für CNAME-Subdomains</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Das Control Panel ermöglicht es Ihnen jetzt, die SSL-Zertifikate Ihrer Subdomains zu erneuern, die mit der CNAME-Methode konfiguriert wurden.</p><p>Weitere Informationen finden Sie in der <a href="subdomains-certificates/using/renewing-subdomain-certificate.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

## April 2020 {#april-2020}

<table>
<thead>
<tr>
<th><strong>Verwaltung von Google TXT-Einträgen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Fügen Sie allen Subdomains, die zum Senden von E-Mails an Gmail-Adressen über das Campaign Control Panel verwendet werden, einen Eintrag der TXT-Websiteüberprüfung von Google hinzu.</p><p>Weitere Informationen finden Sie in der <a href="subdomains-certificates/using/managing-txt-records.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Überwachung von Datenbankspeicherplatz</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Das Campaign Control Panel verfügt über Funktionen zur Datenbanküberwachung, mit denen Sie die Auslastung Ihres Datenbankspeicherplatzes zu einem bestimmten Zeitpunkt und im Zeitverlauf anzeigen können.</p><p>Weitere Informationen finden Sie in der <a href="performance-monitoring/using/database-monitoring.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Benachrichtigungen per E-Mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Das Campaign Control Panel bietet Funktionen zum Empfang von E-Mail-Warnungen in Echtzeit. Wenn Sie sich beim Control Panel anmelden und Warnhinweise abonnieren, werden Sie benachrichtigt, wenn Ihrem System eine Leistungsverschlechterung droht oder eine Aktion erforderlich ist, um eine künftig hohe Leistung sicherzustellen.</p><p>Weitere Informationen finden Sie in der <a href="performance-monitoring/using/email-alerting.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

## Januar 2020 {#january-2020}

Für Admin-Benutzer wurden neue Funktionen hinzugefügt, mit denen sie über das Control Panel Subdomains konfigurieren und SSL-Zertifikate verlängern können.

Weitere Informationen finden Sie auf den folgenden Seiten:
* [Einrichten einer neuen Subdomain](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Verlängern des SSL-Zertifikats einer Subdomain](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Diese Funktionen werden als Betaversion verfügbar sein und häufigen Aktualisierungen und Änderungen ohne vorherige Ankündigung unterliegen.

## September 2019 {#september-2019}

Admin-Benutzern wurden neue Funktionen hinzugefügt, mit denen sie IP-Adressen zur Zulassungsliste hinzufügen können, um eine Verbindung zu Campaign v7/v8-Instanzen herzustellen.
Außerdem können Admin-Benutzer jetzt die Liste der Campaign v7/v8-Instanzen und die Berechtigung für Build-Upgrades anzeigen.

Weitere Informationen finden Sie in der [entsprechenden Dokumentation](instances-settings/using/ip-allow-listing-instance-access.md).

## August 2019 {#august-2019}

Für Admin-Benutzer wurden neue Funktionen hinzugefügt, durch die sie benachrichtigt werden, bevor die SSL-Zertifikate für ihre Domains ablaufen. Weitere Informationen finden Sie im [entsprechenden Handbuch](subdomains-certificates/using/monitoring-ssl-certificates.md).

Darüber hinaus können die Admin-Benutzer jetzt SSH-Schlüssel löschen, die für den Zugriff auf SFTP-Server hinzugefügt wurden.

## Juli 2019 {#july-2019}

Wir haben neue Funktionen hinzugefügt, mit denen Admin-Benutzer die Einstellungen der Campaign v7/v8-Instanzen besser steuern können. Zu den neuen Control Panel-Funktionen gehört die Möglichkeit, URLs hinzuzufügen, mit denen Adobe Campaign eine Verbindung herstellen kann, um Daten bzw. Dateien zu übertragen.

Weitere Informationen finden Sie im [entsprechenden Handbuch](instances-settings/using/url-permissions.md).
