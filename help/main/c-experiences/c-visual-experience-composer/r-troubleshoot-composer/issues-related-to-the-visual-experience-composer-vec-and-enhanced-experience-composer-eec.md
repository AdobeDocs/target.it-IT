---
keywords: Inserire nell'elenco Consentiti Targeting;compositore esperienza visivo;whitelist;whitelist;compositore;elenco consentiti;compositore esperienza visivo avanzato;vec;risoluzione dei problemi compositore esperienza visivo;risoluzione dei problemi;eec;esperienza avanzata;tls;tls 1.2
description: Scopri come risolvere i problemi che a volte si verificano nell’Adobe [!DNL Target] In determinate condizioni, il Compositore esperienza visivo e il Compositore esperienza avanzato.
title: Come posso risolvere i problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato?
feature: Visual Experience Composer (VEC)
exl-id: d829cd63-950f-4bb4-aa58-0247f85de383
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '1427'
ht-degree: 51%

---

# Risoluzione dei problemi relativi al [!UICONTROL Compositore esperienza visivo] e [!UICONTROL Compositore esperienza avanzato]

Talvolta si verificano problemi di visualizzazione e altri problemi in [!DNL Adobe Target] [!UICONTROL Compositore esperienza visivo] (VEC) e [!UICONTROL Compositore esperienza avanzato] (CEE) a determinate condizioni.

## In che modo i criteri di implementazione dei cookie SameSite di Google Chrome influiscono sul Compositore esperienza visivo e sul Compositore esperienza avanzato? {#samesite}

Tieni presente le modifiche che interessano il Compositore esperienza visivo e il Compositore esperienza avanzato quando utilizzi le seguenti versioni di Chrome:

>[!NOTE]
>
>La seguente modifica interessa tutti e tre gli aggiornamenti descritti di seguito:
>
> * Will *non* essere in grado di utilizzare il Compositore esperienza visivo senza che sia installata e abilitata l’estensione VEC Helper per le pagine dei siti protette da password. I cookie di accesso al sito sono considerati cookie di terze parti e non vengono inviati con richieste di accesso all’interno dell’editor del Compositore esperienza visivo in modalità Sfoglia. L’unica eccezione si verifica quando i cookie di accesso al sito presentano già il `SameSite=None` e `Secure` attributi impostati.


**Chrome 94 (21 settembre 2021)**: con le modifiche imminenti pianificate per la versione di Chrome 94 (21 settembre 2021), la seguente modifica influisce su tutti gli utenti con le versioni del browser Chrome 94+:

* Flag della riga di comando `--disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure` verrà rimosso.

**Chrome 91 (25 maggio 2021)**: con le modifiche implementate per la versione di Chrome 91 (25 maggio 2021), la seguente modifica influisce su tutti gli utenti con le versioni del browser Chrome 91+:

* I flag `#same-site-by-default-cookies` e `#cookies-without-same-site-must-be-secure` sono stati rimossi da `chrome://flags`. Questo comportamento è ora abilitato per impostazione predefinita.

**Chrome 80 (agosto 2020)**: con le modifiche implementate ad agosto 2020, tutti gli utenti con le versioni del browser Chrome 80+:

* Will *non* essere in grado di scaricare [!DNL Target] librerie durante la modifica di un’attività (quando non sono già presenti nel sito). Questo perché la chiamata di download viene effettuata dal dominio del cliente verso un [!DNL Adobe] e viene rifiutato in quanto non autenticato.
* Il CEE *non* per tutti gli utenti perché non è in grado di impostare l’attributo SameSite per i cookie su `adobemc.com domain`. Senza questo attributo, il browser rifiuta questi cookie, causando il mancato funzionamento del Compositore esperienza avanzato.

### Determinare quali cookie sono bloccati

Per determinare quali cookie sono bloccati a causa dei criteri di imposizione dei cookie SameSite, utilizza gli strumenti per sviluppatori in Chrome.

1. Per accedere agli strumenti per sviluppatori, durante la visualizzazione del Compositore esperienza visivo in Chrome, fai clic su **[!UICONTROL puntini di sospensione]** nell’angolo in alto a destra di Chrome > **[!UICONTROL Altri strumenti]** > **[!UICONTROL Strumenti per sviluppatori]**.
1. Fai clic su **[!UICONTROL Rete]** , quindi cerca i cookie bloccati.

   >[!NOTE]
   >
   >Utilizza il **[!UICONTROL Ha bloccato i cookie]** casella di controllo per facilitare la ricerca dei cookie bloccati.

   La figura seguente mostra un cookie bloccato:

   ![Strumenti per sviluppatori > Scheda Rete che mostra un cookie bloccato](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/chrome-developer-tools.png)

