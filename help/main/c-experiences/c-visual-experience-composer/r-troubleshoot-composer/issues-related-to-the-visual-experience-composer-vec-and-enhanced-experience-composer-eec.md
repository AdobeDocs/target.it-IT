---
keywords: Targeting;compositore esperienza visivo;whitelist;whitelist;lista bianca;inserisco nell'elenco Consentiti esperienza visivo;elenco consentiti;compositore esperienza visivo avanzato;vec;risoluzione dei problemi compositore esperienza visivo;risoluzione dei problemi;compositore esperienza avanzato;tls;tls 1.2
description: Scopri come risolvere i problemi che a volte si verificano nel Compositore esperienza visivo (VEC) di Adobe [!DNL Target] e nel Compositore esperienza avanzato in determinate condizioni.
title: Come posso risolvere i problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato?
feature: Visual Experience Composer (VEC)
exl-id: d829cd63-950f-4bb4-aa58-0247f85de383
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '1401'
ht-degree: 46%

---

# Risoluzione dei problemi relativi a [!UICONTROL Visual Experience Composer] e [!UICONTROL Enhanced Experience Composer]

A volte si verificano problemi di visualizzazione e altri problemi in [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) e [!UICONTROL Enhanced Experience Composer] (EEC) in determinate condizioni.

## In che modo i criteri di implementazione dei cookie SameSite di Google Chrome influiscono sul Compositore esperienza visivo e sul Compositore esperienza avanzato? {#samesite}

Tieni presente le modifiche che interessano il Compositore esperienza visivo e il Compositore esperienza avanzato quando utilizzi le seguenti versioni di Chrome:

>[!NOTE]
>
>La seguente modifica interessa tutti e tre gli aggiornamenti descritti di seguito:
>
> * *non* potrà utilizzare il Compositore esperienza visivo senza che l&#39;estensione VEC Helper sia installata e abilitata per le pagine protette da password dei tuoi siti. I cookie di accesso al sito sono considerati cookie di terze parti e non vengono inviati con richieste di accesso all’interno dell’editor del Compositore esperienza visivo in modalità Sfoglia. L&#39;unica eccezione si verifica quando i cookie di accesso al sito dispongono già degli attributi `SameSite=None` e `Secure` impostati.

**Chrome 94 (21 settembre 2021)**: con le modifiche imminenti pianificate per la versione di Chrome 94 (21 settembre 2021), la seguente modifica interessa tutti gli utenti con le versioni del browser Chrome 94+:

* Il flag della riga di comando `--disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure` verrà rimosso.

**Chrome 91 (25 maggio 2021)**: con le modifiche implementate per la versione di Chrome 91 (25 maggio 2021), la seguente modifica interessa tutti gli utenti con le versioni del browser Chrome 91+:

* I flag `#same-site-by-default-cookies` e `#cookies-without-same-site-must-be-secure` sono stati rimossi da `chrome://flags`. Questo comportamento è ora abilitato per impostazione predefinita.

**Chrome 80 (agosto 2020)**: con le modifiche implementate ad agosto 2020, tutti gli utenti con le versioni del browser Chrome 80+:

* *non* potrà scaricare [!DNL Target] librerie durante la modifica di un&#39;attività (se non sono già presenti nel sito). Questo perché la chiamata di download viene effettuata dal dominio del cliente verso un dominio [!DNL Adobe] protetto e viene rifiutata perché non autenticata.
* Il Compositore esperienza avanzato *non* funzionerà per tutti gli utenti perché non è in grado di impostare l&#39;attributo SameSite per i cookie su `adobemc.com domain`. Senza questo attributo, il browser rifiuta questi cookie, causando il mancato funzionamento del Compositore esperienza avanzato.

### Determinare quali cookie sono bloccati

Per determinare quali cookie sono bloccati a causa dei criteri di imposizione dei cookie SameSite, utilizza gli strumenti per sviluppatori in Chrome.

1. Per accedere agli strumenti per sviluppatori e visualizzare il Compositore esperienza visivo in Chrome, fai clic sull’icona **[!UICONTROL ellipsis]** in alto a destra in Chrome > **[!UICONTROL More Tools]** > **[!UICONTROL Developer Tools]**.
1. Fai clic sulla scheda **[!UICONTROL Network]** > quindi cerca i cookie bloccati.

   >[!NOTE]
   >
   >Utilizza la casella di controllo **[!UICONTROL Has blocked cookies]** per facilitare la ricerca dei cookie bloccati.

   La figura seguente mostra un cookie bloccato:

   ![Strumenti per sviluppatori > scheda Rete che mostra un cookie bloccato](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/chrome-developer-tools.png)

