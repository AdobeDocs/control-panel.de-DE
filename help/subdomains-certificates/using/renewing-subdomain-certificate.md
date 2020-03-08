---
title: Verlängern des SSL-Zertifikats einer Subdomain
description: Erfahren Sie, wie Sie die Zertifikate Ihrer Subdomains verlängern.
translation-type: tm+mt
source-git-commit: f22e356b283ee2601c948d5c1d514a9a59c58451

---


# Verlängern des SSL-Zertifikats einer Subdomain {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id=&quot;cp_add_ssl_certificate&quot;
>title=&quot;SSL-Zertifikat hinzufügen&quot;
>abstract=&quot;Um ein SSL-Zertifikat hinzuzufügen, müssen Sie ein CSR generieren, das SSL-Zertifikat für Ihre Subdomänen erwerben und das Zertifikat-Bundle installieren.&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr&quot; text=&quot;Generating a Certificate Signing Request (CSR)&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#installing-ssl-certificate&quot; text=&quot;So installieren Sie ein SSL-Zertifikat&quot;

>[!IMPORTANT]
>
>Die Subdomain-Zuweisung über das Control Panel befindet sich in der Beta-Phase und unterliegt häufigen Aktualisierungen und Änderungen ohne Vorankündigung.

## Über die Zertifikatsverlängerung {#about-certificate-renewal-process}

Der Verlängerungsprozess eines SSL-Zertifikats besteht aus drei Schritten:

1. **Generieren der Certificate Signing Request (CSR)** Die Adobe-Kundenunterstützung generiert eine CSR für Sie. Sie müssen einige Informationen angeben, die für die Generierung der CSR erforderlich sind (z. B. Gebrauchsname, Organisationsname und Adresse).
1. **Kauf des SSL-Zertifikats**
Sobald die CSR generiert wurde, können Sie sie herunterladen und zum Kauf des SSL-Zertifikats bei der von Ihrem Unternehmen genehmigten Zertifizierungsstelle verwenden.
1. **Installation des SSL-Zertifikats**
Nachdem Sie das SSL-Zertifikat erworben haben, können Sie es in der gewünschten Subdomain installieren.

>[!NOTE]
>
>Die Verlängerung von SSL-Zertifikaten über das Control Panel ist nur für **vollständig zugewiesene Subdomains** verfügbar.

## Generieren einer Certificate Signing Request (CSR) {#generating-csr}

>[!CONTEXTUALHELP]
>id=&quot;cp_generate_csr&quot;
>title=&quot;CSR generieren&quot;
>abstract=&quot;Certificate Signing Request muss für die Instanz und Subdomänen, die Sie vor dem Erwerb eines Zertifikats sichern möchten, generiert werden.&quot;

>[!CONTEXTUALHELP]
>id=&quot;cp_select_subdomains&quot;
>title=&quot;Auswählen der Subdomänen für Ihre CSR&quot;
>abstract=&quot;Sie können festlegen, dass alle oder nur bestimmte Subdomänen in Ihre Zertifikatsignaturanforderung aufgenommen werden sollen. Nur ausgewählte Subdomänen werden über das erworbene SSL-Zertifikat zertifiziert.&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr&quot; text=&quot;Generating a Certificate Signing Request (CSR)&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/subdomains-branding.html&quot; text=&quot;Informationen zum Branding von Subdomänen&quot;

Gehen Sie wie folgt vor, um eine Certificate Signing Request (CSR) zu erstellen:

1. Wählen Sie auf der **[!UICONTROL Subdomains & Certificates]** Karte die gewünschte Instanz aus und klicken Sie dann auf die **[!UICONTROL Manage Certificate]** Schaltfläche.

   ![](assets/renewal1.png)

1. Select **[!UICONTROL Generate a CSR]**, then click **[!UICONTROL Next]** to launch the wizard that will guide you through the CSR generation process.

   ![](assets/renewal2.png)

1. Daraufhin wird ein Formular mit allen Details angezeigt, die zum Generieren Ihrer CSR erforderlich sind.

   Make sure you fill in the requested information fully and accurately, otherwise the certificate may not be renewed (contact your internal team, Security and IT teams if necessary), then click **[!UICONTROL Next]**.

   * **[!UICONTROL Organization]**: Name der amtlichen Einrichtung.
   * **[!UICONTROL Organization Unit]**: mit der Subdomäne verknüpfte Einheit (Beispiel: Marketing, IT).
   * **[!UICONTROL Instance]** (Fertigspritze): URL der der Subdomäne zugeordneten Kampagneninstanz.
   ![](assets/renewal3.png)

