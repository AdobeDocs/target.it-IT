---
keywords: Targeting;compositore esperienza visivo;vec;risoluzione dei problemi compositore esperienza visivo;risoluzione dei problemi;tls;tls 1.2
description: Scopri come risolvere i problemi in [!UICONTROL Visual Experience Composer] (VEC).
title: Come posso risolvere i problemi relativi a [!UICONTROL Visual Experience Composer]?
feature: Visual Experience Composer (VEC)
exl-id: ca251025-25e8-4e56-9b59-81310fc763c1
source-git-commit: 7c0d0154b81fbd3f89a82b31cd18541a7f0ea1a7
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 23%

---

# Risoluzione dei problemi relativi al [!UICONTROL Visual Experience Composer]

Talvolta si verificano problemi di visualizzazione in [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) in determinate condizioni.

## Quando apro il sito Web in [!UICONTROL Visual Experience Composer], il [!DNL Target] le librerie non vengono caricate. (Solo Compositore esperienza visivo)  {#section_8A7D3F4AD2CC4C3B823EE9432B97E06F}

[!DNL Target] aggiunge due parametri (`mboxEdit=1` e `mboxDisable=1`) durante l&#39;apertura del sito Web in [!UICONTROL Visual Experience Composer].

Se il tuo sito web (in particolare le app a pagina singola) taglia i parametri o li rimuove mentre navighi da una pagina all&#39;altra (senza ricaricare la pagina) il [!DNL Target] interruzioni di funzionalità e [!DNL Target] le librerie non vengono caricate.

Per evitare questo problema, assicurati di non tagliare o rimuovere questi due parametri.

## La pagina non si apre nel Compositore esperienza avanzato, o si carica lentamente. Le attività o le esperienze si caricano lentamente nel Compositore esperienza visivo. (Solo Compositore esperienza visivo)  {#section_71E7601BE9894E3DA3A7FBBB72B6B0C1}

Diversi problemi possono influire sulle prestazioni della pagina in [!UICONTROL Target] compositori di esperienze. Alcuni problemi comuni includono:

* Sulla pagina non è oresente una mbox.
* Il sito utilizza il blocco proxy, che non consente l&#39;apertura della pagina in nessuno dei Compositori esperienza.
* Il sito non si lascia aprire in un iFrame.

Se si verificano problemi in [!UICONTROL Enhanced Experience Composer], provare a disattivare [!UICONTROL Enhanced Experience Composer] e utilizza [!UICONTROL Visual Experience Composer] invece.

Per disattivare [!UICONTROL Enhanced Experience Composer], vai a **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** e spegnere il **[!UICONTROL Enable Enhanced Experience Composer]** opzione.

Alcuni utenti visualizzano il seguente messaggio di errore nella console:

![Messaggio di errore della console](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/console_error_message.jpg)

