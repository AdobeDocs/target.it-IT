---
keywords: contenuto misto;protetto;non protetto;chrome;risoluzione dei problemi;vec;compositore esperienza visivo;non sicuro;http;https;firefox;internet explorer
description: Scopri come abilitare i contenuti misti in [!DNL Chrome], [!DNL Firefox], e [!DNL Edge].
title: Come abilitare i contenuti misti nel browser
feature: Visual Experience Composer (VEC)
exl-id: a2209af6-65e5-427e-b2cb-53b803728ef3
source-git-commit: c5b43faa2fc55c2c8737e586cfdfaa1444a05880
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 65%

---

# Consentire contenuti misti nel browser

I contenuti misti si verificano se la richiesta iniziale è protetta tramite HTTPS, ma per visualizzare la pagina web vengono caricati i contenuti HTTPS *e* HTTP. Il contenuto HTTPS è sicuro. Il contenuto HTTP non è sicuro.

I browser moderni potrebbero bloccare la visualizzazione di una pagina o visualizzare messaggi di avviso in caso di combinazione di contenuto sicuro e contenuto non sicuro.

Viene visualizzato un messaggio di avviso se il [!UICONTROL Compositore esperienza visivo] (VEC) in [!DNL Adobe Target] tenta di aprire una pagina con contenuti misti. Questo messaggio spiega come disattivare il blocco nel browser. La disattivazione del blocco consente di aprire un sito HTTP o un sito con contenuti misti (HTTPS e HTTP).

![Avviso contenuti misti](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/mixed_content_warning.png)

In precedenza, quando i contenuti misti non erano consentiti, era comunque possibile eseguire alcune azioni nel passaggio 1 del flusso di lavoro guidato in tre passaggi durante la creazione di attività. [!DNL Target] Ora blocca le azioni nel passaggio 1. Quando viene visualizzato questo messaggio, prima di continuare la creazione dell’attività devi abilitare i contenuti misti.

Le impostazioni di sicurezza del browser potrebbero bloccare i contenuto misti o non sicuri (HTTP) caricati in una pagina o in un frame sicuri (HTTPS) (come, ad esempio Compositore esperienza visivo). Se non vuoi disabilitare le impostazioni di sicurezza del browser, devi disporre di un sito web HTTPS.

Se il sito web è in esecuzione su un dominio non sicuro (HTTP), devi consentire al Compositore esperienza visivo di caricare i contenuti misti attivi.

>[!IMPORTANT]
>
>Consentire l’utilizzo di contenuti misti influenza solo il Compositore esperienza visivo e non il sito attivo.

Per ulteriori informazioni, consulta la pagina sui [contenuti misti](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content) nel sito web di *Mozilla Developer Network* (MDN).

## Consentire contenuti misti in [!DNL Google Chrome] {#task_FF297A08F66E47A588C14FD67C037B3A}

Se stai visitando un sito tramite una connessione sicura, [!DNL Chrome] verifica che il contenuto della pagina web sia stato trasmesso in modo sicuro.

Consulta &quot;[Gestione avvisi sui siti non sicuri](https://support.google.com/chrome/answer/99020?hl=it)&quot; nella Guida di Google Chrome.

Se utilizzi il Compositore esperienza visivo con l’ultima versione di [!DNL Chrome] (versione 79.0.3945.117 o successiva), è necessario aggiornare le impostazioni del sito. I visitatori del sito non devono completare questi passaggi.

1. Fai clic sull’icona del lucchetto (avviso), quindi fai clic su **[!UICONTROL Impostazioni sito]**.

   ![Impostazioni sito](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/site-settings.png)

1. Scorri fino a **[!UICONTROL Contenuto non sicuro]**, quindi utilizza l’elenco a discesa per modificare “Blocca (predefinita)” in “Consenti”.

   ![Contenuto non sicuro](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/insecure-content.png)

1. Ricarica la pagina del Compositore esperienza visivo.

## Consentire contenuti misti in [!DNL Mozilla Firefox] {#task_5448763B8DC941FD80F84041AEF0A14D}

Per impostazione predefinita, [!DNL Firebox] blocca le pagine che contengono un misto di contenuti sicuri e non sicuri. È necessario modificare definitivamente questa impostazione per utilizzare [!DNL Target]. I visitatori del sito non devono completare questi passaggi.

1. In Firefox, digita `about:config` nella barra degli indirizzi.
1. Conferma il messaggio di avvertenza visualizzato da [!DNL Firefox].

   ![Avvertenza di Firefox](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox.png)

1. Nella barra di ricerca digita `block_active`.

   ![Impostazione block_active di Firefox](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox3.png)

1. Fai doppio clic su ` **[!UICONTROL security.mixed_content.block_active_content]**`.

   Il valore cambia da “Vero” a “Falso”. Quando il valore è impostato su “False”, l’operazione è completata.

   ![Sicurezza di Firefox](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox2.png)

1. Riavvia il computer dopo aver modificato questa impostazione.

## Consentire contenuti misti in [!DNL Microsoft Edge]

Se stai visitando un sito tramite una connessione sicura, [!DNL Edge] verifica che il contenuto della pagina web sia stato trasmesso in modo sicuro.

Se utilizzi il Compositore esperienza visivo con l’ultima versione di [!DNL Edge], è necessario aggiornare le impostazioni del sito. I visitatori del sito non devono completare questi passaggi.

1. In entrata [!DNL Edge], fai clic su **[!DNL Microsoft Edge]** nella barra dei menu, **[!UICONTROL Impostazioni]**, quindi fai clic su **Cookie e autorizzazioni per il sito**.

1. Scorri fino a **[!UICONTROL Contenuto non sicuro]**.

1. Clic **[!UICONTROL Contenuto non sicuro]**, quindi fai clic su **[!UICONTROL Aggiungi]** accanto a **[!UICONTROL Consenti]**, aggiungi il sito su cui consentire contenuti non sicuri, quindi fai clic su **[!UICONTROL Aggiungi]**.

1. Ricarica la pagina del Compositore esperienza visivo.
