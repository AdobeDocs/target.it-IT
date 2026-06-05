---
keywords: qa;modalità qa; qa attività;qa url;qa url;anteprima url;anteprima url
description: Scopri come utilizzare gli URL di controllo qualità di Adobe [!DNL Target] per eseguire in modo semplice e completo il controllo qualità delle attività con collegamenti di anteprima che restano invariati, targeting facoltativo del pubblico e rapporti di controllo qualità mantenuti segmentati dai dati delle attività live.
title: Come posso eseguire il controllo qualità delle attività?
feature: Activities
exl-id: 5c606d61-6d13-4a9b-9a23-4840f1754d3c
TQID: https://experienceleague.adobe.com/glE1Kx2xhqagq9v-SgSkdwr6lYwpioe4DlSkLRFQ0jI
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1815
ht-degree: 27%

---

# Controllo di qualità delle attività

Gli URL di controllo qualità in [!DNL Adobe Target] consentono di verificare in modo semplice e completo la qualità delle attività tramite collegamenti di anteprima che restano invariati, l&#39;eventuale definizione di un pubblico di destinazione e rapporti di controllo qualità mantenuti separati dai dati delle attività live.

[!UICONTROL Controllo qualità attività] consente di testare completamente le attività [!DNL Target] prima di avviarle in tempo reale. La funzionalità [!UICONTROL Controllo qualità attività] include:

* Collegamenti da condividere con i membri del team che non devono essere modificati o rigenerati, indipendentemente dagli aggiornamenti apportati alle esperienze o alle attività. Questa funzione consente di testare completamente le attività in tutto il percorso di utenti.
* Possibilità di rispettare o meno le condizioni di pubblico, per testare i criteri di targeting o per ignorarli al fine di verificare come si presentano le esperienze senza dover soddisfare le condizioni di pubblico.
* Il rapporto di controllo qualità viene acquisito per permettere agli addetti al marketing di confermare che le metriche aumentano come previsto, e i relativi dati sono tenuti separati dai rapporti di produzione (per la generazione di rapporti non A4T).
* Possibilità di visualizzare in anteprima un&#39;esperienza in isolamento o con altre attività live che soddisfano i criteri di consegna (pagina/[!DNL Target] richiesta/pubblico).
* Capacità di eseguire il controllo qualità sull’intero percorso dell’utente. Puoi accedere al tuo sito una volta con il collegamento di controllo qualità e quindi navigare nell’intero sito in modalità di controllo qualità dell’attività. Resterai in Controllo qualità attività fino alla fine della sessione o fino a quando non utilizzi il bookmarklet [Controllo qualità di Target](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) per uscire dalla [!UICONTROL Controllo qualità attività]. Questa funzione è utile se hai un’attività che si estende su più pagine web.

  >[!NOTE]
  >
  >Questa funzionalità è valida per le implementazioni di at.js con versione 2.*x* o successiva. Per le implementazioni di at.js 1.*x*, questa funzionalità è true solo se il browser del visitatore non blocca i cookie di terze parti.

## Accesso e condivisione di un URL di controllo qualità {#section_1C59BAA247B247BDB125D1BE8EAD4547}

1. Dalla pagina [!UICONTROL Panoramica] di un&#39;attività, fai clic su **[!UICONTROL Controllo qualità attività]**.

