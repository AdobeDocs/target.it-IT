---
description: Introduzione alle attività di Target Recommendations che visualizzano automaticamente prodotti o contenuti che potrebbero interessare ai clienti in base all'attività utente precedente o ad altri algoritmi. I consigli aiutano a indirizzare i clienti verso elementi rilevanti di cui potrebbero non essere a conoscenza.
keywords: Consigli;
seo-description: Introduzione alle attività di Adobe Target Recommendations che visualizzano automaticamente prodotti o contenuti che potrebbero interessare ai clienti in base all'attività utente precedente o ad altri algoritmi. I consigli aiutano a indirizzare i clienti verso elementi rilevanti di cui potrebbero non essere a conoscenza.
seo-title: Introduzione alle attività di Recommendations in Adobe Target
solution: Target
title: Introduzione a Recommendations
title-outputclass: premium
topic: Premium
badge: premium
translation-type: tm+mt
source-git-commit: 04a4585e1d56f1754b65a248715fa5bdd4f8986f

---


# ![Introduzione a](/help/assets/premium.png) RECOMMENDATIONS

The text in this article comes from the *Introduction to Recommendations* webinar, which you can view in its entirety below.

The *Introduction to Recommendations* webinar includes an in-depth exploration of how to leverage the value of [!DNL Adobe Target Recommendations]. Scopri in che modo questa attività [!DNL Target] visualizza automaticamente prodotti o contenuti che potrebbero interessare ai clienti ottimizzando i suggerimenti in tempo reale basati sulle visite precedenti. Inoltre, immergiti nell’interfaccia utente [!DNL Target] per una panoramica dettagliata su come creare un’attività [!DNL Recommendations].

## Introduzione

Sappiamo tutti i tipi di raccomandazioni che vediamo nel settore retail. Sempre più spesso, i clienti si aspettano questi suggerimenti e li utilizzano come punto di partenza per esplorare altre opzioni disponibili. Se pensate al comportamento di shopping, questi tipi di raccomandazioni funzionano correttamente. Quasi tutti gli utenti hanno acquistato un prodotto che abbiamo visto prima in una raccomandazione, a prescindere dal fatto che sia in uno store o su una proprietà digitale.

L'illustrazione seguente mostra una raccomandazione che visualizza gli accessori acquistati comunemente con un telefono nuovo, inclusi stazioni di carico, casi e cuffie.

![Raccomandazione che mostrano gli accessori acquistati da altri con un telefono nuovo.](/help/c-recommendations/assets/intro-1.png)

Ma ciò che non si pensa sempre è il modo in cui i marchi digitali alzano la barra delle aspettative dei clienti. Sempre più, il modo in cui utilizziamo contenuti multimediali e contenuti è guidato da raccomandazioni personalizzate. Pensate alla prima cosa che vedi quando aprite Netflix, Spotify o YouTube. Questi marchi avviano la customer experience con le raccomandazioni. In un mondo in cui sono disponibili più alternative che mai, è importante identificare i contenuti più rilevanti per il cliente al momento dell'interazione.

![Consigli per mostrare i marchi digitali](/help/c-recommendations/assets/intro-2.png)

Marketers use [!DNL Adobe Target] to drive personalized experiences across a wide variety of industries, customer types, and channels.

[!DNL Adobe Target] distribuisce contenuti personalizzati ovunque.

![Illustrazione che mostra come Target distribuisce le raccomandazioni in vari luoghi](/help/c-recommendations/assets/intro-3.png)

