---
title: Aktuelle Version
description: Auf dieser Seite werden alle neuen Funktionen und Verbesserungen für das Control Panel aufgelistet.
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 26%

---

# Aktuelle Version {#control-panel-releases}

Diese Seite listet alle neuen Funktionen und Verbesserungen für das Control Panel auf.

## Oktober 2023 {#october-2023}

**Benutzeroberfläche**

* Das Control Panel ist jetzt in zusätzlichen Sprachen verfügbar. [Weitere Informationen](../discover/using/discovering-the-interface.md#supported-languages-languages)

**Überwachen aktiver Profile**

* Sie können jetzt die Anzahl der aktiven Profile überwachen, die Sie für Ihr Unternehmen berechtigt sind, sowie die Gesamtzahl der in Ihrem Unternehmen verwendeten Profile in allen Instanzen, wenn Sie mehrere Instanzen verwenden. [Weitere Informationen](../performance-monitoring/using/active-profiles-monitoring.md)

**DMARC-Einträge**

* Mehrere E-Mail-Adressen können jetzt E-Mails zu aggregierten Berichten und Fehlerberichten erhalten. [Weitere Informationen](../subdomains-certificates/using/dmarc.md)
* Änderungen wurden vorgenommen, wenn sowohl DMARC- als auch BIMI-Datensätze für eine Subdomain vorhanden sind:

   * DMARC-Datensätze können nicht gelöscht werden. Wenn Sie einen Eintrag löschen möchten, müssen Sie zuerst den BIMI-Datensatz löschen.
   * DMARC-Einträge können bearbeitet werden, aber das Downgrade der Richtlinie auf &quot;Keine&quot;ist nicht zulässig und der Prozentwert muss 100 betragen.

