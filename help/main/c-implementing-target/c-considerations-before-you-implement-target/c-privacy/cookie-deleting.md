---
keywords: cookie;cookie;elimina cookie;elimina cookie target;google chrome;chrome;mozilla firefox;firefox;microsoft edge;safari
description: Scopri come eliminare il tuo [!DNL Target] cookie del browser per convalidare le esperienze.
title: Come si elimina il [!DNL Target] Cookie?
feature: Privacy & Security
role: Developer
exl-id: f2bc079e-593a-4689-a7cd-dfc6f86f6bb4
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Elimina [!DNL Target] cookie

È possibile eliminare [!DNL Adobe Target] cookie del browser (mbox) in modo da poter convalidare tutte le esperienze durante il test.

Se non esiste [!DNL Target] cookie (mbox), sei considerato un nuovo visitatore e ti viene mostrata una nuova esperienza. Ci sono diversi modi per eliminare la mbox senza eliminare tutti i cookie del browser.

>[!NOTE]
>
>Le seguenti istruzioni sono corrette per i browser e le versioni elencate. Cerca le istruzioni per il tuo browser o versione specifico su Internet.

## Elimina [!DNL Target] cookie da Google Chrome

Versione 84.0.4147.105

1. Fai clic sul pulsante **Chrome** menu > **Preferenze**.
1. Fai clic sul pulsante **Privacy e sicurezza** scheda .
1. Fai clic su **Cookie e altri dati del sito**.
1. Fai clic su **Visualizza tutti i cookie e i dati del sito**.
1. Espandi la `adobe.com` seleziona la sezione **mbox** cookie , quindi fai clic sull’icona Elimina (X).

## Elimina [!DNL Target] cookie da Mozilla Firefox

Versione 79.0

### Elimina tutti i cookie associati a `adobe.com`

1. Fai clic sul pulsante **Firefox** menu > **Preferenze**.
1. Fai clic sul pulsante **Privacy e sicurezza** scheda .
1. Sotto **Cookie e dati del sito**, fai clic su **Gestire i dati**.
1. Seleziona la `adobe.com` sito, quindi fai clic su **Rimuovi selezionati**.

   >[!NOTE]
   >
   >Questo elimina tutti i cookie associati al `adobe.com` sito. Per eliminare un singolo cookie per un sito, segui le istruzioni riportate di seguito.

### Eliminare un singolo cookie (mbox)

1. In Firefox, fai clic su **Strumenti** > **Sviluppatore web** > **Ispettore di memoria**.
1. Fai clic sul pulsante **Avanzate** scheda .
1. Passa alla pagina web contenente il cookie da eliminare.
1. Espandi la **Cookie** sezione , quindi fai clic su `https://experience.adobe.com`.
1. Fai clic con il pulsante destro del mouse sul pulsante **mbox** cookie, quindi fai clic su **Elimina**.

## Elimina [!DNL Target] cookie da Microsoft Edge

Versione 84.0.522.52

1. Fai clic sul pulsante **Microsoft Edge** menu > **Preferenze**.
1. Fai clic sul pulsante **Autorizzazioni sito** scheda .
1. Fai clic su **Cookie e dati del sito**.
1. Fai clic su **Visualizza tutti i cookie e i dati del sito**.
1. Espandi la `adobe.com` seleziona la sezione **mbox** cookie , quindi fai clic sull’icona Elimina (X).

## Elimina [!DNL Target] cookie da Apple Safari

Versione 13.1.2

### Elimina tutti i cookie associati a `adobe.com`

1. Fai clic sul pulsante **Safari** menu > **Preferenze**.
1. Fai clic sul pulsante **Privacy** scheda .
1. Fai clic su **Gestire i dati del sito web**.
1. Seleziona i siti per i cookie da eliminare, quindi fai clic su **Rimuovi**.

   >[!NOTE]
   >
   >Questo elimina tutti i cookie associati al `adobe.com` sito. Per eliminare un singolo cookie per un sito, segui le istruzioni riportate di seguito.

### Eliminare un singolo cookie (mbox)

1. Fai clic sul pulsante **Safari** menu > **Preferenze**.
1. Fai clic sul pulsante **Avanzate** scheda .
1. Seleziona la **Mostra menu di sviluppo nella barra dei menu** opzione .
1. Passa alla pagina web contenente il cookie da eliminare.
1. Fai clic sul pulsante **Sviluppa** menu > **Mostra controllo Web**.
1. Fai clic sul pulsante **Storage** scheda .
1. Espandi la **Cookie** sezione , quindi fai clic su `www.adobe.com`.
1. Fai clic con il pulsante destro del mouse sul pulsante **mbox** cookie, quindi fai clic su **Elimina**.
