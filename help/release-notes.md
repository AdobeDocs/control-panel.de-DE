---
title: Control Panel-Versionen
translation-type: tm+mt
source-git-commit: 0bea4b1508305254d53eb23d45bd62944a32495a
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 82%

---


# Control Panel-Versionen {#control-panel-releases}

Hier finden Sie Informationen zu den neuesten Versionen von Control Panel.

>[!NOTE]
>
>Beachten Sie, dass das Control Panel nur für Kunden verfügbar ist, die auf AWS gehostet werden (mit Ausnahme der hybriden Umgebungen, die noch nicht unterstützt werden). Für den Zugriff auf das Control Panel sind keine Aktualisierungen erforderlich. Sie müssen Administrator sein, um darauf zugreifen zu können.

## Juni 2020{#june-2020}

**Entfernung von &#39;Whitelist&#39;/&#39;Blacklist&#39;**

Sowohl die Begriffe &quot;Whitelist&quot;als auch &quot;Blacklist&quot;wurden aus der Dokumentation zum Adobe Campaign entfernt. Einige dieser Begriffe sind möglicherweise in der Produktoberfläche, in Optionsnamen und im internen Code noch vorhanden, werden jedoch in den kommenden Kampagnen-Versionen mit &quot;blockierungsliste&quot;und &quot;zulassungsliste&quot;ersetzt.

**Überwachung aktiver Profile**

Über die Systemsteuerung können Sie jetzt die Anzahl der aktiven Profil überwachen, die von Ihren Instanzen verwendet und für Rechnungszwecke gezählt werden. [mehr dazu](performance-monitoring/using/active-profiles-monitoring.md)

>[!IMPORTANT]
>
>Die Überwachung aktiver Profile über das Control Panel befindet sich in der Beta-Phase und unterliegt häufigen Aktualisierungen und Änderungen ohne Vorankündigung.
>
>Die Funktion steht Kunden zur Verfügung, die ab Build 10368 von Campaign Standard und Build 8931 von Campaign Classic auf AWS gehostet werden. Wenn Sie einen früheren Build verwenden, müssen Sie ein Upgrade durchführen, um diese Funktion zu verwenden.

## Mai 2020 {#may-2020}

**Zertifikatverwaltung für CNAME-Subdomains**

Das Control Panel ermöglicht es Ihnen jetzt, die SSL-Zertifikate Ihrer Subdomains zu erneuern, die mit der CNAME-Methode zugewiesen wurden. [Mehr dazu](subdomains-certificates/using/renewing-subdomain-certificate.md)

## April 2020 {#april-2020}

**Verwaltung von Google TXT-Einträgen**

Fügen Sie allen Subdomains, die zum Senden von E-Mails an Gmail-Adressen über das Campaign Control Panel verwendet werden, einen Eintrag der TXT-Websiteüberprüfung von Google hinzu. [Mehr dazu](subdomains-certificates/using/managing-txt-records.md)

**Überwachung von Datenbankspeicherplatz**

Das Campaign Control Panel verfügt über Funktionen zur Datenbanküberwachung, mit denen Sie die Auslastung Ihres Datenbankspeicherplatzes zu einem bestimmten Zeitpunkt und im Zeitverlauf anzeigen können. [Mehr dazu](performance-monitoring/using/database-monitoring.md)

**Warnungen per E-Mail**

Das Campaign Control Panel bietet Funktionen zum Empfang von E-Mail-Warnungen in Echtzeit. Wenn Sie sich beim Control Panel anmelden und Warnhinweise abonnieren, werden Sie benachrichtigt, wenn Ihrem System eine Leistungsverschlechterung droht oder eine Aktion erforderlich ist, um eine künftig hohe Leistung sicherzustellen. [Mehr dazu](performance-monitoring/using/email-alerting.md)

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

Es wurden neue Funktionen hinzugefügt, mit denen Administratoren der zulassungsliste IP-Adressen hinzufügen können, um eine Verbindung zu Campaign Classic-Instanzen herzustellen.
Außerdem können Admin-Benutzer jetzt die Liste der Campaign Classic-Instanzen und die Berechtigung für Build-Upgrades einsehen.

Weitere Informationen finden Sie in der [entsprechenden Dokumentation](instances-settings/using/ip-whitelisting-instance-access.md).

## August 2019 {#august-2019}

Für Admin-Benutzer wurden neue Funktionen hinzugefügt, durch die sie benachrichtigt werden, bevor die SSL-Zertifikate für ihre Domains ablaufen. Weitere Informationen finden Sie im [entsprechenden Handbuch](subdomains-certificates/using/monitoring-ssl-certificates.md).

Darüber hinaus können die Admin-Benutzer jetzt SSH-Schlüssel löschen, die für den Zugriff auf SFTP-Server hinzugefügt wurden.

## Juli 2019 {#july-2019}

Für Admin-Benutzer wurden neue Funktionen hinzugefügt, mit denen sie die Einstellungen der Campaign Classic-Instanzen besser steuern können. Zu den neuen Control Panel-Funktionen gehört die Möglichkeit, URLs hinzuzufügen, mit denen Adobe Campaign eine Verbindung herstellen kann, um Daten bzw. Dateien zu übertragen.

Weitere Informationen finden Sie im [entsprechenden Handbuch](instances-settings/using/url-permissions.md).
