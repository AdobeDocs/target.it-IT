---
keywords: welcome kit;target welcome kit;intro;introduction;getting started
description: Kit di benvenuto  Adobe Target - Capitolo 4 - Suggerimenti per l'utilizzo di Target
title: Kit di benvenuto  Adobe Target - Capitolo 4 - Suggerimenti per l'utilizzo di Target
feature: intro
translation-type: tm+mt
source-git-commit: a05d2a28b7bea3aa559cd0174930af10c6d94134
workflow-type: tm+mt
source-wordcount: '2880'
ht-degree: 0%

---


# Capitolo 4: Suggerimenti per l&#39;utilizzo di Target

Sulla base del nostro lavoro con molti [!DNL Target] utenti, abbiamo osservato come sia possibile ottenere più valore dalla soluzione [!DNL Target]. Questi sono stati riassunti nei numerosi suggerimenti che abbiamo incluso in questo capitolo. Anche se potreste non essere pronti a usare tutte queste idee immediatamente, tenete su questo elenco. Più esperienza si ottiene con la soluzione e più il programma matura, più si vedrà come questi suggerimenti possono aiutare a ottenere di più con [!DNL Target].

## Suggerimento 1: Approfondisci la personalizzazione aumentando il profilo del visitatore con dati aggiuntivi.

Puoi personalizzare le esperienze con i dati [!DNL Target] immediatamente disponibili. Ma personalizza più profondamente aggiungendo i tuoi dati al mix. Puoi aumentare il tuo profilo con dati storici da [!DNL Adobe Analytics] e dati in tempo reale da [!DNL Adobe Audience Manager]. È inoltre possibile utilizzare Attributi del cliente, una funzionalità all&#39;interno del servizio di base Persone in [!DNL Adobe Experience Cloud], per trasferire facilmente dati CRM, dati di partner di seconda parte e dati acquistati di terze parti in [!DNL Target].

Ad esempio, puoi associare i dati di acquisto dal tuo sistema di punti vendita a un profilo visitatore. Per farlo, basta creare un file CSV con fino a 200 variabili offline, e caricarlo direttamente in [!DNL Adobe Experience Cloud] tramite un caricamento di file, oppure utilizzare l&#39;FTP per ospitare e pianificare il file da aggiornare regolarmente. Una volta che gli attributi cliente sono in [!DNL Adobe Experience Cloud], puoi mapparli su soluzioni [!DNL Experience Cloud] come [!DNL Adobe Analytics] e [!DNL Target] dove saranno disponibili per analisi, test e personalizzazione.

Per istruzioni dettagliate, vedere [Attributi personalizzati](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/working-with-customer-attributes.html).

**Buono a conoscere**: Poiché  [!DNL Target] è una piattaforma aperta e agnostica che funziona bene con tecnologie diverse, puoi aggiungere dati CRM o acquistati in molti modi diversi. Ciò significa che potete scegliere un metodo che funzioni meglio per la vostra organizzazione.

Per ulteriori informazioni, vedere [Metodi per inserire dati in Target](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md).

## Suggerimento 2: Personalizza in modo più approfondito combinando i tipi di pubblico Target con altri tipi di pubblico Adobe Experience Cloud.

La combinazione di tipi di pubblico che vivono in diverse soluzioni [!DNL Adobe Experience Cloud] può fornire una conoscenza molto più ampia dei clienti, nonché la possibilità di personalizzare in modo più approfondito. Ad esempio, sebbene [!DNL Target] fornisca dati sul pubblico in tempo reale, [!DNL Adobe Analytics] fornisca dati sul pubblico storico. Combinando questi due elementi è possibile identificare quando il comportamento di un cliente è coerente e quando potrebbe esserci l&#39;opportunità di agire su un nuovo comportamento. È sufficiente fare clic sul menu a discesa accanto a &quot;Tutti i visitatori&quot; durante la creazione di un&#39;attività. Quindi, selezionate le caselle contenenti fino a venti audience, fate clic su &quot;Combina più audience&quot; e fate clic su &quot;Salva&quot;.

