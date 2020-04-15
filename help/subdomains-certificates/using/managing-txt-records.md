---
title: Verwalten von TXT-Einträgen
description: Erfahren Sie, wie Sie TXT-Einträge zur Verifizierung von Domain-Besitz verwalten können.
translation-type: tm+mt
source-git-commit: 77165e3f408f75dfb57434111b07b20ad9caab5e

---


# Verwalten von TXT-Einträgen {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="Verwalten von TXT-Einträgen"
>abstract="Bei bestimmten Diensten wie Google müssen Sie Ihren Domain-Einstellungen einen TXT-Eintrag hinzufügen, um zu verifizieren, dass Sie der Besitzer der Domain sind."

>[!IMPORTANT]
>
>Die Verwaltung von TXT-Datensätzen über die Systemsteuerung wird Ende April verfügbar sein.

## Über TXT-Einträge {#about-txt-records}

TXT-Einträge sind eine Art von DNS-Einträgen, die der Bereitstellung von Textinformationen über eine Domain dienen und von externen Quellen gelesen werden können.

Für hohe Posteingangsraten und niedrige Spam-Raten setzen bestimmte Dienste wie Google voraus, dass Sie Ihren Domain-Einstellungen einen TXT-Eintrag hinzufügen, um zu verifizieren, dass Sie der Besitzer der Domain sind.

Gmail gehört derzeit zu den beliebtesten Anbietern von E-Mail-Adressen. Für optimale Zustellbarkeit und einen erfolgreichen Versand von E-Mails an Gmail-Adressen können Sie Ihren Subdomains mit Adobe Campaign spezielle TXT-Einträge der Websiteüberprüfung von Google hinzufügen, um für ihre Verifizierung zu sorgen.

Zusätzliche Ressourcen:

* [Tutorial für Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/administrating/control-panel/google-txt-record-management.html).
* [Tutorial für Campaign Classic](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/administrating/control-panel/google-txt-record-management.html)

## Hinzufügen eines Google TXT-Eintrags für eine Subdomain {#adding-a-google-txt-record}

Gehen Sie wie folgt vor, um Ihrer Subdomain, die Sie zum Versenden von E-Mails an Gmail-Adressen nutzen, einen Google TXT-Eintrag hinzuzufügen:

1. Navigieren Sie zur **[!UICONTROL Subdomain and Certificates]** Karte.

1. Wählen Sie Ihre Instanz aus und öffnen Sie dann die Details der Subdomain, der Sie einen DNS-Eintrag hinzufügen möchten.

   ![](assets/txt_subdomaindetails.png)

1. Click the **[!UICONTROL Add TXT record]** button, then enter the value generated in G Suite Admin tools. Weiterführende Informationen finden Sie in der [G Suite Admin-Hilfe](https://support.google.com/a/answer/183895).

   ![](assets/txt_addtxt.png)

1. Click the **[!UICONTROL Add]** button to confirm.

   ![](assets/txt_txtadded.png)

Nachdem der TXT-Eintrag hinzugefügt wurde, müssen Sie ihn von Google verifizieren lassen. Rufen Sie dazu die G Suite Admin-Tools auf und starten Sie dann den Verifizierungsschritt (siehe [G Suite Admin-Hilfe](https://support.google.com/a/answer/183895)).

Um einen Eintrag zu löschen, wählen Sie ihn in der Liste der Einträge aus und klicken Sie dann auf die Schaltfläche „Entfernen“.

>[!NOTE]
>
>Der einzige Eintrag, den Sie aus der Liste der DNS-Einträge löschen können, ist derjenige, den Sie zuvor hinzugefügt haben (in unserem Fall der Google TXT-Eintrag).


