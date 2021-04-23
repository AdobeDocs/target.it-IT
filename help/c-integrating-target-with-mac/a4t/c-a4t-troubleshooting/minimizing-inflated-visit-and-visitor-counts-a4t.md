---
keywords: dati parziali;dati parziali;A4T;incongruenze;analytics for target;orfano;suite rapporti virtuali;phantom;risoluzione dei problemi;dati parziali;gonfiato;non specificato
description: Scopri come ridurre al minimo gli effetti dei conteggi gonfiati per visite e visitatori quando utilizzi Analytics for [!DNL Target] (A4t). Scopri cosa sono i "dati parziali" e come ridurli.
title: Come posso ridurre al minimo i conteggi gonfiati per visite e visitatori in A4T?
feature: Analytics for Target (A4T)
exl-id: 308711f7-e630-4f6b-8a6d-a1f36ed7902d
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '1362'
ht-degree: 48%

---

# Minimizzare i conteggi gonfiati per visite e visitatori in A4T

Informazioni che consentono di ridurre al minimo gli effetti dei conteggi gonfiati per visite e visitatori quando si utilizza [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Adobe Target] (A4T).

>[!IMPORTANT]
>Il 14 novembre 2016, in Adobe Analytics sonos tate cambiate le modalità di elaborazione di alcuni dati per i clienti che utilizzano le funzioni di reporting di Analytics per Target (A4T). Queste modifiche consentono un migliore allineamento dei dati di Adobe Target con il modello dati di Adobe Analytics. Le suddette modifiche sono state apportate per tutti i clienti che utilizzano A4T. Queste modifiche rispondono specificamente a un problema notato dai clienti, relativo a un conteggio eccessivo dei visitatori quando le attività di Target sono in esecuzione.
>
>Questo cambiamento non è retroattivo. Se i rapporti cronologici mostrano conteggi gonfiati e desideri escluderli, puoi creare una suite di rapporti virtuale, come descritto di seguito.
>
>Inoltre, diverse librerie JavaScript sono state aggiornate per ridurre al minimo i conteggi gonfiati. Adobe consiglia di eseguire l&#39;aggiornamento alle seguenti versioni della libreria (o successive):
>
>* Servizio ID visitatore di Experience Cloud: visitorAPI.js versione 2.3.0 o successiva.
>* Adobe Analytics: appMeasurement.js versione 2.1.
>* Adobe Target: at.js versione 0.9.6 o successiva (eccetto versione 1.1.0 se si utilizza il reindirizzamento con A4T).

>
>  
La libreria mbox.js non supporta le offerte di reindirizzamento con A4T. L’implementazione deve utilizzare at.js.

## Cosa è cambiato? {#section_9CCF45F5D66D48EBA88F3A178B27D986}

Quando [!DNL Adobe Analytics] viene utilizzato per misurare le attività [!DNL Target] (chiamate A4T), [!DNL Analytics] raccoglie dati aggiuntivi che non sono disponibili quando non è presente alcuna attività [!DNL Target] nella pagina. L’attività [!DNL Target] genera una chiamata nella parte superiore della pagina, ma [!DNL Analytics] in genere genera le chiamate di raccolta dati nella parte inferiore della pagina. Nell’implementazione di A4T fino a oggi, l’Adobe include questi dati aggiuntivi ogni volta che un’attività [!DNL Target] era attiva. In futuro, Adobe include questi dati aggiuntivi solo quando sono attivati sia i tag [!DNL Target] che [!DNL Analytics] .

## Perché Adobe ha introdotto questa modifica? {#section_92380A4BD69E4B8886692DD27540C92A}

L&#39;accuratezza e la qualità dei dati sono motivo di orgoglio per Adobe. Quando il tag [!DNL Target] viene attivato, ma il tag [!DNL Analytics] no, Analytics registra i dati parziali (a volte denominati &quot;hit non uniti&quot;). Questi risultati non uniti non vengono acquisiti da [!DNL Analytics] in assenza di attività [!DNL Target]. L’inclusione dei dati parziali nella reportistica di [!DNL Analytics] fornisce informazioni aggiuntive, ma genera anche hit incoerenti per i dati precedenti relativi a periodi in cui non vi erano attività [!DNL Target] in esecuzione. Questa situazione può causare problemi agli utenti [!DNL Analytics] che analizzano le tendenze nel tempo. Al fine di garantire la coerenza dei dati in [!DNL Analytics], l’Adobe esclude tutti i dati parziali.

