---
title: Anmeldung bei Ihrem SFTP-Server
description: Erfahren Sie, wie Sie sich beim SFTP-Server anmelden
translation-type: tm+mt
source-git-commit: 8ee999b89af88a1a59956838d5722ce8fc6b3955

---


# Anmeldung bei Ihrem SFTP-Server {#logging-into-sft-server}

Die folgenden Schritte beschreiben, wie Sie mit Ihrer SFTP-Client-Applikation eine Verbindung mit Ihrem SFTP-Server herstellen.

Bevor Sie sich beim Server anmelden, überprüfen Sie, ob folgende Voraussetzungen gegeben sind:

* Your SFTP server is **hosted by Adobe**.
* Ihr **Benutzername** wurde für den Server eingerichtet. You can check this information directly in the Control Panel, in the **Key management** tab from the SFTP Card.
* Sie verfügen über ein **Paar aus privatem und öffentlichem Schlüssel**, um sich am SFTP-Server anzumelden. Refer to [this section](../../sftp/using/key-management.md) for more on how to add the SSH key.
* Ihre **öffentliche IP-Adresse wurde auf dem SFTP-Server auf die Whitelist** gesetzt. If not, refer to [this section](../../sftp/using/ip-range-whitelisting.md) for more on how to whitelist your IP range.
* You have an access to a **SFTP client software**. Fragen Sie Ihre IT-Abteilung nach der von ihr empfohlenen SFTP-Client-Applikation oder suchen Sie im Internet nach einer, wenn dies durch Ihre Unternehmensrichtlinien erlaubt ist.

Gehen Sie wie folgt vor, um eine Verbindung mit dem SFTP-Server herzustellen:

1. Launch the Control Panel, then select the **[!UICONTROL Key Management]** tab from the **[!UICONTROL SFTP]** card.

   ![](assets/fingerprintNEW2.png)

1. Starten Sie Ihre SFTP-Clientanwendung und kopieren Sie dann die Serveradresse aus der Systemsteuerung, gefolgt von "campaign.adobe.com", und geben Sie dann Ihren Benutzernamen ein.

   ![](assets/connect1.png)

1. Wählen Sie im Feld **[!UICONTROL SSH Private Key]die auf Ihrem Computer gespeicherte Datei für den privaten Schlüssel aus.** Sie ist eine Textdatei und hat denselben Namen wie Ihr öffentlicher Schlüssel, jedoch ohne die Erweiterung ".pub" (z. B. "enable").

   ![](assets/connect2.png)

   Der private Schlüssel der Datei wird automatisch in das Feld **[!UICONTROL Passwort]eingetragen.**

   ![](assets/connect3.png)

   Sie können überprüfen, ob der Schlüssel, den Sie verwenden möchten, in der Systemsteuerung gespeichert wird, indem Sie den Fingerabdruck des privaten oder öffentlichen Schlüssels mit dem Fingerabdruck der Schlüssel auf der Registerkarte Key Management der SFTP-Karte vergleichen.

   ![](assets/fingerprint3.png)

   >[!NOTE]
   >
   >Wenn Sie einen Mac-Computer verwenden, können Sie den Fingerabdruck des auf Ihrem Computer gespeicherten privaten Schlüssels anzeigen, indem Sie folgenden Befehl ausführen:
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. Sobald alle Informationen ausgefüllt sind, wählen Sie **[!UICONTROL Connect]aus, um sich bei Ihrem SFTP-Server anzumelden.**

   ![](assets/sftpconnected.png)
