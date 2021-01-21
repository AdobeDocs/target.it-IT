---
keywords: faq;frequently asked questions;analytics for target;a4T;report;reports;view reports;reporting;counting methodology;impressions;visitors;visits;default metric;activity conversions;unspecified
description: Questo argomento contiene le risposte alle domande che vengono spesso poste in merito alla visualizzazione dei rapporti durante l’utilizzo di Analytics come origine per la creazione di rapporti per Target (A4T).
title: Visualizzare i rapporti - Domande frequenti su A4T
feature: a4t troubleshooting
translation-type: tm+mt
source-git-commit: 541adbdf8a2512761fc3f2f676cabec085b6825a
workflow-type: tm+mt
source-wordcount: '2347'
ht-degree: 54%

---


# Visualizzare i rapporti - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande frequenti sulla visualizzazione dei rapporti quando si utilizza [!DNL Analytics] come origine di reporting per [!DNL Target] (A4T).

## Posso visualizzare i dati di attività Target in Analysis Workspace? {#workspace}

È possibile utilizzare [!DNL Analysis Workspace] per analizzare le attività e le esperienze [!DNL Target]. Il pannello [Analytics for Target](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html) consente di visualizzare tre metriche di successo con un livello di affidabilità e di incremento. Puoi anche approfondire la ricerca utilizzando tabelle e visualizzazioni.

