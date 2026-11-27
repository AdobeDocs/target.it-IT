---
keywords: risoluzione dei problemi;domande frequenti;FAQ;consigli;caratteri speciali;ponderazione degli attributi;somiglianza contenuti
description: Visualizza un elenco delle domande e risposte più frequenti sulle attività [!DNL Target Recommendations].
title: Dove posso trovare domande e risposte su [!DNL Recommendations]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: aaa52923-1c2d-44ae-bd89-671329222077
TQID: 'https://experienceleague.adobe.com/Hz37Dp21q-25Pj6mmbiaGqONY14eImVB9Ebz8VH9hMA'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '3560'
ht-degree: 10%
---
# Domande frequenti sui consigli {#recommendations-faq}

>[!BEGINSHADEBOX]

**In questa pagina:** Trova le risposte alle domande frequenti sulle attività [!DNL Adobe Target] [!DNL Recommendations].

>[!ENDSHADEBOX]

## Dati e API {#data-and-apis}

+++ Gli oggetti [!DNL Recommendations] creati tramite l&#39;API vengono visualizzati nell&#39;interfaccia utente [!DNL Target]?

Sì. Gli oggetti (**[!UICONTROL Criteri]**, **[!UICONTROL Progettazioni]**, **[!UICONTROL Raccolte]** e **[!UICONTROL Esclusioni]**) di [!UICONTROL Recommendations] creati tramite l&#39;API sono disponibili nell&#39;interfaccia utente e possono essere modificati tramite l&#39;API o l&#39;interfaccia utente [!DNL Target].

+++

+++ Le offerte visive create nell&#39;interfaccia utente di [!DNL Target] possono essere gestite con le API di [!DNL Target]?

No. Impossibile gestire con le API [!DNL Target] le attività [!DNL Recommendations] con offerte visive create nell&#39;interfaccia utente [!DNL Target]. Queste attività vengono visualizzate nell&#39;elenco **[!UICONTROL Attività]**, ma non possono essere lette o aggiornate (con GET o PUT).

+++

+++ Qual è il limite di dimensione di una chiamata API per inserire o aggiornare prodotti? È possibile aggiornare 50.000 prodotti in una chiamata invece di un feed?

[!DNL Target] impone un limite per i post di 50 MB a livello di applicazione, ma solo quando viene passata l&#39;intestazione del tipo di contenuto `application/x-www-form-urlencoded`.

È possibile effettuare una singola chiamata con 50.000 prodotti. Se la chiamata non riesce, può essere divisa in batch. Adobe consiglia batch di 5.000 o 10.000 prodotti per ridurre la probabilità di un timeout dovuto al carico del sistema.

+++

+++ Qual è la dimensione massima di un file CSV per un caricamento del feed?

Non esiste alcun limite sul numero di righe o sulla dimensione del file per il caricamento di un file CSV di feed. Come best practice, Adobe consiglia di limitare il file CSV a 1 GB per evitare errori durante il caricamento. Un file che supera 1 GB può idealmente essere suddiviso in più file di feed.

Il numero massimo di colonne di attributi personalizzati è 100 e gli attributi personalizzati sono limitati a 4096 caratteri. Nella pagina Limitazioni di [[!DNL Target]  sono disponibili altri limiti per la lunghezza delle colonne richieste](/help/main/r-troubleshooting-target/target-limits.md).

+++

+++ Perché **[!UICONTROL Ricerca nel catalogo]** non mostra i risultati corretti durante la ricerca di un attributo personalizzato con un valore numerico?

Quando si esegue una ricerca nel catalogo per un attributo personalizzato con un valore numerico, l’attributo viene considerato come stringa anziché come valore numerico.

Al momento non è disponibile alcuna funzionalità che consenta ai clienti di modificare il tipo di un attributo. Per apportare una modifica, [apri un problema cliente](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) che fa riferimento agli attributi il cui tipo deve passare da stringa a numerico.

+++

