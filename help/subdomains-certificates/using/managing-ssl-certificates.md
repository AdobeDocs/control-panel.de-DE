---
title: SSL-Zertifikate für Subdomänen verwalten
description: Erfahren Sie, wie Sie die SSL-Zertifikate Ihrer Subdomänen überwachen und den Erneuerungsprozess starten können
translation-type: tm+mt
source-git-commit: 6bc165f995d34d21b5bce379db3095317db10906

---


# SSL-Zertifikate für Subdomänen verwalten {#managing-subdomains-ssl-certificates}

Mit der **[!UICONTROL Karte &quot;Subdomänen&quot;und &quot;Zertifikate]**&quot;können Sie sehen, welche Ihrer Subdomänen und zugehörigen Subdomänen Ihre Einstiegsseiten und Ressourcen mit auf ihnen installierten SSL-Zertifikaten hosten. Sie können auch leicht erkennen, welche Subdomänen ablaufende Zertifikate besitzen, damit Sie deren Ablauf vorhersehen können.

Wenn ein Zertifikat demnächst abläuft, können Sie dann eine Kundendienstanfrage mit allen erforderlichen Informationen starten, um das Zertifikat zu verlängern und sicherzustellen, dass Ihre Instanz ordnungsgemäß funktioniert.

>[!NOTE]
>
>Adobe empfiehlt, das SSL-Zertifikat der zugehörigen Subdomänen zu verlängern, **wenn das Ablaufdatum näher rückt**. Die Verlängerung eines Zertifikats kann je nach Unternehmen einige Tage dauern. Wir empfehlen daher, für diesen Vorgang eine entsprechende Dauer einzuplanen.

## SSL-Zertifikate überwachen {#monitoring-ssl-certificates}

Die Liste der Subdomänen für jede Ihrer Instanzen ist beim Auswählen der Karte &quot; **[!UICONTROL Subdomänen und Zertifikate]**&quot;direkt verfügbar.

Subdomänen werden nach dem nächsten Ablaufdatum des SSL-Zertifikats mit visuellen Informationen zum Ablauf in Tagen angeordnet:

* **Grün**: Die Subdomäne hat kein Zertifikat, das innerhalb der nächsten 60 Tage abläuft.
* **Orange**: eine oder mehrere Subdomänen über ein Zertifikat verfügen, das innerhalb der nächsten 60 Tage abläuft.
* **Rot**: eine oder mehrere Subdomänen über ein Zertifikat verfügen, das innerhalb der nächsten 30 Tage abläuft.

![](assets/visual_alert2.png)

Um weitere Details zu den Zertifikaten einer Subdomäne abzurufen, klicken Sie auf die Schaltfläche **[!UICONTROL Zertifikatdetails]**.

![](assets/certificate_details4.png)

Die Liste aller verwandten Subdomänen wird auf ihren Zertifikaten angezeigt. Es umfasst in der Regel Subdomänen von Einstiegsseiten, Ressourcenseiten usw.

![](assets/monitoring_subdomains_details2.png)

Bei Bedarf können Sie in diesem Fenster eine Anforderung zur Erneuerung des Zertifikats starten. Weitere Informationen dazu finden Sie im folgenden Abschnitt.

## SSL-Zertifikatverlängerung starten {#initiating-ssl-certificate-renewal}

>[!NOTE]
>
>Die Zertifikatverlängerung wird in der Systemsteuerung nicht automatisch verwaltet. Sie können den Erneuerungsprozess **nur** initiieren, indem Sie die Anfrage an den Kundendienst von Adobe Campaign vorbereiten.

Der SSL-Zertifikatverlängerungsprozess umfasst drei Schritte:

1. **Generierung der Zertifikatssignaturanfrage (CSR)** Der Adobe-Kundendienst generiert auf Anfrage über das Kundendienstportal einen CSR für Sie. Sie müssen einige Informationen angeben, die zum Generieren der CSR erforderlich sind (z. B. Allgemeiner Name, Name und Adresse des Unternehmens usw.). In der Systemsteuerung sehen Sie die Liste der erforderlichen Elemente, wenn Sie den Erneuerungsprozess starten. Weitere Informationen dazu finden Sie im folgenden Abschnitt.
1. **Erwerb des SSL-Zertifikats** Sobald der Kundendienst das CSR generiert hat, können Sie es herunterladen und das SSL-Zertifikat bei der von Ihrem Unternehmen zugelassenen Zertifizierungsstelle erwerben.
1. **Installation des SSL-Zertifikats** Sobald Sie das SSL-Zertifikat erwerben, müssen Sie es der Adobe-Kundenunterstützung bereitstellen. Das Zertifikat wird installiert, und die aktualisierten Ablaufdaten der Zertifikate werden in der Systemsteuerung angezeigt.

