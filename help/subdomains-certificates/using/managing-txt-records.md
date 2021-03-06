---
product: campaign
solution: Campaign
title: Verwalten von TXT-Einträgen
description: Erfahren Sie, wie Sie TXT-Einträge zur Verifizierung von Domain-Besitz verwalten können.
feature: Control Panel
role: Architect
level: Experienced
exl-id: 547ca6f2-720f-4d58-b31b-5b2611ba9156
source-git-commit: c1c80c03a351613ec0c6870a11ab39a634e8eab7
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 100%

---

# Verwalten von TXT-Einträgen {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="Verwalten von TXT-Einträgen"
>abstract="Bei bestimmten Diensten wie Google müssen Sie Ihren Domain-Einstellungen einen TXT-Eintrag hinzufügen, um zu verifizieren, dass Sie der Besitzer der Domain sind."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=de" text="Einrichten einer neuen Subdomain"

## Über TXT-Einträge {#about-txt-records}

TXT-Einträge sind eine Art von DNS-Einträgen, die der Bereitstellung von Textinformationen über eine Domain dienen und von externen Quellen gelesen werden können.

Für hohe Posteingangsraten und niedrige Spam-Raten setzen bestimmte Dienste wie Google voraus, dass Sie Ihren Domain-Einstellungen einen TXT-Eintrag hinzufügen, um zu verifizieren, dass Sie der Besitzer der Domain sind.

Gmail gehört derzeit zu den beliebtesten Anbietern von E-Mail-Adressen. Für optimale Zustellbarkeit und einen erfolgreichen Versand von E-Mails an Gmail-Adressen können Sie Ihren Subdomains mit Adobe Campaign spezielle TXT-Einträge der Websiteüberprüfung von Google hinzufügen, um für ihre Verifizierung zu sorgen.

![](assets/do-not-localize/how-to-video.png) Entdecken Sie diese Funktion bei der Verwendung von [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html?lang=de#subdomains-and-certificates) oder [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html?lang=de#subdomains-and-certificates) im Video.

## Hinzufügen eines Google TXT-Eintrags für eine Subdomain {#adding-a-google-txt-record}

Gehen Sie wie folgt vor, um Ihrer Subdomain, die Sie zum Versenden von E-Mails an Gmail-Adressen nutzen, einen Google TXT-Eintrag hinzuzufügen:

1. Navigieren Sie zur Karte **[!UICONTROL Subdomains und Zertifikate]**.

1. Wählen Sie Ihre Instanz aus und öffnen Sie dann die Details der Subdomain, der Sie einen DNS-Eintrag hinzufügen möchten.

   ![](assets/txt_subdomaindetails.png)

1. Klicken Sie auf die Schaltfläche **[!UICONTROL TXT-Eintrag hinzufügen]** und geben Sie dann den Wert ein, der in den G Suite Admin-Tools generiert wurde. Weiterführende Informationen finden Sie in der [G Suite Admin-Hilfe](https://support.google.com/a/answer/183895).

   ![](assets/txt_addtxt.png)

1. Klicken Sie zur Bestätigung auf die Schaltfläche **[!UICONTROL Hinzufügen]**.

   ![](assets/txt_txtadded.png)

Nachdem der TXT-Eintrag hinzugefügt wurde, müssen Sie ihn von Google verifizieren lassen. Rufen Sie dazu die G Suite Admin-Tools auf und starten Sie dann den Verifizierungsschritt (siehe [G Suite Admin-Hilfe](https://support.google.com/a/answer/183895)).

Um einen Eintrag zu löschen, wählen Sie ihn in der Liste der Einträge aus und klicken Sie dann auf die Schaltfläche „Entfernen“.

>[!NOTE]
>
>Der einzige Eintrag, den Sie aus der Liste der DNS-Einträge löschen können, ist derjenige, den Sie zuvor hinzugefügt haben (in unserem Fall der Google TXT-Eintrag).
