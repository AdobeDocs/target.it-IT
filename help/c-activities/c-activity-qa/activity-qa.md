---
keywords: qa;modalità qa; qa attività;url qa;url qa;url di anteprima;url di anteprima
description: Scopri come utilizzare gli URL di controllo qualità di Adobe [!DNL Target] per eseguire attività di controllo qualità end-to-end in modo semplice, con collegamenti di anteprima che non cambiano mai, targeting di pubblico facoltativo e rapporti di controllo qualità mantenuti separati dai dati delle attività live.
title: Come Faccio A Controllare Le Attività?
feature: Attività
exl-id: 5c606d61-6d13-4a9b-9a23-4840f1754d3c
source-git-commit: ceb98a1f940bb4253aa75639b67f2277f25acbbd
workflow-type: tm+mt
source-wordcount: '1760'
ht-degree: 36%

---

# Controllo di qualità delle attività

Gli URL di controllo qualità in [!DNL Adobe Target] consentono di verificare in modo semplice e completo la qualità delle attività tramite collegamenti di anteprima che restano invariati, l’eventuale definizione di un pubblico di destinazione e rapporti di controllo qualità mantenuti separati dai dati delle attività live.

[!UICONTROL Il ] controllo qualità delle attività ti consente di testare completamente  [!DNL Target] le attività prima di avviarle in diretta. La funzionalità [!UICONTROL Controllo di qualità delle attività] include:

* Collegamenti da condividere con i membri del team che non cambiano mai o richiedono la rigenerazione, indipendentemente dagli aggiornamenti apportati alle esperienze o attività. Questa funzione consente di testare completamente le attività in tutto il percorso di utenti.
* Possibilità di rispettare o meno le condizioni di pubblico, per testare i criteri di targeting o per ignorarli al fine di verificare come si presentano le esperienze senza dover soddisfare le condizioni di pubblico.
* Il rapporto di controllo qualità viene acquisito per permettere agli addetti al marketing di confermare che le metriche aumentano come previsto, e i relativi dati sono tenuti separati dai rapporti di produzione (per la generazione di rapporti non A4T).
* Possibilità di visualizzare in anteprima un’esperienza in isolamento o con altre attività live che soddisfano i criteri di consegna (pagina/richiesta Target/pubblico).
* Capacità di eseguire il controllo qualità sull’intero percorso dell’utente. Puoi accedere al tuo sito una volta con il collegamento di controllo qualità e quindi navigare nell’intero sito in modalità di controllo qualità dell’attività. Resterai in tale modalità fino alla fine della sessione o fino a quando utilizzi il [Bookmarklet di controllo qualità di Target](/help/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879)[!UICONTROL  per uscire dalla modalità di controllo qualità dell’attività]. Questa funzione è utile se si dispone di un’attività che si estende su più pagine web.

   >[!NOTE]
   >
   >Questa funzionalità è valida per le implementazioni at.js con versione 2.** xor in seguito. Per at.js 1.** ximplementations, questa funzionalità è vera solo se il browser del visitatore non blocca i cookie di terze parti.

## Accesso e condivisione di un URL di controllo qualità {#section_1C59BAA247B247BDB125D1BE8EAD4547}

1. Dalla pagina [!UICONTROL Panoramica] di un&#39;attività, fai clic sul collegamento **[!UICONTROL Controllo di qualità delle attività]** .

   ![Collegamento Controllo di qualità attività](assets/qa_link.png)