### [!DNL Adobe Target] Estensione VEC Helper

A partire dalla versione 0.7.1 di, [!DNL Adobe Target] L’estensione VEC Helper per il browser aggiunge `SameSite=None` e `Secure` attributi a tutti i cookie sulle risposte provenienti da pagine web modificate all’interno del Compositore esperienza visivo quando l’opzione &quot;Cookie&quot; è attivata nell’interfaccia utente dell’estensione:

![Interfaccia utente dell’estensione Adobe Target VEC Helper UIAdobe Target VEC Helper](assets/cookies-vec-helper.png)

### Alternative e soluzioni alternative

Utilizza una delle seguenti opzioni per garantire che il Compositore esperienza visivo e il Compositore esperienza avanzato continuino a funzionare come previsto:

* Scarica e utilizza il file aggiornato [Estensione VEC Helper](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak?hl=en).
* Utilizza il browser Mozilla Firefox. Firefox non sta ancora applicando questo criterio.
* Utilizza i seguenti flag per eseguire Google Chrome dalla riga di comando fino al 21 settembre 2021. Dopo il 21 settembre, le funzioni che richiedono i cookie non funzioneranno più nel Compositore esperienza visivo, come ad esempio le finestre a comparsa per il consenso di accesso o dei cookie. Se esegui l’aggiornamento a Chrome 94, devi generare manualmente i cookie con `SameSite=none` e `Secure` sui tuoi siti web.

   ```
   --disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure
   ```

## Does [!DNL Target] supporta gli iframe a più livelli?

[!DNL Target] non supporta gli iframe a più livelli. Se il sito web carica un iframe contenente un iframe secondario, at.js interagisce solo con l’iframe principale. [!DNL Target]Le librerie di non interagiscono con l’iframe secondario.

Come soluzione alternativa, puoi aggiungere all’esperienza una pagina con l’URL dell’iframe secondario.

## Quando si tenta di modificare una pagina, compare solo un’icona che ruota anziché la pagina. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_313001039F79446DB28C70D932AF5F58}

Questa situazione può verificarsi se l’URL contiene un carattere #. Per risolvere il problema, passa alla modalità Sfoglia nel Compositore esperienza visivo, quindi ritorna alla modalità Componi. L’icona che ruota scompare e la pagina viene caricata correttamente.

## Le intestazioni Content Security Policy (CSP) bloccano il [!DNL Target] librerie sul mio sito web. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_89A30C7A213D43BFA0822E66B482B803}

Se le intestazioni CSP del tuo sito web bloccano le librerie di Target, quindi caricano il sito web ma ne impediscono la modifica, assicurati che le librerie di Target non siano bloccate.

>[!NOTE]
>
>Oltre alle seguenti informazioni, puoi utilizzare l’estensione [Adobe Target VEC Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) per il browser Google Chrome.

![immagine cps_headers](assets/cps_headers.png)

Come soluzione alternativa, è possibile configurare una regola con Requestly per rimuovere le intestazioni CSP, come illustrato di seguito:

![immagine cps_headers_2](assets/cps_headers_2.png)

È possibile configurare con Requestly una regola simile per qualsiasi intestazione che impedisce il caricamento di una risorsa all&#39;interno del Compositore esperienza visivo.

Per Requestly, ogni volta che è necessario rimuovere le intestazioni, bisogna eseguire una delle seguenti operazioni:

* Aggiungere regole URL per l&#39;URL che si desidera aprire nel Compositore esperienza visivo in modo tale che le intestazioni vengano rimosse solo per tali URL.
* Abilitare la regola quando si effettuano modifiche nel Compositore esperienza visivo e disabilitarla quando non lo si utilizza.

## Il Compositore esperienza visivo o Compositore esperienza avanzato sembra non funzionare o non viene inizializzato quando si vuole modificare un&#39;attività già salvata. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_5AC3BA8F8FBB451EA814F298D0645E54}

Se il sito web è stato modificato al di fuori del Compositore esperienza visivo dopo la configurazione dell&#39;esperienza, non è possibile trovare i selettori su cui sono state eseguite le azioni in precedenza quando l&#39;attività viene riaperta per essere nuovamente modificata. La pagina apparentemente non funziona, senza che venga visualizzato alcun avviso.