Per istruzioni dettagliate, vedere [Combinazione di più tipi di pubblico](/help/c-target/combining-multiple-audiences.md).

**Buono a conoscere**:  [!DNL Adobe Audience Manager] le audience sono disponibili in  [!DNL Target] automatico. Ma la condivisione di [!DNL Adobe Analytics] audience richiede un po&#39; di configurazione manuale. È sufficiente selezionare la casella con l&#39;etichetta &quot;Make this an  Experience Cloud audience&quot; durante il processo di creazione dell&#39;audience in [!DNL Analytics]. Quindi, da [!DNL Target], fate clic su &quot;Importa pubblico  Experience Cloud&quot;.

## Suggerimento 3: Esportate i dati da Target per utilizzarli con strumenti di terze parti.

Grazie ai token di risposta, gli amministratori possono estrarre facilmente i dati da [!DNL Target] e inserirli in strumenti di terze parti. Questo può essere utile per aggiungere i dati ai dati raccolti in uno strumento di sondaggio. Ad esempio, se un sondaggio mostra un campione di una popolazione che ha ottenuto un punteggio &quot;9&quot; e un&#39;altra ha ottenuto un punteggio pari a &quot;4&quot;, potete utilizzare i vostri dati per vedere chi ha visto l&#39;esperienza A e chi ha visto l&#39;esperienza B. È inoltre possibile utilizzare i token di risposta per esportare i dati [!DNL Target] nel data warehouse interno. Fai clic su &quot;Amministrazione&quot;, quindi seleziona il pulsante accanto al Token di risposta desiderato nella posizione attiva. Quindi, create un&#39;attività. I dati sono quindi pronti per essere trasferiti al fornitore di terze parti. È possibile verificare che [!DNL Target] stia esportando i dati utilizzando gli strumenti di debug.

Per istruzioni dettagliate, vedere [Token di risposta](/help/administrating-target/response-tokens.md).

**Suggerimenti utili**: Prima che un amministratore possa attivare un token di risposta associato a una terza parte, lo sviluppatore deve impostare una partnership con tale società terza.

Per istruzioni dettagliate, vedere [Token di risposta](/help/administrating-target/response-tokens.md).

**Effettuate prima** questa operazione: Accertatevi di utilizzare at.js versione 1.1 o successiva. Se utilizzate una versione precedente, vedrete i token di risposta, ma at.js non sarà in grado di utilizzarli.

## Suggerimento 4: Create audience da queste variabili chiave per aumentare il valore dell&#39;attività.

Quando create audience per il targeting o testate promozioni e offerte, prendete in considerazione le seguenti variabili:

* Comportamento. Modelli di visita del sito e modelli di acquisto
* Referrer. Riferimenti a siti e campagne
* Temporale. Orari del giorno, giorni della settimana e fattori stagionali
* Offline. Visita e modelli di acquisto presso negozi fisici
* Ambiente. Paese di origine, sistema operativo, tipo di browser

## Suggerimento 5: Dare agli utenti il livello di accesso di cui hanno bisogno per svolgere il loro lavoro.

Semplificate l&#39;utilizzo dei dati aziendali e manteneteli al sicuro. [!DNL Target Premium] consente agli amministratori di controllare il livello di accesso concesso ai diversi team interni ed esterni.

Per ulteriori informazioni, vedere [Autorizzazioni utente Enterprise](/help/administrating-target/c-user-management/property-channel/property-channel.md).

**Suggerimenti utili**: Quando aggiungete utenti, se il nome di un membro del team non è stato aggiunto in precedenza all’organizzazione, ad esempio nel caso di un dipendente di un’agenzia di terze parti, l’immissione del relativo indirizzo e-mail e della relativa password attiverà un invito e-mail a partecipare all’area di lavoro di un team.

Utilizzo di Target Standard È comunque possibile [assegnare tre livelli di accesso](/help/administrating-target/c-user-management/c-user-management/user-management.md) agli utenti con ruoli di sola lettura, editor e approver!

