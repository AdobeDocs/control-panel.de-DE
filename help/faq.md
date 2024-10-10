---
product: campaign
solution: Campaign
title: Control Panel – Häufig gestellte Fragen
description: Häufige Fragen zum Control Panel
feature: Control Panel
role: Admin
level: Intermediate
exl-id: 4f329764-ed8b-4939-affc-ed994fd6101d
source-git-commit: 98cf425548884c3a5e503c35ce5ea5b7ceaee67f
workflow-type: ht
source-wordcount: '719'
ht-degree: 100%

---

# Häufig gestellte Fragen {#faq}

## Control Panel {#control-panel}

### Was ist das Control Panel?

Mit dem Control Panel können Produktadministratoren direkt verschiedene Einstellungen verwalten und die Kapazität der mit Adobe Campaign verbundenen SFTP-Server überwachen.

### Welche aktuellen Funktionen hat das Control Panel?

Das Control Panel ermöglicht es Ihnen, Speicherplatz zu überwachen, IP-Adressen auf die Zulassungsliste zu setzen, SSH-Schlüssel für Ihre SFTP-Server nach Ihren Bedürfnissen selbst zu verwalten sowie andere Aktionen auszuführen.

Weitere Informationen zu den vom Control Panel unterstützten Aktionen finden Sie in der Dokumentation.

### Gibt es Funktionen, die von Campaign v8 noch nicht unterstützt werden, aber in Campaign Classic v7 verfügbar sind?{#v8-restrictions}

Nein. Alle in Campaign v7 verfügbaren Funktionen werden jetzt auch über das Control Panel in Campaign v8 unterstützt, einschließlich Funktionen für die Subdomain- und Zertifikatverwaltung.

### Wird das Control Panel nur für Adobe Campaign verwendet?

Ja, Sie können im Control Panel nur die Einstellungen für Adobe Campaign verwalten.

### Kann jeder das Control Panel nutzen?

Das Control Panel kann nur von Produktadministratoren bzw. -administratorinnen unserer aktuellen Kunden verwendet werden, bei denen Adobe Campaign auf AWS gehostet wird.

Das Control Panel ermöglicht es Kunden mit einem hybriden Hosting-Modell, spezifische Funktionen des Control Panels zu nutzen. Dazu müssen sie die in ihrer Marketing-Instanz im Control Panel konfigurierte URL der MID/RT-Instanz angeben. [Weitere Informationen](instances-settings/using/external-accounts.md)

Wenn Sie kein Administrator sind, aber Zugriff wünschen, wenden Sie sich an Ihren Produktadministrator mit der Bitte, Sie als Administrator hinzuzufügen.

### Welche Bedingungen gelten für den Zugriff auf das Control Panel, wenn man Campaign Classic v7-Benutzer ist? {#v7-restrictions}

Das Control Panel steht nur Administratoren zur Verfügung. [Weitere Informationen](discover/using/managing-permissions.md).

