---
keywords: qa;modalità qa; qa attività;qa url;qa url;anteprima url;anteprima url
description: Scopri come utilizzare Adobe [!DNL Target] URL di controllo qualità per eseguire in modo semplice e completo il controllo qualità delle attività, con collegamenti di anteprima che restano invariati, targeting facoltativo del pubblico e rapporti di controllo qualità mantenuti segmentati dai dati delle attività live.
title: Come posso eseguire il controllo qualità delle attività?
feature: Activities
exl-id: 5c606d61-6d13-4a9b-9a23-4840f1754d3c
source-git-commit: 645116e1c1efba3d861b21bce110e5fb9aec1f0c
workflow-type: tm+mt
source-wordcount: '1724'
ht-degree: 35%

---

# Controllo di qualità delle attività

Utilizzare gli URL di controllo qualità in [!DNL Adobe Target] per eseguire in modo semplice e completo il controllo qualità delle attività, con collegamenti di anteprima che restano invariati, targeting facoltativo del pubblico e rapporti di controllo qualità mantenuti segmentati dai dati delle attività live.

[!UICONTROL Controllo di qualità delle attività] consente di testare completamente [!DNL Target] attività prima di lanciarle in diretta. Il [!UICONTROL Controllo di qualità delle attività] Le funzionalità includono:

* Collegamenti da condividere con i membri del team che non devono essere modificati o rigenerati, indipendentemente dagli aggiornamenti apportati alle esperienze o alle attività. Questa funzione consente di testare completamente le attività in tutto il percorso di utenti.
* Possibilità di rispettare o meno le condizioni di pubblico, per testare i criteri di targeting o per ignorarli al fine di verificare come si presentano le esperienze senza dover soddisfare le condizioni di pubblico.
* Il rapporto di controllo qualità viene acquisito per permettere agli addetti al marketing di confermare che le metriche aumentano come previsto, e i relativi dati sono tenuti separati dai rapporti di produzione (per la generazione di rapporti non A4T).
* Possibilità di visualizzare in anteprima un’esperienza in isolamento o con altre attività live che soddisfano i criteri di consegna (pagina/[!DNL Target] richiesta/pubblico).
* Capacità di eseguire il controllo qualità sull’intero percorso dell’utente. Puoi accedere al tuo sito una volta con il collegamento di controllo qualità e quindi navigare nell’intero sito in modalità di controllo qualità dell’attività. Resterai in tale modalità fino alla fine della sessione o fino a quando utilizzi il [Bookmarklet di controllo qualità di Target](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879)[!UICONTROL  per uscire dalla modalità di controllo qualità dell’attività]. Questa funzione è utile se hai un’attività che si estende su più pagine web.

  >[!NOTE]
  >
  >Questa funzionalità è vera per le implementazioni at.js con versione 2.*x* o più tardi. Per at.js 1.*x* implementazioni di, questa funzionalità è valida solo se il browser del visitatore non blocca i cookie di terze parti.

## Accesso e condivisione di un URL di controllo qualità {#section_1C59BAA247B247BDB125D1BE8EAD4547}

1. Da un’attività di [!UICONTROL Panoramica] pagina, fai clic su **[!UICONTROL Controllo di qualità delle attività]**.

   ![Collegamento Controllo di qualità attività](assets/qa_link.png)