1. Configura le seguenti impostazioni:

   ![Opzioni di configurazione del collegamento Controllo di qualità attività](assets/qa_link_config.png)

   * **[!UICONTROL Fai corrispondere le regole del pubblico per visualizzare le esperienze]:** a volte puoi voler verificare che la corrispondenza del pubblico funzioni. Altre volte puoi controllare l’aspetto dell’attività. Se questa impostazione viene attivata, i soggetti del test devono soddisfare i requisiti di targeting per risultare idonei a visualizzare le esperienze. Per le attività di targeting di esperienza (XT), viene fornito un singolo URL di attività. Se il visitatore soddisfa le regole di targeting, l’esperienza verrà visualizzata.

      Se questa impostazione è disattivata, quando si fa clic sui collegamenti le esperienze vengono sempre visualizzate, anche se le regole non sono soddisfatte. Durante il controllo qualità, puoi attivare e disattivare questa opzioni per richiedere o ignorare il rispetto delle regole di targeting del pubblico.

   * **Mostra contenuto predefinito per tutte le altre attività:** se questa opzione è attivata, viene visualizzato il contenuto predefinito per tutte le altre attività. Ad esempio, l’anteprima viene visualizzata in isolamento senza considerare tutte le altre attività live presenti nella stessa pagina/[!DNL Target] richiesta.

      Se questa impostazione è disattivata, considera quanto segue:

      * Se ci sono conflitti tra l’attività che stai testando e altre attività live, valgono le [normali regole di priorità](/help/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F). A causa di conflitti, è possibile che non sia possibile visualizzare l’attività che si intende eseguire al controllo qualità.
      * Le metriche vengono incrementate per le attività visualizzate, ma solo nell’ambiente di reporting ai fini del controllo qualità.

1. Fai clic su **[!UICONTROL Fine]** per salvare le modifiche.
1. Condividi gli URL di collegamento dell’attività con i membri dell’organizzazione a scopo di test.

   I collegamenti alle attività non scadono mai e non è necessario inviare nuovamente i collegamenti se un utente modifica un’attività o un’esperienza. Tuttavia, se applichi un pubblico diverso dalla [!UICONTROL Libreria tipi di pubblico], anziché semplicemente modificare l&#39;attività, viene generato un nuovo collegamento che devi condividere.

   Ogni URL di collegamento di un’attività (per l’esperienza A, l’esperienza B e così via) consente di avviare il percorso di utenti dall’esperienza corrispondente. Fai clic sull’URL generato per un’esperienza, quindi continua con la normale navigazione sul sito per visualizzare le esperienze su più pagine (se esistono più pagine). Per ogni esperienza viene generato un solo URL, anche se l’esperienza si estende su più pagine (test di modelli o test multipagina).

   Puoi navigare nel sito per vedere le altre pagine, perché la modalità [!UICONTROL Controllo qualità delle attività] è persistente. Questa situazione è vera per le implementazioni at.js con versione 2.** xor in seguito. Per at.js 1.** ximplementazioni, questa situazione è vera solo se il browser del visitatore non blocca i cookie di terze parti.

1. Per visualizzare i rapporti generati dagli URL di collegamento dell&#39;attività, fai clic sulla pagina **[!UICONTROL Rapporti]** dell&#39;attività, fai clic sull&#39;icona **[!UICONTROL Impostazioni]** ( ![](assets/icon_gear.png) ), quindi seleziona **[!UICONTROL Traffico in modalità QA]** dall&#39;elenco a discesa **[!UICONTROL Ambiente]**.

## Considerazioni {#section_B256EDD7BFEC4A6DA72A8A6ABD196D78}

* Il collegamento [!UICONTROL Controllo qualità attività] viene visualizzato nella pagina [!UICONTROL Panoramica] di tutti i tipi di attività eccetto [!UICONTROL Targeting automatico] e [!UICONTROL Automated Personalization] (AP).
* [!UICONTROL I collegamenti di anteprima Controllo di qualità delle attività per le attività salvate potrebbero non venire caricati se nel tuo account sono presenti troppe attività salvate. ] Il nuovo tentativo dei collegamenti di anteprima dovrebbe funzionare. Per evitare che questa situazione continui, archivia le attività salvate che non vengono più utilizzate attivamente.
* [!UICONTROL Gli URL controllo qualità delle attività sono disponibili per le attività in cui Analytics è impostato come origine per la creazione di rapporti (A4T). ] Gli hit generati durante l’esecuzione del controllo qualità utilizzando [!UICONTROL Controllo qualità attività] confluiscono nella stessa suite di rapporti in cui i dati dell’attività scorrono anche dopo che l’attività è diventata attiva.
* [!UICONTROL La funzione Controllo di qualità attività non visualizza i contenuti di attività archiviate o scadute. ] Se disattivi un&#39;attività terminata, devi salvare nuovamente l&#39;attività affinché [!UICONTROL Controllo qualità delle attività] funzioni.
* Le attività importate in [!DNL Target Standard/Premium] (ad esempio da [!DNL Target Classic]) non supportano gli URL di controllo qualità.
* Nelle attività [!UICONTROL Allocazione automatica] e [!UICONTROL Recommendations], le visite acquisite in [!UICONTROL Controllo qualità attività] non influiscono sul modello.
* [!UICONTROL Il ] controllo qualità delle attività è persistente. Dopo aver navigato su un sito web in [!UICONTROL Controllo di qualità delle attività], la sessione [!DNL Target] deve scadere o essere stato rilasciato [!DNL Target] da [!UICONTROL Controllo di qualità delle attività] prima di poter visualizzare il sito come un normale visitatore. Utilizza il bookmarklet [Controllo di qualità di Target](/help/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) per uscire da [!UICONTROL Controllo di qualità delle attività].

   Puoi anche forzare manualmente l’uscita dalla modalità di controllo qualità caricando una pagina del sito con il parametro `at_preview_token` con un valore vuoto (ad esempio, `https://www.mysite.com/?at_preview_token=`).

