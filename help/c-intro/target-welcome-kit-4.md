---
keywords: kit di benvenuto;kit di benvenuto target;intro;introduzione;guida introduttiva
description: Leggi i suggerimenti del nostro gruppo di esperti sull’utilizzo di Adobe  [!DNL Target]  come parte delle tue attività di test e personalizzazione.
title: Dove posso trovare suggerimenti per l’utilizzo di Target?
feature: Panoramica
exl-id: 86437ad1-83ea-4670-b503-6c3c1fff0c16
source-git-commit: 4c696f55f56a116cff61c2c307f750e72cc0107c
workflow-type: tm+mt
source-wordcount: '2898'
ht-degree: 99%

---

# Capitolo 4: Suggerimenti per l’utilizzo di Target

In base al nostro lavoro con molti utenti [!DNL Target], abbiamo osservato come è possibile ottenere più valore dalla soluzione [!DNL Target]. Questi sono i numerosi suggerimenti che abbiamo incluso in questo capitolo. Anche se potresti non essere pronto a utilizzare tutte queste idee immediatamente, attendi a questo elenco. Più esperienza acquisisci con la soluzione e più il programma matura, più vedrai come questi suggerimenti possono aiutare a ottenere di più con [!DNL Target].

## Suggerimento 1: approfondisci la personalizzazione incrementando il profilo del visitatore con dati aggiuntivi.

Puoi personalizzare le esperienze con dati [!DNL Target] pronti all’uso. Ma personalizza ulteriormente aggiungendo i tuoi dati nel mix. Puoi migliorare il tuo profilo con dati storici da [!DNL Adobe Analytics] e dati in tempo reale da [!DNL Adobe Audience Manager]. Puoi anche utilizzare Attributi del cliente, una funzionalità all’interno del servizio core Persone in [!DNL Adobe Experience Cloud], per inserire facilmente i dati di gestione delle relazioni con i clienti, i dati dei partner di seconde parti e i dati acquistati di terze parti in [!DNL Target].

Ad esempio, puoi associare i dati di acquisto dal sistema del punto vendita a un profilo visitatore. Per farlo, crea un file CSV con fino a 200 variabili offline e caricalo direttamente in [!DNL Adobe Experience Cloud] tramite un caricamento di file, oppure usa l’FTP per ospitare e pianificare il tuo file in modo che venga aggiornato regolarmente. Una volta inseriti gli attributi del cliente in [!DNL Adobe Experience Cloud], puoi mapparli su soluzioni [!DNL Experience Cloud] come [!DNL Adobe Analytics] e [!DNL Target] dove saranno disponibili per l’analisi, il test e la personalizzazione.

Per istruzioni dettagliate, consulta [Attributi personalizzati](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/working-with-customer-attributes.html?lang=it).

**Buono a sapersi**: poiché [!DNL Target] è una piattaforma aperta e agnostica che funziona bene con tecnologie diverse, puoi aggiungere dati di gestione delle relazioni con i clienti o dati acquistati in modi diversi. Ciò significa che puoi scegliere un metodo che funzioni al meglio per la tua organizzazione.

Per ulteriori informazioni, consulta [Metodi per immettere i dati in Target](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md).

## Suggerimento 2: personalizza in modo più avanzato, combinando i tipi di pubblico di [!DNL Target] con altri tipi di pubblico di Adobe Experience Cloud.

La fusione dei tipi di pubblico che vivono in diverse soluzioni [!DNL Adobe Experience Cloud] può offrirti una comprensione molto più ampia dei tuoi clienti e la possibilità di personalizzare in modo più approfondito. Ad esempio, anche se [!DNL Target] fornisce dati sul pubblico in tempo reale, [!DNL Adobe Analytics] fornisce dati sullo storico del pubblico. Combinare questi due elementi può aiutarti a identificare quando il comportamento di un cliente è coerente e quando potrebbe esserci l’opportunità di agire su un nuovo comportamento. Fai clic sul menu a discesa accanto a “Tutti i visitatori” durante la creazione di un’attività. Quindi, seleziona le caselle di massimo venti tipi di pubblico, fai clic su “Combina più tipi di pubblico” e poi su “Salva”.

