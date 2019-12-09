---
title: SSL-Zertifikate von Subdomänen überwachen
description: Erfahren Sie, wie Sie die SSL-Zertifikate Ihrer Subdomänen überwachen.
translation-type: tm+mt
source-git-commit: cde5b58c1cf65d23b68c5fa6b1a484fc6db40325

---


# SSL-Zertifikate von Subdomänen überwachen {#monitoring-ssl-certificates}

Adobe Campaign empfiehlt, dass Sie die Subdomänen, auf denen Ihre Einstiegsseiten gehostet werden, schützen, insbesondere diejenigen, die vertrauliche Informationen über Ihre Kunden erfassen.

**Die SSL-Verschlüsselung (Secure Socket Layer)** stellt sicher, dass die Subdomänen, die Sie an Adobe delegiert haben, sicher sind. Wenn Ihr Kunde ein Webformular ausfüllt oder eine von Adobe Campaign gehostete Einstiegsseite besucht, werden die Informationen standardmäßig über ein nicht sicheres Protokoll (HTTP) gesendet. Um zusätzliche Sicherheit zu gewährleisten, müssen Sie sichere gesendete Informationen mit einem HTTPS-Protokoll sichern. Ihre Subdomänenadresse &quot;http://info.mywebsite.com/&quot;lautet nun &quot;https://info.mywebsite.com/&quot;.

**SSL-Zertifikate werden nicht auf den delegierten Subdomänen selbst** installiert. Sie werden auf den zugehörigen Subdomänen installiert, hauptsächlich auf denjenigen, die Einstiegsseiten, Ressourcenseiten und andere hosten.

**SSL-Zertifikate werden für einen bestimmten Zeitraum** (1 Jahr, 60 Tage usw.) bereitgestellt. Nach Ablauf eines Zertifikats treten möglicherweise Probleme auf, wenn Sie auf die Einstiegsseiten zugreifen oder Ressourcen aus der Subdomäne verwenden. Um dies zu verhindern, können Sie mit der Systemsteuerung die SSL-Zertifikate Ihrer Subdomänen überwachen und deren Erneuerung initiieren.

Weitere Informationen zur Subdomänenübertragung finden Sie [hier](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).

Mit der **[!UICONTROL Karte &quot;Subdomänen&quot;und &quot;Zertifikate]**&quot;können Sie sehen, welche Ihrer Subdomänen und zugehörigen Subdomänen Ihre Einstiegsseiten und Ressourcen mit auf ihnen installierten SSL-Zertifikaten hosten.

Sie können auch leicht erkennen, welche Subdomänen abgelaufene Zertifikate besitzen, und diese bei Bedarf erneuern.

>[!NOTE]
>
>Adobe empfiehlt, das SSL-Zertifikat der zugehörigen Subdomänen zu verlängern, **wenn das Ablaufdatum näher rückt**. Die Verlängerung eines Zertifikats kann je nach Unternehmen einige Tage dauern. Wir empfehlen daher, für diesen Vorgang eine entsprechende Dauer einzuplanen.
<!-- note to remove? immediate, no more delay? -->

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
