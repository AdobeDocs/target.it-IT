---
keywords: Targeting;compositore esperienza visivo;vec;risoluzione dei problemi compositore esperienza visivo;risoluzione dei problemi;tls;tls 1.2
description: Scopri come risolvere i problemi in [!UICONTROL Visual Experience Composer] (VEC).
title: Come posso risolvere i problemi relativi a [!UICONTROL Visual Experience Composer]?
feature: Visual Experience Composer (VEC)
exl-id: ca251025-25e8-4e56-9b59-81310fc763c1
source-git-commit: ef5df0ae37ca1d07c0e51c06ed78739b2d2983fc
workflow-type: tm+mt
source-wordcount: '1009'
ht-degree: 23%

---

# Risoluzione dei problemi relativi a [!UICONTROL Visual Experience Composer]

In determinate condizioni si verificano a volte problemi di visualizzazione in [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC).

## Quando apro il sito Web in [!UICONTROL Visual Experience Composer], le librerie [!DNL Target] non vengono caricate. (Solo Compositore esperienza visivo)  {#section_8A7D3F4AD2CC4C3B823EE9432B97E06F}

+++Dettagli
[!DNL Target] aggiunge due parametri (`mboxEdit=1` e `mboxDisable=1`) mentre apre il sito Web in [!UICONTROL Visual Experience Composer].

Se il sito Web (in particolare le app a pagina singola) taglia i parametri o li rimuove mentre ci si sposta da una pagina all&#39;altra (senza ricaricare la pagina), la funzionalità [!DNL Target] non funziona e le librerie [!DNL Target] non vengono caricate.

Per evitare questo problema, assicurati di non tagliare o rimuovere questi due parametri.

+++

## La pagina non si apre nel Compositore esperienza avanzato, o si carica lentamente. Le attività o le esperienze si caricano lentamente nel Compositore esperienza visivo. (Solo Compositore esperienza visivo)  {#section_71E7601BE9894E3DA3A7FBBB72B6B0C1}

+++Dettagli
Diversi problemi possono influire sulle prestazioni della pagina nei compositori esperienza [!UICONTROL Target]. Alcuni problemi comuni includono:

* Sulla pagina non è oresente una mbox.
* Il sito utilizza il blocco proxy, che non consente l&#39;apertura della pagina in nessuno dei Compositori esperienza.
* Il sito non si lascia aprire in un iFrame.

Se si verificano problemi in [!UICONTROL Enhanced Experience Composer], provare a disattivare [!UICONTROL Enhanced Experience Composer] e utilizzare invece [!UICONTROL Visual Experience Composer].

Per disabilitare [!UICONTROL Enhanced Experience Composer], passare a **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** e disattivare l&#39;opzione **[!UICONTROL Enable Enhanced Experience Composer]**.

Alcuni utenti visualizzano il seguente messaggio di errore nella console:

![Messaggio di errore della console](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/console_error_message.jpg)

Se né [!UICONTROL Visual Experience Composer] né [!UICONTROL Enhanced Experience Composer] funzionano, utilizza un&#39;estensione del browser come [!DNL Requestly] ([!DNL Chrome] o [!DNL Firefox]) o Modifica intestazioni di risposta (Firefox) che può sovrascrivere le opzioni di intestazione X-Frames per il sito e consentirne il caricamento in iFrame, abilitando il Compositore esperienza visivo. Se non riesci a utilizzare le estensioni del browser, utilizza il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

>[!NOTE]
>
>Oltre alle informazioni seguenti, è possibile utilizzare l&#39;estensione [[!DNL Adobe Target] [!UICONTROL Visual Editing Helper]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) per [!DNL Google Chrome].

>[!NOTE]
>
>Questi plug-in devono essere utilizzati solo nel contesto di modifica del Compositore esperienza visivo.
>
>Per l&#39;estensione [!DNL Requestly], ogni volta che è necessario rimuovere le intestazioni, eseguire una delle operazioni seguenti:
>
>* Aggiungere regole URL per l&#39;URL che si desidera aprire nel Compositore esperienza visivo in modo tale che le intestazioni vengano rimosse solo per tali URL.
>
>* Abilitare la regola quando si effettuano modifiche nel Compositore esperienza visivo e disabilitarla quando non lo si utilizza.
>
>Per l&#39;estensione [!UICONTROL Modify Response Header] ([!DNL Firefox]), poiché non è possibile aggiungere una regola URL, è necessario eseguire le operazioni seguenti:
>
>* Abilitare la regola quando si effettuano modifiche nel Compositore esperienza visivo e disabilitarla quando non lo si utilizza.

**Per utilizzare l&#39;estensione [!DNL Requestly] in [!DNL Chrome] o [!DNL Firefox]:**

1. Disattivare [!UICONTROL Enhanced Experienced Composer].
1. Installa l&#39;estensione del browser [!DNL Requestly] in [!DNL Chrome] o [!DNL Firefox].
1. Apri l&#39;estensione e configurala:
1. Selezionare **[!UICONTROL Modify headers]**.
1. Immetti quanto segue:

   * Nome regola
   * Regole di modifica

      * Attiva **[!UICONTROL Add]** su **[!UICONTROL Remove]**.
      * Attiva **[!UICONTROL Request]** su **[!UICONTROL Response]**.
      * Immetti “X-Frame-Options” come nome dell&#39;intestazione.
      * Ripeti i passaggi precedenti e immetti “x-frame-options” come nome dell&#39;intestazione.

        >[!NOTE]
        >
        >Le intestazioni manipolate tramite [!DNL Requestly] fanno distinzione tra maiuscole e minuscole.

      * Cambia **[!UICONTROL Equals]** in **[!UICONTROL Contains]** come condizione per l&#39;URL di origine e immetti l&#39;URL dell&#39;attività da caricare nel Compositore esperienza visivo.

     ![immagine chrome_extension](assets/chrome_extension.png)

