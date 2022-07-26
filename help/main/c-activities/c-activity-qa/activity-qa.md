---
keywords: qa;modalità qa; qa attività;url qa;url qa;url di anteprima;url di anteprima
description: Scopri come utilizzare Adobe [!DNL Target] Gli URL di controllo qualità consentono di verificare in modo semplice e completo la qualità delle attività tramite collegamenti di anteprima che restano invariati, l’eventuale definizione di un pubblico di destinazione e rapporti di controllo qualità mantenuti separati dai dati delle attività live.
title: Come Faccio A Controllare Le Attività?
feature: Activities
exl-id: 5c606d61-6d13-4a9b-9a23-4840f1754d3c
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '1832'
ht-degree: 37%

---

# Controllo di qualità delle attività

Utilizzare gli URL di controllo qualità in [!DNL Adobe Target] per eseguire attività di controllo qualità end-to-end con collegamenti di anteprima che non cambiano mai, targeting del pubblico facoltativo e reporting di controllo qualità mantenuti separati dai dati delle attività live.

[!UICONTROL Controllo di qualità delle attività] consente di testare completamente il [!DNL Target] attività prima di lanciarle in diretta. La [!UICONTROL Controllo di qualità delle attività] le funzionalità includono:

* Collegamenti da condividere con i membri del team che non cambiano mai o richiedono la rigenerazione, indipendentemente dagli aggiornamenti apportati alle esperienze o attività. Questa funzione consente di testare completamente le attività in tutto il percorso di utenti.
* Possibilità di rispettare o meno le condizioni di pubblico, per testare i criteri di targeting o per ignorarli al fine di verificare come si presentano le esperienze senza dover soddisfare le condizioni di pubblico.
* Il rapporto di controllo qualità viene acquisito per permettere agli addetti al marketing di confermare che le metriche aumentano come previsto, e i relativi dati sono tenuti separati dai rapporti di produzione (per la generazione di rapporti non A4T).
* Possibilità di visualizzare in anteprima un’esperienza in isolamento o con altre attività live che soddisfano i criteri di consegna (pagina/richiesta Target/pubblico).
* Capacità di eseguire il controllo qualità sull’intero percorso dell’utente. Puoi accedere al tuo sito una volta con il collegamento di controllo qualità e quindi navigare nell’intero sito in modalità di controllo qualità dell’attività. Resterai in tale modalità fino alla fine della sessione o fino a quando utilizzi il [Bookmarklet di controllo qualità di Target](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879)[!UICONTROL  per uscire dalla modalità di controllo qualità dell’attività]. Questa funzione è utile se si dispone di un’attività che si estende su più pagine web.

   >[!NOTE]
   >
   >Questa funzionalità è valida per le implementazioni at.js con versione 2.*x* o successiva. Per at.js 1.*x* implementazioni , questa funzionalità è vera solo se il browser del visitatore non blocca i cookie di terze parti.

## Accesso e condivisione di un URL di controllo qualità {#section_1C59BAA247B247BDB125D1BE8EAD4547}

1. Da un’ [!UICONTROL Panoramica] fai clic su **[!UICONTROL Controllo di qualità delle attività]** link.

   ![Collegamento Controllo di qualità attività](assets/qa_link.png)