## Aggiorna tempistica {#update-timing}

+++ Quanto tempo ci vuole affinché gli aggiornamenti degli articoli nel catalogo vengano rispecchiati sul sito?

L’arco temporale e i risultati variano a seconda di come vengono aggiornati gli elementi.

| Aggiorna | Consigli | Ricerca nel catalogo |
| --- | --- | --- |
| Attributi degli elementi aggiornati tramite una mbox o l’API | Entro 15 minuti | Dopo l’indice del catalogo (3-8 ore) |
| Attributi degli articoli aggiornati tramite un feed | Dopo l’acquisizione del feed (2-8 ore) | Dopo l’acquisizione dei feed (2-8 ore) e il successivo indice di catalogo (3-8 ore), entro 5-16 ore in totale |
| Elemento eliminato dal catalogo tramite l&#39;interfaccia utente o l&#39;API [!DNL Target] | Entro 15 minuti | Dopo l’indice del catalogo (3-8 ore) |
| Elemento aggiunto al catalogo tramite una mbox o l’API | Dopo la successiva esecuzione dell’algoritmo. Le esecuzioni degli algoritmi sono pianificate ogni 12 ore per gli algoritmi a 1-2 giorni e ogni 24 ore per gli algoritmi a 7+ giorni | Dopo l’indice del catalogo (3-8 ore) |
| Elemento aggiunto al catalogo tramite un feed | Dopo l’acquisizione dei feed (2-8 ore) e l’esecuzione degli algoritmi successivi, pianificati ogni 12 ore per gli algoritmi a 1-2 giorni e ogni 24 ore per gli algoritmi a 7+ giorni, entro un totale di 2-32 ore | Dopo l’acquisizione dei feed (2-8 ore) e l’indice del catalogo (3-8 ore), entro 5-16 ore in totale |

Finché gli aggiornamenti non saranno disponibili, verrà visualizzato il seguente contenuto:

* Per gli elementi aggiornati o eliminati, vengono visualizzati i consigli e gli attributi degli elementi esistenti.
* Per un elemento aggiunto, i consigli esistenti vengono visualizzati se l’elemento aggiunto non è una chiave richiesta. I consigli di backup vengono visualizzati se l’elemento aggiunto è una chiave richiesta.

Dopo l’importazione di un file di feed, o dopo aver ricevuto gli aggiornamenti delle entità tramite l’API o una mbox, le seguenti modifiche vengono riportate in meno di 60 minuti:

* Se un elemento è stato escluso in precedenza ma ora deve essere incluso, viene incluso nella successiva esecuzione dell’algoritmo (12-24 ore).

  Questa situazione si verifica perché [!DNL Target] applica le esclusioni sia online che offline. Quando un elemento viene escluso di recente, l’esclusione online viene applicata rapidamente. Quando un elemento viene incluso di recente, l’esclusione online viene applicata rapidamente, ma quella offline viene applicata solo alla successiva esecuzione dell’algoritmo.

* Se un elemento era incluso in precedenza ma ora deve essere escluso, l’elemento viene escluso in base alle righe temporali della tabella, a seconda della sorgente: 15 minuti tramite una mbox o l’API, oppure 12-24 ore tramite un feed.

Le seguenti modifiche vengono applicate solo dopo l’esecuzione dell’algoritmo successivo (entro 12-24 ore):

* Attributi degli articoli utilizzati nelle regole di raccolta dell’attività.
* Attributi degli articoli utilizzati in una promozione basata su un attributo o su una raccolta associata all’attività.
* La categoria dell&#39;articolo in cui l&#39;elemento viene visualizzato per una &quot;Categoria corrente&quot; o una &quot;Categoria preferita&quot; nell&#39;algoritmo **[!UICONTROL Più venduti]** o **[!UICONTROL Più visualizzati]**.
* La classificazione degli elementi consigliati, quando l’attributo modificato è un attributo personalizzato utilizzato come chiave personalizzata per un algoritmo.
* La classificazione degli articoli consigliati in base a uno o più attributi modificati, quando la logica dei consigli è &quot;Articoli con attributi simili&quot; o quando vengono utilizzati i fattori &quot;Somiglianza del contenuto&quot; o &quot;Ponderazione degli attributi&quot;.