1. Configura le seguenti impostazioni:

   ![Opzioni di configurazione del collegamento Controllo di qualità attività](assets/qa_link_config.png)

   * **[!UICONTROL Fai corrispondere le regole di pubblico per visualizzare le esperienze]:** A volte puoi voler verificare che la corrispondenza del pubblico funzioni. Altre volte si desidera controllare l&#39;aspetto dell&#39;attività. Se questa impostazione viene attivata, i soggetti del test devono soddisfare i requisiti di targeting per risultare idonei a visualizzare le esperienze. Per le attività di targeting di esperienza (XT), viene fornito un singolo URL di attività. Se il visitatore soddisfa le regole di targeting, l’esperienza verrà visualizzata.

     Se questa impostazione è disattivata, quando si fa clic sui collegamenti le esperienze vengono sempre visualizzate, anche se le regole non sono soddisfatte. Durante il controllo qualità, puoi attivare e disattivare questa opzioni per richiedere o ignorare il rispetto delle regole di targeting del pubblico.

   * **Mostra contenuto predefinito per tutte le altre attività:** Se questa opzione è attivata, il contenuto predefinito viene visualizzato per tutte le altre attività. Ad esempio, l’anteprima viene visualizzata in isolamento senza considerare tutte le altre attività live presenti nella stessa pagina/[!DNL Target] richiesta.

     Se questa impostazione è disattivata, considera quanto segue:

      * Se ci sono conflitti tra l’attività che stai testando e altre attività live, valgono le [normali regole di priorità](/help/main/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F). A causa di conflitti, è possibile che non riesca a visualizzare l’attività di cui intendi eseguire il controllo qualità.
      * Le metriche vengono incrementate per le attività visualizzate, ma solo nell’ambiente di reporting ai fini del controllo qualità.

1. Fai clic su **[!UICONTROL Fine]** per salvare le modifiche.
1. Condividi gli URL di collegamento dell’attività con i membri della tua organizzazione per il test.

   I collegamenti alle attività non scadono mai e non è necessario inviarli di nuovo se qualcuno cambia un’attività o un’esperienza. Tuttavia, se applichi un pubblico diverso da [!UICONTROL Libreria tipi di pubblico], invece di modificare semplicemente l’attività, viene generato un nuovo collegamento da condividere nuovamente.

   Ogni URL di collegamento di attività (per Esperienza A, Esperienza B e così via) consente di avviare il percorso di utenti dall’esperienza corrispondente. Fai clic sull’URL generato per un’esperienza, quindi procedi alla normale navigazione del sito per visualizzare le esperienze su più pagine (se esistono più pagine). Per ogni esperienza viene generato un solo URL, anche se l’esperienza si estende su più pagine (test di modelli o test multipagina).

   È possibile navigare nel sito per visualizzare le altre pagine perché [!UICONTROL Controllo di qualità delle attività] la modalità è permanente. Questa situazione si verifica per le implementazioni at.js con versione 2.*x* o più tardi. Per at.js 1.*x* implementazioni di, questa situazione si verifica solo se il browser del visitatore non blocca i cookie di terze parti.

1. Per visualizzare i rapporti generati dagli URL di collegamento di un’attività, fai clic su **[!UICONTROL Rapporti]** , fare clic su **[!UICONTROL Impostazioni]** icona (  ![icon_gear image](assets/icon_gear.png) ), quindi seleziona **[!UICONTROL Traffico modalità Controllo di qualità]** dal **[!UICONTROL Ambiente]** elenco a discesa.

## Considerazioni {#section_B256EDD7BFEC4A6DA72A8A6ABD196D78}

