---
product: campaign
solution: Campaign
title: Verlängern des SSL-Zertifikats einer Subdomain
description: Erfahren Sie, wie Sie die Zertifikate Ihrer Subdomains verlängern.
feature: Control Panel
role: Architect
level: Experienced
exl-id: e9b7c67d-6afa-44f9-b19d-39c0ec9a7edd
source-git-commit: 5a5ac1a604fe5bdce07479ff84184abdb2e0ddba
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 62%

---

# Verlängern eines SSL-Zertifikats {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="Verlängerung von SSL-Zertifikaten"
>abstract="Um ein SSL-Zertifikat hinzuzufügen, müssen Sie eine CSR generieren, das SSL-Zertifikat für Ihre Subdomain erwerben und das Zertifikat-Bundle installieren."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html?lang=de#generating-csr" text="Generieren einer Certificate Signing Request (CSR)"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html?lang=de#installing-ssl-certificate" text="Installieren eines SSL-Zertifikats"

>[!IMPORTANT]
>
>Die Verlängerung von SSL-Zertifikaten über das Control Panel befindet sich in der Beta-Version und unterliegt häufigen Aktualisierungen und Änderungen ohne Vorankündigung.
>
>Wenn Sie eine Instanz mit einem Hybrid-Hosting-Modell verwenden, können Sie nur Zertifikate anzeigen, die mit den zugewiesenen Subdomains verknüpft sind, und diese nicht verlängern.

Der Verlängerungsprozess eines SSL-Zertifikats besteht aus drei Schritten:

1. **Erstellung der Certificate Signing Request (CSR)**

   Vor dem Kauf eines Zertifikats muss eine Certificate Signing Request für die Instanz und die Subdomains generiert werden, die Sie schützen möchten.  Darauf müssen Sie alle für die Erstellung einer CSR erforderlichen Informationen bereitstellen (z. B. Gebrauchsname, Organisationsname und Adresse). [Weitere Informationen](generate-csr.md)

1. **Erwerb des SSL-Zertifikats**

   Sobald die CSR generiert wurde, können Sie damit das SSL-Zertifikat bei der von Ihrem Unternehmen genehmigten Zertifizierungsstelle erwerben.

1. **Installation des SSL-Zertifikats**

   Installieren Sie das erworbene SSL-Zertifikat auf der gewünschten Subdomain, um sie zu schützen. [Weitere Informationen](install-ssl-certificate.md)

![](assets/do-not-localize/how-to-video.png) Entdecken Sie diese Funktion bei der Verwendung von [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=de#subdomains-and-certificates) oder [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=de#adding-ssl-certificates) im Video.

**Verwandte Themen:**

* [Best Practice-Handbuch für die Zustellbarkeit - SSL-Zertifikatanforderungsprozess für Adobe Campaign](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/campaign/ac-ssl-certificate-request.html)
* [Subdomain-Branding](../../subdomains-certificates/using/subdomains-branding.md)
* [Überwachen von Subdomains](../../subdomains-certificates/using/monitoring-subdomains.md)
