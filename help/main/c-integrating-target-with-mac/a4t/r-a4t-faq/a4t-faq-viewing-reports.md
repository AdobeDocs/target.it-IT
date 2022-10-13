---
keywords: FAQ;domande frequenti;analytics for target;a4t;rapporto;report;visualizzare rapporti;reporting;metodologia di conteggio;impression;visitatori;visite;metriche predefinite;conversioni di attività;non specificato
description: Trova le risposte alle domande più frequenti sulla visualizzazione dei rapporti durante l’utilizzo di Analytics per [!DNL Target] (A4T). A4T consente di utilizzare i rapporti di Analytics per [!DNL Target] attività.
title: Trova risposte alle domande sulla visualizzazione di rapporti con A4T?
feature: Analytics for Target (A4T)
exl-id: a02eeb34-3975-424b-a046-e51f10ae1823
source-git-commit: 34461e3fb6022a0d241cba2e6e31c3113006ee94
workflow-type: tm+mt
source-wordcount: '2638'
ht-degree: 31%

---

# Visualizzare i rapporti - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande più frequenti sulla visualizzazione dei rapporti durante l’utilizzo [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Adobe Target] (A4T).

## Posso visualizzare la mia [!DNL Target] dati attività in [!DNL Analysis Workspace]? {#workspace}

È possibile utilizzare [!DNL Analysis Workspace] per analizzare [!DNL Target] attività ed esperienze. La [Pannello Analytics for Target](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=it) ti consente di visualizzare l’incremento e l’affidabilità per fino a tre metriche di successo. Puoi anche approfondire l’uso di tabelle e visualizzazioni.

Per informazioni ed esempi dettagliati, apri la [Analytics e Target: Esercitazione sulle best practice per l’analisi](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), [!UICONTROL Adobe Experience League].

## Dove possono essere applicati i segmenti in [!DNL Analysis Workspace]? {#segmentation}

I segmenti vengono più comunemente utilizzati nella parte superiore di un pannello nella zona di rilascio dei segmenti. Il segmento viene applicato a tutte le tabelle e visualizzazioni nel pannello . Questa tecnica è particolarmente utile per vedere in che modo il test interessa un sottoinsieme di persone (ad esempio, come si è verificato questo test per le persone nel Regno Unito)?

Un segmento può anche essere disposto su più livelli direttamente all’interno della tabella a forma libera, ma è necessario sovrapporlo all’interno dell’intera tabella per mantenere i calcoli di incremento e affidabilità all’interno del pannello A4T. I segmenti a livello di colonna non sono attualmente supportati nel pannello .

## Posso applicare il modello di Attribution IQ &quot;Same Touch&quot; (Stesso contatto) in [!DNL Analysis Workspace]?

Quando utilizzi [!DNL Target] impression di attività e conversioni in [!DNL Analysis Workspace], applica il modello di Attribution IQ &quot;Same Touch&quot; (Stesso contatto) alle metriche per garantire un conteggio accurato. Per applicare un [modello di attribuzione non predefinito](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/column-row-settings/column-settings.html?lang=it), fai clic con il pulsante destro del mouse sulla metrica per **modificare le impostazioni delle colonne > abilitare Usa modello di attribuzione non predefinito > seleziona Stesso modello di contatto**. Senza l’applicazione di questo modello, le metriche vengono sovrascritte.

Tutte le correnti [!DNL Adobe Analytics] i pacchetti possono aggiungere questo modello con [!UICONTROL Attribution IQ]. Se non hai accesso a [!UICONTROL Attribution IQ]si prega di basarsi sui dati A4T in [!UICONTROL Reports &amp; Analytics].

## Quando si applica un segmento di hit per uno specifico [!DNL Target] perché vengono restituite esperienze non collegate? {#activity-segmentation}

La variabile di [!DNL Target] inviata ad [!DNL Analytics] ha un periodo di scadenza predefinito di 90 giorni. (Nota: se necessario, questo periodo di scadenza può essere regolato dall’Assistenza clienti). Quando i visitatori navigano nel sito in questa finestra di scadenza, fanno parte di molti [!DNL Target] attività, tutte raccolte nella dimensione .

Quando si segmenta l&#39;attività per essere presente in un hit, si ottengono tutte le esperienze che fanno parte di tale attività *plus* qualsiasi altra esperienza persistente su quell&#39;hit.

## Durante la configurazione della [!UICONTROL Metriche dell&#39;obiettivo], perché non posso accedere a [!UICONTROL Impostazioni avanzate]?

