---
keywords: Overview and Reference;act
description: Informazioni sui concetti chiave che ti aiuteranno a comprendere le funzionalità di Adobe Target.
title: Concetti chiave di Target
feature: intro
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1513'
ht-degree: 98%

---


# Concetti chiave di Target{#target-key-concepts}

Informazioni sui concetti chiave che ti aiuteranno a comprendere le funzionalità di Adobe Target.

## Attività e test {#section_BEA0A0C51A8847579B566060206DE7E8}

Un’attività determina le esperienze potenziali di un visitatore del sito.

Ad esempio, puoi progettare un&#39;attività che sottopone a test due diverse pagine di destinazione, una con informazioni in evidenza sulle scarpe estive da donna e un&#39;altra con in evidenza abbigliamento estivo generico. L&#39;attività determina le condizioni che controllano quando ciascuna di queste pagine di destinazione viene visualizzata e le metriche che determinano quale pagina ha più successo. L&#39;attività è configurata per iniziare e terminare quando vengono soddisfatte determinate condizioni, ad esempio tra date specifiche, o per iniziare quando l&#39;attività viene approvata e per terminare quando viene disattivata.

Pianifica con attenzione durante la progettazione di una attività. Determina quando inizierà l&#39;attività e quanto tempo durerà. Quindi, crea un elenco delle offerte e assegna un tipo di pubblico a ciascuna.

Target include diversi tipi di attività. La tabella seguente fornisce una panoramica di ogni tipo di attività con collegamenti per ulteriori informazioni. Per aiutarti a scegliere meglio il tipo di attività migliore, abbiamo anche creato la [Guida alle attività di Adobe Target](/help/c-activities/target-activities-guide.md).

