---
description: Alcuni browser bloccano la visualizzazione di una pagina se contiene un misto di contenuti protetti e non protetti.
keywords: contenuto misto;sicuro;non sicuro;chrome;risoluzione dei problemi;compositore esperienza visivo;non protetto
seo-description: Alcuni browser bloccano la visualizzazione di una pagina se contiene un misto di contenuti protetti e non protetti.
seo-title: Consentire contenuti misti nel browser
solution: Target
title: Consentire contenuti misti nel browser
topic: Advanced,Standard,Classic
uuid: 6944ce97-ff73-4b61-b006-35862ff83ef1
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Consentire contenuti misti nel browser{#enabling-mixed-content-in-your-browser}

Alcuni browser bloccano la visualizzazione di una pagina se contiene un misto di contenuti protetti e non protetti.

## Consentire contenuti misti nel browser {#concept_46D022D50280468C9EF6D5DF6EFC911C}

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

## Consentire contenuti misti in Firefox {#task_5448763B8DC941FD80F84041AEF0A14D}

Per impostazione predefinita, Firefox blocca le pagine che contengono un misto di contenuti protetti e non protetti. Si consiglia di modificare definitivamente questa impostazione per utilizzare [!DNL Target].

<!-- 

target/t_mixed_content_firefox.xml

 -->

1. In Firefox, digita `about:config` nella barra degli indirizzi.
1. Conferma il messaggio di avvertenza visualizzato da Firefox.
1. Nella barra di ricerca digita `block_active`.
1. Fai doppio clic su ` **[!UICONTROL security.mixed_content.block_active_content]**`.

   Il valore cambia da “Vero” a “Falso”. Quando il valore è impostato su “Falso”, l'operazione è completata.  È consigliabile riavviare il computer dopo aver modificato questa impostazione.

## Consentire contenuti misti in Internet Explorer {#task_59E7D13C04DF486C92CD78D0C63DDDE8}

Per impostazione predefinita, Internet Explorer blocca le pagine che contengono un misto di contenuti protetti e non protetti. È consigliabile modificare in modo permanente questa impostazione per utilizzare Target Standard.

<!-- 

target/t_mixed_content_ie.xml

 -->

1. In Internet Explorer, fai clic sull’icona Impostazioni &gt; **[!UICONTROL Opzioni Internet]**.
1. Apri la scheda [!UICONTROL Sicurezza.]
1. Seleziona **[!UICONTROL Internet]**, quindi fai clic su **[!UICONTROL Livello personalizzato]**.
1. Seleziona **[!UICONTROL Varie]**.
1. In [!UICONTROL Varie], abilita **[!UICONTROL Visualizza contenuto misto]**.
1. Fai clic su **[!UICONTROL OK]** &gt; **[!UICONTROL Sì]** &gt; **[!UICONTROL Applica]**.

È consigliabile riavviare il computer dopo aver modificato questa impostazione.

## Consentire contenuti misti in Chrome {#task_FF297A08F66E47A588C14FD67C037B3A}

Se stai visitando un sito tramite una connessione sicura, Google Chrome verifica che i contenuti della pagina web siano trasmessi in modo sicuro.

<!-- 

target/t_mixed_content_chrome.xml

 -->

Consulta [Gestire gli avvisi per i siti non sicuri](https://support.google.com/chrome/answer/1342714?hl=en) nella guida di Google Chrome.
