---
product: campaign
solution: Campaign
title: Hinzufügen von BIMI-Datensätzen
description: Erfahren Sie, wie Sie einen BIMI-Datensatz für eine Subdomain hinzufügen.
feature: Control Panel
role: Architect
level: Experienced
exl-id: eb7863fb-6e6d-4821-a156-03fee03cdd0e
source-git-commit: 64ea5e26786eea107983ee5025025c81334b0a91
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# Hinzufügen von BIMI-Datensätzen {#dmarc}

## Über BIMI-Datensätze {#about}

Brand Indicators for Message Identification (BIMI) ist ein Branchenstandard, der es ermöglicht, ein genehmigtes Logo neben der E-Mail eines Absenders in den Postfächern von Postfachanbietern anzuzeigen, um die Markenerkennung und das Vertrauen zu verbessern. Dies hilft, das Spoofing und Phishing von E-Mails zu verhindern, indem die Identität des Absenders durch DMARC-Authentifizierung überprüft wird. Dadurch wird es für böswillige Akteure schwieriger, sich in E-Mails als legitime Marken auszugeben.

Detaillierte Informationen zur BIMI-Implementierung finden Sie unter [Best Practices für die Adobe-Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-bimi.html)

![](assets/bimi-example.png){width="70%" align="center"}

## Einschränkungen und Voraussetzungen {#limitations}

* SPF-, DKIM- und DMARC-Datensätze sind Voraussetzungen für die Erstellung eines BIMI-Datensatzes.
* BIMI-Datensätze können nur für Subdomains hinzugefügt werden, die eine vollständige Subdomain-Zuweisung verwenden. [Weitere Informationen zu den Konfigurationsmethoden von Subdomains](subdomains-branding.md#subdomain-delegation-methods)
* Voraussetzungen für DMARC-Datensätze:

   * Der Richtlinientyp für die Aufzeichnung der Subdomain muss auf &quot;Quarantäne&quot;oder &quot;Ablehnen&quot;eingestellt sein. Die Erstellung von BIMI-Datensätzen ist nicht verfügbar, wenn der DMARC-Richtlinientyp auf &quot;Keine&quot;festgelegt ist.
   * Der Prozentsatz der E-Mails, auf die die DMARC-Richtlinie angewendet wird, muss 100 % betragen. BIMI unterstützt keine DMARC-Richtlinien, deren Prozentsatz auf weniger als 100 % festgelegt ist.

[Erfahren Sie, wie Sie DMARC-Datensätze konfigurieren](dmarc.md)

## Hinzufügen eines BIMI-Datensatzes für eine Subdomain {#add}

Gehen Sie wie folgt vor, um einen BIMI-Datensatz für eine Subdomain hinzuzufügen:

1. Klicken Sie in der Liste der Subdomains auf die Suchschaltfläche neben der gewünschten Subdomain und wählen Sie **[!UICONTROL Details der Subdomain]**.

1. Klicken Sie auf **[!UICONTROL TXT-Eintrag hinzufügen]** und wählen Sie **[!UICONTROL BIMI]** aus dem **[!UICONTROL Record Type]** Dropdown-Liste.

   ![](assets/bimi-add.png)

1. Im **[!UICONTROL Firmen-Logo-URL]**, geben Sie die URL der SVG-Datei an, die Ihr Logo enthält.

1. Husten **[!UICONTROL ZertifikatURL]** optional ist, ist es für einige Postfachanbieter wie Gmail und Apple erforderlich, die 80 % des Postfachmarkts abdecken. Daher empfehlen wir, ein Verified Mark Certificate (VMC) zu erhalten, um BIMI wirklich zu nutzen.

   +++Wie erhalte ich einen VMC?

   Die wichtigsten Schritte zum Abrufen eines VMC sind:

   1. Registrieren Sie Ihr Markenlogo als Marke bei einem Büro für geistiges Eigentum, das von VMC-Emittenten anerkannt wird. Wenn Sie über ein Rechtsteam verfügen, empfehlen wir Ihnen, mit ihnen zusammenzuarbeiten, um Ihr Logo mit einem Markenzeichen zu versehen oder zu überprüfen, ob es bereits mit einer Marke versehen ist.

   1. Nachdem Sie sich vergewissert haben, dass Ihr Logo mit einer Marke versehen ist, wenden Sie sich an DigiCert oder die Zertifizierungsstelle von Entrust (CA), um einen VMC anzufordern.

   1. Wenn Ihr VMC genehmigt ist, erhalten Sie eine PEM-Datei (Privacy Enhanced Mail) mit einem Entitätszertifikat. Hängen Sie alle anderen Zwischenzertifikate, die Sie von der Zertifizierungsstelle erhalten, an diese PEM-Datei an. Laden Sie die PEM-Datei (zusammen mit angehängten Dateien) auf Ihren öffentlichen Webserver hoch und notieren Sie sich die PEM-Datei-URL. Sie verwenden die URL in Ihrem BIMI TXT-Eintrag.

   1. Sobald der BIMI-Datensatz auf der Detailseite der Subdomain für eine bestimmte Subdomain sichtbar ist, können Sie den verfügbaren BIMI-Inspektor verwenden [here](https://bimigroup.org/bimi-generator/) um zu überprüfen, ob der BIMI-Datensatz ordnungsgemäß funktioniert.

   Detaillierte Informationen zur BIMI-Implementierung finden Sie im Abschnitt [BIMI-Standarddokumentation](https://bimigroup.org/implementation-guide/)
+++

1. Klicks **[!UICONTROL Hinzufügen]** , um die Erstellung des BIMI-Datensatzes zu bestätigen.

Sobald die Erstellung des BIMI-Datensatzes verarbeitet wurde (etwa 5 Minuten), wird er im Detailbildschirm der Subdomains angezeigt. [Erfahren Sie, wie Sie TXT-Einträge für Ihre Subdomains überwachen.](gs-txt-records.md#monitor)