Gehen Sie wie folgt vor, um die Erneuerung der SSL-Zertifikate in der Systemsteuerung zu starten:

1. Öffnen Sie die Karte **[!UICONTROL Subdomänen &amp; Zertifikate]**und klicken Sie dann auf das Symbol**[!UICONTROL  Zertifikatdetails]** der Subdomäne, deren Zertifikate bald ablaufen.

   ![](assets/renewal1.png)

1. Daraufhin wird eine Liste verwandter Subdomänen angezeigt. Sie beinhaltet normalerweise Subdomänen von Einstiegsseiten, Ressourcenseiten usw.
Klicken Sie auf die Schaltfläche **[!UICONTROL Ticket-Details]**, um den Vorgang zur Erneuerung der Zertifikate zu starten.

   ![](assets/renewal2.png)

1. Es wird ein Formular mit allen Details angezeigt, die zur Erneuerung des SSL-Zertifikats erforderlich sind. Vergewissern Sie sich, dass Sie die angeforderten Informationen vollständig und genau ausfüllen (wenden Sie sich bei Bedarf an Ihr internes Team, Ihre Sicherheits- und IT-Teams). Andernfalls kann keine Zertifikatsignaturanforderung generiert werden, und Sie können das Zertifikat nicht verlängern.

   * **[!UICONTROL IMS-Org]**: ID Ihrer Organisation.
   * **[!UICONTROL Instanz]**: URL der mit der Subdomäne verknüpften Kampagneninstanz.
   * **[!UICONTROL Allgemeiner Name]**: Hierbei handelt es sich in der Regel um eine Tracking-Subdomäne-URL, die der Subdomäne mit dem abgelaufenen Zertifikat zugeordnet ist.
   * **[!UICONTROL Subdomänen]**: Subdomänen, die mit einem abgelaufenen Zertifikat mit der Subdomäne verknüpft sind. Wenn Sie ein einzelnes SSL-Zertifikat auf andere Subdomänen anwenden möchten, können Sie sie dieser Liste hinzufügen. Stellen Sie in diesem Fall sicher, dass diese Subdomänen mit derselben IMS-Org- und Instanz-URL verknüpft sind.
   >[!CAUTION]
   >
   >The **[!UICONTROL IMS Org]**and**[!UICONTROL  Instance]** fields are filled in automatically by the Control Panel and should not be modified.

   ![](assets/renewal3.png)

1. Klicken Sie nach dem Ausfüllen des Formulars auf die Schaltfläche &quot;Details **[!UICONTROL kopieren]**&quot;, um die Informationen in der Zwischenablage zu speichern.

   >[!NOTE]
   >
   >Wenn Sie Ihren Browserverlauf nicht löschen, werden die eingegebenen Informationen gespeichert, sodass Sie das Zertifikat später verlängern können.

1. Klicken Sie auf die Schaltfläche Neues Ticket **[!UICONTROL protokollieren]**. Sie werden automatisch zur Anmeldeseite des Adobe Campaign-Kundendienstes weitergeleitet.

   ![](assets/renewal4.png)

1. Melden Sie sich an und erstellen Sie dann ein neues Support-Ticket mit dem Betreff &quot;SSL-Zertifikat-CSR-Anforderung&quot;.
Fügen Sie alle zuvor kopierten Informationen in den Text des Tickets ein und klicken Sie dann auf Senden.

   >[!NOTE]
   >
   >Wenn Sie nicht berechtigt sind, Supportfälle für Ihr Unternehmen einzureichen, leiten Sie bitte alle kopierten Informationen an Ihren Support-Ansprechpartner weiter und bitten Sie ihn, ein neues Customer Care Ticket für Sie zu öffnen.

**Verwandte Themen:**

* [Tutorialvideo zu Campaign Standard](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/managing-ssl-certificates.html)
* [Tutorialvideo zur Kampagnenklassik](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/managing-ssl-certificates.html)