Se nessuno dei due [!UICONTROL Visual Experience Composer] né il [!UICONTROL Enhanced Experience Composer] funziona, utilizza un’estensione del browser come [!DNL Requestly] ([!DNL Chrome] o [!DNL Firefox]) o Modifica le intestazioni di risposta (Firefox) che possono sovrascrivere le opzioni di intestazione X-Frames per il sito e consentirne il caricamento in iFrame, abilitando il Compositore esperienza visivo. Se non riesci a utilizzare le estensioni del browser, utilizza [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

>[!NOTE]
>
>Oltre alle seguenti informazioni, puoi utilizzare [[!DNL Adobe Target] [!UICONTROL Visual Editing Helper] estensione](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) per [!DNL Google Chrome].


>[!NOTE]
>
>Questi plug-in devono essere utilizzati solo nel contesto di modifica del Compositore esperienza visivo.
>
>Per [!DNL Requestly] estensione, ogni volta che è necessario rimuovere le intestazioni, effettua una delle seguenti operazioni:
>
>* Aggiungere regole URL per l&#39;URL che si desidera aprire nel Compositore esperienza visivo in modo tale che le intestazioni vengano rimosse solo per tali URL.
>
>* Abilitare la regola quando si effettuano modifiche nel Compositore esperienza visivo e disabilitarla quando non lo si utilizza.
>
>Per [!UICONTROL Modify Response Header] estensione ([!DNL Firefox]), poiché non è possibile aggiungere una regola URL, è necessario effettuare le seguenti operazioni:
>
>* Abilitare la regola quando si effettuano modifiche nel Compositore esperienza visivo e disabilitarla quando non lo si utilizza.

**Per utilizzare [!DNL Requestly] estensione su [!DNL Chrome] o [!DNL Firefox]:**

1. Disattiva il [!UICONTROL Enhanced Experienced Composer].
1. Installare [!DNL Requestly] estensione browser su [!DNL Chrome] o [!DNL Firefox].
1. Apri l&#39;estensione e configurala:
1. Seleziona **[!UICONTROL Modify headers]**.
1. Immetti quanto segue:

   * Nome regola
   * Regole di modifica

      * Attiva/Disattiva **[!UICONTROL Add]** a **[!UICONTROL Remove]**.
      * Attiva/Disattiva **[!UICONTROL Request]** a **[!UICONTROL Response]**.
      * Immetti “X-Frame-Options” come nome dell&#39;intestazione.
      * Ripeti i passaggi precedenti e immetti “x-frame-options” come nome dell&#39;intestazione.

        >[!NOTE]
        >
        >Intestazioni manipolate tramite [!DNL Requestly] sono sensibili all’uso di maiuscole e minuscole.

      * Cambia **[!UICONTROL Equals]** a **[!UICONTROL Contains]** come condizione per l’URL di origine e immetti l’URL dell’attività da caricare nel Compositore esperienza visivo.

     ![immagine chrome_extension](assets/chrome_extension.png)

1. Clic **[!UICONTROL Save]**.

   ![richiedi immagine](assets/requestly.png)

   Ora dovresti essere in grado di caricare la pagina rapidamente con [!UICONTROL Visual Experience Composer].

**Per utilizzare [!DNL Modify Response Headers] estensione su [!UICONTROL Firefox]:**

1. Installare [!UICONTROL Modify Response Headers] il [!DNL Firefox] e riavvia il browser.
1. Dal tuo [!DNL Firefox] , seleziona l&#39;estensione Modify Response Headers.
1. Clic **[!UICONTROL Preferences]**.
1. Seleziona **[!UICONTROL Filter]** dal [!UICONTROL Action] a discesa.
1. In [!UICONTROL Header Name] , immetti: **[!UICONTROL X-Frame-Options]**.
1. Ripeti i passaggi 4 e 5 per aggiungere un filtro con **[!UICONTROL x-frame-options]**.
1. Clic **[!UICONTROL Add]**.
1. Clic **[!UICONTROL Start]**.

![Estensione Firefox](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox_extension.png)

Dopo aver configurato un&#39;estensione, apri [!DNL Target]. A questo punto le pagine dovrebbero essere caricate in [!UICONTROL Visual Experience Composer], anche se [!UICONTROL Enhanced Experience Composer] è disabilitato.

## La pagina non viene visualizzata nel Compositore esperienza visivo (solo Compositore esperienza visivo) {#does-not-load}

* La migliore compatibilità con VEC è garantita dalla versione più recente dell’estensione: [[!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper extension]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md).

  Per verificare se utilizzi la versione più recente, vai a [!UICONTROL Extensions] > [!UICONTROL Manage Extensions] quindi fai clic su [!UICONTROL Details].

* Il [!UICONTROL Visual Experience Composer] richiede la creazione di librerie per eseguire modifiche sulla pagina web. Queste librerie sono incorporate nella libreria at.js e vengono scaricate dall&#39;estensione da [!DNL Adobe] ogni volta che viene utilizzato il Compositore esperienza visivo.

  L&#39;estensione scarica la libreria at.js indipendentemente dal fatto che at.js o [!DNL Adobe Experience Platform Web SDK] sono già inclusi nella pagina.

  Assicurati che non siano state aggiunte modifiche non valide alle intestazioni at.js configurate in [!UICONTROL Administration] > [!UICONTROL Implementation] sezione.

* Assicurati che la pagina web non blocchi le richieste obbligatorie da caricare quando è incorporata all’interno di un iFrame. Ciò include l’utilizzo di direttive CSP precedenti ai fotogrammi o di codice JS personalizzato incorporato nel sito web del cliente, tag meta-HTML o intestazione x-frame-options.

* Assicurati che il codice JavaScript della pagina web non interferisca con le librerie di authoring. Non utilizzare o includere file che utilizzano i seguenti nomi riservati:

   * `target-vec-helper.js`
   * `target-vec.js`
   * `target.js`
   * `admin.css`
   * `sizzle.js`
   * `mixContentCheck.html`

     Inoltre, la sostituzione accidentale di variabili o eventi definiti in questi file potrebbe causare problemi con il Compositore esperienza visivo.

* Il browser sta bloccando una pagina non sicura su un sito sicuro.

  Fai clic sull’icona a sinistra dell’URL nella barra degli indirizzi del browser e fai clic su **[!UICONTROL Disable protection on this page]**

* Hai immesso un URL non valido.
* Se il sito web non viene caricato nel Compositore esperienza visivo o si comporta in modo imprevisto, è possibile che vengano accettati dei cookie sul sito web nel browser prima di tentare di caricare il sito web in [!DNL Target].

## Il Compositore esperienza visivo sembra non funzionare quando uso la modalità Sfoglia. (Solo Compositore esperienza visivo)  {#section_FA2A18E8FD6A4274B2E395DBAA2FB407}

Quando si utilizza la modalità Sfoglia, se si accede a un URL che non dispone di [!DNL Target] librerie implementate ([at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html?lang=it){target=_blank} or [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=it){target=_blank}) o contiene un’intestazione frame-buster, il Compositore esperienza visivo sembra non funzionare. A causa di problemi di sicurezza del browser, [!DNL Target] non può accedere correttamente all’URL a cui sei passato oppure l’URL del Compositore esperienza visivo non viene aggiornato in modo coerente se la pagina viene caricata.

Questo problema si verifica perché il Compositore esperienza visivo carica la pagina web in un `<iframe>`. Gli attuali meccanismi di sicurezza dei browser impediscono [!DNL Target] L’interfaccia utente non accede agli elementi del frame specificato a causa del criterio relativo alla stessa origine. I browser bloccano gli script che tentano di accedere a un frame con un’origine diversa e che include informazioni quali `location.href`.

È necessario utilizzare il nuovo [Estensione Helper per editing video](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) (consigliato) o [vecchia estensione](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) per iniettare [!DNL Target] nelle pagine per sfogliarle in modo ottimale.

## Problemi causati da conflitti CSS in [!UICONTROL Visual Experience Composer]

Verifica se sono presenti file CSS che potrebbero influire sulla visibilità durante il caricamento della pagina web nell’editor. Ad esempio, utilizzando `overflow: hidden` nel corpo della pagina potrebbe causare problemi di scorrimento o attivare eventi di clic che potrebbero interferire con il menu per l’authoring.