* Se hai specificato &quot;URL is&quot; durante la creazione dell&#39;attività [perfezionamenti nel Compositore basato su moduli](/help/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) o [opzioni di consegna pagina nel Compositore esperienza visivo)](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81), l&#39;URL di controllo qualità non funziona perché [!UICONTROL Controllo qualità attività] aggiunge parametri URL. Per risolvere questo problema, fai clic su URL di controllo qualità per passare al sito, rimuovi dall’URL i parametri aggiunti, quindi carica il nuovo l’URL.
* Se disponi di at.js 1.*x*,  [!UICONTROL Activity ] QAmode non è persistente se utilizzi Safari o un altro browser che blocca i cookie di terze parti. In questi casi, devi aggiungere i parametri di anteprima a ciascun URL a cui accedi. Lo stesso vale se hai implementato [CNAME](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md).
* Se un’attività utilizza più tipi di pubblico per le esperienze (ad esempio, un sito US e UK inclusi nella stessa attività), i collegamenti di controllo qualità non vengono generati per le quattro combinazioni (sito A/US, sito A/UK, sito B/US dell’esperienza, sito B/UK). Vengono creati solo due collegamenti di controllo qualità (Esperienza A ed Esperienza B) e la pagina verrà visualizzata dagli utenti che risultano idonei per il pubblico appropriato. Una persona di controllo qualità nel Regno Unito non può visualizzare il sito degli Stati Uniti.
* Tutti i parametri e i valori `at_preview` sono già codificati nell’URL. Nella maggior parte dei casi, tutto funziona come previsto. Tuttavia, alcuni clienti devono caricare bilanciatori o server Web che tentano di codificare nuovamente i parametri della stringa di query.

   A causa di questa doppia codifica, quando [!DNL Target] tenta di decodificare il `at_preview_token`, [!DNL Target] non può estrarre il valore corretto del token e l’anteprima non funziona.

   Adobe consiglia di parlare con il team IT per assicurarsi che tutti i parametri di anteprima siano inseriti nell&#39;elenco Consentiti in modo che tali valori non vengano trasformati in alcun modo.

   Nella tabella seguente sono elencati i parametri che possono essere inseriti nell&#39;elenco Consentiti nel dominio:

   | Parametro | Tipo | Valore | Descrizione |
   |--- |--- |--- |--- |
   | `at_preview_token` | Stringa crittografata | Obbligatorio; nessun valore predefinito | Un’entità cifrata che contiene l’elenco degli ID delle campagne che possono essere eseguiti in modalità Controllo qualità. |
   | `at_preview_index` | Stringa | Vuoto | Il formato del parametro è `<campaignIndex>` o `<campaignIndex>_< experienceIndex>`<br>Entrambi gli indici iniziano con 1. |
   | `at_preview_listed_activities_only` | Boolean (true/false) | Valore predefinito: false | Se “true”, vengono elaborate tutte le campagne specificate nei parametri `at_preview_index`.<br>Se “false”, vengono elaborate tutte le campagne della pagina, anche se non sono state specificate nel token di anteprima. |
   | `at_preview_evaluate_as_true_audience_ids` | Stringa | Vuoto | Elenco degli ID dei segmenti separati da underscore (&quot;_&quot;) che devono sempre (a livello di targeting e di reporting) essere valutati come &quot;true&quot; nell’ambito della richiesta [!DNL Target]. |
   | `_AT_Debug` | Stringa | Finestra o console | Log della console o nuova finestra. |
   | `adobe_mc_ref` |  |  | Passa l&#39;URL di riferimento della pagina predefinita alla nuova pagina. Se utilizzato con `AppMeasurement.js` versione 2.1 (o successiva), [!DNL Adobe Analytics] utilizza questo valore di parametro come URL di riferimento nella nuova pagina. |
   | `adobe_mc_sdid` |  |  | Passa i valori [!DNL Supplemental Data Id] (SDID) e [!DNL Experience Cloud Org Id] dalla pagina predefinita alla nuova pagina. Il passaggio di questi ID consente a [!UICONTROL Analytics for Target] (A4T) di &quot;unire&quot; la richiesta [!DNL Target] nella pagina predefinita con la richiesta [!DNL Analytics] nella nuova pagina. |