>[!NOTE]
>
>Un file di feed viene considerato importato quando il suo stato cambia da “Importazione elementi” a “Preparazione aggiornamenti indice di ricerca”. Gli aggiornamenti possono richiedere più di 60 minuti per essere rispecchiati nell&#39;interfaccia utente di **[!UICONTROL Ricerca nel catalogo]**. **[!UICONTROL La ricerca nel catalogo]** è aggiornata quando lo stato del feed diventa &quot;Aggiornamenti completati&quot;. Anche se **[!UICONTROL Ricerca nel catalogo]** non è ancora aggiornato, gli aggiornamenti vengono rispecchiati nel sito entro i periodi di tempo elencati sopra. Nella pagina **[!UICONTROL Ricerca nel catalogo]** viene visualizzata l&#39;ora dell&#39;aggiornamento più recente dell&#39;indice **[!UICONTROL Ricerca nel catalogo]**.

+++

+++ Quanto tempo ci vuole affinché una modifica alla configurazione di un&#39;attività, un&#39;offerta, una promozione o impostazioni di criteri di [!UICONTROL Recommendations] venga riportata sul sito?

* Una modifica alle impostazioni di promozione può richiedere fino a cinque ore per essere visualizzata sul sito.
* Una modifica alle impostazioni di altri criteri potrebbe essere applicata solo alla successiva esecuzione dell’algoritmo:

  * Alcune impostazioni di criteri, ad esempio l’aggiunta di una regola di inclusione dinamica, vengono applicate immediatamente.
  * Non è possibile incorporare altre impostazioni di criteri, ad esempio la rimozione di una regola di inclusione dinamica o una modifica dell’intervallo di lookback fino alla successiva esecuzione dell’algoritmo.
  * Queste modifiche attivano l’esecuzione di un algoritmo che può richiedere fino a 24 ore. Anche gli algoritmi vengono eseguiti secondo una pianificazione, ogni 12-24 ore.

+++

+++ Quanto tempo ci vuole affinché il comportamento di un utente (ad esempio, clic sul prodotto A e acquisto del prodotto B) si rifletta nei consigli ricevuti dallo stesso utente?

* Il prodotto o il contenuto attualmente visualizzato o acquistato influisce sui consigli ricevuti dall&#39;utente sulla stessa visualizzazione di pagina o sulla richiesta di contenuto [!DNL Target].
* Con tale richiesta viene aggiornato il comportamento storico degli utenti, ad esempio &quot;ultimo prodotto visualizzato&quot;, &quot;prodotto più visualizzato&quot; e la cronologia generale di visualizzazione e acquisto. Influisce sui consigli che l’utente riceve alla visualizzazione della pagina o alla richiesta di contenuto successiva. Ad esempio, gli algoritmi **[!UICONTROL Articoli visualizzati di recente]** e **[!UICONTROL Consigliati per te]** vengono aggiornati con ogni visualizzazione di prodotto o acquisto e l&#39;aggiornamento si riflette nella successiva richiesta di contenuto.

+++

+++ Quanto tempo ci vuole affinché il comportamento di un utente si rifletta nei consigli ricevuti da altri utenti?

Il comportamento degli utenti in aggregato viene incorporato nell’elaborazione offline dell’algoritmo. Questa elaborazione viene eseguita con ogni esecuzione dell’algoritmo, ogni 12-24 ore.

+++

+++ I consigli basati sugli elementi visualizzati di recente persistono su più dispositivi per un singolo visitatore?

Quando un visitatore avvia una sessione, l’ID della sessione è associato a un singolo dispositivo perimetrale su cui viene memorizzata una cache di profilo temporanea. Le richieste successive dalla stessa sessione leggono questa cache del profilo, inclusi gli elementi visualizzati di recente.

