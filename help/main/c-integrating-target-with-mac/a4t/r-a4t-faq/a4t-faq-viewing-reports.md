---
keywords: FAQ;domande frequenti;analytics for target;a4t;rapporto;report;visualizzare rapporti;reporting;metodologia di conteggio;impression;visitatori;visite;metriche predefinite;conversioni di attività;non specificato
description: Trova le risposte alle domande che vengono spesso poste in merito alla visualizzazione dei rapporti durante l'utilizzo di Analytics for [!DNL Target] (A4T). A4T consente di utilizzare la funzione di reporting di Analytics per  [!DNL Target]  attività.
title: Risposte alle domande sulla visualizzazione di rapporti con A4T?
feature: Analytics for Target (A4T)
exl-id: a02eeb34-3975-424b-a046-e51f10ae1823
source-git-commit: c747a8a0ed480130f254818e21b98addca16ca41
workflow-type: tm+mt
source-wordcount: '2539'
ht-degree: 23%

---

# Visualizzare i rapporti - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande più frequenti sulla visualizzazione dei report quando si utilizza [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Adobe Target] (A4T).

## Posso visualizzare i dati di attività [!DNL Target] in [!DNL Analysis Workspace]? {#workspace}

+++Risposta
Puoi utilizzare [!DNL Analysis Workspace] per analizzare le tue attività ed esperienze [!DNL Target]. Il pannello [Analytics for Target](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=it) consente di visualizzare incremento e affidabilità per un massimo di tre metriche di successo. Puoi anche approfondire la ricerca utilizzando tabelle e visualizzazioni.

Per informazioni ed esempi dettagliati, apri l&#39;esercitazione [Analytics &amp; Target: Best Practices for Analysis](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), fornita da [!UICONTROL Adobe Experience League].

+++

## Dove applicare i segmenti in [!DNL Analysis Workspace]? {#segmentation}

+++Risposta
I segmenti vengono comunemente utilizzati nella parte superiore di un pannello nella zona di rilascio dei segmenti. Il segmento viene applicato a tutte le tabelle e visualizzazioni nel pannello. Questa tecnica è più utile per vedere in che modo il test influisce su un sottoinsieme di persone (ad esempio, come ha funzionato questo test per le persone nel Regno Unito)?

Un segmento può anche essere aggiunto a livelli direttamente all’interno della tabella a forma libera, ma tieni presente che devi sovrapporlo all’intera tabella per mantenere i calcoli di incremento e affidabilità all’interno del pannello A4T. Al momento, i segmenti a livello di colonna non sono supportati nel pannello.

+++

## Quale modello di Attribution IQ viene utilizzato in [!DNL Analysis Workspace]?

+++Risposta
Quando si utilizzano le impression e le conversioni dell&#39;attività [!DNL Target] in [!DNL Analysis Workspace], il modello di Attribution IQ &quot;Same Touch&quot; (Stesso contatto) è il modello predefinito applicato alle metriche per garantire un conteggio accurato. Questo modello funziona bene nel 99% dei casi. Tuttavia, puoi ignorare questa attribuzione standard in Attribution IQ.

+++

## Quando applico un segmento di hit per una specifica attività [!DNL Target], perché vengono restituite esperienze non correlate? {#activity-segmentation}

+++Risposta
La variabile [!DNL Target] inviata a [!DNL Analytics] ha un periodo di scadenza predefinito di 90 giorni. (Nota: se necessario, questo periodo di scadenza può essere modificato dall’Assistenza clienti). I visitatori che navigano nel sito in tutta questa finestra di scadenza fanno parte di molte attività di [!DNL Target], che si raccolgono tutte nella dimensione.

Quando si segmenta un&#39;attività affinché sia presente in un hit, si ottengono tutte le esperienze che fanno parte di tale attività *più* qualsiasi altra esperienza che persiste in tale hit.

+++

## Perché non posso accedere a [!UICONTROL Advanced Settings] durante la configurazione di [!UICONTROL Goal Metrics]?

+++Risposta
Per le attività che utilizzano [!DNL Analytics] come origine per la generazione di rapporti (A4T), la metrica di obiettivo utilizza le impostazioni &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot; e &quot;[!UICONTROL On Every Impression]&quot;. Queste impostazioni sono *non* configurabili.

