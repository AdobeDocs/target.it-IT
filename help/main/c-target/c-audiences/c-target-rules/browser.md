---
keywords: opzioni browser;tipo;tipo di browser;lingua del browser;lingua;versione;versione del browser
description: Scopri come creare tipi di pubblico in [!DNL Adobe Target] per eseguire il targeting degli utenti che visitano la pagina utilizzando un browser specifico o opzioni specifiche del browser.
title: Posso indirizzare i visitatori in base al tipo di browser?
feature: Audiences
exl-id: 8420bbe3-b58a-4ddb-89bb-0265dab6b5fc
source-git-commit: 784f41a73941877135a5902f2331972ba9d0e880
workflow-type: tm+mt
source-wordcount: '1015'
ht-degree: 33%

---

# [!UICONTROL Browser]

Puoi indirizzare l’attività agli utenti che visitano la pagina utilizzando un browser specifico o opzioni specifiche del browser.

È possibile indirizza l’attività ai seguenti browser:

* [!UICONTROL Chrome]
* [!UICONTROL Firefox]
* [!UICONTROL Safari]
* [!UICONTROL Internet Explorer]
* [!UICONTROL Microsoft Edge]
* [!UICONTROL Opera]
* [!DNL iPad]
* [!DNL iPhone]

>[!IMPORTANT]
>
>A partire da [!DNL Target] Standard/Premium 24.3.1 (4-6 marzo 2024), tipi di pubblico incorporati creati utilizzando l’interfaccia utente di Target, ad esempio `Browser:iPad` e `Browser:iPhone` sono stati aggiornati per eseguire il targeting corretto per [!DNL iPad] e [!DNL iPhone] utilizzo `profile.mobile.deviceVendor`, `profile.mobile.isMobilePhone`, e `profile.mobile.isTablet`.
>
>Questo aggiornamento non richiede alcuna azione da parte dei clienti. Le etichette in [!DNL Target] L’interfaccia utente verrà modificata in futuro e verrà annunciata in [[!DNL Target] note sulla versione (corrente)](/help/main/r-release-notes/release-notes.md) quando vengono apportate queste modifiche.
>
>Per le impostazioni della soluzione alternativa, consulta [Aggiornamenti per [!DNL iPad] e [!DNL iPhone] in [!UICONTROL Browser] attributi del pubblico (30 aprile 2024)](#updates) di seguito.

Esistono due modi per indirizzare i browser:

* **Pubblico predefinito:** il pubblico predefinito è utile se desideri indirizzare un’attività solo ai visitatori che utilizzano un browser specifico per visitare il tuo sito. Ad esempio, se offri un [!DNL Chrome] estensione, esegui solo il targeting [!DNL Chrome] utenti.

   1. Durante la configurazione dell’attività, seleziona il browser dall’elenco a discesa.

      Questa opzione indirizza l’attività solo ai visitatori che utilizzano il browser specificato.

      ![Utenti di Target Chrome](/help/main/c-target/c-audiences/c-target-rules/assets/target-chrome.png)

* **Regola pubblico browser personalizzato:** Un pubblico personalizzato consente di rivolgerti a più browser o di impostare regole o esclusioni per specifici browser, versioni o lingue del browser. Questa funzionalità offre una flessibilità significativa quando esegui il targeting di un’attività in base agli attributi del browser.

   1. In [!DNL Target] , fare clic su **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
   1. Assegna un nome al pubblico e aggiungi una descrizione facoltativa.
   1. Trascina **[!UICONTROL Browser]** in Audience Builder.

      ![Rules (Regole) > Browser](assets/target_browser.png)

   1. Clic **[!UICONTROL Select]**, quindi seleziona una delle seguenti opzioni:

      * **Tipo**: Includi o escludi gli utenti che usano un determinato browser. Consulta [Tipo](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_6ADC758F23F145B3A310151546D83D56).
      * **Lingua:** Includi o escludi alcuni browser impostati per una specifica lingua. Consulta [Lingua](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_7520D1AA464A45A6843EABE2D2B431A1).
      * **Versione:** includi o escludi una determinata versione del browser. Consulta [Versione](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_37CC8CE45DA04E8682AE6388321BA6EF).

   1. (Facoltativo) Imposta regole aggiuntive per il pubblico.
   1. Clic **[!UICONTROL Done]**.

  L’esempio seguente mostra un pubblico che include [!DNL Microsoft Edge] utenti nelle versioni 91 o 92:

  ![Target Edge 91 o 92](assets/target_edge.png)

## Opzioni browser {#concept_221D8EEF53CC45AEACEB17CF336A3658}

Per un’attività, puoi includere o escludere i partecipanti in base al tipo, alla lingua o alla versione del browser utilizzato.

### Tipo {#section_6ADC758F23F145B3A310151546D83D56}

Includi o escludi gli utenti che usano un determinato browser.

Seleziona **[!UICONTROL Type]**, quindi scegliere è uguale a o non è uguale a.

* [!UICONTROL Equals]: esegui il targeting dei browser selezionati.
* [!UICONTROL Does not equal]: escludi i browser selezionati.

Seleziona uno o più browser. Le opzioni multiple sono collegate con l’operatore O.

### Lingua {#section_7520D1AA464A45A6843EABE2D2B431A1}

Includi o escludi alcuni browser impostati per una specifica lingua.

Ad esempio, se un’offerta è disponibile solo in inglese, puoi indirizzarla ai soli browser impostati per la lingua inglese. Oppure, se la pagina non è abilitata per caratteri a doppio byte, puoi escludere i browser impostati per lingue orientali.

L’inclusione o l’esclusione in base alla lingua del browser può permetterti di definire meglio i visitatori a cui ti rivolgi rispetto a parametri basati sulla località geografica nei casi in cui la lingua riveste un ruolo più importante della posizione geografica. Ad esempio, se offri un articolo scritto in inglese, puoi destinarlo ai paesi di lingua inglese oppure a chi utilizza browser impostati in lingua inglese. Con il targeting in base al browser, l’articolo sarà disponibile per gli anglofoni che si collegano da paesi in cui l’inglese non è la lingua principale.

Seleziona **[!UICONTROL Language]**, quindi scegliere è uguale a o non è uguale a.

* [!UICONTROL Equals]: esegui il targeting delle lingue del browser selezionate.
* [!UICONTROL Does not equal]: esclude le lingue del browser selezionate.

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

Ad esempio, se la pagina non viene visualizzata correttamente in [!DNL Internet Explorer] versione 11 o precedente, puoi creare un pubblico che escluda tali versioni. In tal caso, imposta una regola in cui il tipo di browser è uguale a [!DNL Internet Explorer] e aggiungi una seconda regola in cui la versione è minore o uguale a 11.

Seleziona **[!UICONTROL Version]**, quindi scegli un operatore:

* [!UICONTROL Equals]
* [!UICONTROL Does not equal]
* [!UICONTROL Is greater than]
* È maggiore o uguale a
* [!UICONTROL Is less than]
* [!UICONTROL Is less than or equal to]

Digita il numero di versione. In questo campo di testo è possibile immettere solo le versioni principali. La versione specificata include tutte le eventuali versioni secondarie di tale versione principale. Ad esempio, se specifichi la versione 10, sono inclusi anche i visitatori della versione 10.1.

Le opzioni multiple sono collegate con l’operatore O.

## Video di formazione: Creazione di tipi di pubblico ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video contiene informazioni sull&#39;utilizzo delle categorie di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392)

## Aggiornamenti per [!DNL iPad] e [!DNL iPhone] in [!UICONTROL Browser] attributi del pubblico (30 aprile 2024) {#updates}

[!DNL Adobe Target] consente di: [esegui il targeting su uno qualsiasi dei vari attributi di categoria](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), inclusi gli utenti che visitano la pagina utilizzando un browser o opzioni di browser specifiche.

A partire da [!DNL Target] Standard/Premium 24.3.1 (4-6 marzo 2024), tipi di pubblico incorporati creati utilizzando l’interfaccia utente di Target, ad esempio `Browser:iPad` e `Browser:iPhone` sono stati aggiornati per eseguire il targeting corretto per [!DNL iPad] e [!DNL iPhone] utilizzo `profile.mobile.deviceVendor`, `profile.mobile.isMobilePhone` e `profile.mobile.isTablet`.

Tipi di pubblico incorporati creati utilizzando [!DNL Target] Interfaccia utente, ad esempio `Browser:iPad` e `Browser:iPhone`, verrà automaticamente spostato nella nuova definizione di pubblico e non richiede alcuna azione da parte dei clienti. Tuttavia, andando avanti, è necessario utilizzare le impostazioni [descritto di seguito](#ui).

Se usa `user.browserType` in qualsiasi script di profilo per verificare se è un [!DNL iPhone] o [!DNL iPad] (ad esempio, `user.browserType == 'iphone'` o `user.browserType != 'ipad'`), questi script di profilo devono essere modificati come [istruzioni di seguito](#profile-scripts) entro il 30 aprile 2024 per garantire che tali tipi di pubblico continuino a funzionare come previsto.

I tipi di pubblico JavaScript sono tipi di pubblico legacy che utilizzano [!DNL Target] espressioni dichiarate obsolete con il [!DNL Target Classic] UI. Questi tipi di pubblico possono essere modificati solo tramite API. I clienti devono aggiornare questi tipi di pubblico solo se continuano a utilizzare i tipi di pubblico precedenti nelle attività.

### Tipi di pubblico creati utilizzando [!DNL Target] UI {#ui}

In futuro sarà possibile utilizzare le seguenti impostazioni:

* **Per corrispondenze browser[!DNL Apple]**: [!UICONTROL Mobile] > [!UICONTROL Device Vendor] [!UICONTROL matches] [!DNL Apple]

  ![Apple](/help/main/r-release-notes/assets/apple.png)

* **Per il browser corrisponde al tablet**: [!UICONTROL Mobile] > [!UICONTROL is Tablet] > [!UICONTROL true]

  ![Il dispositivo mobile è un tablet](/help/main/r-release-notes/assets/is-tablet.png)

* **Per il browser corrisponde a iPad**: [!UICONTROL Mobile] > [!UICONTROL Device Marketing Name] [!UICONTROL matches] [!DNL iPad] con un contenitore And con [!UICONTROL Mobile] > [!UICONTROL Is Tablet] è [!DNL true]

  ![iPad](/help/main/r-release-notes/assets/ipad.png)

* **Per il browser corrisponde a iPhone**: [!UICONTROL Mobile] > [!UICONTROL Device Marketing Name] [!UICONTROL matches] [!DNL iPhone] con un contenitore And con [!UICONTROL Mobile] > [!UICONTROL Is Mobile Phone] è [!DNL true]

  ![iPhone](/help/main/r-release-notes/assets/iphone.png)

È possibile utilizzare molte altre impostazioni, ad esempio quando le condizioni vengono negate. Di seguito sono riportati alcuni esempi di condizioni negate:

* **Per il browser non corrisponde a iPhone**: [!UICONTROL Mobile] > [!UICONTROL Device Vendor] [!UICONTROL does not match] [!UICONTROL Apple] con un contenitore O con [!UICONTROL Mobile] > [!UICONTROL Is Mobile Phone] è [!UICONTROL false]

  ![Non telefono cellulare](/help/main/r-release-notes/assets/mobile-phone-false.png)

* **Per il browser non corrisponde a iPad**: [!UICONTROL Mobile] > [!UICONTROL Device Vendor] [!UICONTROL does not match] [!UICONTROL Apple] con un contenitore O con [!UICONTROL Mobile] > [!UICONTROL Is Tablet] è [!UICONTROL false].

  ![Non tablet](/help/main/r-release-notes/assets/tablet-false.png)

### Tipi di pubblico creati mediante script di profilo {#profile-scripts}

Se usa `user.browserType` in legacy [!DNL Target Classic] tipi di pubblico o negli script di profilo, le modifiche devono includere quanto segue:

* **BrowserType è iPhone**:

  Sostituisci:

  `user.browserType=="iphone"`

  Con:

  `profile.mobile.deviceVendor == "Apple" && profile.mobile.isMobilePhone`

* **BrowserType non è iPhone**:

  Sostituisci:

  `user.browserType!="iphone"`

  Con:

  `profile.mobile.deviceVendor != "Apple" || !profile.mobile.isMobilePhone`

* **BrowserType è iPad**:

  Sostituisci:

  `user.browserType=="ipad"`

  Con:

  `profile.mobile.deviceVendor == "Apple" && profile.mobile.isTablet`

* **BrowserType non è iPad**:

  Sostituisci:

  `user.browserType!="ipad"`

  Con:

  `profile.mobile.deviceVendor != "Apple" || !profile.mobile.isTablet`