1. Wählen Sie zuerst die Subdomains aus, die in die CSR einbezogen werden sollen, und danach **[!UICONTROL OK]**.

   ![](assets/renewal4.png)

1. Die ausgewählten Subdomains werden in der Liste angezeigt. For each of them, select the subdomains to include, then click **[!UICONTROL Next]**.

   ![](assets/renewal5.png)

1. In einer Zusammenfassung werden alle Subdomains angezeigt, die in die CSR einbezogen werden sollen. Click **[!UICONTROL Submit]** to confirm your request.

   ![](assets/renewal6.png)

1. Die .csr-Datei wird entsprechend Ihrer Auswahl automatisch generiert und heruntergeladen. Mit dieser Datei können Sie nun das SSL-Zertifikat bei der von Ihrem Unternehmen genehmigten Zertifizierungsstelle erwerben.

   >[!NOTE]
   >
   >Wenn die CSR nicht gespeichert/heruntergeladen wird, geht sie verloren und Sie müssen sie erneut generieren.

## Kaufen eines Zertifikats mit der CSR {#purchasing-certificate}

Nachdem Sie eine Certificate Signing Request (CSR) über das Control Panel generiert haben, können Sie bei einer von Ihrer Organisation genehmigten Zertifizierungsstelle ein SSL-Zertifikat kaufen.

## Installieren des SSL-Zertifikats {#installing-ssl-certificate}

>[!CONTEXTUALHELP]
>id=&quot;cp_install_ssl_certificate&quot;
>title=&quot;SSL-Zertifikat installieren&quot;
>abstract=&quot;Installieren Sie das SSL-Zertifikat, das Sie bei der von Ihrem Unternehmen zugelassenen Zertifizierungsstelle erworben haben.&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/subdomains-branding.html&quot; text=&quot;Informationen zum Branding von Subdomänen&quot;

Sobald Sie ein SSL-Zertifikat gekauft haben, können Sie es auf Ihrer Instanz installieren. Bevor Sie fortfahren, achten Sie auf folgende Voraussetzungen:

* Die Certificate Signing Request (CSR) muss über das Control Panel generiert worden sein. Andernfalls können Sie das Zertifikat nicht über das Control Panel installieren.
* Die Certificate Signing Request (CSR) sollte mit der Subdomain übereinstimmen, die Adobe zugewiesen wurde. Sie kann beispielsweise nicht mehr Subdomains enthalten als diejenige, die zugewiesen wurde.
* Das Datum des Zertifikats muss aktuell sein. Es ist nicht möglich, Zertifikate mit einem Datum in der Zukunft zu installieren. Zertifikate dürfen nicht abgelaufen sein (d. h. gültiges Start- und Enddatum).
* Das Zertifikat muss von einer vertrauenswürdigen Zertifizierungsstelle (CA) wie Comodo, DigiCert, GoDaddy usw. ausgestellt sein.
* Die Größe des Zertifikats darf maximal 2048 Bit betragen und der Algorithmus muss vom Typ RSA sein.
* Das Zertifikat muss im X.509 PEM-Format vorliegen.
* SAN-Zertifikate werden unterstützt.
* Wildcard-Zertifikate werden nicht unterstützt.
* Die ZIP-Datei bzw. das Zertifikat darf nicht passwortgeschützt sein.
* Die ZIP-Datei darf – möglichst in einzelnen Dateien – nur Folgendes enthalten:
   * End-Entity-Zertifikat.
   * Intermediate-Zertifikatskette (in der richtigen Reihenfolge angeordnet).
   * Root-Zertifikat (optional).

Gehen Sie wie folgt vor, um das Zertifikat zu installieren:

1. Wählen Sie auf der **[!UICONTROL Subdomains & Certificates]** Karte die gewünschte Instanz aus und klicken Sie dann auf die **[!UICONTROL Manage Certificate]** Schaltfläche.

   ![](assets/renewal1.png)

1. Click **[!UICONTROL Install SSL Certificate]**, then **[!UICONTROL Next]** to launch the wizard that will guide you through the certificate installation process.

   ![](assets/install1.png)

1. Select the .zip file that contains the certificate to install, then click **[!UICONTROL Submit]**.

   ![](assets/install2.png)

Nach der Installation des SSL-Zertifikats werden das Ablaufdatum und das Statussymbol des Zertifikats entsprechend aktualisiert.

**Verwandte Themen:**

* [Hinzufügen von SSL-Zertifikaten (Tutorial-Video)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [Subdomain-Branding](../../subdomains-certificates/using/subdomains-branding.md)
* [Überwachen von Subdomains](../../subdomains-certificates/using/monitoring-subdomains.md)