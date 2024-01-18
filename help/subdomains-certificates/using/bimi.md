---
product: campaign
solution: Campaign
title: Hinzufügen von BIMI-Einträgen
description: Erfahren Sie, wie Sie einen BIMI-Eintrag für eine Subdomain hinzufügen.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: eb7863fb-6e6d-4821-a156-03fee03cdd0e
source-git-commit: e601f74ae9e53d3a008c55e1fd568013ca0196f8
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 86%

---

# Hinzufügen von BIMI-Einträgen {#dmarc}

## Über BIMI-Einträge {#about}

Brand Indicators for Message Identification (BIMI) ist ein Branchenstandard, der es ermöglicht, ein genehmigtes Logo neben der Absender-E-Mail in den Postfächern von E-Mail-Anbietern anzuzeigen, um die Markenerkennung und das Vertrauen zu fördern. Dies hilft, das Spoofing und Phishing von E-Mails zu verhindern, indem die Identität der Absenderin bzw. des Absenders durch DMARC-Authentifizierung überprüft wird. Dadurch wird es für böswillig Agierende schwieriger, sich in E-Mails als legitime Marken auszugeben.

Sie können mehrere Logos für eine bestimmte Subdomain haben. Dazu müssen Sie für jedes Logo einen BIMI-Datensatz einrichten und jedem Datensatz einen BIMI-Selektor zuweisen. [Erfahren Sie, wie Sie einen BIMI-Datensatz hinzufügen](#add)

Detaillierte Informationen zur BIMI-Implementierung finden Sie im [Adobe-Handbuch für Best Practices zur Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-bimi.html?lang=de)

![](assets/bimi-example.png){width="70%" align="center"}

## Einschränkungen und Voraussetzungen {#limitations}

* SPF-, DKIM- und DMARC-Einträge sind Voraussetzung für das Erstellen eines BIMI-Eintrags.
* BIMI-Einträge können nur für Subdomains hinzugefügt werden, die eine vollständige Subdomain-Delegierung verwenden. [Hier finden Sie weitere Informationen zu den Konfigurationsmethoden von Subdomains](subdomains-branding.md#subdomain-delegation-methods)
* Voraussetzungen für DMARC-Einträge:

   * Der Richtlinientyp für die Einträge der Subdomain muss auf „Quarantäne“ oder „Ablehnen“ eingestellt sein. Die Erstellung von BIMI-Einträgen ist nicht verfügbar, wenn der DMARC-Richtlinientyp auf „Keine“ festgelegt ist.
   * Der Prozentsatz der E-Mails, auf die die DMARC-Richtlinie angewendet wird, muss 100 % betragen. BIMI unterstützt keine DMARC-Richtlinien, deren Prozentsatz auf weniger als 100 % festgelegt ist.

[Erfahren Sie, wie Sie DMARC-Einträge konfigurieren](dmarc.md)

## Hinzufügen eines BIMI-Eintrags für eine Subdomain {#add}

Gehen Sie wie folgt vor, um einen BIMI-Eintrag für eine Subdomain hinzuzufügen:

1. Klicken Sie in der Liste der Subdomains auf die Schaltfläche mit den Auslassungspunkten neben der gewünschten Subdomain und wählen Sie **[!UICONTROL Details der Subdomain]**.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL TXT-Eintrag hinzufügen]** und wählen Sie **[!UICONTROL BIMI]** aus der Dropdown-Liste **[!UICONTROL Typ des Eintrages]**.

   ![](assets/bimi-add.png)

1. Die **[!UICONTROL Selektor]** -Feld können Sie einen BIMI-Selektor für den Datensatz angeben. Ein BIMI-Selektor ist eine eindeutige Kennung, die Sie einem BIMI-Datensatz zuweisen können. Auf diese Weise können Sie mehrere Logos für eine bestimmte Subdomain definieren.

1. Geben Sie in der **[!UICONTROL Firmen-Logo-URL]** die URL der SVG-Datei an, die Ihr Logo enthält.

1. Obwohl die **[!UICONTROL Zertifikats-URL]** optional ist, ist sie bei einigen E-Mail-Anbietern wie Gmail und Apple erforderlich, die 80 % des E-Mail-Markts abdecken. Daher empfehlen wir, ein Verified Mark Certificate (VMC) zu erhalten, um BIMI wirklich auszunutzen.

   +++Wie erhalte ich ein VMC?

   Die wichtigsten Schritte zum Erhalten eines VMC sind:

   1. Registrieren Sie Ihr Markenlogo als Marke bei einem Büro für geistiges Eigentum, das von VMC-Emittierenden anerkannt wird. Wenn Sie über eine Rechtsabteilung verfügen, empfehlen wir Ihnen, mit ihr zusammenzuarbeiten, um Ihr Logo zu schützen oder zu überprüfen, ob es bereits geschützt ist.

   1. Nachdem Sie sich vergewissert haben, dass Ihr Logo geschützt ist, wenden Sie sich an die Zertifizierungsstelle (certificate authority, CA) DigiCert oder Entrust, um ein VMC anzufordern.

   1. Wenn Ihr VMC genehmigt ist, erhalten Sie eine Privacy Enhanced Mail(PEM)-Datei mit einem Entitätszertifikat. Hängen Sie alle anderen Zwischenzertifikate, die Sie von der CA erhalten, an diese PEM-Datei an. Laden Sie die PEM-Datei (zusammen mit angehängten Dateien) auf Ihren öffentlichen Webserver hoch und notieren Sie sich die URL der PEM-Datei. Sie werden diese URL in Ihrem BIMI-TXT-Eintrag verwenden.

   1. Sobald der BIMI-Eintrag auf der Detailseite einer bestimmten Subdomain sichtbar ist, können Sie den [hier](https://bimigroup.org/bimi-generator/) verfügbaren BIMI-Inspektor verwenden, um zu überprüfen, ob der BIMI-Eintrag ordnungsgemäß funktioniert.

   Detaillierte Informationen zur BIMI-Implementierung finden Sie in der [Dokumentation zu den BIMI-Standards](https://bimigroup.org/implementation-guide/)
+++

1. Klicken Sie auf **[!UICONTROL Hinzufügen]**, um die Erstellung des BIMI-Eintrags zu bestätigen.

Sobald die Erstellung des BIMI-Eintrags verarbeitet wurde (etwa 5 Minuten), wird er im Detailbildschirm der Subdomains angezeigt. [Erfahren Sie, wie Sie TXT-Einträge für Ihre Subdomains überwachen.](gs-txt-records.md#monitor)
