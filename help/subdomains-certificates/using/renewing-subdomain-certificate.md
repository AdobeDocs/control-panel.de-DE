---
title: Verlängern des SSL-Zertifikats einer Subdomain
description: Erfahren Sie, wie Sie die Zertifikate Ihrer Subdomains verlängern.
translation-type: tm+mt
source-git-commit: 17f51b60310b4fbc89e2106eb4ee9251fd525a59
workflow-type: tm+mt
source-wordcount: '867'
ht-degree: 94%

---


# Verlängern des SSL-Zertifikats einer Subdomain {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="Hinzufügen eines SSL-Zertifikats"
>abstract="Um ein SSL-Zertifikat hinzuzufügen, müssen Sie eine CSR generieren, das SSL-Zertifikat für Ihre Subdomains erwerben und das Zertifikat-Bundle installieren."
>additional-url="https://docs.adobe.com/content/help/de-DE/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr" text="Generieren einer Certificate Signing Request (CSR)"
>additional-url="https://docs.adobe.com/content/help/de-DE/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#installing-ssl-certificate" text="Installieren eines SSL-Zertifikats"

>[!IMPORTANT]
>
>Die Subdomänenkonfiguration über die Systemsteuerung ist in der Beta-Version verfügbar und unterliegt häufigen Aktualisierungen und Änderungen ohne Vorankündigung.

## Über die Zertifikatsverlängerung {#about-certificate-renewal-process}

Der Verlängerungsprozess eines SSL-Zertifikats besteht aus drei Schritten:

1. **Generieren der Certificate Signing Request (CSR)** Die Adobe-Kundenunterstützung generiert eine CSR für Sie. Sie müssen einige Informationen angeben, die für die Generierung der CSR erforderlich sind (z. B. Gebrauchsname, Organisationsname und Adresse).
1. **Kauf des SSL-Zertifikats**
Sobald die CSR generiert wurde, können Sie sie herunterladen und zum Kauf des SSL-Zertifikats bei der von Ihrem Unternehmen genehmigten Zertifizierungsstelle verwenden.
1. **Installation des SSL-Zertifikats**
Nachdem Sie das SSL-Zertifikat erworben haben, können Sie es in der gewünschten Subdomain installieren.

## Generieren einer Certificate Signing Request (CSR) {#generating-csr}

>[!CONTEXTUALHELP]
>id="cp_generate_csr"
>title="Erstellen einer CSR"
>abstract="Vor dem Kauf eines Zertifikats muss eine Certificate Signing Request für die Instanz und die Subdomains generiert werden, die Sie schützen möchten."

>[!CONTEXTUALHELP]
>id="cp_select_subdomains"
>title="Auswählen der Subdomains für Ihre CSR"
>abstract="Sie können auswählen, ob Sie alle oder nur bestimmte Subdomains in Ihre Certificate Signing Request aufnehmen möchten. Nur ausgewählte Subdomains werden über das erworbene SSL-Zertifikat zertifiziert."
>additional-url="https://docs.adobe.com/content/help/de-DE/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr" text="Generieren einer Certificate Signing Request (CSR)"
>additional-url="https://docs.adobe.com/content/help/de-DE/control-panel/using/subdomains-and-certificates/subdomains-branding.html" text="Über Subdomain-Branding"

Gehen Sie wie folgt vor, um eine Certificate Signing Request (CSR) zu erstellen:

1. Wählen Sie zuerst auf der Karte **[!UICONTROL Subdomains &amp; Zertifikate]** die gewünschte Instanz und danach **[!UICONTROL Zertifikat verwalten]** aus.

   ![](assets/renewal1.png)

1. Wählen Sie **[!UICONTROL 1 - Erstellen einer CSR]** und dann **[!UICONTROL Weiter]** aus, um den Assistenten zu starten, der Sie durch den CSR-Generierungsprozess führt.

   ![](assets/renewal2.png)

1. Daraufhin wird ein Formular mit allen Details angezeigt, die zum Generieren Ihrer CSR erforderlich sind.

   Vergewissern Sie sich, dass Sie die angeforderten Informationen vollständig und korrekt ausgefüllt haben. Anderenfalls kann das Zertifikat möglicherweise nicht verlängert werden. (Wenden Sie sich bei Bedarf an Ihr internes Team bzw. Ihr Sicherheits- oder IT-Team.) Wählen Sie dann **[!UICONTROL Weiter]** aus.

   * **[!UICONTROL Organisation]**: Offizieller Name der Organisation.
   * **[!UICONTROL Organisationseinheit]**: Die mit der Subdomain verknüpfte Einheit (Beispiel: Marketing, IT).
   * **[!UICONTROL Instanz]** (vorbelegt): URL der Campaign-Instanz, die mit der Subdomain verknüpft ist.

   ![](assets/renewal3.png)

