---
description: Informazioni sui problemi noti per questa versione di Target. Include inoltre informazioni sui problemi risolti.
keywords: problemi noti;problemi risolti;note sulla versione
seo-description: Informazioni sui problemi noti per questa versione di Target. Include inoltre informazioni sui problemi risolti.
seo-title: Problemi noti e problemi risolti
solution: Target
title: Problemi noti e problemi risolti
topic: Premium
uuid: f8e8e057-1842-4922-ab7f-4d5441048573
translation-type: tm+mt
source-git-commit: e1d5f642505ce62900fc55784b178ba0fb320184

---


# Problemi noti e problemi risolti{#known-issues-and-resolved-issues}

Informazioni sui problemi noti per questa versione di Target. Include inoltre informazioni sui problemi risolti.

>[!NOTE]
>
>I codici tra parentesi sono per uso interno di Adobe.

## Problemi noti {#section_AEDC98B67CF24C9F8E0CF0D2EB9ACAEF}

Nelle sezioni seguenti sono elencati i problemi noti per [!DNL Target]:

### Annullamento del caricamento di una pagina all&#39;interno della VEC {#cancel}

* Il seguente problema noto esiste al momento per annullare il caricamento di un&#39;attività [!UICONTROL A/B Test] o [!UICONTROL Experience Targeting] (XT) all&#39;interno del VEC che contiene un URL di reindirizzamento.

   Nel passaggio uno dei flussi di lavoro guidato in tre parti all&#39;interno della VEC, quando si annulla il caricamento della pagina viene visualizzato il [!UICONTROL pannello Modifiche] nell&#39;aula virtuale e il reindirizzamento al modello URL viene applicato all&#39;esperienza (ad esempio, &quot;Esperienza B). Quando eseguite un passaggio a due o tre e quindi tornate al punto uno, si verifica la situazione seguente.

   In &quot;Esperienza B&quot;, per impostazione predefinita, il rendering del modello di caricamento sito Web annullato e [!UICONTROL il] pannello Modifiche sono accessibili, operazione non consigliata perché l&#39;esperienza ha un modello di reindirizzamento a un modello URL. Dovrebbe essere visualizzato il modello reindirizzamento al modello URL.

   Per visualizzare lo stato corretto dell&#39;esperienza nell&#39;aula virtuale:

   Se passate a un&#39;altra esperienza e quindi tornate a &quot;Esperienza B&quot; [!DNL Target] , viene visualizzato il modello di reindirizzamento al modello URL applicato a questa esperienza e il [!UICONTROL pannello Modifiche] non è accessibile. (TGT-32138)

* Per i siti Web delle applicazioni singole (SPA), l&#39;annullamento del caricamento non consente di modificare le azioni nel pannello [!UICONTROL Modifiche] .

### Supporto delle autorizzazioni Enterprise nelle API di Target {#api}

Le offerte di codice create dall&#39;interfaccia utente di Target nella libreria Offerte possono essere visualizzate nell&#39;area di lavoro predefinita se l&#39;elenco delle offerte viene rimosso utilizzando GET API. Il problema verrà risolto nella prima settimana di marzo 2019. Dopo la correzione, le offerte del codice verranno visualizzate nell&#39;area di lavoro appropriata quando vengono richiamate dalle API. Questo problema *non* influisce sulle offerte create dalle API. Ad esempio, le offerte di codice create dalle API vengono visualizzate nell&#39;area di lavoro in cui sono state create, recuperate utilizzando GET API o dall&#39;interfaccia utente di Target.

### Consigli 

Di seguito sono riportati i problemi noti relativi alle attività Consigli:

