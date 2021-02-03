---
keywords: Recommendations;intro;introduzione;webinar;demo
description: Introduzione alle attività Consigli di Adobe Target per visualizzare automaticamente prodotti o contenuti che potrebbero interessare i clienti in base alle loro attività precedenti o ad altri algoritmi. I consigli aiutano a indirizzare i clienti verso elementi rilevanti di cui potrebbero non essere a conoscenza.
title: Introduzione alle attività Recommendations
feature: Recommendations
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '2131'
ht-degree: 96%

---


# ![PREMIUM](/help/assets/premium.png) Introduzione alla funzione Consigli

Il testo di questo articolo proviene dal *webinar introduttivo alla funzione Consigli*, a cui puoi accedere qui sotto.

Il webinar *Introduzione alla funzione Consigli* include una descrizione approfondita di come sfruttare il valore di [!DNL Adobe Target Recommendations]. Scopri in che modo questa attività [!DNL Target] visualizza automaticamente prodotti o contenuti che potrebbero interessare ai clienti ottimizzando i suggerimenti in tempo reale basati sulle visite precedenti. Inoltre, immergiti nell’interfaccia utente [!DNL Target] per una panoramica dettagliata su come creare un’attività [!DNL Recommendations].

## Introduzione

Conosciamo tutti i tipi di consigli che vediamo nel settore retail. Sempre più spesso, i clienti si aspettano di ricevere questi consigli e li utilizzano come punto di partenza per scoprire altre possibilità. Se pensi al tuo comportamento di shopping, concorderai che in effetti funzionano. Ci è capitato praticamente a tutti di acquistare un prodotto che ci era stato consigliato da qualche parte, in un negozio fisico o una proprietà digitale.

L’illustrazione seguente mostra alcuni articoli consigliati: accessori acquistati spesso insieme a un telefono nuovo, come stazione di ricarica, custodie e cuffie.

![Prodotti consigliati, in base agli accessori che altri utenti hanno acquistato insieme a un telefono nuovo.](/help/c-recommendations/assets/intro-1.png)

Ma non ci soffermiamo spesso a pensare in che modo le realtà digital-first contribuiscono ad alzare le aspettative dei clienti. Il modo in cui usiamo contenuti e media è sempre più spesso guidato da suggerimenti e consigli personalizzati. Pensa alla prima cosa che vedi quando apri Netflix, Spotify o YouTube. L’esperienza dei clienti inizia sempre con una serie di articoli consigliati. In un mondo in cui sono disponibili più alternative che mai, è fondamentale riuscire a individuare i contenuti più rilevanti per il cliente al momento dell’interazione.

![Consigli proposti da brand digitali](/help/c-recommendations/assets/intro-2.png)

Gli addetti al marketing utilizzano [!DNL Adobe Target] per promuovere esperienze personalizzate per un’ampia gamma di settori, tipi di clienti e canali.

[!DNL Adobe Target] è in grado di fornire contenuti personalizzati ovunque.

![Illustrazione che mostra come Target distribuisce i consigli in vari luoghi](/help/c-recommendations/assets/intro-3.png)

