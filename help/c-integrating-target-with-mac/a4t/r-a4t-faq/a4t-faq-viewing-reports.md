---
keywords: faq;frequently asked questions;analytics for target;a4T;report;reports;view reports;reporting;counting methodology;impressions;visitors;visits;default metric;activity conversions;unspecified
description: Questo argomento contiene le risposte alle domande che vengono spesso poste in merito alla visualizzazione dei rapporti durante l’utilizzo di Analytics come origine per la creazione di rapporti per Target (A4T).
title: Visualizzare i rapporti - Domande frequenti su A4T
feature: a4t troubleshooting
translation-type: tm+mt
source-git-commit: 7ad57c6f3814140df0826f57d8052f6db3fda301
workflow-type: tm+mt
source-wordcount: '2196'
ht-degree: 57%

---


# Visualizzare i rapporti - Domande frequenti su A4T

This topic contains answers to questions that are frequently asked about viewing reports when using [!DNL Analytics] as the reporting source for [!DNL Target] (A4T).

## Posso visualizzare i dati di attività Target in Analysis Workspace? {#workspace}

Potete utilizzare [!DNL Analysis Workspace] per analizzare le [!DNL Target] attività e le esperienze. Il pannello [](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html) Analisi per Target consente di visualizzare tre metriche di successo con un livello di affidabilità e di incremento. Puoi anche approfondire la ricerca utilizzando tabelle e visualizzazioni.

For detailed information and examples, open the [Analytics &amp; Target: Best Practices for Analysis tutorial](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), provided by Adobe Experience League.

## Dove si possono applicare i segmenti in  Analysis Workspace? {#segmentation}

I segmenti vengono applicati più comunemente nella parte superiore di un pannello nella zona di rilascio del segmento. Il segmento viene applicato a tutte le tabelle e le visualizzazioni nel pannello. Questa tecnica è particolarmente utile per vedere in che modo il test interessa un sottoinsieme di persone (ad esempio, come è stato eseguito questo test per le persone nel Regno Unito)?

## Quando applico un segmento di hit per una specifica attività Target, perché viene restituita un&#39;esperienza non correlata? {#activity-segmentation}