* **Pubblicazione**: Gli editori Web usano [!DNL Target Recommendations] per raccomandare articoli ai visitatori del sito e incrementare il coinvolgimento.
* **Esercitazioni video**: [!DNL Adobe Creative Cloud] utilizza [!DNL Target] per raccomandare le esercitazioni video agli utenti Photoshop nell'applicazione Photoshop.
* **Gioco**: Le aziende di gaming usano [!DNL Target] per raccomandare giochi e contenuti agli utenti sulle loro console.
* **Vendite B 2 B**: L'azienda aziendale usa [!DNL Target] per raccomandare video, whitepaper e post di blog ai potenziali prospect B 2 B; distribuire download; e fornire aiuto ai clienti esistenti (https://theblog.adobe.com/testing-shifts-high-gear-intel).
* **Viaggi**: Un booker tedesco utilizza [!DNL Target] per raccomandare alberghi e molto altro ai viaggiatori (https://2017.summit.adobe.com/na/sessions/summit-online/online-2017/#17608).
* **Vendita al dettaglio**: Un rivenditore B 2 B leader utilizza [!DNL Target] per raccomandare categorie e prodotti principali per restituire visitatori nel browser e nell'app mobile (https://theblog.adobe.com/optimization-personalization-b2b-powerhouse-grainger/).

Questi sono solo alcuni dei modi in cui i clienti usano Target per distribuire raccomandazioni personalizzate.

Cosa fare per raccomandazioni fantastiche?

![Illustrazione che mostra i tre elementi che offrono raccomandazioni fantastiche](/help/c-recommendations/assets/intro-4.png)

Raccomandazioni fantastiche dovrebbero essere pertinenti e personalizzate. Ciò significa che hai bisogno di tre elementi per promuovere rilevanza e personalizzazione:

* **Controlli** per i marketer per stimolare la pertinenza degli elementi raccomandati. In qualità di esperto di marketing, date un contesto prezioso alla tabella e sapete quali attributi dei prodotti o dei contenuti sono rilevanti per un modello di Recommendations da considerare. Se si esegue un sito video, si sa che gli utenti potrebbero essere interessati a visualizzare i filmati dallo stesso regista, ma probabilmente non possono vedere i filmati generati dallo stesso studio. [!DNL Target] offre controlli che consentono di ottimizzare gli algoritmi con questa conoscenza del dominio.
* **Modelli sofisticati** per dare un'idea di milioni di elementi nel catalogo e negli eventi di interazione. [!DNL Target] offre sofisticate funzionalità di machine learning create su un decennio di esperienza e gestiamo miliardi di raccomandazioni all'anno.
* **Contesto utente** per assicurare che le raccomandazioni siano puntuali e rilevanti per gli utenti. Non vorrai raccomandare il video che qualcuno ha appena guardato o la camicia appena aggiunta al loro carrello. Il profilo utente avanzato di Target può essere utilizzato nelle raccomandazioni per garantire la personalizzazione.

## Implementazione delle raccomandazioni di Target

Inizia con una strategia.

![Illustrazione sulla strategia delle raccomandazioni](/help/c-recommendations/assets/intro-5.png)

* **Quali elementi si consiglia di raccomandare?** Innanzitutto, pensate agli elementi da raccomandare. Potrebbe trattarsi di prodotti, video o contenuti.
* **Dove si desidera visualizzare le raccomandazioni?** Quindi, pensate al punto in cui desiderate formulare le raccomandazioni. In generale, quali canali (Web, dispositivi mobili, in-store, chiocciola e così via). Quali parti del percorso del cliente conterranno le raccomandazioni? Quali pagine del sito conterranno le raccomandazioni?
* **Come determinerete se le raccomandazioni hanno esito positivo?** Supponete di disporre di un'esperienza senza raccomandazioni e di un'esperienza con raccomandazioni, oppure di avere due tipi diversi di raccomandazioni. Come determinare quale esperienza è stata un'esperienza migliore per i clienti? Alcune metriche potrebbero essere più difficili di quelle da misurare. Ad esempio, l'impatto delle raccomandazioni sul valore del ciclo di vita del cliente spesso è difficile da raggiungere. Pertanto, spesso è più facile arrivare a una metrica astratta e una più concreta, ad esempio, entrate per visita, valore medio dell'ordine o numero di clic. In alcuni casi, potrebbe essere necessario ridurre a icona una metrica, ad esempio il numero di chiamate di assistenza.

After you come up with your strategy, you are ready to start the implementation of [!DNL Target Recommendations].

Nella creazione dell'implementazione delle raccomandazioni sono disponibili tre passaggi generali:

![Illustrazione sulla procedura per creare l'implementazione delle raccomandazioni](/help/c-recommendations/assets/intro-6.png)

1. Teach [!DNL Target] about your context or products.
1. Acquisire il comportamento degli utenti.
1. Ottenere raccomandazioni nel contesto giusto.

### Teach [!DNL Target] about your context or products

When you start with [!DNL Recommendations], you pass information about every item you want to recommend. [!DNL Target] offre diverse opzioni di integrazione per creare il catalogo.

![Illustrazione che mostra come insegnare Target sul tuo contesto o prodotti](/help/c-recommendations/assets/intro-7.png)

Il metodo più semplice e più frequente consiste nell'inviare un file CSV a base giornaliera o settimanale dal sistema di gestione delle informazioni sui prodotti o dal sistema di gestione dei contenuti. But you can also pass information on the data layer from your page using the [!DNL Adobe Target] Javascript library, leverage our APIs to pass information directly from your source system, or use our [!DNL Adobe Analytics] integration if you are already passing catalog data to [!DNL Analytics].

A volte può essere utile utilizzare insieme più opzioni, ad esempio passando la maggior parte dei dati giornalieri tramite un file CSV e passando più frequentemente gli aggiornamenti di inventario tramite un'API.

In genere, il reparto IT sarà coinvolto nell'impostazione di questo passaggio.

A prescindere dal metodo scelto, è necessario includere metadati su ogni elemento in tre categorie:

![Illustrazione che mostra le informazioni sui metadati per il catalogo](/help/c-recommendations/assets/intro-8.png)

* Dati da visualizzare all'utente che riceve la raccomandazione. Ad esempio, il nome del filmato e un URL di immagine in miniatura.
* Dati utili per applicare controlli di marketing e merchandising. Ad esempio, la valutazione del filmato in modo che non si consigliino filmati NC -17.
* Dati utili per determinare la similarità degli elementi ad altri elementi. Ad esempio, il genere del filmato o gli attori presenti nel filmato.

### Acquisire il comportamento degli utenti

Next, you should add tags or leverage you existing [!DNL Analytics] implementation to track the conversion events (such as views and purchases) that drive [!DNL Target] algorithms.

![Illustrazione che mostra come acquisire il comportamento degli utenti](/help/c-recommendations/assets/intro-9.png)

You need to ensure that [!DNL Target] is aware of the items that your users are viewing and purchasing. Se l'acquisto non è pertinente al contesto, potrebbe essere utile tenere traccia di un diverso tipo di evento di conversione, ad esempio scaricare un PDF, completare un sondaggio, abbonarsi a una newsletter, guardare un video e così via.

If you are already using [!DNL Target] to run A/B Tests activities on your site, you might have already completed this step. Or if you are already using [!DNL Adobe Analytics] to report on site visits and conversion behavior, you can use [!DNL Analytics] as your behavioral datasource. If not, it’s easiest to set this up using a tag manager such as [Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md). It’s also possible to send offline or in-app interactions to [!DNL Target] via real-time API.

### Ottenere raccomandazioni con il contesto giusto

Pass information about the user and context at the point of interaction to [!DNL Target] to return relevant and personalized recommendations.

![Illustrazione che mostra come ottenere raccomandazioni nel contesto giusto](/help/c-recommendations/assets/intro-10.png)

Besides user behavior in aggregate, you need to pass [!DNL Target] the specific context where recommendations are being shown. Ciò include informazioni sulla pagina e informazioni sul profilo utente. [!DNL Target] utilizza queste informazioni per effettuare raccomandazioni personalizzate. Ad esempio, in un sito Web per la vendita al dettaglio, vuoi conoscere il prodotto e la categoria di prodotti attualmente visualizzati dal visitatore. Desiderate anche conoscere le informazioni sull'utente (marchio preferito, categoria di prodotti preferita, livello fedeltà e così via). This information is important so that [!DNL Target] can filter items and improve the personalization of recommendations.

## Creazione della prima attività di Recommendations

What is a [!DNL Recommendations] activity?

![Illustrazione che mostra le parti che fanno una buona attività di Recommendations](/help/c-recommendations/assets/intro-11.png)

A [!DNL Recommendations] activity is made up of the following components:

* **Pubblico**: Chi deve visualizzare queste raccomandazioni?
* **Criteri**: Quali elementi devono essere raccomandati?
* **Progettazione**: Come devono essere visualizzati gli elementi raccomandati?

![Illustrazione che mostra cosa compongono un'attività di Recommendations: Audience, Criteri e progettazioni](/help/c-recommendations/assets/intro-12.png)

Out of the box, [!DNL Target] includes 14 built-in audiences, 42 built-in criteria, and 10 built-in design templates. Potete personalizzare ciascuno di questi elementi o aggiungerne altri. We’ve had previous [webinars about building audiences](https://landing.adobe.com/acs/2018/na/adobe-target/registration.html) in [!DNL Target]. Questa sezione si concentra sulla definizione dei criteri, che definiscono gli elementi delle streghe.

In Target viene utilizzato il concetto della scheda dei criteri. Una scheda di criteri è come una ricetta per la personalizzazione.

![Illustrazione scheda Criteri](/help/c-recommendations/assets/intro-13.png)

È importante scegliere o creare i criteri giusti per ottenere i risultati di personalizzazione desiderati. Un criterio è simile a un funnel che porta dall'intero catalogo all'insieme finale di raccomandazioni.

![Illustrazione funnel](/help/c-recommendations/assets/intro-14.png)

The following sections describe the various parts of this funnel and how they work in [!DNL Target]:

### Filtri statici (raccolte ed esclusioni)

I filtri statici sono regole in generale applicabili agli attributi del catalogo che non si prevede di modificare frequentemente.

![Raccolte raccolte ed esclusioni](/help/c-recommendations/assets/intro-16.png)

Ad esempio, in un contesto di contenuto, potreste voler includere tutti i filmati nelle raccomandazioni, escludendo i filmati classificati NC -17. In un contesto retail, potete avere più marchi in diverse parti del mondo, ma consigliare solo i prodotti disponibili negli Stati Uniti. Potete anche escludere i prodotti da un'etichetta privata regionale.

Si tratta di attributi del catalogo che sono in genere applicabili in più raccomandazioni e che non si prevede possano modificare frequentemente.

### Algoritmo (chiave di raccomandazione e logica)

La fase successiva consiste nel scegliere una chiave e una logica di raccomandazione. Questo è il punto in cui decidete quale è la base della raccomandazione.

![Illustrazione dell'algoritmo](/help/c-recommendations/assets/intro-17.png)

La prima cosa da scegliere è la chiave di raccomandazione. La chiave di raccomandazione è ciò che state cercando per scegliere la raccomandazione. Si tratta di ciò su cui si basa la raccomandazione.

Potete basare la raccomandazione su:

* L'elemento attualmente visualizzato dal visitatore
* La categoria attualmente visualizzata dal visitatore
* L'elemento acquistato o aggiunto al carrello nel carrello
* Un attributo personalizzato relativo a un visitatore o a un elemento

In base a queste chiavi, scegliete la logica di raccomandazione:

* Articoli con attributi simili
* Elementi più visualizzati in una particolare categoria
* I clienti che hanno acquistato questo elemento hanno acquistato anche questi elementi
* Un attributo personalizzato

Out of the box, [!DNL Target] includes a portfolio of algorithms.

![Portfolio di illustrazioni degli algoritmi](/help/c-recommendations/assets/intro-15.png)

* **Gli algoritmi basati su popolarità** includono Most Viewed (Più visualizzato) e Top Sellers (Più venduti).
* **Gli algoritmi basati sul contenuto** includono la similarità dei contenuti.
* **Gli algoritmi di filtraggio collaborativo basati su elementi** includono Visualizzato/Visualizzato, Visualizzato/Acquistato ed Acquistato/Acquistato. «Acquistato» può essere qualsiasi conversione.
* **Gli algoritmi personalizzati** includono l'articolo visualizzato recentemente, Affinità di sito e filtro collaborativo migliorato per i profili.
* **Gli algoritmi di inserimento personalizzati** consentono di utilizzare algoritmi personalizzati.

### Regole aziendali online

L'ultimo passaggio consiste nell'applicazione di regole aziendali online. Questa è la posizione in cui abilitate gli algoritmi con conoscenza del dominio e contesto corrente in base a ciò che il visitatore sta realizzando sulla vostra proprietà digitale.

![Illustrazione sulle regole aziendali online](/help/c-recommendations/assets/intro-18.png)

Ad esempio, nel contesto del contenuto potete escludere i filmati che il visitatore ha precedentemente guardato, raccomandare i filmati in base allo stesso regista o incrementare i filmati nello stesso genere. Nel contesto della vendita al dettaglio, potete escludere prodotti fuori stock, mostrare elementi con un intervallo di $ 5 a $ 500, oppure incrementare gli elementi provenienti dallo stesso marchio.

## Demo

Una volta completate le attività illustrate nell'imbuto della raccomandazione descritto qui sopra, verrete lasciati con la raccomandazione finale. To watch an in-product demonstration inside [!DNL Target], the demo begins at 21:00 in the *Adobe Target Basics Webinar*, linked to below.

## Webinar di base su Adobe Target: Introduzione a Recommendations {#intro-to-recs}

[Introduzione a Recommendations](https://forums.adobe.com/external-link.jspa?url=https%3A%2F%2Fadobecustomersuccess.adobeconnect.com%2Fp8gt31drhs3e%2F%3FOWASP_CSRFTOKEN%3D4bd6cac5d0806167ee0a5449ba93d6300548d09c922bcb751c38973897a5703a)