## Cosa contribuisce ai dati parziali? {#section_C9C906BEAA7D44DAB9D3C03932A2FEB8}

Ad Adobe, alcuni clienti con tassi elevati di dati parziali in [!DNL Analytics]. Elevati tassi di dati parziali possono derivare da un’implementazione impropria, ma esistono anche cause legittime.

Le cause identificate dei dati parziali includono le seguenti:

* **ID delle suite di rapporti non allineati (implementazione):** la suite di rapporti specificata durante la configurazione dell’attività non corrisponde alla suite di rapporti nella pagina in cui viene consegnato il test. I dati non possono essere riconciliati sui server [!DNL Analytics], in modo da avere un aspetto simile ai dati parziali.
* **Pagine lente:** [!DNL Target] le chiamate sono nella parte superiore della pagina e le  [!DNL Analytics] chiamate solitamente sono nella parte inferiore della pagina. Se la pagina viene caricata lentamente, aumenta la probabilità che un visitatore lasci la pagina dopo che la chiamata [!DNL Target] viene attivata, ma prima della chiamata [!DNL Analytics] . Le pagine lente possono essere particolarmente problematiche sui siti web mobili, dove le connessioni sono spesso più lente.
* **Errori di pagina:** se ci sono errori JavaScript o altri scenari in cui ciascuno dei punti di contatto non si attiva (servizio Experience Cloud ID, Target e Analytics), risultati di dati parziali.
* **Offerte di reindirizzamento nell’ [!DNL Target] attività:** per le offerte di reindirizzamento nelle attività che utilizzano A4T, l’implementazione deve soddisfare determinati requisiti minimi. Inoltre, è necessario conoscere informazioni importanti. Per ulteriori informazioni, consulta [Offerte di reindirizzamento: domande frequenti su A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#section_FA9384C2AA9D41EDBCE263FFFD1D9B58).
* **Versioni precedenti delle librerie:** nell’ultimo anno Adobe ha apportato diversi miglioramenti alle librerie JavaScript (  [!DNL appMeasurement.js],  `at.js/mbox.js` e  `visitorAPI.js`) per garantire che i dati vengano inviati nel modo più efficiente possibile. Per ulteriori informazioni sui requisiti di implementazione, consulta [Prima di implementare](/help/c-integrating-target-with-mac/a4t/before-implement.md#concept_046BC89C03044417A30B63CE34C22543).

## Quali sono le best practice per ridurre i dati parziali? {#section_065C38501527451C8058278054A1818D}

Esamina i seguenti passaggi per ridurre la raccolta parziale dei dati:

| Passaggio | Attività |
| --- | --- |
| ![Passaggio 1](assets/step1_icon.png) | Assicurati che la suite di rapporti selezionata in [!DNL Target] sia la stessa di quella sulle pagine in cui viene presentata l&#39;attività. |
| ![Passaggio 2](assets/step2_icon.png) | Assicurati che le librerie visitorAPI.js, appMeasurement.js, at.js / mbox.js siano in versioni compatibili con A4T. Per ulteriori informazioni sui requisiti di implementazione, consulta [Prima di implementare](/help/c-integrating-target-with-mac/a4t/before-implement.md). |
| ![Passaggio 3](assets/step3_icon.png) | Assicurati che l’identificatore SDID sia impostato su tutte le chiamate [!DNL Target] e [!DNL Analytics] che lasciano la pagina e che corrispondano.<br/>Utilizza un analizzatore di rete o uno strumento di debug per garantire che il  `mboxMCSDID` parametro sulle  [!DNL Target] chiamate corrisponda al parametro SDID nella  [!DNL Analytics] chiamata . |
| ![Passaggio 4](assets/step4_icon.png) | Verifica che le librerie di implementazione nei tuoi siti vengano caricate nell&#39;ordine corretto. Per ulteriori informazioni, consulta [Implementazione di Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4timplementation.md). |

## Come posso vedere quanti dati parziali ci sono? {#section_89B663E2824A4805AB934153508A0F4B}

Sebbene queste informazioni non siano disponibili direttamente in [!DNL Analytics], è possibile contattare l’Assistenza clienti di Adobe per richiedere un rapporto sui dati parziali. Questo rapporto ha lo scopo di facilitare il debug.

## Come posso visualizzare le tendenze della cronologia senza dati parziali? {#section_4C9DED560FAD4428B362DDA2064897C3}

Questa modifica di elaborazione influisce sui dati solo dopo la data di rilascio (14 novembre 2016). Se desideri modificare le metriche storiche in modo che corrispondano, Adobe consiglia di creare un segmento per escludere i dati parziali.

Le informazioni seguenti relative a questo cambiamento includono istruzioni su come definire il segmento e applicarlo a una suite di rapporti virtuale in modo che questo segmento venga sempre applicato alle visualizzazioni di [!DNL Analytics].

Nella maggior parte delle situazioni, un risultato di [!DNL Target] è vincolato a un risultato di [!DNL Analytics] su ogni pagina web. Questo vincolo si verifica se c’è un SDID coerente nella chiamata di [!DNL Target] e in quella di [!DNL Analytics] e un [!DNL Experience Cloud ID] (MCID) nella chiamata di [!DNL Analytics] sulla stessa pagina. [!DNL Target] Normalmente ha anche il MCID, ma se la chiamata a  [!DNL Target] si verifica prima che l&#39;ID visitatore venga restituito, il risultato è ancora vincolato a causa dell&#39;SDID. Inoltre, l’utente deve rimanere sulla pagina abbastanza a lungo per generare una chiamata [!DNL Analytics] dopo che è stata attivata una chiamata di [!DNL Target]. Questo scenario è ideale.

**Risultati con dati parziali:** gli utenti a volte non rimangono su una pagina abbastanza a lungo per inviare una chiamata di [!DNL Analytics], ma [!DNL Target] ha un MCID corretto. Questo scenario si traduce in risultati con dati parziali (risultati senza visualizzazioni di pagina [!DNL Analytics]). Se questi utenti tornano sul tuo sito e visualizzano una pagina contenente codice [!DNL Analytics], vengono conteggiati correttamente come visitatori di ritorno. Questi risultati verrebbero persi se sulla pagina fosse presente solo il codice [!DNL Analytics] . Alcuni clienti non desiderano i dati per questi risultati perché gonfiano determinate metriche (visite) e ne riducono altre (visualizzazioni di pagina per visita, durata per visita, ecc.). Puoi anche vedere le visite senza alcuna visualizzazione di pagina. Tuttavia, esistono anche validi motivi per mantenere questi dati.

Per ridurre al minimo i risultati con dati parziali, velocizza il caricamento della pagina, aggiorna le librerie alle versioni più recenti oppure crea una [suite di rapporti virtuale](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) che escluda tali risultati. Per istruzioni dettagliate, consulta [Creare suite di rapporti virtuali](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) nella *Guida ai componenti di Analytics*.

Nell&#39;illustrazione seguente viene mostrata la definizione di un segmento per la suite di rapporti virtuale:

![](assets/ts_a4t.png)

Quando si crea la suite di rapporti virtuale, specificare la seguente configurazione per la definizione del segmento (come mostrato nell&#39;illustrazione precedente):

* **Mostra risultato:**
* Analytics for Target: esiste
* E
* Visualizzazioni pagine: non esiste
* E
* Istanze di collegamento personalizzato: non esiste
* E
* Istanze di collegamento di download: non esiste
* E
* Istanze di collegamento di uscita: non esiste

**Risultati orfani:** in poche situazioni, gli utenti non rimangono sulla pagina abbastanza a lungo per una chiamata Analytics e Target non riceve un MCID corretto. Questi hit sono quelli che l’Adobe definisce hit &quot;orfani&quot;. Rappresentano i clienti che ritornano raramente e gonfiano il conteggio delle visite e dei visitatori.

Per ridurre al minimo i risultati orfani, è possibile creare una [suite di rapporti virtuale](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html) che escluda tali risultati, come spiegato in precedenza.

## Che cosa significa questo per i rapporti di [!DNL Target]? {#section_AAD354C722BE46D4875507F0FCBA5E36}

Una volta che si verifica questa modifica, potresti notare una diminuzione dei nuovi visitatori e delle visite ai test live perché [!DNL Adobe] non elabora i dati parziali in arrivo. Le conversioni e i risultati di altre metriche [!DNL Analytics] non cambieranno.
