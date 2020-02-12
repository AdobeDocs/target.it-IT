---
keywords: mixed content;secure;insecure;chrome;troubleshooting;vec;visual experience composer;unsecure
description: Alcuni browser bloccano la visualizzazione di una pagina se contiene un misto di contenuti protetti e non protetti.
title: Abilitazione di contenuti misti nel browser
topic: Advanced,Standard,Classic
uuid: 6944ce97-ff73-4b61-b006-35862ff83ef1
translation-type: tm+mt
source-git-commit: 65a4fd0d05ad065c9291a83dc0b3066451f7373e

---


# Enabling mixed content in your browser{#enabling-mixed-content-in-your-browser}

Alcuni browser bloccano la visualizzazione di una pagina se contiene un misto di contenuti protetti e non protetti.

Se il Compositore esperienza visivo tenta di aprire una pagina contenente un misto di contenuti protetti e non protetti, un messaggio indica come disabilitare il blocco nel browser in modo da poter aprire un sito HTTP o un sito con chiamate miste (HTTPS e HTTP).

![](assets/mixed_content_warning.gif)

In precedenza, quando i contenuti misti non erano consentiti, era comunque possibile eseguire alcune azioni nel passaggio 1 del flusso di lavoro guidato in tre passaggi durante la creazione di attività. Ora Target blocca le azioni nel passaggio 1. Quando viene visualizzato questo messaggio, prima di continuare è necessario abilitare i contenuti misti.

Le impostazioni di sicurezza del browser potrebbero bloccare i contenuto misti o non protetti (HTTP) caricati in una pagina o in un frame protetti (HTTPS) (come, ad esempio Compositore esperienza visivo). Se non si desidera disabilitare le impostazioni di sicurezza del browser, è necessario disporre di un sito web HTTPS.

Se il sito web è in esecuzione su un dominio non protetto (HTTP), è necessario consentire al Compositore esperienza visivo di caricare i contenuti misti attivi.

>[!NOTE]
>
>Consentire l’utilizzo di contenuti misti influenza solo il Compositore esperienza visivo e non il sito attivo.

Per ulteriori informazioni, vedi la sezione sui [contenuto misti](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content) nel sito web di *Mozilla Developer Network* (MDN).

## Enabling mixed content in Google Chrome {#task_FF297A08F66E47A588C14FD67C037B3A}

Se stai visitando un sito tramite una connessione sicura, Google Chrome verifica che i contenuti della pagina web siano trasmessi in modo sicuro.

Consulta [Gestire gli avvisi per i siti non sicuri](https://support.google.com/chrome/answer/1342714?hl=en) nella guida di Google Chrome.

### Video di formazione: Abilitare il VEC in Chrome versione 79.0.3945.117 o successiva (Gen. 2020) ![Etichetta Panoramica](/help/assets/overview.png)

Se utilizzate il VEC con la versione più recente di Chrome (versione 79.0.3945.117 o successiva), dovete aggiornare le impostazioni del sito. I visitatori del sito non dovranno completare questi passaggi.

>[!VIDEO](https://www.youtube.com/watch?v=6zGCi5Y8eVo)

Il video riportato sopra illustra i passaggi necessari:

1. Fate clic sull&#39;icona Blocca o Avviso, quindi fate clic su Impostazioni sito.

   ![Impostazioni sito](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/site-settings.png)

1. Scorri fino al contenuto non protetto, quindi usa l&#39;elenco a discesa per cambiare Blocca (impostazione predefinita) in Consenti.

   ![Contenuto non protetto](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/insecure-content.png)

1. Ricaricare la pagina VEC.

## Enabling mixed content in Mozilla Firefox {#task_5448763B8DC941FD80F84041AEF0A14D}

Per impostazione predefinita, Firefox blocca le pagine che contengono un misto di contenuti protetti e non protetti. Si consiglia di modificare definitivamente questa impostazione per utilizzare [!DNL Target].

1. In Firefox, digita `about:config` nella barra degli indirizzi.
1. Conferma il messaggio di avvertenza visualizzato da Firefox.
1. Nella barra di ricerca digita `block_active`.
1. Fai doppio clic su ` **[!UICONTROL security.mixed_content.block_active_content]**`.

   Il valore cambia da “Vero” a “Falso”. Quando il valore è impostato su “Falso”, l&#39;operazione è completata.  È consigliabile riavviare il computer dopo aver modificato questa impostazione.

## Enabling mixed content in Microsoft Internet Explorer {#task_59E7D13C04DF486C92CD78D0C63DDDE8}

Per impostazione predefinita, Internet Explorer blocca le pagine che contengono un misto di contenuti protetti e non protetti. Si consiglia di modificare definitivamente questa impostazione per utilizzare Target.

1. In Internet Explorer, fai clic sull’icona Impostazioni > **[!UICONTROL Opzioni Internet]**.
1. Apri la scheda [!UICONTROL Sicurezza.]
1. Seleziona **[!UICONTROL Internet]**, quindi fai clic su **[!UICONTROL Livello personalizzato]**.
1. Seleziona **[!UICONTROL Varie]**.
1. In [!UICONTROL Varie], abilita **[!UICONTROL Visualizza contenuto misto]**.
1. Fai clic su **[!UICONTROL OK]** > **[!UICONTROL Sì]** > **[!UICONTROL Applica]**.

È consigliabile riavviare il computer dopo aver modificato questa impostazione.