Per istruzioni dettagliate, consulta [Combinazione di più tipi di pubblico](/help/c-target/combining-multiple-audiences.md).

**Buono a sapersi**: [!DNL Adobe Audience Manager] i tipi di pubblico sono disponibili in [!DNL Target] automaticamente. Ma la condivisione del pubblico [!DNL Adobe Analytics] richiede una configurazione manuale. È sufficiente selezionare la casella con l’etichetta “Rendi questo un pubblico Experience Cloud” durante il processo di creazione del pubblico in [!DNL Analytics]. Quindi, da [!DNL Target], fai clic su “Importa tipi di pubblico di Experience Cloud”.

## Suggerimento 3: esporta dati da [!DNL Target] da utilizzare con strumenti di terze parti.

Con i token di risposta, gli amministratori possono estrarre facilmente i dati da [!DNL Target] e in strumenti di terze parti. Questa funzione può essere utile quando desideri aggiungere i dati ai dati raccolti in uno strumento di sondaggio. Ad esempio, se un sondaggio mostra un campione di una popolazione con un punteggio di esperienza pari a “9” e un’altra con un punteggio di esperienza pari a “4”, puoi utilizzare i tuoi dati per vedere chi ha visto l’esperienza A e chi ha visto l’esperienza B. Puoi inoltre utilizzare i token di risposta per esportare i dati [!DNL Target] nel data warehouse interno. Fai clic su “Amministrazione”, quindi attiva il pulsante accanto al token di risposta desiderato. Quindi, crea un’attività. I dati sono quindi pronti per essere trasferiti al fornitore di terze parti. Puoi verificare che [!DNL Target] stia esportando i dati utilizzando gli strumenti di debug.

Per istruzioni dettagliate, consulta [Token di risposta](/help/administrating-target/response-tokens.md).

**Suggerimento utile**: prima che un amministratore possa attivare un token di risposta associato a una terza parte, uno sviluppatore deve impostare una partnership con tale società di terze parti.

Per istruzioni dettagliate, consulta [Token di risposta](/help/administrating-target/response-tokens.md).

**Esegui prima questa operazione**: assicurati di utilizzare at.js versione 1.1 o successiva. Se utilizzi una versione precedente, visualizzerai i token di risposta, ma at.js non sarà in grado di utilizzarli.

## Suggerimento 4: crea tipi di pubblico da queste variabili chiave per aumentare il valore dell’attività.

Quando crei tipi di pubblico per il targeting o il test di promozioni e offerte, considera innanzitutto queste variabili:

* Comportamento. Modelli di visita del sito e modelli di acquisto
* Referrer. Siti e campagne di riferimento
* Temporale. Ore del giorno, giorni della settimana e fattori stagionali
* Non in linea. Visita e acquista modelli presso negozi fisici
* Ambiente. Paese di origine, sistema operativo, tipo di browser

## Suggerimento 5: dai agli utenti il livello di accesso di cui hanno bisogno per svolgere il loro lavoro.

Semplifica l’utilizzo dei dati dell’organizzazione mantenendo al contempo la sicurezza. [!DNL Target Premium] consente agli amministratori di controllare il livello di accesso assegnato ai diversi team interni ed esterni.

Per ulteriori informazioni, consulta [Autorizzazioni per gli utenti aziendali](/help/administrating-target/c-user-management/property-channel/property-channel.md).

**Suggerimento utile**: quando aggiungi degli utenti, se il nome di un membro del team non è stato aggiunto in precedenza all’organizzazione, ad esempio nel caso di un dipendente di un’agenzia di terze parti, l’immissione del proprio indirizzo e-mail e della relativa password attiverà un invito e-mail a partecipare all’area di lavoro di un team.

Utilizzare Target Standard? Puoi comunque [assegnare tre livelli di accesso](/help/administrating-target/c-user-management/c-user-management/user-management.md) agli utenti con ruoli di sola lettura, editor e approvatore!

