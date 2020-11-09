---
keywords: known issues;resolved issues;release notes;bugs;issues;fixes
description: Informazioni sui problemi noti per questa versione di Adobe Target. Include inoltre informazioni sui problemi risolti.
title: Problemi noti e problemi risolti in Adobe Target
feature: known issues
uuid: f8e8e057-1842-4922-ab7f-4d5441048573
translation-type: tm+mt
source-git-commit: a05d2a28b7bea3aa559cd0174930af10c6d94134
workflow-type: tm+mt
source-wordcount: '3895'
ht-degree: 78%

---


# Problemi noti e problemi risolti

Informazioni sui problemi noti per questa versione di Target. Include inoltre informazioni sui problemi risolti.

>[!NOTE]
>
>I codici tra parentesi sono per uso interno di Adobe.

## Problemi noti {#section_AEDC98B67CF24C9F8E0CF0D2EB9ACAEF}

Nelle sezioni seguenti sono elencati i problemi noti per [!DNL Target]:

### Metriche di Analytics per Target (A4T) per le attività di allocazione automatica e di targeting automatico

Esiste un problema noto corrente nell&#39; [!DNL Target] interfaccia utente che consente agli utenti di selezionare metriche di coinvolgimento e ricavi non supportate come metrica di obiettivo principale per l&#39;ottimizzazione nelle attività [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target] . Sono supportate le metriche di conversione; le metriche di coinvolgimento e ricavi *non* sono supportate. Se selezionate le metriche dell&#39;obiettivo di coinvolgimento o delle entrate, non verrà creato un modello di ottimizzazione (anche se l&#39; [!DNL Target] interfaccia utente al momento consente di selezionare metriche di obiettivo non supportate).

Per un elenco delle metriche di obiettivo supportate e non supportate, vedi Metriche [di obiettivo](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa) supportate in *Creare un&#39;attività che utilizza Analytics come origine* di reporting. (TNT-38409)

### Consegna delle pagine {#page-delivery}

Se aggiungi una regola del modello, ad esempio l’URL contiene (/checkout, /cart) nella [consegna pagine](/help/c-activities/t-experience-target/t-xt-create/xt-activity-url.md), alla regola vengono anteposti degli spazi in più. Si tratta di un problema cosmetico che non influisce sulla creazione di definizioni di pubblico né sulla consegna delle offerte. (TGT-35920)

### Collegamenti di anteprima QA

I collegamenti di anteprima Controllo di qualità delle attività per le attività salvate potrebbero non venire caricati se nel tuo account sono presenti troppe attività salvate. Riprova a generare i collegamenti di anteprima. Archivia le attività salvate che non vengono più utilizzate attivamente per impedire che il problema continui. (TNT-37294)

### Modalità QA per le attività Recommendations

Un problema noto impedisce l&#39;anteprima se i criteri utilizzati nell&#39;attività sono basati su elementi o categorie. (TNT-37455)

### Offerte di reindirizzamento {#redirect}

Di seguito sono riportati i problemi noti relativi alle offerte di reindirizzamento:

* In alcune condizioni, un numero limitato di clienti ha segnalato maggiore varianza nella distribuzione del traffico quando si utilizza un’offerta di reindirizzamento in attività configurate con Analytics per Target (A4T). Gli ingegneri Adobe stanno indagando su questo problema.
* Alcune attività di reindirizzamento nelle implementazioni at.js possono generare la ripetizione ciclica dell’URL di anteprima (l’offerta viene consegnata ripetutamente). Utilizza la [modalità Controllo qualità](/help/c-activities/c-activity-qa/activity-qa.md) invece di eseguire anteprima e controllo qualità. Questo problema non ha alcun impatto sull’effettiva consegna dell’offerta. (TGT-23019)

### Annullare il caricamento di una pagina all’interno del Compositore esperienza visivo {#cancel}

