---
title: Verlängern des SSL-Zertifikats einer Subdomain
description: Erfahren Sie, wie Sie die Zertifikate Ihrer Subdomains verlängern.
translation-type: ht
source-git-commit: f08b0e68cf0a208b1385052510c06ca1eb679e63

---


# Verlängern des SSL-Zertifikats einer Subdomain {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="[!CONTEXTUALHELP]
>id=&quot;cp_add_ssl_certificate&quot;
>title=&quot;Hinzufügen von SSL-Zertifikaten&quot;
>abstract=&quot;Um ein SSL-Zertifikat hinzuzufügen, müssen Sie eine CSR generieren, das SSL-Zertifikat für Ihre Subdomain erwerben und das Zertifikat-Bundle installieren.&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/de-DE/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr&quot; text=&quot;Generieren einer Certificate Signing Request (CSR)&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/de-DE/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#installing-ssl-certificate&quot; text=&quot;Installieren eines SSL-Zertifikats&quot;"
>abstract="[!IMPORTANT]"
>additional-url="Die Subdomain-Zuweisung über das Control Panel befindet sich in der Beta-Phase und unterliegt häufigen Aktualisierungen und Änderungen ohne Vorankündigung." text="Über die Zertifikatsverlängerung {#about-certificate-renewal-process}"
>additional-url="Der Verlängerungsprozess eines SSL-Zertifikats besteht aus drei Schritten:" text="**Generieren der Certificate Signing Request (CSR)** Die Adobe-Kundenunterstützung generiert eine CSR für Sie. Sie müssen einige Informationen angeben, die für die Generierung der CSR erforderlich sind (z. B. Gebrauchsname, Organisationsname und Adresse)."

>**Kauf des SSL-Zertifikats**
Sobald die CSR generiert wurde, können Sie sie herunterladen und zum Kauf des SSL-Zertifikats bei der von Ihrem Unternehmen genehmigten Zertifizierungsstelle verwenden.
>
>**Installation des SSL-Zertifikats**
Nachdem Sie das SSL-Zertifikat erworben haben, können Sie es in der gewünschten Subdomain installieren.

## [!NOTE]

Die Verlängerung von SSL-Zertifikaten über das Control Panel ist nur für **vollständig zugewiesene Subdomains** verfügbar.

