---
keywords: Recommendations;consigli;intro;introduzione;webinar;demo
description: Scopri le attività Consigli in Adobe [!DNL Target] che consentono di visualizzare automaticamente contenuti che potrebbero interessare ai clienti in base alle loro attività precedenti o ad altri algoritmi.
title: Quali sono le attività Consigli?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: bc4d9a46-ea21-4687-b8a0-7f2e1dc33ebf
TQID: 'https://experienceleague.adobe.com/6jmXI9CsdCnyyQrQXKzq5WF8OQPQSCbE2Zb8AnpUvks'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
source-git-commit: 4f38c80880eedd9b966cdb2f178f408bb529b60c
workflow-type: tm+mt
source-wordcount: '1633'
ht-degree: 9%
---
# Introduzione alla funzione Consigli {#introduction-to-recommendations}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come le attività di [!DNL Recommendations] in [!DNL Adobe Target] visualizzano prodotti o contenuti rilevanti per i visitatori e come pianificare e creare un&#39;implementazione e un&#39;attività di [!DNL Recommendations].

>[!ENDSHADEBOX]

Questa pagina è basata sul webinar *Introduzione alla funzione Consigli*. Un&#39;attività [!DNL Recommendations] visualizza automaticamente prodotti o contenuti che potrebbero interessare i clienti ottimizzando i suggerimenti in tempo reale basati sulle visite precedenti. Nella pagina viene inoltre descritto come creare un&#39;attività [!DNL Recommendations] nell&#39;interfaccia utente [!DNL Target].

## Introduzione

I clienti si aspettano sempre più consigli e li utilizzano come punto di partenza per esplorare altre opzioni disponibili. Quasi tutti hanno acquistato un prodotto che hanno visto per la prima volta in un consiglio, sia in un negozio che su una proprietà digitale.

![Suggerimento che mostra gli accessori comunemente acquistati con un telefono nuovo, incluse le stazioni di ricarica, le custodie e le cuffie.](/help/main/c-recommendations/assets/intro-1.png)

Il modo in cui le persone utilizzano media e contenuti è sempre più guidato da consigli personalizzati, e i brand digitali come Netflix, Spotify e YouTube iniziano l’esperienza del cliente con i consigli. Poiché sono disponibili più alternative che mai, è fondamentale identificare i contenuti più rilevanti per un cliente al momento dell’interazione.

Gli addetti al marketing utilizzano [!DNL Adobe Target] per promuovere esperienze personalizzate per un’ampia gamma di settori, tipi di clienti e canali. Nella tabella seguente sono elencati alcuni esempi di utilizzo di [!DNL Target] da parte dei clienti per la distribuzione di consigli personalizzati.

