---
title: SSL-Zertifikate
description: Weitere Informationen zu SSL-Zertifikaten
translation-type: tm+mt
source-git-commit: 6bc165f995d34d21b5bce379db3095317db10906

---


# SSL-Zertifikate {#about-ssl-certificates}

Adobe Campaign empfiehlt, dass Sie die Subdomänen, auf denen Ihre Einstiegsseiten gehostet werden, schützen, insbesondere diejenigen, die vertrauliche Informationen über Ihre Kunden erfassen.

**Die SSL-Verschlüsselung (Secure Socket Layer)** stellt sicher, dass die Subdomänen, die Sie an Adobe delegiert haben, sicher sind. Wenn Ihr Kunde ein Webformular ausfüllt oder eine von Adobe Campaign gehostete Einstiegsseite besucht, werden die Informationen standardmäßig über ein nicht sicheres Protokoll (HTTP) gesendet. Um zusätzliche Sicherheit zu gewährleisten, müssen Sie sichere gesendete Informationen mit einem HTTPS-Protokoll sichern. Ihre Subdomänenadresse &quot;http://info.mywebsite.com/&quot;lautet nun &quot;https://info.mywebsite.com/&quot;.

**SSL-Zertifikate werden nicht auf den delegierten Subdomänen selbst** installiert. Sie werden auf den zugehörigen Subdomänen installiert, hauptsächlich auf denjenigen, die Einstiegsseiten, Ressourcenseiten und andere hosten.

**SSL-Zertifikate werden für einen bestimmten Zeitraum** (1 Jahr, 60 Tage usw.) bereitgestellt. Nach Ablauf eines Zertifikats treten möglicherweise Probleme auf, wenn Sie auf die Einstiegsseiten zugreifen oder Ressourcen aus der Subdomäne verwenden. Um dies zu verhindern, können Sie mit der Systemsteuerung die SSL-Zertifikate Ihrer Subdomänen überwachen und deren Erneuerung initiieren.

Weitere Informationen zur Subdomänenübertragung finden Sie [hier](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).