Per ulteriori informazioni, consulta &quot;Perché non posso accedere alle opzioni Impostazioni avanzate durante la configurazione delle metriche dell’obiettivo?&quot; in [Definizioni delle metriche - Domande frequenti su A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

+++

## Devo utilizzare visitatori, visite o impression di attività come metrica di normalizzazione (cioè come metodologia di conteggio)? {#metrics}

+++Risposta
Esistono diverse opzioni per normalizzare le metriche nel reporting di A4T. Questa metrica, detta anche metodologia di conteggio, diventa il denominatore del calcolo dell’incremento. Inoltre, influisce sul modo in cui i dati vengono aggregati prima dell’applicazione del calcolo dell’affidabilità.

* ***Visitatori univoci*** incrementano una volta quando un utente si qualifica per la prima volta per un&#39;attività.
* Incremento di ***Visite*** per ogni sessione una volta che un utente (Visitatore univoco) entra in un&#39;attività, anche se l&#39;attività non viene visualizzata nelle visite successive.
* ***Le impression dell&#39;attività*** vengono incrementate ogni volta che viene distribuito il contenuto dell&#39;attività. (Misurato da [!DNL Target]).

Quando un visitatore visualizza una pagina che contiene un&#39;attività, viene impostata una variabile per quel visitatore che contiene il nome di tale attività. Consulta gli scenari dettagliati di seguito per il confronto di ciascuna metodologia di conteggio.

Considera i seguenti aspetti:

* Le metriche precedenti si attivano quando un utente si qualifica per un&#39;attività e il contenuto viene restituito da [!DNL Target]. Ciò non significa necessariamente che l&#39;utente abbia visto l&#39;offerta. Se l&#39;esperienza di un’attività si trova nella parte inferiore della pagina e l&#39;utente non scorre la pagina verso il basso, allora l&#39;offerta è stata servita da [!DNL Target] ma non è stata vista dall&#39;utente.
* [!UICONTROL Activity Impressions] (misurato da [!DNL Target]) e [!UICONTROL Instances] (misurato da [!DNL Analytics]) sono uguali, a meno che non vi siano più chiamate mbox sulla stessa pagina nella stessa attività. Questo fa sì che vengano conteggiati più [!UICONTROL Activity Impressions], ma solo un singolo [!UICONTROL Instance].

Per ulteriori informazioni, consulta [Come impostare i rapporti A4T in Analysis Workspace per le attività di Targeting automatico](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=it) in *Tutorials di Adobe Target*.

+++

## Perché le &quot;impressioni attività&quot; e le &quot;conversioni attività&quot; sono più alte in [!DNL Analysis Workspace] rispetto a [!UICONTROL Reports & Analytics]? {#sametouch}

+++Risposta
[!DNL Reports & Analytics] applica un modello di attribuzione di stesso contatto alle &quot;impression attività&quot; e alle &quot;conversioni attività&quot;, mentre [!DNL Analysis Workspace] visualizza le metriche non elaborate, che possono apparire gonfiate a causa della persistenza della dimensione [!DNL Target].

Per valutare metriche precise di [!UICONTROL Activity Impressions] e [!UICONTROL Activity Conversions] in [!DNL Analysis Workspace], assicurati che a entrambe siano applicati modelli di attribuzione [!UICONTROL Same Touch]. Per applicare i modelli, fare clic sull&#39;ingranaggio delle impostazioni di colonna, abilitare [!UICONTROL Non-default attribution models], quindi selezionare [!UICONTROL Same Touch]. Per ulteriori informazioni sull&#39;attribuzione, consulta la [panoramica su Attributes IQ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/attribution.html) nella *Guida agli strumenti di Analytics*.

+++

## Cosa significa &quot;conversioni di attività&quot; se l&#39;addetto al marketing sceglie una metrica [!DNL Analytics] durante la configurazione dell&#39;attività? {#section_F3EBACF85AF846E9B366A549AAB64356}

+++Risposta
Le &quot;Conversioni di attività&quot; sono vuote se è stata selezionata una metrica [!DNL Analytics] come metrica di conversione per l&#39;attività.

+++

## Perché viene visualizzato &quot;non specificato&quot; nei report [!DNL Analytics]? Che cosa significa? {#unspecified}

+++Risposta
In altri rapporti, &quot;non specificato&quot; significa che i dati non soddisfano una regola di classificazione, ma in A4T questo non dovrebbe mai accadere. Se viene visualizzato “non specificato”, il servizio di classificazione non è ancora stato eseguito. In genere i dati relativi all’attività vengono visualizzati nei rapporti dopo 24-72 ore. Anche se le attività non compaiono ancora nel rapporto, tutti i dati dei visitatori associati a tali attività vengono comunque acquisiti e visualizzati al termine della classificazione.

Dopo il periodo di classificazione, i dati sono visualizzati in questi rapporti circa un&#39;ora dopo essere stati raccolti dal sito. Tutte le metriche, i segmenti e i valori nei rapporti provengono dalla suite di rapporti selezionata quando si configura l’attività.

Nel caso in cui la classificazione sia stata eseguita per l&#39;attività e nel report venga ancora visualizzata una riga con dicitura &quot;Non specificata&quot;, verificare che il report non utilizzi una metrica non [!DNL Target] per visualizzare i dati. A meno che il report non utilizzi una metrica specifica di [!DNL Target], la riga &quot;Non specificato&quot; contiene eventi per chiamate non associate a [!DNL Target]. La riga non conterrà alcuna informazione associata a [!DNL Target] (ad esempio, visitatori/visite/impression).

+++

## Perché [!DNL Target] metriche vengono inviate a [!DNL Analytics] anche dopo la disattivazione dell&#39;attività? {#section_38AA8380A4D54A18972F1EF3E73E22EF}

+++Risposta
La variabile [!DNL Target] inviata a [!DNL Analytics] ha un periodo di scadenza predefinito di 90 giorni. Se necessario, questo periodo di scadenza può essere modificato dall’Assistenza clienti. Questa impostazione è globale per tutte le attività; tuttavia, non deve essere corretta per un caso.

Potresti visualizzare [!DNL Target] variabili inviate a [!DNL Analytics] dopo il periodo di scadenza perché la scadenza è di 90 giorni, ma solo se l&#39;utente non vede mai un&#39;altra attività [!DNL Target] abilitata per A4T. Se un utente torna al sito dopo 45 giorni e visualizza un’altra attività, l’intero valore eVar di A4T viene ripristinato e i 90 giorni ripartono da tale momento. In questo caso, la prima campagna dal giorno 1 potrebbe quindi durare fino a 45 + 90 = 135 giorni. Se l&#39;utente continua a tornare, è possibile che si arrivi al punto in cui si vedono le metriche inviate a [!DNL Analytics] nei rapporti da attività molto più vecchie. Poiché gli utenti eliminano i cookie e non tornano sul sito, i numeri in tale attività diminuiscono, ma puoi ancora visualizzarli.

Ciò significa che le attività continuano a ricevere visualizzazioni di pagina, visite e così via, fino a 90 giorni dopo il termine dell’attività per i visitatori che sono diventati parte dell’attività mentre era attiva. Tuttavia, se esamini la metrica [!UICONTROL Activity Impressions], non dovresti vedere alcuna impression al termine dell&#39;attività.

Questo è un comportamento normale e atteso. La variabile A4T funziona come qualsiasi altro eVar: il valore è associato all’utente finché non raggiunge il periodo di scadenza (90 giorni). Di conseguenza, se un’attività è attiva solo per due settimane, il valore rimane associato all’utente per almeno i successivi 90 giorni.

Si consiglia di visualizzare i rapporti per tale attività solo per il periodo di tempo in cui era in corso. Le date devono essere impostate correttamente per impostazione predefinita quando si visualizza l&#39;attività in [!DNL Analytics], quindi, a meno che non si sia estesa manualmente la data, questo non dovrebbe essere un problema dal punto di vista della generazione rapporti.

Ad esempio, supponiamo che la variabile A4T scada dopo 90 giorni e che il test sia attivo dal 1° gennaio al 15 gennaio.

Il 1° gennaio, l’utente entra nel sito, vede l’attività XYZ una volta e visualizza cinque pagine. Nelle due settimane successive, l’utente non ritorna più sul sito. Per questo utente i dati saranno di questo tipo:

| Nome attività | Istanze (impression) | Visualizzazioni pagina | Visite | Visitatori univoci |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 5 | 1 | 1 |

L’utente ritorna il 1° febbraio, visualizza altre cinque pagine e non incontra più attività di Target e l’attività originale non è più attiva. Anche se l’attività non è più attiva, continua a seguire l’utente tramite la persistenza eVar. I dati ora si presentano così:

| Nome attività | Istanze (impression) | Visualizzazioni pagina | Visite | Visitatori univoci |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 10 | 2 | 1 |

L’utente torna il 1° marzo e vede una nuova attività: ABC. Anche questa volta l’utente visualizza cinque pagine. Poiché l’attività XYZ segue ancora l’utente attraverso la persistenza e questo utente dispone quindi di un set ABC, nel reporting verranno visualizzate due righe:

| Nome attività | Istanze (impression) | Visualizzazioni pagina | Visite | Visitatori univoci |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 15 | 3 | 1 |
| ABC | 1 | 5 | 1 | 1 |

L’utente poi torna il 1° aprile, visualizza altre cinque pagine ed effettua un acquisto. La scadenza di 90 giorni del primo valore eVar viene reimpostata il 1 aprile, e ciò viene visualizzato nel reporting. Tutte le attività di Target che l’utente ha visto ricevono credito per la conversione, ma il numero totale di conversioni viene deduplicato:

| Nome attività | Istanze (impression) | Visualizzazioni pagina | Visite | Visitatori univoci | Ordini |
|--- |--- |--- |--- |--- |--- |
| XYZ | 1 | 20 | 4 | 1 | 1 |
| ABC | 1 | 10 | 2 | 1 | 1 |
| Totale | 2 | 20 | 3 | 1 | 1 |

Poiché entrambe le esperienze sono state viste prima della conversione, entrambe ricevono il &quot;merito&quot; per l’ordine. Tuttavia, nel sistema è stato effettuato un solo ordine e il totale riflette questa situazione. Per il reporting di [!DNL Target], poiché non stai confrontando un&#39;attività di [!DNL Target] con un&#39;altra attività per vedere quale ha più successo, non importa che tutte le attività che l&#39;utente ha visto abbiano ottenuto credito. Stai confrontando i risultati di due elementi all’interno della singola attività. Non è possibile per un utente vedere diverse esperienze nella stessa attività, quindi non devi preoccuparti della contaminazione incrociata del credito dell’ordine.

Per ulteriori informazioni, consulta [Variabili di conversione (eVar](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html)) nella *Guida per l&#39;amministratore di Analytics*.

+++

## Perché continuo a vedere più impression dopo la disattivazione dell’attività? {#deactivated}

+++Risposta
Una fonte di impression per il rapporto di un’attività A4T dopo la disattivazione può essere il traffico in modalità QA. Target di solito non registra gli eventi per un’attività disattivata, ma Analytics non dispone di un modo per sapere che le impression provengono dalla modalità di controllo qualità. Quando il rapporto attività di Target viene recuperato da Analytics, mostra queste impression. Questo funziona come previsto perché i clienti hanno bisogno di un modo per controllare i rapporti A4T anche se l’attività non è attiva utilizzando la modalità di controllo qualità.

+++

## Perché [!DNL Analytics] e [!UICONTROL Analytics for Adobe Target] (A4T) calcolano i numeri per la metrica [!UICONTROL Unique Visitors] in modo diverso? {#section_0C3B648AB54041F9A2AA839D51791883}

+++Risposta
Quando si esegue un test A/B, che utilizza il test t di [Welch](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank} (la metrica di affidabilità) per scegliere un vincitore di un test, uno dei presupposti è che vi sia un orizzonte temporale fisso. Il test non è statisticamente valido a meno che non si osservi la dimensione del campione fissa.

La metrica [!UICONTROL Unique Visitors] è diversa in [!DNL Analytics] e [!DNL Target] solo quando si considera un periodo più breve del test effettivo. Se non hai raggiunto la dimensione del campione, il test non è altrettanto affidabile. Per ulteriori informazioni, consulta [How Not to Run an A/B Test](https://www.evanmiller.org/how-not-to-run-an-ab-test.html) (Come non eseguire un test A/B) sul [sito web di Evan Miller](https://www.evanmiller.org/index.html).

La metrica [!UICONTROL Unique Visitors] visualizza il numero di persone che sono state esposte al test che hanno visitato il sito durante il periodo di tempo specificato. Queste persone fanno parte del test e devono essere conteggiate. Se si desidera visualizzare solo il numero di persone esposte durante una sola settimana, è possibile creare un segmento di visitatori per i quali è stata registrata un’impression di attività e applicare tale segmento al rapporto.

È possibile ridurre il tempo di persistenza della variabile [!DNL Target] in una sessione; tuttavia, ciò è problematico per i test in cui la probabilità che l&#39;evento di conversione si verifichi all&#39;interno della stessa sessione non è altrettanto elevata.

+++

## Perché lo stesso visitatore a volte viene conteggiato in più esperienze in [!DNL Analytics]? {#section_1397E972D31C4207A142E4D2D6D794A2}

+++Risposta
L&#39;elenco seguente spiega i motivi per cui lo stesso visitatore potrebbe essere conteggiato in più esperienze in [!DNL Analytics]:

* Il profilo [!DNL Target] è scaduto ma il cookie [!DNL Analytics] è ancora presente. In questa situazione, [!DNL Target] rivaluta l&#39;utente ma [!DNL Analytics] considera il visitatore come la stessa persona.
* Se il visitatore utilizza `mbox3rdPartyId`, quando il visitatore anonimo viene unito al profilo ID di terze parti, [!DNL Target] potrebbe porre il visitatore in un&#39;esperienza diversa per farlo corrispondere all&#39;ID di terze parti. Per ulteriori informazioni, consulta [Sincronizzazione dei profili in tempo reale per mbox3rdPartyID](/help/main/c-target/c-visitor-profile/3rd-party-id.md#concept_BF4113593F614987B1D3E359AE1C5732).
* [!DNL Analytics] potrebbe tracciare dispositivi diversi come lo stesso visitatore in un modo diverso da [!DNL Target] traccia tali dispositivi: la configurazione dell&#39;ID di terze parti in [!DNL Target] è diversa da quella in Analytics.

+++

## A4T supporta le suite di rapporti virtuali? {#virtual}

+++Risposta
Sebbene le suite di rapporti virtuali non siano incluse nell&#39;elenco [!UICONTROL Report Suite], qualsiasi dato A4T condiviso con una suite di rapporti collegata a una suite di rapporti virtuale in [!DNL Analytics] ha accesso a tali dati. Nessun pubblico creato da una suite di rapporti virtuale può essere condiviso di nuovo in [!DNL Target].

+++

## Posso cambiare la percentuale di allocazione del traffico in un’attività che utilizza A4T dopo che l’attività è stata attivata?

+++Risposta
La modifica della percentuale di allocazione del traffico in un&#39;attività dopo l&#39;attivazione può causare rapporti incoerenti in [!DNL Analytics] perché la modifica interessa solo i nuovi visitatori. I visitatori di ritorno non sono interessati da tale modifica.

Come procedura ottimale, devi arrestare l’attività esistente, quindi creare una nuova attività invece di modificare la percentuale dopo l’attivazione. La generazione di rapporti per la nuova attività inizia con nuovi visitatori e i dati dei visitatori di ritorno non causano rapporti incoerenti.

+++

## Come vengono conteggiate le visite in [!DNL Analytics] e il credito di conversione allocati in un&#39;attività [!UICONTROL Auto-Target] che utilizza A4T?

+++Risposta
Quando un visitatore si qualifica per, visualizza il contenuto o converte in un&#39;attività A4T, [!DNL Target] invia i dati dell&#39;evento a [!DNL Analytics]. Questi dati evento consentono a [!DNL Analytics] di attribuire eventi di conversione e altri eventi clickstream che si verificano sulla pagina alle attività e alle esperienze [!DNL Target] rilevanti.

Di seguito sono riportati alcuni punti da tenere presenti quando si visualizzano i report [!DNL Analytics]:

* In generale, come best practice, l’intervallo di reporting deve iniziare dalla data di inizio dell’attività.
* Se si verifica una conversione all&#39;esterno della finestra del report, la conversione non sarà visibile in [!DNL Analytics].
* Nella sezione &quot;mirata&quot; del traffico per le attività [!UICONTROL Auto-Target], i visitatori potrebbero visualizzare esperienze diverse da una sessione all&#39;altra. Ad esempio, se il profilo o il contesto sono cambiati e gli algoritmi di apprendimento automatico di [!DNL Target] decidono che è più probabile che vengano convertiti in una nuova esperienza. Man mano che i visitatori passano da un’esperienza all’altra, il conteggio delle visite aumenta per ogni esperienza visualizzata. A differenza delle normali attività di test A/B, in cui le esperienze sono permanenti per un visitatore durante le visite.
* Se un visitatore vede più esperienze in più visite, qualsiasi conversione viene sempre attribuita all’ultima esperienza che ha visto. Come accennato, il conteggio delle visite aumenta per ogni esperienza visualizzata dal visitatore. Questo può deprimere artificialmente i tassi di conversione per esperienza durante la visualizzazione delle esperienze nella dimensione &quot;[!UICONTROL Targeted]&quot; nei report [!DNL Adobe Analytics].

+++

## Come si tiene traccia delle impression dell&#39;attività in [!DNL Analysis Workspace] quando si utilizza [!UICONTROL Analytics for Target] (A4T)? {#activity-impressions}

+++Risposta

Per visualizzare le impression dell&#39;attività in [!DNL Analysis Workspace]:

1. Nell&#39;interfaccia utente di [!DNL Target], fare clic su **[!UICONTROL View in Analytics]**.
1. Aggiungere la colonna **[!UICONTROL Activity Impressions]** al report [[!DNL Analytics Workspace]](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html){target=_blank}.
1. Nella colonna **[!UICONTROL Activity Impressions]** fare clic sull&#39;icona [!UICONTROL Gear].
1. Fare clic su **[!UICONTROL Use non-default attribution model]**.
1. Selezionare **[!UICONTROL Same Touch Model]** > **[!UICONTROL Apply]**.

+++
