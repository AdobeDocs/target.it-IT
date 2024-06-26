---
keywords: elenco attività;attività;tipi di attività;modificare attività;azioni attività;attributo attività;filtro elenco attività;limitazioni attività;personalizzare;personalizzazione;elenco attività;activity list;activities types;edit activity;actions;activity attribute;activity list filter;activity limits;personalization
description: Scopri come le attività in [!DNL Target] consente di personalizzare il contenuto per tipi di pubblico specifici e di testare le progettazioni di pagine.
title: Come posso personalizzare il contenuto e testare le progettazioni di pagine con [!DNL Target]?
feature: Activities
exl-id: 7e61525d-b2db-44f6-a7c2-df5a8d28eca2
source-git-commit: be63fa4c89f229e3f4566cb400e1268d2cdf08d2
workflow-type: tm+mt
source-wordcount: '2290'
ht-degree: 36%

---

# Attività

Attività in [!DNL Adobe Target] consente di personalizzare il contenuto per tipi di pubblico specifici e di testare le progettazioni di pagine.

Ad esempio, puoi progettare un’attività che sottopone a test due diverse pagine di destinazione, una con informazioni in evidenza sulle scarpe estive da donna e un’altra con abbigliamento estivo generico. L&#39;attività determina le condizioni che controllano quando ciascuna di queste pagine di destinazione viene visualizzata e le metriche che determinano quale pagina ha più successo. L&#39;attività è configurata per iniziare e terminare quando vengono soddisfatte determinate condizioni, ad esempio tra date specifiche, o per iniziare quando l&#39;attività viene approvata e per terminare quando viene disattivata.

Pianifica con attenzione durante la progettazione di una attività. Determina quando deve iniziare l’attività e per quanto tempo dura. Quindi, crea un elenco delle offerte e assegna un tipo di pubblico a ciascuna.

## Elenco attività {#section_DE8E2DB30D534962A931EF8BB48240F5}

Il [!UICONTROL Activities] è la visualizzazione predefinita all&#39;apertura di [!DNL Target]. Puoi creare attività da questa pagina e gestire quelle esistenti.

È inoltre possibile visualizzare [!UICONTROL Activities] facendo clic sul pulsante [!UICONTROL Activities] nella parte superiore della sezione [!DNL Target] UI.

![Attività, elenco](/help/main/c-activities/assets/activities-list-new.png)

Il [!UICONTROL Activities] L’elenco fornisce una panoramica di tutte le attività e consente di eseguire varie azioni:

