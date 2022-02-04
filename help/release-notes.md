---
product: campaign
solution: Campaign
title: Control Panel-Versionen
description: Aktuelle Control Panel-Versionshinweise.
feature: Control Panel
role: Architect
level: Beginner
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: 10c4cf41dc9502bb66566951780cf8f963b08aa9
workflow-type: ht
source-wordcount: '858'
ht-degree: 100%

---

# Control Panel-Versionen {#control-panel-releases}

Hier finden Sie Informationen zu den aktuellen Versionen des Control Panel.

>[!NOTE]
>
>Das Control Panel ist nur für Administratoren zugänglich. Weiterführende Informationen zu Berechtigungen finden Sie in [diesem Abschnitt](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=de#discover-control-panel).
>
>Für Campaign Classic v7 muss Ihre Instanz auf Amazon Web Services (AWS) gehostet und auf den neuesten [stabilen Campaign-Build](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=de#rn-statuses) (oder auf Build 9032 oder höher) aktualisiert werden. Erfahren Sie in [diesem Abschnitt](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=de#getting-your-campaign-version), wie Sie Ihre Version überprüfen. Um zu überprüfen, ob Ihre Instanz auf AWS gehostet wird, folgen Sie den Schritten auf [dieser Seite](faq.md#hosted-aws).

## Januar 2022 {#january-2022}

**Überwachung aktiver Abfragen**

Mit dem Control Panel können Sie jetzt diejenigen Abfragen überwachen, die auf Ihren Instanzen am längsten ausgeführt werden. [Mehr dazu](performance-monitoring/using/database-active-queries.md)

**Überwachung von Durchsätzen und Latenzzeiten**

Sie können jetzt die Entwicklung der Durchsätze und Latenzzeiten Ihrer Instanzen über einen bestimmten Zeitraum hinweg überwachen. [Mehr dazu](performance-monitoring/using/thoughputs-latencies.md)

**Vorgänge von SSL-Zertifikaten auf neuen Subdomains**

Vorgänge von SSL-Zertifikaten können jetzt auf einer neu eingerichteten Subdomain ausgeführt werden, auch wenn die Zustellbarkeitsprüfung noch läuft. [Mehr dazu](subdomains-certificates/using/renewing-subdomain-certificate.md)

## Oktober 2021 {#october-2021}

**IP-Bereich und Gültigkeitszeitraum des öffentlichen Schlüssels**

Es ist jetzt möglich, eine Dauer für die Verfügbarkeit von IP-Bereichen und öffentlichen Schlüsseln festzulegen. Weitere Informatioinen dazu finden Sie in den Abschnitten [Zulassungsauflistung für IP-Bereiche](sftp/using/ip-range-allow-listing.md#adding-ip-addresses-allow-list) und [Schlüsselverwaltung](sftp/using/key-management.md#installing-ssh-key).

**IP-Bereich und Ausgabe öffentlicher Schlüssel**

Sie können jetzt die [IP-Bereiche](sftp/using/ip-range-allow-listing.md#editing-ip-ranges) und die [öffentlichen Schlüssel](sftp/using/key-management.md#editing-public-keys) bearbeiten, die Sie erstellen. Beachten Sie, dass diese Funktion nicht für die Elemente verfügbar ist, die vor der aktuellen Control Panel-Version erstellt wurden.

**Benachrichtigung zum SFTP-IP-Bereich und zum Ablauf öffentlicher Schlüssel**

Die E-Mail-Warnfunktion enthält jetzt Warnhinweise zum Verfall der SFTP-IP-Zulassungsauflistung und der öffentlichen SFTP-Schlüssel.
[Mehr dazu](performance-monitoring/using/email-alerting.md)

**Vollständige Unterstützung in Campaign v8**

Die Vewaltungsfunktionen **Subdomain** und **Zertifikat** werden jetzt vom Control Panel in Adobe Campaign v8 unterstützt.

## August 2021 {#august-2021}

**Unterstützung in Campaign v8**

Das Control Panel ist jetzt für Adobe Campaign v8 verfügbar, mit Ausnahme der Verwaltungsfunktionen **Subdomain** und **Zertifikat**, die noch nicht unterstützt werden. Weitere Informationen finden Sie in der [Dokumentation zu Campaign v8](https://experienceleague.adobe.com/docs/campaign/campaign-v8/deploy/self-service.html?lang=de){target=&quot;_blank&quot;}

## Oktober 2020 {#october-2020}

**Subdomain-Konfiguration mit CNAME**

Im Control Panel können Sie jetzt mit CNAME eine Subdomain für die Verwendung mit Adobe direkt über die Benutzeroberfläche konfigurieren. [Mehr dazu](subdomains-certificates/using/setting-up-new-subdomain.md)

**Verbesserungen bei der Datenbanküberwachung**

Die Datenbanküberwachung wurde um zusätzliche Metriken erweitert, sodass Sie detaillierte Informationen zu den Ressourcen erhalten können, die Speicherplatz in Ihrer Datenbank belegen. [Mehr dazu](performance-monitoring/using/database-monitoring.md)

## Juni 2020 {#june-2020}

**Prüfung der Subdomain-Zustellbarkeit**

Nachdem Sie eine neue Subdomain zugewiesen haben, können Sie nun mit dem Control Panel die vom Zustellbarkeitsteam durchgeführte Prüfung verfolgen. [Mehr dazu](subdomains-certificates/using/setting-up-new-subdomain.md)

**GPG-Schlüsselverwaltung**

Im Control Panel können Sie jetzt ein GPG-Schlüsselpaar generieren, sodass Sie in Campaign eingehende externe Daten problemlos entschlüsseln können. Darüber hinaus können Sie einen öffentlichen GPG-Schlüssel installieren, um von Campaign ausgehende Daten zu verschlüsseln. [Mehr dazu](instances-settings/using/gpg-keys-management.md)

**Überwachung aktiver Profile**

Im Control Panel können Sie jetzt die Anzahl der aktiven Profile überwachen, die von Ihren Instanzen verwendet und für Abrechnungszwecke gezählt werden. [Mehr dazu](performance-monitoring/using/active-profiles-monitoring.md)

>[!IMPORTANT]
>
>Die Überwachung aktiver Profile über das Control Panel befindet sich in der Beta-Phase und unterliegt häufigen Aktualisierungen und Änderungen ohne Vorankündigung.

## Mai 2020 {#may-2020}

**Zertifikatverwaltung für CNAME-Subdomains**

Das Control Panel ermöglicht es Ihnen jetzt, die SSL-Zertifikate Ihrer Subdomains zu erneuern, die mit der CNAME-Methode konfiguriert wurden. [Mehr dazu](subdomains-certificates/using/renewing-subdomain-certificate.md)

## April 2020 {#april-2020}

**Verwaltung von Google TXT-Einträgen**

Fügen Sie allen Subdomains, die zum Senden von E-Mails an Gmail-Adressen über das Campaign Control Panel verwendet werden, einen Eintrag der TXT-Websiteüberprüfung von Google hinzu. [Mehr dazu](subdomains-certificates/using/managing-txt-records.md)

**Überwachung von Datenbankspeicherplatz**

Das Campaign Control Panel verfügt über Funktionen zur Datenbanküberwachung, mit denen Sie die Auslastung Ihres Datenbankspeicherplatzes zu einem bestimmten Zeitpunkt und im Zeitverlauf anzeigen können. [Mehr dazu](performance-monitoring/using/database-monitoring.md)

**Benachrichtigungen per E-Mail**

Das Campaign Control Panel bietet Funktionen zum Empfang von E-Mail-Warnungen in Echtzeit. Wenn Sie sich beim Control Panel anmelden und Warnhinweise abonnieren, werden Sie benachrichtigt, wenn Ihrem System eine Leistungsverschlechterung droht oder eine Aktion erforderlich ist, um eine künftig hohe Leistung sicherzustellen. [Mehr dazu](performance-monitoring/using/email-alerting.md)

## Januar 2020 {#january-2020}

*22. Januar 2020*

Für Admin-Benutzer wurden neue Funktionen hinzugefügt, mit denen sie über das Control Panel Subdomains konfigurieren und SSL-Zertifikate verlängern können.

Weitere Informationen finden Sie auf den folgenden Seiten:
* [Einrichten einer neuen Subdomain](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Verlängern des SSL-Zertifikats einer Subdomain](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Diese Funktionen werden als Betaversion verfügbar sein und häufigen Aktualisierungen und Änderungen ohne vorherige Ankündigung unterliegen.

## September 2019 {#september-2019}

*16. September 2019*

Für Admin-Benutzer wurden neue Funktionen hinzugefügt, mit denen sie IP-Adressen auf die Zulassungsliste setzen können, um eine Verbindung zu Campaign Classic-Instanzen herzustellen.
Außerdem können Admin-Benutzer jetzt die Liste der Campaign Classic-Instanzen und die Berechtigung für Build-Upgrades einsehen.

Weitere Informationen finden Sie in der [entsprechenden Dokumentation](instances-settings/using/ip-allow-listing-instance-access.md).

## August 2019 {#august-2019}

Für Admin-Benutzer wurden neue Funktionen hinzugefügt, durch die sie benachrichtigt werden, bevor die SSL-Zertifikate für ihre Domains ablaufen. Weitere Informationen finden Sie im [entsprechenden Handbuch](subdomains-certificates/using/monitoring-ssl-certificates.md).

Darüber hinaus können die Admin-Benutzer jetzt SSH-Schlüssel löschen, die für den Zugriff auf SFTP-Server hinzugefügt wurden.

## Juli 2019 {#july-2019}

Für Admin-Benutzer wurden neue Funktionen hinzugefügt, mit denen sie die Einstellungen der Campaign Classic-Instanzen besser steuern können. Zu den neuen Control Panel-Funktionen gehört die Möglichkeit, URLs hinzuzufügen, mit denen Adobe Campaign eine Verbindung herstellen kann, um Daten bzw. Dateien zu übertragen.

Weitere Informationen finden Sie im [entsprechenden Handbuch](instances-settings/using/url-permissions.md).
