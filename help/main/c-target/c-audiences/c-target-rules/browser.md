---
keywords: opzioni browser;tipo;tipo di browser;lingua del browser;lingua;versione;versione del browser
description: Scopri come creare tipi di pubblico in [!DNL Adobe Target] per eseguire il targeting degli utenti che utilizzano un browser specifico o opzioni di browser specifiche quando visitano la tua pagina.
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
>A partire da [!DNL Target] Standard/Premium 24.3.1 (4-6 marzo 2024), i tipi di pubblico incorporati creati utilizzando l&#39;interfaccia utente di Target, come `Browser:iPad` e `Browser:iPhone`, sono stati aggiornati per eseguire il targeting corretto per [!DNL iPad] e [!DNL iPhone] utilizzando `profile.mobile.deviceVendor`, `profile.mobile.isMobilePhone` e `profile.mobile.isTablet`.
>
>Questo aggiornamento non richiede alcuna azione da parte dei clienti. Le etichette nell&#39;interfaccia utente di [!DNL Target] verranno modificate in futuro e saranno annunciate nelle [[!DNL Target] note sulla versione (corrente)](/help/main/r-release-notes/release-notes.md) quando verranno apportate queste modifiche.
>
>Per le impostazioni della soluzione alternativa, vedere [Aggiornamenti per [!DNL iPad] e [!DNL iPhone] negli attributi del pubblico [!UICONTROL Browser] (30 aprile 2024)](#updates) di seguito.

Esistono due modi per indirizzare i browser:

* **Pubblico predefinito:** il pubblico predefinito è utile se desideri indirizzare un’attività solo ai visitatori che utilizzano un browser specifico per visitare il tuo sito. Ad esempio, se offri un&#39;estensione [!DNL Chrome], esegui il targeting solo per [!DNL Chrome] utenti.

   1. Durante la configurazione dell’attività, seleziona il browser dall’elenco a discesa.

      Questa opzione indirizza l’attività solo ai visitatori che utilizzano il browser specificato.

      ![Utenti Chrome di destinazione](/help/main/c-target/c-audiences/c-target-rules/assets/target-chrome.png)

* **Regola di pubblico personalizzato per browser:** un pubblico personalizzato consente di rivolgerti a più browser o di impostare regole o esclusioni per specifici browser, versioni o lingue del browser. Questa funzionalità offre una flessibilità significativa quando esegui il targeting di un’attività in base agli attributi del browser.

   1. Nell&#39;interfaccia [!DNL Target], fare clic su **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
   1. Assegna un nome al pubblico e aggiungi una descrizione facoltativa.
   1. Trascina **[!UICONTROL Browser]** nel generatore di pubblico.

      ![Regole > Browser](assets/target_browser.png)

   1. Fare clic su **[!UICONTROL Select]**, quindi selezionare una delle opzioni seguenti:

      * **Tipo**: Includi o escludi gli utenti che usano un determinato browser. Consulta [Tipo](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_6ADC758F23F145B3A310151546D83D56).
      * **Lingua:** Includi o escludi alcuni browser impostati per l&#39;utilizzo di lingue specifiche. Consulta [Lingua](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_7520D1AA464A45A6843EABE2D2B431A1).
      * **Versione:** includi o escludi una determinata versione del browser. Consulta [Versione](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_37CC8CE45DA04E8682AE6388321BA6EF).

   1. (Facoltativo) Imposta regole aggiuntive per il pubblico.
   1. Fare clic su **[!UICONTROL Done]**.

  L&#39;esempio seguente mostra un pubblico che include [!DNL Microsoft Edge] utenti nelle versioni 91 o 92:

  ![Edge 91 o 92](assets/target_edge.png) di destinazione

## Opzioni browser {#concept_221D8EEF53CC45AEACEB17CF336A3658}

Per un’attività, puoi includere o escludere i partecipanti in base al tipo, alla lingua o alla versione del browser utilizzato.

### Tipo {#section_6ADC758F23F145B3A310151546D83D56}

Includi o escludi gli utenti che usano un determinato browser.

Seleziona **[!UICONTROL Type]**, quindi scegli &quot;è uguale a&quot; o &quot;è diverso da&quot;.

* [!UICONTROL Equals]: esegui il targeting dei browser selezionati.
* [!UICONTROL Does not equal]: escludere i browser selezionati.

Seleziona uno o più browser. Le opzioni multiple sono collegate con l’operatore O.

### Lingua {#section_7520D1AA464A45A6843EABE2D2B431A1}

Includi o escludi alcuni browser impostati per una specifica lingua.

Ad esempio, se un’offerta è disponibile solo in inglese, puoi indirizzarla ai soli browser impostati per la lingua inglese. Oppure, se la pagina non è abilitata per caratteri a doppio byte, puoi escludere i browser impostati per lingue orientali.

L’inclusione o l’esclusione in base alla lingua del browser può permetterti di definire meglio i visitatori a cui ti rivolgi rispetto a parametri basati sulla località geografica nei casi in cui la lingua riveste un ruolo più importante della posizione geografica. Ad esempio, se offri un articolo scritto in inglese, puoi destinarlo ai paesi di lingua inglese oppure a chi utilizza browser impostati in lingua inglese. Con il targeting in base al browser, l’articolo sarà disponibile per gli anglofoni che si collegano da paesi in cui l’inglese non è la lingua principale.

Seleziona **[!UICONTROL Language]**, quindi scegli &quot;è uguale a&quot; o &quot;è diverso da&quot;.

* [!UICONTROL Equals]: Eseguire il targeting delle lingue del browser selezionate.
* [!UICONTROL Does not equal]: Escludi le lingue del browser selezionate.

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

Ad esempio, se la pagina non viene visualizzata correttamente in [!DNL Internet Explorer] versione 11 o precedente, è possibile creare un pubblico che escluda tali versioni. In tal caso, puoi impostare una regola in cui il tipo di browser è uguale a [!DNL Internet Explorer] e aggiungere una seconda regola in cui la versione è minore o uguale a 11.

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

## Aggiornamenti per [!DNL iPad] e [!DNL iPhone] negli attributi del pubblico [!UICONTROL Browser] (30 aprile 2024) {#updates}

[!DNL Adobe Target] consente di [eseguire il targeting per uno qualsiasi degli attributi di categoria](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), inclusi gli utenti che utilizzano un browser o opzioni di browser specifiche quando visitano la pagina.

A partire da [!DNL Target] Standard/Premium 24.3.1 (4-6 marzo 2024), i tipi di pubblico incorporati creati utilizzando l&#39;interfaccia utente di Target, come `Browser:iPad` e `Browser:iPhone`, sono stati aggiornati per eseguire il targeting corretto per [!DNL iPad] e [!DNL iPhone] utilizzando `profile.mobile.deviceVendor`, `profile.mobile.isMobilePhone` e `profile.mobile.isTablet`.

I tipi di pubblico incorporati creati utilizzando l&#39;interfaccia utente [!DNL Target], ad esempio `Browser:iPad` e `Browser:iPhone`, verranno automaticamente spostati nella nuova definizione di pubblico e non richiedono alcuna azione da parte dei clienti. In futuro, tuttavia, sarà necessario utilizzare le impostazioni [descritte di seguito](#ui).

Se utilizzi `user.browserType` in uno degli script di profilo per verificare se si tratta di [!DNL iPhone] o [!DNL iPad] (ad esempio, `user.browserType == 'iphone'` o `user.browserType != 'ipad'`), questi script di profilo devono essere modificati come [indicato di seguito](#profile-scripts) prima del 30 aprile 2024 per garantire che questi tipi di pubblico continuino a funzionare come previsto.

I tipi di pubblico di JavaScript sono tipi di pubblico legacy che utilizzano espressioni [!DNL Target] che sono state dichiarate obsolete con l&#39;interfaccia utente [!DNL Target Classic]. Questi tipi di pubblico possono essere modificati solo tramite API. I clienti devono aggiornare questi tipi di pubblico solo se continuano a utilizzare i tipi di pubblico precedenti nelle attività.

### Tipi di pubblico creati tramite l&#39;interfaccia utente [!DNL Target] {#ui}

In futuro sarà possibile utilizzare le seguenti impostazioni:

* **Per le corrispondenze del browser[!DNL Apple]**: [!UICONTROL Mobile] > [!UICONTROL Device Vendor] [!UICONTROL matches] [!DNL Apple]

  ![Apple](/help/main/r-release-notes/assets/apple.png)

* **Per le corrispondenze del browser con il tablet**: [!UICONTROL Mobile] > [!UICONTROL is Tablet] > [!UICONTROL true]

  ![Il dispositivo mobile è un tablet](/help/main/r-release-notes/assets/is-tablet.png)

* **Per le corrispondenze del browser con iPad**: [!UICONTROL Mobile] > [!UICONTROL Device Marketing Name] [!UICONTROL matches] [!DNL iPad] con un contenitore And con [!UICONTROL Mobile] > [!UICONTROL Is Tablet] è [!DNL true]

  ![iPad](/help/main/r-release-notes/assets/ipad.png)

* **Per le corrispondenze del browser con iPhone**: [!UICONTROL Mobile] > [!UICONTROL Device Marketing Name] [!UICONTROL matches] [!DNL iPhone] con un contenitore And con [!UICONTROL Mobile] > [!UICONTROL Is Mobile Phone] è [!DNL true]

  ![iPhone](/help/main/r-release-notes/assets/iphone.png)

È possibile utilizzare molte altre impostazioni, ad esempio quando le condizioni vengono negate. Di seguito sono riportati alcuni esempi di condizioni negate:

* **Per il browser non corrisponde ad iPhone**: [!UICONTROL Mobile] > [!UICONTROL Device Vendor] [!UICONTROL does not match] [!UICONTROL Apple] con un contenitore Or con [!UICONTROL Mobile] > [!UICONTROL Is Mobile Phone] è [!UICONTROL false]

  ![Non telefono cellulare](/help/main/r-release-notes/assets/mobile-phone-false.png)

* **Per il browser non corrisponde ad iPad**: [!UICONTROL Mobile] > [!UICONTROL Device Vendor] [!UICONTROL does not match] [!UICONTROL Apple] con un contenitore Or con [!UICONTROL Mobile] > [!UICONTROL Is Tablet] è [!UICONTROL false].

  ![Non tablet](/help/main/r-release-notes/assets/tablet-false.png)

### Tipi di pubblico creati mediante script di profilo {#profile-scripts}

Se utilizzi `user.browserType` nei tipi di pubblico legacy [!DNL Target Classic] o negli script di profilo, le modifiche devono includere quanto segue:

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