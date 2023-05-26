---
keywords: FAQ;domande frequenti;analytics for target;a4t;rapporto;report;visualizzare rapporti;reporting;metodologia di conteggio;impression;visitatori;visite;metriche predefinite;conversioni di attività;non specificato
description: Risposte alle domande più frequenti sulla visualizzazione dei rapporti durante l’utilizzo di Analytics per [!DNL Target] (A4T). A4T consente di utilizzare il reporting di Analytics per [!DNL Target] attività.
title: Risposte alle domande sulla visualizzazione di rapporti con A4T?
feature: Analytics for Target (A4T)
exl-id: a02eeb34-3975-424b-a046-e51f10ae1823
source-git-commit: 79ae58377c9eea0faca1ade11f2ab53da56b7bc1
workflow-type: tm+mt
source-wordcount: '2714'
ht-degree: 29%

---

# Visualizzare i rapporti - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande che vengono spesso poste in merito alla visualizzazione dei report durante l&#39;utilizzo di [!DNL Adobe Analytics] come origine di reporting per [!DNL Adobe Target] (A4T).

## Posso visualizzare il mio [!DNL Target] dati attività in [!DNL Analysis Workspace]? {#workspace}

+++Risposta utilizzabile [!DNL Analysis Workspace] per analizzare [!DNL Target] attività ed esperienze. Il [Pannello Analytics for Target](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=it) consente di visualizzare incremento e affidabilità per un massimo di tre metriche di successo. Puoi anche approfondire la ricerca utilizzando tabelle e visualizzazioni.