Beachten Sie für Campaign v7, dass Ihre Instanz auf Amazon Web Services (AWS) gehostet und auf den neuesten [stabilen Campaign-Build](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=de#rn-statuses) (oder auf Build 9032 oder höher) aktualisiert werden muss. In [diesem Abschnitt](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=de#getting-your-campaign-version) erfahren Sie, wie Sie Ihre Campaign Classic v7-Version überprüfen können. Um zu überprüfen, ob Ihre Campaign Classic-Instanz auf AWS gehostet wird, folgen Sie den Schritten in [diesem Abschnitt](#hosted-aws).

### Wie kann ich auf das Control Panel zugreifen?

Folgen Sie der detaillierten Anleitung in der Dokumentation im Abschnitt zum Zugriff auf das Control Panel.

### Gibt es eine zusätzliche Gebühr für die Nutzung des Control Panel?

Nein, es fallen keine zusätzlichen Kosten an, wenn Sie bereits Kunde von Adobe Campaign sind.

## Organisations-ID {#ims-org-id}

### Was ist eine Organisations-ID?

Dies ist eine eindeutige Kennung, die Ihrer Instanz bei der ersten Anmeldung in Adobe Experience Cloud zugewiesen wird. Sie sollte im folgenden Format vorliegen: xxx@AdobeOrg.

Weitere Informationen finden Sie in der [Adobe Experience Cloud-Dokumentation](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=de).

### Wo finde ich meine Organisations-ID?

Eine Möglichkeit besteht darin, zur [Startseite von Adobe Experience Cloud](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]** zu navigieren. Ihre Organisations-ID finden Sie in der Administration unten im Bereich **[!UICONTROL Schnellzugriff]**. Detailliertere Informationen finden Sie in der [Adobe Experience Cloud-Dokumentation](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=de).

Eine andere Möglichkeit besteht darin, die **Admin Console** zu starten. Ihre Organisations-ID wird in Ihrer URL angezeigt. Sie sieht in etwa so aus: https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

### Warum muss ich meine Organisations-ID kennen?

Damit Sie die Einstellungen für Ihre Instanz verwalten können, möchten wir sicherstellen, dass Sie die richtigen Informationen für die richtige Instanz erhalten, falls Sie mehrere Instanzen für Ihr Unternehmen verwenden.

### Was passiert, wenn ich mehrere Organisations-IDs habe?

Eine einheitliche Organisations-ID für Analytics und Campaign ist eine Voraussetzung, um die Lösungen zu integrieren und komplexe Anwendungsfälle wie Warenkorbabbrüche (für Adobe Analytics + Adobe Campaign) zu nutzen. Wenn Sie Zugriff auf mehrere Adobe-Lösungen haben, kann es sein, dass Sie mehr als eine Organisations-ID besitzen. In diesem Fall ist die richtige Organisations-ID diejenige, die Sie unter Ihrer Adobe Campaign-Instanz sehen.

<!--
>[!NOTE]
>
>If you have different organization IDs for Adobe Campaign and Adobe Analytics, please reach out to Customer Care to get them aligned.
-->

### Woher weiß ich, ob meine Adobe Campaign-Instanz auf AWS gehostet wird oder nicht?{#hosted-aws}

Gehen Sie wie folgt vor, um zu überprüfen, ob Ihre Instanz auf AWS gehostet wird:

1. Rufen Sie Ihre Anmelde-URL ab. Dies ist die URL, die Sie für die Anmeldung bei Ihrer Campaign-Instanz verwenden. Sie endet normalerweise auf „.campaign.adobe.com“ or „.neolane.net“.
1. Öffnen Sie das Terminal und führen Sie dann einen **[!DNL nslookup]** -Vorgang auf Ihrer Anmelde-URL aus.

   `doe-macOS% nslookup myinstance.campaign.adobe.com`

1. In der Antwort erhalten Sie Informationen zu Ihrer Instanz.

   ```
   doe-macOS% nslookup myinstance.campaign.adobe.com
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   myinstance.campaign.adobe.com
   canonical name = myinstance-mkt-prod1.campaign.adobe.com.
   myinstance-mkt-prod1.campaign.adobe.com
   canonical name = myinstance-mkt-prod1-1.campaign.adobe.com.
   Name: myinstance-mkt-prod1-1.campaign.adobe.com
   Address: 12.34.567.89
   ```

1. Führen Sie einen **nslookup**-Vorgang auf der zurückgegebenen IP-Adresse aus.

   `doe-macOS% nslookup 12.34.567.89`

1. Überprüfen Sie den Wert &quot;name&quot; im zurückgegebenen Ergebnis. Wenn er &quot;amazonaws.com&quot; enthält, wird Ihre Instanz auf AWS gehostet.

   ```
   doe-macOS% nslookup 12.34.567.89
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   89.567.34.12.in-addr.arpa   name = ec2-12-34-567-89.address.amazonaws.com.
   ```

>[!NOTE]
>
>Wenn Sie zu AWS migrieren möchten, wenden Sie sich an Ihren Customer Success Manager.
