---
product: campaign
solution: Campaign
title: Hinzufügen von DMARC-Datensätzen
description: Erfahren Sie, wie Sie einen DMARC-Datensatz für eine Subdomain hinzufügen.
feature: Control Panel
role: Architect
level: Experienced
exl-id: 2ca66983-5beb-495a-9639-a31905500cff
source-git-commit: 64ea5e26786eea107983ee5025025c81334b0a91
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Hinzufügen von DMARC-Datensätzen {#dmarc}

## Über DMARC-Einträge {#about}

Domain based Message Authentication, Reporting and Conformance (DMARC) ist ein E-Mail-Authentifizierungsprotokollstandard, der Unternehmen dabei unterstützt, ihre E-Mail-Domains vor Phishing- und Spoofing-Angriffen zu schützen. Sie können damit festlegen, wie ein Postfachanbieter E-Mails verarbeiten soll, die bei SPF- und DKIM-Prüfungen fehlschlagen. So können Sie die Domäne des Absenders authentifizieren und eine unbefugte Nutzung der Domain zu bösartigen Zwecken verhindern.

Detaillierte Informationen zur DMARC-Implementierung finden Sie unter [Best Practices für die Adobe-Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html)

## Einschränkungen und Voraussetzungen {#limitations}

* SPF- und DKIM-Datensätze sind Voraussetzungen für die Erstellung eines DMARC-Datensatzes.
* DMARC-Einträge können nur für Subdomains hinzugefügt werden, die eine vollständige Subdomain-Zuweisung verwenden. [Weitere Informationen zu den Konfigurationsmethoden von Subdomains](subdomains-branding.md#subdomain-delegation-methods)

## Hinzufügen eines DMARC-Datensatzes für eine Subdomain {#add}

Gehen Sie wie folgt vor, um einen DMARC-Datensatz für eine Subdomain hinzuzufügen:

1. Klicken Sie in der Liste der Subdomains auf die Suchschaltfläche neben der gewünschten Subdomain und wählen Sie **[!UICONTROL Details der Subdomain]**.

1. Klicken Sie auf **[!UICONTROL TXT-Eintrag hinzufügen]** und wählen Sie **[!UICONTROL DMARC]** aus dem **[!UICONTROL Record Type]** Dropdown-Liste.

   ![](assets/dmarc-add.png)

1. Wählen Sie die **[!UICONTROL Richtlinientyp]** dass der Empfängerserver folgen sollte, wenn eine Ihrer E-Mails fehlschlägt. Verfügbare Richtlinientypen sind:

   * **[!UICONTROL Keine]**,
   * **[!UICONTROL Quarantäne]** (Platzierung von Spam-Ordnern),
   * **[!UICONTROL Ablehnen]** (E-Mail blockieren).

   Als Best Practice wird empfohlen, die DMARC-Implementierung langsam einzuführen, indem Sie Ihre DMARC-Richtlinie von p=none auf p=quarantine eskalieren und p=reject, sobald DMARC die potenziellen Auswirkungen von DMARC erkennt.

   * **Schritt 1:** Analysieren Sie das Feedback, das Sie erhalten und verwenden (p=none), das den Empfänger anweist, keine Aktionen für Nachrichten durchzuführen, die die Authentifizierung nicht befolgen, aber trotzdem E-Mail-Berichte an den Absender senden. Überprüfen und beheben Sie außerdem Probleme mit SPF/DKIM, wenn die Authentifizierung für legitime Nachrichten fehlschlägt.

   * **Schritt 2:** Bestimmen Sie, ob SPF und DKIM abgestimmt sind und übergeben Sie die Authentifizierung für alle legitimen E-Mails und verschieben Sie dann die Richtlinie auf (p=quarantine), wodurch der E-Mail-Empfangs-Server angewiesen wird, E-Mails unter Quarantäne zu stellen, die die Authentifizierung fehlschlagen (im Allgemeinen bedeutet dies, dass diese Nachrichten im Spam-Ordner abgelegt werden). Wenn die Richtlinie auf Quarantäne gesetzt ist, wird empfohlen, mit einem kleinen Prozentsatz Ihrer E-Mails zu beginnen.

   * **Schritt 3:** Richtlinie anpassen auf (p=reject). HINWEIS: Verwenden Sie diese Richtlinie mit Vorsicht und legen Sie fest, ob sie für Ihre Organisation geeignet ist. Die p=-Zurückweisungsrichtlinie weist den Empfänger an, jede E-Mail für die Domain, bei der die Authentifizierung fehlschlägt, vollständig zu verweigern (Bounce). Wenn diese Richtlinie aktiviert ist, haben nur E-Mails, die zu 100 % von Ihrer Domäne authentifiziert wurden, sogar die Möglichkeit, die Posteingangsplatzierung durchzuführen.

   >[!NOTE]
   >
   > Die Erstellung von BIMI-Datensätzen ist nicht verfügbar, wenn der DMARC-Datensatzrichtlinientyp auf &quot;Keine&quot;festgelegt ist.

1. Füllen Sie die E-Mail-Adressen aus, an die die DMARC-Berichte gesendet werden sollen. Wenn eine Ihrer E-Mails fehlschlägt, werden DMARC-Berichte automatisch an die E-Mail-Adresse Ihrer Wahl gesendet:

   * Aggregate-DMARC-Berichte enthalten allgemeine Informationen wie z. B. die Anzahl der E-Mails, die in einem bestimmten Zeitraum fehlgeschlagen sind.
   * Berichte zu forensischen DMARC-Fehlern enthalten detaillierte Informationen, z. B. von welcher IP-Adresse die fehlgeschlagene E-Mail stammt.

1. Wenn die DMARC-Richtlinie auf &quot;Keine&quot;gesetzt ist, geben Sie einen Prozentsatz ein, der für 100 % der E-Mails gilt.

   Wenn die Richtlinie auf &quot;Ablehnen&quot;oder &quot;Quarantäne&quot;gesetzt ist, wird empfohlen, mit einem kleinen Prozentsatz Ihrer E-Mails zu beginnen. Wenn mehr E-Mails aus Ihrer Domain die Authentifizierung mit Empfangs-Servern bestehen, aktualisieren Sie Ihren Datensatz langsam mit einem höheren Prozentsatz.

   >[!NOTE]
   >
   >Wenn Ihre Domäne BIMI verwendet, muss Ihre DMARC-Richtlinie einen Prozentwert von 100 % haben. BIMI unterstützt keine DMARC-Richtlinien, deren Wert auf unter 100 % festgelegt ist.

   ![](assets/dmarc-add2.png)

1. DMARC-Berichte werden alle 24 Stunden gesendet. Sie können die Versandfrequenz der Berichte im **[!UICONTROL Berichtsintervall]** -Feld. Das zulässige Mindestintervall beträgt 1 Stunde, der maximal zulässige Wert 2190 Stunden (d. h. 3 Monate).

1. Im **SPF** und **[!UICONTROL DKIM-Identifikationsausrichtung]** Geben Sie an, wie streng die Empfängerserver sein sollten, während Sie die SPF- und DKIM-Authentifizierung für eine E-Mail überprüfen.

   * **[!UICONTROL Relaxed]** mode: der Server akzeptiert die Authentifizierung, selbst wenn die E-Mail von einer Subdomain gesendet wird,
   * **[!UICONTROL Streng]** Der -Modus akzeptiert nur dann die Authentifizierung, wenn die Absenderdomäne genau mit einer SPF- und DKIM-Domäne übereinstimmt.

   Angenommen, wir arbeiten mit der `http://www.luma.com` Domäne. Im Modus &quot;Entspannt&quot; werden E-Mails von der `marketing.luma.com` Die Subdomain wird vom Server autorisiert, während sie im Modus &quot;Streng&quot; zurückgewiesen wird.

1. Klicks **[!UICONTROL Hinzufügen]** , um die Erstellung des DMARC-Datensatzes zu bestätigen.

Sobald die Erstellung des DMARC-Datensatzes verarbeitet wurde (etwa 5 Minuten), wird er im Detailbildschirm der Subdomains angezeigt. [Erfahren Sie, wie Sie TXT-Einträge für Ihre Subdomains überwachen.](gs-txt-records.md#monitor)