Per informazioni ed esempi dettagliati, apri [Analytics &amp; Target: esercitazione sulle best practice per l&#39;analisi](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), fornito da [!UICONTROL Adobe Experience League].

+++

## Dove possono essere applicati i segmenti in [!DNL Analysis Workspace]? {#segmentation}

+++I segmenti di risposta sono più comunemente utilizzati nella parte superiore di un pannello nella zona di rilascio dei segmenti. Il segmento viene applicato a tutte le tabelle e visualizzazioni nel pannello. Questa tecnica è più utile per vedere in che modo il test influisce su un sottoinsieme di persone (ad esempio, come ha funzionato questo test per le persone nel Regno Unito)?

Un segmento può anche essere aggiunto a livelli direttamente all’interno della tabella a forma libera, ma tieni presente che devi sovrapporlo all’intera tabella per mantenere i calcoli di incremento e affidabilità all’interno del pannello A4T. Al momento, i segmenti a livello di colonna non sono supportati nel pannello.

+++

## Posso applicare il modello di Attribution IQ &quot;Same Touch&quot; (Stesso contatto) in? [!DNL Analysis Workspace]?

+++Rispondi quando si utilizza [!DNL Target] impressioni di attività e conversioni in [!DNL Analysis Workspace], applica il modello di Attribution IQ &quot;Same Touch&quot; (Stesso contatto) alle metriche per garantire un conteggio preciso. Per applicare un [modello di attribuzione non predefinito](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/column-row-settings/column-settings.html?lang=it), fai clic con il pulsante destro del mouse sulla metrica per **modificare le impostazioni delle colonne > abilitare Usa modello di attribuzione non predefinito > seleziona Stesso modello di contatto**. Senza l’applicazione di questo modello, le metriche vengono sovrascritte.

Tutti gli attuali [!DNL Adobe Analytics] I pacchetti possono aggiungere questo modello con [!UICONTROL Attribution IQ]. Se non hai accesso a [!UICONTROL Attribution IQ], utilizza i dati A4T in [!UICONTROL Reports &amp; Analytics].

+++

## Quando applico un segmento di hit per uno specifico [!DNL Target] attività, perché vengono restituite esperienze non correlate? {#activity-segmentation}

+++Rispondi [!DNL Target] variabile inviata a [!DNL Analytics] ha un periodo di scadenza predefinito di 90 giorni. (Nota: se necessario, questo periodo di scadenza può essere modificato dall’Assistenza clienti). I visitatori che navigano nel sito attraverso questa finestra di scadenza fanno parte di molti [!DNL Target] attività, che si raccolgono tutte nella dimensione.

Quando segmenti un’attività affinché sia presente in un hit, ottieni tutte le esperienze che fanno parte di tale attività *più* qualsiasi altra esperienza che persiste su tale hit.

+++

## Durante la configurazione di [!UICONTROL Metriche obiettivo], perché non posso accedere a [!UICONTROL Impostazioni avanzate]?

+++Risposta per le attività che utilizzano [!DNL Analytics] come origine per la generazione di rapporti (A4T), la metrica di obiettivo utilizza il codice &quot;[!UICONTROL Incrementa il conteggio e mantieni l&#39;utente attivo]&quot; e &quot;[!UICONTROL A ogni impression]&quot;. Queste impostazioni sono *non* configurabile.

Per ulteriori informazioni, consulta &quot;Perché non posso accedere alle opzioni Impostazioni avanzate durante la configurazione delle metriche dell’obiettivo?&quot; in [Definizioni delle metriche - Domande frequenti su A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

+++

## Devo utilizzare visitatori, visite o impression di attività come metrica di normalizzazione (cioè come metodologia di conteggio)? {#metrics}

+++Risposta Esistono diverse opzioni per normalizzare le metriche nei rapporti di A4T. Questa metrica, detta anche metodologia di conteggio, diventa il denominatore del calcolo dell’incremento. Inoltre, influisce sul modo in cui i dati vengono aggregati prima dell’applicazione del calcolo dell’affidabilità.

* I ***visitatori univoci*** incrementano una volta quando un utente si qualifica per la prima volta per un&#39;attività.
* Le ***visite*** incrementano per ogni sessione una volta che un utente (Visitatore univoco) entra in un&#39;attività, anche se l&#39;attività non viene visualizzata nelle visite successive.
* Le ***impressioni dell’attività*** aumentano ogni volta che il contenuto dell&#39;attività viene servito. (Misurato da [!DNL Target]).

Quando un visitatore visualizza una pagina che contiene un&#39;attività, viene impostata una variabile per quel visitatore che contiene il nome di tale attività. Consulta gli scenari dettagliati di seguito per il confronto di ciascuna metodologia di conteggio.

Considera i seguenti aspetti:

* Le metriche di cui sopra si attivano quando un utente si qualifica per un&#39;attività e il contenuto viene restituito da [!DNL Target]. Ciò non significa necessariamente che l&#39;utente abbia visto l&#39;offerta. Se l&#39;esperienza di un’attività si trova nella parte inferiore della pagina e l&#39;utente non scorre la pagina verso il basso, allora l&#39;offerta è stata servita da [!DNL Target] ma non è stata vista dall&#39;utente.
* Le [!UICONTROL impressioni dell’attività] (misurate da [!DNL Target]) e le [!UICONTROL istanze] (misurate da [!DNL Analytics]) sono uguali, a meno che non vi siano più chiamate mbox sulla stessa pagina nella stessa attività. In tal caso si contano più [!UICONTROL impressioni dell’attività], ma solo una singola [!UICONTROL istanza].

Per ulteriori informazioni, consulta [Impostare rapporti A4T in Analysis Workspace per le attività di Targeting automatico](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=it) in *Tutorials Adobe Target*.

+++

## Perché le &quot;impressioni di attività&quot; e le &quot;conversioni di attività&quot; sono più alte in [!DNL Analysis Workspace] rispetto a [!UICONTROL Reports &amp; Analytics]? {#sametouch}

+++Risposta
[!DNL Reports & Analytics] applica un modello di attribuzione di stesso contatto alle &quot;impression dell’attività&quot; e alle &quot;conversioni dell’attività&quot;, mentre [!DNL Analysis Workspace] visualizza le metriche non elaborate, che possono apparire gonfiate a causa della persistenza del [!DNL Target] dimensione.

Per valutare accuratamente [!UICONTROL Impression attività] e [!UICONTROL Conversioni attività] metriche in [!DNL Analysis Workspace], assicurati che entrambe le metriche abbiano [!UICONTROL Stesso contatto] modelli di attribuzione applicati. Per applicare i modelli, fai clic sulla colonna delle impostazioni (icona ingranaggio), abilita [!UICONTROL Modelli di attribuzione non predefiniti], quindi seleziona [!UICONTROL Stesso contatto]. Ulteriori informazioni sull’attribuzione in [Panoramica di Attributes IQ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/attribution.html) nel *Guida agli strumenti di Analytics*.

+++

## Che cosa significa &quot;conversioni di attività&quot; se l’addetto al marketing sceglie un [!DNL Analytics] metrica durante la configurazione dell’attività? {#section_F3EBACF85AF846E9B366A549AAB64356}

+++La risposta &quot;Conversioni attività&quot; è vuota se un [!DNL Analytics] metrica selezionata come metrica di conversione per l’attività.

+++

## Perché viene visualizzato &quot;non specificato&quot; nella [!DNL Analytics] rapporti? Che cosa significa? {#unspecified}

+++Risposta In altri rapporti, &quot;non specificato&quot; significa che i dati non soddisfano una regola di classificazione, ma in A4T questo non dovrebbe mai accadere. Se viene visualizzato “non specificato”, il servizio di classificazione non è ancora stato eseguito. In genere i dati relativi all’attività vengono visualizzati nei rapporti dopo 24-72 ore. Anche se le attività non compaiono ancora nel rapporto, tutti i dati dei visitatori associati a tali attività vengono comunque acquisiti e visualizzati al termine della classificazione.

Dopo il periodo di classificazione, i dati sono visualizzati in questi rapporti circa un&#39;ora dopo essere stati raccolti dal sito. Tutte le metriche, i segmenti e i valori nei rapporti provengono dalla suite di rapporti selezionata quando si configura l’attività.

Nel caso in cui la classificazione sia stata eseguita per tale attività e nel rapporto venga ancora visualizzata una riga con dicitura &quot;Non specificata&quot;, assicurati che il rapporto non utilizzi un tag[!DNL Target] metrica per visualizzare i dati. A meno che il report non utilizzi [!DNL Target]metrica specifica di, la riga con dicitura &quot;Non specificata&quot; contiene eventi per chiamate non associate a [!DNL Target]. La riga non conterrà alcun [!DNL Target]informazioni associate a (ad esempio, visitatori/visite/impression).

+++

## Perché sono [!DNL Target] metriche inviate a [!DNL Analytics] anche dopo la disattivazione dell’attività? {#section_38AA8380A4D54A18972F1EF3E73E22EF}

+++Rispondi [!DNL Target] variabile inviata a [!DNL Analytics] ha un periodo di scadenza predefinito di 90 giorni. Se necessario, questo periodo di scadenza può essere modificato dall’Assistenza clienti. Questa impostazione è globale per tutte le attività; tuttavia, non deve essere corretta per un caso.

Potresti vedere [!DNL Target] variabili inviate a [!DNL Analytics] dopo il periodo di scadenza perché la scadenza è di 90 giorni, ma solo se tale utente non vede mai un altro A4T-abilitato [!DNL Target] attività. Se un utente torna al sito dopo 45 giorni e visualizza un’altra attività, l’intero valore eVar di A4T viene ripristinato e i 90 giorni ripartono da tale momento. In questo caso, la prima campagna dal giorno 1 potrebbe quindi durare fino a 45 + 90 = 135 giorni. Se l’utente continua a tornare, si potrebbe arrivare al punto in cui vengono visualizzate le metriche inviate a [!DNL Analytics] nei rapporti da attività molto più vecchie. Poiché gli utenti eliminano i cookie e non tornano sul sito, i numeri in tale attività diminuiscono, ma puoi ancora visualizzarli.

Ciò significa che le attività continuano a ricevere visualizzazioni di pagina, visite e così via, fino a 90 giorni dopo il termine dell’attività per i visitatori che sono diventati parte dell’attività mentre era attiva. Tuttavia, se osservi la metrica di [!UICONTROL Impression attività], non dovresti più vedere impression dopo la fine dell’attività.

Questo è un comportamento normale e atteso. La variabile A4T funziona come qualsiasi altro eVar: il valore è associato all’utente finché non raggiunge il periodo di scadenza (90 giorni). Di conseguenza, se un’attività è attiva solo per due settimane, il valore rimane associato all’utente per almeno i successivi 90 giorni.

Si consiglia di visualizzare i rapporti per tale attività solo per il periodo di tempo in cui era in corso. Le date devono essere impostate correttamente per impostazione predefinita quando visualizzi l’attività in [!DNL Analytics], quindi a meno che tu non abbia esteso manualmente la data, questo non dovrebbe essere un problema dal punto di vista della reportistica.

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

Poiché entrambe le esperienze sono state viste prima della conversione, entrambe ricevono il &quot;merito&quot; per l’ordine. Tuttavia, nel sistema è stato effettuato un solo ordine e il totale riflette questa situazione. Per [!DNL Target] generazione rapporti, perché non stai inserendo un [!DNL Target] per vedere quale attività ha più successo, non importa che tutte le attività viste dall’utente abbiano ricevuto credito. Stai confrontando i risultati di due elementi all’interno della singola attività. Non è possibile per un utente vedere diverse esperienze nella stessa attività, quindi non devi preoccuparti della contaminazione incrociata del credito dell’ordine.

Per ulteriori informazioni, consulta [Variabili di conversione (eVar)](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html)) in *Guida per l’amministratore di Analytics*.

+++

## Perché continuo a vedere più impression dopo la disattivazione dell’attività? {#deactivated}

+++Risposta Un’origine di impression al rapporto di un’attività A4T dopo la disattivazione può essere il traffico in modalità QA. Target di solito non registra gli eventi per un’attività disattivata, ma Analytics non dispone di un modo per sapere che le impression provengono dalla modalità di controllo qualità. Quando il rapporto attività di Target viene recuperato da Analytics, mostra queste impression. Questo funziona come previsto perché i clienti hanno bisogno di un modo per controllare i rapporti A4T anche se l’attività non è attiva utilizzando la modalità di controllo qualità.

+++

## Perché farlo [!DNL Analytics] e [!UICONTROL Analytics per Adobe Target] (A4T) calcola i numeri per [!UICONTROL Visitatori univoci] metrica in modo diverso? {#section_0C3B648AB54041F9A2AA839D51791883}

+++Risposta quando si esegue un test A/B, che utilizza il [Test t di Welch](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank} (la metrica di affidabilità) per scegliere un vincitore di un test, uno dei presupposti è che vi sia un orizzonte temporale fisso. Il test non è statisticamente valido a meno che non si osservi la dimensione del campione fissa.

Il [!UICONTROL Visitatori univoci] la metrica è diversa in [!DNL Analytics] e [!DNL Target] solo quando si osserva un periodo più breve del test effettivo. Se non hai raggiunto la dimensione del campione, il test non è altrettanto affidabile. Per ulteriori informazioni, consulta [How Not to Run an A/B Test](https://www.evanmiller.org/how-not-to-run-an-ab-test.html) (Come non eseguire un test A/B) sul [sito web di Evan Miller](https://www.evanmiller.org/index.html).

Il [!UICONTROL Visitatori univoci] metrica mostra il numero di persone che sono state esposte al test e che hanno visitato il sito durante il periodo di tempo specificato. Queste persone fanno parte del test e devono essere conteggiate. Se si desidera visualizzare solo il numero di persone esposte durante una sola settimana, è possibile creare un segmento di visitatori per i quali è stata registrata un’impression di attività e applicare tale segmento al rapporto.

È possibile ridurre la quantità di tempo [!DNL Target] La variabile persiste fino a una sessione; tuttavia, ciò è problematico per i test in cui la probabilità che l’evento di conversione si verifichi all’interno della stessa sessione non è altrettanto elevata.

+++

## Perché lo stesso visitatore a volte viene conteggiato in più esperienze in [!DNL Analytics]? {#section_1397E972D31C4207A142E4D2D6D794A2}

+++Risposta Il seguente elenco spiega perché lo stesso visitatore potrebbe essere conteggiato in più esperienze in [!DNL Analytics]:

* Il [!DNL Target] profilo scaduto ma il [!DNL Analytics] Il cookie è ancora lì. In questa situazione, [!DNL Target] rivaluta l’utente ma [!DNL Analytics] considera il visitatore come la stessa persona.
* Se il visitatore utilizza `mbox3rdPartyId`, quando il visitatore anonimo viene unito al profilo ID di terze parti, [!DNL Target] potrebbe porre il visitatore in un’esperienza diversa per farlo corrispondere all’ID di terze parti. Per ulteriori informazioni, consulta [Sincronizzazione dei profili in tempo reale per mbox3rdPartyID](/help/main/c-target/c-visitor-profile/3rd-party-id.md#concept_BF4113593F614987B1D3E359AE1C5732).
* [!DNL Analytics] potrebbe tracciare dispositivi diversi dello stesso visitatore in modo diverso rispetto a [!DNL Target] tiene traccia di tali dispositivi: l’impostazione dell’ID di terze parti in [!DNL Target] è diverso da Analytics.

+++

## A4T supporta le suite di rapporti virtuali? {#virtual}

+++Risposta Sebbene le suite di rapporti virtuali non siano incluse nel [!UICONTROL Suite di rapporti] , qualsiasi dato A4T condiviso con una suite di rapporti collegata a una suite di rapporti virtuale in [!DNL Analytics] ha accesso a tali dati. Nessun pubblico creato da suite di rapporti virtuali può essere condiviso nuovamente in [!DNL Target].

+++

## Posso cambiare la percentuale di allocazione del traffico in un’attività che utilizza A4T dopo che l’attività è stata attivata?

+++Risposta La modifica della percentuale di allocazione del traffico in un’attività dopo l’attivazione può causare rapporti incoerenti in [!DNL Analytics] perché la modifica interessa solo i nuovi visitatori. I visitatori di ritorno non sono interessati da tale modifica.

Come procedura ottimale, devi arrestare l’attività esistente, quindi creare una nuova attività invece di modificare la percentuale dopo l’attivazione. La generazione di rapporti per la nuova attività inizia con nuovi visitatori e i dati dei visitatori di ritorno non causano rapporti incoerenti.

+++

## Come vengono conteggiate le visite in [!DNL Analytics] e credito di conversione allocati in un [!UICONTROL Targeting automatico] attività che utilizza A4T?

+++Risposta quando un visitatore si qualifica per, visualizza contenuto o converte in un’attività A4T, [!DNL Target] invia dati evento a [!DNL Analytics]. Questi dati evento consentono [!DNL Analytics] per attribuire gli eventi di conversione e altri eventi clickstream che si verificano sulla pagina a [!DNL Target] attività ed esperienze.

Di seguito sono riportati alcuni punti da tenere presenti durante la visualizzazione [!DNL Analytics] rapporti:

* In generale, come best practice, l’intervallo di reporting deve iniziare dalla data di inizio dell’attività.
* Se si verifica una conversione all’esterno della finestra del rapporto, la conversione non è visibile in [!DNL Analytics].
* Quando si trova nella sezione &quot;mirata&quot; del traffico per [!UICONTROL Targeting automatico] attività, i visitatori potrebbero visualizzare esperienze diverse da una sessione all’altra. Ad esempio, se il loro profilo o contesto è cambiato e [!DNL Target]Gli algoritmi di apprendimento automatico di decidono che hanno maggiori probabilità di essere convertiti in una nuova esperienza. Man mano che i visitatori passano da un’esperienza all’altra, il conteggio delle visite aumenta per ogni esperienza visualizzata. A differenza delle normali attività di test A/B, in cui le esperienze sono permanenti per un visitatore durante le visite.
* Se un visitatore vede più esperienze in più visite, qualsiasi conversione viene sempre attribuita all’ultima esperienza che ha visto. Come accennato, il conteggio delle visite aumenta per ogni esperienza visualizzata dal visitatore. Questo può deprimere artificialmente i tassi di conversione per esperienza quando si visualizzano le esperienze in &quot;[!UICONTROL Target]&quot; dimensione in [!DNL Adobe Analytics] rapporti.

+++

## Come si tiene traccia delle impression dell’attività in [!DNL Analysis Workspace] quando utilizzi [!UICONTROL Analytics for Target] (A4T)? {#activity-impressions}

+++Risposta

Per visualizzare le impression dell’attività in [!DNL Analysis Workspace]:

1. In [!DNL Target] UI, fai clic su **[!UICONTROL Visualizza in Analytics]**.
1. Aggiungi il **[!UICONTROL Impression attività]** colonna al [[!DNL Analytics Workspace]](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html){target=_blank} rapporto.
1. Il giorno **[!UICONTROL Impression attività]** , fare clic sul pulsante [!UICONTROL Ingranaggio] icona.
1. Clic **[!UICONTROL Usa modello di attribuzione non predefinito]**.
1. Seleziona **[!UICONTROL Stesso modello di contatto]** > **[!UICONTROL Applica]**.

+++