* L’indice del feed di Recommendations può mostrare il messaggio “In attesa dell’indice” se gli elementi nel feed sono identici a quelli della precedente esecuzione. Questo non influisce sull’assimilazione del prodotto per la consegna. (RECS-6663)
* L’errore &quot;error.restapi.algorithmProfileAttributeInvalid&quot; relativo alla funzionalità Consigli si verifica quando specifici attributi di profilo vengono utilizzati come chiave di criterio.
* Quando l’opzione Promozione dopo viene utilizzata in un’attività Consigli, i filtri di inclusione dei criteri non vengono applicati ai consigli di backup.
* L’interfaccia dei feed della funzionalità Consigli non mostra lo stato di indicizzazione corretto. I processi di backend funzionano correttamente, ma non è possibile recuperare e visualizzare nell’interfaccia utente lo stato corrente.

   **Soluzione alternativa**: per determinare se un feed di Recommendations per un determinato gruppo host è stato indicizzato correttamente, accedi come amministratore all’interfaccia utente per la ricerca dei prodotti e osserva l’ora dell’ultima indicizzazione. Questa corrisponde all’ultima volta che è stato indicizzato il feed per un determinato gruppo host. (TGT-27116)

* Nei prodotti consigliati potrebbero essere non essere visualizzati valori fino a due cifre decimali. Ad esempio, se si tenta di visualizzare il valore nella progettazione come 35,00 la funzionalità Consigli visualizza 35 (nessuna cifra decimale anziché due cifre decimali). (RECS-5972)

   **Soluzione**: passa il valore dell’entità in due parametri entity.attributes . Il primo, `entity.value`, è un parametro riservato che richiede un valore doppio. Il secondo, può essere un parametro entity.attribute personalizzato che memorizzerà il valore dell’entità come stringa per consentirne il rendering corretto.

   Ad esempio:

   `"entity.value" : 35.00, "entity.displayValue" : "35.00",`

### Attività di test multivariato (MVT)

In un’attività MVT, il vincitore mostrato nella tabella e nel grafico non è coerente quando si controllano le metriche. Questo si verifica se un utente passa dalla visualizzazione Riepilogo alla visualizzazione Grafico, quindi torna alla visualizzazione Riepilogo, modifica una metrica e passa alla visualizzazione Grafico. Quando si verifica questo problema, la visualizzazione Riepilogo mostra sempre il vincitore corretto. Se l’utente non passa mai dalla vista Grafico alla vista Riepilogo, la vista Grafico mostra il vincitore corretto.

### at.js 

Di seguito sono riportati problemi noti relativi a at.js:

