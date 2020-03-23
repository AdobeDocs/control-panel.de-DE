---
title: Überwachen von SSL-Zertifikaten der Subdomains
description: Erfahren Sie, wie Sie die SSL-Zertifikate Ihrer Subdomains überwachen.
translation-type: ht
source-git-commit: f22e356b283ee2601c948d5c1d514a9a59c58451

---


# Überwachen von SSL-Zertifikaten der Subdomains {#monitoring-ssl-certificates}

## Über SSL-Zertifikate {#about-ssl-certificates}

Adobe Campaign empfiehlt, die Subdomains zu schützen, die Ihre Landingpages hosten, insbesondere jene, die sensible Kundendaten erfassen.

Mit der **SSL-Verschlüsselung (Secure Socket Layer)** stellen Sie sicher, dass die Adobe zugewiesenen Subdomains sicher sind. Wenn Ihr Kunde ein Web-Formular ausfüllt oder eine von Adobe Campaign gehostete Landingpage besucht, werden die Daten standardmäßig über ein nicht-sicheres Protokoll (HTTP) übertragen. Verwenden Sie zur Datenübertragung ein HTTPS-Protokoll, um besseren Schutz zu gewährleisten. Ihre Subdomain-Adresse &quot;http://info.mywebsite.com/&quot; würde dann &quot;https://info.mywebsite.com/&quot; lauten.

**SSL-Zertifikate sind nicht auf den zugewiesenen Subdomains selbst installiert**. Sie sind auf verbundenen Subdomains installiert, darunter vor allem auf jenen, die Landingpages oder Seiten mit Ressourcen hosten.

**SSL-Zertifikate werden für einen bestimmten Zeitraum bereitgestellt** (1 Jahr, 60 Tage usw.). Wenn ein Zertifikat abgelaufen ist, können Probleme beim Zugriff auf die Landingpages oder bei der Verwendung von auf der Subdomain vorhandenen Ressourcen auftreten. Um dies zu verhindern, können Sie über das Control Panel die SSL-Zertifikate Ihrer Subdomains überwachen und eine Verlängerung beantragen.

![](assets/no_certificate.png)

## Überwachung von SSL-Zertifikaten {#monitoring-certificates}

>[!CONTEXTUALHELP]
>id=&quot;cp_subdomain_details&quot;
>title=&quot;Details der Subdomain&quot;
>abstract=&quot;Rufen Sie Informationen zu Ihren Subdomains ab.&quot;

Der Status der SSL-Zertifikate Ihrer Subdomains ist direkt in der Liste der Subdomains verfügbar, wenn Sie die Karte **[!UICONTROL Subdomains &amp; Zertifikate]** auswählen.

Die Subdomains sind nach dem nächsten Ablaufdatum des SSL-Zertifikats geordnet, wobei das Ablaufdatum in Tagen optisch dargestellt wird:

* **Grün**: Das Zertifikat der Subdomain läuft nicht innerhalb der nächsten 60 Tage ab.
* **Orange**: Mindestens eine Subdomain hat ein Zertifikat, das innerhalb der nächsten 60 Tage abläuft.
* **Rot**: Mindestens eine Subdomain hat ein Zertifikat, das innerhalb der nächsten 30 Tage abläuft.
* **Grau**: Für die Subdomain wurde kein Zertifikat installiert.

![](assets/subdomains_list.png)

Wählen Sie die Schaltfläche **[!UICONTROL Details der Subdomain]** aus, um weitere Details zu einer Subdomain zu erhalten.
Die Liste aller zugehörigen Subdomains wird angezeigt. Normalerweise sind dies Subdomains von Landingpages, Seiten mit Ressourcen usw.

Die Registerkarte **[!UICONTROL Absenderdetails]** enthält Informationen zu den konfigurierten Postfächern (Absender-, Antwort-, Fehler-E-Mail).

![](assets/subdomain_details.png)

Wenn eines der SSL-Zertifikate Ihrer Subdomain bald abläuft, können Sie es direkt im Control Panel verlängern. Weitere Informationen dazu finden Sie in diesem Abschnitt: [Verlängern des SSL-Zertifikats einer Subdomain](../../subdomains-certificates/using/renewing-subdomain-certificate.md).

>[!IMPORTANT]
>
>Die Zertifikatsverlängerung über das Control Panel befindet sich in der Beta-Phase und unterliegt häufigen Aktualisierungen und Änderungen ohne Vorankündigung.

**Verwandte Themen:**

* [Hinzufügen von SSL-Zertifikaten (Tutorial-Video)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [Verlängern des SSL-Zertifikats einer Subdomain](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Subdomain-Branding](../../subdomains-certificates/using/subdomains-branding.md)
