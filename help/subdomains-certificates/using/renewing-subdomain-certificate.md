---
title: Verlängern des SSL-Zertifikats einer Subdomain
description: Erfahren Sie, wie Sie die Zertifikate Ihrer Subdomains verlängern.
translation-type: tm+mt
source-git-commit: c44f6800a0f7905fe9e5619388c7007f0af8f973

---


# Verlängern des SSL-Zertifikats einer Subdomain {#renewing-subdomains-ssl-certificates}

>[!IMPORTANT]
>
>Die Subdomänendelegation der Kontrollgruppe wird bis Ende Januar als Beta-Version verfügbar sein, vorbehaltlich häufiger Aktualisierungen und Änderungen ohne Vorankündigung.

## Über die Zertifikatverlängerung {#about-certificate-renewal-process}

Der Verlängerungsprozess eines SSL-Zertifikats besteht aus drei Schritten:

1. **Generieren der Certificate Signing Request (CSR)** Die Adobe-Kundenunterstützung generiert eine CSR für Sie. Sie müssen einige Informationen angeben, die für die Generierung der CSR erforderlich sind (z. B. Gebrauchsname, Organisationsname und Adresse).
1. **Kauf des SSL-Zertifikats**
Sobald die CSR generiert wurde, können Sie sie herunterladen und zum Kauf des SSL-Zertifikats bei der von Ihrem Unternehmen genehmigten Zertifizierungsstelle verwenden.
1. **Installation des SSL-Zertifikats**
Nachdem Sie das SSL-Zertifikat erworben haben, können Sie es in der gewünschten Subdomain installieren.

>[!NOTE]
>
>Die Erneuerung von SSL-Zertifikaten über die Systemsteuerung ist nur für **vollständig delegierte Subdomänen** verfügbar.

## Generieren einer Certificate Signing Request (CSR) {#generating-csr}

Gehen Sie wie folgt vor, um eine Certificate Signing Request (CSR) zu erstellen:

1. Wählen Sie zuerst auf der Karte **[!UICONTROL Subdomains &amp; Zertifikate]**die gewünschte Instanz und danach**[!UICONTROL  Zertifikat verwalten]** aus.

   ![](assets/renewal1.png)

1. Wählen Sie **[!UICONTROL CSR generieren]**und dann**[!UICONTROL  Weiter]** aus, um den Assistenten zu starten, der Sie durch den CSR-Generierungsprozess führt.

   ![](assets/renewal2.png)

1. Daraufhin wird ein Formular mit allen Details angezeigt, die zum Generieren Ihrer CSR erforderlich sind.

   Make sure you fill in the requested information fully and accurately, otherwise the certificate may not be renewed (contact your internal team, Security and IT teams if necessary), then click **[!UICONTROL Next]**.

   * **[!UICONTROL Einrichtung]**: Name der amtlichen Einrichtung.
   * **[!UICONTROL Referat]**Einrichtung: mit der Subdomäne verknüpfte Einheit (Beispiel: Marketing, IT).
   * **[!UICONTROL Instanz]**(vorausgefüllt): URL der der Subdomäne zugeordneten Kampagneninstanz.
   ![](assets/renewal3.png)

1. Wählen Sie zuerst die Subdomains aus, die in die CSR einbezogen werden sollen, und danach **[!UICONTROL OK]**.

   ![](assets/renewal4.png)

1. Die ausgewählten Subdomains werden in der Liste angezeigt. Wählen Sie für jede davon die einzubeziehenden Subdomains und dann **[!UICONTROL Weiter]**aus.

   ![](assets/renewal5.png)

1. In einer Zusammenfassung werden alle Subdomains angezeigt, die in die CSR einbezogen werden sollen. Bestätigen Sie Ihre Anfrage durch die Auswahl von **[!UICONTROL Senden]**.

   ![](assets/renewal6.png)

1. Die .csr-Datei wird entsprechend Ihrer Auswahl automatisch generiert und heruntergeladen. Mit dieser Datei können Sie nun das SSL-Zertifikat bei der von Ihrem Unternehmen genehmigten Zertifizierungsstelle erwerben.

## Kaufen eines Zertifikats mit der CSR {#purchasing-certificate}

Nachdem Sie eine Certificate Signing Request (CSR) über das Control Panel generiert haben, können Sie bei einer von Ihrer Organisation genehmigten Zertifizierungsstelle ein SSL-Zertifikat kaufen.

## Installieren des SSL-Zertifikats {#installing-ssl-certificate}

Nachdem Sie ein SSL-Zertifikat erworben haben, können Sie es auf Ihrer Instanz installieren. Bevor Sie fortfahren, stellen Sie sicher, dass Sie die folgenden Voraussetzungen kennen:

* Die Zertifikatsignaturanforderung (Certificate Signing Request, CSR) muss über die Systemsteuerung generiert worden sein. Andernfalls können Sie das Zertifikat nicht über die Systemsteuerung installieren.
* Stellen Sie sicher, dass die Anforderung zur Zertifikatsignierung (Certificate Signing Request, CSR) mit der Subdomäne übereinstimmt, die an Adobe delegiert wurde. Es kann beispielsweise nicht mehr Subdomänen enthalten, als die delegierte Domäne.
* Das Zertifikat muss ein aktuelles Datum haben. Es ist nicht möglich, Zertifikate mit Terminen in der Zukunft zu installieren.

Gehen Sie wie folgt vor, um das Zertifikat zu installieren:

1. Wählen Sie auf der Karte **[!UICONTROL Subdomains &amp; Zertifikate]**zuerst die gewünschte Instanz und danach**[!UICONTROL  Zertifikat verwalten]** aus.

   ![](assets/renewal1.png)

1. Wählen Sie **[!UICONTROL Installieren eines SSL-Zertifikats]**und dann**[!UICONTROL  Weiter]** aus, um den Assistenten zu starten, der Sie durch den Zertifikatinstallationsprozess führt.

   ![](assets/install1.png)

1. Wählen Sie die .zip-Datei aus, die das zu installierende Zertifikat enthält, und wählen Sie danach **[!UICONTROL Senden]**aus.

   ![](assets/install2.png)

Nach der Installation des SSL-Zertifikats werden das Ablaufdatum und das Statussymbol des Zertifikats entsprechend aktualisiert.

Die URL-Adresse Ihrer Subdomäne ändert sich von **http** in **https**.