* Quando si carica una pagina nel Compositore esperienza visivo, Target deve determinare se l’impostazione mbox globale è abilitata o disabilitata e se entityID o categoryId è presente nel percorso in cui l’utente sta tentando di applicare il consiglio nel Compositore esperienza visivo. L’elenco dei criteri viene filtrato sulla base di queste informazioni. L’elenco predefinito contiene algoritmi filtrati, ma la casella di controllo [Compatibile](https://marketing.adobe.com/resources/help/en_US/target/recs/t_algo_select_recs.html) consente di visualizzare l’elenco completo degli algoritmi.

   Quando si utilizza at.js, la casella di controllo Compatibile è nascosta e non è pertanto possibile visualizzare gli algoritmi non compatibili.

   Questo problema è relativo solo alle attività Consigli che utilizzano il Compositore esperienza visivo.

   **Soluzione alternativa**: disabilita l’opzione [!UICONTROL Filtra criteri incompatibili] in [!UICONTROL Recommendations &gt; Impostazioni]. Dopo aver disabilitato questa impostazione, nel selettore dei criteri verranno visualizzati tutti i criteri (compatibili e non). (TGT-25949)

* Dopo l’aggiornamento alla versione 1.0 di at.js, le mbox non funzionano nei browser Microsoft Explorer 11 a causa dell’interazione tra at.js e Visitor API 2.2.0. Questo problema riguarda le versioni 0.9.6 e successive di at.js. (TNT-27600)
* at.js potrebbe non funzionare con le app Cordova/Hybrid perché non supportano i cookie di prima parte. (TNT-26166)

   **Soluzione alternativa**: configura at.js con l’opzione “Solo x” attivata e passa `mboxThirdPartyId` nelle chiamate per la gestione degli utenti.

### mbox.js

La libreria mbox.js non supporta linguaggi di template lato client, come Handlebar e Mustache. La libreria at.js *supporta* tali linguaggi.

**Nota**: la libreria mbox.js non verrà più sviluppata. Tutti i clienti devono migrare da mbox.js a at.js. Per ulteriori informazioni, consulta [Migrazione a at.js da mbox.js](../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA).

### Offerte di reindirizzamento

Di seguito sono riportati i problemi noti relativi alle offerte di reindirizzamento:

* Una condizione di concorrenza può determinare un conteggio delle visualizzazioni di pagina sia nella pagina originale sia in quella di reindirizzamento. Sono previsti aggiornamenti nel secondo trimestre del 2018 per l’implementazione di at.js in modo da evitare tale condizione di concorrenza. Per ulteriori informazioni sul problema e una soluzione alternativa, consulta [Offerte di reindirizzamento - Domande frequenti su A4T](../c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905) .
* Alcune attività di reindirizzamento nelle implementazioni at.js possono generare la ripetizione ciclica dell’URL di anteprima (l’offerta viene consegnata ripetutamente). Utilizza la [modalità Controllo qualità](../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) invece di eseguire anteprima e controllo qualità. Questo problema non ha alcun impatto sull’effettiva consegna dell’offerta. (TGT-23019)

### Implementazione: Creazione automatica mbox globale

Nella scheda Implementazione ([!UICONTROL Configurazione &gt; Implementazione]) il campo [!UICONTROL Creazione automatica mbox globale] è impostato su “false” per impostazione predefinita per un tenant nuovo.

Quando mbox.js viene scaricato per la prima volta dopo il provisioning, il campo [!UICONTROL Creazione automatica mbox globale] è impostato su “true” nel file mbox.js scaricato e nel backend di [!DNL Target], ma continua a mostrare “false” nella pagina [!UICONTROL Implementazione] dell’interfaccia utente fino a quando la pagina non viene aggiornata (dopo l’aggiornamento della pagina, lo stato diventa “true”).

at.js verrà scaricato con `global_mbox_autocreate = false` per un tenant nuovo. Se mbox. js viene scaricato per primo, global\_mbox\_autocreate è impostato su “true” e anche at.js sarà scaricato con `global_mbox_autocreate = true`. (TGT-15929)

### Metriche di successo

Le metriche di successo con l’opzione avanzata “Come verrà incrementato il conteggio?” impostata su “A ogni impression” o “A ogni impression (esclusi aggiornamenti pagina)” non possono essere utilizzate come metriche di successo da cui dipende un’altra metrica.

Quando una metrica di successo è impostata per essere incrementata a ogni impression, Target conta il visitatore ogni volta che visita questa metrica di successo. Quindi, Target reimposta su 0 la metrica di successo “Appartenenza” in modo da contare di nuovo l’impression successiva. Pertanto, se un’altra metrica richiede che questa metrica sia stata vista per prima, Target non è in grado di capire se l’utente ha visto la prima metrica.

### Analytics for Target (A4T)

Le impressioni e le conversioni delle attività di Target vengono attualmente conteggiate in modo errato in Analysis Workspace .

Come soluzione alternativa, basati sui dati A4T in Reports &amp; Analytics fino a quando questo problema non viene risolto.

### API di Target

I clienti non possono eseguire operazioni CRUD sulle attività di allocazione automatica tramite la versione v3 dell’API A/B Activities in Adobe I/O.

## Problemi risolti {#section_FD2FC86E7C734D60B1EDC9DEF60E1014}

Man mano che i suddetti problemi noti vengono risolti, saranno spostati nella sezione seguente e verranno eventualmente integrati con note aggiuntive.

### Gruppi di esclusione

* Quando viene applicata la deduplicazione automatica dopo la creazione di gruppi di esclusione, il conteggio nel diagramma dell’attività potrebbe non essere corretto nell’interfaccia utente.
* Quando si modifica un’attività esistente di un gruppo di esclusione, le inclusioni manuali potrebbero non essere riportate correttamente nell’interfaccia utente.

Questi problemi sono stati risolti.

### API di Target

La versione v1 delle API Offer su Adobe I/O considera tutte le offerte create tramite Target come nell’area di lavoro predefinita. (TTTEAM-41957)

Questo problema è stato risolto.

### at.js 

Dopo l’aggiornamento alla versione 1.0 di at.js, le mbox non funzionano nei browser Microsoft Explorer 11 a causa dell’interazione tra at.js e Visitor API 2.2.0. Questo problema riguarda le versioni 0.9.6 e successive di at.js. (TNT-27600)

Risolto con il rilascio della versione 2.3.0 o successive dell’API.

### Geotargeting

La ricerca di una stringa contenente caratteri speciali (ad esempio uno spazio o una virgola) non è attualmente supportata durante la creazione di tipi di pubblico di geotargeting. Questo problema affiora, ad esempio, quando si creano tipi di pubblico basati su città, stati, paesi, ecc. Ad esempio, quando si cerca “new york”, la ricerca non restituisce risultati validi.

Corretto a novembre 2018.

### at.js 

Quando si utilizza la versione 1.6.0 di at.js i reindirizzamenti di Analytics for Target (A4T) si verificano ma senza qualificazione dell&#39;attività.

Risolto con il rilascio della versione 1.6.2 di at.js.

### Attività, aree di lavoro ed eliminare API attività

Le attività nell&#39;area di lavoro predefinita eliminate tramite API continuano a essere visualizzate nell&#39;interfaccia utente di Target. Come soluzione alternativa, elimina tutte le attività nell&#39;area di lavoro predefinita utilizzando l&#39;interfaccia utente di Target. (TGT-31315)

Risolto il 25 ottobre 2018.

### Rapporti a livello di offerta di Personalizzazione automatizzata (AP)

Quando si fa clic sull&#39;esperienza con targeting nel rapporto di un&#39;attività di Personalizzazione automatizzata (AP) per visualizzare i rapporti a livello di offerta, al momento vengono visualizzati risultati vuoti, un messaggio di errore o un&#39;icona in rotazione. (TNT-30695)

Risolto il 27 settembre 2018.

### Editor di codice

Se si ricarica il Compositore esperienza visivo al passaggio 1 del flusso di lavoro guidato in tre passaggi mentre si lavora con l&#39;editor di codice in Firefox e Internet Explorer, il rendering della scheda Modifiche non viene eseguito correttamente; tuttavia, la funzionalità del Compositore esperienza visivo non viene influenzata. (TGT-28730)

Ciò è stato corretto nella versione 18.9.1.

### Attività Consigli che utilizza una regola di promozione attributi

Quando si modifica o si copia un&#39;attività di Consigli che utilizza una regola di promozione attributi, viene visualizzato l&#39;errore “Campo mancante” quando si fa clic su Salva .

Ciò è stato corretto nella versione 17.8.1.

### Stato dell&#39;indice dei feed dei consigli

L’interfaccia dei feed della funzionalità Consigli non mostra lo stato di indicizzazione corretto. I processi di backend funzionano correttamente, ma non è possibile recuperare e visualizzare nell’interfaccia utente lo stato corrente.

Ciò è stato corretto nella versione 17.10.1.

### Consigli di backup

I consigli di backup mostrano erroneamente lo stato “Abilitato” nelle schede degli articoli visualizzati di recente nell’interfaccia utente di Target. (TGT-29308)

Ciò è stato corretto nella versione 18.4.1 in modo che venga visualizzato “Disattivato”.

### Attività Auto-Target e tipi di pubblico per rapporti

Quando viene modificato il nome di un pubblico per la creazione di rapporti utilizzato in un&#39;attività Auto-Target, gli aggiornamenti successivi da Target per quell&#39;attività potrebbero non essere inclusi e comparirà un messaggio di errore.

Questo problema è stato risolto con la versione 18.5.1 (22 maggio 2018).

### at.js 

L’algoritmo per l’estrazione del dominio di primo livello che deve essere utilizzato quando si salvano i cookie è stato modificato nella versione 0.9.6. di at.js. A causa di questa modifica, i cookie non possono essere salvati in indirizzi IP. La maggior parte degli indirizzi IP si utilizza a scopo di test, ma in alternativa puoi utilizzare le voci DNS, regolare il file host in una casella locale oppure utilizzare la funzione targetGlobalSettings() di at.js per inserire uno snippet di codice per il supporto degli indirizzi IP.

Questo problema è stato risolto nella versione 1.2 di at.js.

### Autorizzazioni utente Enterprise per Target Premium

Come parte della migrazione delle autorizzazioni Enterprise, la gestione degli utenti Target Premium è stata spostata dall’interfaccia utente di Adobe Target ad Adobe Admin Console.

Come risultato della migrazione, esistono due potenziali problemi:

* Gli utenti non amministratori hanno ricevuto un’e-mail che comunica che ora hanno accesso ad Adobe Target. Ciò indica che la migrazione per l’organizzazione è stata completata. L’e-mail stessa può essere ignorata.
* Dopo la migrazione, sono stati segnalati alcuni casi in cui utenti precedentemente disabilitati sono diventati nuovamente visibili in Adobe Admin Console. Questo potrebbe essere un problema per la tua organizzazione se gli utenti disabilitati in Adobe Admin Console erano ancora inclusi nell’elenco di utenti di Target prima della migrazione. Consigliamo agli amministratori di rivedere l’elenco degli utenti in Admin Console per convalidare l’accesso.

Questo problema è stato risolto il 30 agosto 2017

### Creazione di attività 

Un problema relativo alla versione 17.6.2 potrebbe aver interessato le attività create e/o aggiornate tra il 22 giugno 2017 e il 29 giugno 2017. Il problema ha riguardato le seguenti attività:

* Eventuali esperienze che sono state riorganizzate in Targeting esperienza (XT) sono tornate all’ordine originale.
* Eventuali regole di segmenti locali per l’attività (non salvate in un pubblico) sono andate perse: tipi di pubblico combinati, perfezionamenti di posizione ed eventuali regole su metriche di successo.

Questo problema non interessa nessun’altra attività.

**Importante**: questo problema non viene corretto automaticamente. Per risolverlo, è necessario salvare nuovamente le attività interessate.

Questo problema è stato risolto il 29 giugno 2017

### Compositore esperienza basato su moduli

In relazione all’utilizzo del Compositore esperienza basato su moduli, sono stati segnalati i seguenti problemi:

* Se utilizzi il Compositore esperienza basato su moduli con una mbox diversa da quella globale creata automaticamente (target-global-mbox) e selezioni una metrica di coinvolgimento come metrica di successo, potrai visualizzare gli incrementi di metrica solo sulle pagine che hanno la mbox utilizzata nell&#39;attività. Ad esempio, se la mbox è homepage\_mbox, la metrica Pagine per visita corrisponde al numero di hit su homepage\_mbox durante quella visita. (TGT-22789)
* Se si elimina un’esperienza in un’attività Targeting esperienza (XT), viene generata un’eccezione JavaScript quando si utilizza il Compositore esperienza basato su moduli al passaggio 1 del processo. (TGT-24366)

Il primo problema è stato risolto nella versione 17.3.1 di Target (marzo 2017).

Il secondo problema è stato risolto nella versione 17.6.1 di Target (giugno 2017).

### at.js 

A partire dalla versione 17.4.1 di Target (27 aprile 2017), se si utilizza l’azione Inserisci immagine nel Compositore esperienza visivo, il contenuto dell’offerta non viene consegnato quando si utilizza la libreria at.js.

Il problema è stato risolto nella versione 0.9.7 di at.js rilasciata il 22 maggio 2017.

### Consigli 

L’elaborazione dei feed Consigli richiede più tempo del previsto. (COR-2836)

Risolto nella versione 16.10.1 di Target.

### Reporting: attività A/B e di Targeting esperienza (XT)

Per le attività A/B e XT create o modificate tra il 27 aprile alle 21:00 PST e il 5 maggio alle 06:00 PST con qualsiasi metrica utilizzando l’azione di conversione “Visualizza una pagina” (non basate su altre metriche), le conversioni potrebbero essere registrate in modo errato. Questo problema ora è risolto, tuttavia, i dati nei rapporti per l’azione di conversione “Visualizzazione di una pagina” per queste attività durante il periodo di tempo indicato, potrebbe non essere accurati e, sfortunatamente, non possono essere corretti. Per queste attività consigliamo di basarsi solo sui dati registrati prima o dopo tale periodo per prendere decisioni basate sulle azioni di conversione “Visualizzazione di una pagina”.

Questo problema non interessa i dati di reporting per altre metriche, che possono quindi essere utilizzati.

Risolto nell’aggiornamento rapido 17.4.3 di Target.

### Offerte: attività A/B e di Targeting esperienza (XT)

Un problema ha interessato la consegna e l’anteprima di offerte in attività A/B e XT con almeno due esperienze e che sono state create o modificate utilizzando il Compositore esperienza basato su moduli tra venerdì 28 aprile (21:00 PT) e lunedì 1 maggio (21:15 PT). Venivano visualizzate solo le offerte con contenuto predefinito.

Risolto nell’aggiornamento rapido 17.4.3 di Target.

### at.js 

Le seguenti azioni hanno causato la mancata consegna dell’offerta collegata all’utilizzo delle funzioni Sposta e Ridisponi del Compositore esperienza visivo e di at.js.

Questo problema è stato risolto nella versione 0.9.6 di at.js.

### Rapporti

La possibilità di visualizzare più metriche in un rapporto, inclusa nella versione 17.3.1 di Target (30 marzo 2017), è stata rimossa a causa di un comportamento imprevisto. Questa funzione sarà nuovamente disponibile in una versione successiva.

La possibilità di visualizzare più metriche in un rapporto è stata inclusa nella versione 17.4.1 di Target (27 aprile 2017).

### Offerte

Le immagini eliminate dalla libreria Offerte immagine (Offerte \&gt; Offerte immagine) rimangono visibili nell’interfaccia utente. In una versione futura, le immagini eliminate non verranno più visualizzate. Nel frattempo, le immagini eliminate vengono visualizzate nell’interfaccia utente, ma presentano lo stato Eliminato . (TGT-23793)

Risolto nella versione 17.4.1 di Target (27 aprile 2017).

### Offerte di reindirizzamento

Per il criterio Visualizzato di recente, le regole dinamiche basate su entità non produrranno alcun consiglio se il parametro entity.id non viene passato alla richiesta mbox. (RECS-6241)

Questo problema è stato risolto con il rilascio della funzionalità Consigli (22 marzo 2018). Dopo il rilascio della funzionalità Consigli, Target ignora le regole dinamiche basate su entità se entity.id non viene passato alla richiesta mbox.

### at.js 

Quando gli utenti tentano di scaricare at.js dalla pagina dei dettagli Implementazioni dopo l’aggiornamento delle impostazioni di at.js, mbox.js viene scaricato al suo posto. (TGT-23069)

Risolto nella versione 17.3.1 di Target (30 marzo 2017).

### Regole di esclusione globale

Le regole di esclusione globale impiegano 10-20 minuti per propagarsi alla rete Edge per Recommendations Premium. (RECS-5270)

Risolto nella versione 17.2.2.0 di Recommendations (6 marzo 2017).

### Reporting di Analytics for Target (A4T)

I rapporti non vengono aggiornati quando si cambia la metrica di reporting. Questo è un problema di interfaccia utente. Non vi è alcun impatto sulla raccolta dei dati di reporting o sulla consegna. (TGT-22970)

Risolto nella versione 17.2.2.0 di Target (24 febbraio 2017).

### Rapporti CSV

I rapporti scaricati non rispettano l’impostazione Escludi ordini estremi. (TGT-21871)

Risolto nella versione 17.2.1.0 di Target.