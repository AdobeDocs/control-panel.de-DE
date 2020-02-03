---
title: Control Panel – Häufig gestellte Fragen
description: Häufige Fragen zum Control Panel
translation-type: tm+mt
source-git-commit: ddf4ca24c1583e388c07aae110522627220d5e66

---


# Häufig gestellte Fragen {#faq}

## Kennung der IMS-Organisation {#ims-org-id}

**Was ist die Kennung der IMS-Organisation?**

Dies ist eine eindeutige Kennung, die Ihrer Instanz bei der ersten Anmeldung in Adobe Experience Cloud zugewiesen wird. Sie sollte im folgenden Format vorliegen: xxx@AdobeOrg.

Weitere Informationen finden Sie in der [Adobe Experience Cloud-Dokumentation](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html).

**Wo finde ich meine Kennung der IMS-Organisation?**

Eine Möglichkeit besteht darin, zur [Startseite von Adobe Experience Cloud](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]**zu navigieren. Die Kennung Ihrer IMS-Organisation finden Sie in der Administration unten im Bereich**[!UICONTROL  Schnellzugriff]**. Detailliertere Informationen finden Sie in der [Adobe Experience Cloud-Dokumentation](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html).

Eine andere Möglichkeit besteht darin, die **Admin Console** zu starten. Die Kennung Ihrer IMS-Organisation wird in Ihrer URL angezeigt. Sie sieht in etwa so aus: https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

**Warum muss ich wissen, wie meine Kennung der IMS-Organisation lautet?**

Damit Sie die Einstellungen für Ihre Instanz verwalten können, möchten wir sicherstellen, dass Sie die richtigen Informationen für die richtige Instanz erhalten, falls Sie mehrere Instanzen für Ihr Unternehmen verwenden.

**Was passiert, wenn ich mehrere Kennungen der IMS-Organisation habe?**

Wenn Sie Zugriff auf mehrere Adobe-Lösungen haben, kann es sein, dass Sie mehr als eine Kennung der IMS-Organisation besitzen. In diesem Fall ist die korrekte Kennung der IMS-Organisation, die Sie verwenden sollten, diejenige unter Ihrer Adobe Campaign-Instanz.

>[!NOTE]
>
>Wenn Sie dieselbe Kennung für Adobe Campaign und Adobe Analytics haben, ist das von Vorteil. Eine von Analytics und Campaign gemeinsam genutzte Kennung der IMS-Organisation ist Voraussetzung, um diese Lösungen zu integrieren und um komplexe Anwendungsfälle zu nutzen wie z. B. den Abbruch von Warenkörben (für AA und AC).
>
>Wenn für Adobe Campaign und Adobe Analytics unterschiedliche Kennungen der IMS-Organisation vorhanden sind, wenden Sie sich an die Kundenunterstützung mit der Bitte um eine Angleichung der beiden Kennungen.

**Woher weiß ich, ob meine Adobe Campaign-Instanz auf AWS gehostet wird oder nicht?**

Gehen Sie wie folgt vor, um zu überprüfen, ob Ihre Instanz auf AWS gehostet wird:

1. Rufen Sie Ihre Anmelde-URL ab. Es ist die URL, mit der Sie sich bei Ihrer Kampagneninstanz anmelden, und endet meist mit &quot;.campaign.adobe.com&quot;oder&quot;.neolane.net&quot;.
1. Öffnen Sie das Terminal und führen Sie dann einen **[!DNL nslookup]**--Vorgang auf Ihrer Anmelde-URL aus.

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

## Control Panel {#control-panel}

**Was ist das Control Panel?**

Mit dem Control Panel können Produktadministratoren direkt verschiedene Einstellungen verwalten und die Kapazität der mit Adobe Campaign verbundenen SFTP-Server überwachen.

**Welche aktuellen Funktionen hat das Control Panel?**


Das Control Panel ermöglicht es Ihnen, Speicherplatz zu überwachen, IP-Adressen auf die Whitelist zu setzen, SSH-Schlüssel für Ihre SFTP-Server nach Ihren Bedürfnissen selbst zu verwalten sowie andere Aktionen auszuführen.

Weitere Informationen finden Sie in der Dokumentation zu den vom Control Panel unterstützten Aktionen.

**Wird das Control Panel nur für Adobe Campaign verwendet?**

Ja, Sie können im Control Panel nur die Einstellungen für Adobe Campaign verwalten.

**Kann jeder das Control Panel nutzen?**

Das Control Panel steht nur Produktadministratoren unserer aktuellen Kunden offen, bei denen Adobe Campaign auf AWS gehostet wird.

Wenn Sie kein Administrator sind, aber Zugriff wünschen, wenden Sie sich an Ihren Produktadministrator mit der Bitte, Sie als Administrator hinzuzufügen.

**Wie kann ich auf das Control Panel zugreifen?**

Folgen Sie der detaillierten Anleitung in der Dokumentation zum Zugriff auf das Control Panel.

**Gibt es eine zusätzliche Gebühr für die Nutzung des Control Panels?**

Nein, es fallen keine zusätzlichen Kosten an, wenn Sie bereits Kunde von Adobe Campaign sind.