| Caso d’uso | Esempio |
|---|---|
| Pubblicazione | Gli editori Web utilizzano [!DNL Target Recommendations] per consigliare articoli ai visitatori del sito e aumentare il coinvolgimento. |
| Tutorial video | [!DNL Adobe Creative Cloud] utilizza [!DNL Target] per consigliare esercitazioni video agli utenti di Photoshop nell&#39;applicazione Photoshop. |
| Giochi | Le aziende di gaming usano [!DNL Target] per consigliare giochi e contenuti agli utenti sulle loro console. |
| Vendite B2B | Le aziende business-to-business utilizzano [!DNL Target] per consigliare video, white paper e articoli di blog ai potenziali clienti B2B, per fornire download e assistenza ai clienti esistenti. |
| Viaggi | Un sistema di prenotazione viaggi tedesco utilizza [!DNL Target] per consigliare hotel e altri servizi ai viaggiatori. Per informazioni dettagliate, vedere [Sessione Adobe Summit](https://2017.summit.adobe.com/na/sessions/summit-online/online-2017/#17608){target=_blank}. |
| Vendita al dettaglio | Un retailer B2B leader utilizza [!DNL Target] per consigliare categorie e prodotti di rilievo ai visitatori che ritornano sul suo sito nel browser e nella sua app mobile. |

## Elementi di raccomandazioni importanti

I consigli più efficaci sono pertinenti e personalizzati. Tre elementi determinano rilevanza e personalizzazione:

* **Controlli addetti al marketing** per determinare la rilevanza degli elementi consigliati. Gli addetti al marketing sanno quali attributi dei loro prodotti o contenuti un modello di consigli deve considerare. Ad esempio, in un sito di video, gli utenti potrebbero essere interessati ai film dello stesso regista, ma probabilmente non ai film dello stesso studio. [!DNL Target] fornisce controlli per migliorare gli algoritmi con questa conoscenza del dominio.
* **Modelli sofisticati** per ottenere informazioni su milioni di elementi del catalogo ed eventi di interazione. [!DNL Target] dispone di funzionalità di apprendimento automatico che includono oltre dieci anni di esperienza e gestisce miliardi di consigli all&#39;anno.
* **Contesto utente** per garantire che i consigli siano puntuali e pertinenti. Ad esempio, i consigli non devono includere il video appena guardato o la camicia appena aggiunta al carrello. Il profilo utente [!DNL Target] può essere utilizzato nei consigli per garantire la personalizzazione.

## Implementare le attività Consigli di [!DNL Target]

Inizia con una strategia che definisce i seguenti punti:

* **Elementi da consigliare**: prodotti, video o contenuti.
* **Posizioni per i consigli**: i canali (web, mobile, in-store, chiosco e così via), le parti del percorso clienti e le pagine del sito che contengono consigli.
* **Misurazione del successo**: come determinare se i consigli sono efficaci, ad esempio, confrontando un&#39;esperienza senza consigli con un&#39;esperienza con consigli o confrontando due diversi tipi di consigli. Alcune metriche, come l’impatto sul valore del ciclo di vita del cliente, sono difficili da misurare direttamente, pertanto una metrica più concreta è spesso più facile da utilizzare, come ricavi per visita, valore medio dell’ordine o numero di clic. In alcuni casi, l’obiettivo è quello di ridurre al minimo una metrica, ad esempio il numero di chiamate di supporto.

Dopo aver definito la strategia, l&#39;implementazione di [!DNL Target Recommendations] prevede tre passaggi generali:

![Illustrazione che mostra i tre passaggi di un&#39;implementazione dei consigli: insegnare a Target i contenuti o i prodotti, acquisire il comportamento degli utenti e ottenere i consigli nel contesto giusto.](assets/intro-6.png)

### Insegna a [!DNL Target] i tuoi contenuti o prodotti

Quando si inizia con [!DNL Recommendations], si trasmettono informazioni su ogni elemento che si desidera consigliare.

![Illustrazione che mostra come insegnare a Target i tuoi contenuti o prodotti: feed in formato CSV o Feed di Google, il livello dati con Target, l&#39;API e l&#39;integrazione di Analytics.](assets/intro-7.png)

Il metodo più semplice e più frequentemente utilizzato consiste nell’inviare un file CSV su base giornaliera o settimanale da un sistema di gestione delle informazioni sui prodotti o da un sistema di gestione dei contenuti. Altre opzioni consentono di passare informazioni sul livello dati dalla pagina utilizzando la libreria JavaScript [!DNL Adobe Target], di utilizzare le API per passare informazioni direttamente dal sistema di origine o di utilizzare l&#39;integrazione [!DNL Adobe Analytics] se si stanno già passando dati catalogo a [!DNL Analytics]. Puoi utilizzare insieme più opzioni, ad esempio trasmettere la maggior parte dei dati ogni giorno tramite un file CSV e gli aggiornamenti dell’inventario più frequentemente tramite un’API. Il reparto IT è solitamente coinvolto nella configurazione di questa fase.

Indipendentemente dal metodo scelto, includi metadati su ogni elemento in tre categorie:

* **Dati che si desidera visualizzare all&#39;utente che riceve il consiglio.** Ad esempio, il nome del film e un URL per l’immagine in miniatura.
* **Dati utili per applicare controlli di marketing e merchandising.** Ad esempio, la classificazione del film, se vuoi evitare di consigliare i film vietati ai minori di 18 anni.
* **Dati utili per determinare la somiglianza di elementi con altri elementi.** Ad esempio, il genere o gli attori del film.

### Acquisire il comportamento degli utenti

![Illustrazione che mostra come acquisire il comportamento degli utenti: le visualizzazioni e i clic portano ad acquisti, conversioni, download, abbonamenti e riproduzioni, tracciati con Target, Analytics o l&#39;API.](assets/intro-9.png)

Aggiungi i tag o utilizza l&#39;implementazione [!DNL Analytics] esistente in modo che [!DNL Target] sia a conoscenza degli elementi visualizzati e acquistati dagli utenti. Se l’acquisto non è pertinente al tuo contesto, tieni traccia di un altro tipo di evento di conversione, ad esempio il download di un PDF, il completamento di un sondaggio, l’abbonamento a una newsletter o la visione di un video.

Se utilizzi già [!DNL Target] per eseguire attività Test A/B sul tuo sito, potresti aver già completato questo passaggio. Se utilizzi già [!DNL Adobe Analytics] per generare rapporti sulle visite al sito e sul comportamento di conversione, puoi utilizzare [!DNL Analytics] come origine dei dati comportamentali. In caso contrario, l&#39;opzione più semplice consiste nell&#39;impostare questa impostazione con un gestore di tag, ad esempio i tag in [[!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-using-adobe-launch.html?lang=it){target=_blank}. È inoltre possibile inviare a [!DNL Target] interazioni offline o in-app tramite l&#39;API in tempo reale.

### Inserire i consigli nel contesto giusto

![Illustrazione che mostra come ottenere consigli nel contesto giusto: il prodotto corrente visualizzato, la categoria di prodotto corrente, la categoria preferita dall&#39;utente, il marchio preferito dall&#39;utente e il livello di fedeltà dell&#39;utente vengono passati a Target.](assets/intro-10.png)

Oltre al comportamento dell&#39;utente sotto forma di dati aggregati, [!DNL Target] ha bisogno del contesto specifico in cui vengono visualizzati i consigli, che include informazioni sulla pagina e sul profilo utente. [!DNL Target] utilizza queste informazioni per filtrare gli elementi e migliorare la personalizzazione dei consigli.

## Creare la prima attività Consigli

Un&#39;attività [!DNL Recommendations] combina un pubblico, criteri e una progettazione. [!DNL Target] include 14 tipi di pubblico incorporati, 42 criteri incorporati e 10 modelli di progettazione incorporati. Puoi personalizzare ciascuno di questi elementi o aggiungerne di nuovi.

![Illustrazione che mostra le parti che compongono una buona attività di Consigli: il pubblico (chi dovrebbe vedere i Consigli), i criteri (quali elementi dovrebbero essere consigliati) e la struttura (come vengono visualizzati gli elementi consigliati).](assets/intro-11.png)

[!DNL Target] utilizza il concetto di scheda dei criteri, che è come una ricetta per la personalizzazione. La scelta o la creazione dei criteri giusti è importante per ottenere i risultati di personalizzazione desiderati. Una scheda di criteri funziona come un funnel che ti porta dall’intero catalogo al set finale di consigli.

![Illustrazione dei criteri funnel: contenuto del catalogo, filtri statici (raccolte ed esclusioni), algoritmo (chiave e logica per i consigli), regole di business online (filtro dinamico e ponderazione degli attributi) e consigli finali, accanto a una scheda dei criteri di esempio.](assets/intro-14.png)

Le sezioni seguenti descrivono le parti di questo funnel e come funzionano in [!DNL Target].

### Filtri statici (raccolte ed esclusioni)

I filtri statici sono regole applicabili in generale agli attributi del catalogo e non dovrebbero essere soggetti a modifiche frequenti, per cui puoi utilizzarli in più consigli.

![Illustrazione di filtri statici. Contenuto: includi tutti i film ed escludi i film classificati NC-17 dai consigli. Prodotti: include tutti i prodotti disponibili negli Stati Uniti ed esclude i prodotti da un&#39;etichetta privata regionale.](assets/intro-16.png)

### Algoritmo (chiave e logica per la generazione dei consigli)

Il passaggio successivo consiste nel scegliere una chiave e una logica per la generazione dei consigli, che sono la base per la generazione dei consigli. La chiave indica cosa vuoi consultare per scegliere un consiglio,

![Illustrazione del passaggio dell&#39;algoritmo. Chiave consiglio: articolo attualmente visualizzato, categoria attualmente visualizzata, ultimo articolo acquistato o attributo personalizzato. Logica per i consigli: articoli con attributi simili, articoli più visualizzati nella categoria, clienti che hanno acquistato questo articolo hanno acquistato anche questi articoli o algoritmo personalizzato.](assets/intro-17.png)

[!DNL Target] include un portfolio di algoritmi.

![Illustrazione del portfolio di algoritmi: basati sulla popolarità (Più visualizzati, Più venduti), basati sui contenuti (Somiglianza contenuti), filtraggio collaborativo basato sugli elementi (Visualizzato/Visualizzato, Visualizzato/Acquistato, Acquistato/Acquistato, dove Acquistato può essere qualsiasi conversione), personalizzati (Visualizzato di recente, Affinità sito, Collab avanzato profilo. Filtro) e creare un proprio (algoritmi personalizzati).](assets/intro-15.png)

### Regole di business online

L’ultimo passaggio consiste nell’applicare regole di business online, che migliorano gli algoritmi con la conoscenza del dominio e il contesto corrente, in base a ciò che il visitatore sta facendo sulla proprietà digitale.

![Illustrazione delle regole di business online. Contenuto: escludi i film già guardati, mostra film dello stesso regista e migliora i film dello stesso genere. Prodotti: escludi i prodotti esauriti, mostra gli articoli con un prezzo da $ 5 a $ 500 e incrementa quelli dello stesso marchio.](/help/main/c-recommendations/assets/intro-18.png)
