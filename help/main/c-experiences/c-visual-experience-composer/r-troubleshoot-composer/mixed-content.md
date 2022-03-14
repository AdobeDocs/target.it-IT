---
keywords: contenuto misto;sicuro;non sicuro;chrome;risoluzione dei problemi;vec;compositore esperienza visivo;non sicuro;http;https;firefox;internet explorer
description: Alcuni browser bloccano la visualizzazione di una pagina se contiene un misto di contenuti protetti e non protetti. Scopri come abilitare i contenuti misti in Chrome, Firefox e Edge.
title: Come si attivano i contenuti misti nel browser?
feature: Visual Experience Composer (VEC)
exl-id: a2209af6-65e5-427e-b2cb-53b803728ef3
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 26%

---

# Consentire contenuto misto nel browser

Il contenuto misto si verifica se la richiesta iniziale è protetta tramite HTTPS, ma HTTPS *e* Il contenuto HTTP viene caricato per visualizzare la pagina web. Il contenuto HTTPS è protetto. Il contenuto HTTP non è protetto.

I browser moderni potrebbero bloccare la visualizzazione di una pagina o visualizzare messaggi di avviso in caso di combinazione di contenuto protetto e contenuto non protetto.

Viene visualizzato un messaggio di avviso se [!UICONTROL Compositore esperienza visivo] (Compositore esperienza visivo) in [!DNL Target] tenta di aprire una pagina contenente contenuti misti. Questo messaggio spiega come disattivare il blocco nel browser. La disattivazione del blocco consente di aprire un sito HTTP o un sito con chiamate miste (HTTPS e HTTP).

![Avviso contenuto misto](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/mixed_content_warning.png)

In precedenza, quando i contenuti misti non erano consentiti, era comunque possibile eseguire alcune azioni nel passaggio 1 del flusso di lavoro guidato in tre passaggi durante la creazione di attività. [!DNL Target]Ora blocca le azioni nel passaggio 1. Quando viene visualizzato questo messaggio, è necessario abilitare i contenuti misti prima di continuare la creazione dell’attività.

Le impostazioni di sicurezza del browser potrebbero bloccare i contenuto misti o non protetti (HTTP) caricati in una pagina o in un frame protetti (HTTPS) (come, ad esempio Compositore esperienza visivo). Se non desideri disabilitare le impostazioni di sicurezza del browser, devi disporre di un sito web HTTPS.

Se il sito web è in esecuzione su un dominio non sicuro (HTTP), devi consentire al Compositore esperienza visivo di caricare contenuti misti attivi.

>[!NOTE]
>
>Consentire l’utilizzo di contenuti misti influenza solo il Compositore esperienza visivo e non il sito attivo.

Per ulteriori informazioni, vedi la sezione sui [contenuto misti](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content) nel sito web di *Mozilla Developer Network* (MDN).

## Abilitazione di contenuti misti in Google Chrome {#task_FF297A08F66E47A588C14FD67C037B3A}

Se stai visitando un sito tramite una connessione sicura, Chrome verifica che il contenuto della pagina web sia stato trasmesso in modo sicuro.

Vedere &quot;[La pagina presenta contenuto non protetto](https://support.google.com/chrome/answer/1342714?hl=en)&quot; nell’Aiuto di Google Chrome.

Se utilizzi il Compositore esperienza visivo con la versione più recente di Chrome (versione 79.0.3945.117 o successiva), devi aggiornare le impostazioni del sito. I visitatori del sito non devono completare questi passaggi.

1. Fai clic sull’icona Blocca (avviso), quindi fai clic su **[!UICONTROL Impostazioni del sito]**.

   ![Impostazioni sito](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/site-settings.png)

1. Scorri fino a **[!UICONTROL Contenuto non protetto]**, quindi utilizzare l&#39;elenco a discesa per cambiare &quot;Blocco (predefinito)&quot; in &quot;Consenti&quot;.

   ![Contenuto non protetto](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/insecure-content.png)

1. Ricarica la pagina del Compositore esperienza visivo.

## Abilitazione dei contenuti misti in Mozilla Firefox {#task_5448763B8DC941FD80F84041AEF0A14D}

Per impostazione predefinita, Firefox blocca le pagine che contengono un misto di contenuti protetti e non protetti. Si consiglia di modificare definitivamente questa impostazione per utilizzare [!DNL Target]. I visitatori del sito non devono completare questi passaggi.

1. In Firefox, digita `about:config` nella barra degli indirizzi.
1. Conferma il messaggio di avvertenza visualizzato da Firefox.

   ![Avviso Firefox](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox.png)

1. Nella barra di ricerca digita `block_active`.

   ![Impostazione Firefox block_active](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox3.png)

1. Fai doppio clic su ` **[!UICONTROL security.mixed_content.block_active_content]**`.

   Il valore cambia da “Vero” a “Falso”. Quando il valore è impostato su “Falso”, l&#39;operazione è completata.

   ![Sicurezza Firefox](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox2.png)

Riavvia il computer dopo aver modificato questa impostazione.

## Abilitazione di contenuti misti in Microsoft Edge

Se stai visitando un sito tramite una connessione sicura, Edge verifica che il contenuto della pagina web sia stato trasmesso in modo sicuro.

Se utilizzi il Compositore esperienza visivo con l’ultima versione di Edge, devi aggiornare le impostazioni del sito. I visitatori del sito non devono completare questi passaggi.

1. Fai clic sull’icona Blocca (avviso), quindi fai clic su **[!UICONTROL Autorizzazioni sito]**.

   ![Autorizzazioni del sito in Microsoft Edge](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/ms-edge.png)

1. Scorri fino a **[!UICONTROL Contenuto non protetto]**, quindi utilizzare l&#39;elenco a discesa per cambiare &quot;Blocco (predefinito)&quot; in &quot;Consenti&quot;.

   ![Contenuto non protetto](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/ms-edge-2.png)

1. Ricarica la pagina del Compositore esperienza visivo.
