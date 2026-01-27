---
title: Aktuelle Version
description: Auf dieser Seite werden alle neuen Funktionen und Verbesserungen für das Control Panel aufgelistet.
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '150'
ht-degree: 100%

---

# Aktuelle Version {#control-panel-releases}

Diese Seite listet alle neuen Funktionen und Verbesserungen für das Control Panel auf.

## Oktober 2023 {#october-2023}

**Benutzeroberfläche**

* Control Panel ist jetzt in weiteren Sprachen verfügbar. [Weitere Informationen](../discover/using/discovering-the-interface.md#supported-languages-languages)

**Überwachung aktiver Profile**

* Sie können jetzt die Anzahl der aktiven Profile überwachen, die Ihnen für Ihre Organisation zustehen, sowie die Gesamtzahl der in Ihrer Organisation verwendeten Profile in allen Instanzen, wenn Sie mehrere Instanzen verwenden. [Weitere Informationen](../performance-monitoring/using/active-profiles-monitoring.md)

**DMARC-Einträge**

* Mehrere E-Mail-Adressen können jetzt E-Mails zu aggregierten Berichten und Fehlerberichten erhalten. [Weitere Informationen](../subdomains-certificates/using/dmarc.md)
* Es wurden Änderungen für den Fall vorgenommen, dass sowohl DMARC- als auch BIMI-Einträge für eine Subdomain vorhanden sind:

   * DMARC-Einträge können nicht gelöscht werden. Wenn Sie einen Eintrag löschen möchten, müssen Sie zuerst den BIMI-Eintrag löschen.
   * DMARC-Einträge können bearbeitet werden, aber das Herunterstufen der Richtlinie auf „Keine“ ist nicht zulässig und der Prozentwert muss 100 betragen.

