---
keywords: contenuto misto;protetto;non protetto;chrome;risoluzione dei problemi;vec;compositore esperienza visivo;non sicuro;http;https;firefox;internet explorer
description: Scopri come abilitare i contenuti misti in [!DNL Chrome], [!DNL Firefox] e [!DNL Edge].
title: Come abilitare i contenuti misti nel browser
feature: Visual Experience Composer (VEC)
exl-id: a2209af6-65e5-427e-b2cb-53b803728ef3
TQID: 'https://experienceleague.adobe.com/6Q1UvNmU-vSr9sp3pe2JN-wkjFUMWFxtPkgQegArrVw'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 11%
---
# Consentire contenuti misti nel browser {#mixed-content}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come abilitare i contenuti misti in [!DNL Google Chrome], [!DNL Mozilla Firefox] e [!DNL Microsoft Edge], in modo che il **[!UICONTROL Compositore esperienza visivo]** possa aprire siti HTTP e siti con contenuti misti.

>[!ENDSHADEBOX]

Una pagina contiene contenuti misti quando viene richiesta in modo sicuro tramite HTTPS ma carica sia contenuti HTTPS che HTTP. Il contenuto HTTPS è sicuro, mentre il contenuto HTTP non lo è, pertanto i browser moderni potrebbero bloccare una pagina di questo tipo o visualizzare un messaggio di avviso.

Quando il **[!UICONTROL Compositore esperienza visivo]** (VEC) in [!DNL Adobe Target] tenta di aprire una pagina con contenuti misti, viene visualizzato un messaggio di avviso con le istruzioni per disattivare il blocco nel browser. La disattivazione del blocco consente di aprire un sito HTTP o un sito con contenuti misti (HTTPS e HTTP).

![Pagina di creazione attività con il messaggio che gli script del browser devono essere caricati per creare attività, accanto a un&#39;illustrazione del prompt di ricaricamento del browser](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/mixed_content_warning.png)

In precedenza, alcune azioni nel passaggio 1 del flusso di lavoro guidato in tre passaggi rimanevano disponibili quando i contenuti misti non erano consentiti. [!DNL Target] ora blocca tutte le azioni nel passaggio 1, pertanto i contenuti misti devono essere abilitati prima che la creazione dell&#39;attività possa continuare.

Le impostazioni di sicurezza del browser potrebbero bloccare il contenuto non sicuro (HTTP) caricato in una pagina o in un frame protetto (HTTPS), ad esempio nel Compositore esperienza visivo. L&#39;alternativa alla modifica di queste impostazioni è un sito Web HTTPS. Se il sito web viene eseguito su un dominio non sicuro (HTTP), il Compositore esperienza visivo deve essere autorizzato a caricare contenuti misti attivi.

>[!IMPORTANT]
>
>Consentire l’utilizzo di contenuti misti influisce solo sul Compositore esperienza visivo e non sul sito web live.

Per ulteriori informazioni, consulta la pagina sui [contenuti misti](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content) nel sito web di *Mozilla Developer Network* (MDN).

## Abilita contenuto misto in [!DNL Google Chrome]

[!DNL Chrome] verifica che il contenuto di una pagina richiesta tramite una connessione sicura sia stato trasmesso in modo sicuro. Consulta “[Gestire avvisi sui siti non sicuri](https://support.google.com/chrome/answer/99020?hl=it)” nella guida di Google Chrome.

Per utilizzare il Compositore esperienza visivo con la versione più recente di [!DNL Chrome] (versione 79.0.3945.117 o successiva), aggiornare le impostazioni del sito come indicato di seguito. I visitatori del sito non devono completare questi passaggi.

1. Fai clic sull&#39;icona del lucchetto (avviso), quindi fai clic su **[!UICONTROL Impostazioni sito]**.

   ![Barra degli indirizzi di Chrome con il menu di connessione aperto e le impostazioni del sito evidenziate](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/site-settings.png)

1. In **[!UICONTROL Contenuto non sicuro]**, modificare &quot;Blocca (predefinito)&quot; in &quot;Consenti&quot; nell&#39;elenco a discesa.

   ![Impostazioni del sito Chrome con il menu a discesa Contenuto non sicuro aperto e Consenti selezione](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/insecure-content.png)

1. Ricarica la pagina del Compositore esperienza visivo.

## Abilita contenuto misto in [!DNL Mozilla Firefox]

Per impostazione predefinita, [!DNL Firefox] blocca le pagine che contengono un misto di contenuti protetti e non protetti, pertanto questa impostazione deve essere modificata definitivamente per utilizzare [!DNL Target]. I visitatori del sito non devono completare questi passaggi.

1. In [!DNL Firefox] immettere `about:config` nella barra degli indirizzi.
1. Confermare il messaggio di avviso visualizzato da [!DNL Firefox].

   ![Firefox Procedi con la pagina di avviso Attenzione per circa:config con il pulsante Accetta il rischio e continua](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox.png)

1. Nella barra di ricerca immettere `block_active`.

   ![Firefox about:config cerca block_active mostrando security.mixed_content.block_active_content impostato su true](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox3.png)

1. Fare doppio clic su `security.mixed_content.block_active_content`.

   Il valore cambia da &quot;True&quot; a &quot;False&quot;. Quando il valore è impostato su &quot;False&quot;, la modifica è completa.

   ![Firefox about:config che mostra security.mixed_content.block_active_content impostato su false](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox2.png)

1. Riavviare il computer dopo aver modificato questa impostazione.

## Abilita contenuto misto in [!DNL Microsoft Edge]

[!DNL Edge] verifica che il contenuto di una pagina richiesta tramite una connessione sicura sia stato trasmesso in modo sicuro. Per utilizzare il Compositore esperienza visivo con la versione più recente di [!DNL Edge], aggiornare le impostazioni del sito come indicato di seguito. I visitatori del sito non devono completare questi passaggi.

1. In [!DNL Edge], fai clic su **[!DNL Microsoft Edge]** nella barra dei menu, fai clic su **[!UICONTROL Impostazioni]**, quindi su **Cookie e autorizzazioni sito**.
1. Scorri fino a **[!UICONTROL Contenuto non sicuro]** e fai clic su di esso.
1. Accanto a **[!UICONTROL Consenti]**, fare clic su **[!UICONTROL Aggiungi]**, immettere il sito in cui consentire il contenuto non sicuro, quindi fare clic su **[!UICONTROL Aggiungi]**.
1. Ricarica la pagina del Compositore esperienza visivo.
