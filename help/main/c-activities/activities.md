---
keywords: elenco attività;attività;tipi di attività;modificare attività;azioni attività;attributo attività;filtro elenco attività;limitazioni attività;personalizzare;personalizzazione;elenco attività;activity list;activities types;edit activity;actions;activity attribute;activity list filter;activity limits;personalization
description: Personalizza contenuti e progetti di pagine di prova per tipi di pubblico specifici con [!DNL Adobe Target] attività.
title: Come posso personalizzare il contenuto e testare le progettazioni di pagine con  [!DNL Target]?
feature: Activities
exl-id: 7e61525d-b2db-44f6-a7c2-df5a8d28eca2
source-git-commit: c445775bc96623f9742f648a82ed9b4e64bd463a
workflow-type: tm+mt
source-wordcount: '2291'
ht-degree: 25%

---

# Panoramica sulle attività

Personalizzare contenuti e progettazioni di pagine di prova per tipi di pubblico specifici con [!DNL Adobe Target] attività.

Ad esempio, puoi progettare un’attività che sottopone a test due diverse pagine di destinazione, una con informazioni in evidenza sulle scarpe estive da donna e un’altra con abbigliamento estivo generico. L’attività determina le condizioni che controllano quando ciascuna di queste pagine di destinazione viene visualizzata e le metriche che determinano quale pagina ha più successo. L’attività è configurata per iniziare e terminare quando vengono soddisfatte determinate condizioni, ad esempio tra date specifiche. Oppure puoi scegliere di iniziare quando l’attività viene approvata e di terminare quando viene disattivata.

Pianifica con attenzione durante la progettazione di una attività. Determina quando deve iniziare l’attività e per quanto tempo dura. Quindi, crea un elenco delle offerte e assegna un tipo di pubblico a ciascuna.

## Elenco attività {#section_DE8E2DB30D534962A931EF8BB48240F5}

L&#39;elenco [!UICONTROL Activities] è la visualizzazione predefinita all&#39;apertura di [!DNL Target]. Puoi creare attività da questa pagina e gestire quelle esistenti.

È inoltre possibile visualizzare l&#39;elenco [!UICONTROL Activities] facendo clic sulla scheda [!UICONTROL Activities] nella parte superiore dell&#39;interfaccia utente [!DNL Target].

L&#39;elenco [!UICONTROL Activities] fornisce una panoramica di tutte le attività nell&#39;implementazione di [!DNL Target] e consente di eseguire varie azioni.

La tabella seguente consente di comprendere vari elementi dell&#39;elenco [!UICONTROL Activities] nell&#39;interfaccia utente [!DNL Target]:

| Elemento | Descrizione |
|--- |--- |
| Icona [!UICONTROL Show filters]<P>![Icona Mostra filtri](/help/main/assets/icons/Filter.svg) | Per accedere ai filtri, fai clic sull&#39;icona **[!UICONTROL Show Filters]** nella parte superiore dell&#39;elenco per filtrare le attività in base a [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], [!UICONTROL Decisioning Source], [!UICONTROL Activity Source] e [!UICONTROL Properties].<P>I filtri configurati rimangono invariati nella sessione corrente.<P>Per ulteriori informazioni, vedere [Applica filtri all&#39;elenco [!UICONTROL Activities]](#filters) di seguito. |
| Cerca campo | Trovare rapidamente un&#39;attività o ridurre il numero di attività visualizzate nell&#39;elenco [!UICONTROL Activity]. È possibile eseguire ricerche per [!UICONTROL Activity Name], [!UICONTROL URL] o [!UICONTROL ID] utilizzando il menu a discesa.<P>Le opzioni di ricerca configurate sono permanenti nella sessione corrente. |
| [!UICONTROL Create Activity] | Crea un’attività.<P>Per ulteriori informazioni sulla creazione dei vari tipi di attività, consulta: <ul><li>[Crea un&#39;attività [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)</li><li>[Crea un&#39;attività [!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md)</li><li>[Crea un&#39;attività [!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/create-auto-target.md)</li><li>[Crea un&#39;attività [!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)</li><li>[Crea un&#39;attività [!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md)</li><li>[Crea un&#39;attività](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md)</li><li>[Crea un&#39;attività [!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)</li></ul>Per ulteriori informazioni su ciascun tipo, vedi [Tipi di attività](#types) di seguito. |
| [!UICONTROL Create mobile preview link]<P>![Menu altre azioni](/help/main/assets/icons/MoreVertical.svg) | Utilizza i [collegamenti di anteprima per dispositivi mobili](https://experienceleague.adobe.com/en/docs/target-dev/developer/mobile-apps/target-mobile-preview) per eseguire un controllo qualità end-to-end semplice per le attività delle app mobili.<P>Fai clic sull&#39;icona **Altre opzioni**, seleziona il **Crea collegamento di anteprima mobile**, quindi scegli le attività da testare su dispositivi mobili. |
| Personalizza tabella<P>![Icona Personalizza tabella](/help/main/assets/icons/ColumnSetting.svg) | Modificare le colonne visualizzate nell&#39;elenco [!UICONTROL Activity] facendo clic sull&#39;icona **[!UICONTROL Customize Table]** in alto a destra della pagina, quindi selezionando o deselezionando le colonne desiderate.<P>Le modifiche vengono applicate al tuo account e rimangono attive anche dopo la disconnessione da [!DNL Target]. |
| Caselle di controllo per le operazioni in blocco<P>![Icona Operazioni in blocco](/help/main/assets/icons/Rectangle.svg) | Eseguire operazioni in blocco su tutte le attività o sulle attività selezionate.<P>Per un elenco delle azioni disponibili (a seconda delle autorizzazioni e dello stato dell&#39;attività), consulta [Eseguire azioni rapide](#quick-actions) di seguito. |
| [!UICONTROL Type] | Il tipo di attività. La colonna [!UICONTROL Type] consente di identificare rapidamente ogni attività per tipo. <ul><li>**AB-M**: manuale [!UICONTROL A/B Test]</li><li>**AB-AA**: [!UICONTROL Auto-Allocate]</li><li>**AB-AT**: [!UICONTROL Auto-Target]</li><li>**AP**: [!UICONTROL Automated Personalization]</li><li>**XT**: [!UICONTROL Experience Targeting]</li><li>**MVT**: [!UICONTROL Multivariate Test]</li><li>**REC**: [!UICONTROL Recommendations]</li></ul>Per ulteriori informazioni su ciascun tipo, vedi [Tipi di attività](#types) di seguito. |
| [!UICONTROL Name] | Nome dell’attività. Fai clic sull&#39;icona **[!UICONTROL Quick Info]** ( ![icona Informazioni rapide](/help/main/assets/icons/InfoOutline.svg) ) accanto al nome di ogni attività per visualizzare ulteriori informazioni su tale attività in una scheda a comparsa, inclusi [!UICONTROL Activity ID], [!UICONTROL Activity Objective], [!UICONTROL Activity Location], [!UICONTROL Goal] e [!UICONTROL Status].<P>Fai clic sull&#39;icona **[!UICONTROL More actions]** ( ![Icona Altre azioni](/help/main/assets/icons/MoreSmallList.svg) ) accanto al nome di ogni attività per aprire un menu che consente di eseguire azioni rapide su un&#39;attività. Sono disponibili le azioni seguenti (a seconda delle autorizzazioni e dello stato dell&#39;attività): [!UICONTROL Edit], [!UICONTROL Activate], [!UICONTROL Deactivate], [!UICONTROL Copy], [!UICONTROL Delete] e [!UICONTROL Archive].<P>Per ulteriori informazioni su ciascuna azione, vedere [Eseguire azioni rapide](#quick-actions) di seguito.<P>Fai clic sull’intestazione della tabella per ordinare l’elenco in ordine alfabetico in ordine crescente o decrescente per nome. |
| [!UICONTROL Status] | Lo stato dell’attività può essere uno tra i seguenti:<ul><li>**[!UICONTROL Live]**: l&#39;attività è attualmente in esecuzione.</li><li>**[!UICONTROL Scheduled]**: l&#39;attività è pronta per essere attivata quando arrivano la data e l&#39;ora di inizio specificate.</li><li>**[!UICONTROL Inactive]**: l&#39;attività è stata sospesa o disattivata.</li><li>**[!UICONTROL Ended]**: la data e l&#39;ora di fine specificate dell&#39;attività sono state raggiunte e l&#39;attività non verrà più distribuita.</li><li>**[!UICONTROL Archived]**: attività archiviata. È possibile attivare un&#39;attività archiviata per utilizzarla nuovamente.</li></ul>**Nota**: quando esegui determinate azioni, ad esempio l&#39;attivazione di un&#39;attività al di fuori dell&#39;interfaccia utente di [!DNL Target] utilizzando i metodi API, l&#39;aggiornamento può richiedere fino a dieci minuti per propagarsi all&#39;interfaccia utente di [!DNL Target]. |
| [!UICONTROL Last Updated] | La data e l’ora dell’ultimo aggiornamento dell’attività, e da chi.<P>Fai clic sull’intestazione della tabella per ordinare l’elenco in ordine crescente o decrescente per data. |
| [!UICONTROL Priority] | La priorità dell’attività.<P>La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.<P>A seconda delle [impostazioni](/help/main/administrating-target/reporting.md), l&#39;interfaccia utente di [!DNL Target] e le opzioni per [!UICONTROL Priority] variano. È possibile utilizzare le impostazioni legacy di [!UICONTROL Low], [!UICONTROL Medium] o [!UICONTROL High] oppure abilitare le priorità precise da 0 a 999.<P>Per ulteriori informazioni sulle impostazioni di priorità, vedere [Priorità](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#section_DCBDC354261F420EBD4B43EA34947BAC) in *Impostazioni attività* in *Obiettivi e impostazioni*. |
| [!UICONTROL Property] | Mostra la [proprietà](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) per l’attività.<P>Le autorizzazioni per gli utenti Enterprise sono una funzionalità di [Target Premium](/help/main/c-intro/intro.md#premium). |
| [!UICONTROL Estimated Lift in Revenue] | Mostra l&#39;aumento previsto dei ricavi se il 100% del pubblico visualizza l&#39;esperienza vincente.<P>È calcolato con la seguente formula:<P>`(<winning experience> - <control experience>)*<total number of visitors>`<P>Se nella forma condensata è presente solo una cifra prima del decimale, il risultato viene arrotondato al massimo a una cifra decimale. Ad esempio: $ 1,6 M, $ 60 K, $ 900, $ 8,5 K, $ 205 K.<P>In questa colonna viene visualizzato “---” per le attività prive di dati sufficienti per richiamare una visualizzazione vincente o prive di un preventivo di spesa.<P>Consulta [Stima dell’incremento dei ricavi](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) per maggiori informazioni. |
| [!UICONTROL Source] | Mostra dove è stata creata l&#39;attività: [!DNL Adobe Target], [API Adobe Target](https://experienceleague.adobe.com/en/docs/target-dev/developer/overview), [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html?lang=it), [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=it) o [Adobe Mobile Services](https://developer.adobe.com/client-sdks/documentation/). |
| [!UICONTROL Author] | Nome della persona che ha creato l&#39;attività. |
| [!UICONTROL Decisioning Method] | Il metodo decisionale utilizzato in ogni attività: [Lato server](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html?lang=it) o [Lato client](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html). |

<!--|[!UICONTROL Location]|The URL for the activity identifies where the activity is displayed. This column helps you quickly identify an activity and determine whether a particular page already has an activity running on it.<P>If an activity runs on multiple URLs, a link shows how many more URLs are used. Click the link to view the complete list of URLs for that activity.<P>You can search based on the URL. Use the drop-down list next to the search box and select [!UICONTROL URL].|-->

## Tipi di attività {#types}

[!DNL Target] include diversi tipi di attività. La tabella seguente fornisce una panoramica di ogni tipo di attività con collegamenti per ulteriori informazioni. Per aiutarti a scegliere meglio il tipo di attività migliore, utilizza la [Guida alle attività di Adobe Target](/help/main/c-activities/target-activities-guide.md).

| Tipo di attività | Descrizione |
|--- |--- |
| [[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md) | Il test A/B confronta due o più versioni del contenuto del sito web per vedere quale versione migliora meglio le conversioni durante un periodo di test pre-specificato. |
| [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | [!UICONTROL Auto-Allocate], un tipo di test A/B, identifica un vincitore tra due o più esperienze e ridistribuisce automaticamente più traffico per aumentare le conversioni, mentre il test continua a essere eseguito e ad apprendere. |
| [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)<P>![Target Premium](/help/main/assets/premium.png) | La funzione Targeting automatico, un tipo di test A/B, utilizza l’apprendimento automatico avanzato per identificare più esperienze ad alte prestazioni definite dall’addetto al marketing. Inoltre, indica l’esperienza più adatta per ogni visitatore in base al profilo del singolo cliente e al comportamento dei visitatori precedenti con profili simili, per personalizzare contenuti e favorire le conversioni. |
| [[!UICONTROL Multivariate Test]](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | [!UICONTROL Multivariate Testing] (MVT) confronta le combinazioni di offerte negli elementi di una pagina per determinare quale combinazione funziona meglio per un pubblico specifico e identifica quale elemento influisce maggiormente sul successo dell&#39;attività. |
| [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) | [!UICONTROL Experience Targeting] (XT) fornisce contenuti a un pubblico specifico in base a una serie di regole e criteri definiti dall&#39;addetto al marketing. |
| [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md)<P>![Target Premium](/help/main/assets/premium.png) | [!UICONTROL Automated Personalization] (AP) combina offerte o messaggi e utilizza l&#39;apprendimento automatico avanzato per abbinare diverse varianti a ciascun visitatore in base al suo profilo cliente, per personalizzare i contenuti e favorire le conversioni. |
| [[!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)<P>![Target Premium](/help/main/assets/premium.png) | Un consiglio determina in che modo un prodotto viene suggerito a un visitatore del sito web, in base alle sue attività sul sito.<P>Ad esempio, potrebbe essere utile incoraggiare l&#39;acquirente di uno zaino a considerare l&#39;acquisto di scarpe e bastoncini da trekking. Puoi creare un consiglio che mostra gli elementi spesso acquistati insieme con l&#39;algoritmo “Chi ha acquistato questo ha acquistato anche”. Oppure, potresti voler incoraggiare i visitatori a trascorrere più tempo sul sito multimediale consigliando video simili al video che stanno guardando, utilizzando l’algoritmo &quot;Persone che hanno visualizzato questo hanno visualizzato quello&quot;.<P>**NOTA**: è inoltre possibile includere i consigli nelle attività [!UICONTROL A/B Test], [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target] e [!UICONTROL Experience Targeting] (XT). Per ulteriori informazioni, consulta [Consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md). Questa funzionalità richiede una [licenza di Target Premium](/help/main/c-intro/intro.md#premium). |

## Applicare i filtri all’elenco Attività {#filters}

Per accedere ai filtri, fai clic sull&#39;icona **[!UICONTROL Show Filters]** ( ![icona Mostra filtri](/help/main/assets/icons/Filter.svg) ) nella parte superiore dell&#39;elenco.

Il menu consente di filtrare le attività in base ai seguenti attributi:

| Attributo | Dettagli |
| --- | --- |
| [!UICONTROL Type] | Filtra per [tipo di attività](#types). |
| [!UICONTROL Status] | Filtra per stato attività.<ul><li>**[!UICONTROL Live]**: l&#39;attività è attualmente in esecuzione.</li><li>**[!UICONTROL Scheduled]**: l&#39;attività è pronta per essere attivata quando arrivano la data e l&#39;ora di inizio specificate.</li><li>**[!UICONTROL Inactive]**: l&#39;attività è stata sospesa o disattivata.</li><li>**[!UICONTROL Ended]**: la data e l&#39;ora di fine specificate dell&#39;attività sono state raggiunte e l&#39;attività non verrà più distribuita.</li><li>**[!UICONTROL Archived]**: attività archiviata. È possibile attivare un&#39;attività archiviata per utilizzarla nuovamente.</li></ul>Per ulteriori informazioni sugli stati obsoleti di [!UICONTROL Save as Draft] e [!UICONTROL Syncing], consulta la nota sotto questa tabella. |
| [!UICONTROL Reporting Source] | Filtra per origine di reporting.<ul><li>[[!DNL Analytics]](/help/main/c-integrating-target-with-mac/a4t/a4t.md): visualizza le attività che utilizzano [!UICONTROL Analytics for Target] (A4T) come origine per la generazione di rapporti.</li><li>[[!DNL Target]](/help/main/c-reports/reports.md): visualizza le attività che utilizzano [!DNL Target] come origine per la generazione di rapporti.</li><li>[[!DNL Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md): visualizza le attività che utilizzano [!DNL Adobe Customer Analytics] come origine per la generazione di rapporti.</li></ul> |
| [!UICONTROL Experience Composer] | Filtro in base al quale il compositore esperienza è stato utilizzato durante la creazione dell’attività:<ul><li>[Visivo](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md): visualizza le attività create utilizzando [!UICONTROL Visual Experience Composer] (VEC).</li><li>[Basato su modulo](/help/main/c-experiences/form-experience-composer.md): visualizza le attività create utilizzando [!UICONTROL Form-Based Experience Composer].</li></ul> |
| [!UICONTROL Metrics Type] | Filtro in base al quale [metrica di successo](/help/main/c-activities/r-success-metrics/success-metrics.md) è stata scelta durante la creazione dell&#39;attività.<ul><li>[!UICONTROL Conversion]</li><li>[!UICONTROL Revenue]</li><li>[!UICONTROL Engagement]</li><li>[!UICONTROL Use an Analytics metric]</lI></ul> |
| [!UICONTROL Decisioning Method] | Filtra in base al metodo decisionale utilizzato in ogni attività.<ul><li>[Lato server](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html?lang=it): visualizza le attività che utilizzano le decisioni lato server.</li><li>[Lato client](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html): visualizza le attività che utilizzano le decisioni lato client.</li></ul> |
| [!UICONTROL Activity Source] | Filtra in base all’origine dell’attività utilizzata per creare ogni attività.<ul><li>[!DNL Adobe Target]</li><li>[[!DNL Adobe Target] API](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html?lang=it)</li><li>[[!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/docs/experience-platform.html?lang=it)</li><li>[[!DNL Adobe Experience Manager]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=it)</li><li>[[!DNL Adobe Mobile Services]](https://developer.adobe.com/client-sdks/home/)</li></ul> |
| [!UICONTROL Property] | Filtra in base alla [proprietà](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) in cui è stata creata l&#39;attività. |


>[!NOTE]
>
>**Aggiornamento sugli stati attività nell&#39;interfaccia utente aggiornata**: con gli ultimi aggiornamenti all&#39;interfaccia utente, gli stati [!UICONTROL Save as Draft] e [!UICONTROL Syncing] non sono più disponibili. Questo perché tutte le attività di creazione e modifica ora vengono eseguite direttamente nel sistema di consegna [!DNL Target] del back-end utilizzando il livello GraphQL, garantendo un processo più semplice ed efficiente.
>
>In precedenza, le attività venivano salvate nell&#39;interfaccia utente [!DNL Target] e quindi sincronizzate nel sistema di consegna [!DNL Target], che richiedeva tali stati intermedi. Poiché non è più così, questi stati sono stati rimossi.
>
>[!DNL Adobe] ha capito che alcuni clienti hanno espresso interesse per la funzione [!UICONTROL Save as Draft]. Pur apprezzando questo feedback, al momento questa funzionalità non è supportata.

## Eseguire azioni rapide {#quick-actions}

Fai clic sull&#39;icona **[!UICONTROL More actions]** ( ![Menu altre azioni](/help/main/assets/icons/MoreVertical.svg) ) accanto al nome di ogni attività per aprire un menu che consente di eseguire azioni rapide su un&#39;attività.

Sono disponibili le seguenti azioni (a seconda delle autorizzazioni e dello stato dell’attività):

| Azione | Descrizione |
| --- | --- |
| [!UICONTROL Edit] | Modifica l&#39;attività. Qualsiasi attività può essere modificata.<P>Per ulteriori informazioni sulle diverse modalità di modifica delle attività, vedere [Modificare un&#39;attività o salvarla come bozza](/help/main/c-activities/edit-activity.md). |
| [!UICONTROL Deactivate] | Interrompe un&#39;attività in esecuzione o pianificata. Un’attività disattivata può essere riattivata o archiviata.<P>Se disattivi o archivi un’attività e poi la riattivi in un secondo momento, un visitatore continuerà a esserne parte dopo la riattivazione se vi partecipava prima che fosse disattivata o archiviata. Ogni metrica di conversione registrata durante il periodo trascorso tra i due eventi non verrà attribuita a quell’attività. |
| [!UICONTROL Activate] | Avvia un’attività inattiva o pronta per essere attivata. |
| [!UICONTROL Archive] | Invia l&#39;attività all&#39;archivio. Per impostazione predefinita, le attività archiviate non vengono più visualizzate nell&#39;elenco [!UICONTROL Activities]. Modificare il filtro per l&#39;elenco [!UICONTROL Activities] in modo da includere le attività archiviate per visualizzarle. È possibile attivare un&#39;attività archiviata per utilizzarla nuovamente.<P>Se disattivi o archivi un’attività e poi la riattivi in un secondo momento, un visitatore continuerà a esserne parte dopo la riattivazione se si trovava in tale attività prima che fosse disattivata o archiviata. Ogni metrica di conversione registrata durante il periodo trascorso tra i due eventi non verrà attribuita a quell’attività. |
| [!UICONTROL Copy] | Copia un&#39;attività. Qualsiasi attività può essere copiata. Quando si copia un&#39;attività viene creata una nuova attività con lo stesso nome e la dicitura “Copia”. Ad esempio, la copia di un test denominato “Offerte browser” sarà denominata “Copia Offerte browser”.<P>Le offerte visive vengono copiate con l&#39;attività. È possibile modificare in modo sicuro le offerte nella copia senza influire sull&#39;attività originale. L&#39;unica eccezione sono le offerte e le immagini salvate nella cartella Contenuto/Risorse. |
| [!UICONTROL Delete] | Elimina una bozza o un’attività.<P>**NOTA**: non è possibile recuperare le attività eliminate. A meno che tu non sia sicuro che questa attività non sarà mai più necessaria, utilizza l&#39;azione [!UICONTROL Archive]. Se necessario, puoi quindi riattivare l’attività. |

## Considerazioni

Osservare i dettagli seguenti sull&#39;elenco [!UICONTROL Activity]:

* Le attività [!UICONTROL Archived] e [!UICONTROL Ended] non vengono visualizzate nell&#39;elenco [!UICONTROL Activities]. Per visualizzare queste attività, filtrale utilizzando l&#39;icona [Filtri](#filters) ( ![Mostra icona Filtri](/help/main/assets/icons/Filter.svg) ) nella parte superiore dell&#39;elenco.
* Quando un&#39;attività originariamente creata in [!DNL Target Classic] viene disattivata o eliminata, viene eliminata da [!DNL Target Standard/Premium]. Le attività eliminate originariamente create in [!DNL Target Classic] non vengono inviate alla cartella [!UICONTROL Archive] in [!DNL Target Standard/Premium]. La funzionalità di cartella archiviata è applicabile solo alle attività create in [!DNL Target Standard/Premium].
* Tutti i tipi di attività diversi da [!UICONTROL Automated Personalization] (AP), [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target] consentono di scegliere se utilizzare [!DNL Target] o [!DNL Adobe Analytics] come origine dati. [!UICONTROL Automated Personalization], [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target] *utilizza sempre* dati [!DNL Target].
* Le attività sono disponibili per diversi canali:

   * Siti web e mobili
   * Schermi e dispositivi collegati a Internet, inclusi chioschi e sportelli automatici
   * Email e altri canali di acquisizione o siti partner
   * App mobili
   * In qualsiasi altro luogo sia possibile fornire contenuti con tag

## Limitazioni  {#section_049D4684403A4E07B998067EB8E9BE56}

Ogni attività [!DNL Target] presenta le seguenti limitazioni di contenuto:

| Elemento | Limite |
|--- |--- |
| Selettori univoci | 300 se un selettore viene ripetuto in un’esperienza diversa, viene conteggiato una volta. Tuttavia, se si ripete nella stessa esperienza, viene conteggiato nuovamente. |
| Offerte in ogni esperienza | 350 |
| Selettori di tracciamento dei clic nelle metriche | 50 |
| Mbox nelle metriche | 50 |
| Tipi di pubblico e posizioni | 50 combinazioni di pubblico e posizioni (mbox) non devono essere più di 50. |

L’attività non può essere salvata se superi uno di questi limiti.

L&#39;aumento del numero di questi elementi nell&#39;attività aumenta anche il tempo necessario per sincronizzare l&#39;attività in [!DNL Target].

Per ulteriori limiti di [!UICONTROL Visual Experience Composer] (VEC), vedi [Limitazioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721).

## Attributi importati in [!DNL Target] per attività aggiornate al di fuori di [!DNL Target] {#section_802B0D174E6A44E1A96F404CA81AAE44}

Se le attività create in [!DNL Target] vengono aggiornate dall&#39;esterno di [!DNL Target] (ad esempio tramite API), i seguenti attributi di attività vengono importati nuovamente in [!DNL Target]: `thirdpartyId`, `startDate`, `endDate`, `status`, `priority` e `marketingCloudMetadata(remoteModifiedBy)`.

Questo processo di importazione viene eseguito all&#39;apertura dell&#39;elenco [!UICONTROL Activities], con un ritardo massimo di dieci minuti.