## Suggerimento 6: Scopri le prestazioni di un&#39;offerta lungo il percorso del cliente testandola su ogni pagina del percorso.

Scopri le prestazioni di un’offerta, ad esempio la spedizione gratuita, durante il percorso del cliente che si svolge su più pagine del sito Web.

Per istruzioni dettagliate, vedere [Attività multipagina](/help/c-experiences/c-visual-experience-composer/multipage-activity.md).

**Suggerimenti utili**: Modificando l&#39;URL dopo che avete specificato un intervallo di pagine, l&#39;esperienza verrà reimpostata. Ciò significa che le varianti specificate non verranno più visualizzate. Se dovete modificare l&#39;URL, ricordate di ridefinire l&#39;esperienza.

## Suggerimento 7: Sottoponete a test un&#39;offerta con audience diverse per scoprire se il pubblico ha preferenze diverse.

Con Versioni esperienza, puoi eseguire un test con varianti per il numero desiderato di tipi di pubblico. Ad esempio, potete creare un banner pubblicitario che offre la spedizione gratuita, con immagini e variazioni di valuta per i clienti negli Stati Uniti, nel Regno Unito e negli Stati Uniti, senza dover eseguire test per tre tipi di pubblico diversi.

Per istruzioni dettagliate, vedere [Tipi di pubblico con esperienza multipla in un test A/B](/help/c-activities/t-test-ab/t-test-create-ab/target-experience-to-multiple-audiences.md) e [Versioni esperienza in  Adobe Target](https://helpx.adobe.com/target/how-to/experience-versions.html?playlist=/ccx/v1/collection/product/target/seg-%20ment/business-practitioners/explevel/beginner-adls/applaunch/how-to-2/collection.ccx.js?ref=helpx.adobe.com).

## Suggerimento 8: Risparmiate tempo replicando esperienze di attività su pagine simili.

Create una variante su una pagina Web, ad esempio un nuovo colore pulsante, e applicatela automaticamente a tutte le pagine che condividono lo stesso modello. Potete specificare le pagine o applicare le varianti a tutte le pagine simili all’interno del sito Web.

Per istruzioni dettagliate, consultate [Includere la stessa esperienza in pagine simili](/help/c-experiences/c-visual-experience-composer/temtest.md).

## Suggerimento 9: Riduci il disordine nella Libreria Pubblico creando audience una tantum.

Se stai effettuando il targeting di un segmento che sai non sarà nuovamente utilizzato, ad esempio, i clienti colpiti da un evento meteo imprevisto, la creazione di un pubblico monouso può aiutarti a portare a termine il lavoro senza dover aggiungere confusione alla Libreria Pubblico. In questo modo è più facile trovare le audience utilizzate più e più volte.

Per istruzioni dettagliate, consultate [Creare un&#39;audience solo per l&#39;attività](/help/c-target/creating-activity-only-audience.md).

**Funzionalità** altamente richiesta: I nostri clienti ci hanno chiesto di poter evitare che i tipi di pubblico a uso singolo vengano salvati automaticamente nella Libreria Pubblico. Ora, non devono più eliminare manualmente i tipi di pubblico per mantenere organizzate le loro librerie.

## Suggerimento 10: Eseguire semplici test più velocemente, evitando di passare attraverso il processo standard di controllo qualità.

Non c&#39;è niente di peggio che avere un&#39;attività pronta per andare e poi settimane di attesa per completare il processo di QA standard. È possibile QA la maggior parte delle attività semplicemente passando alcuni collegamenti QA ai colleghi per provarli su vari browser. Molto probabilmente vorrete eseguire più test di qualità per gli sforzi che modificano radicalmente la funzione del sito, ma in realtà, dovreste avere meno di queste attività e molto di più delle attività di base. L&#39;aggiunta di migliori controlli sui diritti in modo che meno persone possano spingere le cose completamente in vita aggiunge anche limiti significativi e consente di realizzare ciò a cui avete bisogno senza sacrificare velocità ed efficienza. Un&#39;altra opzione consiste nel disporre di una risorsa IT specifica per fornire una supervisione tempestiva del processo di controllo della qualità.

Per istruzioni dettagliate, vedere [Attività QA](/help/c-activities/c-activity-qa/activity-qa.md).

## Suggerimento 11: Eseguite i test sulle pagine con traffico elevato in modo che raggiungano più rapidamente la rilevanza statistica.

Molti esperti di marketing avviano programmi di ottimizzazione per la segmentazione del pubblico e il targeting senza verificare se i livelli di traffico e le audience rappresentati forniranno risultati significativi entro il periodo di tempo di test per i loro obiettivi di ottimizzazione e conversione. Per evitare questo errore comune, rispondete anticipatamente a queste domande:

* Quanti visitatori unici giornalieri ha la pagina?
* Qual è il tasso di conversione per la pagina?
* Per quanto tempo si prevede di eseguire il test prima di poterlo chiamare completo?

**Suggerimento** utile: Utilizzate il  [calcolatore delle dimensioni ](https://docs.adobe.com/content/target-microsite/testcalculator.html) del campione di Target per determinare le dimensioni del campione necessarie per un test di successo.

## Suggerimento 12: Progettate test più semplici per essere certi di poterli creare e implementare.

Dopo aver preso in considerazione tutti gli aspetti di come progettare un test, un piano può diventare molto complesso. In base a dove si trova la vostra azienda con i test e alla capacità del vostro gruppo di progettare, programmare, eseguire e analizzare i risultati, stabilite se il test sembra troppo ambizioso. In caso affermativo, essere pronti a ridurre la portata e la complessità della questione. Meglio iniziare con dimensioni ridotte che non eseguire il test. Non potete fornire un incremento di impatto se non avviate mai il test. È importante bilanciare le aspirazioni del team con le realtà delle proprie risorse e capacità.

## Suggerimento 13: Suddividere i test complessi in attività di test più piccole per renderli realizzabili.

Anziché sviluppare un unico test di grandi dimensioni con più variabili e uno sviluppo complesso, è necessario sviluppare una serie meno complessa di test di dimensioni più ridotte con variabili minime. Questo consente di comprendere meglio le prestazioni dei test in base a variabili specifiche. Riduce anche le possibili questioni tecniche che derivano dallo sviluppo di progetti più grandi.

![Interruzione di un&#39;illustrazione di test complessi](/help/c-intro/assets/break-complex-tasks.png)

## Suggerimento 14: Ottimizzate l&#39;impatto del test eseguendo test più vicini alla fine del funnel di conversione.

Il test eseguito vicino alla pagina in cui i visitatori fanno clic su Completa acquisto, Invia applicazione o completano in altro modo una conversione tende a fornire i risultati più incisivi. I visitatori che raggiungono la fine dell&#39;imbuto sono più qualificati, hanno investito più tempo e sono pronti all&#39;acquisto, pertanto la verifica delle informazioni sulle loro preferenze e azioni può aiutarti a realizzare cambiamenti redditizi. Poiché le pagine del percorso di acquisto sono fondamentali per i tassi di conversione, i test condotti su tali pagine dovrebbero essere socializzati con le principali parti interessate prima di distribuirli.

![Imbuto di conversione illustrazione](/help/c-intro/assets/conversion-funnel.png)

## Suggerimento 15: Aggiornate costantemente i test per apportare miglioramenti ripetitivi.

Se la tua ipotesi non si è rivelata vera, pensa a come migliorare il test. Tenete presente che anche se nessuna delle esperienze testate è stata eseguita meglio, l’esperimento non è stato una perdita di tempo. Un test di successo non implica sempre un incremento delle entrate o delle conversioni. Se il test ha effettivamente sostenuto l’ipotesi, siete sulla strada per sviluppare una teoria generale. Ma anche quando hai un risultato vincente chiaro, non fermarti lì. Troppo spesso, gli esperti di marketing commettono l&#39;errore di testare una volta per tutte questi risultati senza comprendere realmente cosa abbia portato al successo. Piuttosto, pianificare un&#39;iterazione su questi risultati per capire perché il front-runner è stato avanti. In questo modo potrai ottenere informazioni più approfondite che potrai utilizzare nelle campagne future.

## Suggerimento 16: Confronta test e attività di personalizzazione per idee per migliorare il targeting.

Confrontando le prestazioni di conversione di audience diverse all&#39;interno di test diversi in diverse aree, è possibile mettere a fuoco e perfezionare la strategia di ottimizzazione di un&#39;azienda. Utilizzate i confronti di test per identificare quali tipi di pubblico sono più importanti da sottoporre a test, quali dovrebbero ricevere esperienze mirate e quali tipi di esperienze sono più propensi a suscitare una risposta.

Ad esempio, un cliente di servizi finanziari ha condotto una campagna promozionale per una carta di credito che ha coinvolto incentivi per eventi sportivi professionali. Attraverso il test multivariato fattoriale parziale delle pagine di destinazione, il cliente è stato in grado di bilanciare in modo ottimale i messaggi sui benefici delle carte di credito con incentivi sportivi per indirizzare audience distinte dalla base di clienti. Questo approccio ha permesso all&#39;azienda di sfruttare e massimizzare la conversione durante una finestra sensibile al tempo intorno a un evento sportivo importante.

## Suggerimento 17: Rendi i test utili solo avviandoli se sai di poter agire sui dati.

Un test è inutile se non sai bene in che modo agirai sui dati. Ciò include la conoscenza della metrica di successo chiave, ciò che deve accadere per spingere un vincitore, come seguirete i risultati dei test e cosa farete con le informazioni sul pubblico. Per un test rapido e di successo, è fondamentale che ogni gruppo coinvolto nel test (sviluppatori, creativi, specialisti di test e altri) sia consapevole del suo ruolo prima del lancio del test.

## Suggerimento 18: Prima di avviare un test, assicurati che il business supporti la promozione del vincitore.

Le organizzazioni di ottimizzazione di successo credono nel concetto di test e comprendono che le loro opinioni professionali su quale esperienza vincerà il test non sempre si rivelano vere. Determinano il vincitore in base a solide basi di dati e sono desiderosi e disposti a trasmettere live l&#39;esperienza vincente dopo che i risultati sono stati raggiunti, anche se non è in linea con le loro aspettative o sembra incoerente.

Ad esempio, un cliente di servizi sanitari di  Adobe ha recentemente dimostrato il valore dei test mostrando come un banner eroe che il team aveva considerato una fetta di fenditura avesse avuto un impatto negativo sulla conversione. Se l’organizzazione non ha ancora adottato completamente i test, è meglio eseguire prima test dell’ambito più semplici e di dimensioni più ridotte, in modo che le modifiche dai risultati dei test possano essere apportate in modo incrementale.

## Suggerimento 19: Informate tutti che avete avviato un test per evitare preoccupazioni in caso di modifica del sito.

Uno dei vantaggi della configurazione delle attività per l&#39;utilizzo dei parametri di QA è che potete condividere tali collegamenti con tutti i membri del team. Rendete più consapevoli dell&#39;attività e assicuratevi che il sito non funzioni correttamente quando raggiungono una variante di test.

Dopo aver completato i test, comunicare gli avvii delle campagne, i risultati dei test e soprattutto le lezioni apprese consente di acquisire consapevolezza e interesse per i risultati del test. La condivisione dei risultati con tutti nell&#39;organizzazione evita inoltre di ripetere un&#39;ipotesi, educa tutti su ciò che funziona e li aiuta a sfidare fondamentalmente le proprie idee su ciò che funziona in base a ciò che hai trovato. È buona norma preparare un modello che usate ogni volta per condividere i risultati e le informazioni chiave.
Quindi prendete in considerazione la creazione di un libro condivisibile o di un deck Microsoft PowerPoint che acquisisca cumulativamente queste informazioni.

## Suggerimento 20: Sfruttate la funzionalità mobile per creare attività mobili più innovative.

Le esperienze degli utenti di tablet e smartphone devono concentrarsi sui controlli touch come interazione principale con il visitatore, anziché sui clic del mouse e sui controlli della tastiera. Sfruttate i controlli per la visualizzazione mobile, quali sfioramento del dito, tocco, trascinamento, avvicinamento delle dita e zoom. Utilizzate pulsanti semplici e grandi per specificare interazioni e navigazione, ad esempio un grande carrello o un pulsante di riproduzione video. Per la progettazione per la vendita al dettaglio per dispositivi mobili, incorporate una visualizzazione di prodotto avanzata ottimizzata per il tipo di dispositivo. Cercate sempre l&#39;opportunità di spostare l&#39;attenzione dell&#39;utente su visualizzatori incorporati, di grandi dimensioni o con scorrimento e zoom interattivi a schermo intero, 360 gradi e funzionalità video migliorate.

## Suggerimento 21: Aiuta i visitatori di dispositivi mobili a trovare ciò che desiderano ottimizzando la ricerca per dispositivi mobili.

Gli utenti di dispositivi mobili hanno un intento elevato. La maggior parte di loro utilizza la ricerca prima di fare qualsiasi altra cosa sui siti di m-commerce, rendendo cruciale l&#39;ottimizzazione della ricerca di siti mobili. Per migliorare l&#39;ottimizzazione SEO (Search Engine Optimization, ottimizzazione dei motori di ricerca) per dispositivi mobili, utilizzate suggerimenti di navigazione espliciti per semplificare la navigazione. Inoltre, è possibile implementare il suggerimento automatico e la correzione automatica nelle caselle di immissione della ricerca per risolvere la difficoltà di digitazione mobile. Fornire risultati di ricerca accattivanti e pertinenti ottimizzati per le dimensioni e la posizione dello schermo.

## Suggerimento 22: Raggiungete il pubblico dei dispositivi mobili in modo migliore utilizzando il targeting in base ai tempi per le campagne SEM per dispositivi mobili.

Scopri come e quando raggiungere il pubblico e come gestire meglio la spesa pubblicitaria giornaliera &quot;suddividendo giorno per giorno&quot; le tue campagne mobili in segmenti diversi nel corso della giornata.

Molti esperti di marketing commettono l&#39;errore di non riuscire a allocare abbastanza budget per acquisire quella quota di voce nelle ore in cui l&#39;uso di particolari dispositivi è più pesante, lasciando così molti ricavi e lead sul tavolo.

Ad esempio, l&#39;uso del tablet solitamente picchi nelle ore serali, e molti utenti sfogliano mentre guardano il televisore. Al contrario, gli utenti di smartphone solitamente accedono ai contenuti in movimento. I tempi di conversione dei picchi variano anche a seconda del settore, pertanto è importante capire quando i clienti unici sono più propensi a comportarsi.

## Nota bene

Considerate le seguenti idee prima di passare al prossimo capitolo: &quot;Ispirazione per attività di test e personalizzazione.&quot;

### Quando create i test, non decorate, siate intenzionali.

* Controllare il flusso con i percorsi oculari intenzionali focalizzati sui punti di conversione.
* Assicurati di usare il tuo immobile a proprio vantaggio.
* Sfruttate la messa a fuoco dell’immagine per garantire che le immagini non siano decorative, ma che funzionino per voi.
* Con Copia semplificata potete ridurre l&#39;ingombro, l&#39;attrito e la sfocatura.
* Assicurati di disporre di chiamate efficaci alle azioni quando devi che l&#39;utente intervenga.
* Se possibile, aggiungete credibilità tramite il contenuto generato dagli utenti.

### Semplificate il sito Web.

* Non fate leggere ai clienti. Non lo faranno.
* Semplificate la scansione.
* Utilizzare blocchi di copia puntati.
* Assicurarsi che la copia segua un processo di pensiero chiaro e sequenziale.

### Utilizzo di Call To Actions (CTA) efficaci

* Mettiti nei panni del cliente.
* Utilizzare un linguaggio orientato alle azioni.
* Considerate la motivazione per la conversione.
* Indirizzo del risultato della conversione.
* Assicuratevi che i CTA siano visibili!