### Estensione VEC Helper [!DNL Adobe Target]

A partire dalla versione 0.7.1, l&#39;estensione [!DNL Adobe Target] VEC Helper per browser aggiunge gli attributi `SameSite=None` e `Secure` a tutti i cookie nelle risposte provenienti da pagine Web modificate nel Compositore esperienza visivo quando l&#39;opzione &quot;Cookie&quot; è attivata nell&#39;interfaccia utente dell&#39;estensione:

![Interfaccia utente dell&#39;estensione Adobe Target VEC Helper UIAdobe Target VEC Helper](assets/cookies-vec-helper.png)

### Alternative e soluzioni alternative

Utilizza una delle seguenti opzioni per garantire che il Compositore esperienza visivo e il Compositore esperienza avanzato continuino a funzionare come previsto:

* Scarica e utilizza l&#39;estensione [VEC Helper](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak?hl=en) aggiornata.
* Utilizza il browser Mozilla Firefox. Firefox non applica ancora questo criterio.
* Utilizza i seguenti flag per eseguire Google Chrome dalla riga di comando fino al 21 settembre 2021. Dopo il 21 settembre, le funzioni che richiedono i cookie non funzioneranno più nel Compositore esperienza visivo, come ad esempio le finestre a comparsa per il consenso di accesso o dei cookie. Se si esegue l&#39;aggiornamento a Chrome 94, è necessario generare manualmente i cookie con `SameSite=none` e `Secure` sui siti Web.

  ```
  --disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure
  ```

## [!DNL Target] supporta gli iframe a più livelli?

[!DNL Target] non supporta gli iframe a più livelli. Se il sito web carica un iframe contenente un iframe secondario, at.js interagisce solo con l’iframe principale. [!DNL Target] librerie non interagiscono con l&#39;iframe secondario.

Come soluzione alternativa, puoi aggiungere all’esperienza una pagina con l’URL dell’iframe secondario.

## Quando si tenta di modificare una pagina, compare solo un’icona che ruota anziché la pagina. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_313001039F79446DB28C70D932AF5F58}

Questa situazione può verificarsi se l’URL contiene un carattere #. Per risolvere il problema, passa alla modalità Sfoglia nel Compositore esperienza visivo, quindi ritorna alla modalità Componi. L’icona che ruota scompare e la pagina viene caricata correttamente.

## Le intestazioni Content Security Policy (CSP) bloccano le librerie [!DNL Target] nel sito Web. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_89A30C7A213D43BFA0822E66B482B803}

Se le intestazioni CSP del tuo sito web bloccano le librerie di Target, quindi caricano il sito web ma ne impediscono la modifica, assicurati che le librerie di Target non siano bloccate.

>[!NOTE]
>
>Oltre alle seguenti informazioni, puoi utilizzare l’estensione [Adobe Target VEC Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) per il browser Google Chrome.

![immagine cps_headers](assets/cps_headers.png)

Come soluzione alternativa, è possibile configurare una regola con Requestly per rimuovere le intestazioni CSP, come illustrato di seguito:

![cps_headers_2 immagine](assets/cps_headers_2.png)

È possibile configurare con Requestly una regola simile per qualsiasi intestazione che impedisce il caricamento di una risorsa all&#39;interno del Compositore esperienza visivo.

Per Requestly, ogni volta che è necessario rimuovere le intestazioni, bisogna eseguire una delle seguenti operazioni:

* Aggiungere regole URL per l&#39;URL che si desidera aprire nel Compositore esperienza visivo in modo tale che le intestazioni vengano rimosse solo per tali URL.
* Abilitare la regola quando si effettuano modifiche nel Compositore esperienza visivo e disabilitarla quando non lo si utilizza.

## Il Compositore esperienza visivo o Compositore esperienza avanzato sembra non funzionare o non viene inizializzato quando si vuole modificare un&#39;attività già salvata. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_5AC3BA8F8FBB451EA814F298D0645E54}

Se il sito web è stato modificato al di fuori del Compositore esperienza visivo dopo la configurazione dell&#39;esperienza, non è possibile trovare i selettori su cui sono state eseguite le azioni in precedenza quando l&#39;attività viene riaperta per essere nuovamente modificata. La pagina apparentemente non funziona, senza che venga visualizzato alcun avviso.

## Il Compositore esperienza visivo o Compositore esperienza avanzato non mostra i miei banner rotanti e altri contenuti che contengono JavaScript. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_8B5BE6EB050B42D6A14A054724C41330}

Per impostazione predefinita, il Compositore esperienza visivo blocca gli elementi JavaScript. Per utilizzarli, disattiva JavaScript nelle impostazioni del Compositore esperienza visivo. In base alla configurazione del sito, alcuni elementi potrebbero continuare a essere visualizzati in modo non corretto o rimanere non disponibili.

## Alla modifica di un elemento della pagina, vengono modificati più elementi. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_309188ACF34942989BE473F63C5710AF}

Se lo stesso ID di elemento DOM è utilizzato in più elementi della pagina, la modifica di uno di questi elementi influenza tutti gli elementi con lo stesso ID. Per evitare il problema, è opportuno utilizzare ciascun ID solo una volta in ogni pagina. Questa è una best practice standard per i HTML. Per ulteriori informazioni, vedere [Scenari di modifica delle pagine](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Non sono in grado di modificare le esperienze per un sito non compatibile con iFrame. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_9FE266B964314F2EB75604B4D7047200}

Questo problema può essere affrontato abilitando il Compositore esperienza avanzato. Fai clic su **[!UICONTROL Administation]** > **[!UICONTROL Visual Experience Composer]**, quindi seleziona la casella di controllo che abilita il Compositore esperienza avanzato. Il Compositore esperienza avanzato utilizza un proxy gestito da Adobe per caricare la pagina da modificare. Questo proxy consente la modifica su siti non compatibili con iFrame e la modifica su siti e pagine in cui non è stato ancora aggiunto il codice Adobe Target. Le attività non vengono fornite al sito fino all&#39;aggiunta del codice. È possibile che alcuni siti non vengano caricati tramite il Compositore esperienza avanzato. In questo caso, deseleziona questa opzione per caricare il Compositore esperienza visivo tramite un iFrame.

>[!NOTE]
>
>Le pagine ospitate localmente o le pagine che non sono accessibili all’esterno della rete non sono accessibili al server proxy Adobe e non possono essere aperte nel Compositore esperienza avanzato. Queste pagine potrebbero includere gli URL di staging, i test di accettazione degli utenti (TAU) o le pagine in hosting locale.

## Desidero configurare test su pagine che per ora sono prive dell&#39;implementazione mbox/target. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_DE63BCCB5B124E10A71FA579B582A80A}

Vedi “Non sono in grado di modificare le esperienze per un sito non compatibile con iFrame” più sopra.

## Gli stili di testo in grassetto e corsivo con Modifica testo/HTML o Cambia testo/HTML non vengono visualizzati sulla mia pagina. A volte il testo scompare dopo l&#39;applicazione di queste modifiche. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_7A71D6DF41084C58B34C18701E8774E5}

Se si utilizza **[!UICONTROL Edit Text/HTML]** nel Compositore esperienza visivo per A/B o le attività di targeting per l&#39;esperienza o **[!UICONTROL Change Text/HTML]** per Automated Personalization o per attività di test multivariato per rendere il testo in grassetto o corsivo, questi stili potrebbero non essere applicati nella pagina o il testo potrebbe scomparire dalla pagina nel Compositore esperienza visivo. Ciò si verifica a causa del modo in cui l’editor Rich Text applica questi stili potrebbero interferire con il markup del sito web.

Se vedi questo problema:

1. Fare clic sul pulsante **[!UICONTROL HTML]** nell&#39;editor Rich Text per accedere alla modalità di modifica della sorgente.
1. Trova gli elementi di stile di testo.

   * Per il testo in grassetto, modifica gli elementi `<strong>` in `<b>`.

   * Per il testo in corsivo, modifica gli elementi `<em>` in `<i>`.

## Per le attività di personalizzazione automatizzata, lo scambio di immagini nel Compositore esperienza visivo e Compositore esperienza avanzato sembra non funzionare. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_88AABFDFE6A3420299B0D508B12A3994}

L&#39;aggiunta dell&#39;offerta di un immagine a una posizione prende la dimensione totale dello spazio immagine originale nel Compositore esperienza visivo e Compositore esperienza avanzato. Alla consegna, l&#39;immagine non viene espansa ed è mostrata così com&#39;è, quindi non c&#39;è impatto sulla consegna.