| Elemento | Descrizione |
|--- |--- |
| Barra di navigazione a sinistra | Passare dalle attività salvate o live a quelle non riuscite o [progetti di attività](/help/main/c-activities/edit-activity.md). |
| [!UICONTROL Show filters] icona<P>![Icona Mostra filtri](/help/main/c-activities/assets/show-filters-icon.png) | Accedere ai filtri facendo clic sul pulsante **[!UICONTROL Show Filters]** nella parte superiore dell’elenco.<P>Per ulteriori informazioni, consulta [Applicare i filtri all’elenco Attività](#filters) di seguito. |
| Casella di ricerca | Trovare rapidamente un’attività o ridurre il numero di attività visualizzate in [!UICONTROL Activity] elenco. Puoi eseguire ricerche per [!UICONTROL Name], [!UICONTROL URL], o [!UICONTROL ID]. |
| [!UICONTROL Create Activity] | Crea un’attività. Per ulteriori informazioni sulla creazione dei vari tipi di attività, consulta: <ul><li>[Creare un test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)</li><li>[Creare un’attività](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md)</li><li>[Creare un’attività](/help/main/c-activities/auto-target/create-auto-target.md)</li><li>[Creare un&#39;attività di Automated Personalization](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)</li><li>[Creare un’attività Targeting esperienze](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md)</li><li>[Creazione di un test multivariato](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md)</li><li>[Creare un’attività Consigli](/help/main/c-recommendations/recommendations.md)</li></ul>Per ulteriori informazioni su ciascun tipo, consulta [Tipi di attività](#types) di seguito. |
| [!UICONTROL Create mobile preview link]<P>![Menu Altre azioni](/help/main/c-activities/assets/icon-create-mobile-link.png) | Utilizzare [collegamenti di anteprima mobile](https://experienceleague.adobe.com/docs/target-dev/developer/mobile-apps/target-mobile-preview.html?lang=it) per eseguire un controllo qualità end-to-end semplice per le attività delle app mobili.<P>Fai clic su **Altre opzioni** (i puntini di sospensione verticali), seleziona la **Crea collegamento di anteprima mobile**, quindi scegli le attività da testare su dispositivi mobili. |
| Personalizza tabella<P>![Icona Personalizza tabella](/help/main/c-activities/assets/icon-customize-table.png) | Modificare le colonne visualizzate in [!UICONTROL Activity] facendo clic sul pulsante **[!UICONTROL Customize Table]** in alto a destra, quindi selezionando o deselezionando le colonne desiderate.<P>Le modifiche vengono applicate al tuo account e rimangono attive anche dopo la disconnessione da [!DNL Target]. |
| Caselle di controllo per le operazioni in blocco | Eseguire operazioni in blocco su tutte le attività o sulle attività selezionate.<P>Per un elenco delle azioni disponibili (a seconda delle autorizzazioni e dello stato dell’attività), consulta [Eseguire azioni rapide](#quick-actions) di seguito. |
| [!UICONTROL Type] | Il tipo di attività. Il [!UICONTROL Type] consente di identificare rapidamente ogni attività per tipo. <ul><li>AB-M: manuale [!UICONTROL A/B Test]</li><li>AB-AA: [!UICONTROL Auto-Allocate]</li><li>AB-AT: [!UICONTROL Auto-Target]</li><li>AP: [!UICONTROL Automated Personalization]</li><li>XT: [!UICONTROL Experience Targeting]</li><li>MVT: [!UICONTROL Multivariate Test]</li><li>REC: [!UICONTROL Recommendations]</li></ul>Per ulteriori informazioni su ciascun tipo, consulta [Tipi di attività](#types) di seguito. |
| [!UICONTROL Name] | Nome dell’attività. Fai clic sul nome di un’attività per visualizzarne [!UICONTROL Overview] pagina. <P>Fai clic su **[!UICONTROL Quick Info]** accanto al nome di ogni attività per visualizzare ulteriori informazioni su tale attività in una scheda a comparsa.<p>Fai clic su **[!UICONTROL More actions]** (i puntini di sospensione orizzontali) accanto al nome di ogni attività per aprire un menu che consente di eseguire azioni rapide su un’attività. Sono disponibili le seguenti azioni (a seconda delle autorizzazioni e dello stato dell’attività): [!UICONTROL Edit], [!UICONTROL Activate], [!UICONTROL Deactivate], [!UICONTROL Copy], [!UICONTROL Delete], e [!UICONTROL Archive]. Per ulteriori informazioni su ciascuna azione, consulta [Eseguire azioni rapide](#quick-actions) di seguito.<P>Fai clic sull’intestazione della tabella per ordinare l’elenco in ordine alfabetico in ordine crescente o decrescente per nome. |
| [!UICONTROL Status] | Lo stato dell’attività può essere uno tra i seguenti:<ul><li>**Live**: l’attività è attualmente in esecuzione.</li><li>**Bozza**: la configurazione dell’attività è iniziata, ma l’attività si trova in [modalità bozza](/help/main/c-activities/edit-activity.md) e non è ancora pronto per l’esecuzione.</li><li>**Pianificata**: l’attività è pronta per essere attivata nella data e nell’ora di inizio specificate.</li><li>**Inattiva**: l&#39;attività è stata sospesa o disattivata.</li><li>**Sincronizzazione**: l’attività è stata salvata e viene sincronizzata nel [!DNL Target] rete di consegna.</li><li>**Terminato**: la data e l’ora di fine specificate dell’attività sono state raggiunte e l’attività non viene più distribuita.</li><li>**Archiviata**: l’attività è stata archiviata. È possibile attivare un&#39;attività archiviata per utilizzarla nuovamente.</li></ul>**Nota**: quando esegui determinate azioni, ad esempio l’attivazione di un’attività al di fuori del [!DNL Target] tramite i metodi API, l&#39;aggiornamento può richiedere fino a dieci minuti per propagarsi al [!DNL Target] UI. |
| [!UICONTROL Last Updated] | La data e l’ora dell’ultimo aggiornamento dell’attività, e da chi.<P>Fai clic sull’intestazione della tabella per ordinare l’elenco in ordine crescente o decrescente per data. |
| [!UICONTROL Priority] | La priorità dell’attività.<P>La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.<P>A seconda del [impostazioni](/help/main/administrating-target/reporting.md), il [!DNL Target] Interfaccia utente e opzioni per [!UICONTROL Priority] variare. È possibile utilizzare le impostazioni legacy Bassa, Media o Alta, oppure attivare la priorità precisa da 0 a 999. |
| [!UICONTROL Property] | Mostra la [proprietà](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) per l’attività.<P>Le autorizzazioni per gli utenti Enterprise sono [Target Premium](/help/main/c-intro/intro.md#premium) funzionalità. |
| [!UICONTROL Estimated Lift in Revenue] | Mostra l&#39;aumento previsto dei ricavi se il 100% del pubblico visualizza l&#39;esperienza vincente.<P>È calcolato con la seguente formula:<P>`(<winning experience> - <control experience>)*<total number of visitors>`<P>Se nella forma condensata è presente solo una cifra prima del decimale, il risultato viene arrotondato al massimo a una cifra decimale. Ad esempio: $ 1,6 M, $ 60 K, $ 900, $ 8,5 K, $ 205 K.<P>In questa colonna viene visualizzato “---” per le attività prive di dati sufficienti per richiamare una visualizzazione vincente o prive di un preventivo di spesa.<P>Consulta [Stima dell’incremento dei ricavi](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) per maggiori informazioni. |
| [!UICONTROL Source] | Mostra dove è stata creata l’attività: [!DNL Adobe Target], [API ADOBE TARGET](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html?lang=it), [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html?lang=it), [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=it), o [Adobe Mobile Services](https://developer.adobe.com/client-sdks/documentation/). |
| [!UICONTROL Location] | L’URL dell’attività identifica dove viene visualizzata. Questa colonna consente di identificare rapidamente un’attività e determinare se su una pagina specifica è già in esecuzione un’attività.<P>Se un’attività viene eseguita su più URL, un collegamento mostra il numero di URL utilizzati. Fai clic sul collegamento per visualizzare l’elenco completo degli URL per l’attività.<P>Puoi eseguire ricerche in base all’URL. Utilizza l’elenco a discesa accanto alla casella di ricerca e seleziona [!UICONTROL URL]. |
| Autore | Nome della persona che ha creato l&#39;attività. |
| [!UICONTROL Decisioning Method] | Il metodo decisionale utilizzato in ogni attività: [Lato server](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html?lang=it) o [Lato client](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html). |

## Tipi di attività {#types}

[!DNL Target] include diversi tipi di attività. La tabella seguente fornisce una panoramica di ogni tipo di attività con collegamenti per ulteriori informazioni. Per aiutarti a scegliere meglio il tipo di attività migliore, abbiamo anche creato la [Guida alle attività di Adobe Target](/help/main/c-activities/target-activities-guide.md).

| Tipo di attività | Descrizione |
|--- |--- |
| [Test A/B](/help/main/c-activities/t-test-ab/test-ab.md) | Il test A/B confronta due o più versioni del contenuto del sito web per vedere quale versione migliora meglio le conversioni durante un periodo di test pre-specificato. |
| [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | [!UICONTROL Auto-Allocate], un tipo di test A/B, identifica un vincitore tra due o più esperienze e ridistribuisce automaticamente più traffico per aumentare le conversioni, mentre il test continua a essere eseguito e ad apprendere. |
| [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md)<P>![Target Premium](/help/main/assets/premium.png) | La funzione Targeting automatico, un tipo di test A/B, utilizza l’apprendimento automatico avanzato per identificare più esperienze ad alte prestazioni definite dall’addetto al marketing. Inoltre, indica l’esperienza più adatta per ogni visitatore in base al profilo del singolo cliente e al comportamento dei visitatori precedenti con profili simili, per personalizzare contenuti e favorire le conversioni. |
| [Test multivariato](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | [!UICONTROL Multivariate Testing] (MVT) confronta le combinazioni di offerte negli elementi di una pagina per determinare quale combinazione funziona meglio per un pubblico specifico e identifica quale elemento influisce maggiormente sul successo dell’attività. |
| [Targeting esperienza](/help/main/c-activities/t-experience-target/experience-target.md) | [!UICONTROL Experience Targeting] (XT) fornisce contenuti a un pubblico specifico sulla base di una serie di regole e criteri definiti dall’addetto al marketing. |
| [Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/automated-personalization.md)<P>![Target Premium](/help/main/assets/premium.png) | [!UICONTROL Automated Personalization] (AP) combina offerte o messaggi e utilizza l’apprendimento automatico avanzato per abbinare diverse varianti a ciascun visitatore in base al suo profilo cliente, per personalizzare i contenuti e favorire le conversioni. |
| [Raccomandazioni](/help/main/c-recommendations/recommendations.md)<P>![Target Premium](/help/main/assets/premium.png) | Un consiglio determina in che modo un prodotto viene suggerito a un visitatore del sito web, in base alle sue attività sul sito.<P>Ad esempio, potrebbe essere utile incoraggiare l&#39;acquirente di uno zaino a considerare l&#39;acquisto di scarpe e bastoncini da trekking. Puoi creare un consiglio che mostra gli elementi spesso acquistati insieme con l&#39;algoritmo “Chi ha acquistato questo ha acquistato anche”. Oppure, potresti voler incoraggiare i visitatori a trascorrere più tempo sul sito multimediale consigliando video simili al video che stanno guardando, utilizzando l’algoritmo &quot;Persone che hanno visualizzato questo hanno visualizzato quello&quot;.<P>**NOTA**: puoi anche includere i consigli in [!UICONTROL A/B Test], [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], e [!UICONTROL Experience Targeting] (XT) attività. Per ulteriori informazioni, consulta [Consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md). Questa funzionalità richiede una [licenza di Target Premium](/help/main/c-intro/intro.md#premium). |

## Applicare i filtri all’elenco Attività {#filters}

Accedere ai filtri facendo clic sul pulsante **[!UICONTROL Show Filters]** nella parte superiore dell’elenco.

![Opzioni filtro](/help/main/c-activities/assets/show-filters-options.png)

Il menu consente di filtrare le attività in base ai seguenti attributi: Attributo|Dettagli| | — | — | |[!UICONTROL Type]|Filtra per [tipo di attività](#types).| |[!UICONTROL Status]|Filtra per stato attività.| |[!UICONTROL Reporting Source]|Filtrare in base all&#39;origine per la generazione di rapporti.<ul><li>[[!DNL Analytics]](/help/main/c-integrating-target-with-mac/a4t/a4t.md): visualizza le attività che utilizzano [!UICONTROL Analytics for Target] (A4T) come origine per la generazione di rapporti.</li><li>[[!DNL Target]](/help/main/c-reports/reports.md): visualizza le attività che utilizzano [!DNL Target] come origine per la generazione di rapporti.</li><li>[[!DNL Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md): visualizza le attività che utilizzano [!DNL Adobe Customer Analytics] come origine per la generazione di rapporti.</li></ul>| |[!UICONTROL Experience Composer]|Filtro in base al quale il compositore esperienza è stato utilizzato durante la creazione dell&#39;attività:<ul><li>[Visivo](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md): visualizza le attività create utilizzando [!UICONTROL Visual Experience Composer] (VEC).</li><li>[Basato su modulo](/help/main/c-experiences/form-experience-composer.md): visualizza le attività create utilizzando [!UICONTROL Form-Based Experience Composer].</li></ul>| |[!UICONTROL Metrics Type]|Filtro in base al quale [metrica di successo](/help/main/c-activities/r-success-metrics/success-metrics.md) è stato scelto durante la creazione dell’attività.<ul><li>Conversione</li><li>Ricavi</li><li>Coinvolgimento</li></ul>| |[!UICONTROL Decisioning Method]|Filtrare in base al metodo decisionale utilizzato in ogni attività<ul><li>[Lato server](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html?lang=it): visualizza le attività che utilizzano il decisioning lato server.</li><li>[Lato client](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html): visualizza le attività che utilizzano decisioni lato client.</li></ul>| |[!UICONTROL Activity Source]|Filtra in base all&#39;origine dell&#39;attività utilizzata per creare ogni attività.<ul><li>[!DNL Adobe Target]</li><li>[API ADOBE TARGET](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html?lang=it)</li><li>[Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html?lang=it)</li><li>[Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=it)</li><li>[Adobe Mobile Services](https://developer.adobe.com/client-sdks/documentation/)</li></ul>| |[!UICONTROL Property]|Filtra per [proprietà](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) in cui è stata creata l&#39;attività.|

## Eseguire azioni rapide {#quick-actions}

Fai clic su **[!UICONTROL More actions]** (i puntini di sospensione orizzontali) accanto al nome di ogni attività per aprire un menu che consente di eseguire azioni rapide su un’attività.

![Opzioni azioni rapide](/help/main/c-activities/assets/quick-actions.png)

Sono disponibili le seguenti azioni (a seconda delle autorizzazioni e dello stato dell’attività):

| Azione | Descrizione |
| --- | --- |
| [!UICONTROL Edit] | Modifica l&#39;attività. Qualsiasi attività può essere modificata.<P>Per ulteriori informazioni su come modificare le attività, consulta [Modificare un’attività o salvarla come bozza](/help/main/c-activities/edit-activity.md). |
| [!UICONTROL Deactivate] | Interrompe un&#39;attività in esecuzione o pianificata. Un’attività disattivata può essere riattivata o archiviata.<P>Se disattivi o archivi un’attività e poi la riattivi in un secondo momento, un visitatore continuerà a esserne parte dopo la riattivazione se vi partecipava prima che fosse disattivata o archiviata. Ogni metrica di conversione registrata durante il periodo trascorso tra i due eventi non verrà attribuita a quell’attività. |
| [!UICONTROL Activate] | Avvia un’attività inattiva o pronta per essere attivata. |
| [!UICONTROL Archive] | Invia l&#39;attività all&#39;archivio. Per impostazione predefinita, le attività archiviate non vengono più visualizzate nel [!UICONTROL Activities] elenco. Per includere nell’elenco anche le attività archiviate, devi cambiare il filtro per l&#39;elenco delle attività. È possibile attivare un&#39;attività archiviata per utilizzarla nuovamente.<P>Se disattivi o archivi un’attività e poi la riattivi in un secondo momento, un visitatore continuerà a esserne parte dopo la riattivazione se si trovava in tale attività prima che fosse disattivata o archiviata. Ogni metrica di conversione registrata durante il periodo trascorso tra i due eventi non verrà attribuita a quell’attività. |
| [!UICONTROL Copy] | Copia un&#39;attività. Qualsiasi attività può essere copiata. Quando si copia un&#39;attività viene creata una nuova attività con lo stesso nome e la dicitura “Copia”. Ad esempio, la copia di un test denominato “Offerte browser” sarà denominata “Copia Offerte browser”.<P>Le offerte visive vengono copiate con l&#39;attività. È possibile modificare in modo sicuro le offerte nella copia senza influire sull&#39;attività originale. L&#39;unica eccezione sono le offerte e le immagini salvate nella cartella Contenuto/Risorse. |
| [!UICONTROL Delete] | Elimina una bozza o un’attività.<P>**NOTA**: non è possibile recuperare le attività eliminate. A meno che tu non sia sicuro che questa attività non sarà mai più necessaria, utilizza [!UICONTROL Archive] azione. Se necessario, puoi quindi riattivare l’attività. |

## Considerazioni

Tieni presente i seguenti dettagli sulla [!UICONTROL Activity] elenco:

* Le attività archiviate e terminate non vengono visualizzate nel [!UICONTROL Activities] elenco. Per visualizzare queste attività, filtrale utilizzando [Icona Filtri](#filters) nella parte superiore dell’elenco.
* Quando un’attività è stata originariamente creata in [!DNL Target Classic] viene disattivato o eliminato, viene eliminato da [!DNL Target Standard/Premium]. Attività eliminate originariamente create in [!DNL Target Classic] non vengono inviate al [!UICONTROL Archive] cartella in [!DNL Target Standard/Premium]. La funzionalità di cartella archiviata è applicabile solo alle attività create in [!DNL Target Standard/Premium].
* Tutti i tipi di attività diversi da [!UICONTROL Automated Personalization] AP) [!UICONTROL Auto-Allocate], e [!UICONTROL Auto-Target] consente di scegliere tra [!DNL Target] o [!DNL Adobe Analytics] come origine di dati. [!UICONTROL AP], [!UICONTROL Auto-Allocate], e [!UICONTROL Auto-Target] *sempre* utilizzare [!DNL Target] dati.
* Le attività sono disponibili per diversi canali:

   * Siti web e mobili
   * Schermi e dispositivi collegati a Internet, inclusi chioschi e sportelli automatici
   * Email e altri canali di acquisizione o siti partner
   * App mobili
   * In qualsiasi altro luogo sia possibile fornire contenuti con tag

## Limitazioni  {#section_049D4684403A4E07B998067EB8E9BE56}

Ogni attività di Target presenta le seguenti limitazioni di contenuto:

| Elemento | Limite |
|--- |--- |
| Selettori univoci | 300 se un selettore viene ripetuto in un’esperienza diversa, viene conteggiato una volta. Tuttavia, se si ripete nella stessa esperienza, viene conteggiato nuovamente. |
| Offerte in ogni esperienza | 350 |
| Selettori di tracciamento dei clic nelle metriche | 50 |
| Mbox nelle metriche | 50 |
| Tipi di pubblico e posizioni | 50 combinazioni di pubblico e posizioni (mbox) non devono essere più di 50. |

L’attività non può essere salvata se superi uno di questi limiti.

L’aumento del numero di questi elementi nell’attività aumenta anche il tempo necessario per sincronizzare l’attività tra [!DNL Target].

Per limiti aggiuntivi della V[!UICONTROL isual Experience Composer] VEC, vedi [Limitazioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721).

## Attributi importati in [!DNL Target] per le attività aggiornate al di fuori di [!DNL Target] {#section_802B0D174E6A44E1A96F404CA81AAE44}

Se le attività sono state create in [!DNL Target] sono aggiornati dall&#39;esterno di [!DNL Target] (ad esempio, tramite API), i seguenti attributi di attività vengono importati nuovamente in [!DNL Target]: `thirdpartyId`, `startDate`, `endDate`, `status`, `priority`, e `marketingCloudMetadata(remoteModifiedBy)`.

Questo processo di importazione viene eseguito all’apertura della pagina attività, con un ritardo massimo di dieci minuti.

## Video di formazione {#section_BE80D13A2E81460C885F902010E1AD87}

Il video seguente contiene ulteriori informazioni sui concetti descritti in questo articolo.

### Tipi di attività (9:03)

Questo video spiega i tipi di attività disponibili in [!DNL Target Standard/Premium].

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/17386)