* Perché il Controllo di qualità delle attività è ora disponibile per tutti [!DNL Target] tipi di attività, la funzione &quot;Anteprima delle attività di Automated Personalization con URL di anteprima dell’esperienza&quot; non è più necessaria.
* [!UICONTROL I collegamenti di anteprima Controllo di qualità delle attività per le attività salvate potrebbero non venire caricati se nel tuo account sono presenti troppe attività salvate. ] Riprovare i collegamenti di anteprima. Per evitare che questa situazione continui a verificarsi, archivia le attività salvate che non vengono più utilizzate attivamente.
* [!UICONTROL Controllo di qualità delle attività] Gli URL sono disponibili con le attività con [Analytics come origine di reporting](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T). Hit generati durante l’esecuzione del controllo qualità tramite [!UICONTROL Controllo di qualità delle attività] passare alla stessa suite di rapporti in cui i dati dell’attività fluiscono anche dopo l’esecuzione dell’attività.
* [!UICONTROL La funzione Controllo di qualità attività non visualizza i contenuti di attività archiviate o scadute. ] Se disattivi un’attività terminata, devi salvarla nuovamente per [!UICONTROL Controllo di qualità delle attività] al lavoro.
* Attività importate in [!DNL Target Standard/Premium] (da [!DNL Target Classic], ad esempio) non supportano gli URL di controllo qualità.
* In entrata [!UICONTROL Allocazione automatica] e [!UICONTROL Recommendations] attività, il modello non è interessato dalle visite acquisite in [!UICONTROL Controllo di qualità delle attività].
* [!UICONTROL Controllo di qualità delle attività] è appiccicoso. Dopo aver navigato su un sito web in [!UICONTROL Controllo di qualità delle attività], il tuo [!DNL Target] la sessione deve scadere o [!DNL Target] rilascia da [!UICONTROL Controllo di qualità delle attività] prima di poter visualizzare il sito come un normale visitatore.

   * **Equivalente in at.js 2.*x***: se il tuo sito dispone di at.js 2.*x* , utilizza [Bookmarklet di controllo qualità di Target](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) per forzarti a uscire da [!UICONTROL Controllo di qualità delle attività]. Il caricamento di una pagina del sito con un valore vuoto, come descritto nel punto successivo, *non* rimuovi il cookie di controllo qualità dal browser quando si utilizza at.js 2.*x* è implementato.

   * **at.js 1.*x***: se il tuo sito dispone di at.js 1.*x* implementato, oltre a utilizzare il [Bookmarklet di controllo qualità di Target](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879), puoi anche forzare manualmente l’uscita dalla modalità di controllo qualità caricando una pagina del sito con il `at_preview_token` con un valore vuoto (ad esempio, `https://www.mysite.com/?at_preview_token=`).

* Se hai specificato un URL durante la creazione dell’attività [Miglioramenti nel Compositore basato su moduli](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) o [opzioni di consegna delle pagine nel Compositore esperienza visivo)](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81), l’URL di controllo qualità non funziona perché [!UICONTROL Controllo di qualità delle attività] aggiunge i parametri URL. Per risolvere questo problema, fai clic su URL di controllo qualità per passare al sito, rimuovi dall’URL i parametri aggiunti, quindi carica il nuovo l’URL.
* Se hai at.js 1.*x*, [!UICONTROL Controllo di qualità delle attività] La modalità non è definitiva se utilizzi Safari o un altro browser che blocca i cookie di terze parti. In questi casi, devi aggiungere i parametri di anteprima a ogni URL a cui vai. Lo stesso vale se hai implementato [CNAME](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/implement-cname-support-in-target.html){target=_blank}.
* Se un’attività utilizza più tipi di pubblico per le esperienze (ad esempio, se nella stessa attività sono inclusi un sito britannico e uno statunitense), i collegamenti di controllo qualità non vengono generati per le quattro combinazioni (Esperienza A/sito US, Esperienza A/sito UK, Esperienza B/sito US, Esperienza B/sito UK). Vengono creati solo due collegamenti di controllo qualità (Esperienza A ed Esperienza B) e la pagina verrà visualizzata dagli utenti che risultano idonei per il pubblico appropriato. Una persona che effettua il controllo qualità nel Regno Unito non può visualizzare il sito degli Stati Uniti.
* Tutti i parametri e i valori `at_preview` sono già codificati nell’URL. Nella maggior parte dei casi, tutto funziona come previsto. Tuttavia, alcuni clienti devono caricare bilanciatori o server Web che tentano di codificare nuovamente i parametri della stringa di query.

  A causa di questa doppia codifica, quando [!DNL Target] tenta di decodificare il `at_preview_token`, [!DNL Target] impossibile estrarre il valore token corretto. l&#39;anteprima non funziona.

  [!DNL Adobe] consiglia di parlare con il team IT per assicurarsi che tutti i parametri di anteprima siano inseriti nell&#39;elenco Consentiti in modo che questi valori non vengano trasformati in alcun modo.

  Nella tabella seguente sono elencati i parametri che possono essere inseriti nell&#39;elenco Consentiti nel dominio:

  | Parametro | Tipo | Valore | Descrizione |
  |--- |--- |--- |--- |
  | `at_preview_token` | Stringa crittografata | Obbligatorio; nessun valore predefinito | Un’entità crittografata che contiene l’elenco degli ID delle campagne che possono essere eseguiti in modalità di controllo qualità. |
  | `at_preview_index` | Stringa | Vuoto | Il formato del parametro è `<campaignIndex>` o `<campaignIndex>_< experienceIndex>`<br>Entrambi gli indici iniziano con 1. |
  | `at_preview_listed_activities_only` | Boolean (true/false) | Valore predefinito: false | Se “true”, vengono elaborate tutte le campagne specificate nei parametri `at_preview_index`.<br>Se “false”, vengono elaborate tutte le campagne della pagina, anche se non sono state specificate nel token di anteprima. |
  | `at_preview_evaluate_as_true_audience_ids` | Stringa | Vuoto | L’elenco degli ID segmento separati da underscore (&quot;_&quot;) deve sempre (a livello di targeting e di reporting) essere valutato come &quot;true&quot; nell’ambito del [!DNL Target] richiesta. |
  | `_AT_Debug` | Stringa | Finestra o console | Log della console o nuova finestra. |
  | `adobe_mc_ref` |  |  | Passa l&#39;URL di riferimento della pagina predefinita alla nuova pagina. Se utilizzato con `AppMeasurement.js` versione 2.1 (o successiva), [!DNL Adobe Analytics] utilizza questo valore di parametro come URL di riferimento nella nuova pagina. |
  | `adobe_mc_sdid` |  |  | Supera il [!DNL Supplemental Data Id] (SDID) [!DNL Experience Cloud Org Id] dalla pagina predefinita alla nuova pagina. Il passaggio di questi ID consente [!UICONTROL Analytics for Target] (A4T) per &quot;unire&quot; insieme il [!DNL Target] nella pagina predefinita con [!DNL Analytics] nella nuova pagina. |