* L&#39;interfaccia utente [!UICONTROL Modalità di controllo qualità di Target] mostra solo il primo URL di un&#39;esperienza in un&#39;attività multipagina. Si presume infatti che si stia creando un test di percorso e che si passi dall’URL1 all’URL2. Tuttavia, se desideri passare all’URL2 indipendentemente, copia tutti i parametri URL forniti per l’URL1 e applicali all’URL2 dopo aver inserito un segno &quot;?&quot;, come nell’URL1.

## Compatibilità con la libreria JavaScript di Target [!UICONTROL Modalità QA] {#compatibility}

[!DNL Target] supporta le seguenti librerie JavaScript:

* [at.js 1.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)
* [at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)
* [Tutorial per Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md)

La tabella seguente elenca i vari tipi di attività e indica se la modalità [!UICONTROL Controllo qualità delle attività] è supportata per ogni libreria:

| Tipo di attività | at.js 1.x | at.js 2.x | SDK per web per Platform |
| --- | --- | --- | --- |
| [!UICONTROL Test A/B] | Sì | Sì | Sì |
| [!UICONTROL Allocazione automatica] | Sì | Sì | Sì |
| [!UICONTROL Targeting automatico] | No | No | No |
| [!UICONTROL Personalizzazione automatizzata] (AP) | No | No | No |
| [!UICONTROL Targeting esperienza] (XT) | Sì | Sì | Sì |
| [!UICONTROL Test multivariato] (MVT) | Sì | Sì | Sì |
| [!UICONTROL Recommendations] | Sì | Sì | Sì |

## URL di anteprima {#preview}

Gli URL di anteprima dell’esperienza possono essere generati per tutti i tipi di attività [!DNL Target]. Gli URL di anteprima consentono di visualizzare il contenuto dell’esperienza direttamente sul sito prima che l’attività sia attiva a scopo di anteprima e controllo qualità. Gli URL di anteprima dell’esperienza ignorano il targeting per forzare la visualizzazione di una particolare esperienza.

Per informazioni sul funzionamento degli URL di anteprima con le attività [!UICONTROL Automated Personalization] (AP), consulta [Anteprima delle attività Automated Personalization con URL di anteprima esperienza](/help/c-activities/t-automated-personalization/experience-preview.md).

Per accedere e condividere un URL di anteprima, dalla pagina **[!UICONTROL Panoramica]** di un&#39;attività, fai clic sul collegamento **[!UICONTROL Controllo qualità attività]** .

>[!NOTE]
>
>Il collegamento [!UICONTROL Controllo di qualità attività] e l&#39;URL di anteprima sono gli stessi per tutte le attività diverse dalle attività di Personalizzazione automatizzata [!DNL Target].

La tabella seguente elenca i vari tipi di attività e indica se la funzione URL di anteprima è supportata per ogni libreria o API:

| Tipo di attività | at.js 1.x | at.js 2.x | SDK per web per Platform |
| --- | --- | --- | --- |
| [!UICONTROL Test A/B] | Sì | Sì | Sì |
| [!UICONTROL Allocazione automatica] | Sì | Sì | Sì |
| [!UICONTROL Targeting automatico] | Sì | Sì | Sì |
| [!UICONTROL Personalizzazione automatizzata] (AP) | Sì | Sì | Sì |
| [!UICONTROL Targeting esperienza] (XT) | Sì | Sì | Sì |
| [!UICONTROL Test multivariato] (MVT) | Sì | Sì | Sì |
| [!UICONTROL Recommendations] | Sì | Sì | Sì |