* Al momento si verifica il seguente problema noto quando si annulla il caricamento di un’attività [!UICONTROL Test A/B] o [!UICONTROL Targeting esperienze] (XT) nel Compositore esperienze visivo in presenza di un URL di reindirizzamento.

   Nel passaggio 1 del flusso di lavoro guidato in tre parti nel Compositore esperienze visivo, durante l’annullamento del caricamento della pagina, viene visualizzato il pannello [!UICONTROL Modifiche] nel Compositore esperienze visivo e viene applicato il modello di reindirizzamento all’URL (ad esempio, “Esperienza B”). Quando ritorni al passaggio 1 dal passaggio 2 o 3, si verifica la seguente situazione.

   In “Esperienza B”, per impostazione predefinita, viene eseguito il rendering del modello di caricamento del sito web annullato e il pannello [!UICONTROL Modifiche] è accessibile. Questo non dovrebbe accadere, perché questa esperienza ha un reindirizzamento al modello di URL applicato. Dovrebbe essere visualizzato il modello di reindirizzamento all’URL.

   Per visualizzare lo stato corretto dell’esperienza nel Compositore esperienza visivo:

   Se passi a un’altra esperienza e quindi torni a “Esperienza B”, [!DNL Target] visualizza il modello di reindirizzamento al modello URL applicato a questa esperienza e il pannello [!UICONTROL Modifiche] non è accessibile. (TGT-32138)

* Per i siti web delle applicazioni a pagina singola, l’annullamento del caricamento non consente di modificare le azioni nel pannello [!UICONTROL Modifiche].

### Consigli

Di seguito sono riportati i problemi noti relativi alle attività Consigli:

* Le entità scadono correttamente una volta trascorsi 60 giorni senza ricevere aggiornamenti tramite feed o API; tuttavia, dopo la scadenza le entità scadute non vengono rimosse dall’indice di ricerca del catalogo. (IRI-857)
* Le sovrapposizioni “Informazioni sull’utilizzo” per i criteri e le progettazioni non riflettono l’utilizzo in attività A/B e Targeting esperienza. (TGT-34331)
* Le offerte Consigli nelle attività A/B e Targeting esperienza non presentano un’anteprima visiva della barra dei consigli. (TGT-33426)
* Le raccolte, le esclusioni, i criteri e le progettazioni creati mediante API non sono visibili nell’interfaccia di Target e possono essere modificati solo tramite API. (TGT-35777)
* Le attività Consigli create tramite API sono visibili nell’interfaccia, ma possono essere modificate solo tramite API.
* Lo stato del feed dei criteri personalizzati visualizzato nell’elenco (scheda) Criteri viene aggiornato ogni dieci minuti e in alcune rare circostanze potrebbe contenere dati risalenti a oltre dieci minuti prima. Lo stato visualizzato nella vista di modifica dei criteri personalizzati viene recuperato in tempo reale ed è sempre aggiornato. (TGT-35896, TGT-36173)

### Attività di test multivariato (MVT)

In un’attività MVT, il vincitore mostrato nella tabella e nel grafico non è coerente quando si controllano le metriche. Questo si verifica se un utente passa dalla visualizzazione Riepilogo alla visualizzazione Grafico, quindi torna alla visualizzazione Riepilogo, modifica una metrica e passa alla visualizzazione Grafico. Quando si verifica questo problema, la visualizzazione Riepilogo mostra sempre il vincitore corretto. Se l’utente non passa mai dalla vista Grafico alla vista Riepilogo, la vista Grafico mostra il vincitore corretto.

### at.js {#atjs}

Di seguito sono riportati problemi noti relativi a at.js:

* Utilizzando le versioni at.js precedenti alla versione 2.2.0, nel monitoraggio dei clic non sono incluse le conversioni in Analytics for Target (A4T) se il codice Adobe Analytics non è presente sugli elementi di pagina (come i pulsanti). Questo problema è stato corretto in at.js 2.2.0. Se riscontri questo problema, [effettua l’aggiornamento all’ultima versione di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).
* Se crei un’esperienza senza modifiche utilizzando at.js 2.1.1 o versioni precedenti (ad esempio, un’esperienza predefinita), questa potrebbe non essere conteggiata nei rapporti, in Analytics for Target (A4T), Adobe Analytics o Google Analytics. Inoltre, il [plug-in ttMeta](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-plugins.md) potrebbe non funzionare correttamente.

   Come soluzione alternativa, inserisci uno spazio vuoto nel contenuto dell’esperienza. (TNT-33366)

   >[!NOTE]
   >
   >Questo problema è stato corretto in at.js 2.2.0. Esegui l’aggiornamento all’[ultima versione di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) oppure, solo per le versioni di at.js precedenti alla 2.2.0, utilizza la soluzione alternativa indicata qui sopra.

* Quando si carica una pagina nel Compositore esperienza visivo, Target deve determinare se l’impostazione mbox globale è abilitata o disabilitata e se entityID o categoryID è presente nel percorso in cui l’utente sta tentando di applicare il consiglio nel Compositore esperienza visivo. L’elenco dei criteri viene filtrato sulla base di queste informazioni. L’elenco predefinito contiene algoritmi filtrati, ma la casella di controllo [Compatibile](/help/c-recommendations/t-create-recs-activity/algo-select-recs.md) consente di visualizzare l’elenco completo degli algoritmi.

   Quando si utilizza at.js, la casella di controllo Compatibilità è nascosta e non è quindi possibile visualizzare gli algoritmi non compatibili.

   Questo problema è relativo solo alle attività Consigli che utilizzano il Compositore esperienza visivo.

   **Soluzione alternativa**: disabilita l’opzione [!UICONTROL Filtra criteri incompatibili] in [!UICONTROL Recommendations > Impostazioni]. Dopo aver disabilitato questa impostazione, nel selettore dei criteri verranno visualizzati tutti i criteri (compatibili e non). (TGT-25949)

* Dopo l’aggiornamento alla versione 1.0 di at.js, le mbox non funzionano nei browser Microsoft Explorer 11 a causa dell’interazione tra at.js e Visitor API 2.2.0. Questo problema riguarda le versioni 0.9.6 e successive di at.js. (TNT-27600)
* at.js potrebbe non funzionare con le app Cordova/Hybrid perché non supportano i cookie di prima parte. (TNT-26166)

   **Soluzione alternativa**: configura at.js con l’opzione “Solo x” attivata e passa `mboxThirdPartyId` nelle chiamate per la gestione degli utenti.

### Metriche di successo

Le metriche di successo con l’opzione avanzata “Come verrà incrementato il conteggio?” impostata su “A ogni impression” o “A ogni impression (esclusi aggiornamenti pagina)” non possono essere utilizzate come metriche di successo da cui dipende un’altra metrica.

Quando una metrica di successo è impostata per essere incrementata a ogni impression, Target conta il visitatore ogni volta che visita questa metrica di successo. Quindi, Target reimposta su 0 la metrica di successo “Appartenenza” in modo da contare di nuovo l’impression successiva. Pertanto, se un’altra metrica richiede che questa metrica sia stata vista per prima, Target non è in grado di capire se l’utente ha visto la prima metrica.

### Analytics for Target (A4T)

Quando utilizzi impression e conversioni dell&#39;attività Target in  Analysis Workspace, applica il modello di Attribution IQ  &quot;Same Touch&quot; alle metriche per garantire un conteggio accurato. Per applicare un modello [di attribuzione](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/column-row-settings/column-settings.html)non predefinito, fai clic con il pulsante destro del mouse sulla metrica per **modificare le Impostazioni colonna > abilita Usa modello di attribuzione non predefinito > Seleziona Modello** di attribuzione simile. Senza l&#39;applicazione di questo modello, le metriche sono sopravvalutate.

Tutti i pacchetti Analytics correnti possono aggiungere questo modello con  Attribution IQ. Se non avete accesso alle  Attribution IQ, fate affidamento sui dati A4T in Reporting e analisi.

