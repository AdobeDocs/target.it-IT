---
keywords: FAQ;domande frequenti;analytics for target;a4t;rapporto;report;visualizzare rapporti;reporting;metodologia di conteggio;impression;visitatori;visite;metriche predefinite;conversioni di attività;non specificato
description: Trova le risposte alle domande più frequenti sulla visualizzazione dei rapporti durante l’utilizzo di Analytics for Target (A4T). A4T consente di utilizzare i rapporti di Analytics per le attività di Target.
title: Trova risposte alle domande sulla visualizzazione di rapporti con A4T?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: e45f0d2d2370f9c7aba2c2bd26afdd4c0e401db8
workflow-type: tm+mt
source-wordcount: '2405'
ht-degree: 40%

---


# Visualizzare i rapporti - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande più frequenti sulla visualizzazione dei rapporti quando si utilizza [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Adobe Target] (A4T).

## Posso visualizzare i dati di attività Target in Analysis Workspace? {#workspace}

Puoi utilizzare [!DNL Analysis Workspace] per analizzare le attività e le esperienze [!DNL Target]. Il pannello [Analytics for Target](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html) ti consente di visualizzare l’incremento e l’affidabilità per fino a tre metriche di successo. Puoi anche approfondire l’uso di tabelle e visualizzazioni.

