---
title: Verlängern des SSL-Zertifikats einer Subdomain
description: Erfahren Sie, wie Sie die Zertifikate Ihrer Subdomains verlängern.
translation-type: tm+mt
source-git-commit: 50d29d25891adc866d624888ca72e16e529ae7bf

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

   >[!NOTE]
   >
   >Wenn der CSR nicht gespeichert/heruntergeladen wird, geht er verloren und Sie müssen ihn erneut generieren.

## Kaufen eines Zertifikats mit der CSR {#purchasing-certificate}

Nachdem Sie eine Certificate Signing Request (CSR) über das Control Panel generiert haben, können Sie bei einer von Ihrer Organisation genehmigten Zertifizierungsstelle ein SSL-Zertifikat kaufen.

## Installieren des SSL-Zertifikats {#installing-ssl-certificate}

Nachdem Sie ein SSL-Zertifikat erworben haben, können Sie es auf Ihrer Instanz installieren. Bevor Sie fortfahren, stellen Sie sicher, dass Sie die folgenden Voraussetzungen kennen:

* Die Zertifikatsignaturanforderung (Certificate Signing Request, CSR) muss über die Systemsteuerung generiert worden sein. Andernfalls können Sie das Zertifikat nicht über die Systemsteuerung installieren.
* Die Zertifikatssignaturanforderung (CSR) sollte mit der Subdomäne übereinstimmen, die an Adobe delegiert wurde. Es kann beispielsweise nicht mehr Subdomänen enthalten, als die delegierte Domäne.
* Das Zertifikat sollte ein aktuelles Datum haben. Es ist nicht möglich, Zertifikate mit Terminen in der Zukunft zu installieren, und sollte nicht abgelaufen sein (d.h. gültige Start- und Enddaten).
* Das Zertifikat sollte von einer vertrauenswürdigen Zertifizierungsstelle (CA) wie Comodo, DigiCert, GoDaddy usw. ausgestellt werden.
* Die Größe des Zertifikats sollte 2048 Bit und der Algorithmus RSA sein.
* Das Zertifikat sollte im Format X.509 PEM vorliegen.
* SAN-Zertifikate werden unterstützt.
* Wildcard-Zertifikate werden nicht unterstützt.
* Die ZIP-Datei oder das Zertifikat sollte nicht kennwortgeschützt sein.
* Die ZIP-Datei sollte nur Folgendes in vorzugsweise einzelnen Dateien enthalten:
   * Endentitätszertifikat.
   * Zwischenzeitliche Zertifikatskette (in der richtigen Reihenfolge angeordnet).
   * Stammzertifikat (optional).

Gehen Sie wie folgt vor, um das Zertifikat zu installieren:

1. Wählen Sie auf der Karte **[!UICONTROL Subdomains &amp; Zertifikate]**zuerst die gewünschte Instanz und danach**[!UICONTROL  Zertifikat verwalten]** aus.

   ![](assets/renewal1.png)

1. Wählen Sie **[!UICONTROL Installieren eines SSL-Zertifikats]**und dann**[!UICONTROL  Weiter]** aus, um den Assistenten zu starten, der Sie durch den Zertifikatinstallationsprozess führt.

   ![](assets/install1.png)

1. Wählen Sie die .zip-Datei aus, die das zu installierende Zertifikat enthält, und wählen Sie danach **[!UICONTROL Senden]**aus.

   ![](assets/install2.png)

Nach der Installation des SSL-Zertifikats werden das Ablaufdatum und das Statussymbol des Zertifikats entsprechend aktualisiert.