### API di Target

I clienti non possono eseguire operazioni CRUD sulle attività di allocazione automatica tramite la versione v3 dell’API A/B Activities in Adobe I/O.

### Targeting GEO

Il 10 maggio 2020 abbiamo aggiornato i file del nostro provider GEO, che hanno introdotto alcune incongruenze. Ad esempio, sono stati aggiunti alcuni valori contenenti virgole; anche se, i valori nelle audience esistenti non avevano una virgola. Questa modifica non ha interessato tutti i server di distribuzione. Di conseguenza, tra il 10 maggio e il 22 luglio 2020 l&#39;audience che utilizza tali valori potrebbe non avere qualificato tutti i visitatori corretti.

### Offerte di immagini che mostrano l&#39;etichetta &quot;Elaborazione&quot;

Le offerte di immagini nella pagina Offerte talvolta mantengono l’etichetta di &quot;elaborazione&quot; per diverse ore dopo il caricamento delle immagini. Nella maggior parte dei casi si tratta di un problema relativo solo all&#39;etichetta: le offerte di immagini possono essere ancora utilizzate nelle attività e distribuite. In alcuni casi, tuttavia, un’offerta immagine potrebbe non essere disponibile per l’azione Sostituisci contenuto > Immagine. In questo caso, caricate di nuovo l’offerta immagine e verificate dopo alcune ore se l’offerta è disponibile per la sostituzione. (TGT-37458)

## Problemi risolti {#section_FD2FC86E7C734D60B1EDC9DEF60E1014}

Man mano che i suddetti problemi noti vengono risolti, saranno spostati nella sezione seguente e verranno eventualmente integrati con note aggiuntive.

### Generazione di rapporti con targeting automatico {#at-metrics}