Per informazioni ed esempi dettagliati, apri [Analytics &amp; Target: Esercitazione sulle best practice per l&#39;analisi](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), fornita da Adobe Experience League.

## Dove si possono applicare i segmenti in Analysis Workspace? {#segmentation}

I segmenti vengono più comunemente utilizzati nella parte superiore di un pannello nella zona di rilascio dei segmenti. Il segmento viene applicato a tutte le tabelle e visualizzazioni nel pannello . Questa tecnica è particolarmente utile per vedere in che modo il test interessa un sottoinsieme di persone (ad esempio, come si è verificato questo test per le persone nel Regno Unito)?

Un segmento può anche essere disposto su più livelli direttamente all’interno della tabella a forma libera, ma è necessario sovrapporlo all’interno dell’intera tabella per mantenere i calcoli di incremento e affidabilità all’interno del pannello A4T. I segmenti a livello di colonna non sono attualmente supportati nel pannello .

## Quando applico un segmento di hit per una specifica attività di Target, perché vengono restituite esperienze non collegate? {#activity-segmentation}

La variabile di [!DNL Target] inviata ad [!DNL Analytics] ha un periodo di scadenza predefinito di 90 giorni. (Nota: se necessario, questo periodo di scadenza può essere regolato dall’Assistenza clienti). Quando i visitatori navigano nel sito in questa finestra di scadenza, fanno parte di numerose attività [!DNL Target], tutte raccolte nella dimensione .

Quando si segmenta l&#39;attività per essere presente in un hit, si ottengono tutte le esperienze che fanno parte di tale attività *più* tutte le altre esperienze che persistono su tale hit.

## Durante la configurazione delle metriche obiettivo, perché non posso accedere alle impostazioni avanzate?

Per le attività che utilizzano [!DNL Analytics] come origine per la generazione di rapporti (A4T), la metrica obiettivo utilizza le impostazioni &quot;[!UICONTROL Incrementa il conteggio e mantieni l’utente in attività]&quot; e &quot;[!UICONTROL Su ogni impression]&quot;. Queste impostazioni sono *non* configurabili.

Per ulteriori informazioni, consulta &quot;Durante la configurazione delle metriche dell’obiettivo, perché non posso accedere alle opzioni Impostazioni avanzate?&quot; in [Definizioni delle metriche - Domande frequenti su A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

## È necessario utilizzare visitatori, visite o impression di attività come metrica di normalizzazione (ovvero metodologia di conteggio)? {#metrics}

Esistono diverse opzioni per normalizzare le metriche nel reporting di A4T. Questa metrica, detta anche metodologia di conteggio, diventa il denominatore del calcolo dell’incremento. Inoltre, influisce sul modo in cui i dati vengono aggregati prima dell’applicazione del calcolo dell’affidabilità.

* I ***visitatori univoci*** incrementano una volta quando un utente si qualifica per la prima volta per un&#39;attività.
* Le ***visite*** incrementano per ogni sessione una volta che un utente (Visitatore unico) entra in un&#39;attività, anche se l&#39;attività non viene visualizzata nelle visite successive.
* Le ***impressioni dell’attività*** aumentano ogni volta che il contenuto dell&#39;attività viene servito. (Misurato da [!DNL Target]).

Quando un visitatore visualizza una pagina che contiene un&#39;attività, viene impostata una variabile per quel visitatore che contiene il nome di tale attività. Consulta gli scenari dettagliati di seguito per il confronto di ciascuna metodologia di conteggio.

Considera i seguenti aspetti:

* Le metriche sopra indicate si attivano quando un utente si qualifica per un&#39;attività e il contenuto viene restituito da [!DNL Target]. Ciò non significa necessariamente che l&#39;utente abbia visto l&#39;offerta. Se l&#39;esperienza di un’attività si trova nella parte inferiore della pagina e l&#39;utente non scorre la pagina verso il basso, allora l&#39;offerta è stata servita da [!DNL Target] ma non è stata vista dall&#39;utente.
* Le [!UICONTROL impressioni dell’attività] (misurate da [!DNL Target]) e le [!UICONTROL istanze] (misurate da [!DNL Analytics]) sono uguali, a meno che non vi siano più chiamate mbox sulla stessa pagina nella stessa attività. In tal caso si contano più [!UICONTROL impressioni dell’attività], ma solo una singola [!UICONTROL istanza].

## Perché le &quot;impression di attività&quot; e le &quot;conversioni di attività&quot; sono più alte in Analysis Workspace rispetto a Reports &amp; Analytics? {#sametouch}

[!DNL Reports & Analytics] applica un modello di attribuzione con lo stesso contatto alle &quot;impression di attività&quot; e alle &quot;conversioni di attività&quot;, mentre  [!DNL Analysis Workspace] visualizza le metriche non elaborate, che possono apparire gonfiate a causa della persistenza della  [!DNL Target] dimensione.

Per valutare le metriche accurate [!UICONTROL Impressioni attività] e [!UICONTROL Conversioni attività] in [!DNL Analysis Workspace], assicurati che entrambe le metriche abbiano applicato i modelli di attribuzione [!UICONTROL Stesso contatto] . Per applicare i modelli, fai clic sulla colonna delle impostazioni (icona ingranaggio), abilita [!UICONTROL Modelli di attribuzione non predefiniti], quindi seleziona [!UICONTROL Stesso contatto]. Ulteriori informazioni sull&#39;attribuzione in [Panoramica di Attribution IQ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/attribution.html) nella *Guida agli strumenti di Analytics*.

## Che cosa significa “conversioni di attività” se l’addetto al marketing sceglie una metrica di Analytics durante l’impostazione dell’attività? {#section_F3EBACF85AF846E9B366A549AAB64356}

Le &quot;Conversioni attività&quot; sono vuote se è stata selezionata una metrica [!DNL Analytics] come metrica di conversione per l’attività.

## Perché è indicato “non specificato” nei rapporti di Analytics? Che cosa significa? {#unspecified}

In altri rapporti, “non specificato” significa che i dati non soddisfano una regola di classificazione, ma in A4T non dovrebbe mai verificarsi. Se viene visualizzato “non specificato”, il servizio di classificazione non è ancora stato eseguito. In genere i dati relativi all’attività vengono visualizzati nei rapporti dopo 24-72 ore. Anche se le attività non compaiono in questo rapporto fino a quel momento, tutti i dati dei visitatori associati a tali attività vengono acquisiti e vengono visualizzati al termine della classificazione.

Dopo il periodo di classificazione, i dati sono visualizzati in questi rapporti circa un&#39;ora dopo essere stati raccolti dal sito. Tutte le metriche, i segmenti e i valori nei rapporti provengono dalla suite di rapporti selezionata quando si configura l’attività.

Nel caso in cui la classificazione sia stata effettuata per quell’attività e nel rapporto sia ancora presente una riga &quot;Non specificato&quot;, accertati che il rapporto non utilizzi una metrica non[!DNL Target] per visualizzare i dati. A meno che il rapporto non utilizzi una metrica specifica [!DNL Target], la riga &quot;Non specificato&quot; contiene eventi per chiamate non associate a [!DNL Target]. Tale riga non conterrà alcuna informazione associata a [!DNL Target] (ad esempio, visitatori/visite/impression).

## Perché le metriche di Target vengono inviate ad Analytics anche dopo la disattivazione dell’attività? {#section_38AA8380A4D54A18972F1EF3E73E22EF}

La variabile di [!DNL Target] inviata ad [!DNL Analytics] ha un periodo di scadenza predefinito di 90 giorni. Se necessario, questo periodo di scadenza può essere regolato dall’Assistenza clienti. Tuttavia, questa impostazione è globale per tutte le attività, quindi non deve essere regolata per un solo caso.

È possibile che dopo il periodo di scadenza vengano visualizzate le variabili [!DNL Target] inviate a [!DNL Analytics] perché la scadenza è di 90 giorni, ma solo se l’utente non visualizza mai un’altra attività [!DNL Target] abilitata per A4T. Se un utente torna al sito dopo 45 giorni e visualizza un’altra attività, l’intero valore eVar di A4T viene ripristinato e i 90 giorni ripartono da tale momento. In questo caso, la prima campagna dal giorno 1 potrebbe quindi durare fino a 45 + 90 = 135 giorni. Se l’utente continua a tornare, potrebbe arrivare al punto in cui vengono visualizzate le metriche inviate a [!DNL Analytics] nel rapporto da attività molto più vecchie. Man mano che gli utenti eliminano i cookie e non ritornano al sito, i numeri in quell’attività diminuiscono, ma puoi comunque visualizzarli.

Questo significa che le attività continuano a ricevere visualizzazioni di pagina, visite e così via, per un massimo di 90 giorni dal termine dell’attività per i visitatori che sono diventati parte dell’attività mentre era attiva. Tuttavia, se osservi la metrica di [!UICONTROL Impression attività], non dovresti più vedere impression dopo la fine dell’attività.

Questo è un comportamento normale e atteso. La variabile A4T funziona come qualsiasi altro eVar: il valore è associato all’utente finché non raggiunge il periodo di scadenza (90 giorni). Di conseguenza, se un’attività è attiva solo per due settimane, il valore rimane associato all’utente per almeno i successivi 90 giorni.

Si consiglia di visualizzare i rapporti per tale attività solo per il periodo di tempo in cui era in corso. Le date devono essere impostate correttamente per impostazione predefinita quando visualizzi l’attività in [!DNL Analytics], pertanto, a meno che non sia stata estesa manualmente la data, non dovrebbe essere un problema dal punto di vista della generazione di rapporti.

Ad esempio, supponiamo che la variabile A4T scada dopo 90 giorni e che il test sia attivo dal 1° gennaio al 15 gennaio.

Il 1° gennaio, l’utente entra nel sito, vede l’attività XYZ una volta e visualizza cinque pagine. Nelle due settimane successive, l’utente non ritorna più sul sito. Per questo utente i dati saranno di questo tipo:

| Nome attività | Istanze (impression) | Visualizzazioni pagina | Visite | Visitatori univoci |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 5 | 1 | 1 |

L’utente torna il 1° febbraio, visualizza altre cinque pagine, non incontra altre attività di Target e l’attività originale non è più attiva. Anche se l’attività non è più attiva, continua a seguire l’utente tramite la persistenza eVar. I dati ora si presentano così:

| Nome attività | Istanze (impression) | Visualizzazioni pagina | Visite | Visitatori univoci |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 10 | 2 | 1 |

L’utente torna il 1° marzo e vede una nuova attività: ABC. Anche questa volta l’utente visualizza cinque pagine. Poiché l’attività XYZ continua a seguire l’utente attraverso la persistenza e questo utente ha quindi impostato ABC, vedrai due voci nel rapporto:

| Nome attività | Istanze (impression) | Visualizzazioni pagina | Visite | Visitatori univoci |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 15 | 3 | 1 |
| ABC | 1 | 5 | 1 | 1 |

L’utente poi torna il 1° aprile, visualizza altre cinque pagine ed effettua un acquisto. La scadenza di 90 giorni di quel primo valore eVar viene reimpostata il 1° aprile, quindi lo puoi vedere nei rapporti. Tutte le attività di Target che l’utente ha visto ricevono credito per la conversione, ma il numero totale di conversioni viene deduplicato:

| Nome attività | Istanze (impression) | Visualizzazioni pagina | Visite | Visitatori univoci | Ordini |
|--- |--- |--- |--- |--- |--- |
| XYZ | 1 | 20 | 4 | 1 | 1 |
| ABC | 1 | 10 | 2 | 1 | 1 |
| Totale | 2 | 20 | 1 | 1 | 1 |

Poiché entrambe le esperienze sono state viste prima della conversione, entrambe ottengono &quot;credito&quot; per l’ordine. Tuttavia, nel sistema è stato effettuato un solo ordine e il totale riflette questa situazione. Per il reporting [!DNL Target], poiché non stai mettendo un&#39;attività [!DNL Target] contro un&#39;altra attività per vedere quale ha più successo, non importa che tutte le attività visualizzate dall&#39;utente abbiano ricevuto credito. Stai confrontando i risultati di due elementi all’interno della singola attività. Non è possibile che un utente veda diverse esperienze nella stessa attività, in modo da non doverti preoccupare della contaminazione incrociata del credito d’ordine.

Per ulteriori informazioni, consulta [Variabili di conversione (eVar](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html)) nella *Guida per l’amministrazione di Analytics*.

## Perché Analytics e Analytics for Target (A4T) calcolano i numeri per la metrica Visitatori univoci in modo diverso? {#section_0C3B648AB54041F9A2AA839D51791883}

Quando si esegue un test A/B, che utilizza il test t di Student (la metrica di affidabilità) per scegliere un vincitore di un test, uno dei presupposti è che ci sia un orizzonte temporale fisso. Il test non è statisticamente valido a meno che tu non stia esaminando la dimensione del campione fisso.

La metrica [!UICONTROL Visitatori unici] è diversa in [!DNL Analytics] e [!DNL Target] solo quando stai guardando un periodo più breve del test effettivo. Se non hai raggiunto la dimensione del campione, il test non è affidabile. Per ulteriori informazioni, consulta [How Not to Run an A/B Test](https://www.evanmiller.org/how-not-to-run-an-ab-test.html) (Come non eseguire un test A/B) sul [sito web di Evan Miller](https://www.evanmiller.org/index.html).

La metrica [!UICONTROL Visitatori unici] mostra il numero di persone che sono state esposte al test che hanno visitato il sito durante il periodo di tempo specificato. Queste persone fanno parte del test e dovrebbero essere conteggiate. Se si desidera visualizzare solo il numero di persone esposte durante una sola settimana, è possibile creare un segmento di visitatori per i quali è stata registrata un’impression di attività e applicare tale segmento al rapporto.

È possibile ridurre il tempo in cui la variabile [!DNL Target] persiste fino a una sessione; tuttavia, ciò è problematico per i test in cui è improbabile che l’evento di conversione si verifichi entro la stessa sessione.

## Perché lo stesso visitatore a volte viene conteggiato in più esperienze in Analytics?  {#section_1397E972D31C4207A142E4D2D6D794A2}

Di seguito sono elencati i motivi per cui lo stesso visitatore potrebbe essere conteggiato in più esperienze in [!DNL Analytics]:

* Il profilo [!DNL Target] è scaduto ma il cookie [!DNL Analytics] è ancora presente. In questa situazione, [!DNL Target] rivaluta l’utente ma [!DNL Analytics] considera il visitatore come la stessa persona.
* Se il visitatore utilizza il `mbox3rdPartyId`, quando il visitatore anonimo viene unito al profilo ID di terze parti, [!DNL Target] potrebbe porre il visitatore in un’esperienza diversa per farlo corrispondere all’ID di terze parti. Per ulteriori informazioni, consulta [Sincronizzazione dei profili in tempo reale per mbox3rdPartyID](/help/c-target/c-visitor-profile/3rd-party-id.md#concept_BF4113593F614987B1D3E359AE1C5732).
* [!DNL Analytics] potrebbe tenere traccia di dispositivi diversi come lo stesso visitatore in un modo diverso rispetto a  [!DNL Target] quelli tracciati: la configurazione dell’ID di terze parti in  [!DNL Target] è diversa da in Analytics.

## A4T supporta le suite di rapporti virtuali?

Le suite di rapporti virtuali *non* sono incluse nell’elenco Suite di rapporti e i tipi di pubblico di suite di rapporti virtuali non sono supportati nelle funzioni di reporting di A4T.

## Posso cambiare la percentuale di allocazione del traffico in un’attività che utilizza A4T dopo che l’attività è stata attivata?

La modifica della percentuale di allocazione del traffico in un&#39;attività dopo l&#39;attivazione può causare rapporti incoerenti in [!DNL Analytics] perché la modifica interessa solo i nuovi visitatori. I visitatori di ritorno non sono interessati da tale modifica.

Come procedura ottimale, devi arrestare l’attività esistente, quindi creare una nuova attività invece di modificare la percentuale dopo l’attivazione. Il reporting per la nuova attività inizia con nuovi visitatori e i dati dei visitatori di ritorno non causano rapporti incoerenti.

## Come vengono conteggiate le visite in Analytics e il credito di conversione allocati in un’attività di Targeting automatico che utilizza A4T?

Quando un visitatore si qualifica, visualizza il contenuto o effettua la conversione in un’attività A4T, [!DNL Target] invia i dati dell’evento a [!DNL Analytics]. Questi dati evento consentono a [!DNL Analytics] di attribuire eventi di conversione e altri eventi clickstream che si verificano sulla pagina alle attività e alle esperienze pertinenti [!DNL Target].

Di seguito sono riportati alcuni punti da tenere a mente durante la visualizzazione dei rapporti [!DNL Analytics] :

* In generale, come best practice, l’intervallo di reporting deve iniziare dalla data di inizio dell’attività.
* Se una conversione si verifica all’esterno della finestra del rapporto, la conversione non è visibile in [!DNL Analytics].
* Quando nella parte &quot;mirata&quot; del traffico per le attività [!UICONTROL Targeting automatico], i visitatori potrebbero vedere esperienze diverse da una sessione all&#39;altra. Ad esempio, se il profilo o il contesto sono cambiati e gli algoritmi di machine-learning di [!DNL Target] decidono che è più probabile la conversione in base a una nuova esperienza. Man mano che i visitatori passano dall’esperienza all’esperienza, il conteggio delle visite incrementa per ogni esperienza visualizzata. Ciò è diverso dalle normali attività di test A/B in cui le esperienze sono appiccicose a un visitatore durante le visite.
* Se un visitatore visualizza più esperienze in più visite, qualsiasi conversione è sempre attribuita all’ultima esperienza che il visitatore ha visto. Come indicato, il conteggio delle visite incrementa ogni esperienza visualizzata dal visitatore. Questo può eliminare artificialmente i tassi di conversione per esperienza quando si visualizzano le esperienze sotto la dimensione &quot;[!UICONTROL Target]&quot; nei rapporti [!DNL Adobe Analytics].