1. Fare clic su **[!UICONTROL Save]**.

   ![immagine richiedente](assets/requestly.png)

   Ora dovrebbe essere possibile caricare la pagina rapidamente con [!UICONTROL Visual Experience Composer].

**Per utilizzare l&#39;estensione [!DNL Modify Response Headers] in [!UICONTROL Firefox]:**

1. Installa [!UICONTROL Modify Response Headers] in [!DNL Firefox] e riavvia il browser.
1. Dalle estensioni [!DNL Firefox], seleziona l&#39;estensione Modify Response Headers.
1. Fare clic su **[!UICONTROL Preferences]**.
1. Selezionare **[!UICONTROL Filter]** dal menu a discesa [!UICONTROL Action].
1. Nel campo [!UICONTROL Header Name] immettere: **[!UICONTROL X-Frame-Options]**.
1. Ripetere i passaggi 4 e 5 per aggiungere un filtro con **[!UICONTROL x-frame-options]**.
1. Fare clic su **[!UICONTROL Add]**.
1. Fare clic su **[!UICONTROL Start]**.

![Estensione Firefox](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox_extension.png)

Dopo aver configurato un&#39;estensione, aprire [!DNL Target]. Le pagine devono ora essere caricate in [!UICONTROL Visual Experience Composer], anche se [!UICONTROL Enhanced Experience Composer] è disabilitato.

+++

## La pagina non viene visualizzata nel Compositore esperienza visivo (solo Compositore esperienza visivo) {#does-not-load}

+++Dettagli
* La compatibilità con Compositore esperienza visivo è garantita dalla versione più recente dell&#39;estensione: [[!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper extension]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md).

  Per verificare se si sta utilizzando la versione più recente, passare a [!UICONTROL Extensions] > [!UICONTROL Manage Extensions] e fare clic su [!UICONTROL Details].

* [!UICONTROL Visual Experience Composer] richiede la creazione di librerie per eseguire le modifiche sulla pagina Web. Queste librerie sono incorporate nella libreria at.js e vengono scaricate dall&#39;estensione dai server [!DNL Adobe] ogni volta che viene utilizzato il Compositore esperienza visivo.

  L&#39;estensione scarica la libreria at.js indipendentemente dal fatto che at.js o [!DNL Adobe Experience Platform Web SDK] siano già inclusi nella pagina.

  Verifica che non siano state aggiunte modifiche non valide alle intestazioni at.js configurate nella sezione [!UICONTROL Administration] > [!UICONTROL Implementation].

* Assicurati che la pagina web non blocchi le richieste obbligatorie da caricare quando è incorporata all’interno di un iFrame. Ciò include l’utilizzo di direttive CSP precedenti ai fotogrammi o di codice JS personalizzato incorporato nel sito web del cliente, tag meta HTML o intestazione x-frame-options.

* Assicurati che il codice JavaScript della pagina web non interferisca con le librerie di authoring. Non utilizzare o includere file che utilizzano i seguenti nomi riservati:

   * `target-vec-helper.js`
   * `target-vec.js`
   * `target.js`
   * `admin.css`
   * `sizzle.js`
   * `mixContentCheck.html`

     Inoltre, la sostituzione accidentale di variabili o eventi definiti in questi file potrebbe causare problemi con il Compositore esperienza visivo.

* Il browser sta bloccando una pagina non sicura su un sito sicuro.

  Fare clic sull&#39;icona a sinistra dell&#39;URL nella barra degli indirizzi del browser e fare clic su **[!UICONTROL Disable protection on this page]**

* Hai immesso un URL non valido.
* Se il sito web non viene caricato nel Compositore esperienza visivo o si comporta in modo imprevisto, è possibile che vengano accettati dei cookie sul sito web nel browser prima di tentare di caricare il sito web in [!DNL Target].

+++

## Il Compositore esperienza visivo sembra non funzionare quando utilizzo la modalità [!UICONTROL Browse]. (Solo Compositore esperienza visivo)  {#section_FA2A18E8FD6A4274B2E395DBAA2FB407}

+++Dettagli
Quando si utilizza la modalità [!UICONTROL Browse], se si accede a un URL in cui non sono implementate [!DNL Target] librerie ([at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html?lang=it){target=_blank} o [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=it){target=_blank}) o che contiene un&#39;intestazione frame-buster, il Compositore esperienza visivo risulta interrotto. A causa di problemi di sicurezza del browser, [!DNL Target] non può accedere correttamente all&#39;URL a cui sei passato oppure l&#39;URL del Compositore esperienza visivo non viene aggiornato in modo coerente se la pagina viene caricata.

Questo problema si verifica perché VEC carica la pagina web in un `<iframe>`. I meccanismi di sicurezza correnti dei browser impediscono all&#39;interfaccia utente [!DNL Target] di accedere agli elementi del frame specificato a causa del criterio di origine uguale. I browser bloccano gli script che tentano di accedere a un frame con un&#39;origine diversa e che include informazioni quali `location.href`.

È necessario utilizzare la nuova estensione [Helper per editing video](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) per inserire la libreria [!DNL Target] nelle pagine per visualizzarle in modo ottimale.

+++

## Problemi causati da conflitti CSS in [!UICONTROL Visual Experience Composer]

+++Dettagli
Verifica se sono presenti file CSS che potrebbero influire sulla visibilità durante il caricamento della pagina web nell’editor. Ad esempio, l&#39;utilizzo della proprietà `overflow: hidden` nel corpo della pagina potrebbe causare problemi di scorrimento o attivare eventi di clic che potrebbero interferire con il menu per la creazione.

+++
