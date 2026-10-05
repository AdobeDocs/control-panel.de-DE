---
product: campaign
solution: Campaign
title: Über die SFTP-Verwaltung
description: Weitere Informationen zur SFTP-Verwaltung im Control Panel
testing: SSECD-836 2
feature: Control Panel, SFTP Management
role: Admin
level: Intermediate
exl-id: b2c3be80-0d1b-4998-87ab-5280c6213f3d
TQID: 'https://experienceleague.adobe.com/UZHhTNCld6p1RFGh3DY-2r3VRiLNxCtP0anuPxPnWVE'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: ae9127b0-c11d-467b-903d-a84cef43f6ed
    internal-label: Control Panel
  - id: c5474392-5419-4296-9e41-f6f4ce4f6e9b
    internal-label: Administration
subfeature_v2:
  - id: e8445399-14db-4931-a0bb-477780230387
    internal-label: SFTP Management
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
source-git-commit: b2723b0683a305a992b710a37a3e47927e1fb65e
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 100%
---
# Über die SFTP-Verwaltung {#about-sftp-management}

Über das Control Panel können Sie alle SFTP-Server verwalten, die mit den Campaign-Instanzen verbunden sind, auf die Sie Zugriff haben. Die meisten Instanzen verfügen über verbundene SFTP-Server (in manchen Fällen sind Entwicklungs- und Staging-Instanzen mit keinen SFTP-Servern verbunden).

Der Zugriff auf SFTP-Server erfolgt über SFTP-Client-Software, die Sie online finden und herunterladen können. Um entweder über eine Client-Anwendung oder eine API eine Verbindung zu einem Server herzustellen, müssen Sie einen öffentlichen SSH-Schlüssel einrichten und die IP-Adresse, die die Verbindung zu Ihrem SFTP-Server herstellt, auf die Zulassungsliste setzen.

Im Control Panel können Sie die folgenden Aktionen ausführen, um Ihre SFTP-Server zu verwalten:

* Überwachen der **Speicherkapazität**,
* Verwalten der **Zulassungsauflistung von IP-Adressen**: Hinzufügen oder Löschen von IP-Adressbereichen für einen oder mehrere Server,
* Verwalten der **öffentlichen SSH-Schlüssel** für den Server-Zugriff.

Detaillierte Informationen zu jeder dieser Aktionen finden Sie in den folgenden Abschnitten.
