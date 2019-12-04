---
title: Über SSL-Zertifikate
description: Weitere Informationen zu SSL-Zertifikaten
translation-type: tm+mt
source-git-commit: ce93b595f4fbc2b3d72aadd034f93392565cb0e2

---


# Über SSL-Zertifikate {#about-ssl-certificates}

Adobe Campaign empfiehlt, dass Sie die Subdomänen, auf denen Ihre Einstiegsseiten gehostet werden, schützen, insbesondere diejenigen, die vertrauliche Informationen über Ihre Kunden erfassen.

Mit der **SSL-Verschlüsselung (Secure Socket Layer)** stellen Sie sicher, dass die Adobe zugewiesenen Sub-Domains sicher sind. Wenn Ihr Kunde ein Webformular ausfüllt oder eine von Adobe Campaign gehostete Landingpage besucht, werden die Daten standardmäßig über ein nicht-sicheres Protokoll (HTTP) übertragen. Verwenden Sie zur Datenübertragung ein HTTPS-Protokoll, um besseren Schutz zu gewährleisten. Ihre Subdomänenadresse "http://info.mywebsite.com/"lautet nun "https://info.mywebsite.com/".

**SSL-Zertifikate sind nicht auf den zugewiesenen Sub-Domains selbst installiert**. Sie werden auf den zugehörigen Subdomänen installiert, hauptsächlich auf denjenigen, die Einstiegsseiten, Ressourcenseiten und andere hosten.

**SSL-Zertifikate werden für einen bestimmten Zeitraum** (1 Jahr, 60 Tage usw.) bereitgestellt. Wenn ein Zertifikat abgelaufen ist, können Probleme beim Zugriff auf die Landingpages oder bei der Verwendung von auf der Sub-Domain vorhandenen Ressourcen auftreten. Um dies zu verhindern, können Sie über das Control Panel die SSL-Zertifikate Ihrer Sub-Domains überwachen und eine Verlängerung beantragen.

More details on subdomain delegation is available [here](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).