È stato risolto un problema che interessava la generazione di rapporti su [!DNL Adobe Target Premium] Auto-Target  degli utenti a partire dal 15 settembre alle 14:30. (PDT) al 6 ottobre, 9:25 (PDT). Quando visualizzate i rapporti per le metriche di conversione interessate (configurate utilizzando l&#39;opzione &quot;[!UICONTROL Visualizzato una pagina]&quot; o &quot;[!UICONTROL Premuto su mbox]&quot;), i tassi di conversione vengono segnalati in modo non corretto. Nessun problema di consegna noto al momento.

Per risincronizzare e correggere il reporting:

1. Copiate e salvate le attività [!UICONTROL Auto-Target] interessate.
1. Attiva le attività salvate di recente (se le attività interessate sono live).
1. Eliminate le attività originali (interessate).

(TGT-38522, CSO 20201006007)

### Generazione di rapporti {#conversions-audiences}

Le conversioni al momento aumentano in modo diverso in base al tipo di pubblico utilizzato.

Ad esempio, per lo stesso visitatore, se il conteggio di conversione è impostato per incrementare &quot;Once per Entrant:&quot;

* Pubblico: Per le conversioni a livello di visita, &quot;Tutti i visitatori qualificati&quot; incrementano una sola volta. Questo è il comportamento previsto.
* Pubblico: &quot;Nuovi visitatori&quot; per le conversioni a livello di visita aumentano in modo errato ogni volta, invece di incrementare solo una volta. Questo non è il comportamento previsto.

Se il conteggio di conversione è impostato per incrementare &quot;Su ogni impressione:&quot;

* Pubblico: &quot;Tutti i visitatori qualificati&quot; per le conversioni a livello di visitatore, l’incremento non è corretto e non è sufficiente una sola volta, bensì ogni volta. Questo non è il comportamento previsto.
* Pubblico: &quot;Nuovi visitatori&quot; per le conversioni a livello di visitatore vengono incrementate ogni volta. Questo è il comportamento previsto.

Questo problema è correlato solo alla [!DNL Target] generazione di rapporti. Questo non è un problema quando si utilizza il reporting di [!UICONTROL Analytics per Target] (A4T).

Questo problema è stato risolto.

### Pagine non caricate in Visual Experience Composer (VEC) o Enhanced Experience Composer (EEC) quando si utilizza Google Chrome versione 80+

Questo problema noto riguarda la decisione di Google di modificare il comportamento predefinito dei cookie senza l&#39;attributo SameSite a partire da Chrome versione 80. Prima della modifica, Chrome aveva impostato tutti i cookie senza l&#39;attributo SameSite su &quot;SameSite=None&quot; per impostazione predefinita e ora su &quot;SameSite=Lax&quot; per impostazione predefinita, modificando il modo in cui i cookie vengono inviati sulle richieste di GET e POST. Consultate Aggiornamenti [](https://www.chromium.org/updates/same-site)SameSite.

Per ulteriori informazioni e una correzione, vedere &quot;In che modo le politiche di applicazione dei cookie Google Chrome SameSite recentemente annunciate influiscono sul VEC e la CEE?&quot; in [Troubleshooting Issues Related to the Visual Experience Composer and Enhanced Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

### Il rapporto grafico per un’attività di Targeting automatico non viene riprodotto correttamente quando si utilizza come controllo un’esperienza personalizzata.

Il rapporto grafico per un’attività di Targeting automatico non viene riprodotto correttamente per le modalità “differenziali” (Incremento medio e Incremento giornaliero) in assenza di dati (visite 0) in qualsiasi esperienza. Questa situazione può verificarsi nella fase iniziale di un’attività quando si utilizza come controllo un’esperienza personalizzata. Per le altre modalità (Media corrente per controllo e destinazione, Giornaliero per controllo e destinazione, Visite) funziona correttamente. Non appena sono presenti alcuni dati (numero di visite diverso da zero), il rapporto viene riprodotto come previsto.

Questo problema è stato risolto con la versione 19.7.1 di Target. 

### mbox.js

La libreria mbox.js non supporta linguaggi di template lato client, come Handlebar e Mustache. La libreria at.js *supporta* tali linguaggi.

**Nota**: la libreria mbox.js non verrà più sviluppata. Tutti i clienti devono migrare da mbox.js a at.js. Per ulteriori informazioni, consulta [Migrazione a at.js da mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA).

### Implementazione: Creazione automatica mbox globale

On the Implementation tab ([!UICONTROL Administration > Implementation]) the [!UICONTROL Global Mbox Auto Create] field will be &quot;false&quot; by default for a newly provisioned tenant.

Quando mbox.js viene scaricato per la prima volta dopo il provisioning, il campo [!UICONTROL Creazione automatica mbox globale] è impostato su “true” nel file mbox.js scaricato e nel backend di [!DNL Target], ma continua a mostrare “false” nella pagina [!UICONTROL Implementazione] dell’interfaccia utente fino a quando la pagina non viene aggiornata (dopo l’aggiornamento della pagina, lo stato diventa “true”).

at.js verrà scaricato con `global_mbox_autocreate = false` per un tenant nuovo. Se mbox. js viene scaricato per primo, global\_mbox\_autocreate è impostato su “true” e anche at.js sarà scaricato con `global_mbox_autocreate = true`. (TGT-15929)

### Supporto delle autorizzazioni Enterprise nelle API di Target {#api}

Le offerte di codice create dall’interfaccia utente di Target nella libreria Offerte possono essere visualizzate nell’area di lavoro predefinita se l’elenco delle offerte viene rimosso utilizzando API GET. Il problema verrà risolto nella prima settimana di marzo 2019. Dopo la correzione, le offerte di codice verranno visualizzate nell’area di lavoro appropriata quando vengono richiamate dalle API. Questo problema *non* influisce sulle offerte create dalle API. Ad esempio, le offerte di codice create dalle API vengono visualizzate nell’area di lavoro in cui sono state create o recuperate utilizzando API GET o dall’interfaccia utente di Target.

### Generazione di rapporti e ordini estremi

Dal 25 novembre 2019 al 26 aprile 2020, un server di Target ha riscontrato un problema che ha portato a conteggiare i valori degli ordini estremi nelle metriche dei report basate sulle entrate (AOV, RPV). Dal 19 dicembre 2019 al 23 aprile 2020, un altro server ha riscontrato lo stesso problema. Questo problema non ha interessato tutti i server Target o tutti i clienti Target.

L&#39;utente *non* è stato interessato se:

* L&#39;implementazione di Target utilizza server diversi.
* I rapporti non escludevano ordini estremi.
* È stata utilizzata una metrica di conversione per misurare le attività.
* Le attività Target utilizzano Analytics per Target (A4T).
* Si trova la regione Asia-Pacifico (APAC).

Per determinare se questo problema ha avuto un impatto sui report di Target, rivolgiti a [Client Care](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB).

### Consigli

* L’indice del feed di Recommendations può mostrare il messaggio “In attesa dell’indice” se gli elementi nel feed sono identici a quelli della precedente esecuzione. Questo non influisce sull’assimilazione del prodotto per la consegna. (RECS-6663)

   Questo problema è stato risolto con la versione 19.4.2 di Target. 

* L’elaborazione dei feed Consigli richiede più tempo del previsto. (COR-2836)

   Risolto nella versione 16.10.1 di Target.

* L’interfaccia dei feed della funzionalità Consigli non mostra lo stato di indicizzazione corretto. I processi di backend funzionano correttamente, ma non è possibile recuperare e visualizzare nell’interfaccia utente lo stato corrente.

   Questo problema è stato risolto nella versione 17.10.1.

### Offerte di reindirizzamento

Una situazione di tipo “race condition” può determinare un conteggio delle visualizzazioni di pagina sia nella pagina originale sia in quella di reindirizzamento. Sono previsti aggiornamenti per l’implementazione di at.js in modo da evitare tale situazione di tipo “race condition”. 

Questo problema è stato risolto in at.js 1.6.3.

### Gruppi di esclusione

* Quando viene applicata la deduplicazione automatica dopo la creazione di gruppi di esclusione, il conteggio nel diagramma dell’attività potrebbe non essere corretto nell’interfaccia utente.
* Quando si modifica un’attività esistente di un gruppo di esclusione, le inclusioni manuali potrebbero non essere riportate correttamente nell’interfaccia utente.

Questi problemi sono stati risolti.

### API di Target

La versione v1 delle API Offer su Adobe I/O considera tutte le offerte create tramite Target come nell’area di lavoro predefinita. (TTTEAM-41957)

Questo problema è stato risolto.

### at.js {#at-js-2}

Dopo l’aggiornamento alla versione 1.0 di at.js, le mbox non funzionano nei browser Microsoft Explorer 11 a causa dell’interazione tra at.js e Visitor API 2.2.0. Questo problema riguarda le versioni 0.9.6 e successive di at.js. (TNT-27600)

Risolto con il rilascio della versione 2.3.0 o successive dell’API.

### Geotargeting

La ricerca di una stringa contenente caratteri speciali (ad esempio uno spazio o una virgola) non è attualmente supportata durante la creazione di tipi di pubblico di geotargeting. Questo problema affiora, ad esempio, quando si creano tipi di pubblico basati su città, stati, paesi, ecc. Ad esempio, quando si cerca “new york”, la ricerca non restituisce risultati validi.

Corretto a novembre 2018.

### at.js {#at-js-3}

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

Questo problema è stato risolto nella versione 18.9.1.

### Attività Consigli che utilizza una regola di promozione attributi

Quando si modifica o si copia un&#39;attività di Consigli che utilizza una regola di promozione attributi, viene visualizzato l&#39;errore “Campo mancante” quando si fa clic su Salva.

Questo problema è stato risolto nella versione 17.8.1.

### Consigli di backup

I consigli di backup mostrano erroneamente lo stato “Abilitato” nelle schede degli articoli visualizzati di recente nell’interfaccia utente di Target. (TGT-29308)

Ciò è stato corretto nella versione 18.4.1 in modo che venga visualizzato “Disattivato”.

### Attività Auto-Target e tipi di pubblico per rapporti

Quando viene modificato il nome di un pubblico per la creazione di rapporti utilizzato in un&#39;attività Auto-Target, gli aggiornamenti successivi da Target per quell&#39;attività potrebbero non essere inclusi e comparirà un messaggio di errore.

Questo problema è stato risolto con la versione 18.5.1 (22 maggio 2018).

### at.js {#at-js-4}

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

### at.js {#at-js-5}

A partire dalla versione 17.4.1 di Target (27 aprile 2017), se si utilizza l’azione Inserisci immagine nel Compositore esperienza visivo, il contenuto dell’offerta non viene consegnato quando si utilizza la libreria at.js.

Il problema è stato risolto nella versione 0.9.7 di at.js rilasciata il 22 maggio 2017.

### Reporting: attività A/B e di Targeting esperienza (XT)

Per le attività A/B e XT create o modificate tra il 27 aprile alle 21:00 PST e il 5 maggio alle 06:00 PST con qualsiasi metrica utilizzando l’azione di conversione “Visualizza una pagina” (non basate su altre metriche), le conversioni potrebbero essere registrate in modo errato. Questo problema ora è risolto, tuttavia, i dati nei rapporti per l’azione di conversione “Visualizzazione di una pagina” per queste attività durante il periodo di tempo indicato, potrebbe non essere accurati e, sfortunatamente, non possono essere corretti. Per queste attività consigliamo di basarsi solo sui dati registrati prima o dopo tale periodo per prendere decisioni basate sulle azioni di conversione “Visualizzazione di una pagina”.

Questo problema non interessa i dati di reporting per altre metriche, che possono quindi essere utilizzati.

Risolto nell’aggiornamento rapido 17.4.3 di Target.

### Offerte: attività A/B e di Targeting esperienza (XT)

Un problema ha interessato la consegna e l’anteprima di offerte in attività A/B e XT con almeno due esperienze e che sono state create o modificate utilizzando il Compositore esperienza basato su moduli tra venerdì 28 aprile (21:00 PT) e lunedì 1 maggio (21:15 PT). Venivano visualizzate solo le offerte con contenuto predefinito.

Risolto nell’aggiornamento rapido 17.4.3 di Target.

### at.js {#at-js-6}

Le seguenti azioni hanno causato la mancata consegna dell’offerta collegata all’utilizzo delle funzioni Sposta e Ridisponi del Compositore esperienza visivo e di at.js.

Questo problema è stato risolto nella versione 0.9.6 di at.js.

### Rapporti

La possibilità di visualizzare più metriche in un rapporto, inclusa nella versione 17.3.1 di Target (30 marzo 2017), è stata rimossa a causa di un comportamento imprevisto. Questa funzione sarà nuovamente disponibile in una versione successiva.

La possibilità di visualizzare più metriche in un rapporto è stata inclusa nella versione 17.4.1 di Target (27 aprile 2017).

### Offerte

Le immagini eliminate dalla libreria Offerte immagine (Offerte > Offerte immagine) rimangono visibili nell’interfaccia utente. In una versione futura, le immagini eliminate non verranno più visualizzate. Nel frattempo, le immagini eliminate vengono visualizzate nell’interfaccia utente, ma presentano lo stato Eliminato. (TGT-23793)

Risolto nella versione 17.4.1 di Target (27 aprile 2017).

### Offerte di reindirizzamento

Per il criterio Visualizzato di recente, le regole dinamiche basate su entità non produrranno alcun consiglio se il parametro entity.id non viene passato alla richiesta mbox. (RECS-6241)

Questo problema è stato risolto con il rilascio della funzionalità Consigli (22 marzo 2018). Dopo il rilascio della funzionalità Consigli, Target ignora le regole dinamiche basate su entità se entity.id non viene passato alla richiesta mbox.

### at.js {#at-js-7}

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
