---
title: Versionshinweise 2022
description: Auf dieser Seite sind alle Control Panel-Versionen des Jahres 2022 aufgelistet.
exl-id: 9fb18bb6-c4e4-48aa-849c-d9129add5266
source-git-commit: c3c8d71e36cb1d55c2fcc8600b5063ea73d6e2e8
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 100%

---

# Versionshinweise 2021 {#rn-2022}

## Juni 2022 {#june-2022}

### Neue Funktionen

<table>
<thead>
<tr>
<th><strong>Die 10 Top-Dateien, die auf SFTP-Servern Speicherplatz verbrauchen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt die 10 Dateien identifizieren, die den meisten Speicherplatz auf einem SFTP-Server belegen. <a href="../sftp/using/sftp-storage-management.md">Weitere Informationen</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Service-Kalender-Erinnerungen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Im Service-Kalender können Sie jetzt Erinnerungen einstellen, sodass Sie per E-Mail benachrichtigt werden, bevor ein Ereignis auf Ihren Instanzen eintritt. <a href="../service-events/service-events.md">Weitere Informationen</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Verbesserungen bei der CSR-Generierung von Subdomains</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der Prozess der CSR-Generierung wurde in mehreren Punkten verbessert. <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">Weitere Informationen</a></p><ul><li>Beim Generieren einer CSR können Sie jetzt eine der enthaltenen Subdomains als Gebrauchsnamen auswählen.</li><li>Sie können jetzt die CSR-Zusammenfassung kopieren, bevor Sie die CSR generieren.</li><li>Nachdem eine CSR generiert wurde, können Sie sie erneut aus den Vorgangslogs herunterladen. Diese Funktion gilt nicht für Zertifikate, die vor dieser Version generiert wurden.</li></ul><p>

</td>
</tr>
</tbody>
</table>

### Verbesserungen

**Instanzeneinstellungen**

* Die maximale Anzahl der GPG-Schlüssel im Control Panel wurde auf 60 Schlüssel erhöht. [Weitere Informationen](../instances-settings/using/gpg-keys-management.md)

## Mai 2022 {#may-2022}

<table>
<thead>
<tr>
<th><strong>Verfügbarkeit des Control Panels für das Hybrid-Hosting-Modell</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Das Control Panel ist ab jetzt für Kunden mit einem Hybrid-Hosting-Modell verfügbar. Diese Kunden können die Funktionen des Control Panels nutzen, indem sie die URL ihrer MID/RT-Instanz, die in ihrer Marketing-Instanz konfiguriert ist, im Control Panel angeben.</p><p>Weitere Informationen finden Sie in der <a href="../instances-settings/using/external-accounts.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aktualisierungen der Überwachung von Durchsätzen und Latenzen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die Überwachungsfunktionen für Durchsätze und Latenzen wurden verbessert:<ul><li>Sie können jetzt die IDs der 5 Sendungen identifizieren, die am stärksten zum Durchsatz Ihrer Instanz beitragen.</li><li>Kunden von Campaign Classic v7/v8 können jetzt die Latenz für einen bestimmten Kanal visualisieren.</p></li><p>Weitere Informationen finden Sie in der <a href="../performance-monitoring/using/thoughputs-latencies.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>


## April 2022 {#april-2022}

<table>
<thead>
<tr>
<th><strong>Überwachung wichtiger Kontakte und Ereignisse auf Ihren Instanzen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt frühere und künftige Releases und Service-Reviews auf Ihren Instanzen überwachen sowie auf eine Liste der wichtigsten Ansprechpartner bei Adobe zugreifen, wenn Sie eine Anfrage oder ein Problem haben.</p><p>Weitere Informationen finden Sie in der <a href="../service-events/service-events.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

## März 2022 {#march-2022}

<table>
<thead>
<tr>
<th><strong>Verfügbarkeit der Überwachung von Durchsätzen und Latenzen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die Durchsatz- und Latenzüberwachung sind jetzt für alle Campaign Standard- und v8-Kunden sowie für Campaign v7-Kunden mit den Build-Nummern 9032, 9330, 9346 oder 9349 verfügbar, die eigenständige Bereitstellungen (ohne Mid-Instanz) besitzen.</p><p>Weitere Informationen finden Sie in der <a href="../performance-monitoring/using/thoughputs-latencies.md">entsprechenden Dokumentation.</a></p>
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
<p>Sie können jetzt Workflow-Parameter überwachen, die möglicherweise besondere Aufmerksamkeit erfordern, um Probleme in Ihren Instanzen zu vermeiden. </p><p>Weitere Informationen finden Sie in der <a href="../performance-monitoring/using/workflow-monitoring.md">entsprechenden Dokumentation</a>.</p>
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
<p>Mit dem Control Panel können Sie jetzt diejenigen Abfragen überwachen, die am längsten auf Ihren Instanzen ausgeführt werden.</p><p>Weitere Informationen finden Sie in der <a href="../performance-monitoring/using/database-active-queries.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Überwachen von Durchsätzen und Latenzen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt die Entwicklung der Durchsätze und Latenzen Ihrer Instanzen über einen bestimmten Zeitraum hinweg überwachen.</p><p>Weitere Informationen finden Sie in der <a href="../performance-monitoring/using/thoughputs-latencies.md">entsprechenden Dokumentation</a>.</p>
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
<p>Vorgänge von SSL-Zertifikaten können jetzt auf einer neu eingerichteten Subdomain ausgeführt werden, auch wenn die Zustellbarkeitsprüfung noch läuft.</p><p>Weitere Informationen finden Sie in der <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">entsprechenden Dokumentation</a>.</p>
</td>
</tr>
</tbody>
</table>
