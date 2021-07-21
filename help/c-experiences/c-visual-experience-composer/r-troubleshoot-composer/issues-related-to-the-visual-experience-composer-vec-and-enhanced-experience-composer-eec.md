---
keywords: Targeting;compositore esperienza visivo;whitelist;white list;inserire nell'elenco Consentiti;elenco consentiti;compositore esperienza visivo avanzato;vec;risoluzione dei problemi compositore esperienza visivo;risoluzione dei problemi;eec;compositore esperienza avanzato;tls;tls 1.2
description: Scopri come risolvere i problemi che a volte si verificano in Adobe [!DNL Target] Compositore esperienza visivo (VEC) e nel Compositore esperienza avanzato (EEC) in determinate condizioni.
title: Come posso risolvere i problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato?
feature: Compositore esperienza visivo
exl-id: d829cd63-950f-4bb4-aa58-0247f85de383
source-git-commit: 13b980bbcd63bf6fd6b3ac880a80bd7bd4b67653
workflow-type: tm+mt
source-wordcount: '1554'
ht-degree: 49%

---

# Risoluzione dei problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato

Problemi di visualizzazione e altri problemi si verificano a volte nel [!DNL Adobe Target] [!UICONTROL Compositore esperienza visivo] (VEC) e nel [!UICONTROL Compositore esperienza avanzato] (EEC) a determinate condizioni.

## In che modo i criteri di implementazione dei cookie SameSite di Google Chrome influiscono sul Compositore esperienza visivo e sul Compositore esperienza avanzato? {#samesite}

Tieni presente le modifiche che influiscono sul Compositore esperienza visivo e sul Compositore esperienza avanzato quando utilizzi le seguenti versioni di Chrome:

>[!NOTE]
>
>La seguente modifica interessa tutti e tre gli aggiornamenti descritti di seguito:
>
> * *not* sarà in grado di utilizzare il Compositore esperienza visivo (con o senza l’estensione VEC Helper installata e abilitata) nelle pagine protette da password dei propri siti. I cookie di accesso al sito sono considerati un cookie di terze parti e vengono inviati con la richiesta di accesso. L’unica eccezione è quando il cookie di accesso al sito dispone già del parametro SameSite impostato su &quot;none&quot;.


**Chrome 94 (21 settembre 2021)**: Con le imminenti modifiche pianificate per la versione di Chrome 94 (21 settembre 2021), le seguenti modifiche hanno un impatto su tutti gli utenti con le versioni del browser Chrome 94+:

* Il flag della riga di comando `--disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure` verrà rimosso.

**Chrome 91 (25 maggio 2021)**: Con le modifiche implementate per la versione di Chrome 91 (25 maggio 2021), le seguenti modifiche hanno un impatto su tutti gli utenti con le versioni del browser Chrome 91+:

* I flag `#same-site-by-default-cookies` e `#cookies-without-same-site-must-be-secure` sono stati rimossi da `chrome://flags`. Questo comportamento ora è abilitato per impostazione predefinita.

**Chrome 80 (agosto 2020)**: Con le modifiche implementate ad agosto 2020, tutti gli utenti con versioni del browser Chrome 80+:

* *not* sarà in grado di scaricare le librerie [!DNL Target] durante la modifica di un&#39;attività (quando queste non sono già sul sito). Questo perché la chiamata di download viene effettuata dal dominio del cliente verso un dominio di Adobe protetto e viene rifiutata come non autenticata.
* Il Compositore esperienza avanzato *non* funziona per tutti gli utenti perché non è in grado di impostare l’attributo SameSite per i cookie su `adobemc.com domain`. Senza questo attributo, il browser rifiuta questi cookie, causando il mancato funzionamento del Compositore esperienza avanzato.

### Determinare quali cookie sono bloccati

Per determinare quali cookie sono bloccati a causa dei criteri di imposizione dei cookie SameSite, utilizza gli strumenti per sviluppatori in Chrome.

1. Per accedere agli Strumenti per sviluppatori, mentre visualizzi il Compositore esperienza visivo in Chrome, fai clic sull&#39;icona **[!UICONTROL ellissi]** nell&#39;angolo in alto a destra di Chrome > **[!UICONTROL Altri strumenti]** > **[!UICONTROL Strumenti per sviluppatori]**.
1. Fai clic sulla scheda **[!UICONTROL Rete]** , quindi cerca i cookie bloccati.

   >[!NOTE]
   >
   >Utilizza la casella di controllo **[!UICONTROL Ha bloccato i cookie]** per semplificare la ricerca dei cookie bloccati.

   La figura seguente mostra un cookie bloccato:

   ![Strumenti sviluppatore > Scheda Rete che mostra un cookie bloccato](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/chrome-developer-tools.png)