| Tipo di attività | Descrizione |
|--- |--- |
| [Test A/B](/help/c-activities/t-test-ab/test-ab.md) | Il test A/B confronta due o più versioni del contenuto del sito web per vedere quale versione migliora maggiormente le conversioni durante un dato periodo di test.<br>**Nota:** ora puoi includere i [consigli nelle attività di test A/B](/help/c-recommendations/recommendations-as-an-offer.md). Questa funzionalità richiede una [licenza di Target Premium](/help/c-intro/intro.md#premium). |
| [Allocazione automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | L’allocazione automatica identifica un vincitore tra due o più esperienze e, di conseguenza, ridistribuisce automaticamente più traffico per aumentare le conversioni, mentre il test continua a essere eseguito e ad apprendere.<br>**Nota:** ora puoi includere i [consigli nelle attività di allocazione automatica](/help/c-recommendations/recommendations-as-an-offer.md). Questa funzionalità richiede una [licenza di Target Premium](/help/c-intro/intro.md#premium). |
| [Targeting automatico](/help/c-activities/auto-target/auto-target-to-optimize.md)<br>![Target Premium](/help/assets/premium.png) | La funzione Targeting automatico utilizza l’apprendimento automatico avanzato per individuare più esperienze ad alte prestazioni definite dall’addetto al marketing. Inoltre, indica l’esperienza più adatta per ogni visitatore in base al suo profilo cliente individuale e al comportamento dei visitatori precedenti con profili simili, al fine di personalizzare contenuti e favorire le conversioni.<br>**Nota:** ora puoi includere i [consigli nelle attività di targeting automatico](/help/c-recommendations/recommendations-as-an-offer.md). Questa funzionalità richiede una [licenza di Target Premium](/help/c-intro/intro.md#premium). |
| [Utilizzo dei dati di Analytics](/help/c-activities/t-test-ab/t-test-create-ab/create-a4t.md) (A4T) | Puoi configurare un&#39;attività per utilizzare [!DNL Adobe Analytics] come origine per i rapporti. Questo tipo di attività richiede di collegare il tuo account [!DNL Adobe Experience Cloud] sia con [!DNL Analytics] sia con [!DNL Target]. |
| [Test multivariato](/help/c-activities/c-multivariate-testing/multivariate-testing.md) | Il test multivariato (Multivariate Testing, MVT) confronta le combinazioni di offerte negli elementi di una pagina per determinare quale combinazione funziona al meglio per un pubblico specifico e identifica quale elemento influisce maggiormente sul successo dell’attività. |
| [Targeting esperienza](/help/c-activities/t-experience-target/experience-target.md) | La funzione Targeting esperienza (XT) fornisce contenuti a un pubblico specifico basato su una serie di regole e criteri definiti dagli addetti al marketing.<br>**Nota:** ora puoi includere i [consigli nelle attività di targeting delle esperienze](/help/c-recommendations/recommendations-as-an-offer.md). Questa funzionalità richiede una [licenza di Target Premium](/help/c-intro/intro.md#premium). |
| [Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/automated-personalization.md)<br>![Target Premium](/help/assets/premium.png) | La personalizzazione automatizzata (AP) combina offerte o messaggi e utilizza l&#39;apprendimento automatico avanzato per abbinare diverse varianti a ciascun visitatore in base al suo profilo cliente, per personalizzare i contenuti ed effettuare le conversioni. |
| [Consigli](/help/c-recommendations/recommendations.md)<br>![Target Premium](/help/assets/premium.png) | Un consiglio determina il modo in cui un prodotto viene suggerito a un utente del sito web, a seconda delle attività dell&#39;utente sul sito.<br>Ad esempio, potrebbe essere utile incoraggiare l&#39;acquirente di uno zaino a considerare l&#39;acquisto di scarpe e bastoncini da trekking. Puoi creare un consiglio che mostra gli elementi spesso acquistati insieme con l&#39;algoritmo “Chi ha acquistato questo ha acquistato anche”. Oppure, potrebbe essere utile incoraggiare i visitatori a trascorrere più tempo sul sito multimediale, consigliando un video simile a quello che stanno visualizzando, mediante l&#39;algoritmo “Chi ha visualizzato questo ha visualizzato anche”.<br>**Nota:** ora puoi includere i consigli nelle attività di test A/B (tra cui Allocazione automatica e Targeting automatico) e targeting delle esperienze (XT). Consulta [Consigli come offerta](/help/c-recommendations/recommendations-as-an-offer.md). |

## Posizioni {#section_F18FBF1ED23340ED9F39C51971A4E874}

Il termine “posizione” si riferisce in genere a una pagina del sito web. Ma può anche riferirsi a un’ubicazione in un’app mobile, un messaggio e-mail o qualsiasi altro ambito in cui si esegue un’ottimizzazione.

Le posizioni sono elementi essenziali per le attività e le esperienze. Sarai tu a decidere se per una posizione devono essere eseguite le attività seguenti, solo una di esse o nessuna:

* Visualizzare e sostituire il contenuto per i visitatori.
* Registrare il comportamento dei visitatori.

In [!DNL Target Standard], una posizione può essere un qualsiasi elemento in una pagina, purché la pagina contenga una singola riga di codice che abilita [!DNL Target] nella sezione `<head>` di ogni pagina da monitorare. Questa riga di codice richiama le librerie JavaScript necessarie per raccogliere le informazioni e trasmettere esperienze mirate ai visitatori.

Le posizioni vengono combinate con i tipi di pubblico per fornire un numero praticamente infinito di opzioni per indirizzare le informazioni ai clienti. Ad esempio, se un visitatore non è mai stato prima sul tuo sito, puoi presentargli un buono sconto speciale per i nuovi clienti. Allo stesso modo, la pagina potrebbe essere modificata con offerte ottimizzate per i clienti che ritornano.

Inoltre è possibile utilizzare le posizioni per monitorare i movimenti di un visitatore all’interno del sito web o il completamento di specifiche metriche di successo, ad esempio l’aggiunta di un articolo al carrello o un acquisto.

## Esperienze e progettazioni di pagine {#section_B806FB752EC1470784755C1EB3D4AC70}

Un’esperienza, a volte detta ricetta, definisce il contenuto visualizzato sulla pagina, così come altri elementi della pagina stessa, ad esempio i collegamenti.

Un’esperienza determina quale offerta visualizzare in una determinata posizione quando sono soddisfatte specifiche condizioni di targeting. Ad esempio, per i visitatori che ritornano al sito, l’esperienza fa sì che nella parte superiore della pagina venga presentata un’offerta di spedizione rapida. Se invece si tratta della prima visita di un visitatore, l’esperienza fa sì che nella stessa posizione venga presentato uno sconto del 10%.

Un’esperienza è costituita da offerte, risorse immagine o altri elementi HTML (come i collegamenti) che vengono visualizzati sulla pagina allo scopo di dirigere il visitatore verso il risultato desiderato. [!DNL Target] combina posizioni, offerte ed esperienze per determinare quali contenuti visualizzare sul sito durante uno specifico test.

Un’esperienza può essere rappresentata anche da una diversa progettazione di pagina. Ad esempio, è possibile che un’esperienza includa un insieme di collegamenti nella parte superiore della pagina, e un’altra includa collegamenti diversi o gli stessi disposti in un diverso ordine. Potrebbe essere utile verificare se un’immagine fornisce un incremento maggiore di un’altra, o se è più probabile che venga fatto clic su un annuncio nella parte superiore della pagina piuttosto che un’altra posizione.

Con [!DNL Target] è possibile ottimizzare le esperienze per ogni visitatore nei diversi ambienti digitali, sottoponendo a test esperienze diverse per determinare quale avrà maggior successo. Mediante un targeting delle esperienze attentamente pianificato, puoi fare in modo che i visitatori del sito ricevano le offerte più rilevanti nelle posizioni migliori sulla pagina, ottimizzando le probabilità di successo di una visita.

## Offerte {#section_973D4CC4CEB44711BBB9A21BF74B89E9}

Un’offerta è il contenuto visualizzato sulle pagine web durante le campagne o le attività.

Quando esegui un test sulle pagine web, misuri il successo di ogni esperienza con offerte diverse nelle tue posizioni.

Un’offerta può contenere diversi tipi di contenuto, inclusi:

* Immagine
* Testo
* HTML
* Collegamento
* Pulsante

Ad esempio, una pagina web può visualizzare una tra due offerte, sulla base di un’eventuale precedente visita sul tuo sito da parte del visitatore.

Un’*esperienza* determina il contenuto visualizzato quando si verificano determinate condizioni.

## Tipi di pubblico {#section_3F32DA46BDF947878DD79DBB97040D01}

Ottimizza i contenuti destinati ai partecipanti all’attività che soddisfano criteri specifici.

I tipi di pubblico definiscono a chi si rivolge l’attività e sono utilizzati ovunque sia disponibile il targeting.

Il pubblico di [!DNL Target] è un insieme di criteri definiti e collegati ai visitatori. Puoi eseguire il targeting delle offerte per tipi di pubblico (o segmenti) specifici. Solo i visitatori che appartengono a quel pubblico visualizzeranno l’esperienza a loro destinata.

Ad esempio, puoi eseguire il targeting di un’attività per un pubblico composto dai visitatori che usano un particolare sistema operativo o browser.

In alternativa, puoi eseguire il targeting di un’attività per i visitatori provenienti da una determinata area geografica o per chi accede alla pagina da un determinato motore di ricerca.

I tipi di pubblico possono essere salvati e riutilizzati in più attività, oppure possono essere creati per un’attività specifica.

| Tipo di pubblico | Descrizione |
|--- |--- |
| Pubblico riutilizzabile | I tipi di pubblico riutilizzabili possono essere selezionati per qualsiasi attività. Se modifichi uno di questi tipi di pubblico, la modifica viene applicata a tutte le attività che lo utilizzano. |
| Segmenti personalizzati | I segmenti personalizzati (o segmenti specifici della campagna) sono specifici per una determinata campagna in Target Classic. Vengono creati come parte della campagna e non possono essere riutilizzati in altre campagne. |
| Pubblico condiviso | Il pubblico può essere condiviso tra le diverse soluzioni [!DNL Adobe Experience Cloud]. See [Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html) for examples. |

Per informazioni su come il profilo visitatore tiene traccia delle informazioni sui visitatori del sito, consulta [Profili dei visitatori](/help/c-target/c-visitor-profile/visitor-profile.md#concept_5E53D1A6DF224D7BAE76F4AE390B9DA1).

## Video di formazione:

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Tipi di attività (9:03) ![badge Panoramica](/help/assets/overview.png)

Questo video spiega i tipi di attività disponibili in [!DNL Target Standard/Premium].

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Utilizzo dell&#39;audience  contrassegno ![Panoramica di Adobe Target (6:21)](/help/assets/overview.png)

Questo video spiega come utilizzare i tipi di pubblico in [!DNL Target Standard/Premium].

* Spiegazione del termine “pubblico”
* Spiegazione dei due modi in cui il pubblico viene utilizzato per lʼottimizzazione
* Trovare un pubblico nellʼelenco Tipi di pubblico
* Indirizzare unʼattività a un pubblico
* Utilizzare i tipi di pubblico per la reportistica passiva in un’attività

>[!VIDEO](https://video.tv.adobe.com/v/17398)
