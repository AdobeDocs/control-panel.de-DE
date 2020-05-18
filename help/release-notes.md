---
title: Control Panel-Versionen
translation-type: tm+mt
source-git-commit: 49d84c42446ed1fc996b9d57005565b15ca24e77
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 61%

---


# Control Panel-Versionen {#control-panel-releases}

Hier finden Sie Informationen zu den neuesten Versionen von Control Panel.

>[!NOTE]
>
>Beachten Sie, dass die Systemsteuerung nur für Kunden verfügbar ist, die auf AWS gehostet werden, mit Ausnahme von Hybrid-Umgebung, die noch nicht unterstützt werden. Für den Zugriff auf das Control Panel sind keine Aktualisierungen erforderlich. Sie müssen Administrator sein, um darauf zugreifen zu können.

## Mai 2020 (#Mai-2020)

**GPG-Schlüsselverwaltung**

Über die Systemsteuerung können Sie jetzt ein Paar GPG-Schlüssel generieren, damit Sie die Daten, die von außen in die Kampagne gelangen, einfach entschlüsseln können. Darüber hinaus haben wir eine Funktion hinzugefügt, mit der Sie einen öffentlichen GPG-Schlüssel installieren können, um Daten zu verschlüsseln, die Kampagne verlassen. [mehr dazu](instances-settings/using/gpg-keys-management.md)

**Zertifikatverwaltung für CNAME-Subdomänen**

Über die Systemsteuerung können Sie jetzt die SSL-Zertifikate Ihrer Subdomänen erneuern, die mit der CNAME-Methode delegiert wurden. [mehr dazu](subdomains-certificates/using/renewing-subdomain-certificate.md)

## April 2020 {#april-2020}

**Verwaltung von Google TXT-Einträgen**

Fügen Sie allen Subdomains, die zum Senden von E-Mails an Gmail-Adressen über das Campaign Control Panel verwendet werden, einen Eintrag der TXT-Websiteüberprüfung von Google hinzu. [mehr dazu](subdomains-certificates/using/managing-txt-records.md)

**Überwachung von Datenbankspeicherplatz**

Kampagne Control Panel ist mit Datenbanküberwachungsfunktionen ausgestattet, mit denen Sie die Auslastung Ihres Datenbankplatzes bei Bedarf und im Zeitverlauf Ansicht haben können. [mehr dazu](performance-monitoring/using/database-monitoring.md)

**Warnungen per E-Mail**

Das Control Panel für Kampagnen verfügt über Echtzeit-E-Mail-Warnfunktionen, mit denen Sie sich bei der Systemsteuerung anmelden und sich für den Empfang von Warnhinweisen anmelden können, wenn Ihr System Gefahr läuft, dass die Leistung beeinträchtigt wird, oder eine Aktion erforderlich ist, um eine hohe Leistung für die Zukunft sicherzustellen. [Mehr dazu](performance-monitoring/using/email-alerting.md)

## Januar 2020 {#january-2020}

*22. Januar 2020*

Für Admin-Benutzer wurden neue Funktionen hinzugefügt, mit denen sie über das Control Panel Subdomains zuweisen und SSL-Zertifikate verlängern können.

Weitere Informationen finden Sie auf den folgenden Seiten:
* [Einrichten einer neuen Subdomain](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Verlängern des SSL-Zertifikats einer Subdomain](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Diese Funktionen werden als Beta-Version verfügbar sein und häufigen Aktualisierungen und Änderungen ohne vorherige Ankündigung unterliegen.

## September 2019 {#september-2019}

*16. September 2019*

Für Admin-Benutzer wurden neue Funktionen hinzugefügt, mit denen sie IP-Adressen auf die Whitelist setzen können, um eine Verbindung zu Campaign Classic-Instanzen herzustellen.
Außerdem können Admin-Benutzer jetzt die Liste der Campaign Classic-Instanzen und die Berechtigung für Build-Upgrades einsehen.

Weitere Informationen finden Sie in der [entsprechenden Dokumentation](instances-settings/using/ip-whitelisting-instance-access.md).

## August 2019 {#august-2019}

Für Admin-Benutzer wurden neue Funktionen hinzugefügt, durch die sie benachrichtigt werden, bevor die SSL-Zertifikate für ihre Domains ablaufen. Weitere Informationen finden Sie im [entsprechenden Handbuch](subdomains-certificates/using/monitoring-ssl-certificates.md).

Darüber hinaus können die Admin-Benutzer jetzt SSH-Schlüssel löschen, die für den Zugriff auf SFTP-Server hinzugefügt wurden.

## Juli 2019 {#july-2019}

Für Admin-Benutzer wurden neue Funktionen hinzugefügt, mit denen sie die Einstellungen der Campaign Classic-Instanzen besser steuern können. Zu den neuen Control Panel-Funktionen gehört die Möglichkeit, URLs hinzuzufügen, mit denen Adobe Campaign eine Verbindung herstellen kann, um Daten bzw. Dateien zu übertragen.

Weitere Informationen finden Sie im [entsprechenden Handbuch](instances-settings/using/url-permissions.md).