### Estensione Google VEC Helper

Adobe ha inviato un&#39;estensione VEC Helper aggiornata a Google Chrome Store. Questa estensione sovrascrive gli attributi dei cookie per impostare l&#39;attributo `SameSite="none"` quando necessario. L&#39; [estensione aggiornata si trova qui](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak?hl=en). Per ulteriori informazioni sull&#39;installazione e l&#39;utilizzo dell&#39;estensione VEC Helper, consulta [Estensione helper del Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md).

Per i cookie del tuo sito, devi specificare i cookie per nome.

>[!NOTE]
>
>Questo approccio è adatto solo quando tutti i cookie sono impostati in un unico dominio. L’helper VEC non consente a [!DNL Target] di specificare i cookie per più di un dominio.

Passa il cursore [!UICONTROL Cookie] nella posizione attiva, quindi specifica il cookie per nome e il dominio del cookie. Il nome del cookie è &quot;mbox&quot; e il dominio del cookie è il secondo e il primo livello dei domini da cui distribuisci la mbox. Dato che viene distribuito dal dominio della società, il cookie è un cookie dei siti Web visualizzati. Esempio: `mycompany.com`. Per ulteriori informazioni, consulta [Cookie Adobe Target](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-target.html?lang=it) nella *Guida utente dell&#39;interfaccia Experience Cloud*.

![L’opzione Cookie nell’estensione VEC Helper](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

### Alternative e soluzioni alternative

Utilizza una delle seguenti opzioni per garantire che VEC e Compositore esperienza avanzato continuino a funzionare come previsto:

* Scarica e utilizza l&#39;estensione VEC Helper aggiornata [a1/>.](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak?hl=en)
* Usa il browser Mozilla Firefox. Firefox non ha ancora applicato questo criterio.
* Utilizza i seguenti flag per eseguire Google Chrome dalla riga di comando fino al 21 settembre 2021. Dopo il 21 settembre, il tuo sito web non funzionerà più nel Compositore esperienza visivo. Se esegui l’aggiornamento a Chrome 94, devi generare manualmente i cookie con `SameSite=none` e `Secure` sui tuoi siti web.

   ```
   --disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure
   ```

## [!DNL Target] supporta iframe a più livelli?

[!DNL Target] non supporta gli iframe a più livelli. Se il sito web carica un iframe con un iframe secondario, at.js interagisce solo con l’iframe principale. [!DNL Target]Le librerie di non interagiscono con l’iframe secondario.

Come soluzione alternativa, puoi aggiungere all’esperienza una pagina con l’URL dell’iframe secondario.

## Quando si tenta di modificare una pagina, compare solo un’icona che ruota anziché la pagina. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_313001039F79446DB28C70D932AF5F58}

Questa situazione può verificarsi se l’URL contiene un carattere #. Per risolvere il problema, passa alla modalità Sfoglia nel Compositore esperienza visivo, quindi ritorna alla modalità Componi. L’icona che ruota scompare e la pagina viene caricata correttamente.

## Le intestazioni Content Security Policy (CSP) bloccano le librerie [!DNL Target] sul mio sito web. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_89A30C7A213D43BFA0822E66B482B803}

Se le intestazioni CSP del tuo sito web bloccano le librerie di Target, quindi caricano il sito web ma ne impediscono la modifica, assicurati che le librerie di Target non siano bloccate.

>[!NOTE]
>
>Oltre alle seguenti informazioni, puoi utilizzare l’estensione [Adobe Target VEC Helper](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) per il browser Google Chrome.

![](assets/cps_headers.png)

Come soluzione alternativa, è possibile configurare una regola con Requestly per rimuovere le intestazioni CSP, come illustrato di seguito:

![](assets/cps_headers_2.png)

È possibile configurare con Requestly una regola simile per qualsiasi intestazione che impedisce il caricamento di una risorsa all&#39;interno del Compositore esperienza visivo.

Per Requestly, ogni volta che è necessario rimuovere le intestazioni, bisogna eseguire una delle seguenti operazioni:

* Aggiungere regole URL per l&#39;URL che si desidera aprire nel Compositore esperienza visivo in modo tale che le intestazioni vengano rimosse solo per tali URL.
* Abilitare la regola quando si effettuano modifiche nel Compositore esperienza visivo e disabilitarla quando non lo si utilizza.

## Il Compositore esperienza visivo o Compositore esperienza avanzato sembra non funzionare o non viene inizializzato quando si vuole modificare un&#39;attività già salvata. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_5AC3BA8F8FBB451EA814F298D0645E54}

Se il sito web è stato modificato al di fuori del Compositore esperienza visivo dopo la configurazione dell&#39;esperienza, non è possibile trovare i selettori su cui sono state eseguite le azioni in precedenza quando l&#39;attività viene riaperta per essere nuovamente modificata. La pagina apparentemente non funziona, senza che venga visualizzato alcun avviso.

## Il Compositore esperienza visivo o Compositore esperienza avanzato non mostra i miei banner rotanti e altri contenuti che contengono JavaScript. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_8B5BE6EB050B42D6A14A054724C41330}

Per impostazione predefinita, il Compositore esperienza visivo blocca gli elementi JavaScript. Per utilizzarli, disattiva JavaScript nelle impostazioni del Compositore esperienza visivo. In base alla configurazione del sito, alcuni elementi potrebbero continuare a essere visualizzati in modo non corretto o rimanere non disponibili.

## Alla modifica di un elemento della pagina, vengono modificati più elementi. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_309188ACF34942989BE473F63C5710AF}

Se lo stesso ID di elemento DOM è utilizzato in più elementi della pagina, la modifica di uno di questi elementi influenza tutti gli elementi con lo stesso ID. Per evitare il problema, è opportuno utilizzare ciascun ID solo una volta in ogni pagina. Questa pratica è una best practice HTML standard. Per ulteriori informazioni, consulta [Scenari di modifica delle pagine](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Non sono in grado di modificare le esperienze per un sito non compatibile con iFrame. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_9FE266B964314F2EB75604B4D7047200}

Questo problema può essere affrontato abilitando il Compositore esperienza avanzato. Fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Compositore esperienza visivo]**, quindi seleziona la casella di controllo che abilita il Compositore esperienza avanzato. Il Compositore esperienza avanzato utilizza un proxy gestito da Adobe per caricare la pagina da modificare. Questo proxy consente la modifica su siti non compatibili con iFrame e su siti e pagine in cui non hai ancora aggiunto il codice Adobe Target. Le attività non vengono fornite al sito fino all&#39;aggiunta del codice. È possibile che alcuni siti non vengano caricati tramite il Compositore esperienza avanzato. In questo caso, deseleziona questa opzione per caricare il Compositore esperienza visivo tramite un iFrame.