Per le attività che utilizzano [!DNL Analytics] come origine per la generazione di rapporti (A4T), la metrica di obiettivo utilizza il valore &quot;[!UICONTROL Incrementa il conteggio e mantieni l’utente nell’attività]&quot; e &quot;[!UICONTROL A ogni impression]&quot; impostazioni. Queste impostazioni sono *not* configurabile.

Per ulteriori informazioni, consulta &quot;Durante la configurazione delle metriche dell’obiettivo, perché non posso accedere alle opzioni Impostazioni avanzate?&quot; in [Definizioni delle metriche - Domande frequenti su A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

## È necessario utilizzare visitatori, visite o impression di attività come metrica di normalizzazione (ovvero metodologia di conteggio)? {#metrics}

Esistono diverse opzioni per normalizzare le metriche nel reporting di A4T. Questa metrica, detta anche metodologia di conteggio, diventa il denominatore del calcolo dell’incremento. Inoltre, influisce sul modo in cui i dati vengono aggregati prima dell’applicazione del calcolo dell’affidabilità.

* I ***visitatori univoci*** incrementano una volta quando un utente si qualifica per la prima volta per un&#39;attività.
* Le ***visite*** incrementano per ogni sessione una volta che un utente (Visitatore univoco) entra in un&#39;attività, anche se l&#39;attività non viene visualizzata nelle visite successive.
* Le ***impressioni dell’attività*** aumentano ogni volta che il contenuto dell&#39;attività viene servito. (Misurato da [!DNL Target]).

Quando un visitatore visualizza una pagina che contiene un&#39;attività, viene impostata una variabile per quel visitatore che contiene il nome di tale attività. Consulta gli scenari dettagliati di seguito per il confronto di ciascuna metodologia di conteggio.

Considera i seguenti aspetti:

* Le metriche sopra indicate si attivano quando un utente si qualifica per un&#39;attività e il contenuto viene restituito da [!DNL Target]. Ciò non significa necessariamente che l&#39;utente abbia visto l&#39;offerta. Se l&#39;esperienza di un’attività si trova nella parte inferiore della pagina e l&#39;utente non scorre la pagina verso il basso, allora l&#39;offerta è stata servita da [!DNL Target] ma non è stata vista dall&#39;utente.
* Le [!UICONTROL impressioni dell’attività] (misurate da [!DNL Target]) e le [!UICONTROL istanze] (misurate da [!DNL Analytics]) sono uguali, a meno che non vi siano più chiamate mbox sulla stessa pagina nella stessa attività. In tal caso si contano più [!UICONTROL impressioni dell’attività], ma solo una singola [!UICONTROL istanza].

Per ulteriori informazioni, consulta [Come impostare rapporti A4T in Analysis Workspace per le attività di Targeting automatico](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html) in *Tutorials Adobe Target*.

## Perché le &quot;impression di attività&quot; e le &quot;conversioni di attività&quot; sono più alte in [!DNL Analysis Workspace] di [!UICONTROL Reports &amp; Analytics]? {#sametouch}

[!DNL Reports & Analytics] applica un modello di attribuzione con lo stesso contatto a &quot;impression di attività&quot; e &quot;conversioni di attività&quot;, mentre [!DNL Analysis Workspace] visualizza le metriche non elaborate, che possono apparire gonfiate a causa della persistenza del [!DNL Target] dimensione.

Per valutare accuratamente [!UICONTROL Impression attività] e [!UICONTROL Conversioni attività] metriche in [!DNL Analysis Workspace], assicurati che entrambe le metriche abbiano [!UICONTROL Stesso contatto] modelli di attribuzione applicati. Per applicare i modelli, fai clic sulla colonna delle impostazioni (icona ingranaggio), abilita [!UICONTROL Modelli di attribuzione non predefiniti], quindi seleziona [!UICONTROL Stesso contatto]. Ulteriori informazioni sull’attribuzione in [Panoramica degli attributi IQ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/attribution.html) in *Guida agli strumenti di Analytics*.

## Che cosa significa &quot;conversioni di attività&quot; se l’addetto al marketing sceglie un [!DNL Analytics] metrica durante l’impostazione dell’attività? {#section_F3EBACF85AF846E9B366A549AAB64356}

Le &quot;conversioni di attività&quot; sono vuote se è [!DNL Analytics] è stata selezionata come metrica di conversione per l’attività.

## Perché viene visualizzato &quot;non specificato&quot; nel [!DNL Analytics] rapporti? Che cosa significa? {#unspecified}

In altri rapporti, “non specificato” significa che i dati non soddisfano una regola di classificazione, ma in A4T non dovrebbe mai verificarsi. Se viene visualizzato “non specificato”, il servizio di classificazione non è ancora stato eseguito. In genere i dati relativi all’attività vengono visualizzati nei rapporti dopo 24-72 ore. Anche se le attività non compaiono in questo rapporto fino a quel momento, tutti i dati dei visitatori associati a tali attività vengono acquisiti e vengono visualizzati al termine della classificazione.

Dopo il periodo di classificazione, i dati sono visualizzati in questi rapporti circa un&#39;ora dopo essere stati raccolti dal sito. Tutte le metriche, i segmenti e i valori nei rapporti provengono dalla suite di rapporti selezionata quando si configura l’attività.

Nel caso in cui la classificazione sia stata effettuata per quell’attività e nel rapporto sia ancora presente una riga &quot;Non specificato&quot;, assicurati che il rapporto non utilizzi un[!DNL Target] per visualizzare i dati. A meno che il rapporto non utilizzi un [!DNL Target]Metrica specifica: la riga &quot;Non specificato&quot; contiene eventi per chiamate non associate a [!DNL Target]. Tale riga non contiene elementi [!DNL Target]Informazioni associate (ad esempio, visitatori/visite/impression).

## Perché [!DNL Target] metriche inviate a [!DNL Analytics] anche dopo che l’attività è stata disattivata? {#section_38AA8380A4D54A18972F1EF3E73E22EF}

La variabile di [!DNL Target] inviata ad [!DNL Analytics] ha un periodo di scadenza predefinito di 90 giorni. Se necessario, questo periodo di scadenza può essere regolato dall’Assistenza clienti. Questa impostazione è globale per tutte le attività; tuttavia, non deve essere adeguato per un caso.

Potresti vedere [!DNL Target] variabili inviate a [!DNL Analytics] dopo il periodo di scadenza perché la scadenza è di 90 giorni, ma solo se l’utente non visualizza mai un altro utente abilitato per A4T [!DNL Target] attività. Se un utente torna al sito dopo 45 giorni e visualizza un’altra attività, l’intero valore eVar di A4T viene ripristinato e i 90 giorni ripartono da tale momento. In questo caso, la prima campagna dal giorno 1 potrebbe quindi durare fino a 45 + 90 = 135 giorni. Se l’utente continua a tornare, potresti arrivare al punto in cui visualizzi le metriche inviate a [!DNL Analytics] nel reporting da attività molto più vecchie. Man mano che gli utenti eliminano i cookie e non ritornano al sito, i numeri in quell’attività diminuiscono, ma puoi comunque visualizzarli.

Questo significa che le attività continuano a ricevere visualizzazioni di pagina, visite e così via, per un massimo di 90 giorni dal termine dell’attività per i visitatori che sono diventati parte dell’attività mentre era attiva. Tuttavia, se osservi la metrica di [!UICONTROL Impression attività], non dovresti più vedere impression dopo la fine dell’attività.

Questo è un comportamento normale e atteso. La variabile A4T funziona come qualsiasi altro eVar: il valore è associato all’utente finché non raggiunge il periodo di scadenza (90 giorni). Di conseguenza, se un’attività è attiva solo per due settimane, il valore rimane associato all’utente per almeno i successivi 90 giorni.

Si consiglia di visualizzare i rapporti per tale attività solo per il periodo di tempo in cui era in corso. Le date devono essere impostate correttamente per impostazione predefinita quando visualizzi l’attività in [!DNL Analytics], quindi, a meno che tu non abbia esteso manualmente la data, questo non dovrebbe essere un problema dal punto di vista della generazione di rapporti.

Ad esempio, supponiamo che la variabile A4T scada dopo 90 giorni e che il test sia attivo dal 1° gennaio al 15 gennaio.

Il 1° gennaio, l’utente entra nel sito, vede l’attività XYZ una volta e visualizza cinque pagine. Nelle due settimane successive, l’utente non ritorna più sul sito. Per questo utente i dati saranno di questo tipo:

| Nome attività | Istanze (impression) | Visualizzazioni pagina | Visite | Visitatori univoci |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 5 | 1 | 1 |

L’utente torna il 1° febbraio, visualizza altre cinque pagine e non incontra altre attività di Target e l’attività originale non è più attiva. Anche se l’attività non è più attiva, continua a seguire l’utente tramite la persistenza eVar. I dati ora si presentano così:

| Nome attività | Istanze (impression) | Visualizzazioni pagina | Visite | Visitatori univoci |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 10 | 2 | 1 |

L’utente torna il 1° marzo e vede una nuova attività: ABC. Anche questa volta l’utente visualizza cinque pagine. Poiché l’attività XYZ continua a seguire l’utente attraverso la persistenza e questo utente ha quindi impostato ABC, vedrai due voci nel rapporto:

| Nome attività | Istanze (impression) | Visualizzazioni pagina | Visite | Visitatori univoci |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 15 | 3 | 1 |
| ABC | 1 | 5 | 1 | 1 |

L’utente poi torna il 1° aprile, visualizza altre cinque pagine ed effettua un acquisto. La scadenza di 90 giorni di quel primo valore di eVar viene reimpostata il 1° aprile, quindi lo puoi vedere nei rapporti. Tutte le attività di Target che l’utente ha visto ricevono credito per la conversione, ma il numero totale di conversioni viene deduplicato:

| Nome attività | Istanze (impression) | Visualizzazioni pagina | Visite | Visitatori univoci | Ordini |
|--- |--- |--- |--- |--- |--- |
| XYZ | 1 | 20 | 4 | 1 | 1 |
| ABC | 1 | 10 | 2 | 1 | 1 |
| Totale | 2 | 20 | 3 | 1 | 1 |

Poiché entrambe le esperienze sono state viste prima della conversione, entrambe ottengono &quot;credito&quot; per l’ordine. Tuttavia, nel sistema è stato effettuato un solo ordine e il totale riflette questa situazione. Per [!DNL Target] rapporti, perché non stai inserendo un [!DNL Target] attività contro un&#39;altra attività per vedere quale ha più successo, non importa che tutte le attività che l&#39;utente ha visto hanno ricevuto credito. Stai confrontando i risultati di due elementi all’interno della singola attività. Non è possibile per un utente vedere diverse esperienze nella stessa attività in modo da non doversi preoccupare di contaminazione incrociata del credito d&#39;ordine.

Per ulteriori informazioni, consulta [Variabili di conversione (eVar)](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html)) nel *Guida per l’amministratore di Analytics*.