1. Configura le seguenti impostazioni:

   * **[!UICONTROL Abbina le regole del pubblico per visualizzare le esperienze]:** A volte puoi voler verificare che la corrispondenza del pubblico funzioni. Altre volte si desidera controllare l&#39;aspetto dell&#39;attività. Se questa impostazione viene attivata, i soggetti del test devono soddisfare i requisiti di targeting per risultare idonei a visualizzare le esperienze. Per le attività di targeting di esperienza (XT), viene fornito un singolo URL di attività. Se il visitatore soddisfa le regole di targeting, l’esperienza verrà visualizzata.

     Se questa impostazione è disattivata, quando si fa clic sui collegamenti le esperienze vengono sempre visualizzate, anche se le regole non sono soddisfatte. Durante il controllo qualità, puoi attivare e disattivare questa opzioni per richiedere o ignorare il rispetto delle regole di targeting del pubblico.

   * **Mostra contenuto predefinito per tutte le altre attività:** Se questa opzione è attivata, il contenuto predefinito viene visualizzato per tutte le altre attività. Ad esempio, l&#39;anteprima viene visualizzata in isolamento senza considerare tutte le altre attività live nella stessa richiesta di pagina/[!DNL Target].

     Se questa impostazione è disattivata, considera quanto segue:

      * Se ci sono conflitti tra l&#39;attività che stai testando e altre attività live, vengono applicate [le normali regole di priorità](/help/main/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F). A causa di conflitti, è possibile che non riesca a visualizzare l’attività di cui intendi eseguire il controllo qualità.
      * Le metriche vengono incrementate per le attività visualizzate, ma solo nell’ambiente di reporting ai fini del controllo qualità.

1. Fai clic su **[!UICONTROL Fine]** per salvare le modifiche.
1. Condividi gli URL di collegamento dell’attività con i membri della tua organizzazione per il test.

   I collegamenti alle attività non scadono mai e non è necessario inviarli di nuovo se qualcuno cambia un’attività o un’esperienza. Tuttavia, se applichi un pubblico diverso dalla [!UICONTROL Libreria tipi di pubblico], invece di modificare semplicemente l&#39;attività, viene generato un nuovo collegamento che devi condividere di nuovo.

   Ogni URL di collegamento di attività (per Esperienza A, Esperienza B e così via) consente di avviare il percorso di utenti dall’esperienza corrispondente. Fai clic sull’URL generato per un’esperienza, quindi procedi alla normale navigazione del sito per visualizzare le esperienze su più pagine (se esistono più pagine). Per ogni esperienza viene generato un solo URL, anche se l’esperienza si estende su più pagine (test di modelli o test multipagina).

   È possibile spostarsi nel sito per visualizzare le altre pagine perché la modalità di controllo qualità [!UICONTROL Attività] è permanente. Questa situazione si verifica per le implementazioni di at.js con versione 2.*x* o successiva. Per le implementazioni di at.js 1.*x*, questa situazione si verifica solo se il browser del visitatore non blocca i cookie di terze parti.

1. Per visualizzare i report generati dagli URL di collegamento dell&#39;attività, fai clic sulla pagina **[!UICONTROL Report]** dell&#39;attività, poi sull&#39;icona **[!UICONTROL Impostazioni]** (![icona_ingranaggio](assets/icon_gear.png) ), quindi seleziona **[!UICONTROL Traffico modalità Controllo di qualità]** dall&#39;elenco a discesa **[!UICONTROL Ambiente]**.

## Rilascio dalla modalità di controllo qualità

[!UICONTROL Il Controllo di qualità attività] è permanente. Dopo aver navigato in un sito Web in [!UICONTROL Controllo di qualità attività], la sessione di [!DNL Target] deve scadere o è necessario disporre di [!DNL Target] per il rilascio da [!UICONTROL Controllo di qualità attività] prima di poter visualizzare il sito come un normale visitatore.

### at.js 2.*x*

Se nel tuo sito è stato implementato at.js 2.*x*, utilizza il [bookmarklet di controllo qualità di Target](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) per uscire dalla [!UICONTROL verifica qualità attività]. Il caricamento di una pagina del sito con un valore vuoto, come descritto nel punto successivo, *non* rimuove il cookie di controllo qualità dal browser quando viene distribuito at.js 2.*x*.

### at.js 1.*x*

Se nel tuo sito è stato implementato at.js 1.*x*, oltre a utilizzare il [bookmarklet di controllo qualità di Target](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879), puoi anche forzare manualmente la chiusura caricando una pagina del tuo sito con il parametro `at_preview_token` con un valore vuoto. Ad esempio,

`https://www.mysite.com/?at_preview_token=`

### [!DNL Adobe Experience Platform Web SDK]