## Il Compositore esperienza visivo o Compositore esperienza avanzato non mostra i miei banner rotanti e altri contenuti che contengono JavaScript. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_8B5BE6EB050B42D6A14A054724C41330}

Per impostazione predefinita, il Compositore esperienza visivo blocca gli elementi JavaScript. Per utilizzarli, disattiva JavaScript nelle impostazioni del Compositore esperienza visivo. In base alla configurazione del sito, alcuni elementi potrebbero continuare a essere visualizzati in modo non corretto o rimanere non disponibili.

## Alla modifica di un elemento della pagina, vengono modificati più elementi. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_309188ACF34942989BE473F63C5710AF}

Se lo stesso ID di elemento DOM è utilizzato in più elementi della pagina, la modifica di uno di questi elementi influenza tutti gli elementi con lo stesso ID. Per evitare il problema, è opportuno utilizzare ciascun ID solo una volta in ogni pagina. Questa è una best practice standard per i HTML. Per ulteriori informazioni, consulta [Scenari di modifica delle pagine](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Non sono in grado di modificare le esperienze per un sito non compatibile con iFrame. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_9FE266B964314F2EB75604B4D7047200}

Questo problema può essere affrontato abilitando il Compositore esperienza avanzato. Clic **[!UICONTROL Amministrazione]** > **[!UICONTROL Compositore esperienza visivo]**, quindi seleziona la casella di controllo che abilita il Compositore esperienza avanzato. Il Compositore esperienza avanzato utilizza un proxy gestito da Adobe per caricare la pagina da modificare. Questo proxy consente la modifica su siti non compatibili con iFrame e la modifica su siti e pagine in cui non è stato ancora aggiunto il codice Adobe Target. Le attività non vengono fornite al sito fino all&#39;aggiunta del codice. È possibile che alcuni siti non vengano caricati tramite il Compositore esperienza avanzato. In questo caso, deseleziona questa opzione per caricare il Compositore esperienza visivo tramite un iFrame.

>[!NOTE]
>
>Le pagine ospitate localmente o le pagine che non sono accessibili all’esterno della rete non sono accessibili al server proxy Adobe e non possono essere aperte nel Compositore esperienza avanzato. Queste pagine potrebbero includere gli URL di staging, i test di accettazione degli utenti (TAU) o le pagine in hosting locale.

## Desidero configurare test su pagine che per ora sono prive dell&#39;implementazione mbox/target. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_DE63BCCB5B124E10A71FA579B582A80A}

Vedi “Non sono in grado di modificare le esperienze per un sito non compatibile con iFrame” più sopra.

## Gli stili di testo in grassetto e corsivo con Modifica testo/HTML o Cambia testo/HTML non vengono visualizzati sulla mia pagina. A volte il testo scompare dopo l&#39;applicazione di queste modifiche. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_7A71D6DF41084C58B34C18701E8774E5}

Se si utilizza **[!UICONTROL Modifica testo/HTML]** nel Compositore esperienza visivo per A/B o le attività di targeting per l&#39;esperienza o **[!UICONTROL Cambia testo/HTML]** per la personalizzazione automatizzata o per attività di test multivariato per rendere il testo in grassetto o corsivo, questi stili potrebbero non essere applicati nella pagina o il testo potrebbe scomparire dalla pagina nel Compositore esperienza visivo. Ciò si verifica a causa del modo in cui l’editor Rich Text applica questi stili potrebbero interferire con il markup del sito web.

Se vedi questo problema:

1. Fai clic sul pulsante **[!UICONTROL HTML]** nell&#39;editor rich-text per accedere alla modalità di modifica della sorgente.
1. Trova gli elementi di stile di testo.

   * Per il testo in grassetto, modifica gli elementi `<strong>` in `<b>`.

   * Per il testo in corsivo, modifica gli elementi `<em>` in `<i>`.

## Per le attività di personalizzazione automatizzata, lo scambio di immagini nel Compositore esperienza visivo e Compositore esperienza avanzato sembra non funzionare. (Compositore esperienza visivo e Compositore esperienza avanzato)  {#section_88AABFDFE6A3420299B0D508B12A3994}

L&#39;aggiunta dell&#39;offerta di un immagine a una posizione prende la dimensione totale dello spazio immagine originale nel Compositore esperienza visivo e Compositore esperienza avanzato. Alla consegna, l&#39;immagine non viene espansa ed è mostrata così com&#39;è, quindi non c&#39;è impatto sulla consegna.