Al termine della sessione (generalmente quando scade dopo 30 minuti di assenza di attività), lo stato della sessione, inclusi gli elementi visualizzati di recente, viene mantenuto in un archivio di profili più permanente nello stesso perimetro geografico. Le sessioni successive da diversi dispositivi possono quindi accedere a questi elementi visualizzati di recente, purché la nuova sessione sia collegata al profilo del cliente tramite lo stesso Marketing Cloud ID (MCID), Experience Cloud ID (ECID), CustomerID o `mbox3rdPartyId`.

Se un visitatore ha due sessioni attive contemporaneamente, gli elementi visualizzati di recente su un dispositivo non aggiornano quelli sull’altro dispositivo, a meno che i dispositivi non siano costretti a condividere lo stesso ID sessione. Esiste una potenziale soluzione alternativa, ma [!DNL Target] non supporta direttamente la condivisione di un ID sessione tra più dispositivi. Il cliente deve gestire questa condivisione ID.

Questo comportamento si verifica anche quando un visitatore è attivo su un dispositivo e diventa attivo sull’altro dispositivo pochi minuti dopo. La sessione del primo dispositivo non scade per 30 minuti e possono verificarsi fino a cinque minuti di ritardo prima che lo stato del profilo venga scritto nello stato permanente ed elaborato. Durante il test di questo comportamento, considera che la scadenza della sessione e la memorizzazione del profilo possono richiedere 35 minuti.

Se il visitatore non ha due sessioni attive contemporaneamente, gli elementi visualizzati di recente su un dispositivo aggiornano quelli sull’altro dispositivo, purché la sessione sia terminata. Durante il test di questo comportamento, considera che la scadenza della sessione possa richiedere 35 minuti.

+++

## Criteri, progettazioni e promozioni {#criteria-designs-promotions}

+++ Perché non tutti i criteri, inclusi i criteri personalizzati, sono disponibili per la selezione durante la creazione di un&#39;attività [!DNL Recommendations]?

I criteri disponibili dipendono dalla categoria corrente. Quando vengono create le offerte di consigli, il selettore di algoritmi visualizza i criteri in base all’ID di categoria. Se la posizione in cui vengono applicati i criteri non contiene l’ID di categoria, alcuni criteri non sono disponibili nel selettore dell’algoritmo. Se nella mbox è utilizzata una posizione in cui l’ID di categoria è presente, il selettore di criteri contiene tutti i criteri applicabili.

[!DNL Target] ha un&#39;impostazione [Filtra criteri incompatibili](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html?lang=it){target=_blank} che controlla il filtro intelligente del selettore dell&#39;algoritmo. Per accedere all&#39;impostazione **[!UICONTROL Filtra criteri incompatibili]**, fare clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Consigli]**.