1. Configura le seguenti impostazioni:

   ![Opzioni di configurazione del collegamento Controllo di qualità attività](assets/qa_link_config.png)

   * **[!UICONTROL Applicare le regole del pubblico per visualizzare le esperienze]:** A volte è necessario verificare che la corrispondenza del pubblico funzioni. Altre volte puoi controllare l’aspetto dell’attività. Se questa impostazione viene attivata, i soggetti del test devono soddisfare i requisiti di targeting per risultare idonei a visualizzare le esperienze. Per le attività di targeting di esperienza (XT), viene fornito un singolo URL di attività. Se il visitatore soddisfa le regole di targeting, l’esperienza verrà visualizzata.

      Se questa impostazione è disattivata, quando si fa clic sui collegamenti le esperienze vengono sempre visualizzate, anche se le regole non sono soddisfatte. Durante il controllo qualità, puoi attivare e disattivare questa opzioni per richiedere o ignorare il rispetto delle regole di targeting del pubblico.

   * **Mostra il contenuto predefinito per tutte le altre attività:** Se questa opzione è attivata, viene visualizzato il contenuto predefinito per tutte le altre attività. Ad esempio, l’anteprima viene visualizzata in isolamento senza considerare tutte le altre attività live presenti nella stessa pagina/[!DNL Target] richiesta.

      Se questa impostazione è disattivata, considera quanto segue:

      * Se ci sono conflitti tra l’attività che stai testando e altre attività live, valgono le [normali regole di priorità](/help/main/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F). A causa di conflitti, è possibile che non sia possibile visualizzare l’attività che si intende eseguire al controllo qualità.
      * Le metriche vengono incrementate per le attività visualizzate, ma solo nell’ambiente di reporting ai fini del controllo qualità.

1. Fai clic su **[!UICONTROL Fine]** per salvare le modifiche.
1. Condividi gli URL di collegamento dell’attività con i membri dell’organizzazione a scopo di test.

   I collegamenti alle attività non scadono mai e non è necessario inviare nuovamente i collegamenti se un utente modifica un’attività o un’esperienza. Tuttavia, se applichi un pubblico diverso dal [!UICONTROL Libreria Pubblico], invece di modificare semplicemente l’attività, viene generato un nuovo collegamento che devi condividere.

   Ogni URL di collegamento di un’attività (per l’esperienza A, l’esperienza B e così via) consente di avviare il percorso di utenti dall’esperienza corrispondente. Fai clic sull’URL generato per un’esperienza, quindi continua con la normale navigazione sul sito per visualizzare le esperienze su più pagine (se esistono più pagine). Per ogni esperienza viene generato un solo URL, anche se l’esperienza si estende su più pagine (test di modelli o test multipagina).

   Puoi navigare nel sito per visualizzare le altre pagine, perché [!UICONTROL Controllo di qualità delle attività] la modalità è persistente. Questa situazione è vera per le implementazioni at.js con versione 2.*x* o successiva. Per at.js 1.*x* implementazioni , questa situazione è vera solo se il browser del visitatore non blocca i cookie di terze parti.

1. Per visualizzare i rapporti generati dagli URL di collegamento dell’attività, fai clic su **[!UICONTROL Rapporti]** fai clic su **[!UICONTROL Impostazioni]** icona (  ![icona_ingranaggio](assets/icon_gear.png) ), quindi seleziona **[!UICONTROL Traffico in modalità QA]** dal **[!UICONTROL Ambiente]** elenco a discesa.

## Considerazioni {#section_B256EDD7BFEC4A6DA72A8A6ABD196D78}

* La [!UICONTROL Controllo di qualità delle attività] viene visualizzato il collegamento [!UICONTROL Panoramica] pagina di tutti i tipi di attività tranne [!UICONTROL Targeting automatico] e [!UICONTROL Automated Personalization] (AP).
* [!UICONTROL I collegamenti di anteprima Controllo di qualità delle attività per le attività salvate potrebbero non venire caricati se nel tuo account sono presenti troppe attività salvate. ] Il nuovo tentativo dei collegamenti di anteprima dovrebbe funzionare. Per evitare che questa situazione continui, archivia le attività salvate che non vengono più utilizzate attivamente.
* [!UICONTROL Gli URL controllo qualità delle attività sono disponibili per le attività in cui Analytics è impostato come origine per la creazione di rapporti (A4T). ] Hit generati durante l’esecuzione del controllo qualità utilizzando [!UICONTROL Controllo di qualità delle attività] passa alla stessa suite di rapporti in cui i dati dell’attività scorrono anche dopo che l’attività è diventata attiva.
* [!UICONTROL La funzione Controllo di qualità attività non visualizza i contenuti di attività archiviate o scadute. ] Se disattivi un’attività terminata, devi salvare nuovamente l’attività per [!UICONTROL Controllo di qualità delle attività] per lavorare.
* Attività importate in [!DNL Target Standard/Premium] (da [!DNL Target Classic], ad esempio) non supportano gli URL di controllo qualità.
* In [!UICONTROL Allocazione automatica] e [!UICONTROL Recommendations] attività, il modello non è interessato dalle visite acquisite in [!UICONTROL Controllo di qualità delle attività].
* [!UICONTROL Controllo di qualità delle attività] è appiccicoso. Dopo aver navigato su un sito web in [!UICONTROL Controllo di qualità delle attività], il [!DNL Target] la sessione deve scadere oppure [!DNL Target] rilascia da [!UICONTROL Controllo di qualità delle attività] prima di poter visualizzare il sito come un normale visitatore. Utilizza la [Bookmarklet di controllo qualità di Target](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) per costringerti a uscire [!UICONTROL Controllo di qualità delle attività].

   Puoi anche forzare manualmente l’uscita dalla modalità di controllo qualità caricando una pagina del sito con il parametro `at_preview_token` con un valore vuoto (ad esempio, `https://www.mysite.com/?at_preview_token=`).

