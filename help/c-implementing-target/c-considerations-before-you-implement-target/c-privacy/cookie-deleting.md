---
keywords: cookie;cookies;delete cookie;delete target cookie;google chrome;chrome;mozilla firefox;firefox;microsoft edge;safari
description: Elimina i cookie del browser di Target, in modo da poter convalidare tutte le esperienze.
title: Eliminare il cookie  Adobe Target
feature: Privacy & Security
translation-type: tm+mt
source-git-commit: 6bb75e3b818a71af323614d9150e50e3e9f611b7
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 5%

---


# Eliminare il cookie di Target

Potete eliminare il cookie [!DNL Adobe Target] del browser (mbox) in modo da poter convalidare tutte le esperienze durante il test.

Se non è presente un cookie [!DNL Target] (mbox), viene considerato un nuovo visitatore e viene mostrata una nuova esperienza. Ci sono diversi modi per eliminare la mbox senza eliminare tutti i cookie del browser.

>[!NOTE]
>
>Le seguenti istruzioni sono corrette per i browser e le versioni elencati. Cercate in Internet istruzioni per il browser o la versione specifica in uso.

## Elimina il cookie Target da Google Chrome

Versione 84.0.4147.105

1. Fare clic sul menu **Chrome** > **Preferences**.
1. Fare clic sulla scheda **Privacy e sicurezza**.
1. Fare clic su **Cookie e altri dati del sito**.
1. Fare clic su **Visualizza tutti i cookie e i dati del sito**.
1. Espandete la sezione `adobe.com`, selezionate il cookie **mbox**, quindi fate clic sull&#39;icona di eliminazione (X).

## Elimina il cookie Target da Mozilla Firefox

Versione 79.0

### Elimina tutti i cookie associati a `adobe.com`

1. Fare clic sul menu **Firefox** > **Preferenze**.
1. Fare clic sulla scheda **Privacy e sicurezza**.
1. In **Cookie e dati del sito**, fare clic su **Gestisci dati**.
1. Selezionare il sito `adobe.com`, quindi fare clic su **Rimuovi selezionato**.

   >[!NOTE]
   >
   >Questo elimina tutti i cookie associati al sito `adobe.com`. Se desiderate eliminare un singolo cookie per un sito, seguite le istruzioni riportate di seguito.

### Eliminare un singolo cookie (mbox)

1. In Firefox, fare clic su **Strumenti** > **Web Developer** > **Storage Inspector**.
1. Fare clic sulla scheda **Avanzate**.
1. Passate alla pagina Web contenente il cookie da eliminare.
1. Espandere la sezione **Cookie**, quindi fare clic su `https://experience.adobe.com`.
1. Fare clic con il pulsante destro del mouse sul cookie **mbox**, quindi scegliere **Elimina**.

## Eliminare il cookie Target da Microsoft Edge

Versione 84.0.522.52

1. Fare clic sul menu **Microsoft Edge** > **Preferences**.
1. Fare clic sulla scheda **Autorizzazioni sito**.
1. Fare clic su **Cookie e dati del sito**.
1. Fare clic su **Visualizza tutti i cookie e i dati del sito**.
1. Espandete la sezione `adobe.com`, selezionate il cookie **mbox**, quindi fate clic sull&#39;icona di eliminazione (X).

## Eliminare il cookie Target da Apple Safari

Versione 13.1.2

### Elimina tutti i cookie associati a `adobe.com`

1. Fare clic sul menu **Safari** > **Preferenze**.
1. Fare clic sulla scheda **Privacy**.
1. Fare clic su **Gestisci dati sito Web**.
1. Selezionare i siti per i cookie da eliminare, quindi fare clic su **Remove**.

   >[!NOTE]
   >
   >Questo elimina tutti i cookie associati al sito `adobe.com`. Se desiderate eliminare un singolo cookie per un sito, seguite le istruzioni riportate di seguito.

### Eliminare un singolo cookie (mbox)

1. Fare clic sul menu **Safari** > **Preferenze**.
1. Fare clic sulla scheda **Avanzate**.
1. Selezionare il menu **Mostra sviluppo nella barra dei menu**.
1. Passate alla pagina Web contenente il cookie da eliminare.
1. Fare clic sul menu **Sviluppo** > **Mostra Web Inspector**.
1. Fare clic sulla scheda **Storage**.
1. Espandere la sezione **Cookie**, quindi fare clic su `www.adobe.com`.
1. Fare clic con il pulsante destro del mouse sul cookie **mbox**, quindi scegliere **Elimina**.
