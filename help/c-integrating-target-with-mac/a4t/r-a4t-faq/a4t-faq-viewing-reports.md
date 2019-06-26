---
description: Questo argomento contiene le risposte alle domande che vengono spesso poste in merito alla visualizzazione dei rapporti durante l’utilizzo di Analytics come origine per la creazione di rapporti per Target (A4T).
keywords: FAQ;domande frequenti;analytics for target;a4t;rapporto;report;visualizzare rapporti;reporting;metodologia di conteggio;impression;visitatori;visite;metriche predefinite;conversioni di attività;non specificato
seo-description: Questo argomento contiene le risposte alle domande che vengono spesso poste in merito alla visualizzazione dei rapporti durante l’utilizzo di Analytics come origine per la creazione di rapporti per Target (A4T).
seo-title: Visualizzare i rapporti - Domande frequenti su A4T
solution: Target
title: Visualizzare i rapporti - Domande frequenti su A4T
topic: Standard
uuid: d51991f7-cdda-4a59-b64c-7ef1c3f8380d
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Visualizzare i rapporti - Domande frequenti su A4T{#view-reports-a-t-faq}

Questo argomento contiene le risposte alle domande che vengono spesso poste in merito alla visualizzazione dei rapporti durante l’utilizzo di Analytics come origine per la creazione di rapporti per Target (A4T).

## Qual è la metodologia di conteggio e come si usa? {#section_E9C21C47B5BE4E54BABF0CD7F03D3945}

La metodologia di conteggio specifica quale valore deve essere utilizzato da Target come denominatore per i tassi di conversione. Le scelte sono:

* impression
* visitatori
* visite

## È possibile impostare una metrica predefinita per i rapporti di Target? {#section_50C20D286AA042CCA958184C9C0767DD}

Per il rapporto Attività, gli amministratori possono modificare la metrica predefinita in modo da visualizzare le stesse metriche ogni volta che eseguono il rapporto. In caso contrario, per impostazione predefinita il rapporto utilizza l’ultima metrica applicata all’ultimo rapporto.

Per ulteriori informazioni, consulta [Selezionare la metrica predefinita di un rapporto](https://marketing.adobe.com/resources/help/en_US/sc/user/t_metrics_set_default.html) nella guida *Aiuto per l’interfaccia di Reports and Analytics*.

## Quando si applica un segmento alla metrica (con una metrica calcolata) rispetto a un segmento al rapporto? {#section_BC29DEE6D2734911A5CD6FBF1189EB89}

L’applicazione dei ai rapporti è simile all’applicazione di segmenti nell’interfaccia classica di Target. Questa tecnica è molto utile per vedere come un test interessa un sottoinsieme di persone (ad esempio, per verificare il test per i cittadini del Regno Unito).

È possibile applicare segmenti alla metrica con una metrica calcolata. Questa operazione viene generalmente eseguita se desideri creare un nuovo tipo di evento di successo. Ad esempio, permette di vedere quanti visitatori di ritorno ha generato l’attività o quanti dei visitatori che hanno visto il test hanno poi visitato una determinata pagina. Al momento, per le metriche calcolate non è possibile generare incremento e affidabilità.

## È necessario utilizzare visitatori, impression di attività o visite durante la visualizzazione dei rapporti? {#section_46D0CC450B414B4DA6853BFFEE87D7BE}

Ci sono diverse opzioni, ognuna con i propri vantaggi:

* I ***visitatori univoci*** incrementano una volta quando un utente si qualifica per la prima volta per un&#39;attività.
* Le ***visite*** incrementano per ogni sessione una volta che un utente (Visitatore unico) entra in un&#39;attività, anche se l&#39;attività non viene visualizzata nelle visite successive.
* Le ***impressioni dell’attività*** aumentano ogni volta che il contenuto dell&#39;attività viene servito. (Misurate da Target)
* Le ***istanze*** incrementano una volta per pagina quando viene servito il contenuto dell’attività. (Misurate da Analytics)

Quando un visitatore visualizza una pagina che contiene un&#39;attività, viene impostata una variabile per quel visitatore che contiene il nome di tale attività. Consulta gli scenari dettagliati di seguito per il confronto di ciascuna metodologia di conteggio.

Valuta quanto segue:

* Tutte le metriche sopra indicate si attivano quando un utente si qualifica per un&#39;attività e il contenuto viene restituito da [!DNL Target]. Ciò non significa necessariamente che l&#39;utente abbia visto l&#39;offerta. Se l&#39;esperienza di un’attività si trova nella parte inferiore della pagina e l&#39;utente non scorre la pagina verso il basso, allora l&#39;offerta è stata servita da [!DNL Target] ma non è stata vista dall&#39;utente.
* Le [!UICONTROL impressioni dell’attività] (misurate da [!DNL Target]) e le [!UICONTROL istanze] (misurate da [!DNL Analytics]) sono uguali, a meno che non vi siano più chiamate mbox sulla stessa pagina nella stessa attività. In tal caso si contano più [!UICONTROL impressioni dell’attività], ma solo una singola [!UICONTROL istanza].
* Attualmente le metriche [!UICONTROL Impressioni dell’attività] e [!UICONTROL Conversione dell’attività] vengono gonfiate in [!DNL Analysis Workspace] e non devono essere utilizzate fino a quando il problema non viene risolto.

## Che cosa significa “conversioni di attività” se l’addetto al marketing sceglie una metrica di Analytics durante l’impostazione dell’attività? {#section_F3EBACF85AF846E9B366A549AAB64356}

Le “Conversioni attività” sono vuote se è stata selezionata una metrica di Analytics come metrica di conversione per l’attività.

## Perché è indicato “non specificato” nei rapporti di Analytics? Che cosa significa? {#section_AF38D32DAFEF4DDD95E07424CF682CCA}

![](assets/unspecified.png)

In altri rapporti, “non specificato” significa che i dati non soddisfano una regola di classificazione, ma in A4T non dovrebbe mai verificarsi. Se viene visualizzato “non specificato”, il servizio di classificazione non è ancora stato eseguito. La visualizzazione dei dati relativi all’attività nei rapporti può richiedere fino a 36 ore. Anche se le attività non compaiono in questo rapporto fino a quel momento, tutti i dati dei visitatori legati a tali attività vengono acquisiti e compariranno quando la classificazione sarà completata.

Dopo il periodo di classificazione, i dati sono visualizzati in questi rapporti circa un&#39;ora dopo essere stati raccolti dal sito. Tutte le metriche, i segmenti e i valori nei rapporti provengono dalla suite di rapporti selezionata quando si configura l’attività.

## Perché le metriche di Target vengono inviate ad Analytics anche dopo la disattivazione dell’attività? {#section_38AA8380A4D54A18972F1EF3E73E22EF}

La variabile di [!DNL Target] inviata ad [!DNL Analytics] ha un periodo di scadenza predefinito di 90 giorni. Se necessario, questo periodo di scadenza può essere regolato dall’Assistenza clienti. Tuttavia, questa impostazione è globale per tutte le attività, quindi non deve essere regolata per un solo caso.

Le variabili di Target potrebbero essere inviate ad Analytics anche oltre il periodo di scadenza: i 90 giorni di scadenza, infatti, sono calcolati dalla visualizzazione di una qualsiasi attività di Target abilitata per A4T. Se un utente torna al sito dopo 45 giorni e visualizza un’altra attività, l’intero valore eVar di A4T viene ripristinato e i 90 giorni ripartono da tale momento. In questo caso, la prima campagna dal giorno 1 potrebbe quindi durare fino a 45 + 90 = 135 giorni. Se l’utente continua a tornare, si potrebbe arrivare al punto in cui è possibile visualizzare metriche inviate ad Analytics nel rapporto da attività molto più vecchie. Man mano che gli utenti eliminano i cookie e non tornano sul sito, i numeri per quell’attività diminuiranno, ma sarà comunque possibile visualizzarli ancora.

Ciò significa che le attività continuano a ricevere visualizzazioni di pagina, visite e così via fino a 90 giorni dopo il termine dell’attività, per i visitatori che vi hanno partecipato mentre l’attività era attiva. Tuttavia, se osservi la metrica di [!UICONTROL Impression attività], non dovresti più vedere impression dopo la fine dell’attività.

Questo è un comportamento normale e atteso. La variabile A4T funziona come qualsiasi altro eVar: il valore è associato all’utente finché non raggiunge il periodo di scadenza (90 giorni). Di conseguenza, se un’attività è attiva solo per due settimane, il valore sarà comunque associato all’utente per almeno i prossimi 90 giorni.

Si consiglia di visualizzare i rapporti per tale attività solo per il periodo di tempo in cui era in corso. Le date devono essere impostate correttamente da impostazione predefinita quando visualizzi l’attività in Analytics, quindi, a meno che non si estenda manualmente la data, non dovrebbe essere un problema per i rapporti.

Ad esempio, supponiamo che la variabile A4T scada dopo 90 giorni e che il nostro test sia attivo dal 1° gennaio al 15 gennaio.

Il 1° gennaio, l’utente entra nel sito, vede l’attività XYZ una volta e visualizza cinque pagine. Nelle due settimane successive, l’utente non ritorna più sul sito. Per questo utente i dati saranno di questo tipo:

| Nome attività | Istanze (impression) | Visualizzazioni pagina | Visite | Visitatori univoci |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 5 | 1 | 1 |

L’utente torna il 1° febbraio, visualizza altre cinque pagine, non incontra altre attività di Target e l’attività originale non è più attiva. Anche se l’attività non è più attiva, continua a seguire l’utente tramite la persistenza eVar. I dati ora si presentano così:

| Nome attività | Istanze (impression) | Visualizzazioni pagina | Visite | Visitatori univoci |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 10 | 2 | 1 |

L’utente torna il 1° marzo e vede una nuova attività: ABC. Anche questa volta l’utente visualizza cinque pagine. Poiché l’attività XYZ continua a seguire l’utente tramite la persistenza e per l’utente è stato quindi impostato ABC, vedremo due voci nel rapporto:

| Nome attività | Istanze (impression) | Visualizzazioni pagina | Visite | Visitatori univoci |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 15 | 3 | 1 |
| ABC | 1 | 5 | 1 | 1 |


L’utente poi torna il 1° aprile, visualizza altre cinque pagine ed effettua un acquisto. La scadenza di 90 giorni di quel primo valore eVar viene reimpostata a partire dal 1° aprile, quindi sarà riportato nel rapporto. Tutte le attività di Target che l’utente ha visto ricevono credito per la conversione, ma il numero totale di conversioni viene deduplicato:

| Nome attività | Istanze (impression) | Visualizzazioni pagina | Visite | Visitatori univoci | Ordini |
|--- |--- |--- |--- |--- |--- |
| XYZ | 1 | 20 | 4 | 1 | 1 |
| ABC | 1 | 10 | 2 | 1 | 1 |
| Totale | 2 | 20 | 3 | 1 | 1 |

Poiché entrambe le esperienze sono state viste prima della conversione, entrambe ottengono &quot;credito&quot; per l’ordine. Tuttavia, nel sistema è stato effettuato un solo ordine e il totale riflette questa situazione. Ai fini del rapporto generato da Target, poiché non si stanno confrontando due attività di Target per vedere quale ha più successo, non ha importanza se tutte le attività che l’utente ha visualizzato abbiano ricevuto credito. Si confrontano i risultati di due elementi all’interno della singola attività e non è possibile per un utente vedere diverse esperienze nella stessa attività, quindi non vi è alcun rischio di contaminazione incrociata del credito attribuito per l’ordine.

Per ulteriori informazioni, consulta [Variabili di conversione (eVar)](https://marketing.adobe.com/resources/help/en_US/reference/conversion_var_admin.html) nell’Aiuto di Analytics.

## Perché Analytics e Analytics for Target (A4T) calcolano i numeri per la metrica Visitatori univoci in modo diverso? {#section_0C3B648AB54041F9A2AA839D51791883}

Quando si esegue un test A/B, che utilizza il test t di Student (la metrica di affidabilità) per scegliere un vincitore di un test, uno dei presupposti è che ci sia un orizzonte temporale fisso. Il test non è statisticamente valido a meno che tu non stia esaminando la dimensione del campione fisso.

La metrica Visitatori univoci è diversa in Analytics e Target solo quando si considera un periodo di tempo più breve del test effettivo. Se non hai raggiunto la dimensione del campione, il test non è affidabile. Per ulteriori informazioni, consulta [How Not to Run an A/B Test](https://www.evanmiller.org/how-not-to-run-an-ab-test.html) (Come non eseguire un test A/B) sul [sito web di Evan Miller](https://www.evanmiller.org/index.html).

La metrica Visitatori univoci visualizza il numero di persone che sono state esposte al test e che hanno visitato il sito durante il periodo di tempo specificato. Queste persone sono ancora parte del test e dovrebbero essere conteggiate. Se si desidera visualizzare solo il numero di persone esposte durante una sola settimana, è possibile creare un segmento di visitatori per i quali è stata registrata un’impression di attività e applicare tale segmento al rapporto.

Si può ridurre la durata della variabile di Target a una sola sessione; tuttavia questo può risultare problematico per i test in cui è poco probabile che l’evento di conversione si verifichi nel corso di una stessa sessione.

## Perché lo stesso visitatore a volte viene conteggiato in più esperienze in Analytics? {#section_1397E972D31C4207A142E4D2D6D794A2}

Di seguito sono elencati i motivi per cui lo stesso visitatore potrebbe essere conteggiato in più esperienze in Analytics:

* Il profilo di Target è scaduto ma è ancora presente il cookie di Analytics. In questa situazione, Target rivaluta l’utente, ma Analytics considera il visitatore come la stessa persona.
* Se il visitatore utilizza l’ID `mbox3rdPartyId`, quando il visitatore anonimo viene unito al suo profilo ID di terze parti, Target potrebbe porre il visitatore in un’esperienza diversa per farlo corrispondere all’ID di terze parti. Per ulteriori informazioni, consulta [Sincronizzazione dei profili in tempo reale per mbox3rdPartyID](../../../c-target/c-visitor-profile/3rd-party-id.md#concept_BF4113593F614987B1D3E359AE1C5732).
* Analytics potrebbe tracciare dispositivi diversi associandoli allo stesso visitatore in un modo diverso da come Target traccia tali dispositivi, in quanto l’impostazione dell’ID di terze parti in Target è diversa da quella di Analytics.

## A4T supporta le suite di rapporti virtuali?

Le suite di rapporti virtuali *non* sono incluse nell’elenco Suite di rapporti e i tipi di pubblico di suite di rapporti virtuali non sono supportati nelle funzioni di reporting di A4T.

## Posso cambiare la percentuale di allocazione del traffico in un’attività che utilizza A4T dopo che l’attività è stata attivata?

La modifica della percentuale di allocazione del traffico in un’attività dopo l’attivazione può causare rapporti non coerenti in Analytics, perché la modifica interessa solo i nuovi visitatori. I visitatori di ritorno non sono interessati da tale modifica.

Come procedura ottimale, devi arrestare l’attività esistente, quindi creare una nuova attività invece di modificare la percentuale dopo l’attivazione. La creazione di rapporti per la nuova attività inizia con nuovi visitatori e i dati da visitatori di ritorno non causeranno un reporting incoerente.

## Posso visualizzare i dati di attività Target in Adobe Analysis Workspace?

Puoi utilizzare [!DNL Adobe Analysis Workspace] per approfondire e visualizzare i dati o individuare informazioni nascoste sotto la superficie.

For detailed information and examples, open the [Analytics &amp; Target: Best Practices for Analysis tutorial](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), provided by Adobe Experience League.