Per informazioni dettagliate ed esempi, aprite [Analytics &amp; Target: Esercitazione sulle best practice per l&#39;analisi](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), fornita da  Adobe Experience League.

## Dove si possono applicare i segmenti in  Analysis Workspace? {#segmentation}

I segmenti vengono applicati più comunemente nella parte superiore di un pannello nella zona di rilascio del segmento. Il segmento viene applicato a tutte le tabelle e le visualizzazioni nel pannello. Questa tecnica è particolarmente utile per vedere in che modo il test interessa un sottoinsieme di persone (ad esempio, come è stato eseguito questo test per le persone nel Regno Unito)?

## Quando applico un segmento di hit per una specifica attività Target, perché viene restituita un&#39;esperienza non correlata? {#activity-segmentation}

La variabile di [!DNL Target] inviata ad [!DNL Analytics] ha un periodo di scadenza predefinito di 90 giorni. (Nota: se necessario, tale periodo di scadenza può essere regolato dall&#39;Assistenza clienti). Quando i visitatori navigano nel sito attraverso questa finestra di scadenza, fanno parte di molte attività [!DNL Target], tutte raccolte nella dimensione.

Di conseguenza, quando segmentate la presenza di un&#39;attività in un hit, otterrete tutte le esperienze che fanno parte di tale attività *più* tutte le altre esperienze che persistono su tale hit.

## Durante la configurazione delle metriche obiettivo, perché non è possibile accedere alle impostazioni avanzate?

Per le attività che utilizzano [!DNL Analytics] come origine di reporting (A4T), la metrica di obiettivo utilizzerà sempre le impostazioni &quot;[!UICONTROL Increment Count &amp; Keep User in Activity]&quot; e &quot;[!UICONTROL On Every Impression]&quot;. È possibile configurare *not*.

Per ulteriori informazioni, vedere &quot;Durante la configurazione delle metriche degli obiettivi, perché non è possibile accedere alle opzioni delle impostazioni avanzate?&quot; in [Definizioni metriche - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

## È necessario utilizzare i visitatori, le visite o le impression dell&#39;attività come metrica di normalizzazione (ad es. metodologia di conteggio)? {#metrics}

Esistono diverse opzioni per normalizzare le metriche nel reporting A4T. Questa metrica, detta anche metodologia di conteggio, diventa il denominatore del calcolo dell&#39;incremento. Inoltre, influisce sul modo in cui i dati vengono aggregati prima dell&#39;applicazione del calcolo del valore di confidenza.

* I ***visitatori univoci*** incrementano una volta quando un utente si qualifica per la prima volta per un&#39;attività.
* Le ***visite*** incrementano per ogni sessione una volta che un utente (Visitatore unico) entra in un&#39;attività, anche se l&#39;attività non viene visualizzata nelle visite successive.
* Le ***impressioni dell’attività*** aumentano ogni volta che il contenuto dell&#39;attività viene servito. (misurato da [!DNL Target]).

Quando un visitatore visualizza una pagina che contiene un&#39;attività, viene impostata una variabile per quel visitatore che contiene il nome di tale attività. Consulta gli scenari dettagliati di seguito per il confronto di ciascuna metodologia di conteggio.

Considera i seguenti aspetti:

* Tutte le metriche elencate vengono attivate quando un utente si qualifica per un&#39;attività e il contenuto viene restituito da [!DNL [!DNL Target]]. Ciò non significa necessariamente che l&#39;utente abbia visto l&#39;offerta. Se l&#39;esperienza di un’attività si trova nella parte inferiore della pagina e l&#39;utente non scorre la pagina verso il basso, allora l&#39;offerta è stata servita da [!DNL Target] ma non è stata vista dall&#39;utente.
* Le [!UICONTROL impressioni dell’attività] (misurate da [!DNL Target]) e le [!UICONTROL istanze] (misurate da [!DNL Analytics]) sono uguali, a meno che non vi siano più chiamate mbox sulla stessa pagina nella stessa attività. In tal caso si contano più [!UICONTROL impressioni dell’attività], ma solo una singola [!UICONTROL istanza].

## Perché le &quot;impression dell&#39;attività&quot; e le &quot;conversioni dell&#39;attività&quot; sono più elevate in  Analysis Workspace rispetto a Reporting e analisi? {#sametouch}

[!DNL Reports & Analytics] applica un modello di attribuzione con lo stesso tocco alle &quot;impression dell&#39;attività&quot; e alle &quot;conversioni dell&#39;attività&quot;, mentre  [!DNL Analysis Workspace] visualizza le metriche non elaborate, che possono apparire ingrandite a causa della persistenza della  [!DNL Target] dimensione.

Per valutare le metriche [!UICONTROL Impression attività] e [!UICONTROL Conversioni attività] accurate in [!DNL Analysis Workspace], assicurarsi che entrambe le metriche abbiano applicato i modelli di attribuzione [!UICONTROL Same Touch]. Per applicare i modelli, fai clic sulla colonna delle impostazioni (icona ingranaggio), abilita [!UICONTROL Modelli di attribuzione non predefiniti], quindi seleziona [!UICONTROL Stesso contatto]. Ulteriori informazioni sull&#39;attribuzione in [Panoramica sull&#39;IQ degli attributi](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/attribution.html) nella *Guida agli strumenti di Analytics*.

## Che cosa significa “conversioni di attività” se l’addetto al marketing sceglie una metrica di Analytics durante l’impostazione dell’attività? {#section_F3EBACF85AF846E9B366A549AAB64356}

&quot;Conversioni attività&quot; sarà vuota se è stata selezionata una metrica [!DNL Analytics] come metrica di conversione per l&#39;attività.

## Perché è indicato “non specificato” nei rapporti di Analytics? Che cosa significa? {#unspecified}

In altri rapporti, “non specificato” significa che i dati non soddisfano una regola di classificazione, ma in A4T non dovrebbe mai verificarsi. Se viene visualizzato “non specificato”, il servizio di classificazione non è ancora stato eseguito. In genere i dati relativi all’attività vengono visualizzati nei rapporti dopo 24-72 ore. Anche se le attività non compaiono ancora nel rapporto, tutti i dati dei visitatori legati a tali attività vengono comunque acquisiti e saranno visibili una volta completata la classificazione.

Dopo il periodo di classificazione, i dati sono visualizzati in questi rapporti circa un&#39;ora dopo essere stati raccolti dal sito. Tutte le metriche, i segmenti e i valori nei rapporti provengono dalla suite di rapporti selezionata quando si configura l’attività.

Nel caso in cui la classificazione sia stata effettuata per quell&#39;attività e nel rapporto sia ancora visibile una riga &quot;non specificata&quot;, accertati che il rapporto non utilizzi una metrica non di destinazione per visualizzare i dati.
A meno che il report non utilizzi una metrica specifica di Target, quella riga &quot;non specificata&quot; conterrà eventi per le chiamate che non sono associate a Target.
Rispettivamente, tale riga non conterrà informazioni associate a Target (ad esempio, nessun visitatore/visita/impression).

## Perché le metriche di Target vengono inviate ad Analytics anche dopo la disattivazione dell’attività? {#section_38AA8380A4D54A18972F1EF3E73E22EF}

La variabile di [!DNL Target] inviata ad [!DNL Analytics] ha un periodo di scadenza predefinito di 90 giorni. Se necessario, l&#39;Assistenza clienti può modificare il periodo di scadenza. Tuttavia, questa impostazione è globale per tutte le attività, quindi non deve essere regolata per un solo caso.

È possibile visualizzare le variabili [!DNL Target] inviate a [!DNL Analytics] dopo il periodo di scadenza perché la scadenza è di 90 giorni, ma solo se l&#39;utente non visualizza mai un&#39;altra attività [!DNL Target] abilitata per A4T. Se un utente torna al sito dopo 45 giorni e visualizza un’altra attività, l’intero valore eVar di A4T viene ripristinato e i 90 giorni ripartono da tale momento. In questo caso, la prima campagna dal giorno 1 potrebbe quindi durare fino a 45 + 90 = 135 giorni. Se l&#39;utente continua a tornare indietro, potresti arrivare al punto in cui le metriche inviate a [!DNL Analytics] nel reporting da attività molto più vecchie. Man mano che gli utenti eliminano i cookie e non tornano sul sito, i numeri per quell’attività diminuiranno, ma sarà comunque possibile visualizzarli ancora.

Ciò significa che le attività continuano a ricevere visualizzazioni di pagina, visite e così via fino a 90 giorni dopo il termine dell’attività, per i visitatori che vi hanno partecipato mentre l’attività era attiva. Tuttavia, se osservi la metrica di [!UICONTROL Impression attività], non dovresti più vedere impression dopo la fine dell’attività.

Questo è un comportamento normale e atteso. La variabile A4T funziona come qualsiasi altro eVar: il valore è associato all’utente finché non raggiunge il periodo di scadenza (90 giorni). Di conseguenza, se un’attività è attiva solo per due settimane, il valore sarà comunque associato all’utente per almeno i prossimi 90 giorni.

Si consiglia di visualizzare i rapporti per tale attività solo per il periodo di tempo in cui era in corso. Le date devono essere impostate correttamente per impostazione predefinita quando visualizzate l&#39;attività in [!DNL Analytics], pertanto, a meno che non abbiate esteso manualmente la data, non dovrebbe trattarsi di un problema dal punto di vista del reporting.

Ad esempio, supponiamo che la variabile A4T scada dopo 90 giorni e che il nostro test sia attivo dal 1° gennaio al 15 gennaio.

Il 1° gennaio, l’utente entra nel sito, vede l’attività XYZ una volta e visualizza cinque pagine. Nelle due settimane successive, l’utente non ritorna più sul sito. Per questo utente i dati saranno di questo tipo:

| Nome attività | Istanze (impression) | Visualizzazioni pagina | Visite | Visitatori univoci |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 5 | 3 | 3 |

L’utente torna il 1° febbraio, visualizza altre cinque pagine, non incontra altre attività di Target e l’attività originale non è più attiva. Anche se l’attività non è più attiva, continua a seguire l’utente tramite la persistenza eVar. I dati ora si presentano così:

| Nome attività | Istanze (impression) | Visualizzazioni pagina | Visite | Visitatori univoci |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 10 | 2 | 1 |

L’utente torna il 1° marzo e vede una nuova attività: ABC. Anche questa volta l’utente visualizza cinque pagine. Poiché l’attività XYZ continua a seguire l’utente tramite la persistenza e per l’utente è stato quindi impostato ABC, vedremo due voci nel rapporto:

| Nome attività | Istanze (impression) | Visualizzazioni pagina | Visite | Visitatori univoci |
|--- |--- |--- |--- |--- |
| XYZ | 3 | 15 | 3 | 3 |
| ABC | 3 | 5 | 3 | 3 |

L’utente poi torna il 1° aprile, visualizza altre cinque pagine ed effettua un acquisto. La scadenza di 90 giorni di quel primo valore eVar viene reimpostata a partire dal 1° aprile, quindi sarà riportato nel rapporto. Tutte le attività di Target che l’utente ha visto ricevono credito per la conversione, ma il numero totale di conversioni viene deduplicato:

| Nome attività | Istanze (impression) | Visualizzazioni pagina | Visite | Visitatori univoci | Ordini |
|--- |--- |--- |--- |--- |--- |
| XYZ | 3 | 20 | 4 | 3 | 3 |
| ABC | 3 | 10 | 2 | 1 | 3 |
| Totale | 2 | 20 | 1 | 3 | 3 |

Poiché entrambe le esperienze sono state viste prima della conversione, entrambe ottengono &quot;credito&quot; per l’ordine. Tuttavia, nel sistema è stato effettuato un solo ordine e il totale riflette questa situazione. Per i report [!DNL Target], poiché non state inserendo un&#39;attività [!DNL Target] rispetto a un&#39;altra attività per vedere quale ha più successo, non importa che tutte le attività visualizzate dall&#39;utente abbiano ottenuto credito. Si confrontano i risultati di due elementi all’interno della singola attività e non è possibile per un utente vedere diverse esperienze nella stessa attività, quindi non vi è alcun rischio di contaminazione incrociata del credito attribuito per l’ordine.

Per ulteriori informazioni, vedere [Variabili di conversione ( eVar](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html)) nella *Guida per l&#39;amministratore di Analytics*.

## Perché Analytics e Analytics for Target (A4T) calcolano i numeri per la metrica Visitatori univoci in modo diverso? {#section_0C3B648AB54041F9A2AA839D51791883}

Quando si esegue un test A/B, che utilizza il test t di Student (la metrica di affidabilità) per scegliere un vincitore di un test, uno dei presupposti è che ci sia un orizzonte temporale fisso. Il test non è statisticamente valido a meno che tu non stia esaminando la dimensione del campione fisso.

La metrica [!UICONTROL Visitatori univoci] è diversa in [!DNL Analytics] e [!DNL Target] solo quando si sta osservando un periodo di tempo inferiore al test effettivo. Se non hai raggiunto la dimensione del campione, il test non è affidabile. Per ulteriori informazioni, consulta [How Not to Run an A/B Test](https://www.evanmiller.org/how-not-to-run-an-ab-test.html) (Come non eseguire un test A/B) sul [sito web di Evan Miller](https://www.evanmiller.org/index.html).

La metrica [!UICONTROL Visitatori unici] mostra il numero di persone che sono state esposte al test che hanno visitato il sito durante il periodo di tempo specificato. Queste persone sono ancora parte del test e dovrebbero essere conteggiate. Se si desidera visualizzare solo il numero di persone esposte durante una sola settimana, è possibile creare un segmento di visitatori per i quali è stata registrata un’impression di attività e applicare tale segmento al rapporto.

È possibile ridurre il tempo di permanenza della variabile [!DNL Target] in una sessione; tuttavia, ciò è in genere problematico per i test in cui l’evento di conversione non si verifica con la stessa probabilità all’interno della stessa sessione.

## Perché lo stesso visitatore a volte viene conteggiato in più esperienze in Analytics?  {#section_1397E972D31C4207A142E4D2D6D794A2}

Di seguito sono elencati i motivi per cui lo stesso visitatore potrebbe essere conteggiato in più esperienze in [!DNL Analytics]:

* Il profilo [!DNL Target] è scaduto ma il cookie [!DNL Analytics] è ancora presente. In questa situazione, [!DNL Target] rivaluta l&#39;utente ma [!DNL Analytics] considera il visitatore la stessa persona.
* Se il visitatore utilizza l’ID `mbox3rdPartyId`, quando il visitatore anonimo viene unito al suo profilo ID di terze parti,  potrebbe porre il visitatore in un’esperienza diversa per farlo corrispondere all’ID di terze parti. [!DNL Target] Per ulteriori informazioni, consulta [Sincronizzazione dei profili in tempo reale per mbox3rdPartyID](/help/c-target/c-visitor-profile/3rd-party-id.md#concept_BF4113593F614987B1D3E359AE1C5732).
* [!DNL Analytics] potrebbe tenere traccia di diversi dispositivi come lo stesso visitatore in un modo diverso rispetto a quelli  [!DNL Target] tracciati: l’impostazione ID di terze parti in  [!DNL Target] è diversa da quella di Analytics.

## A4T supporta le suite di rapporti virtuali?

Le suite di rapporti virtuali *non* sono incluse nell’elenco Suite di rapporti e i tipi di pubblico di suite di rapporti virtuali non sono supportati nelle funzioni di reporting di A4T.

## Posso cambiare la percentuale di allocazione del traffico in un’attività che utilizza A4T dopo che l’attività è stata attivata?

La modifica della percentuale di allocazione del traffico in un&#39;attività dopo l&#39;attivazione può causare reportistica incoerente in [!DNL Analytics] perché la modifica interessa solo i nuovi visitatori. I visitatori di ritorno non sono interessati da tale modifica.

Come procedura ottimale, devi arrestare l’attività esistente, quindi creare una nuova attività invece di modificare la percentuale dopo l’attivazione. La creazione di rapporti per la nuova attività inizia con nuovi visitatori e i dati da visitatori di ritorno non causeranno un reporting incoerente.

## In che modo vengono conteggiate le visite in Analytics e il credito di conversione allocati in un&#39;attività di Auto-Target che utilizza A4T?

Quando un visitatore si qualifica, visualizza il contenuto o effettua la conversione in un&#39;attività A4T, [!DNL Target] invia i dati dell&#39;evento a [!DNL Analytics], il che consente a [!DNL Analytics] di attribuire eventi di conversione e altri eventi clickstream che si verificano sulla pagina alle attività ed esperienze [!DNL Target] pertinenti.

Di seguito sono riportati alcuni punti da tenere a mente durante la visualizzazione dei report [!DNL Analytics]:

* In generale, come procedura ottimale, la finestra di reporting deve iniziare dalla data di inizio dell&#39;attività.
* Se una conversione avviene al di fuori della finestra del rapporto, la conversione non sarà visibile in [!DNL Analytics].
* Quando nella parte &quot;targeting&quot; del traffico per le attività [!UICONTROL Auto-Target], i visitatori potrebbero visualizzare esperienze diverse da una sessione all&#39;altra. Ad esempio, se il profilo o il contesto sono cambiati e gli algoritmi di machine-learning di [!DNL Target] stabiliscono che è più probabile che vengano convertiti in base a una nuova esperienza. Quando i visitatori passano dall&#39;esperienza all&#39;esperienza, il conteggio delle visite aumenta per ogni esperienza visualizzata. Ciò è diverso dalle normali attività di test A/B in cui le esperienze sono appiccicose per un visitatore durante le visite.
* Se un visitatore visualizza più esperienze tra una visita e l&#39;altra, qualsiasi conversione viene sempre attribuita all&#39;ultima esperienza visualizzata dal visitatore. Come già detto, il conteggio delle visite incrementa ogni esperienza visualizzata dal visitatore. Questo può eliminare artificialmente i tassi di conversione per esperienza quando si visualizzano esperienze sotto la dimensione &quot;[!UICONTROL Targeting]&quot; nei report [!DNL Adobe Analytics].
