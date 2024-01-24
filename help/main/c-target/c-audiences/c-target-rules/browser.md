---
keywords: opzioni browser;tipo;tipo di browser;lingua del browser;lingua;versione;versione del browser
description: Scopri come creare tipi di pubblico in [!DNL Adobe Target] per eseguire il targeting degli utenti che visitano la pagina utilizzando un browser specifico o opzioni specifiche del browser.
title: Posso indirizzare i visitatori in base al tipo di browser?
feature: Audiences
exl-id: 8420bbe3-b58a-4ddb-89bb-0265dab6b5fc
source-git-commit: 968f9982299156d3f4d599d00322106fe3629610
workflow-type: tm+mt
source-wordcount: '1057'
ht-degree: 36%

---

# Browser

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
>A partire dal 30 aprile 2024, [!DNL iPad] e [!DNL iPhone] verrà rimosso dal [!UICONTROL Browser] digita l’elenco a discesa durante la creazione di categorie per i tipi di pubblico. Per le impostazioni della soluzione alternativa, consulta [Obsolescenza di iPad e iPhone dall’attributo di pubblico del browser (30 aprile 2024)](#deprecation) di seguito.

Esistono due modi per indirizzare i browser:

* **Pubblico predefinito:** il pubblico predefinito è utile se desideri indirizzare un’attività solo ai visitatori che utilizzano un browser specifico per visitare il tuo sito. Ad esempio, se offri un [!DNL Chrome] estensione, esegui solo il targeting [!DNL Chrome] utenti.

   1. Durante la configurazione dell’attività, seleziona il browser dall’elenco a discesa.

      Questa opzione indirizza l’attività solo ai visitatori che utilizzano il browser specificato.

      ![Utenti di Target Chrome](/help/main/c-target/c-audiences/c-target-rules/assets/target-chrome.png)

* **Regola pubblico browser personalizzato:** Un pubblico personalizzato consente di rivolgerti a più browser o di impostare regole o esclusioni per specifici browser, versioni o lingue del browser. Questa funzionalità offre una flessibilità significativa quando esegui il targeting di un’attività in base agli attributi del browser.

   1. In [!DNL Target] , fare clic su **[!UICONTROL Tipi di pubblico]** > **[!UICONTROL Crea pubblico]**.
   1. Assegna un nome al pubblico e aggiungi una descrizione facoltativa.
   1. Trascina **[!UICONTROL Browser]** in Audience Builder.

      ![Rules (Regole) > Browser](assets/target_browser.png)

   1. Fai clic su **[!UICONTROL Seleziona]**, quindi scegli una delle seguenti opzioni:

      * **Tipo**: Includi o escludi gli utenti che usano un determinato browser. Consulta [Tipo](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_6ADC758F23F145B3A310151546D83D56).
      * **Lingua:** Includi o escludi alcuni browser impostati per una specifica lingua. Consulta [Lingua](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_7520D1AA464A45A6843EABE2D2B431A1).
      * **Versione:** includi o escludi una determinata versione del browser. Consulta [Versione](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_37CC8CE45DA04E8682AE6388321BA6EF).

   1. (Facoltativo) Imposta regole aggiuntive per il pubblico.
   1. Fai clic su **[!UICONTROL Fine]**.

  L’esempio seguente mostra un pubblico che include [!DNL Microsoft Edge] utenti nelle versioni 91 o 92:

  ![Target Edge 91 o 92](assets/target_edge.png)

## Opzioni browser {#concept_221D8EEF53CC45AEACEB17CF336A3658}

Per un’attività, puoi includere o escludere i partecipanti in base al tipo, alla lingua o alla versione del browser utilizzato.

### Tipo {#section_6ADC758F23F145B3A310151546D83D56}

Includi o escludi gli utenti che usano un determinato browser.

Seleziona **[!UICONTROL Tipo]**, poi scegli “è uguale a” o “è diverso da”.

* [!UICONTROL Uguale a]: esegui il targeting dei browser selezionati.
* [!UICONTROL Non è uguale a]: escludi i browser selezionati.

Seleziona uno o più browser. Le opzioni multiple sono collegate con l’operatore O.

### Lingua {#section_7520D1AA464A45A6843EABE2D2B431A1}

Includi o escludi alcuni browser impostati per una specifica lingua.

Ad esempio, se un’offerta è disponibile solo in inglese, puoi indirizzarla ai soli browser impostati per la lingua inglese. Oppure, se la pagina non è abilitata per caratteri a doppio byte, puoi escludere i browser impostati per lingue orientali.

L’inclusione o l’esclusione in base alla lingua del browser può permetterti di definire meglio i visitatori a cui ti rivolgi rispetto a parametri basati sulla località geografica nei casi in cui la lingua riveste un ruolo più importante della posizione geografica. Ad esempio, se offri un articolo scritto in inglese, puoi destinarlo ai paesi di lingua inglese oppure a chi utilizza browser impostati in lingua inglese. Con il targeting in base al browser, l’articolo sarà disponibile per gli anglofoni che si collegano da paesi in cui l’inglese non è la lingua principale.

Seleziona **[!UICONTROL Lingua]**, quindi scegli “è uguale a” o “è diverso da”.

* [!UICONTROL Uguale a]: esegui il targeting delle lingue del browser selezionate.
* [!UICONTROL Non è uguale a]: esclude le lingue del browser selezionate.

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

Seleziona **[!UICONTROL Versione]**, quindi scegli un operatore:

* [!UICONTROL Uguale a]
* [!UICONTROL Non è uguale a]
* [!UICONTROL È maggiore di]
* È maggiore o uguale a
* [!UICONTROL È minore di]
* [!UICONTROL È minore di o uguale a]

Digita il numero di versione. In questo campo di testo è possibile immettere solo le versioni principali. La versione specificata include tutte le eventuali versioni secondarie di tale versione principale. Ad esempio, se specifichi la versione 10, sono inclusi anche i visitatori della versione 10.1.

Le opzioni multiple sono collegate con l’operatore O.

## Video di formazione: Creazione di tipi di pubblico ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video contiene informazioni sull&#39;utilizzo delle categorie di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392)

## Rimozione di iPad e iPhone dall’attributo di pubblico del browser (30 aprile 2024) {#deprecation}

[!DNL Adobe Target] consente di: [esegui il targeting su uno qualsiasi dei vari attributi di categoria](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), inclusi gli utenti che visitano la pagina utilizzando un browser o opzioni di browser specifiche.

A partire dal 30 aprile 2024, iPad e iPhone verranno rimossi dal [!UICONTROL Browser] digita l’elenco a discesa durante la creazione di categorie per i tipi di pubblico.

I tipi di pubblico incorporati, come &quot;Browser: iPad&quot; e &quot;Browser: iPhone&quot;, verranno automaticamente spostati nella nuova definizione di pubblico. Tutti gli script di profilo che utilizzano &quot;user.browserType&quot; *non* essere aggiornato automaticamente: se non li aggiorni manualmente, la qualificazione dell’utente potrebbe non avvenire come previsto.

Se hai tipi di pubblico che eseguono il targeting di iPad o iPhone utilizzando [!UICONTROL Browser] , è necessario modificare queste impostazioni prima del 30 aprile 2024 per garantire che tali tipi di pubblico continuino a funzionare come previsto.

### Tipi di pubblico creati utilizzando [!DNL Target] UI

In futuro sarà possibile utilizzare le seguenti impostazioni:

* **Per corrispondenze browser[!DNL Apple]**: [!UICONTROL Dispositivi mobili] > [!UICONTROL Fornitore dispositivo] [!UICONTROL corrisponde a] [!DNL Apple]

  ![Apple](/help/main/r-release-notes/assets/apple.png)

* **Per il browser corrisponde al tablet**: [!UICONTROL Dispositivi mobili] > [!UICONTROL è un tablet] > [!UICONTROL true]

  ![Il dispositivo mobile è un tablet](/help/main/r-release-notes/assets/is-tablet.png)

* **Per il browser corrisponde a iPad**: [!UICONTROL Dispositivi mobili] > [!UICONTROL Nome marketing del dispositivo] [!UICONTROL corrisponde a] [!DNL iPad] con un contenitore And con [!UICONTROL Dispositivi mobili] > [!UICONTROL È un tablet] è [!DNL true]

  ![iPad](/help/main/r-release-notes/assets/ipad.png)

* **Per il browser corrisponde a iPhone**: [!UICONTROL Dispositivi mobili] > [!UICONTROL Nome marketing del dispositivo] [!UICONTROL corrisponde a] [!DNL iPhone] con un contenitore And con [!UICONTROL Dispositivi mobili] > [!UICONTROL È un telefono cellulare] è [!DNL true]

  ![iPhone](/help/main/r-release-notes/assets/iphone.png)

È possibile utilizzare molte altre impostazioni, ad esempio quando le condizioni vengono negate. Di seguito sono riportati alcuni esempi di condizioni negate:

* **Per il browser non corrisponde a iPhone**: [!UICONTROL Dispositivi mobili] > [!UICONTROL Fornitore dispositivo] [!UICONTROL non corrisponde a] [!UICONTROL Apple] con un contenitore O con [!UICONTROL Dispositivi mobili] > [!UICONTROL È un telefono cellulare] è [!UICONTROL false]

  ![Non telefono cellulare](/help/main/r-release-notes/assets/mobile-phone-false.png)

* **Per il browser non corrisponde a iPad**: [!UICONTROL Dispositivi mobili] > [!UICONTROL Fornitore dispositivo] [!UICONTROL non corrisponde a] [!UICONTROL Apple] con un contenitore O con [!UICONTROL Dispositivi mobili] > [!UICONTROL È un tablet] è [!UICONTROL false].

  ![Non tablet](/help/main/r-release-notes/assets/tablet-false.png)

### Tipi di pubblico creati mediante script di profilo

Se usa `user.browserType` nei tipi di pubblico che utilizzano gli script di profilo, come spiegato in [Glossario di profili e variabili](/help/main/c-target/c-visitor-profile/variables-profiles-parameters-methods.md), le modifiche devono includere quanto segue:

>[!NOTE]
>
>I seguenti profili sono pianificati per essere rilasciati nei prossimi giorni, a partire dal 24 gennaio 2024. Il [note sulla versione corrente](/help/main/r-release-notes/release-notes.md) verranno aggiornati quando questi profili saranno disponibili.
>
>Questi profili consentono le seguenti modifiche:
>
>* `profile.mobile.isTablet`
>
>* `profile.mobile.isMobilePhone`

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