>[!NOTE]
>
>Le pagine ospitate localmente o le pagine che non sono accessibili all’esterno della rete non sono accessibili al server proxy Adobe e non possono essere aperte nel Compositore esperienza avanzato. Queste pagine potrebbero includere gli URL di staging, i test di accettazione degli utenti (TAU) o le pagine in hosting locale.

## Desidero configurare test su pagine che per ora sono prive dell&#39;implementazione mbox/target. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_DE63BCCB5B124E10A71FA579B582A80A}

Vedi “Non sono in grado di modificare le esperienze per un sito non compatibile con iFrame” più sopra.

## Gli stili di testo in grassetto e corsivo con Modifica testo/HTML o Cambia testo/HTML non vengono visualizzati sulla mia pagina. A volte il testo scompare dopo l&#39;applicazione di queste modifiche. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_7A71D6DF41084C58B34C18701E8774E5}

Se si utilizza **[!UICONTROL Modifica testo/HTML]** nel Compositore esperienza visivo per A/B o le attività di targeting per l&#39;esperienza o **[!UICONTROL Cambia testo/HTML]** per la personalizzazione automatizzata o per attività di test multivariato per rendere il testo in grassetto o corsivo, questi stili potrebbero non essere applicati nella pagina o il testo potrebbe scomparire dalla pagina nel Compositore esperienza visivo. Questo accade a causa del modo in cui l’editor Rich Text applica questi stili potrebbe interferire con il markup del sito web.

Se vedi questo problema:

1. Fai clic sul pulsante **[!UICONTROL HTML]** nell&#39;editor rich-text per accedere alla modalità di modifica della sorgente.
1. Trova gli elementi di stile di testo.

   * Per il testo in grassetto, modifica gli elementi `<strong>` in `<b>`.

   * Per il testo in corsivo, modifica gli elementi `<em>` in `<i>`.

## Per le attività di personalizzazione automatizzata, lo scambio di immagini nel Compositore esperienza visivo e Compositore esperienza avanzato sembra non funzionare. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_88AABFDFE6A3420299B0D508B12A3994}

L&#39;aggiunta dell&#39;offerta di un immagine a una posizione prende la dimensione totale dello spazio immagine originale nel Compositore esperienza visivo e Compositore esperienza avanzato. Alla consegna, l&#39;immagine non viene espansa ed è mostrata così com&#39;è, quindi non c&#39;è impatto sulla consegna.
