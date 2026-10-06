---
product: campaign
solution: Campaign
title: Verwalten von TXT-Einträgen
description: Erfahren Sie, wie Sie TXT-Einträge zur Verifizierung von Domain-Besitz verwalten können.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: 013d6674-0988-4553-a23e-b3ec23da5323
TQID: 'https://experienceleague.adobe.com/G8eirPm9hY0XRZTtMOBpmdwxuo3-Uvdo9LQjiSiElPU'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: ae9127b0-c11d-467b-903d-a84cef43f6ed
    internal-label: Control Panel
  - id: a7760dfc-5c44-4d77-bb68-c50b1e265c93
    internal-label: Security and privacy
subfeature_v2:
  - id: f807e46f-d823-43a9-98be-82e0b2f3a05c
    internal-label: Subdomains and certificates
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: b2723b0683a305a992b710a37a3e47927e1fb65e
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 100%
---
# Erste Schritte mit TXT-Einträgen {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="Verwalten von TXT-Einträgen"
>abstract="TXT-Einträge sind eine Art von DNS-Einträgen, die der Bereitstellung von Textinformationen zu einer Domain dienen und von externen Quellen gelesen werden können. Mit Control Panel können Sie Ihren Subdomains drei Arten von Einträgen hinzufügen: Google Site-Überprüfungs-, DMARC- und BIMI-Einträge."

## Über TXT-Einträge {#about}

TXT-Einträge sind eine Art von DNS-Einträgen, die der Bereitstellung von Textinformationen zu einer Domain dienen und von externen Quellen gelesen werden können. Mit Control Panel können Sie Ihren Subdomains drei Eintragstypen hinzufügen:

* **Google TXT-Einträge** erlauben Ihnen zu bestätigen, dass Sie Ihre Domain besitzen, was hohe Posteingangsraten und niedrige Spam-Raten für Ihre E-Mails sicherstellt. [Erfahren Sie, wie Sie Google TXT-Einträge hinzufügen](managing-txt-records.md)
* **DMARC-Einträge** bieten eine Möglichkeit, die Absender-Domain zu authentifizieren und die unbefugte Nutzung der Domain für böswillige Zwecke zu verhindern. [Erfahren Sie, wie Sie DMARC-Einträge hinzufügen](dmarc.md)
* **BIMI-Einträge** ermöglichen es Ihnen, ein genehmigtes Logo neben Ihren E-Mails in den Postfächern von E-Mail-Anbietern anzuzeigen, um die Markenerkennung und das Vertrauen zu fördern. [Erfahren Sie, wie Sie BIMI-Einträge hinzufügen](bimi.md)

## Überwachen der Einträge Ihrer Subdomains {#monitor}

Sie können alle TXT-Einträge überwachen, die für jede Subdomain hinzugefügt wurden, indem Sie auf die Details der Subdomains zugreifen.

In diesem Bildschirm werden alle TXT-Einträge für die ausgewählte Subdomain mit Informationen in der Spalte „Wert“ ihrer Konfiguration angezeigt. Um einen Google TXT-, DMARC- oder BIMI-Eintrag zu löschen, klicken Sie auf die Schaltfläche mit den Auslassungspunkten und wählen Sie dann „Löschen“ aus. Sie können DMARC- und BIMI-Einträge bei Bedarf auch bearbeiten.

![](assets/txt-records.png)
