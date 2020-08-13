---
keywords: activities list;activities;activity;activity types;edit activity;activity actions;activity attribute;activity list filter;activity limitations;personalize;personalization
description: Le attività in  Adobe Target consentono di personalizzare il contenuto per audience specifiche e di sottoporre a test i design delle pagine
title: Le attività in  Adobe Target consentono di personalizzare il contenuto per audience specifiche e di sottoporre a test le progettazioni di pagina.
feature: activities
topic: Standard
uuid: 89dca5b4-c23d-4dfa-8f13-f1b05c7ab22c
translation-type: tm+mt
source-git-commit: b2f80c89ecceb6f88a176db7a90e71a162a24641
workflow-type: tm+mt
source-wordcount: '2094'
ht-degree: 97%

---


# Attività{#activities}

Le attività in  Adobe Target consentono di personalizzare il contenuto per audience specifiche e di sottoporre a test le progettazioni di pagina.

Ad esempio, puoi progettare un’attività che sottopone a test due diverse pagine di destinazione, una con informazioni in evidenza sulle scarpe estive da donna e un’altra con abbigliamento estivo generico. L&#39;attività determina le condizioni che controllano quando ciascuna di queste pagine di destinazione viene visualizzata e le metriche che determinano quale pagina ha più successo. L&#39;attività è configurata per iniziare e terminare quando vengono soddisfatte determinate condizioni, ad esempio tra date specifiche, o per iniziare quando l&#39;attività viene approvata e per terminare quando viene disattivata.

Pianifica con attenzione durante la progettazione di una attività. Determina quando inizierà l&#39;attività e quanto tempo durerà. Quindi, crea un elenco delle offerte e assegna un tipo di pubblico a ciascuna.

## Tipi di attività

Target include diversi tipi di attività. La tabella seguente fornisce una panoramica di ogni tipo di attività con collegamenti per ulteriori informazioni. Per aiutarti a scegliere meglio il tipo di attività migliore, abbiamo anche creato la [Guida alle attività di Adobe Target](/help/c-activities/target-activities-guide.md).