![Pagina Impostazioni consigli con l&#39;opzione Filtra criteri incompatibili evidenziata](assets/recs_settings_filter.png)

* Se l&#39;impostazione **[!UICONTROL Filtra criteri incompatibili]** non è abilitata, [!DNL Target] non filtra gli algoritmi nel selettore degli algoritmi e vengono visualizzati tutti gli algoritmi.
* Se l&#39;impostazione è abilitata, in [!UICONTROL Attività del Compositore esperienza visivo], [!DNL Target] legge il codice entityId e l&#39;ID di categoria dalla posizione selezionata. Vengono quindi visualizzati gli algoritmi basati su `currentItem|currentCategory`, se i rispettivi valori sono presenti in tale posizione. Di conseguenza, solo gli algoritmi compatibili con la posizione selezionata vengono visualizzati nel selettore degli algoritmi per impostazione predefinita. Gli algoritmi non compatibili possono essere comunque visualizzati deselezionando la casella di controllo **[!UICONTROL Compatibile]** durante la selezione dei criteri.

  ![Schermata Seleziona criteri con la casella di controllo Compatibile evidenziata](assets/compatible_checkbox.png)

[!DNL Target] non visualizza la casella di controllo **[!UICONTROL Compatibile]** nei casi speciali seguenti:

* Sia l’entityId che l’ID di categoria sono presenti nella posizione, quindi non viene filtrato nulla.
* Viene utilizzata la versione 55 o precedente di [!DNL mbox.js].
* Nessuna chiamata mbox attivata dalla pagina (`!config.isAutoCreateGlobalMbox && !config.isRegionalMbox`).
* I parametri di [!DNL Target] non sono definiti.

>[!NOTE]
>
>L&#39;impostazione **[!UICONTROL Filtra criteri incompatibili]** si applica solo alle attività create nel [!UICONTROL Compositore esperienza visivo] (VEC). Questa impostazione non è applicabile alle attività create nel **[!UICONTROL Compositore esperienza basato su moduli]**, perché [!DNL Target] non ha un contesto di posizione.

+++

+++ Qual è la differenza tra ponderazione attributi generale e ponderazione attributi relativa alla somiglianza dei contenuti?

La ponderazione degli attributi esiste in due forme: &quot;ponderazione attributi standard&quot; e &quot;ponderazione attributi per somiglianza di contenuti&quot;.

* &quot;Ponderazione attributi standard&quot; si applica alla maggior parte dei tipi di criteri, non solo **[!UICONTROL Somiglianza contenuto]**. Questo tipo di ponderazione dà più peso a determinati valori di attributo. Nell’esempio seguente, i prodotti Nike ottengono un aumento dei consigli in uscita.

  ![Sezione Ponderazione attributi con attributo del brand impostato per iniziare con Nike e il cursore al 25%](assets/attribute_weighting_example.png)

* &quot;Ponderazione attributi per somiglianza contenuto&quot; si applica solo ai criteri **[!UICONTROL Somiglianza contenuto]**. Questo tipo di ponderazione è più dinamico e si basa sulla &quot;chiave consiglio&quot; corrente (l’elemento attualmente visualizzato). Nell’esempio seguente (brand x 16), un visitatore che visualizza le sneaker Nike è più propenso ad essere consigliato per altri prodotti Nike (non necessariamente solo per le sneaker) rispetto alle sneaker della concorrenza. Un visitatore che visualizza le sneaker Adidas è più propenso ad essere consigliato prodotti Adidas.

  ![Sezione Somiglianza dei contenuti con l&#39;attributo del brand e il cursore di ponderazione a 16x](assets/content_similarity_example.png)

+++

+++ È necessario specificare il nome mbox per creare [!DNL Recommendations] criteri, promozioni o regole di test di modelli?

Quando viene creata una regola di test di modelli, promozioni o criteri [!DNL Recommendations] in base a un parametro mbox, `mboxParameter` non richiede più di specificare `mboxName`. Il nome dell’elemento mbox è ora facoltativo. Questa modifica consente di utilizzare parametri da più mbox o un riferimento a un parametro che non è ancora stato registrato sul bordo.

Per selezionare il parametro desiderato, utilizzate uno dei seguenti metodi:

* Durante la creazione di un criterio, una promozione o una regola di test del modello, seleziona un nome di parametro dall’elenco. Inizia a digitare i primi caratteri del nome del parametro o il nome completo.
* Se il nome della mbox è noto ma il nome del parametro non lo è, utilizza la casella di controllo per filtrare una mbox nota che trasmette il parametro desiderato.

Con entrambi i metodi, non esiste alcun collegamento tra mbox e il parametro. Il criterio, la promozione o la regola di test del modello funzionano in base al parametro su tutte le mbox che trasmettono tale parametro.

Quando viene modificata una regola di test di criteri, promozioni o modelli esistente, il filtro mostra il nome mbox fornito durante la creazione.

+++

+++ Cosa si può fare quando i caratteri speciali interrompono un array?

Utilizza i valori di escape in JavaScript. Le virgolette (&quot;) possono interrompere l’array. Lo snippet di codice seguente è un esempio di valori di escape:

```
#set($String='') 
#set($escaper=$String.class.forName('org.apache.commons.lang.StringEscapeUtils')) 
<script type="text/javascript"> 
console.log("$escaper.escapeJavaScript($entity1.name)") 
console.log("$escaper.escapeJavaScript($entity2.name)") 
console.log('$escaper.escapeJavaScript($entity3.name)') 
names.push("$escaper.escapeJavaScript($entity4.name)") 
</script>
```

+++

+++ È possibile escludere un’entità in modo dinamico?

Sì. Gli ID entità per le entità da escludere dai consigli possono essere trasmessi nella stringa di query. Ad esempio, puoi escludere gli articoli già presenti nel carrello.

Per abilitare la funzionalità di esclusione, utilizzate il parametro mbox `excludedIds`. Questo parametro punta a un elenco di ID di entità separati da virgole, ad esempio `mboxCreate(..., "excludedIds=1,2,3,4,5")`. Il valore viene inviato quando vengono richiesti i consigli.

L&#39;esclusione viene eseguita solo per la chiamata [!DNL Target] corrente. Gli elementi non vengono esclusi nelle chiamate [!DNL Target] successive a meno che il valore `excludedIds` non venga nuovamente passato. Per escludere gli elementi nel carrello dai consigli su ogni pagina, continua a trasmettere il valore `excludedIds` su ogni pagina.

Per escludere `entityIds`, aggiungi il token `&excludes=${mbox.excludedIds}` all&#39;URL del contenuto dell&#39;offerta. Quando l’URL di contenuto viene estratto, i parametri richiesti vengono sostituiti con i parametri di richiesta mbox correnti.

Per impostazione predefinita, questa funzione è abilitata per i consigli appena creati. I consigli esistenti devono essere salvati per supportare le entità escluse in modo dinamico.

>[!NOTE]
>
>Se escludi troppe entità, i consigli si comportano come se non ci fossero abbastanza entità per compilare il modello di consigli.

+++

+++ Perché un&#39;attività [!DNL Recommendations] legacy non può essere salvata dopo la definizione di un nuovo pubblico?

Assicurati che il pubblico abbia un nome univoco. Se il pubblico ha lo stesso nome di un pubblico esistente, l&#39;attività legacy [!DNL Recommendations] (un&#39;attività [!DNL Recommendations] creata prima di ottobre 2016) non può essere salvata.

+++

+++ È possibile utilizzare in [!DNL Recommendations Premium] un algoritmo creato in [!DNL Adobe Recommendations Classic]?

Gli algoritmi creati in [!DNL Recommendations Classic] non sono supportati in [!DNL Recommendations Premium]. L&#39;algoritmo legacy potrebbe essere utilizzabile in [!DNL Target Premium], ma può creare problemi di sincronizzazione quando l&#39;attività viene disattivata o eliminata nell&#39;interfaccia utente di [!DNL Target Premium]. Per ulteriori informazioni sulle differenze tra le due soluzioni, vedi [[!DNL Recommendations Classic] rispetto a [!DNL Recommendations] attività in [!DNL Target Premium]](/help/main/c-recommendations/c-recommendations-faq/recommendations-classic-versus-recommendations-activities-target-premium.md).

+++

+++ Come possono essere consigliati solo i nuovi articoli o video?

I clienti dei settori media e pubblicazione spesso desiderano che gli elementi consigliati includano solo gli articoli o i video più recenti. Ad esempio, un cliente [!DNL Target] ha utilizzato il seguente approccio per consigliare articoli usciti da meno di 60 giorni:

1. La data di pubblicazione dell’articolo, in formato AAAAMMGG, viene passata come attributo di entità personalizzato. Ad esempio:

   | Attributo di entità | Esempio |
   | --- | --- |
   | issueDate | 2021218 |
   | lastViewDate | 2021701 |
   | parentCategory | commento |
   | publishDate | 20210113 |
   | publishDateDisplay | 13 gennaio 2021 |

1. Crea uno script di profilo che restituisce la data odierna meno 60 giorni, anche questa in formato AAAAMMGG.

   ![Script di profilo denominato priorDate60, descritto come la data odierna meno 60 giorni in formato AAAAMMGG, con lo script che calcola la data](/help/main/c-recommendations/c-recommendations-faq/assets/sample-profile-script.png)

1. Utilizzare una regola di inclusione dinamica nei criteri in modo che `publish date > today's date minus 60 days`.

   ![Sezione Regole di inclusione con una regola di corrispondenza attributo profilo che confronta publishDate con il valore memorizzato in user.priorDate60](/help/main/c-recommendations/c-recommendations-faq/assets/sample-inclusion-rule.png)

Questo esempio può essere eseguito anche con la corrispondenza dei parametri, passando il valore `priorDate60` come parametro mbox.

+++

## Risoluzione dei problemi relativi al {#troubleshooting}

+++ Perché talvolta [!DNL Target] non è in grado di mostrare i consigli?

[!DNL Target] a volte non può mostrare consigli a causa del basso numero di consigli disponibili.

Il numero di valori generati per ciascun criterio è tre volte il numero di entità specificato nel progetto. Il filtro runtime (ad esempio, corrispondenza di inventario o attributi mbox) viene applicato dopo la generazione dei valori 3x, pertanto al momento della consegna possono rimanere meno di 3x valori. Per limitare questa situazione, aumenta il numero di entità nel modello nascondendo altre entità.

Il seguente JavaScript può essere utilizzato all&#39;inizio del modello per aumentare il numero di entità richieste. In questo esempio, il numero di entità richieste è 30 (3x10).

```
#foreach($entity in $entities) 
 #if( $foreach.count > 10 ) 
  #break 
 #end 
 #set ($foo = $entity.id) 
#end 
```

+++

+++ Cosa significa la risposta NO_CONTENT talvolta restituita nella traccia di contenuto [!DNL Recommendations]?

NO_CONTENT viene restituito quando i consigli non sono disponibili per la combinazione di algoritmo e chiave richiesta. Questa situazione si verifica in genere quando i backup vengono disabilitati per l’algoritmo e si verifica anche una o più delle seguenti condizioni:

* I risultati non sono ancora pronti.

  Questa situazione si verifica in genere quando un’attività appena creata viene salvata per la prima volta o dopo che sono state apportate modifiche alla raccolta, ai criteri o alle promozioni utilizzate nell’attività.

* I risultati sono pronti, ma non ancora memorizzati nella cache del server perimetrale più vicino per la combinazione di algoritmo e chiave richiesta.

  La richiesta avvia un’operazione di caching, quindi questo problema viene risolto dopo alcuni ricaricamenti della pagina o dopo pochi minuti.

* I risultati sono pronti, ma non disponibili per il valore chiave fornito.

  Questa situazione si verifica in genere quando vengono richiesti consigli per un elemento aggiunto al catalogo dopo l’esecuzione dell’algoritmo più recente. Viene risolto dopo la successiva esecuzione dell’algoritmo.

* Il rendering parziale del modello è disabilitato e non sono disponibili risultati sufficienti per riempire il modello.

  Questa situazione si verifica in genere con una regola di inclusione dinamica che filtra in modo aggressivo molti elementi dai possibili risultati. Per evitare questa situazione, abilita i backup e non applicare la regola di inclusione ai backup, né utilizzare i criteri in sequenza con criteri filtrati in modo meno aggressivo.

+++

+++ Cosa fare quando una raccolta in [!DNL Recommendations] va a zero (0)?

Quando una raccolta che in precedenza non era uguale a zero va a zero, considera quanto segue:

* Salva nuovamente la raccolta e controlla se il numero viene aggiornato. Il nuovo salvataggio esegue nuovamente tutti gli algoritmi che utilizzano tale raccolta.
* Verifica che sia visualizzato l’ambiente corretto. Fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Consigli]**, quindi controlla l&#39;impostazione **[!UICONTROL Gruppo host predefinito]** nella sezione **[!UICONTROL Catalogo prodotti]**.

  ![Pagina Consigli della scheda Amministrazione con l&#39;elenco a discesa Gruppo host predefinito evidenziato nella sezione Catalogo prodotti](../assets/reco_faq_1.png)

* Verifica che l’indice sia aggiornato. Fai clic su **[!UICONTROL Consigli]** > **[!UICONTROL Ricerca nel catalogo]** e controlla da quante ore esiste l&#39;indice (ad esempio, &quot;indicizzato 3 ore fa&quot;). L’indice può essere aggiornato in base alle esigenze.
* Controlla se nel feed o nel livello dati è stato modificato qualcosa a causa del quale le entità non corrispondevano più alle regole di raccolta. Assicurati che le maiuscole e minuscole corrispondano (le regole distinguono tra maiuscole e minuscole).
* Verifica se il feed è stato eseguito correttamente o se qualcuno ha modificato la directory FTP, la password e così via.
* [!DNL Target] aggiorna la consegna (nella pagina del cliente o nell&#39;app) il più rapidamente possibile e deve anche fornire una rappresentazione nell&#39;interfaccia utente per l&#39;addetto marketing. [!DNL Target] non ritarda gli aggiornamenti di consegna per attendere la sincronizzazione con gli aggiornamenti dell’interfaccia utente. Utilizza [mboxTrace](/help/main/c-activities/c-troubleshooting-activities/content-trouble.md) per visualizzare cosa c&#39;è nel sistema quando arriva una richiesta.

+++

+++ Perché l&#39;azione **[!UICONTROL Scarica dati]** non riesce in un&#39;attività [!DNL Recommendations]?

Quando si fa clic su **[!UICONTROL Scarica dati]** nella pagina **[!UICONTROL Panoramica attività]** di un&#39;attività [!DNL Recommendations], l&#39;interfaccia utente [!DNL Target] potrebbe visualizzare l&#39;errore `Error while fetching recommendation data file.`

Questo errore si verifica in genere quando l’attività ha un set di risultati molto grande. Il CSV generato supera la dimensione di risposta che può essere restituita tramite l’interfaccia utente in un singolo download. I dati dei consigli stessi sono intatti. Solo il percorso di download nel browser non può fornire un file di tali dimensioni.

+++

## Problemi noti {#known-issues}

Di seguito sono riportati i problemi noti relativi alle attività [!UICONTROL Recommendations]:

* Quando [!DNL Target] restituisce un&#39;offerta JSON con `getOffer()`, restituisce un tipo di JSON. Una progettazione JSON [!DNL Recommendations] restituisce tuttavia un tipo di HTML.
* Le entità scadono correttamente una volta trascorsi 60 giorni senza ricevere aggiornamenti tramite un feed o l’API. Tuttavia, le entità scadute non vengono rimosse dall&#39;indice **[!UICONTROL Ricerca nel catalogo]** dopo la scadenza. Le entità eliminate tramite un feed o l&#39;API non vengono attualmente rimosse dall&#39;indice **[!UICONTROL Ricerca nel catalogo]**. (IRI-857)
* Le offerte [!DNL Recommendations] nelle attività A/B e Targeting esperienza non presentano un&#39;anteprima visiva della barra delle applicazioni [!DNL Recommendations]. (TGT-33426)
* Lo stato del feed dei criteri personalizzati visualizzato nell’elenco (scheda) dei criteri viene aggiornato ogni dieci minuti e in rare circostanze potrebbe non essere aggiornato oltre dieci minuti. Lo stato visualizzato nella vista di modifica dei criteri personalizzati viene recuperato in tempo reale ed è sempre aggiornato. (TGT-35896, TGT-36173)