* Il [!UICONTROL Modalità di controllo qualità di Target] L’interfaccia utente mostra solo il primo URL di un’esperienza in un’attività multipagina. Si presume infatti che si sta creando un test di percorso e si passa dall&#39;URL1 all&#39;URL2. Tuttavia, se desideri passare all’URL2 indipendentemente, copia tutti i parametri URL forniti per l’URL1 e applicali all’URL2 dopo aver inserito un segno &quot;?&quot;, come nell’URL1.
* I collegamenti di anteprima Controllo di qualità delle attività per le attività salvate potrebbero non venire caricati se nel tuo account sono presenti troppe attività salvate. Riprova i collegamenti di anteprima. Archivia le attività salvate che non vengono più utilizzate attivamente per impedire che questo problema continui a verificarsi.

## Compatibilità della [!UICONTROL Modalità QA] con la libreria JavaScript di Target {#compatibility}

[!DNL Target] supporta le seguenti librerie JavaScript:

* [at.js 1.x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html)
* [at.js 2.x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html)
* [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html)

Nella tabella seguente sono elencati i vari tipi di attività e viene indicato se [!UICONTROL Controllo di qualità delle attività] è supportata per ogni libreria:

| Tipo di attività | at.js 1.x | at.js 2.x | Platform Web SDK |
| --- | --- | --- | --- |
| [!UICONTROL Test A/B] | Sì | Sì | Sì |
| [!UICONTROL Allocazione automatica] | Sì | Sì | Sì |
| [!UICONTROL Targeting automatico] | Sì | Sì | Sì |
| [!UICONTROL Automated Personalization] (AP) | Sì | Sì | Sì |
| [!UICONTROL Targeting dell’esperienza] (XT) | Sì | Sì | Sì |
| [!UICONTROL Test multivariato] (MVT) | Sì | Sì | Sì |
| [!UICONTROL Raccomandazioni] | Sì | Sì | Sì |