* **Editoria**: gli editori web usano [!DNL Target Recommendations] per consigliare altri articoli ai visitatori del sito e incrementare il loro coinvolgimento.
* **Esercitazioni video**: [!DNL Adobe Creative Cloud] utilizza [!DNL Target] per consigliare specifiche esercitazioni video agli utenti di Photoshop, direttamente nell’applicazione Photoshop.
* **Giochi**: le aziende di gaming usano [!DNL Target] per consigliare giochi e contenuti pertinenti agli utenti sulle loro console.
* **Vendite B2B**: [le aziende business-to-business usano Target per consigliare video, white paper e articoli di blog ai potenziali clienti B2B; per fornire download; e per fornire assistenza ai clienti esistenti](https://theblog.adobe.com/testing-shifts-high-gear-intel).

* **Viaggi**:  [Una prenotazione di viaggio tedesca utilizza Target per consigliare alberghi e altro ai viaggiatori](https://2017.summit.adobe.com/na/sessions/summit-online/online-2017/#17608).

* **Retail**: [un grande rivenditore BB utilizza Target per consigliare categorie e prodotti di rilievo ai visitatori che ritornano sul suo sito sial dal browser che dalla sua app mobile](https://theblog.adobe.com/optimization-personalization-b2b-powerhouse-grainger/)2.

Questi sono solo alcuni esempi di come i nostri clienti usano Target per distribuire consigli personalizzati.

Come si possono proporre consigli efficaci?

![Illustrazione che mostra i tre elementi che contribuiscono a creare consigli efficaci](/help/c-recommendations/assets/intro-4.png)

Per essere efficaci, i consigli devono essere pertinenti e personalizzati. Per garantire rilevanza e personalizzazione servono tre ingredienti:

* **Controlli per gli addetti al marketing** che consentano di ottimizzare la pertinenza degli articoli consigliati. In qualità di addetto al marketing, conosci bene il contesto e sai quali attributi dei prodotti o contenuti devono essere considerati da un modello per la generazione di consigli. Se gestisci un sito di video, sai che gli utenti possono essere interessati a guardare altri filmati di uno stesso regista, ma non necessariamente altri film prodotti dallo stesso studio. [!DNL Target] ti offre i controlli necessari per ottimizzare gli algoritmi con la tua specifica conoscenza del dominio.
* **Modelli sofisticati** con cui ottenere informazioni importanti dai milioni di articoli presenti nel catalogo ed eventi di interazione. [!DNL Target] ha sofisticate funzionalità di apprendimento automatico che attingono a dieci anni di esperienza, e gestisce miliardi di consigli all’anno.
* **Contesto dell’utente** per assicurare che i consigli siano puntuali e rilevanti per i singoli utenti. Non vorrai consigliare un video a chi lo ha già visto, né la stessa camicia a un utente che l’ha appena messa nel carrello. Il profilo utente di Target è molto articolato e può essere utilizzato per generare consigli personalizzati.

## Implementazione dei consigli di Target

Inizia con una strategia.

![Illustrazione che mostra la strategia per i consigli](/help/c-recommendations/assets/intro-5.png)

* **Quali articoli vuoi consigliare?** Innanzitutto, pensa a quali articoli vorresti consigliare ai tuoi utenti. Potrebbe trattarsi di prodotti, video o contenuti.
* **Dove vuoi mostrare i consigli?** Quindi, pensa a dove dovranno essere visibili i consigli. In linea generale, su quali canali (web, dispositivi mobili, negozio, chiosco e così via). In quali aree del percorso del cliente verranno inseriti i consigli? Su quali pagine del sito?
* **Come determinare se i consigli sono efficaci?** Supponiamo di avere un’esperienza senza consigli e una con, oppure due tipi diversi di consigli. Come puoi determinare quale esperienza si è rivelata migliore per i clienti? Alcune metriche potrebbero essere più difficili di altre da misurare. Ad esempio, spesso è difficile risalire all’impatto dei consigli sul valore del ciclo di vita del cliente. Quindi è più facile ottenere una metrica meno astratta e più concreta, ad esempio ricavo per visita, valore medio dell’ordine o numero di clic. In alcuni casi, potresti essere interessato a ridurre una specifica metrica, ad esempio il numero di chiamate di assistenza.

Una volta definita la strategia, sei pronto per implementare [!DNL Target Recommendations].

L’implementazione della funzione di generazione dei consigli comporta tre passaggi generali:

![Illustrazione dei passaggi necessari per implementare i consigli](/help/c-recommendations/assets/intro-6.png)

1. Insegnare a [!DNL Target] come trattare contesto e prodotti.
1. Acquisire il comportamento degli utenti.
1. Inserire i consigli nel contesto giusto.

### Insegna a [!DNL Target] in cosa consistono contesto e prodotti

Quando inizi con [!DNL Recommendations], devi trasmettere informazioni su ogni elemento che vorrai poter consigliare. [!DNL Target] offre diverse opzioni di integrazione per creare il catalogo.

![Illustrazione che mostra come insegnare a Target in cosa consistono contesto e prodotti](/help/c-recommendations/assets/intro-7.png)

Il metodo più semplice e più frequentemente utilizzato consiste nell’inviare un file CSV su base giornaliera o settimanale dal sistema di gestione delle informazioni sui prodotti o dal sistema di gestione dei contenuti. Ma puoi anche trasmetterle sul livello dei dati dalla pagina stessa, utilizzando la libreria JavaScript di [!DNL Adobe Target]; oppure direttamente dal sistema di origine mediante le nostre API; o ancora puoi utilizzare la nostra integrazione [!DNL Adobe Analytics], se trasmetti già i dati del catalogo a [!DNL Analytics].

A volte può essere utile utilizzare insieme più opzioni: ad esempio puoi trasmettere la maggior parte dei dati giornalieri tramite un file CSV, e gli aggiornamenti di inventario a cadenza più frequente tramite un’API.

In genere il reparto IT sarà coinvolto nell’impostazione di questo passaggio.

A prescindere dal metodo scelto, è necessario includere metadati su ogni elemento in tre categorie:

![Illustrazione che mostra le informazioni sui metadati per il catalogo](/help/c-recommendations/assets/intro-8.png)

* Dati da presentare all’utente che riceve il consiglio. Ad esempio, il nome del film e un URL per l’immagine in miniatura.
* Dati utili per applicare controlli di marketing e merchandising. Ad esempio, la classificazione del film, se vuoi evitare di consigliare i film vietati ai minori di 18 anni.
* Dati utili per determinare la similarità tra diversi elementi. Ad esempio, il genere o gli attori del film.

### Acquisire il comportamento degli utenti

Successivamente, devi aggiungere dei tag o sfruttare l’implementazione esistente di [!DNL Analytics] per tenere traccia degli eventi di conversione (come visualizzazioni e acquisti) da utilizzare per li algoritmi di [!DNL Target].

![Illustrazione che mostra come acquisire il comportamento degli utenti](/help/c-recommendations/assets/intro-9.png)

È necessario assicurarsi che [!DNL Target] sia a conoscenza degli articoli che gli utenti visualizzano e acquistano. Se nel tuo contesto l’acquisto non è rilevante, potrebbe essere utile tenere traccia di un altro tipo di evento di conversione, ad esempio download di un PDF, completamento di un sondaggio, abbonamento a una newsletter, video guardato e così via.

Se utilizzi già [!DNL Target] per eseguire attività Test A/B sul tuo sito, potresti aver già completato questo passaggio. Oppure, se utilizzi già [!DNL Adobe Analytics] per generare rapporti sulle visite al sito e sul comportamento di conversione, puoi usare [!DNL Analytics] come origine dei dati comportamentali. In caso contrario, sarà più semplice impostare questo passaggio utilizzando un gestore tag, come [Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md). È anche possibile inviare interazioni offline o in-app a [!DNL Target] tramite API in tempo reale.

### Inserire i consigli nel contesto giusto

Se trasmetti informazioni sull’utente e il contesto al punto dell’interazione, [!DNL Target] sarà in grado di restituire consigli pertinenti e personalizzati.

![Illustrazione che mostra come ottenere consigli nel contesto giusto](/help/c-recommendations/assets/intro-10.png)

Oltre al comportamento dell’utente sotto forma di dati aggregati, è necessario trasmettere a [!DNL Target] il contesto specifico in cui vengono visualizzati i consigli. Questo include informazioni sulla pagina e sul profilo utente. [!DNL Target] utilizza queste informazioni per generare consigli personalizzati. Ad esempio, in un sito web per la vendita al dettaglio, è importante sapere quale prodotto e categoria di prodotti sta attualmente visualizzando il visitatore. Vorrai conoscere anche informazioni sull’utente (marchio preferito, categoria di prodotti preferita, livello fedeltà e così via). Tutte queste consentono a [!DNL Target] di filtrare gli articoli e migliorare la personalizzazione dei consigli.

## Crea la prima attività di Consigli

Cos’è un’attività di [!DNL Recommendations]?

![Illustrazione che mostra le parti che compongono una buona attività di Consigli](/help/c-recommendations/assets/intro-11.png)

Un’attività di [!DNL Recommendations] è composta dai seguenti elementi:

* **Pubblico**: chi potrà vedere i consigli?
* **Criteri**: quali articoli dovranno essere consigliati?
* **Progettazione**: come verranno presentati gli articoli consigliati?

![Illustrazione che mostra gli elementi che compongono un’attività di Consigli: pubblico, criteri e progettazioni](/help/c-recommendations/assets/intro-12.png)

Con [!DNL Target] sono già inclusi 14 tipi di pubblico, 42 criteri e 10 modelli di progettazione. Puoi personalizzare ciascuno di questi elementi o aggiungerne altri. In [sono stati già organizzati seminari Web sulla creazione di audience](https://landing.adobe.com/acs/2018/na/adobe-target/registration.html) in [!DNL Target]. Questa sezione tratta come definire i criteri, i quali a loro volta definiscono quali articoli verranno consigliati.

Target utilizza il concetto di scheda dei criteri. Una scheda di criteri è come una ricetta per la personalizzazione.

![Illustrazione della scheda Criteri](/help/c-recommendations/assets/intro-13.png)

Per ottenere i risultati di personalizzazione desiderati, è importante scegliere o creare i criteri giusti. Un criterio è simile a un funnel, o imbuto, che consente di passare dall’intero catalogo al set di consigli finale.

![Illustrazione di un funnel](/help/c-recommendations/assets/intro-14.png)

Le sezioni seguenti descrivono le varie parti di questo funnel e come funzionano in [!DNL Target]:

### Filtri statici (raccolte ed esclusioni)

I filtri statici sono regole generiche applicabili agli attributi del catalogo, che non saranno soggette a frequenti modifiche.

![Illustrazione di raccolte ed esclusioni](/help/c-recommendations/assets/intro-16.png)

Ad esempio, in un contesto di contenuti, potresti voler includere nei consigli tutti i film eccetto quelli vietati ai minori di 18 anni. In un contesto retail in cui gestisci più marchi, potresti voler consigliare solo i prodotti disponibili per una specifica area geografica. Potresti anche voler escludere i prodotti di un’etichetta locale privata.

Questi sono tutti attributi del catalogo applicabili in ambito generale che possono essere usati in più consigli e che non sono soggetti a modifiche frequenti.

### Algoritmo (chiave e logica per la generazione dei consigli)

La fase successiva consiste nel scegliere una chiave e una logica per la generazione dei consigli. In pratica, devi decidere su che base verranno proposti i consigli.

![Illustrazione dell’algoritmo](/help/c-recommendations/assets/intro-17.png)

Per prima cosa devi scegliere la chiave per i consigli. La chiave indica cosa vuoi consultare per scegliere un consiglio, su cosa si basa il consiglio.

Il consiglio potrebbe dipendere da:

* L’articolo attualmente visualizzato dal visitatore
* La categoria attualmente visualizzata dal visitatore
* L’ultimo articolo acquistato o aggiunto al carrello
* Un attributo personalizzato relativo a un visitatore o a un articolo

In base a queste chiavi, scegli quindi la logica per la generazione del consiglio:

* Articoli con attributi simili
* Articoli più visualizzati in una particolare categoria
* Chi ha comprato questo articolo ha acquistato anche questi
* Attributo personalizzato

Con [!DNL Target] viene fornito anche un portfolio di algoritmi.

![Illustrazione del portfolio di algoritmi](/help/c-recommendations/assets/intro-15.png)

* Gli **algoritmi basati sulla popolarità** includono Più visualizzato e Più venduti.
* Gli **algoritmi basati sul contenuto** includono Somiglianza del contenuto.
* Gli **algoritmi con filtro collaborativo basato sugli articoli** includono Visualizzato/Visualizzato, Visualizzato/Acquistato ed Acquistato/Acquistato. Tieni presente che “Acquistato” può essere una qualsiasi conversione.
* Gli **algoritmi personalizzati** includono Visualizzato di recente, Affinità sito e filtro collaborativo ottimizzato per il profilo.
* Gli **algoritmi propri** consentono di utilizzare propri algoritmi personalizzati.

### Regole di business online

L’ultimo passaggio consiste nell’applicare le regole di business online. In questa fase abiliti gli algoritmi con conoscenza del dominio e del contesto corrente in base all’interazione del visitatore sulla tua proprietà digitale.

![Illustrazione delle regole di business online](/help/c-recommendations/assets/intro-18.png)

Ad esempio, nel contesto dei contenuti, puoi escludere i film che il visitatore ha già guardato, consigliare altri film dello stesso regista o promuovere altri film dello stesso genere. In un contesto retail, puoi escludere ad esempio i prodotti che non sono a magazzino, mostrare solo quelli con prezzo compreso tra 5 e 500 euro, o promuovere quelli di uno stesso marchio.

## Demo

Una volta completate le attività illustrate qui sopra nel funnel per la generazione dei consigli, si passa alla fase di creazione finale. Per una dimostrazione all’interno di [!DNL Target], guarda la demo a partire dal minuto 21:00 nel *webinar sulle nozioni di base di Adobe Target*, dal collegamento che segue.

## Webinar sulle nozioni di base di Adobe Target: introduzione alla funzione consigli {#intro-to-recs}

[Introduzione alla funzione Consigli](https://forums.adobe.com/external-link.jspa?url=https%3A%2F%2Fadobecustomersuccess.adobeconnect.com%2Fp8gt31drhs3e%2F%3FOWASP_CSRFTOKEN%3D4bd6cac5d0806167ee0a5449ba93d6300548d09c922bcb751c38973897a5703a)