1. Generieren einer Certificate Signing Request (CSR) {#generating-csr}**
1. [!CONTEXTUALHELP]
>id=&quot;cp_generate_csr&quot;
>title=&quot;Generieren einer CSR&quot;
>abstract=&quot;Vor dem Kauf eines Zertifikats muss eine Certificate Signing Request für die Instanz und die Subdomains generiert werden, die Sie schützen möchten.&quot;**
1. [!CONTEXTUALHELP]
>id=&quot;cp_select_subdomains&quot;
>title=&quot;Auswählen der Subdomains für Ihre CSR&quot;
>abstract=&quot;Sie können auswählen, ob Sie alle oder nur bestimmte Subdomains in Ihre Certificate Signing Request aufnehmen möchten. Nur ausgewählte Subdomains werden über das erworbene SSL-Zertifikat zertifiziert.&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/de-DE/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr&quot; text=&quot;Generieren einer Certificate Signing Request (CSR)&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/de-DE/control-panel/using/subdomains-and-certificates/subdomains-branding.html&quot; text=&quot;Über Subdomain-Branding&quot;**

>[!NOTE]Gehen Sie wie folgt vor, um eine Certificate Signing Request (CSR) zu erstellen:
>
>Wählen Sie zuerst auf der Karte **[!UICONTROL Subdomains &amp; Zertifikate]** die gewünschte Instanz und danach **[!UICONTROL Zertifikat verwalten]** aus.**

## ![](assets/renewal1.png)

>[!CONTEXTUALHELP]
>id="cp_generate_csr"
>title="Wählen Sie **[!UICONTROL Erstellen einer CSR]** und dann **[!UICONTROL Weiter]** aus, um den Assistenten zu starten, der Sie durch den CSR-Generierungsprozess führt."
>abstract="![](assets/renewal2.png)"

>[!CONTEXTUALHELP]
>id="cp_select_subdomains"
>title="Daraufhin wird ein Formular mit allen Details angezeigt, die zum Generieren Ihrer CSR erforderlich sind."
>abstract="Vergewissern Sie sich, dass Sie die angeforderten Informationen vollständig und korrekt ausgefüllt haben. Anderenfalls kann das Zertifikat möglicherweise nicht verlängert werden. (Wenden Sie sich bei Bedarf an Ihr internes Team bzw. Ihr Sicherheits- oder IT-Team.) Wählen Sie dann **[!UICONTROL Weiter]** aus."
>additional-url="**[!UICONTROL Organisation]**: Offizieller Name der Organisation." text="**[!UICONTROL Organisationseinheit]**: Die mit der Subdomain verknüpfte Einheit (Beispiel: Marketing, IT)."
>additional-url="**[!UICONTROL Instanz]** (vorbelegt): URL der Campaign-Instanz, die mit der Subdomain verknüpft ist." text="![](assets/renewal3.png)"

Wählen Sie zuerst die Subdomains aus, die in die CSR einbezogen werden sollen, und danach **[!UICONTROL OK]**.

1. ![](assets/renewal4.png)]******

   Die ausgewählten Subdomains werden in der Liste angezeigt. Wählen Sie für jede davon die einzubeziehenden Subdomains und dann **[!UICONTROL Weiter]** aus.

1. ![](assets/renewal5.png)]******

   In einer Zusammenfassung werden alle Subdomains angezeigt, die in die CSR einbezogen werden sollen. Bestätigen Sie Ihre Anfrage durch die Auswahl von **[!UICONTROL Senden]**.