La variabile di [!DNL Target] inviata ad [!DNL Analytics] ha un periodo di scadenza predefinito di 90 giorni. (Nota: se necessario, tale periodo di scadenza può essere regolato dall&#39;Assistenza clienti). Quando i visitatori navigano nel sito attraverso questa finestra di scadenza, fanno parte di molte [!DNL Target] attività, tutte raccolte nella dimensione.

Di conseguenza, quando segmentate la presenza di un&#39;attività in un hit, otterrete tutte le esperienze che fanno parte di tale attività *più* qualsiasi altra esperienza persistente su tale hit.

## È necessario utilizzare i visitatori, le visite o le impression dell&#39;attività come metrica di normalizzazione (ad es. metodologia di conteggio)? {#metrics}

Esistono diverse opzioni per normalizzare le metriche nel reporting A4T. Questa metrica, detta anche metodologia di conteggio, diventa il denominatore del calcolo dell&#39;incremento. Inoltre, influisce sul modo in cui i dati vengono aggregati prima dell&#39;applicazione del calcolo del valore di confidenza.

* I ***visitatori univoci*** incrementano una volta quando un utente si qualifica per la prima volta per un&#39;attività.
* Le ***visite*** incrementano per ogni sessione una volta che un utente (Visitatore unico) entra in un&#39;attività, anche se l&#39;attività non viene visualizzata nelle visite successive.
* Le ***impressioni dell’attività*** aumentano ogni volta che il contenuto dell&#39;attività viene servito. (Measured by [!DNL Target]).

Quando un visitatore visualizza una pagina che contiene un&#39;attività, viene impostata una variabile per quel visitatore che contiene il nome di tale attività. Consulta gli scenari dettagliati di seguito per il confronto di ciascuna metodologia di conteggio.

Considera i seguenti aspetti:

* All of the above metrics trigger when a user qualifies for an activity and content is returned from [!DNL [!DNL Target]]. Ciò non significa necessariamente che l&#39;utente abbia visto l&#39;offerta. Se l&#39;esperienza di un’attività si trova nella parte inferiore della pagina e l&#39;utente non scorre la pagina verso il basso, allora l&#39;offerta è stata servita da [!DNL Target] ma non è stata vista dall&#39;utente.
* Le [!UICONTROL impressioni dell’attività] (misurate da [!DNL Target]) e le [!UICONTROL istanze] (misurate da [!DNL Analytics]) sono uguali, a meno che non vi siano più chiamate mbox sulla stessa pagina nella stessa attività. In tal caso si contano più [!UICONTROL impressioni dell’attività], ma solo una singola [!UICONTROL istanza].

## Perché le &quot;impression dell&#39;attività&quot; e le &quot;conversioni dell&#39;attività&quot; sono più elevate in  Analysis Workspace rispetto a Reporting e analisi? {#sametouch}

[!DNL Reports & Analytics] applica un modello di attribuzione con lo stesso tocco alle &quot;impression dell&#39;attività&quot; e alle &quot;conversioni dell&#39;attività&quot;, mentre [!DNL Analysis Workspace] visualizza le metriche non elaborate, che possono apparire ingrandite a causa della persistenza della [!DNL Target] dimensione.

To evaluate accurate [!UICONTROL Activity Impressions] and [!UICONTROL Activity Conversions] metrics in [!DNL Analysis Workspace], ensure that both metrics have [!UICONTROL Same Touch] attribution models applied. Per applicare i modelli, fai clic sulla colonna delle impostazioni (icona ingranaggio), abilita [!UICONTROL Modelli di attribuzione non predefiniti], quindi seleziona [!UICONTROL Stesso contatto]. Ulteriori informazioni sull&#39;attribuzione in [Attributi IQ panoramica](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/attribution.html) nella Guida *agli strumenti di* Analytics.

## Che cosa significa “conversioni di attività” se l’addetto al marketing sceglie una metrica di Analytics durante l’impostazione dell’attività? {#section_F3EBACF85AF846E9B366A549AAB64356}

&quot;Activity conversions&quot; will be empty if an [!DNL Analytics] metric was selected as the conversion metric for the activity.

## Perché è indicato “non specificato” nei rapporti di Analytics? Che cosa significa? {#unspecified}

In altri rapporti, “non specificato” significa che i dati non soddisfano una regola di classificazione, ma in A4T non dovrebbe mai verificarsi. Se viene visualizzato “non specificato”, il servizio di classificazione non è ancora stato eseguito. In genere i dati relativi all’attività vengono visualizzati nei rapporti dopo 24-72 ore. Anche se le attività non compaiono ancora nel rapporto, tutti i dati dei visitatori legati a tali attività vengono comunque acquisiti e saranno visibili una volta completata la classificazione.

Dopo il periodo di classificazione, i dati sono visualizzati in questi rapporti circa un&#39;ora dopo essere stati raccolti dal sito. Tutte le metriche, i segmenti e i valori nei rapporti provengono dalla suite di rapporti selezionata quando si configura l’attività.

## Perché le metriche di Target vengono inviate ad Analytics anche dopo la disattivazione dell’attività? {#section_38AA8380A4D54A18972F1EF3E73E22EF}

La variabile di [!DNL Target] inviata ad [!DNL Analytics] ha un periodo di scadenza predefinito di 90 giorni. Se necessario, l&#39;Assistenza clienti può modificare il periodo di scadenza. Tuttavia, questa impostazione è globale per tutte le attività, quindi non deve essere regolata per un solo caso.

You might see [!DNL Target] variables sent to [!DNL Analytics] after the expiration period because the expiration is 90 days, but only if that user never sees another A4T-enabled [!DNL Target] activity. Se un utente torna al sito dopo 45 giorni e visualizza un’altra attività, l’intero valore eVar di A4T viene ripristinato e i 90 giorni ripartono da tale momento. In questo caso, la prima campagna dal giorno 1 potrebbe quindi durare fino a 45 + 90 = 135 giorni. If the user keeps coming back, you might get to the point where you see metrics sent to [!DNL Analytics] in your reporting from much older activities. Man mano che gli utenti eliminano i cookie e non tornano sul sito, i numeri per quell’attività diminuiranno, ma sarà comunque possibile visualizzarli ancora.

Ciò significa che le attività continuano a ricevere visualizzazioni di pagina, visite e così via fino a 90 giorni dopo il termine dell’attività, per i visitatori che vi hanno partecipato mentre l’attività era attiva. Tuttavia, se osservi la metrica di [!UICONTROL Impression attività], non dovresti più vedere impression dopo la fine dell’attività.

Questo è un comportamento normale e atteso. La variabile A4T funziona come qualsiasi altro eVar: il valore è associato all’utente finché non raggiunge il periodo di scadenza (90 giorni). Di conseguenza, se un’attività è attiva solo per due settimane, il valore sarà comunque associato all’utente per almeno i prossimi 90 giorni.

Si consiglia di visualizzare i rapporti per tale attività solo per il periodo di tempo in cui era in corso. The dates should be set correctly by default when you view the activity in [!DNL Analytics], so unless you have manually extended the date this shouldn’t be an issue from a reporting standpoint.

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

Poiché entrambe le esperienze sono state viste prima della conversione, entrambe ottengono &quot;credito&quot; per l’ordine. Tuttavia, nel sistema è stato effettuato un solo ordine e il totale riflette questa situazione. For [!DNL Target] reporting, because you aren’t putting a [!DNL Target] activity against another activity to see which is more successful, it doesn’t matter that all activities the user saw got credit. Si confrontano i risultati di due elementi all’interno della singola attività e non è possibile per un utente vedere diverse esperienze nella stessa attività, quindi non vi è alcun rischio di contaminazione incrociata del credito attribuito per l’ordine.

For more information, see [Conversion Variables (eVar](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html)) in the *Analytics Admin Guide*.

## Perché Analytics e Analytics for Target (A4T) calcolano i numeri per la metrica Visitatori univoci in modo diverso? {#section_0C3B648AB54041F9A2AA839D51791883}

Quando si esegue un test A/B, che utilizza il test t di Student (la metrica di affidabilità) per scegliere un vincitore di un test, uno dei presupposti è che ci sia un orizzonte temporale fisso. Il test non è statisticamente valido a meno che tu non stia esaminando la dimensione del campione fisso.

The [!UICONTROL Unique Visitors] metric is different in [!DNL Analytics] and [!DNL Target] only when you are looking at a period of time that is shorter than the actual test. Se non hai raggiunto la dimensione del campione, il test non è affidabile. Per ulteriori informazioni, consulta [How Not to Run an A/B Test](https://www.evanmiller.org/how-not-to-run-an-ab-test.html) (Come non eseguire un test A/B) sul [sito web di Evan Miller](https://www.evanmiller.org/index.html).

The [!UICONTROL Unique Visitors] metric displays the number of people who have been exposed to the test who have visited the site during the specified time period. Queste persone sono ancora parte del test e dovrebbero essere conteggiate. Se si desidera visualizzare solo il numero di persone esposte durante una sola settimana, è possibile creare un segmento di visitatori per i quali è stata registrata un’impression di attività e applicare tale segmento al rapporto.

You can shorten the amount of time the [!DNL Target] variable persists down to a session; however, that is usually problematic for tests where the conversion event isn’t as likely to happen within the same session.

## Perché lo stesso visitatore a volte viene conteggiato in più esperienze in Analytics? {#section_1397E972D31C4207A142E4D2D6D794A2}

Di seguito sono elencati i motivi per cui lo stesso visitatore potrebbe essere conteggiato in più esperienze in [!DNL Analytics]:

* The [!DNL Target] profile expired but the [!DNL Analytics] cookie is still there. In this situation, [!DNL Target] re-evaluates the user but [!DNL Analytics] considers the visitor to be the same person.
* Se il visitatore utilizza l’ID `mbox3rdPartyId`, quando il visitatore anonimo viene unito al suo profilo ID di terze parti,  potrebbe porre il visitatore in un’esperienza diversa per farlo corrispondere all’ID di terze parti. [!DNL Target] Per ulteriori informazioni, consulta [Sincronizzazione dei profili in tempo reale per mbox3rdPartyID](/help/c-target/c-visitor-profile/3rd-party-id.md#concept_BF4113593F614987B1D3E359AE1C5732).
* [!DNL Analytics] potrebbe tenere traccia di diversi dispositivi come lo stesso visitatore in un modo diverso rispetto a [!DNL Target] questi dispositivi: l’impostazione ID di terze parti in [!DNL Target] è diversa da quella di Analytics.

## A4T supporta le suite di rapporti virtuali?

Le suite di rapporti virtuali *non* sono incluse nell’elenco Suite di rapporti e i tipi di pubblico di suite di rapporti virtuali non sono supportati nelle funzioni di reporting di A4T.

## Posso cambiare la percentuale di allocazione del traffico in un’attività che utilizza A4T dopo che l’attività è stata attivata?

Changing the traffic allocation percentage in an activity after activation can cause inconsistent reporting in [!DNL Analytics] because the change impacts only new visitors. I visitatori di ritorno non sono interessati da tale modifica.

Come procedura ottimale, devi arrestare l’attività esistente, quindi creare una nuova attività invece di modificare la percentuale dopo l’attivazione. La creazione di rapporti per la nuova attività inizia con nuovi visitatori e i dati da visitatori di ritorno non causeranno un reporting incoerente.

## In che modo vengono conteggiate le visite in Analytics e il credito di conversione allocati in un&#39;attività di Auto-Target che utilizza A4T?

Quando un visitatore soddisfa i requisiti, visualizza il contenuto o converte in un&#39;attività A4T, [!DNL Target] invia i dati dell&#39;evento a [!DNL Analytics], che consente [!DNL Analytics] di attribuire eventi di conversione e altri eventi clickstream che si verificano sulla pagina alle attività e alle esperienze pertinenti [!DNL Target] .

Di seguito sono riportati alcuni punti da tenere a mente quando si visualizzano [!DNL Analytics] i rapporti:

* In generale, la finestra di reporting deve sempre iniziare dalla data di inizio dell&#39;attività.
* Se una conversione avviene al di fuori della finestra del rapporto, la conversione non sarà visibile in [!DNL Analytics].
* Quando nella parte &quot;mirata&quot; del traffico per le attività [!UICONTROL Auto-Target] , i visitatori potrebbero visualizzare esperienze diverse da una sessione all&#39;altra. Ad esempio, il loro profilo o contesto è cambiato e gli algoritmi di machine-learning [!DNL Target]di cui dispongono decideranno che è più probabile che vengano convertiti in base a una nuova esperienza. Ciò è diverso dalle normali attività di test A/B, in cui le esperienze sono appiccicose per un visitatore durante le visite.
* Se un visitatore visualizza più esperienze tra una visita e l&#39;altra, qualsiasi conversione viene sempre attribuita all&#39;ultima esperienza visualizzata dal visitatore; tuttavia, il conteggio delle visite verrà incrementato per ogni esperienza visualizzata dal visitatore. Questo può eliminare artificialmente i tassi di conversione per esperienza quando si visualizzano esperienze sotto la dimensione &quot;[!UICONTROL Target]&quot; nei [!DNL Adobe Analytics] report.