1. Wählen Sie zuerst die Subdomains aus, die in die CSR einbezogen werden sollen, und danach **[!UICONTROL OK]**.

   ![](assets/renewal4.png)

1. Die ausgewählten Subdomains werden in der Liste angezeigt. Wählen Sie für jede davon die einzubeziehenden Subdomains und dann **[!UICONTROL Weiter]** aus.

   ![](assets/renewal5.png)

1. In einer Zusammenfassung werden alle Subdomains angezeigt, die in die CSR einbezogen werden sollen. Bestätigen Sie Ihre Anfrage durch die Auswahl von **[!UICONTROL Senden]**.

   ![](assets/renewal6.png)

1. Die .csr-Datei wird entsprechend Ihrer Auswahl automatisch generiert und heruntergeladen. Mit dieser Datei können Sie nun das SSL-Zertifikat bei der von Ihrem Unternehmen genehmigten Zertifizierungsstelle erwerben.

   >[!NOTE]
   >
   >Wenn die CSR nicht gespeichert/heruntergeladen wird, geht sie verloren und Sie müssen sie erneut generieren.

## Kaufen eines Zertifikats mit der CSR {#purchasing-certificate}

Nachdem Sie eine Certificate Signing Request (CSR) über das Control Panel generiert haben, können Sie bei einer von Ihrer Organisation genehmigten Zertifizierungsstelle ein SSL-Zertifikat kaufen.

## Installieren des SSL-Zertifikats {#installing-ssl-certificate}

>[!CONTEXTUALHELP]
>id="cp_install_ssl_certificate"
>title="Installieren eines SSL-Zertifikats"
>abstract="Installieren Sie das SSL-Zertifikat, das Sie bei der von Ihrem Unternehmen zugelassenen Zertifizierungsstelle erworben haben."
>additional-url="https://docs.adobe.com/content/help/de-DE/control-panel/using/subdomains-and-certificates/subdomains-branding.html" text="Über Subdomain-Branding"

Sobald Sie ein SSL-Zertifikat gekauft haben, können Sie es auf Ihrer Instanz installieren. Bevor Sie fortfahren, achten Sie auf folgende Voraussetzungen:

* Die Certificate Signing Request (CSR) muss über das Control Panel generiert worden sein. Andernfalls können Sie das Zertifikat nicht über das Control Panel installieren.
* Die Zertifikatssignaturanforderung (CSR) sollte mit der Subdomäne übereinstimmen, die für die Verwendung mit Adobe konfiguriert wurde. Es kann beispielsweise nicht mehr Subdomänen enthalten, als die konfigurierte.
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

1. Wählen Sie zuerst auf der Karte **[!UICONTROL Subdomains &amp; Zertifikate]** die gewünschte Instanz und danach **[!UICONTROL Zertifikat verwalten]** aus.

   ![](assets/renewal1.png)

1. Wählen Sie **[!UICONTROL 3 - Zertifikat-Bundle installieren]** und dann **[!UICONTROL Weiter]** aus, um den Assistenten zu starten, der Sie durch den Zertifikatinstallationsprozess führt.

   ![](assets/install1.png)

1. Wählen Sie die .zip-Datei aus, die das zu installierende Zertifikat enthält, und wählen Sie danach **[!UICONTROL Senden]** aus.

   ![](assets/install2.png)

>[!NOTE]
>
>Das Zertifikat wird in allen in der CSR enthaltenen Domains/Subdomains installiert. Zusätzliche Domains/Subdomains, die im Zertifikat vorhanden sind, werden nicht berücksichtigt.

Nach der Installation des SSL-Zertifikats werden das Ablaufdatum und das Statussymbol des Zertifikats entsprechend aktualisiert.

**Verwandte Themen:**

* [Hinzufügen von SSL-Zertifikaten (Tutorial-Video)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [Subdomain-Branding](../../subdomains-certificates/using/subdomains-branding.md)
* [Überwachen von Subdomains](../../subdomains-certificates/using/monitoring-subdomains.md)