| Tipo di attività | Descrizione |
|--- |--- |
| [Test A/B](/help/c-activities/t-test-ab/test-ab.md) | Il test A/B confronta due o più versioni del contenuto del sito web per vedere quale versione migliora maggiormente le conversioni durante un dato periodo di test.<br>**Nota:** ora puoi includere i [consigli nelle attività di test A/B](/help/c-recommendations/recommendations-as-an-offer.md). Questa funzionalità richiede una [licenza di Target Premium](/help/c-intro/intro.md#premium). |
| [Allocazione automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | L’allocazione automatica identifica un vincitore tra due o più esperienze e, di conseguenza, ridistribuisce automaticamente più traffico per aumentare le conversioni, mentre il test continua a essere eseguito e ad apprendere.<br>**Nota:** ora puoi includere i [consigli nelle attività di allocazione automatica](/help/c-recommendations/recommendations-as-an-offer.md). Questa funzionalità richiede una [licenza di Target Premium](/help/c-intro/intro.md#premium). |
| [Targeting automatico](/help/c-activities/auto-target-to-optimize.md)<br>![Target Premium](/help/assets/premium.png) | La funzione Targeting automatico utilizza l’apprendimento automatico avanzato per individuare più esperienze ad alte prestazioni definite dall’addetto al marketing. Inoltre, indica l’esperienza più adatta per ogni visitatore in base al suo profilo cliente individuale e al comportamento dei visitatori precedenti con profili simili, al fine di personalizzare contenuti e favorire le conversioni.<br>**Nota:** ora puoi includere i [consigli nelle attività di targeting automatico](/help/c-recommendations/recommendations-as-an-offer.md). Questa funzionalità richiede una [licenza di Target Premium](/help/c-intro/intro.md#premium). |
| [Utilizzo dei dati di Analytics](/help/c-activities/t-test-ab/t-test-create-ab/create-a4t.md) (A4T) | Puoi configurare un&#39;attività per utilizzare [!DNL Adobe Analytics] come origine per i rapporti. Questo tipo di attività richiede di collegare il tuo account [!DNL Adobe Experience Cloud] sia con [!DNL Analytics] sia con [!DNL Target]. |
| [Test multivariato](/help/c-activities/c-multivariate-testing/multivariate-testing.md) | Il test multivariato (Multivariate Testing, MVT) confronta le combinazioni di offerte negli elementi di una pagina per determinare quale combinazione funziona al meglio per un pubblico specifico e identifica quale elemento influisce maggiormente sul successo dell’attività. |
| [Targeting esperienza](/help/c-activities/t-experience-target/experience-target.md) | La funzione Targeting esperienza (XT) fornisce contenuti a un pubblico specifico basato su una serie di regole e criteri definiti dagli addetti al marketing.<br>**Nota:** ora puoi includere i [consigli nelle attività di targeting delle esperienze](/help/c-recommendations/recommendations-as-an-offer.md). Questa funzionalità richiede una [licenza di Target Premium](/help/c-intro/intro.md#premium). |
| [Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/automated-personalization.md)<br>![Target Premium](/help/assets/premium.png) | La personalizzazione automatizzata (AP) combina offerte o messaggi e utilizza l&#39;apprendimento automatico avanzato per abbinare diverse varianti a ciascun visitatore in base al suo profilo cliente, per personalizzare i contenuti ed effettuare le conversioni. |
| [Consigli](/help/c-recommendations/recommendations.md)<br>![Target Premium](/help/assets/premium.png) | Un consiglio determina il modo in cui un prodotto viene suggerito a un utente del sito web, a seconda delle attività dell&#39;utente sul sito.<br>Ad esempio, potrebbe essere utile incoraggiare l&#39;acquirente di uno zaino a considerare l&#39;acquisto di scarpe e bastoncini da trekking. Puoi creare un consiglio che mostra gli elementi spesso acquistati insieme con l&#39;algoritmo “Chi ha acquistato questo ha acquistato anche”. Oppure, potrebbe essere utile incoraggiare i visitatori a trascorrere più tempo sul sito multimediale, consigliando un video simile a quello che stanno visualizzando, mediante l&#39;algoritmo “Chi ha visualizzato questo ha visualizzato anche”.<br>**Nota:** ora puoi includere i consigli nelle attività di test A/B (tra cui Allocazione automatica e Targeting automatico) e targeting delle esperienze (XT). Consulta [Consigli come offerta](/help/c-recommendations/recommendations-as-an-offer.md). |

## Elenco attività {#section_DE8E2DB30D534962A931EF8BB48240F5}

L’elenco [!UICONTROL Attività] è la vista predefinita all’apertura di [!DNL Target]. Puoi creare nuove attività da questa pagina e gestire quelle esistenti.

Puoi anche visualizzare l’elenco [!UICONTROL Attività] facendo clic sulla scheda [!UICONTROL Attività] nella parte superiore dell’[!DNL Target]interfaccia utente.

![Elenco attività](/help/c-activities/assets/activities-list.png)

L&#39;elenco Attività presenta tutte le attività:

| Elemento | Descrizione |
|--- |--- |
| Tipo | Il tipo di attività, ad esempio A/B o MVT. |
| Nome | Il nome dell&#39;attività. |
| URL | L’URL viene visualizzato in un colore più chiaro sotto il nome.<br>L’URL dell’attività identifica dove viene visualizzata. Consente di identificare rapidamente un’attività e di determinare se su una pagina specifica sia già in esecuzione un test.<br>Se un test viene eseguito su più URL, un collegamento mostra il numero di URL utilizzati. Fai clic sul collegamento per visualizzare l’elenco completo degli URL per l’attività.<br>Puoi eseguire ricerche in base all’URL. Utilizza l’elenco a discesa accanto alla casella di ricerca e seleziona [!UICONTROL Ricerca URL]. |
| Stato | Lo stato dell’attività può essere uno tra i seguenti:<ul><li>**Live**: l’attività è attualmente in esecuzione.</li><li>**Bozza**: la configurazione dell’attività è iniziata, ma l’attività non è ancora pronta per l’esecuzione.</li><li>**Pianificata**: l’attività è pronta per essere attivata nella data e nell’ora di inizio specificate.</li><li>**Inattiva**: l&#39;attività è stata sospesa o disattivata.</li><li>**Sincronizzazione**: l’attività è stata salvata si sta eseguendo la sua sincronizzazione con la rete di consegna Target.</li><li>**Terminata**: la data e l’ora di fine specificate dell’attività sono state raggiunte e l’attività non viene più distribuita.</li><li>**Archiviata**: l’attività è stata archiviata. È possibile attivare un&#39;attività archiviata per utilizzarla nuovamente.</li></ul>**Nota**: quando esegui determinate azioni, ad esempio l’attivazione di un’attività al di fuori dell’interfaccia utente utilizzando i metodi API, l’aggiornamento può richiedere fino a dieci minuti per propagarsi all’interfaccia utente. |
| Origine | Mostra dove è stata creata l&#39;attività:<ul><li>Adobe Target</li><li>Adobe Target Classic</li><li>Adobe Experience Manager (AEM)</li><li>Adobe Mobile Services (AMS)</li></ul> |
| Proprietà | Mostra la [proprietà](/help/administrating-target/c-user-management/property-channel/property-channel.md) per l’attività. |
| Incremento stimato dei ricavi | Mostra l&#39;aumento previsto dei ricavi se il 100% del pubblico visualizza l&#39;esperienza vincente.<br>Calcolato con la seguente formula:<br>`(<winning experience> - <control experience>)*<total number of visitors>`<br>Se nella forma condensata è presente solo una cifra prima del decimale, il risultato viene arrotondato al massimo a una cifra decimale. Ad esempio: $ 1,6 M, $ 60 K, $ 900, $ 8,5 K, $ 205 K<br>In questa colonna viene visualizzato “---” per le attività prive di dati sufficienti per richiamare una visualizzazione vincente o prive di un preventivo di spesa.<br>Consulta [Stima dell’incremento dei ricavi](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) per maggiori informazioni. |
| Ultimo aggiornamento | La data di ultimo aggiornamento dell&#39;attività e l&#39;autore dell&#39;aggiornamento. |

Passa il puntatore del mouse su un’attività per visualizzare le azioni disponibili.

![Elenco delle attività al passaggio del mouse](/help/c-activities/assets/activities_list_hover.png)

Sono disponibili le seguenti azioni (a seconda delle autorizzazioni):

| Azione | Descrizione |
| --- | --- |
| Modifica | Modifica l&#39;attività. Qualsiasi attività può essere modificata.<br>Per ulteriori informazioni su come modificare le attività, consulta [Modificare un’attività o salvarla come bozza](/help/c-activities/edit-activity.md). |
| Disattiva | Interrompe un&#39;attività in esecuzione o pianificata. È possibile riattivare o archiviare una campagna disattivata<br>Se disattivi o archivi un’attività e poi la riattivi in un secondo momento, un visitatore continuerà a esserne parte dopo la riattivazione se vi partecipava prima che fosse disattivata o archiviata. Ogni metrica di conversione registrata durante il periodo trascorso tra i due eventi non verrà attribuita a quell’attività. |
| Attiva | Avvia un&#39;attività inattiva o pronta. |
| Archivia | Invia l&#39;attività all&#39;archivio. Per impostazione predefinita, le attività archiviate non vengono più visualizzate nell&#39;elenco Attività. Per includere nell’elenco anche le attività archiviate, devi cambiare il filtro per l&#39;elenco delle attività. È possibile attivare un&#39;attività archiviata per utilizzarla nuovamente.<br>Se disattivi o archivi un’attività e poi la riattivi in un secondo momento, un visitatore continuerà a esserne parte dopo la riattivazione se vi partecipava prima che fosse disattivata o archiviata. Ogni metrica di conversione registrata durante il periodo trascorso tra i due eventi non verrà attribuita a quell’attività. |
| Copia | Copia un&#39;attività. Qualsiasi attività può essere copiata. Quando si copia un&#39;attività viene creata una nuova attività con lo stesso nome e la dicitura “Copia”. Ad esempio, la copia di un test denominato “Offerte browser” sarà denominata “Copia Offerte browser”.<br>Le offerte visive vengono copiate con l&#39;attività. È possibile modificare in modo sicuro le offerte nella copia senza influire sull&#39;attività originale. L&#39;unica eccezione sono le offerte e le immagini salvate nella cartella Contenuto/Risorse. |
| Elimina | Elimina una bozza o un’attività.<BR>**NOTA**: le attività eliminate non possono essere recuperate. A meno di non essere assolutamente sicuro che questa attività non sarà mai più necessaria, utilizza piuttosto l’azione [!UICONTROL Archivia] in modo da poterla riattivare all’occorrenza. |

Ricorda i seguenti dettagli sull&#39;elenco delle attività:

* Le attività archiviate e terminate non compaiono nell’elenco delle [!UICONTROL Attività]. Per visualizzarle, applica un filtro utilizzando le impostazioni di filtro avanzate nella barra di sinistra.
* Non appena un&#39;attività originariamente creata in [!DNL Target Classic] è disattivata o eliminata, viene eliminata da [!DNL Target Standard/Premium]. Le attività eliminate originariamente create in [!DNL Target Classic] non vengono inviate alla cartella [!UICONTROL Archivio] in [!DNL Target Standard/Premium]. La funzionalità di cartella archiviata è applicabile solo alle attività create in [!DNL Target Standard/Premium].
* Tutti i tipi di attività diversi da [!UICONTROL Personalizzazione automatizzata] (AP), [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] consentono di scegliere se utilizzare [!DNL Target] o [!DNL Adobe Analytics] come origine di dati. [!UICONTROL Personalizzazione automatizzata], [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] usano *sempre* dati [!DNL Target].
* Le attività sono disponibili per diversi canali:

   * Siti web e mobili
   * Schermi e dispositivi collegati a Internet, inclusi chioschi e sportelli automatici
   * Email e altri canali di acquisizione o siti partner
   * App mobili
   * In qualsiasi altro luogo sia possibile fornire contenuti con tag

## Ordinamento e filtraggio dell’elenco Attività {#section_41DAD479FFF740E2BB67BF4825955670}

Per impostazione predefinita, l&#39;elenco è ordinato in base alla data dell&#39;ultima modifica dell&#39;attività, con la modifica più recente in cima. Tuttavia, ci sono diverse opzioni di filtro per aiutarti a personalizzare l&#39;elenco per mostrare le attività che desideri visualizzare.

### Ricerca {#search-heading}

Utilizza il campo di ricerca per cercare le attività corrispondenti ai criteri di ricerca.

![Ricerca attività](/help/c-activities/assets/activities_search_new.png)

Il campo di ricerca include un menu a discesa che consente di restringere la ricerca specificando uno dei seguenti filtri di ricerca: [!UICONTROL Nome attività] e [!UICONTROL URL].

### Filtri per l’elenco Attività

È possibile determinare quali attività vengono visualizzate nell’elenco Attività selezionando i filtri disponibili.

![Filtra attività per tipo](/help/c-activities/assets/activities_filters_new.png)

È possibile filtrare utilizzando le opzioni seguenti. In ogni categoria, se non è selezionato nulla, l&#39;impostazione predefinita è Tutto.

| Categoria filtro | Filtro |
|--- |--- |
| Tipo | Test A/B: [Manuale](/help/c-activities/t-test-ab/test-ab.md), [Allocazione automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) e [Targeting automatico](/help/c-activities/auto-target-to-optimize.md).<br>[Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/automated-personalization.md)<br>[Targeting delle esperienze](/help/c-activities/t-experience-target/experience-target.md)<br>[Test multivariato](/help/c-activities/c-multivariate-testing/multivariate-testing.md)<br>[Consigli](/help/c-recommendations/recommendations.md) |
| Stato | Live<br>Bozza<br>Pianificata<br>Inattiva<br>Sincronizzazione<br>Terminata<br>Archiviata |
| Origine per i rapporti | Target<br>Analytics |
| Compositore esperienza | Visivo<br>Basato su modulo |
| Tipo di metrica | Conversione<br>Revenue<br>Engagement |
| Origine attività | Adobe Target<br>Adobe Target Classic<br>Adobe Experience Manager<br>Adobe Mobile Services |

### Ordina per attributo attività

Fai clic su una delle intestazioni seguenti per impostare se le attività sono elencate in ordine crescente o decrescente per &#39;intestazione selezionata.

* Nome attività
* Tipo di attività

![Elenco delle attività in ordine crescente](/help/c-activities/assets/activities_list_ascending.png)

## Suggerimenti {#section_F77F30A246A14B538D9363B7F3639F97}

Per sfruttare al massimo Adobe Target, scopri di più sulle sue funzioni e come sfruttarle. La funzionalità Suggerimenti offre collegamenti a video, casi d’uso, blog, documentazione e molto altro.

La funzionalità Suggerimenti viene visualizzata periodicamente nella pagina Elenco attività. Dopo aver letto o ignorato un suggerimento, esso non viene visualizzato nuovamente fino a quando non sarà disponibile il suggerimento successivo. È possibile disattivare la visualizzazione di tutti i suggerimenti facendo clic sull&#39;icona Aiuto > [!UICONTROL Disattiva Suggerimento del giorno].

![Disattiva suggerimento del giorno](/help/c-activities/assets/tip-disable-new.png)

## Limitazioni {#section_049D4684403A4E07B998067EB8E9BE56}

Ogni attività di Target presenta le seguenti limitazioni di contenuto:

| Elemento | Limite |
|--- |--- |
| Selettori univoci | 300 Se un selettore viene ripetuto in un&#39;altra esperienza, viene conteggiato una volta. Tuttavia, se si ripete nella stessa esperienza, viene conteggiato nuovamente. |
| Offerte in ogni esperienza | 350 |
| Selettori di tracciamento dei clic nelle metriche | 50 |
| Mbox nelle metriche | 50 |
| Tipi di pubblico e posizioni | 50 Il limite massimo di combinazioni di tipi di pubblico e posizioni (mbox) è 50. |

L’attività non può essere salvata se superi uno di questi limiti.

Un maggior numero di elementi nell&#39;attività comporta anche un aumento del tempo necessario per sincronizzare l&#39;attività in Target.

Per ulteriori limiti del Compositore esperienza visivo, consulta [Limitazioni del Compositore esperienza visivo](../c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721).

## Attributi importati in Target per attività aggiornate al di fuori di Target {#section_802B0D174E6A44E1A96F404CA81AAE44}

Se le attività create in [!DNL Target] vengono aggiornate all&#39;esterno di [!DNL Target] (ad esempio, tramite Adobe I/O), i seguenti attributi di attività vengono importati di nuovo in [!DNL Target]:

`thirdpartyId`

`startDate`

`endDate`

`status`

`priority`

`marketingCloudMetadata(remoteModifiedBy)`

Questo processo di importazione verrà eseguito quando verrà aperta la pagina attività, con un ritardo massimo di dieci minuti. (KB-1526)

## Video di formazione {#section_BE80D13A2E81460C885F902010E1AD87}

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Logo ![Panoramica sui tipi di attività (9:03)](/help/assets/overview.png)

Questo video spiega i tipi di attività disponibili in [!DNL Target Standard/Premium].

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Gestione delle attività (5:55) badge ![Panoramica](/help/assets/overview.png)

Questo video spiega come utilizzare l&#39;elenco Attività per gestire le attività.

* Definizione del termine *attività*
* Trovare le attività nell’elenco Attività
* Modificare, disattivare, copiare ed eliminare le attività

>[!VIDEO](https://video.tv.adobe.com/v/18550)