## Perché continuo a vedere più impression dopo la disattivazione dell’attività? {#deactivated}

Un’origine di impression per il rapporto di un’attività A4T dopo la disattivazione può essere il traffico in modalità QA. Target normalmente non registra gli eventi per un’attività disattivata, ma Analytics non ha un modo per sapere che le impression provengono dalla modalità di controllo qualità. Quando il rapporto di attività di Target viene recuperato da Analytics, mostra queste impression. Questo funziona correttamente perché i clienti devono poter controllare i rapporti A4T anche se l’attività non è attiva utilizzando la modalità di controllo qualità.

## Perché? [!DNL Analytics] e [!UICONTROL Analytics per Adobe Target] (A4T) calcola i numeri per [!UICONTROL Visitatori unici] metrica diversa? {#section_0C3B648AB54041F9A2AA839D51791883}

Quando esegui un test A/B, che utilizza il [Test t di Welch](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank} (metrica di affidabilità) per scegliere un vincitore di un test, uno dei presupposti è che ci sia un orizzonte temporale fisso. Il test non è statisticamente valido a meno che non si osservi la dimensione del campione fisso.

La [!UICONTROL Visitatori unici] metrica diversa in [!DNL Analytics] e [!DNL Target] solo quando si osserva un periodo più breve del test effettivo. Se non hai raggiunto la dimensione del campione, il test non è affidabile. Per ulteriori informazioni, consulta [How Not to Run an A/B Test](https://www.evanmiller.org/how-not-to-run-an-ab-test.html) (Come non eseguire un test A/B) sul [sito web di Evan Miller](https://www.evanmiller.org/index.html).

La [!UICONTROL Visitatori unici] visualizza il numero di persone che sono state esposte al test che hanno visitato il sito durante il periodo di tempo specificato. Queste persone fanno parte del test e dovrebbero essere conteggiate. Se si desidera visualizzare solo il numero di persone esposte durante una sola settimana, è possibile creare un segmento di visitatori per i quali è stata registrata un’impression di attività e applicare tale segmento al rapporto.

È possibile ridurre la quantità di tempo [!DNL Target] persiste fino a una sessione; tuttavia, questo è problematico per i test in cui l’evento di conversione non è così probabile che si verifichi all’interno della stessa sessione.

## Perché lo stesso visitatore a volte viene conteggiato in più esperienze in [!DNL Analytics]? {#section_1397E972D31C4207A142E4D2D6D794A2}

Di seguito sono elencati i motivi per cui lo stesso visitatore potrebbe essere conteggiato in più esperienze in [!DNL Analytics]:

* La [!DNL Target] profilo scaduto ma [!DNL Analytics] cookie c&#39;è ancora. In tale situazione, [!DNL Target] rivaluta l’utente ma [!DNL Analytics] considera il visitatore come la stessa persona.
* Se il visitatore utilizza il `mbox3rdPartyId`, quando il visitatore anonimo viene unito al profilo ID di terze parti, [!DNL Target] potrebbe mettere il visitatore in un’esperienza diversa per farlo corrispondere all’ID di terze parti. Per ulteriori informazioni, consulta [Sincronizzazione dei profili in tempo reale per mbox3rdPartyID](/help/main/c-target/c-visitor-profile/3rd-party-id.md#concept_BF4113593F614987B1D3E359AE1C5732).
* [!DNL Analytics] potrebbe tenere traccia di dispositivi diversi come lo stesso visitatore in un modo diverso rispetto a [!DNL Target] tiene traccia di tali dispositivi: l&#39;impostazione dell&#39;ID di terze parti in [!DNL Target] è diverso da in Analytics.

## A4T supporta le suite di rapporti virtuali? {#virtual}

Anche se le suite di rapporti virtuali non sono incluse nel [!UICONTROL Suite di rapporti] elenco, i dati A4T condivisi con una suite di rapporti collegata a una suite di rapporti virtuale in [!DNL Analytics] ha accesso a tali dati. Qualsiasi pubblico creato da una suite di rapporti virtuale non può essere condiviso nuovamente in [!DNL Target].

## Posso cambiare la percentuale di allocazione del traffico in un’attività che utilizza A4T dopo che l’attività è stata attivata?

La modifica della percentuale di allocazione del traffico in un&#39;attività dopo l&#39;attivazione può causare rapporti incoerenti in [!DNL Analytics] poiché la modifica interessa solo i nuovi visitatori. I visitatori di ritorno non sono interessati da tale modifica.

Come procedura ottimale, devi arrestare l’attività esistente, quindi creare una nuova attività invece di modificare la percentuale dopo l’attivazione. Il reporting per la nuova attività inizia con nuovi visitatori e i dati dei visitatori di ritorno non causano rapporti incoerenti.

## In che modo vengono conteggiate le visite [!DNL Analytics] e credito di conversione assegnato in un [!UICONTROL Targeting automatico] attività che utilizza A4T?

Quando un visitatore si qualifica, visualizza il contenuto o effettua la conversione in un’attività A4T, [!DNL Target] invia i dati evento a [!DNL Analytics]. Questi dati dell’evento consentono [!DNL Analytics] per attribuire gli eventi di conversione e altri eventi clickstream che si verificano sulla pagina al [!DNL Target] attività ed esperienze.

Di seguito sono riportati alcuni punti da tenere a mente durante la visualizzazione [!DNL Analytics] rapporti:

* In generale, come best practice, l’intervallo di reporting deve iniziare dalla data di inizio dell’attività.
* Se una conversione si verifica al di fuori della finestra del rapporto, la conversione non è visibile in [!DNL Analytics].
* Nella parte &quot;mirata&quot; del traffico per [!UICONTROL Targeting automatico] attività, i visitatori potrebbero vedere esperienze diverse da una sessione all’altra. Ad esempio, se il profilo o il contesto sono cambiati e [!DNL Target]Gli algoritmi di machine-learning decidono che è più probabile che siano convertiti su una nuova esperienza. Man mano che i visitatori passano dall’esperienza all’esperienza, il conteggio delle visite incrementa per ogni esperienza visualizzata. Ciò è diverso dalle normali attività di test A/B in cui le esperienze sono appiccicose a un visitatore durante le visite.
* Se un visitatore visualizza più esperienze in più visite, qualsiasi conversione è sempre attribuita all’ultima esperienza visualizzata dal visitatore. Come accennato, il conteggio delle visite incrementa ogni esperienza visualizzata dal visitatore. Questo può eliminare artificialmente i tassi di conversione per esperienza quando visualizzi le esperienze sotto &quot;[!UICONTROL Target]&quot; dimensione in [!DNL Adobe Analytics] rapporti.
