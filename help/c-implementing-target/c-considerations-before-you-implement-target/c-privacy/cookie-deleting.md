---
description: Elimina i cookie del browser di Target, in modo da poter convalidare tutte le esperienze.
title: Eliminare il cookie  Adobe Target
topic: Standard
uuid: 6e95ee4d-dbf2-4432-8abe-cfd9bc928f0c
translation-type: tm+mt
source-git-commit: 79bcd452a9faa0883272d2e686efd7c4ddfa34a2
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 5%

---


# Eliminare il cookie di Target{#delete-the-target-cookie}

Potete eliminare il cookie [!DNL Target] del browser (mbox) in modo da poter convalidare tutte le esperienze durante il test.

If there is no [!DNL Target] cookie (mbox), you are considered a new visitor and shown a new experience. There are several ways to delete your [!DNL Target] cookies without deleting all of your browser cookies.

>[!NOTE]
>
>Le seguenti istruzioni sono corrette per i browser e le versioni elencati. Cerca le istruzioni per il browser o la versione specifica in Internet.

## Elimina il cookie Target da Google Chrome

Versione 84.0.4147.105

1. Fate clic sul menu **Chrome** > **Preferenze**.
1. Fate clic sulla scheda **Privacy e sicurezza** .
1. Fate clic su **Cookie e altri dati** del sito.
1. Fate clic su **Visualizza tutti i cookie e i dati** del sito.
1. Espandete la `adobe.com` sezione, selezionate il cookie **mbox** , quindi fate clic sull&#39;icona di eliminazione (X).

## Elimina il cookie Target da Mozilla Firefox

Versione 79.0

1. Fare clic sul menu **Firefox** > **Preferenze**.
1. Fate clic sulla scheda **Privacy e sicurezza** .
1. In **Cookie e dati** del sito, fai clic su **Gestisci dati**.
1. Selezionate il `adobe.com` sito, quindi fate clic su **Rimuovi selezionato**.

   >[!NOTE]
   >
   >Questo elimina tutti i cookie associati al `adobe.com` sito. Se desiderate eliminare o modificare i singoli cookie di un sito, potete farlo nella finestra di ispezione [dell&#39;archivio degli strumenti](https://developer.mozilla.org/en-US/docs/Tools/Storage_Inspector)di sviluppo. Il cookie specifico da eliminare è denominato &quot;mbox&quot;.

## Eliminare il cookie Target da Microsoft Edge

Versione 84.0.522.52

1. Fate clic sul menu **Microsoft Edge** > **Preferenze**.
1. Fate clic sulla scheda Autorizzazioni **** sito.
1. Fate clic su **Cookie e dati** del sito.
1. Fate clic su **Visualizza tutti i cookie e i dati** del sito.
1. Espandete la `adobe.com` sezione, selezionate il cookie **mbox** , quindi fate clic sull&#39;icona di eliminazione (X).

## Eliminare il cookie Target da Apple Safari

Versione 13.1.2

1. Fate clic sul menu **Safari** > **Preferenze**.
1. Click the **Privacy** tab.
1. Fate clic su **Gestisci dati** sito Web.
1. Selezionate i siti per i cookie da eliminare, quindi fate clic su **Rimuovi**.

>[!NOTE]
>
>Questo elimina tutti i cookie associati al `adobe.com` sito. Se desiderate eliminare un singolo cookie per un sito, seguite le istruzioni riportate di seguito:

1. Fate clic sul menu **Safari** > **Preferenze**.
1. Click the **Advanced** tab.
1. Selezionate il menu **Mostra sviluppo nella barra** dei menu.
1. Passate alla pagina Web contenente il cookie da eliminare.
1. Fate clic sul menu **Sviluppo** > **Mostra ispettore** Web.
1. Click the **Storage** tab.
1. Espandete la sezione **Cookie** , quindi fate clic su `www.adobe.com`.
1. Fate clic con il pulsante destro del mouse sul cookie **mbox** , quindi fate clic su **Elimina**.