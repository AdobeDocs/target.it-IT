---
keywords: opzioni browser;tipo;tipo di browser;lingua del browser;lingua;versione;versione del browser
description: Scopri come creare tipi di pubblico in [!DNL Adobe Target] per eseguire il targeting degli utenti che visitano la pagina utilizzando un browser specifico o opzioni specifiche del browser.
title: Posso indirizzare i visitatori in base al tipo di browser?
feature: Audiences
exl-id: 8420bbe3-b58a-4ddb-89bb-0265dab6b5fc
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 76%

---

# Browser

Puoi indirizzare l’attività agli utenti che visitano la pagina utilizzando un browser specifico o opzioni specifiche del browser.

È possibile indirizza l’attività ai seguenti browser:

* Chrome
* Firefox
* Safari
* Internet Explorer
* Microsoft Edge
* Opera
* iPad 
* iPhone|

Esistono due modi per indirizzare i browser:

* **Pubblico predefinito:** il pubblico predefinito è utile se desideri indirizzare un’attività solo ai visitatori che utilizzano un browser specifico per visitare il tuo sito. Ad esempio, se stai offrendo un’estensione per Chrome, puoi rivolgerti ai soli utenti di Chrome.

   1. Durante la configurazione dell’attività, seleziona il browser dall’elenco a discesa.

      Questa opzione indirizza l’attività solo ai visitatori che utilizzano il browser specificato.

      ![Utenti di Target Chrome](/help/main/c-target/c-audiences/c-target-rules/assets/target-chrome.png)

* **Regola pubblico browser personalizzato:** Un pubblico personalizzato consente di rivolgerti a più browser o di impostare regole o esclusioni per specifici browser, versioni o lingue del browser. Questa funzionalità offre una flessibilità significativa quando esegui il targeting di un’attività in base agli attributi del browser.

   1. Nell’interfaccia di [!DNL Target] fai clic su **[!UICONTROL Pubblico]** > **[!UICONTROL Crea pubblico]**.
   1. Assegna un nome al pubblico e aggiungi una descrizione facoltativa.
   1. Trascina **[!UICONTROL Browser]** in Audience Builder.

      ![Rules (Regole) > Browser](assets/target_browser.png)

   1. Fai clic su **[!UICONTROL Seleziona]**, quindi scegli una delle seguenti opzioni:

      * **Tipo**: Includi o escludi gli utenti che usano un determinato browser. Consulta [Tipo](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_6ADC758F23F145B3A310151546D83D56).
      * **Lingua:** Includi o escludi alcuni browser impostati per una specifica lingua. Consulta [Lingua](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_7520D1AA464A45A6843EABE2D2B431A1).
      * **Versione:** includi o escludi una determinata versione del browser. Consulta [Versione](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_37CC8CE45DA04E8682AE6388321BA6EF).
   1. (Facoltativo) Imposta regole aggiuntive per il pubblico.
   1. Fai clic su **[!UICONTROL Fine]**.

   L’esempio seguente mostra un pubblico che include gli utenti di Microsoft Edge nelle versioni 91 o 92:

   ![Target Edge 91 o 92](assets/target_edge.png)

## Opzioni browser {#concept_221D8EEF53CC45AEACEB17CF336A3658}

Per un’attività, puoi includere o escludere i partecipanti in base al tipo, alla lingua o alla versione del browser utilizzato.

### Tipo {#section_6ADC758F23F145B3A310151546D83D56}

Includi o escludi gli utenti che usano un determinato browser.

Seleziona **[!UICONTROL Tipo]**, quindi scegli “è uguale a” o “è diverso da”.

* È uguale a: includi nell’attività i browser selezionati.
* È diverso da: escludi dall’attività i browser selezionati.

Seleziona uno o più browser. Le opzioni multiple sono collegate con l’operatore O.

### Lingua {#section_7520D1AA464A45A6843EABE2D2B431A1}

Includi o escludi alcuni browser impostati per una specifica lingua.

Ad esempio, se un’offerta è disponibile solo in inglese, puoi indirizzarla ai soli browser impostati per la lingua inglese. Oppure, se la pagina non è abilitata per caratteri a doppio byte, puoi escludere i browser impostati per lingue orientali.

L’inclusione o l’esclusione in base alla lingua del browser può permetterti di definire meglio i visitatori a cui ti rivolgi rispetto a parametri basati sulla località geografica nei casi in cui la lingua riveste un ruolo più importante della posizione geografica. Ad esempio, se offri un articolo scritto in inglese, puoi destinarlo ai paesi di lingua inglese oppure a chi utilizza browser impostati in lingua inglese. Con il targeting in base al browser, l’articolo sarà disponibile per gli anglofoni che si collegano da paesi in cui l’inglese non è la lingua principale.

Seleziona **[!UICONTROL Lingua]**, quindi scegli “è uguale a” o “è diverso da”.

* È uguale a: includi nell’attività i browser nelle lingue selezionate.
* È diverso da: escludi dall’attività i browser nelle lingue selezionate.

Seleziona una o più lingue. Le opzioni multiple sono collegate con l’operatore O.

È possibile includere o escludere le seguenti lingue del browser:

* Inglese
* Francese
* Tedesco
* Giapponese
* Coreano
* Portoghese
* Russo
* Spagnolo
* Cinese tradizionale

### Versione {#section_37CC8CE45DA04E8682AE6388321BA6EF}

Includi o escludi una determinata versione del browser.

Se, ad esempio, la pagina non può essere visualizzata correttamente in Internet Explorer versione 11 o precedente, puoi creare un pubblico escludendo tali versioni. In tal caso, è necessario impostare una regola in cui il tipo di browser è uguale a Internet Explorer e aggiungere una seconda regola in cui la versione è minore o uguale a 11.

Seleziona **[!UICONTROL Versione]**, quindi scegli un operatore:

* È uguale a
* È diverso da
* È maggiore di
* È maggiore o uguale a
* È minore di
* È minore o uguale a

Digita il numero della versione. In questo campo di testo è possibile immettere solo le versioni principali. La versione specificata include tutte le eventuali versioni secondarie di tale versione principale. Ad esempio, se specifichi la versione 10, sono inclusi anche i visitatori della versione 10.1.

Le opzioni multiple sono collegate con l’operatore O.

## Video di formazione: Creazione di tipi di pubblico ![Icona Tutorial](/help/main/assets/tutorial.png)

Questo video contiene informazioni sull&#39;utilizzo delle categorie di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392)