## Suggerimento 6: scopri le prestazioni di un’offerta in un percorso del cliente effettuandone il test in ogni pagina del percorso.

Scopri le prestazioni di un’offerta, ad esempio la spedizione gratuita, durante un percorso di clienti che si svolge su più pagine del sito web.

Per istruzioni dettagliate, consulta [Attività multipagina](/help/c-experiences/c-visual-experience-composer/multipage-activity.md).

**Suggerimento utile**: la modifica dell’URL dopo aver specificato un intervallo di pagine reimposterà l’esperienza. Ciò significa che le varianti specificate non verranno più visualizzate. Se devi modificare l’URL, ricorda di ridefinire l’esperienza.

## Suggerimento 7: sottoponi a test un’offerta con tipi di pubblico diversi per scoprire se i tipi di pubblico hanno preferenze diverse.

Con le versioni Experience, puoi eseguire un test con varianti per un numero illimitato di tipi di pubblico. Ad esempio, puoi creare un banner pubblicitario che offre la spedizione gratuita, con immagini e variazioni di valuta per i clienti negli Stati Uniti, nel Regno Unito e negli Emirati Arabi Uniti, senza dover eseguire test per tre tipi di pubblico diversi.

Per istruzioni dettagliate, consulta [Più tipi di pubblico in un test A/B](/help/c-activities/t-test-ab/t-test-create-ab/target-experience-to-multiple-audiences.md) e [Versioni di Experience in Adobe Target](https://helpx.adobe.com/it/target/how-to/experience-versions.html?playlist=/ccx/v1/collection/product/target/seg-%20ment/business-practitioners/explevel/beginner-adls/applaunch/how-to-2/collection.ccx.js?ref=helpx.adobe.com).

## Suggerimento 8: risparmia tempo replicando esperienze di attività su pagine simili.

Crea una variante su una pagina web, ad esempio un nuovo colore del pulsante, e applicala automaticamente a tutte le pagine che condividono lo stesso modello. Puoi specificare le pagine o applicare le varianti a tutte le pagine simili all’interno del sito web.

Per istruzioni dettagliate, consulta [Includere la stessa esperienza su pagine simili](/help/c-experiences/c-visual-experience-composer/temtest.md).

## Suggerimento 9: riduci il disordine nella libreria tipi di pubblico creando tipi di pubblico occasionali.

Se esegui il targeting di un segmento per il quale sai che non verrà eseguito nuovamente il targeting, ad esempio, per i clienti interessati da un evento meteo imprevisto, la creazione di un pubblico per un utilizzo una tantum può aiutarti a svolgere il lavoro senza aggiungere confusione alla Libreria tipi di pubblico. In questo modo è più facile trovare tipi di pubblico da utilizzare più volte.

Per istruzioni dettagliate, consulta [Creare un pubblico per sola attività](/help/c-target/creating-activity-only-audience.md).

**Funzionalità altamente richiesta**: i nostri clienti ci hanno chiesto di poter evitare che i tipi di pubblico a uso singolo vengano salvati automaticamente nella Libreria tipi di pubblico. Ora non devono più eliminare manualmente i tipi di pubblico per mantenere organizzate le loro librerie.

## Suggerimento 10: esegui più velocemente test semplici non sottoponendoli al processo di controllo qualità standard.

Non c&#39;è niente di peggio che avere un’attività pronta e poi aspettare settimane per il completamento del processo di controllo qualità standard. Puoi eseguire il controllo qualità della maggior parte delle attività semplicemente inoltrando alcuni collegamenti sul controllo qualità ai colleghi per provarli su vari browser. È molto probabile che si desideri eseguire più test di controllo qualità per gli sforzi che modificano radicalmente la funzione del sito, ma in realtà, si dovrebbero avere meno di queste attività e molte più attività di base. L’aggiunta di migliori controlli sui diritti in modo che meno persone possano spingere le cose completamente in diretta aggiunge anche limiti significativi e consente di realizzare ciò di cui hai bisogno senza sacrificare velocità ed efficienza. Un’altra opzione è quella di disporre di una risorsa IT designata per fornire una supervisione tempestiva del processo di controllo qualità.

Per istruzioni dettagliate, consulta [Controllo qualità delle attività](/help/c-activities/c-activity-qa/activity-qa.md).

## Suggerimento 11: esegui test su pagine con traffico elevato in modo che raggiungano la rilevanza statistica più rapidamente.

Molti esperti di marketing lanciano programmi di ottimizzazione per la segmentazione del pubblico e il targeting senza verificare se i livelli di traffico e i tipi di pubblico rappresentati forniranno risultati significativi entro il periodo di tempo di test per i loro obiettivi di ottimizzazione e conversione. Per evitare questo errore comune, rispondi anticipatamente alle seguenti domande:

* Quanti visitatori univoci giornalieri ha la pagina?
* Qual è il tasso di conversione per la pagina?
* Per quanto tempo si prevede che sarà necessario eseguire il test prima di poterlo chiamare completo?

**Suggerimento utile**: utilizza il [calcolatore delle dimensioni del campione](https://experienceleague.adobe.com/tools/calculator/testcalculator.html) di Target per determinare le dimensioni del campione necessarie per il successo del test.

## Suggerimento 12: progetta test più semplici per assicurarti di poterli creare e implementare.

Dopo aver considerato tutti gli aspetti su come progettare un test, un piano può diventare molto complesso. In base a dove si trova la tua azienda con i test e alla capacità del gruppo di progettare, codificare, eseguire e analizzare i risultati, verifica se il test sembra troppo ambizioso. In caso affermativo, riducine la portata e la complessità. Meglio iniziare in piccolo che non eseguire affatto il test. Non puoi offrire un incremento di impatto se non avvii mai il test. È importante bilanciare le aspirazioni del team con le realtà delle risorse e delle capacità.

## Suggerimento 13: suddividi i test complessi in attività di test più piccole per renderli raggiungibili.

Invece di sviluppare un unico test di grandi dimensioni con variabili multiple e sviluppo complesso, sviluppa una serie meno complessa di test più piccoli con variabili minime. Ciò consente di comprendere meglio le prestazioni dei test in base a variabili specifiche. Riduce anche le possibili questioni tecniche che si presentano con lo sviluppo di progetti più ampi.

![Illustrazione della suddivisione di test complessi](/help/c-intro/assets/break-complex-tasks.png)

## Suggerimento 14: massimizza l’impatto del test effettuando test più vicini alla fine del funnel di conversione.

Il test eseguito vicino alla pagina in cui i visitatori fanno clic su Acquisto completo, Invia applicazione o dovunque si completi una conversione tende a fornire i risultati più incisivi. I visitatori che raggiungono la fine del funnel sono più qualificati, hanno investito più tempo e sono pronti per l’acquisto, pertanto testare le informazioni sulle loro preferenze e azioni può aiutarti a realizzare cambiamenti redditizi. Poiché le pagine del percorso di acquisto sono fondamentali per i tassi di conversione, i test condotti su tali pagine devono essere socializzati con le principali parti interessate prima di implementarli.

![Illustrazione del funnel di conversione](/help/c-intro/assets/conversion-funnel.png)

## Suggerimento 15: aggiorna costantemente i test per apportare miglioramenti iterativi.

Se la tua ipotesi non si è rivelata vera, pensa a come migliorare il tuo test. Ricorda che anche se nessuna delle esperienze testate ha avuto risultati migliori, l’esperimento non è stato una perdita di tempo. Un test di successo non implica sempre un aumento dei ricavi o delle conversioni. Se il test ha effettivamente sostenuto la tua ipotesi, allora sei sulla strada per sviluppare una teoria generale. Ma anche quando hai un chiaro risultato di vittoria, non fermarti lì. Troppo spesso, gli esperti di marketing commettono l’errore di testare una volta e poi di fare il punto su tali risultati senza capire realmente cosa ha portato al successo. Piuttosto, pianificare l’iterazione di quei risultati per capire perché il favorito era in testa. Questo ti porterà a informazioni più approfondite che puoi utilizzare nelle campagne future.

## Suggerimento 16: confronta test e attività di personalizzazione per idee per migliorare il targeting.

Confrontare le prestazioni di conversione di diversi tipi di pubblico all’interno di diversi test in posizioni diverse può aiutare a focalizzare l’attenzione e a perfezionare la strategia di ottimizzazione di un’azienda. Utilizza i confronti tra test per identificare quali tipi di pubblico sono più importanti da sottoporre a test, quali dovrebbero ricevere esperienze mirate e quali tipi di esperienze sono più propensi a suscitare una risposta.

Ad esempio, un cliente di servizi finanziari ha condotto una campagna promozionale per una carta di credito che coinvolgeva incentivi per eventi sportivi professionali. Mediante test multivariati fattoriali parziali delle pagine di destinazione, il cliente è stato in grado di bilanciare in modo ottimale la messaggistica sui benefici della carta di credito con incentivi sportivi per indirizzare tipi di pubblico distinti dalla sua base di clienti. Questo approccio ha permesso all’azienda di sfruttare e massimizzare la conversione durante una finestra sensibile al tempo che circonda un importante evento sportivo.

## Suggerimento 17: rendi i test utili avviandoli solo se sai di poter agire sui dati.

Un test è inutile se non hai chiaro come agire sui dati. Ciò include la conoscenza della metrica di successo chiave, ciò che deve accadere per spingere un vincitore, come seguirai i risultati dei test e cosa farai con le informazioni sul pubblico. Per un test rapido e di successo, è fondamentale che ogni gruppo coinvolto nel test (sviluppatori, creativi, specialisti di test e altri) sia consapevole del suo ruolo prima del lancio del test.

## Suggerimento 18: prima di lanciare un test, assicurati che l’azienda supporti la spinta del vincitore.

Le organizzazioni di ottimizzazione di successo credono nel concetto di test e comprendono che le loro opinioni professionali su quale esperienza vincerà il test non sempre si dimostrano vere. Esse determinano il vincitore in base a una solida base di dati e sono desiderose e disposte a trasmettere in diretta l’esperienza vincente dopo che i risultati sono stati raggiunti, anche se non è in linea con le loro aspettative o sembra illogico.

Ad esempio, un cliente dei servizi sanitari di Adobe ha recentemente dimostrato il valore dei test mostrando come un banner eroe che il team aveva considerato uno slam dunk ha avuto un impatto negativo sulla conversione. Se la tua organizzazione non ha ancora adottato completamente i test, è consigliabile eseguire prima test di ambito più semplici e più piccoli in modo che le modifiche dai risultati dei test possano essere apportate in modo incrementale.

## Suggerimento 19: comunica a tutti che hai avviato un test per evitare problemi quando il sito cambia.

Uno dei vantaggi della configurazione delle attività per l’utilizzo dei parametri di controllo qualità è la possibilità di condividere tali collegamenti con tutti gli utenti del team. Fai in modo che più persone siano consapevoli dell’attività e assicurati che non credano che il sito non funzioni correttamente quando raggiungono una variante di test.

Dopo aver completato i test, comunicare i lanci delle campagne, i risultati dei test e in particolare le lezioni apprese ti aiuta a sensibilizzare l’utente sui risultati dei test e a renderli più interessati. Condividere i risultati con tutti nell’organizzazione evita anche di ripetere un’ipotesi, educa tutti su ciò che funziona e li aiuta fondamentalmente a sfidare le proprie idee su ciò che funziona in base a ciò che hai trovato. È consigliabile preparare un modello da utilizzare ogni volta per condividere i risultati e gli insegnamenti chiave.
Quindi prendi in considerazione la creazione di un libro condivisibile o un deck Microsoft PowerPoint che acquisisce cumulativamente questi insegnamenti.

## Suggerimento 20: utilizza la funzionalità mobile per creare attività mobili più innovative.

Le esperienze degli utenti di tablet e smartphone devono concentrarsi sui controlli basati sul tocco come interazione principale del visitatore, anziché sui clic del mouse e sui controlli da tastiera. Sfrutta i controlli dello schermo mobile, tra cui scorrimento del dito, tocco, trascinamento, pizzico e zoom. Utilizza pulsanti semplici e di grandi dimensioni per designare interazioni e navigazione, ad esempio un grande carrello o un pulsante di riproduzione video. Per la progettazione per il retail mobile, incorpora una visualizzazione di prodotti avanzata ottimizzata per il tipo di dispositivo. Cerca sempre le opportunità per spostare il punto di interesse dell’esperienza di utilizzo su visualizzatori di grandi dimensioni incorporati o zoom e panoramica interattivi a schermo intero, rotazione a 360 gradi e funzionalità video migliorate.

## Suggerimento 21: aiuta i visitatori con dispositivi mobili a trovare ciò che desiderano ottimizzando la ricerca sul mobile.

Gli utenti di dispositivi mobili hanno un intento elevato. La maggior parte di loro utilizza la funzione di ricerca prima di fare qualsiasi altra cosa sui siti di m-commerce, rendendo cruciale l’ottimizzazione di tale funzione nei siti per dispositivi mobili. Per migliorare l’ottimizzazione SEO (Search Engine Optimization) per dispositivi mobili, utilizza espliciti suggerimenti di navigazione per una navigazione facile. Inoltre, implementa il suggerimento automatico e la correzione automatica nelle caselle di input di ricerca per risolvere la difficoltà di digitazione sui dispositivi mobili. Fornisci risultati di ricerca convincenti e pertinenti, ottimizzati per le dimensioni e la posizione dello schermo.

## Suggerimento 22: raggiungi meglio il pubblico di dispositivi mobili utilizzando il targeting in base all’ora del giorno per le campagne mobile SEM (Search Engine Marketing).

Scopri come e quando raggiungere il tuo pubblico e come gestire meglio la tua spesa pubblicitaria giornaliera suddividendo giorno per giorno le tue campagne sui dispositivi mobili in segmenti diversi della giornata.

Molti addetti al marketing commettono l’errore di non riuscire ad assegnare abbastanza budget per acquisire tale share of voice nelle ore in cui particolari dispositivi sono più utilizzati, lasciando così andare molti clienti potenziali e ricavi.

Ad esempio, l’utilizzo del tablet ha solitamente picchi nelle ore serali e molti utenti navigano mentre guardano la televisione. Al contrario, gli utenti di smartphone solitamente accedono al contenuto in movimento. I tempi di conversione dei picchi variano anche a seconda del settore, pertanto è importante capire quando è più probabile che i clienti univoci agiscano.

## Nota bene

Considera le seguenti idee prima di passare al prossimo capitolo: “Ispirazione per attività di test e personalizzazione”.

### Quando crei i test, non decorare, sii intenzionale.

* Controlla il flusso con i percorsi oculari intenzionali incentrati sui punti di conversione.
* Assicurati di utilizzare il tuo immobile a tuo vantaggio.
* Sfrutta Image focus per garantire che le immagini non siano decorazioni, ma funzionino per te.
* Riduci l’ingombro, l’attrito e la sfocatura con una copia semplificata.
* Assicurati di disporre di chiamate efficaci alle azioni quando hai bisogno che l’utente agisca.
* Se possibile, aggiungi credibilità tramite i contenuti generati dagli utenti.

### Semplifica il tuo sito web.

* Non fare leggere ai clienti. Non lo faranno.
* Facile da scansionare.
* Utilizza blocchi di copia puntati.
* Assicurati che la tua copia segua un processo di pensiero chiaro e sequenziale.

### Utilizzare i CTA (Call to Actions) efficaci

* Mettiti nei panni del cliente.
* Utilizza un linguaggio orientato alle azioni.
* Considera la motivazione della conversione.
* Risolvi il risultato della conversione.
* Assicurati che i CTA siano visti.
