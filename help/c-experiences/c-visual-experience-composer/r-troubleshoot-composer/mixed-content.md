---
keywords: contenuto misto;sicuro;insicuro;cromo;risoluzione dei problemi;vec;visual experience composer;unsecure;http;https;firefox;internet explorer
description: Alcuni browser bloccano la visualizzazione di una pagina se contiene un misto di contenuti protetti e non protetti. Scoprite come abilitare i contenuti misti in Chrome, Firefox ed Edge.
title: Come si attivano i contenuti misti nel browser?
feature: Compositore esperienza visivo
translation-type: tm+mt
source-git-commit: 453106f7534f83c205722421bbf00044fde7da67
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 26%

---


# Abilitazione di contenuti misti nel browser

Il contenuto misto si verifica se la richiesta iniziale è protetta tramite HTTPS, ma il contenuto HTTPS *e* HTTP viene caricato per visualizzare la pagina Web. Il contenuto HTTPS è sicuro. Il contenuto HTTP non è sicuro.

I browser più recenti potrebbero bloccare la visualizzazione di una pagina o visualizzare messaggi di avviso in caso di combinazione di contenuto protetto e contenuto non protetto.

Viene visualizzato un messaggio di avviso se [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Target] tenta di aprire una pagina contenente contenuti misti. Questo messaggio informa come disattivare il blocco nel browser. La disattivazione del blocco consente di aprire un sito HTTP o un sito con chiamate miste (HTTPS e HTTP).

![Avviso contenuto misto](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/mixed_content_warning.png)

In precedenza, quando i contenuti misti non erano consentiti, era comunque possibile eseguire alcune azioni nel passaggio 1 del flusso di lavoro guidato in tre passaggi durante la creazione di attività. [!DNL Target]Ora blocca le azioni nel passaggio 1. Quando viene visualizzato questo messaggio, è necessario abilitare il contenuto misto prima di continuare a creare l&#39;attività.

Le impostazioni di sicurezza del browser potrebbero bloccare i contenuto misti o non protetti (HTTP) caricati in una pagina o in un frame protetti (HTTPS) (come, ad esempio Compositore esperienza visivo). Se non desiderate disattivare le impostazioni di protezione del browser, dovete disporre di un sito Web HTTPS.

Se il sito Web è in esecuzione su un dominio non sicuro (HTTP), è necessario consentire al VEC di caricare il contenuto misto attivo.

>[!NOTE]
>
>Consentire l’utilizzo di contenuti misti influenza solo il Compositore esperienza visivo e non il sito attivo.

Per ulteriori informazioni, vedi la sezione sui [contenuto misti](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content) nel sito web di *Mozilla Developer Network* (MDN).

## Abilitazione di contenuti misti in Google Chrome {#task_FF297A08F66E47A588C14FD67C037B3A}

Se visitate un sito tramite una connessione protetta, Chrome verifica che il contenuto della pagina Web sia stato trasmesso in modo sicuro.

Vedere &quot;[Questa pagina contiene contenuto non sicuro](https://support.google.com/chrome/answer/1342714?hl=en)&quot; nella Guida di Google Chrome.

Se utilizzate il VEC con la versione più recente di Chrome (versione 79.0.3945.117 o successiva), dovete aggiornare le impostazioni del sito. I visitatori del sito non devono completare questi passaggi.

1. Fate clic sull&#39;icona Blocca (cautela), quindi fate clic su **[!UICONTROL Impostazioni sito]**.

   ![Impostazioni sito](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/site-settings.png)

1. Scorrete fino a **[!UICONTROL Contenuto non sicuro]**, quindi utilizzate l&#39;elenco a discesa per cambiare &quot;Blocca (predefinito)&quot; in &quot;Consenti&quot;.

   ![Contenuto non protetto](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/insecure-content.png)

1. Ricaricare la pagina VEC.

## Abilitazione di contenuti misti in Mozilla Firefox {#task_5448763B8DC941FD80F84041AEF0A14D}

Per impostazione predefinita, Firefox blocca le pagine che contengono un misto di contenuti protetti e non protetti. Si consiglia di modificare definitivamente questa impostazione per utilizzare [!DNL Target]. I visitatori del sito non devono completare questi passaggi.

1. In Firefox, digita `about:config` nella barra degli indirizzi.
1. Conferma il messaggio di avvertenza visualizzato da Firefox.

   ![Avvertimento Firefox](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox.png)

1. Nella barra di ricerca digita `block_active`.

   ![Firefox block_active, impostazione](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox3.png)

1. Fai doppio clic su ` **[!UICONTROL security.mixed_content.block_active_content]**`.

   Il valore cambia da “Vero” a “Falso”. Quando il valore è impostato su “Falso”, l&#39;operazione è completata.

   ![Protezione Firefox](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox2.png)

Dopo aver modificato questa impostazione, riavviare il computer.

## Abilitazione di contenuti misti in Microsoft Edge

Se visitate un sito tramite una connessione protetta, Edge verifica che il contenuto della pagina Web sia stato trasmesso in modo sicuro.

Se utilizzate il VEC con la versione più recente di Edge, dovete aggiornare le impostazioni del sito. I visitatori del sito non devono completare questi passaggi.

1. Fate clic sull&#39;icona Blocca (cautela), quindi fate clic su **[!UICONTROL Autorizzazioni sito]**.

   ![Autorizzazioni del sito in Microsoft Edge](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/ms-edge.png)

1. Scorrete fino a **[!UICONTROL Contenuto non sicuro]**, quindi utilizzate l&#39;elenco a discesa per cambiare &quot;Blocca (predefinito)&quot; in &quot;Consenti&quot;.

   ![Contenuto non protetto](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/ms-edge-2.png)

1. Ricaricare la pagina VEC.