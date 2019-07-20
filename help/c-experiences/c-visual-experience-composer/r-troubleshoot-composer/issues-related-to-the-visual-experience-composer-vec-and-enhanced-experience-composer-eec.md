---
description: In determinate condizioni si possono verificare problemi di visualizzazione nel Compositore esperienza visivo e nel Compositore esperienza avanzato.
keywords: Targeting;compositore esperienza visivo;whitelist;white list;compositore esperienza visivo avanzato;VEC;risoluzione dei problemi del compositore esperienza visivo;risoluzione dei problemi;compositore esperienza avanzato;TLS;TLS 1.2
seo-description: In determinate condizioni si possono verificare problemi di visualizzazione nel Compositore esperienza visivo e nel Compositore esperienza avanzato.
seo-title: Risoluzione dei problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato
solution: Target
title: Risoluzione dei problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato
uuid: 93f646d9-fcbc-43f0-9f84-0ce8e486ff7f
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Risoluzione dei problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato{#troubleshooting-issues-related-to-the-visual-experience-composer-and-enhanced-experience-composer}

In determinate condizioni si possono verificare problemi di visualizzazione nel Compositore esperienza visivo e nel Compositore esperienza avanzato.

## Target supporta iframe a più livelli?

Target non supporta iframe a più livelli. Se il sito Web carica un iframe con un iframe secondario, le librerie Target (in. js e mbox. js) interagiscono solo con l'iframe principale. Le librerie di destinazione non interagiscono con l'iframe secondario.

Come soluzione alternativa, potete aggiungere una pagina nell'esperienza con l'URL dell'iframe secondario.

## Quando si tenta di modificare una pagina, compare solo un’icona che ruota anziché la pagina. (Compositore esperienza visivo e Compositore esperienza avanzato) {#section_313001039F79446DB28C70D932AF5F58}

Questo può avvenire se l'URL contiene un carattere #. Per risolvere il problema, passa alla modalità Sfoglia nel Compositore esperienza visivo, quindi ritorna alla modalità Componi. L’icona che ruota scompare e la pagina viene caricata correttamente.

## Le intestazioni Content Security Policy (CSP) bloccano le librerie di Target nel mio sito web. (Compositore esperienza visivo e Compositore esperienza avanzato) {#section_89A30C7A213D43BFA0822E66B482B803}

Se le intestazioni CSP del tuo sito web bloccano le librerie di Target, quindi caricano il sito web ma ne impediscono la modifica, assicurati che le librerie di Target non siano bloccate.

>[!NOTE]
>
>Oltre alle seguenti informazioni, puoi utilizzare l’estensione [Adobe Target VEC Helper](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) per il browser Google Chrome.

![](assets/cps_headers.png)

Come soluzione alternativa, è possibile configurare una regola con Requestly per rimuovere le intestazioni CSP, come illustrato di seguito:

![](assets/cps_headers_2.png)

È possibile configurare con Requestly una regola simile per qualsiasi intestazione che impedisce il caricamento di una risorsa all'interno del Compositore esperienza visivo.

Per Requestly, ogni volta che è necessario rimuovere le intestazioni, bisogna eseguire una delle seguenti operazioni:

* Aggiungere regole URL per l'URL che si desidera aprire nel Compositore esperienza visivo in modo tale che le intestazioni vengano rimosse solo per tali URL.
* Abilitare la regola quando si effettuano modifiche nel Compositore esperienza visivo e disabilitarla quando non lo si utilizza.

## Il Compositore esperienza visivo o Compositore esperienza avanzato sembra non funzionare o non viene inizializzato quando si vuole modificare un'attività già salvata. (Compositore esperienza visivo e Compositore esperienza avanzato) {#section_5AC3BA8F8FBB451EA814F298D0645E54}

Se il sito web è stato modificato al di fuori del Compositore esperienza visivo dopo la configurazione dell'esperienza, non è possibile trovare i selettori su cui sono state eseguite le azioni in precedenza quando l'attività viene riaperta per essere nuovamente modificata. La pagina apparentemente non funziona, senza che venga visualizzato alcun avviso.

## Il Compositore esperienza visivo o Compositore esperienza avanzato non mostra i miei banner rotanti e altri contenuti che contengono JavaScript. (Compositore esperienza visivo e Compositore esperienza avanzato) {#section_8B5BE6EB050B42D6A14A054724C41330}

Per impostazione predefinita, il Compositore esperienza visivo blocca gli elementi JavaScript. Per utilizzarli, disattiva JavaScript nelle impostazioni del Compositore esperienza visivo. In base alla configurazione del sito, alcuni elementi potrebbero continuare a essere visualizzati in modo non corretto o rimanere non disponibili.

## Impossibile caricare il file target.js in hosting nei successivi ricaricamenti delle pagine. (Compositore esperienza visivo e Compositore esperienza avanzato) {#section_87F6418C2CD142A7B4D1E7037935F81F}

Questo problema si verifica quando i clienti hanno una versione di mbox.js precedente alla 57 (vale a dire la versione 56 o precedente).

È consigliabile che tutti gli utenti del Compositore esperienza visivo effettuino l’aggiornamento alla [versione più recente di mbox. js](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A) oppure che eseguano almeno l’aggiornamento alla versione 57. È inoltre consigliabile [effettuare la transizione a at.js](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17).

## Alla modifica di un elemento della pagina, vengono modificati più elementi. (Compositore esperienza visivo e Compositore esperienza avanzato) {#section_309188ACF34942989BE473F63C5710AF}

Se lo stesso ID di elemento DOM è utilizzato in più elementi della pagina, la modifica di uno di questi elementi influenza tutti gli elementi con lo stesso ID. Per evitare il problema, è opportuno utilizzare ciascun ID solo una volta in ogni pagina. Questa è una best practice HTML standard. Per ulteriori informazioni, consulta [Scenari di modifica delle pagine](../../../c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Non sono in grado di modificare le esperienze per un sito non compatibile con iFrame. (Compositore esperienza visivo e Compositore esperienza avanzato) {#section_9FE266B964314F2EB75604B4D7047200}

Questo problema può essere affrontato abilitando il Compositore esperienza avanzato. Fai clic su **[!UICONTROL Configurazione]** &gt; **[!UICONTROL Preferenze]**, quindi seleziona la casella di controllo che abilita il Compositore esperienza avanzato. Il Compositore esperienza avanzato utilizza un proxy gestito da Adobe per caricare la pagina da modificare. Questo consente la modifica su siti non compatibili con iFrame e su siti e pagine cui non è ancora stato aggiunto il codice di Adobe Target. Le attività non vengono fornite al sito fino all'aggiunta del codice. È possibile che alcuni siti non vengano caricati tramite il Compositore esperienza avanzato. In questo caso, deseleziona questa opzione per caricare il Compositore esperienza visivo tramite un iFrame. []

>[!NOTE]
>
>Le pagine ospitate localmente o le pagine che non sono accessibili all’esterno della rete non sono accessibili al server proxy Adobe e non possono essere aperte nel Compositore esperienza avanzato. Queste pagine potrebbero includere gli URL di staging, i test di accettazione degli utenti (TAU) o le pagine in hosting locale.

## Desidero configurare test su pagine che per ora sono prive dell'implementazione mbox/target. (Compositore esperienza visivo e Compositore esperienza avanzato) {#section_DE63BCCB5B124E10A71FA579B582A80A}

Vedi “Non sono in grado di modificare le esperienze per un sito non compatibile con iFrame” più sopra.

## Gli stili di testo in grassetto e corsivo con Modifica testo/HTML o Cambia testo/HTML non vengono visualizzati sulla mia pagina. A volte il testo scompare dopo l'applicazione di queste modifiche. (Compositore esperienza visivo e Compositore esperienza avanzato) {#section_7A71D6DF41084C58B34C18701E8774E5}

Se si utilizza **[!UICONTROL Modifica testo/HTML]** nel Compositore esperienza visivo per A/B o le attività di targeting per l'esperienza o **[!UICONTROL Cambia testo/HTML]** per la personalizzazione automatizzata o per attività di test multivariato per rendere il testo in grassetto o corsivo, questi stili potrebbero non essere applicati nella pagina o il testo potrebbe scomparire dalla pagina nel Compositore esperienza visivo. Questo perché il modo in cui l'editor rich-text applica questi stili potrebbe interferire con il markup del sito web.

Se vedi questo problema:

1. Fai clic sul pulsante **[!UICONTROL HTML]** nell'editor rich-text per accedere alla modalità di modifica della sorgente.
1. Trova gli elementi di stile di testo.

   * Per il testo in grassetto, modifica gli elementi `<strong>` in `<b>`.

   * Per il testo in corsivo, modifica gli elementi `<em>` in `<i>`.

## Per le attività di personalizzazione automatizzata, lo scambio di immagini nel Compositore esperienza visivo e Compositore esperienza avanzato sembra non funzionare. (Compositore esperienza visivo e Compositore esperienza avanzato) {#section_88AABFDFE6A3420299B0D508B12A3994}

L'aggiunta dell'offerta di un immagine a una posizione prende la dimensione totale dello spazio immagine originale nel Compositore esperienza visivo e Compositore esperienza avanzato. Alla consegna, l'immagine non viene espansa ed è mostrata così com'è, quindi non c'è impatto sulla consegna.