* Se hai specificato &quot;URL is&quot; durante la creazione dell’attività [perfezionamenti nel Compositore basato su moduli](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) o [opzioni di distribuzione delle pagine nel Compositore esperienza visivo)](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81), l’URL di controllo qualità non funziona perché [!UICONTROL Controllo di qualità delle attività] aggiunge parametri URL. Per risolvere questo problema, fai clic su URL di controllo qualità per passare al sito, rimuovi dall’URL i parametri aggiunti, quindi carica il nuovo l’URL.
* Se disponi di at.js 1.*x*, [!UICONTROL Controllo di qualità delle attività] La modalità non è persistente se utilizzi Safari o un altro browser che blocca i cookie di terze parti. In questi casi, devi aggiungere i parametri di anteprima a ciascun URL a cui accedi. Lo stesso vale se hai implementato [CNAME](https://developer.adobe.com/target/before-implement/implement-cname-support-in-target/){target=_blank}.
* Se un’attività utilizza più tipi di pubblico per le esperienze (ad esempio, un sito US e UK inclusi nella stessa attività), i collegamenti di controllo qualità non vengono generati per le quattro combinazioni (sito A/US, sito A/UK, sito B/US dell’esperienza, sito B/UK). Vengono creati solo due collegamenti di controllo qualità (Esperienza A ed Esperienza B) e la pagina verrà visualizzata dagli utenti che risultano idonei per il pubblico appropriato. Una persona di controllo qualità nel Regno Unito non può visualizzare il sito degli Stati Uniti.
* Tutti i parametri e i valori `at_preview` sono già codificati nell’URL. Nella maggior parte dei casi, tutto funziona come previsto. Tuttavia, alcuni clienti devono caricare bilanciatori o server Web che tentano di codificare nuovamente i parametri della stringa di query.

   A causa di questa doppia codifica, quando [!DNL Target] tenta di decodificare il `at_preview_token`, [!DNL Target] Impossibile estrarre il valore corretto del token. L&#39;anteprima non funziona.

   Adobe consiglia di parlare con il team IT per assicurarsi che tutti i parametri di anteprima siano inseriti nell&#39;elenco Consentiti in modo che tali valori non vengano trasformati in alcun modo.

   Nella tabella seguente sono elencati i parametri che possono essere inseriti nell&#39;elenco Consentiti nel dominio:

   | Parametro | Tipo | Valore | Descrizione |
   |--- |--- |--- |--- |
   | `at_preview_token` | Stringa crittografata | Obbligatorio; nessun valore predefinito | Un’entità cifrata che contiene l’elenco degli ID delle campagne che possono essere eseguiti in modalità Controllo qualità. |
   | `at_preview_index` | Stringa | Vuoto | Il formato del parametro è `<campaignIndex>` o `<campaignIndex>_< experienceIndex>`<br>Entrambi gli indici iniziano con 1. |
   | `at_preview_listed_activities_only` | Boolean (true/false) | Valore predefinito: false | Se “true”, vengono elaborate tutte le campagne specificate nei parametri `at_preview_index`.<br>Se “false”, vengono elaborate tutte le campagne della pagina, anche se non sono state specificate nel token di anteprima. |
   | `at_preview_evaluate_as_true_audience_ids` | Stringa | Vuoto | Elenco degli ID dei segmenti separati da underscore (&quot;_&quot;) che devono sempre (a livello di targeting e di reporting) essere valutati come &quot;true&quot; nell’ambito del [!DNL Target] richiesta. |
   | `_AT_Debug` | Stringa | Finestra o console | Log della console o nuova finestra. |
   | `adobe_mc_ref` |  |  | Passa l&#39;URL di riferimento della pagina predefinita alla nuova pagina. Se utilizzato con `AppMeasurement.js` versione 2.1 (o successiva), [!DNL Adobe Analytics] utilizza questo valore di parametro come URL di riferimento nella nuova pagina. |
   | `adobe_mc_sdid` |  |  | Passa la [!DNL Supplemental Data Id] (SDID) e [!DNL Experience Cloud Org Id] dalla pagina predefinita alla nuova pagina. Il passaggio di questi ID consente [!UICONTROL Analytics for Target] (A4T) per &quot;unire&quot; insieme i [!DNL Target] richiesta nella pagina predefinita con [!DNL Analytics] nella nuova pagina. |

* La [!UICONTROL Modalità di controllo qualità di Target] L’interfaccia utente mostra solo il primo URL di un’esperienza in un’attività multipagina. Si presume infatti che si stia creando un test di percorso e che si passi dall’URL1 all’URL2. Tuttavia, se desideri passare all’URL2 indipendentemente, copia tutti i parametri URL forniti per l’URL1 e applicali all’URL2 dopo aver inserito un segno &quot;?&quot;, come nell’URL1.
* I collegamenti di anteprima Controllo di qualità delle attività per le attività salvate potrebbero non venire caricati se nel tuo account sono presenti troppe attività salvate. Riprova i collegamenti di anteprima. Archivia le attività salvate che non vengono più utilizzate attivamente per impedire che questo problema continui a verificarsi.

## Compatibilità della [!UICONTROL Modalità QA] con la libreria JavaScript di Target {#compatibility}

[!DNL Target] supporta le seguenti librerie JavaScript:

* [at.js 1.x](https://developer.adobe.com/target/implement/client-side/atjs/how-atjs-works/how-atjs-works/)
* [at.js 2.x](https://developer.adobe.com/target/implement/client-side/atjs/how-atjs-works/how-atjs-works/)
* [Adobe Experience Platform Web SDK](https://developer.adobe.com/target/implement/client-side/aep-web-sdk/)

La tabella seguente elenca i vari tipi di attività e indica se: [!UICONTROL Controllo di qualità delle attività] è supportata per ogni libreria:

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

Gli URL di anteprima dell’esperienza possono essere generati per tutti [!DNL Target] tipi di attività. Gli URL di anteprima consentono di visualizzare il contenuto dell’esperienza direttamente sul sito prima che l’attività sia attiva a scopo di anteprima e controllo qualità. Gli URL di anteprima dell’esperienza ignorano il targeting per forzare la visualizzazione di una particolare esperienza.

Per informazioni sul funzionamento degli URL di anteprima con [!UICONTROL Automated Personalization] (AP) attività, vedi [Anteprima delle attività di Automated Personalization con URL di anteprima dell’esperienza](/help/main/c-activities/t-automated-personalization/experience-preview.md).

Per accedere e condividere un URL di anteprima da un’attività **[!UICONTROL Panoramica]** fai clic su **[!UICONTROL Controllo di qualità delle attività]** link.

>[!NOTE]
>
>La [!UICONTROL Controllo di qualità delle attività] collegamento e URL di anteprima sono gli stessi per tutte le attività diverse da [!DNL Target] Attività di Personalizzazione automatizzata.

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

