---
keywords: contenuto misto;protetto;non protetto;chrome;risoluzione dei problemi;vec;compositore esperienza visivo;non sicuro;http;https;firefox;internet explorer
description: Scopri come consentire contenuti misti in Chrome, Firefox ed Edge. È possibile abilitare i contenuti misti quando un browser blocca la visualizzazione di una pagina in presenza di contenuti protetti e contenuti non protetti.
title: Come abilitare i contenuti misti nel browser
feature: Visual Experience Composer (VEC)
exl-id: a2209af6-65e5-427e-b2cb-53b803728ef3
source-git-commit: 5e6bb16ad752b85e9a7dad088d15f5f6d3897ee9
workflow-type: ht
source-wordcount: '593'
ht-degree: 100%

---

# Consentire contenuti misti nel browser

I contenuti misti si verificano se la richiesta iniziale è protetta tramite HTTPS, ma per visualizzare la pagina web vengono caricati i contenuti HTTPS *e* HTTP. Il contenuto HTTPS è sicuro. Il contenuto HTTP non è sicuro.

I browser moderni potrebbero bloccare la visualizzazione di una pagina o visualizzare messaggi di avviso in caso di combinazione di contenuto sicuro e contenuto non sicuro.

Viene visualizzato un messaggio di avviso se il [!UICONTROL Compositore esperienza visivo] (VEC) in [!DNL Adobe Target] tenta di aprire una pagina con contenuti misti. Questo messaggio spiega come disattivare il blocco nel browser. La disattivazione del blocco consente di aprire un sito HTTP o un sito con chiamate miste (HTTPS e HTTP).

![Avviso contenuti misti](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/mixed_content_warning.png)

In precedenza, quando i contenuti misti non erano consentiti, era comunque possibile eseguire alcune azioni nel passaggio 1 del flusso di lavoro guidato in tre passaggi durante la creazione di attività. [!DNL Target] Ora blocca le azioni nel passaggio 1. Quando viene visualizzato questo messaggio, prima di continuare la creazione dell’attività devi abilitare i contenuti misti.

Le impostazioni di sicurezza del browser potrebbero bloccare i contenuto misti o non sicuri (HTTP) caricati in una pagina o in un frame sicuri (HTTPS) (come, ad esempio Compositore esperienza visivo). Se non vuoi disabilitare le impostazioni di sicurezza del browser, devi disporre di un sito web HTTPS.

Se il sito web è in esecuzione su un dominio non sicuro (HTTP), devi consentire al Compositore esperienza visivo di caricare i contenuti misti attivi.

>[!NOTE]
>
>Consentire l’utilizzo di contenuti misti influenza solo il Compositore esperienza visivo e non il sito attivo.

Per ulteriori informazioni, consulta la pagina sui [contenuti misti](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content) nel sito web di *Mozilla Developer Network* (MDN).

## Consentire contenuti misti in Google Chrome {#task_FF297A08F66E47A588C14FD67C037B3A}

Se stai visitando un sito tramite una connessione sicura, Chrome verifica che i contenuti della pagina web siano trasmessi in modo sicuro.

Consulta la pagina relativa ai [siti non sicuri](https://support.google.com/chrome/answer/1342714?hl=it) nella guida di Google Chrome.

Se utilizzi il Compositore esperienza visivo con la versione più recente di Chrome (versione 79.0.3945.117 o successiva), devi aggiornare le impostazioni del sito. I visitatori del sito non devono completare questi passaggi.

1. Fai clic sull’icona del lucchetto (avviso), quindi fai clic su **[!UICONTROL Impostazioni sito]**.

   ![Impostazioni sito](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/site-settings.png)

1. Scorri fino a **[!UICONTROL Contenuto non sicuro]**, quindi utilizza l’elenco a discesa per modificare “Blocca (predefinita)” in “Consenti”.

   ![Contenuto non sicuro](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/insecure-content.png)

1. Ricarica la pagina del Compositore esperienza visivo.

## Consentire contenuti misti in Firefox {#task_5448763B8DC941FD80F84041AEF0A14D}

Per impostazione predefinita, Firefox blocca le pagine che contengono un misto di contenuti sicuri e non sicuri. Si consiglia di modificare definitivamente questa impostazione per utilizzare [!DNL Target]. I visitatori del sito non devono completare questi passaggi.

1. In Firefox, digita `about:config` nella barra degli indirizzi.
1. Conferma il messaggio di avvertenza visualizzato da Firefox.

   ![Avvertenza di Firefox](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox.png)

1. Nella barra di ricerca digita `block_active`.

   ![Impostazione block_active di Firefox](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox3.png)

1. Fai doppio clic su ` **[!UICONTROL security.mixed_content.block_active_content]**`.

   Il valore cambia da “Vero” a “Falso”. Quando il valore è impostato su “False”, l’operazione è completata.

   ![Sicurezza di Firefox](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox2.png)

Riavvia il computer dopo aver modificato questa impostazione.

## Consentire contenuti misti in Microsoft Edge

Se stai visitando un sito tramite una connessione sicura, Edge verifica che i contenuti della pagina web siano trasmessi in modo sicuro.

Se utilizzi il Compositore esperienza visivo con l’ultima versione di Edge, devi aggiornare le impostazioni del sito. I visitatori del sito non devono completare questi passaggi.

1. Fai clic sull’icona del lucchetto (avviso), quindi fai clic su **[!UICONTROL Autorizzazioni per questo sito]**.

   ![Autorizzazioni per questo sito in Microsoft Edge](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/ms-edge.png)

1. Scorri fino a **[!UICONTROL Contenuto non sicuro]**, quindi utilizza l’elenco a discesa per modificare “Blocca (predefinito)” in “Consenti”.

   ![Contenuto non sicuro](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/ms-edge-2.png)

1. Ricarica la pagina del Compositore esperienza visivo.
