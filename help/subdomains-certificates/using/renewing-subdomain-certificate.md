---
title: Verlängerung des SSL-Zertifikats einer Subdomäne
description: Erfahren Sie, wie Sie die SSL-Zertifikate Ihrer Subdomänen erneuern.
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Verlängerung des SSL-Zertifikats einer Subdomäne {#renewing-subdomains-ssl-certificates}

## Grundlagen zur Zertifikatverlängerung {#about-certificate-renewal-process}

Der SSL-Zertifikatverlängerungsprozess umfasst drei Schritte, die alle direkt über die Systemsteuerung ausgeführt werden:

1. **Generierung der Zertifikatsignaturanforderung (CSR)** Der Adobe-Kundendienst generiert eine CSR für Sie. Darauf müssen Sie alle für die Erstellung einer CSR erforderlichen Informationen bereitstellen (z. B. Gebrauchsname, Organisationsname und Adresse). 
1. **Erwerb des SSL-Zertifikats** Sobald das CSR generiert wurde, können Sie es herunterladen und zum Kauf des SSL-Zertifikats bei der Zertifizierungsstelle verwenden, die Ihr Unternehmen genehmigt.
1. **Installation des SSL-Zertifikats** Nachdem Sie das SSL-Zertifikat erworben haben, können Sie es in der gewünschten Subdomäne installieren.

## Erstellen einer Zertifikatsignaturanforderung (CSR) {#generating-csr}

Gehen Sie wie folgt vor, um eine CSR-Anforderung (Certificate Signing Request) zu erstellen:

1. Wählen Sie auf der Karte &quot; **[!UICONTROL Subdomänen und Zertifikate]**&quot;die gewünschte Instanz aus und klicken Sie dann auf die Schaltfläche &quot;Zertifikat**[!UICONTROL  verwalten&quot;]** .

   ![](assets/renewal1.png)

1. Wählen Sie &quot;CSR **[!UICONTROL generieren&quot;]**und klicken Sie dann auf &quot;**[!UICONTROL  Weiter]** &quot;, um den Assistenten zu starten, der Sie durch den CSR-Generierungsprozess führt.

   ![](assets/renewal2.png)

1. Es wird ein Formular mit allen zum Generieren der CSR erforderlichen Details angezeigt.

   Make sure you fill in the requested information fully and accurately (contact your internal team, Security and IT teams if necessary), then click **[!UICONTROL Next]**.

   * **[!UICONTROL Organisation]**:
   * **[!UICONTROL Organisationseinheit]**:
   * **[!UICONTROL Instanz]**: URL der der Subdomäne zugeordneten Kampagneninstanz.
   ![](assets/renewal3.png)

1. Wählen Sie die Subdomänen aus, die in die CSR einbezogen werden sollen, und klicken Sie dann auf **[!UICONTROL OK]**.

   ![](assets/renewal4.png)

1. Die ausgewählten Subdomänen werden in der Liste angezeigt. Wählen Sie für jede dieser Domänen die einzuschließenden Subdomänen aus und klicken Sie dann auf **[!UICONTROL Weiter]**.

   ![](assets/renewal5.png)

1. Es wird eine Zusammenfassung der Subdomänen angezeigt, die in das CSR einbezogen werden sollen. Klicken Sie auf **[!UICONTROL Senden]**, um Ihre Anforderung zu bestätigen.

   ![](assets/renewal6.png)

1. Die CSR-Datei, die Ihrer Auswahl entspricht, wird automatisch generiert und heruntergeladen. Sie können es jetzt verwenden, um das SSL-Zertifikat von der Zertifizierungsstelle zu erwerben, die Ihr Unternehmen genehmigt.

## Erwerb eines Zertifikats mit dem CSR {#purchasing-certificate}

Nachdem Sie eine CSR-Anforderung für Zertifikatsignierung von der Systemsteuerung erhalten haben, erwerben Sie ein SSL-Zertifikat von einer Zertifizierungsstelle, die von Ihrem Unternehmen genehmigt wurde.

## SSL-Zertifikat installieren {#installing-ssl-certificate}

Nachdem Sie ein SSL-Zertifikat erworben haben, führen Sie die folgenden Schritte aus, um es auf Ihrer Instanz zu installieren.

1. Wählen Sie auf der Karte &quot; **[!UICONTROL Subdomänen und Zertifikate]**&quot;die gewünschte Instanz aus und klicken Sie dann auf die Schaltfläche &quot;Zertifikat**[!UICONTROL  verwalten&quot;]** .

   ![](assets/renewal1.png)

1. Klicken Sie auf SSL-Zertifikat ****installieren und dann auf**[!UICONTROL  Weiter]** , um den Assistenten zu starten, der Sie durch den Zertifikatinstallationsprozess führt.

   ![](assets/install1.png)

1. Wählen Sie die ZIP-Datei aus, die das zu installierende Zertifikat enthält, und klicken Sie dann auf **[!UICONTROL Senden]**.

   ![](assets/install2.png)