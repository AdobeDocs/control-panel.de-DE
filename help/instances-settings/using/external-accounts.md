---
product: campaign
solution: Campaign
title: MID-/RT-Instanzen verbinden
description: Erfahren Sie, wie Sie MID-/RT-Instanzen mit dem Control Panel verbinden.
feature: Control Panel
role: Architect
level: Intermediate
source-git-commit: 1b712300bd7a1ef8dc784fa977f938bacc4c5e5b
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 7%

---


# MID-/RT-Instanzen verbinden

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_url"
>title="Details der Subdomain"
>abstract="In diesem Bildschirm können Kunden mit einem Hybrid-Hosting-Modell ihre in ihrer Marketing-Instanz vorhandenen MID-/RT-Instanzen bereitstellen, um bestimmte Aktionen im Control Panel durchzuführen."

Mit dem Control Panel können Kunden mit einem Hybrid-Hosting-Modell bestimmte Aktionen im Control Panel ausführen, indem sie ihre MID-/RT-Instanzen in ihrer Marketing-Instanz angeben. Weitere Informationen zu Hosting-Modellen finden Sie unter [Dokumentation zu Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/architecture-and-hosting-models/hosting-models-lp/hosting-models.html).

## Verbinden einer MID/RT-Instanz {#connect}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_operator"
>title="Details der Subdomain"
>abstract="Kennung des Operators, der in der Client-Konsole zum Hinzufügen der MID/RT-Instanz in der Marketing-Instanz verwendet wird."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_password"
>title="Details der Subdomain"
>abstract="Kennwort des Operators, der in der Client-Konsole zum Hinzufügen der MID/RT-Instanz in der Marketing-Instanz verwendet wird."

Gehen Sie wie folgt vor, um eine MID/RT-Instanz im Control Panel bereitzustellen:

1. Im **[!UICONTROL Instanzeneinstellungen]** -Karte, wählen Sie die **[!UICONTROL Externe Konten]** Registerkarte.

1. Wählen Sie die Marketinginstanz aus der Dropdown-Liste aus und klicken Sie auf **[!UICONTROL Neue URL hinzufügen]**.

   ![](assets/external-account-addbutton.png)

1. Geben Sie Informationen über die zu verbindende MID-/RT-Instanz an:
   * **[!UICONTROL URL]**: URL der Instanz,
   * **[!UICONTROL Operator]** / **[!UICONTROL Passwort]**: Anmeldeinformationen des Operators, der in der Client-Konsole zum Hinzufügen der MID/RT-Instanz in der Marketing-Instanz verwendet wird.

   ![](assets/external-account-add.png)

1. Klicken Sie zur Bestätigung auf **[!UICONTROL Speichern]**.

Ihre Instanz ist jetzt mit dem Control Panel verbunden. Sie können eine Verbindung jederzeit entfernen oder deaktivieren, indem Sie sie aus der Liste auswählen.

![](assets/external-account-edit.png)

## Verfügbare Funktionen für MID-/RT-Instanzen {#capabilities}

Sobald eine MID-/RT-Instanz mit dem Control Panel verbunden ist, können Sie die unten aufgeführten Funktionen nutzen, um sie zu überwachen:

* [Details Ihrer Instanz anzeigen](../../instances-settings/using/instance-details.md),
* [Fügen Sie der Zulassungsliste IP-Adressen hinzu, um auf Ihre Instanzen zuzugreifen](../../instances-settings/using/ip-allow-listing-instance-access.md),
* [Anzeigen von Informationen zu delegierten Subdomains](../../subdomains-certificates/using/setting-up-new-subdomain.md),
* [Informationen zu SSL-Zertifikaten anzeigen](../../subdomains-certificates/using/monitoring-ssl-certificates.md).
