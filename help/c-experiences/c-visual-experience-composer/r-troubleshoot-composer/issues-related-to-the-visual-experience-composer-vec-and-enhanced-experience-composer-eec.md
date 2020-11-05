---
keywords: Targeting;visual experience composer;whitelist;white list;allowlist;allow list;enhanced visual experience composer;vec;troubleshoot visual experience composer;troubleshooting;eec;enhanced experience composer;tls;tls 1.2
description: In determinate condizioni si possono verificare problemi di visualizzazione nel Compositore esperienza visivo e nel Compositore esperienza avanzato.
title: Risoluzione dei problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato
feature: vec
uuid: 93f646d9-fcbc-43f0-9f84-0ce8e486ff7f
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '1370'
ht-degree: 68%

---


# Risoluzione dei problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato{#troubleshooting-issues-related-to-the-visual-experience-composer-and-enhanced-experience-composer}

Problemi di visualizzazione e altri problemi possono verificarsi in Visual Experience Composer (VEC) e Enhanced Experience Composer (EEC) a determinate condizioni.

## In che modo le politiche di applicazione dei cookie Google Chrome SameSite recentemente annunciate influiscono sul VEC e CEE? {#samesite}

Con le ultime modifiche (agosto 2020), tutti gli utenti con Chrome 80+ versioni del browser:

* *Non* sarà possibile utilizzare il VEC (con o senza l&#39;estensione VEC Helper installata e attivata) nelle pagine protette da password dei loro siti. Questo perché i cookie di accesso al sito verranno considerati cookie di terze parti e non verranno inviati con la richiesta di accesso. L&#39;unica eccezione è rappresentata dal caso in cui il cookie di login del sito cliente abbia già il parametro SameSite impostato su &quot;none&quot;.
* *Non* sarà possibile scaricare [!DNL Target] le librerie durante la modifica di un&#39;attività (se non sono già sul sito). Questo perché la chiamata di download viene effettuata dal dominio del cliente verso un dominio di Adobe  protetto e viene rifiutata come non autenticata.
* La CEE *non* funziona per tutti gli utenti perché non è in grado di impostare l&#39;attributo SameSite per i cookie su `adobemc.com domain`. Senza questo attributo, il browser rifiuterà questi cookie, causando il fallimento della CEE.

 Adobe ha inviato un&#39;estensione VEC Helper aggiornata a Google Chrome Store. Questa estensione sovrascrive gli attributi del cookie per impostare l’ `SameSite="none"` attributo, se necessario. L&#39;estensione [aggiornata è disponibile qui](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak?hl=en). Per ulteriori informazioni sull&#39;installazione e l&#39;utilizzo dell&#39;estensione VEC Helper, consultate Estensione [helper di](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)Visual Experience Composer (Compositore esperienza visivo).

Per i cookie del tuo sito, devi specificare i cookie per nome. Attiva il cursore [!UICONTROL Cookie] , quindi specifica il cookie per nome e il dominio del cookie. Il nome del cookie è &quot;mbox&quot; e il dominio del cookie è il secondo e il primo livello dei domini da cui viene distribuita la mbox. Dato che viene distribuito dal dominio della società, il cookie è un cookie dei siti Web visualizzati. Esempio: `mycompany.com`. Per ulteriori informazioni, vedere [Cookie](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-target.html) Adobe Target nella Guida *utente dell&#39;interfaccia di* Experience Cloud.

![I cookie si attivano nell&#39;estensione del supporto VEC](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

### Alternative e soluzioni alternative

Utilizzare una delle seguenti opzioni per garantire che il VEC e la CEE continui a funzionare come previsto:

* Scaricate e utilizzate l&#39;estensione [](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak?hl=en)VEC Helper aggiornata.
* Utilizzate il browser Mozilla Firefox. Firefox non ha ancora applicato questo criterio.
* Continuate a utilizzare Chrome, ma impostate il `chrome://flags/#same-site-by-default-cookies` flag su &quot;Disattivato&quot;.

   >[!NOTE]
   >
   >Questo *non* sarà sufficiente se i cookie hanno già l&#39;attributo SameSite impostato su &quot;Lax&quot; o &quot;Strict&quot; dal server.

## Target supporta gli iframe a più livelli?

Target non supporta gli iframe a più livelli. Se il sito web carica un iframe contenente un iframe secondario, le librerie di Target (at.js e mbox.js) interagiscono solo con l’iframe principale. Le librerie di Target non interagiscono con l’iframe secondario.

Come soluzione alternativa, puoi aggiungere all’esperienza una pagina con l’URL dell’iframe secondario.

## Quando si tenta di modificare una pagina, compare solo un’icona che ruota anziché la pagina. (Compositore esperienza visivo e Compositore esperienza avanzato) {#section_313001039F79446DB28C70D932AF5F58}

Questo può avvenire se l&#39;URL contiene un carattere #. Per risolvere il problema, passa alla modalità Sfoglia nel Compositore esperienza visivo, quindi ritorna alla modalità Componi. L’icona che ruota scompare e la pagina viene caricata correttamente.

## Le intestazioni Content Security Policy (CSP) bloccano le librerie di Target nel mio sito web. (Compositore esperienza visivo e Compositore esperienza avanzato) {#section_89A30C7A213D43BFA0822E66B482B803}

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

## Il Compositore esperienza visivo o Compositore esperienza avanzato sembra non funzionare o non viene inizializzato quando si vuole modificare un&#39;attività già salvata. (Compositore esperienza visivo e Compositore esperienza avanzato) {#section_5AC3BA8F8FBB451EA814F298D0645E54}

Se il sito web è stato modificato al di fuori del Compositore esperienza visivo dopo la configurazione dell&#39;esperienza, non è possibile trovare i selettori su cui sono state eseguite le azioni in precedenza quando l&#39;attività viene riaperta per essere nuovamente modificata. La pagina apparentemente non funziona, senza che venga visualizzato alcun avviso.

## Il Compositore esperienza visivo o Compositore esperienza avanzato non mostra i miei banner rotanti e altri contenuti che contengono JavaScript. (Compositore esperienza visivo e Compositore esperienza avanzato) {#section_8B5BE6EB050B42D6A14A054724C41330}

Per impostazione predefinita, il Compositore esperienza visivo blocca gli elementi JavaScript. Per utilizzarli, disattiva JavaScript nelle impostazioni del Compositore esperienza visivo. In base alla configurazione del sito, alcuni elementi potrebbero continuare a essere visualizzati in modo non corretto o rimanere non disponibili.

## Impossibile caricare il file target.js in hosting nei successivi ricaricamenti delle pagine. (Compositore esperienza visivo e Compositore esperienza avanzato) {#section_87F6418C2CD142A7B4D1E7037935F81F}

Questo problema si verifica quando i clienti hanno una versione di mbox.js precedente alla 57 (vale a dire la versione 56 o precedente).

È consigliabile che tutti gli utenti del Compositore esperienza visivo effettuino l’aggiornamento alla [versione più recente di mbox. js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A) oppure che eseguano almeno l’aggiornamento alla versione 57. È inoltre consigliabile [effettuare la transizione a at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17).

## Alla modifica di un elemento della pagina, vengono modificati più elementi. (Compositore esperienza visivo e Compositore esperienza avanzato) {#section_309188ACF34942989BE473F63C5710AF}

Se lo stesso ID di elemento DOM è utilizzato in più elementi della pagina, la modifica di uno di questi elementi influenza tutti gli elementi con lo stesso ID. Per evitare il problema, è opportuno utilizzare ciascun ID solo una volta in ogni pagina. Questa è una best practice HTML standard. Per ulteriori informazioni, consulta [Scenari di modifica delle pagine](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Non sono in grado di modificare le esperienze per un sito non compatibile con iFrame. (Compositore esperienza visivo e Compositore esperienza avanzato) {#section_9FE266B964314F2EB75604B4D7047200}

Questo problema può essere affrontato abilitando il Compositore esperienza avanzato. Click **[!UICONTROL Administation]** > **[!UICONTROL Visual Experience Composer]**, then select the check box that enables the Enhanced Experience Composer. Il Compositore esperienza avanzato utilizza un proxy gestito da Adobe per caricare la pagina da modificare. Questo consente la modifica su siti non compatibili con iFrame e su siti e pagine cui non è ancora stato aggiunto il codice di Adobe Target. Le attività non vengono fornite al sito fino all&#39;aggiunta del codice. È possibile che alcuni siti non vengano caricati tramite il Compositore esperienza avanzato. In questo caso, deseleziona questa opzione per caricare il Compositore esperienza visivo tramite un iFrame. []

>[!NOTE]
>
>Le pagine ospitate localmente o le pagine che non sono accessibili all’esterno della rete non sono accessibili al server proxy Adobe e non possono essere aperte nel Compositore esperienza avanzato. Queste pagine potrebbero includere gli URL di staging, i test di accettazione degli utenti (TAU) o le pagine in hosting locale.

## Desidero configurare test su pagine che per ora sono prive dell&#39;implementazione mbox/target. (Compositore esperienza visivo e Compositore esperienza avanzato) {#section_DE63BCCB5B124E10A71FA579B582A80A}

Vedi “Non sono in grado di modificare le esperienze per un sito non compatibile con iFrame” più sopra.

## Gli stili di testo in grassetto e corsivo con Modifica testo/HTML o Cambia testo/HTML non vengono visualizzati sulla mia pagina. A volte il testo scompare dopo l&#39;applicazione di queste modifiche. (Compositore esperienza visivo e Compositore esperienza avanzato) {#section_7A71D6DF41084C58B34C18701E8774E5}

Se si utilizza **[!UICONTROL Modifica testo/HTML]** nel Compositore esperienza visivo per A/B o le attività di targeting per l&#39;esperienza o **[!UICONTROL Cambia testo/HTML]** per la personalizzazione automatizzata o per attività di test multivariato per rendere il testo in grassetto o corsivo, questi stili potrebbero non essere applicati nella pagina o il testo potrebbe scomparire dalla pagina nel Compositore esperienza visivo. Questo perché il modo in cui l&#39;editor rich-text applica questi stili potrebbe interferire con il markup del sito web.

Se vedi questo problema:

1. Fai clic sul pulsante **[!UICONTROL HTML]** nell&#39;editor rich-text per accedere alla modalità di modifica della sorgente.
1. Trova gli elementi di stile di testo.

   * Per il testo in grassetto, modifica gli elementi `<strong>` in `<b>`.

   * Per il testo in corsivo, modifica gli elementi `<em>` in `<i>`.

## Per le attività di personalizzazione automatizzata, lo scambio di immagini nel Compositore esperienza visivo e Compositore esperienza avanzato sembra non funzionare. (Compositore esperienza visivo e Compositore esperienza avanzato) {#section_88AABFDFE6A3420299B0D508B12A3994}

L&#39;aggiunta dell&#39;offerta di un immagine a una posizione prende la dimensione totale dello spazio immagine originale nel Compositore esperienza visivo e Compositore esperienza avanzato. Alla consegna, l&#39;immagine non viene espansa ed è mostrata così com&#39;è, quindi non c&#39;è impatto sulla consegna.