1. ![](assets/renewal6.png)

   Die .csr-Datei wird entsprechend Ihrer Auswahl automatisch generiert und heruntergeladen. Mit dieser Datei können Sie nun das SSL-Zertifikat bei der von Ihrem Unternehmen genehmigten Zertifizierungsstelle erwerben.****

   * [!NOTE]]**
   * **[!UICONTROL Wenn die CSR nicht gespeichert/heruntergeladen wird, geht sie verloren und Sie müssen sie erneut generieren.]**
   * Kaufen eines Zertifikats mit der CSR {#purchasing-certificate}]**
   ![](assets/renewal3.png)Nachdem Sie eine Certificate Signing Request (CSR) über das Control Panel generiert haben, können Sie bei einer von Ihrer Organisation genehmigten Zertifizierungsstelle ein SSL-Zertifikat kaufen.

1. Installieren des SSL-Zertifikats {#installing-ssl-certificate}]**

   [!CONTEXTUALHELP]
>id=&quot;cp_install_ssl_certificate&quot;
>title=&quot;Installieren von SSL-Zertifikaten&quot;
>abstract=&quot;Installieren Sie das SSL-Zertifikat, das Sie bei der von Ihrem Unternehmen zugelassenen Zertifizierungsstelle erworben haben.&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/de-DE/control-panel/using/subdomains-and-certificates/subdomains-branding.html&quot; text=&quot;Über Subdomain-Branding&quot;

1. Sobald Sie ein SSL-Zertifikat gekauft haben, können Sie es auf Ihrer Instanz installieren. Bevor Sie fortfahren, achten Sie auf folgende Voraussetzungen:****

   ![](assets/renewal5.png)Die Certificate Signing Request (CSR) muss über das Control Panel generiert worden sein. Andernfalls können Sie das Zertifikat nicht über das Control Panel installieren.

1. Die Certificate Signing Request (CSR) sollte mit der Subdomain übereinstimmen, die Adobe zugewiesen wurde. Sie kann beispielsweise nicht mehr Subdomains enthalten als diejenige, die zugewiesen wurde.****

   ![](assets/renewal6.png)Das Datum des Zertifikats muss aktuell sein. Es ist nicht möglich, Zertifikate mit einem Datum in der Zukunft zu installieren. Zertifikate dürfen nicht abgelaufen sein (d. h. gültiges Start- und Enddatum).

1. Das Zertifikat muss von einer vertrauenswürdigen Zertifizierungsstelle (CA) wie Comodo, DigiCert, GoDaddy usw. ausgestellt sein.

   >[!NOTE]Die Größe des Zertifikats darf maximal 2048 Bit betragen und der Algorithmus muss vom Typ RSA sein.
   >
   >Das Zertifikat muss im X.509 PEM-Format vorliegen.

## SAN-Zertifikate werden unterstützt.{#purchasing-certificate}

Wildcard-Zertifikate werden nicht unterstützt.

## Die ZIP-Datei bzw. das Zertifikat darf nicht passwortgeschützt sein.{#installing-ssl-certificate}

>[!CONTEXTUALHELP]
>id="cp_install_ssl_certificate"
>title="Die ZIP-Datei darf – möglichst in einzelnen Dateien – nur Folgendes enthalten:"
>abstract="End-Entity-Zertifikat."
>additional-url="Intermediate-Zertifikatskette (in der richtigen Reihenfolge angeordnet)." text="Root-Zertifikat (optional)."

Gehen Sie wie folgt vor, um das Zertifikat zu installieren:

* Wählen Sie auf der Karte **[!UICONTROL Subdomains &amp; Zertifikate]** zuerst die gewünschte Instanz und danach **[!UICONTROL Zertifikat verwalten]** aus.
* ![](assets/renewal1.png)
* Wählen Sie **[!UICONTROL Installieren eines SSL-Zertifikats]** und dann **[!UICONTROL Weiter]** aus, um den Assistenten zu starten, der Sie durch den Zertifikatinstallationsprozess führt.
* ![](assets/install1.png)
* Wählen Sie die .zip-Datei aus, die das zu installierende Zertifikat enthält, und wählen Sie danach **[!UICONTROL Senden]** aus.
* ![](assets/install2.png)
* [!NOTE]
* Das Zertifikat wird in allen in der CSR enthaltenen Domains/Subdomains installiert. Zusätzliche Domains/Subdomains, die im Zertifikat vorhanden sind, werden nicht berücksichtigt.
* Nach der Installation des SSL-Zertifikats werden das Ablaufdatum und das Statussymbol des Zertifikats entsprechend aktualisiert.
* **Verwandte Themen:**
   * [Hinzufügen von SSL-Zertifikaten (Tutorial-Video)[#$tu67]
   * 
   * 

To install the certificate, follow these steps:

1. In the **[!UICONTROL Subdomains &amp; Certificates]** card, select the desired instance, then click the **[!UICONTROL Manage Certificate]** button.

   ![](assets/renewal1.png)

1. Click **[!UICONTROL Install SSL Certificate]**, then **[!UICONTROL Next]** to launch the wizard that will guide you through the certificate installation process.

   ![](assets/install1.png)

1. Select the .zip file that contains the certificate to install, then click **[!UICONTROL Submit]**.

   ![](assets/install2.png)

>[!NOTE]
>
>The certificate will get installed on all domains/subdomains included in the CSR. Any additional domain/subdomain present in the certificate will not be taken into account.

Once the SSL certificate is installed, the certificate&#39;s expiration date and status icon are updated accordingly.

**Related topics:**

* [Adding SSL certificates (tutorial video)-ERR:REF-NOT-FOUND-
* [Subdomains branding](../../subdomains-certificates/using/subdomains-branding.md)
* [Monitoring your subdomains](../../subdomains-certificates/using/monitoring-subdomains.md)