Se nel sito è implementato [[!UICONTROL Platform Web SDK]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=it){target=_blank}, è possibile forzare manualmente l&#39;uscita caricando una pagina del sito con il parametro `at_qa_mode` con un valore vuoto. Ad esempio,

`https://www.mysite.com/?at_qa_mode=`

## Considerazioni {#section_B256EDD7BFEC4A6DA72A8A6ABD196D78}

* Poiché il Controllo di qualità attività è ora disponibile per tutti i tipi di attività [!DNL Target], la funzione &quot;Anteprima attività Automated Personalization con URL di anteprima esperienza&quot; non è più necessaria.
* [!UICONTROL I collegamenti di anteprima Controllo di qualità attività] per le attività salvate potrebbero non venire caricati se nel tuo account sono presenti troppe attività salvate. Riprovare i collegamenti di anteprima. Per evitare che questa situazione continui a verificarsi, archivia le attività salvate che non vengono più utilizzate attivamente.
* [!UICONTROL Gli URL di controllo qualità attività] sono disponibili con le attività con [Analytics come origine per la generazione di rapporti](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T). Gli hit generati durante il controllo qualità utilizzando [!UICONTROL Controllo qualità attività] fluiscono nella stessa suite di rapporti in cui i dati dell&#39;attività fluiscono anche dopo che l&#39;attività è diventata attiva.
* [!UICONTROL Il Controllo di qualità attività] non visualizza il contenuto per le attività archiviate o le attività che sono scadute. Se si disattiva un&#39;attività terminata, è necessario salvare nuovamente l&#39;attività affinché [!UICONTROL Controllo di qualità attività] funzioni.
* Le attività importate in [!DNL Target Standard/Premium] (ad esempio da [!DNL Target Classic]) non supportano gli URL di controllo qualità.
* Nelle attività [!UICONTROL Allocazione automatica] e [!UICONTROL Consigli], il modello non è interessato dalle visite acquisite in [!UICONTROL Controllo qualità attività].
* Se hai specificato un URL durante la creazione di [perfezionamenti dell&#39;attività nel Compositore basato su modulo](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) o [opzioni di consegna pagine nel Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81), l&#39;URL del controllo qualità non funziona perché [!UICONTROL Controllo qualità attività] aggiunge parametri all&#39;URL. Per risolvere questo problema, fai clic su URL di controllo qualità per passare al sito, rimuovi dall’URL i parametri aggiunti, quindi carica il nuovo l’URL.
* Se disponi di at.js 1.*x*, la modalità [!UICONTROL Controllo qualità attività] non è definitiva se utilizzi Safari o un altro browser che blocca i cookie di terze parti. In questi casi, devi aggiungere i parametri di anteprima a ogni URL a cui vai. Lo stesso vale se hai implementato [CNAME](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/implement-cname-support-in-target.html){target=_blank}.
* Se un’attività utilizza più tipi di pubblico per le esperienze (ad esempio, se nella stessa attività sono inclusi un sito britannico e uno statunitense), i collegamenti di controllo qualità non vengono generati per le quattro combinazioni (Esperienza A/sito US, Esperienza A/sito UK, Esperienza B/sito US, Esperienza B/sito UK). Vengono creati solo due collegamenti di controllo qualità (Esperienza A ed Esperienza B) e la pagina verrà visualizzata dagli utenti che risultano idonei per il pubblico appropriato. Una persona che effettua il controllo qualità nel Regno Unito non può visualizzare il sito degli Stati Uniti.
* Tutti i parametri e i valori `at_preview` sono già codificati nell’URL. Nella maggior parte dei casi, tutto funziona come previsto. Tuttavia, alcuni clienti devono caricare bilanciatori o server Web che tentano di codificare nuovamente i parametri della stringa di query.

  A causa di questa doppia codifica, quando [!DNL Target] tenta di decodificare `at_preview_token`, [!DNL Target] non può estrarre il valore del token corretto. L&#39;anteprima non funziona.

  [!DNL Adobe] consiglia di parlare con il team IT per assicurarsi che tutti i parametri di anteprima siano inseriti nell&#39;elenco Consentiti in modo che tali valori non vengano trasformati in alcun modo.

  Nella tabella seguente sono elencati i parametri che possono essere inseriti nell&#39;elenco Consentiti nel dominio:

  | Parametro | Tipo | Valore | Descrizione |
  |--- |--- |--- |--- |
  | `at_preview_token` | Stringa crittografata | Obbligatorio; nessun valore predefinito | Un’entità crittografata che contiene l’elenco degli ID delle campagne che possono essere eseguiti in modalità di controllo qualità. |
  | `at_preview_index` | Stringa | Vuoto | Il formato del parametro è `<campaignIndex>` o `<campaignIndex>_< experienceIndex>`<br>Entrambi gli indici iniziano con 1. |
  | `at_preview_listed_activities_only` | Boolean (true/false) | Valore predefinito: false | Se “true”, vengono elaborate tutte le campagne specificate nei parametri `at_preview_index`.<br>Se “false”, vengono elaborate tutte le campagne della pagina, anche se non sono state specificate nel token di anteprima. |
  | `at_preview_evaluate_as_true_audience_ids` | Stringa | Vuoto | Elenco di ID segmento separati da underscore (&quot;_&quot;) che devono sempre (a livello di targeting e reporting) essere valutati come &quot;true&quot; nell&#39;ambito della richiesta [!DNL Target]. |
  | `_AT_Debug` | Stringa | Finestra o console | Log della console o nuova finestra. |
  | `adobe_mc_ref` |  |  | Passa l&#39;URL di riferimento della pagina predefinita alla nuova pagina. Se utilizzato con `AppMeasurement.js` versione 2.1 (o successiva), [!DNL Adobe Analytics] utilizza questo valore di parametro come URL di riferimento nella nuova pagina. |
  | `adobe_mc_sdid` |  |  | Passa [!DNL Supplemental Data Id] (SDID) e [!DNL Experience Cloud Org Id] dalla pagina predefinita alla nuova pagina. Il passaggio di questi ID consente a [!UICONTROL Analytics for Target] (A4T) di &quot;unire&quot; la richiesta [!DNL Target] nella pagina predefinita con la richiesta [!DNL Analytics] nella nuova pagina. |

* L&#39;interfaccia utente della modalità di controllo qualità di [!UICONTROL Target] mostra solo il primo URL di un&#39;esperienza in un&#39;attività multipagina. Si presume infatti che si sta creando un test di percorso e si passa dall&#39;URL1 all&#39;URL2. Tuttavia, se desideri passare all’URL2 indipendentemente, copia tutti i parametri URL forniti per l’URL1 e applicali all’URL2 dopo aver inserito un segno &quot;?&quot;, come nell’URL1.
* I collegamenti di anteprima Controllo di qualità delle attività per le attività salvate potrebbero non venire caricati se nel tuo account sono presenti troppe attività salvate. Riprova i collegamenti di anteprima. Archivia le attività salvate che non vengono più utilizzate attivamente per impedire che questo problema continui a verificarsi.

## Compatibilità con la libreria JavaScript di destinazione [!UICONTROL Modalità Controllo di qualità] {#compatibility}

[!DNL Target] supporta le seguenti librerie JavaScript:

* [at.js 1.x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html)
* [at.js 2.x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html)
* [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=it)

Nella tabella seguente sono elencati i vari tipi di attività e viene indicato se la modalità di controllo qualità [!UICONTROL Attività] è supportata per ogni libreria:

| Tipo di attività | at.js 1.x | at.js 2.x | Platform Web SDK |
| --- | --- | --- | --- |
| [!UICONTROL Test A/B] | Sì | Sì | Sì |
| [!UICONTROL Allocazione automatica] | Sì | Sì | Sì |
| [!UICONTROL Targeting automatico] | Sì | Sì | Sì |
| [!UICONTROL Automated Personalization] (AP) | Sì | Sì | Sì |
| [!UICONTROL Targeting dell’esperienza] (XT) | Sì | Sì | Sì |
| [!UICONTROL Test multivariato] (MVT) | Sì | Sì | Sì |
| [!UICONTROL Funzione Consigli] | Sì | Sì | Sì |