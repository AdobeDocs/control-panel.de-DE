---
product: campaign
solution: Campaign
title: Control Panel-Versionen
description: Aktuelle Control Panel-Versionshinweise.
feature: Control Panel
role: Architect
level: Beginner
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
translation-type: ht
source-git-commit: 4c8347f7b0f4a776ea726f02029ea1c92a83406a
workflow-type: ht
source-wordcount: '631'
ht-degree: 100%

---

# Control Panel-Versionen {#control-panel-releases}

Hier finden Sie Informationen zu den aktuellen Versionen des Control Panel.

>[!NOTE]
>
>Das Control Panel steht allen Administratoren zur Verfügung. Die Schritte, um einem Benutzer Administratorzugriff zu gewähren, finden Sie in [diesem Abschnitt](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=de#discover-control-panel).
>
>Beachten Sie für Campaign Classic, dass Ihre Instanz auf AWS gehostet und mit dem neuesten [Gold Standard](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/gs-release/gs-overview.html?lang=de)-Build oder dem neuesten [allgemein verfügbaren Build (21.1)](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/latest-release.html?lang=de#release-notes) aktualisiert werden muss. Erfahren Sie in [diesem Abschnitt](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=de#getting-your-campaign-version), wie Sie Ihre Version überprüfen. Um zu überprüfen, ob Ihre Instanz auf AWS gehostet wird, folgen Sie den Schritten auf [dieser Seite](faq.md).

## Oktober 2020 {#october-2020}

**Subdomain-Konfiguration mit CNAME**

Im Control Panel können Sie jetzt mit CNAME eine Subdomain für die Verwendung mit Adobe direkt über die Benutzeroberfläche konfigurieren. [Mehr dazu](subdomains-certificates/using/setting-up-new-subdomain.md)

**Verbesserungen bei der Datenbanküberwachung**

Die Datenbanküberwachung wurde um zusätzliche Metriken erweitert, sodass Sie detaillierte Informationen zu den Ressourcen erhalten können, die Speicherplatz in Ihrer Datenbank belegen. [Mehr dazu](performance-monitoring/using/database-monitoring.md)

## Juni 2020{#june-2020}

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

**Warnungen per E-Mail**

Das Campaign Control Panel bietet Funktionen zum Empfang von E-Mail-Warnungen in Echtzeit. Wenn Sie sich beim Control Panel anmelden und Warnhinweise abonnieren, werden Sie benachrichtigt, wenn Ihrem System eine Leistungsverschlechterung droht oder eine Aktion erforderlich ist, um eine künftig hohe Leistung sicherzustellen. [Mehr dazu](performance-monitoring/using/email-alerting.md)

## Januar 2020 {#january-2020}

*22. Januar 2020*

Für Admin-Benutzer wurden neue Funktionen hinzugefügt, mit denen sie über das Control Panel Subdomains konfigurieren und SSL-Zertifikate verlängern können.

Weitere Informationen finden Sie auf den folgenden Seiten:
* [Einrichten einer neuen Subdomain](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Verlängern des SSL-Zertifikats einer Subdomain](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Diese Funktionen werden als Beta-Version verfügbar sein und häufigen Aktualisierungen und Änderungen ohne vorherige Ankündigung unterliegen.

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
