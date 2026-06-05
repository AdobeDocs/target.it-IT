---
keywords: elenco attività;attività;tipi di attività;modificare attività;azioni attività;attributo attività;filtro elenco attività;limitazioni attività;personalizzare;personalizzazione;elenco attività;activity list;activities types;edit activity;actions;activity attribute;activity list filter;activity limits;personalization
description: Personalizza contenuti e progetti di pagine di prova per tipi di pubblico specifici con [!DNL Adobe Target] attività.
title: Come posso personalizzare il contenuto e testare le progettazioni di pagine con  [!DNL Target]?
feature: Activities
exl-id: 7e61525d-b2db-44f6-a7c2-df5a8d28eca2
TQID: https://experienceleague.adobe.com/q3-Z8r2eEWTISBkZBBJTJ8XarLi-lTa2qsqj961hhEQ
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eebid: c93393a4-e558-47e1-992e-c91ed4d480ce
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 2633
ht-degree: 25%

---

# Panoramica sulle attività

Personalizzare contenuti e progettazioni di pagine di prova per tipi di pubblico specifici con [!DNL Adobe Target] attività.

Ad esempio, puoi progettare un’attività che sottopone a test due diverse pagine di destinazione, una con informazioni in evidenza sulle scarpe estive da donna e un’altra con abbigliamento estivo generico. L’attività determina le condizioni che controllano quando ciascuna di queste pagine di destinazione viene visualizzata e le metriche che determinano quale pagina ha più successo. L’attività è configurata per iniziare e terminare quando vengono soddisfatte determinate condizioni, ad esempio tra date specifiche. Oppure puoi scegliere di iniziare quando l’attività viene approvata e di terminare quando viene disattivata.

Pianifica con attenzione durante la progettazione di una attività. Determina quando deve iniziare l’attività e per quanto tempo dura. Quindi, crea un elenco delle offerte e assegna un tipo di pubblico a ciascuna.

## Elenco attività {#section_DE8E2DB30D534962A931EF8BB48240F5}

L&#39;elenco [!UICONTROL Attività] è la visualizzazione predefinita all&#39;apertura di [!DNL Target]. Puoi creare attività da questa pagina e gestire quelle esistenti.

Puoi anche visualizzare l&#39;elenco [!UICONTROL Attività] facendo clic sulla scheda [!UICONTROL Attività] nella parte superiore dell&#39;interfaccia utente [!DNL Target].

L&#39;elenco [!UICONTROL Attività] fornisce una panoramica di tutte le attività nell&#39;implementazione di [!DNL Target] e consente di eseguire varie azioni.

La tabella seguente ti aiuta a comprendere vari elementi dell&#39;elenco [!UICONTROL Attività] nell&#39;interfaccia utente [!DNL Target]:

| Elemento | Descrizione |
|--- |--- |
| [!UICONTROL Icona Mostra filtri]<P>![Icona Mostra filtri](/help/main/assets/icons/Filter.svg) | Per accedere ai filtri, fai clic sull&#39;icona **[!UICONTROL Mostra filtri]** nella parte superiore dell&#39;elenco per filtrare le attività in base a [!UICONTROL Tipo], [!UICONTROL Stato], [!UICONTROL Source per la generazione di rapporti], [!UICONTROL Compositore esperienza], [!UICONTROL Tipo di metrica], [!UICONTROL Source per le decisioni], [!UICONTROL Source attività] e [!UICONTROL Proprietà].<P>I filtri configurati rimangono invariati nella sessione corrente.<P>Per ulteriori informazioni, vedere [Applica filtri all&#39;elenco [!UICONTROL Attività]](#filters) di seguito. |
| Cerca campi | Trova rapidamente un&#39;attività o riduci il numero di attività visualizzate nell&#39;elenco [!UICONTROL Attività]. Puoi eseguire ricerche per [!UICONTROL Nome attività], [!UICONTROL URL] o [!UICONTROL ID] utilizzando il menu a discesa.<P>Le opzioni di ricerca configurate sono permanenti nella sessione corrente. |
| [!UICONTROL Crea attività] | Crea un’attività.<P>Per ulteriori informazioni sulla creazione dei vari tipi di attività, consulta: <ul><li>[Crea un&#39;attività [!UICONTROL Test A/B]](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)</li><li>[Crea un&#39;attività [!UICONTROL Allocazione automatica]](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md)</li><li>[Crea un&#39;attività [!UICONTROL Targeting automatico]](/help/main/c-activities/auto-target/create-auto-target.md)</li><li>[Crea un&#39;attività [!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)</li><li>[Crea un&#39;attività [!UICONTROL Targeting esperienze]](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md)</li><li>[Crea un&#39;attività](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md)</li><li>[Creare un&#39;attività [!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)</li></ul>Per ulteriori informazioni su ciascun tipo, vedi [Tipi di attività](#types) di seguito. |
| [!UICONTROL Crea collegamento di anteprima mobile]<P>![Menu altre azioni](/help/main/assets/icons/MoreVertical.svg) | Utilizza i [collegamenti di anteprima per dispositivi mobili](https://experienceleague.adobe.com/en/docs/target-dev/developer/mobile-apps/target-mobile-preview) per eseguire un controllo qualità end-to-end semplice per le attività delle app mobili.<P>Fai clic sull&#39;icona **Altre opzioni**, seleziona il **Crea collegamento di anteprima mobile**, quindi scegli le attività da testare su dispositivi mobili. |
| Personalizza tabella<P>![Icona Personalizza tabella](/help/main/assets/icons/ColumnSetting.svg) | Modifica le colonne da visualizzare nell&#39;elenco [!UICONTROL Attività] facendo clic sull&#39;icona **[!UICONTROL Personalizza tabella]** in alto a destra della pagina, quindi selezionando o deselezionando le colonne desiderate.<P>Le modifiche vengono applicate al tuo account e rimangono attive anche dopo la disconnessione da [!DNL Target]. |
| Caselle di controllo per le operazioni in blocco<P>![Icona Operazioni in blocco](/help/main/assets/icons/Rectangle.svg) | Eseguire operazioni in blocco su tutte le attività o sulle attività selezionate.<P>Per un elenco delle azioni disponibili (a seconda delle autorizzazioni e dello stato dell&#39;attività), consulta [Eseguire azioni rapide](#quick-actions) di seguito. |
| [!UICONTROL Tipo] | Il tipo di attività. La colonna [!UICONTROL Tipo] ti consente di identificare rapidamente ogni attività per tipo. <ul><li>**AB-M**: manuale [!UICONTROL Test A/B]</li><li>**AB-AA**: [!UICONTROL Allocazione automatica]</li><li>**AB-AT**: [!UICONTROL Targeting automatico]</li><li>**AP**: [!UICONTROL Automated Personalization]</li><li>**XT**: [!UICONTROL Targeting esperienza]</li><li>**MVT**: [!UICONTROL Test multivariato]</li><li>**REC**: [!UICONTROL Consigli]</li></ul>Per ulteriori informazioni su ciascun tipo, vedi [Tipi di attività](#types) di seguito. |
| [!UICONTROL Nome] | Il nome dell&#39;attività. Fai clic sull&#39;icona **[!UICONTROL Informazioni rapide]** ( ![Icona Informazioni rapide](/help/main/assets/icons/InfoOutline.svg) ) accanto al nome di ciascuna attività per visualizzare ulteriori informazioni su tale attività in una scheda a comparsa, incluso [!UICONTROL ID attività], [!UICONTROL Obiettivo attività], [!UICONTROL Posizione attività], [!UICONTROL Obiettivo] e [!UICONTROL Stato].<P>Fai clic sull&#39;icona **[!UICONTROL Altre azioni]** ( ![Icona Altre azioni](/help/main/assets/icons/MoreSmallList.svg) ) accanto al nome di ciascuna attività per aprire un menu che consente di eseguire azioni rapide su un&#39;attività. Sono disponibili le seguenti azioni (a seconda delle autorizzazioni e dello stato dell&#39;attività): [!UICONTROL Modifica], [!UICONTROL Attiva], [!UICONTROL Disattiva], [!UICONTROL Copia], [!UICONTROL Elimina] e [!UICONTROL Archivia].<P>Per ulteriori informazioni su ciascuna azione, vedere [Eseguire azioni rapide](#quick-actions) di seguito.<P>Fai clic sull’intestazione della tabella per ordinare l’elenco in ordine alfabetico in ordine crescente o decrescente per nome. |
| [!UICONTROL Stato] | Lo stato dell’attività può essere uno tra i seguenti:<ul><li>**[!UICONTROL Live]**: l&#39;attività è attualmente in esecuzione.</li><li>**[!UICONTROL Pianificato]**: l&#39;attività è pronta per essere attivata alla data e all&#39;ora di inizio specificate.</li><li>**[!UICONTROL Inattiva]**: l&#39;attività è stata sospesa o disattivata.</li><li>**[!UICONTROL Terminata]**: la data e l&#39;ora di fine specificate dell&#39;attività sono state raggiunte e l&#39;attività non verrà più distribuita.</li><li>**[!UICONTROL Archiviata]**: l&#39;attività è stata archiviata. È possibile attivare un&#39;attività archiviata per utilizzarla nuovamente.</li></ul>**Nota**: quando esegui determinate azioni, ad esempio l&#39;attivazione di un&#39;attività al di fuori dell&#39;interfaccia utente di [!DNL Target] utilizzando i metodi API, l&#39;aggiornamento può richiedere fino a dieci minuti per propagarsi all&#39;interfaccia utente di [!DNL Target]. |
| [!UICONTROL Ultimo aggiornamento] | La data e l’ora dell’ultimo aggiornamento dell’attività, e da chi.<P>Fai clic sull’intestazione della tabella per ordinare l’elenco in ordine crescente o decrescente per data. |
| [!UICONTROL Priorità] | La priorità dell’attività.<P>La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.<P>A seconda delle [impostazioni](/help/main/administrating-target/reporting.md), l&#39;interfaccia utente di [!DNL Target] e le opzioni per [!UICONTROL Priorità] variano. Puoi utilizzare le impostazioni legacy di [!UICONTROL Bassa], [!UICONTROL Medium] o [!UICONTROL Alta] oppure abilitare le priorità precise da 0 a 999.<P>Per ulteriori informazioni sulle impostazioni di priorità, vedere [Priorità](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#section_DCBDC354261F420EBD4B43EA34947BAC) in *Impostazioni attività* in *Obiettivi e impostazioni*. |
| [!UICONTROL Proprietà] | Mostra la [proprietà](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) per l’attività.<P>Le autorizzazioni per gli utenti Enterprise sono una funzionalità di [Target Premium](/help/main/c-intro/intro.md#premium). |
| [!UICONTROL Incremento stimato dei ricavi] | Mostra l&#39;aumento previsto dei ricavi se il 100% del pubblico visualizza l&#39;esperienza vincente.<P>È calcolato con la seguente formula:<P>`(<winning experience> - <control experience>)*<total number of visitors>`<P>Se nella forma condensata è presente solo una cifra prima del decimale, il risultato viene arrotondato al massimo a una cifra decimale. Ad esempio: $ 1,6 M, $ 60 K, $ 900, $ 8,5 K, $ 205 K.<P>In questa colonna viene visualizzato “---” per le attività prive di dati sufficienti per richiamare una visualizzazione vincente o prive di un preventivo di spesa.<P>Consulta [Stima dell’incremento dei ricavi](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) per maggiori informazioni. |
| [!UICONTROL Source] | Mostra dove è stata creata l&#39;attività: [!DNL Adobe Target], [API Adobe Target](https://experienceleague.adobe.com/en/docs/target-dev/developer/overview), [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html?lang=it), [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=it) o [Adobe Mobile Services](https://developer.adobe.com/client-sdks/documentation/). |
| [!UICONTROL Autore] | Nome della persona che ha creato l&#39;attività. |
| [!UICONTROL Metodo di decisione] | Il metodo decisionale utilizzato in ogni attività: [Lato server](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html?lang=it) o [Lato client](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html). |

<!--|[!UICONTROL Location]|The URL for the activity identifies where the activity is displayed. This column helps you quickly identify an activity and determine whether a particular page already has an activity running on it.<P>If an activity runs on multiple URLs, a link shows how many more URLs are used. Click the link to view the complete list of URLs for that activity.<P>You can search based on the URL. Use the drop-down list next to the search box and select [!UICONTROL URL].|-->

## Tipi di attività {#types}

[!DNL Target] include diversi tipi di attività. La tabella seguente fornisce una panoramica di ogni tipo di attività con collegamenti per ulteriori informazioni. Per aiutarti a scegliere meglio il tipo di attività migliore, utilizza la [Guida alle attività di Adobe Target](/help/main/c-activities/target-activities-guide.md).

| Tipo di attività | Descrizione |
|--- |--- |
| [[!UICONTROL Test A/B]](/help/main/c-activities/t-test-ab/test-ab.md) | Il test A/B confronta due o più versioni del contenuto del sito web per vedere quale versione migliora meglio le conversioni durante un periodo di test pre-specificato. |
| [[!UICONTROL Allocazione automatica]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | [!UICONTROL Allocazione automatica], un tipo di test A/B, identifica un vincitore tra due o più esperienze e ridistribuisce automaticamente più traffico per aumentare le conversioni, mentre il test continua a essere eseguito e ad apprendere. |
| [[!UICONTROL Targeting automatico]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)<P>![Target Premium](/help/main/assets/premium.png) | La funzione Targeting automatico, un tipo di test A/B, utilizza l’apprendimento automatico avanzato per identificare più esperienze ad alte prestazioni definite dall’addetto al marketing. Inoltre, indica l’esperienza più adatta per ogni visitatore in base al profilo del singolo cliente e al comportamento dei visitatori precedenti con profili simili, per personalizzare contenuti e favorire le conversioni. |
| [[!UICONTROL Test multivariato]](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | [!UICONTROL Multivariate Testing] (MVT) confronta le combinazioni di offerte negli elementi di una pagina per determinare quale combinazione funziona meglio per un pubblico specifico e identifica quale elemento influisce maggiormente sul successo dell&#39;attività. |
| [[!UICONTROL Targeting esperienza]](/help/main/c-activities/t-experience-target/experience-target.md) | [!UICONTROL La funzione Targeting esperienza] (XT) fornisce contenuti a un pubblico specifico in base a una serie di regole e criteri definiti dall&#39;addetto al marketing. |
| [[!UICONTROL Personalizzazione automatizzata]](/help/main/c-activities/t-automated-personalization/automated-personalization.md)<P>![Target Premium](/help/main/assets/premium.png) | [!UICONTROL Automated Personalization] (AP) combina offerte o messaggi e utilizza l&#39;apprendimento automatico avanzato per abbinare diverse varianti a ogni visitatore in base al suo profilo cliente, per personalizzare il contenuto e favorire le conversioni. |
| [[!UICONTROL Funzione Consigli]](/help/main/c-recommendations/recommendations.md)<P>![Target Premium](/help/main/assets/premium.png) | Un consiglio determina in che modo un prodotto viene suggerito a un visitatore del sito web, in base alle sue attività sul sito.<P>Ad esempio, potrebbe essere utile incoraggiare l&#39;acquirente di uno zaino a considerare l&#39;acquisto di scarpe e bastoncini da trekking. Puoi creare un consiglio che mostra gli elementi spesso acquistati insieme con l&#39;algoritmo “Chi ha acquistato questo ha acquistato anche”. Oppure, potresti voler incoraggiare i visitatori a trascorrere più tempo sul sito multimediale consigliando video simili al video che stanno guardando, utilizzando l’algoritmo &quot;Persone che hanno visualizzato questo hanno visualizzato quello&quot;.<P>**NOTA**: è inoltre possibile includere i consigli nelle attività [!UICONTROL Test A/B], [!UICONTROL Allocazione automatica], [!UICONTROL Targeting automatico] e [!UICONTROL Targeting esperienza] (XT). Per ulteriori informazioni, consulta [Consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md). Questa funzionalità richiede una [licenza di Target Premium](/help/main/c-intro/intro.md#premium). |

## Applicare i filtri all’elenco Attività {#filters}

Per accedere ai filtri, fai clic sull&#39;icona **[!UICONTROL Mostra filtri]** ( ![Mostra icona filtri](/help/main/assets/icons/Filter.svg) ) nella parte superiore dell&#39;elenco.

Il menu consente di filtrare le attività in base ai seguenti attributi:

| Attributo | Dettagli |
| --- | --- |
| [!UICONTROL Tipo] | Filtra per [tipo di attività](#types). |
| [!UICONTROL Stato] | Filtra per stato attività.<ul><li>**[!UICONTROL Live]**: l&#39;attività è attualmente in esecuzione.</li><li>**[!UICONTROL Pianificato]**: l&#39;attività è pronta per essere attivata alla data e all&#39;ora di inizio specificate.</li><li>**[!UICONTROL Inattiva]**: l&#39;attività è stata sospesa o disattivata.</li><li>**[!UICONTROL Terminata]**: la data e l&#39;ora di fine specificate dell&#39;attività sono state raggiunte e l&#39;attività non verrà più distribuita.</li><li>**[!UICONTROL Archiviata]**: l&#39;attività è stata archiviata. È possibile attivare un&#39;attività archiviata per utilizzarla nuovamente.</li></ul>Per ulteriori informazioni sugli stati obsoleti [!UICONTROL Salva come bozza] e [!UICONTROL Sincronizzazione], vedi la nota sotto questa tabella. |
| [!UICONTROL Reporting di Source] | Filtra per origine di reporting.<ul><li>[[!DNL Analytics]](/help/main/c-integrating-target-with-mac/a4t/a4t.md): visualizza le attività che utilizzano [!UICONTROL Analytics for Target] (A4T) come origine per la generazione di rapporti.</li><li>[[!DNL Target]](/help/main/c-reports/reports.md): visualizza le attività che utilizzano [!DNL Target] come origine per la generazione di rapporti.</li><li>[[!DNL Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md): visualizza le attività che utilizzano [!DNL Adobe Customer Analytics] come origine per la generazione di rapporti.</li></ul> |
| [!UICONTROL Compositore esperienza] | Filtro in base al quale il compositore esperienza è stato utilizzato durante la creazione dell’attività:<ul><li>[Visivo](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md): visualizza le attività create utilizzando il [!UICONTROL Compositore esperienza visivo].</li><li>[Basato su modulo](/help/main/c-experiences/form-experience-composer.md): visualizza le attività create utilizzando [!UICONTROL Compositore esperienza basato su modulo].</li></ul> |
| [!UICONTROL Tipo di metrica] | Filtro in base al quale [metrica di successo](/help/main/c-activities/r-success-metrics/success-metrics.md) è stata scelta durante la creazione dell&#39;attività.<ul><li>[!UICONTROL Conversione]</li><li>[!UICONTROL Ricavi]</li><li>[!UICONTROL Coinvolgimento]</li><li>[!UICONTROL Usa una metrica di Analytics]</lI></ul> |
| [!UICONTROL Metodo di decisione] | Filtra in base al metodo decisionale utilizzato in ogni attività.<ul><li>[Lato server](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html?lang=it): visualizza le attività che utilizzano le decisioni lato server.</li><li>[Lato client](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html): visualizza le attività che utilizzano le decisioni lato client.</li></ul> |
| [!UICONTROL Source attività] | Filtra in base all’origine dell’attività utilizzata per creare ogni attività.<ul><li>[!DNL Adobe Target]</li><li>[[!DNL Adobe Target] API](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html?lang=it)</li><li>[[!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/docs/experience-platform.html?lang=it)</li><li>[[!DNL Adobe Experience Manager]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=it)</li><li>[[!DNL Adobe Mobile Services]](https://developer.adobe.com/client-sdks/home/)</li></ul> |
| [!UICONTROL Proprietà] | Filtra in base alla [proprietà](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) in cui è stata creata l&#39;attività. |


>[!NOTE]
>
>**Aggiornamento degli stati attività nell&#39;interfaccia utente aggiornata**: con gli ultimi aggiornamenti dell&#39;interfaccia utente, gli stati [!UICONTROL Salva come bozza] e [!UICONTROL Sincronizzazione] non sono più disponibili. Questo perché tutte le attività di creazione e modifica ora vengono eseguite direttamente nel sistema di consegna [!DNL Target] del back-end utilizzando il livello GraphQL, garantendo un processo più semplice ed efficiente.
>
>In precedenza, le attività venivano salvate per la prima volta nel front-end [!DNL Target] e quindi sincronizzate nel sistema di consegna [!DNL Target] del back-end, il che richiedeva tali stati intermedi. Poiché non è più così, questi stati sono stati rimossi.
>
>[!DNL Adobe] ha capito che alcuni clienti hanno espresso interesse per la funzionalità [!UICONTROL Salva come bozza]. Pur apprezzando questo feedback, al momento questa funzionalità non è supportata.

## Eseguire azioni rapide {#quick-actions}

Fai clic sull&#39;icona **[!UICONTROL Altre azioni]** (menu ![Altre azioni](/help/main/assets/icons/MoreVertical.svg)) accanto al nome di ogni attività per aprire un menu che consente di eseguire azioni rapide su un&#39;attività.

Sono disponibili le seguenti azioni (a seconda delle autorizzazioni e dello stato dell’attività):

| Azione | Descrizione |
| --- | --- |
| [!UICONTROL Modifica] | Modifica l&#39;attività. Qualsiasi attività può essere modificata.<P>Per ulteriori informazioni sulle diverse modalità di modifica delle attività, vedere [Modificare un&#39;attività o salvarla come bozza](/help/main/c-activities/edit-activity.md). |
| [!UICONTROL Disattiva] | Interrompe un&#39;attività in esecuzione o pianificata. Un’attività disattivata può essere riattivata o archiviata.<P>Se disattivi o archivi un’attività e poi la riattivi in un secondo momento, un visitatore continuerà a esserne parte dopo la riattivazione se vi partecipava prima che fosse disattivata o archiviata. Ogni metrica di conversione registrata durante il periodo trascorso tra i due eventi non verrà attribuita a quell’attività. |
| [!UICONTROL Attiva] | Avvia un’attività inattiva o pronta per essere attivata. |
| [!UICONTROL Archivia] | Invia l&#39;attività all&#39;archivio. Per impostazione predefinita, le attività archiviate non vengono più visualizzate nell&#39;elenco [!UICONTROL Attività]. Modifica il filtro per l&#39;elenco [!UICONTROL Attività] in modo da includere le attività archiviate per visualizzarle. È possibile attivare un&#39;attività archiviata per utilizzarla nuovamente.<P>Se disattivi o archivi un’attività e poi la riattivi in un secondo momento, un visitatore continuerà a esserne parte dopo la riattivazione se si trovava in tale attività prima che fosse disattivata o archiviata. Ogni metrica di conversione registrata durante il periodo trascorso tra i due eventi non verrà attribuita a quell’attività. |
| [!UICONTROL Copia] | Copia un&#39;attività. Qualsiasi attività può essere copiata. Quando si copia un&#39;attività viene creata una nuova attività con lo stesso nome e la dicitura “Copia”. Ad esempio, la copia di un test denominato “Offerte browser” sarà denominata “Copia Offerte browser”.<P>Le offerte visive vengono copiate con l&#39;attività. È possibile modificare in modo sicuro le offerte nella copia senza influire sull&#39;attività originale. L&#39;unica eccezione sono le offerte e le immagini salvate nella cartella Contenuto/Risorse. |
| [!UICONTROL Elimina] | Elimina una bozza o un’attività.<P>**NOTA**: non è possibile recuperare le attività eliminate. A meno che tu non sia sicuro che questa attività non sarà più necessaria, utilizza l&#39;azione [!UICONTROL Archivia]. Se necessario, puoi quindi riattivare l’attività. |

## Considerazioni

Tieni presente i seguenti dettagli sull&#39;elenco [!UICONTROL Attività]:

* Le attività [!UICONTROL Archiviate] e [!UICONTROL Terminate] non vengono visualizzate nell&#39;elenco [!UICONTROL Attività]. Per visualizzare queste attività, filtrale utilizzando l&#39;icona [Filtri](#filters) ( ![Mostra icona Filtri](/help/main/assets/icons/Filter.svg) ) nella parte superiore dell&#39;elenco.
* Quando un&#39;attività originariamente creata in [!DNL Target Classic] viene disattivata o eliminata, viene eliminata da [!DNL Target Standard/Premium]. Le attività eliminate originariamente create in [!DNL Target Classic] non vengono inviate alla cartella [!UICONTROL Archivio] in [!DNL Target Standard/Premium]. La funzionalità di cartella archiviata è applicabile solo alle attività create in [!DNL Target Standard/Premium].
* Tutti i tipi di attività diversi da [!UICONTROL Automated Personalization] (AP), [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] consentono di scegliere se utilizzare [!DNL Target] o [!DNL Adobe Analytics] come origine dati. [!UICONTROL Automated Personalization], [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] *utilizza sempre* dati [!DNL Target].
* Le attività sono disponibili per diversi canali:

   * Siti web e mobili
   * Schermi e dispositivi collegati a Internet, inclusi chioschi e sportelli automatici
   * Email e altri canali di acquisizione o siti partner
   * App mobili
   * In qualsiasi altro luogo sia possibile fornire contenuti con tag

## Limitazioni {#section_049D4684403A4E07B998067EB8E9BE56}

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

Per ulteriori limiti del [!UICONTROL Compositore esperienza visivo], vedi [Limitazioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721).

## Attributi importati in [!DNL Target] per attività aggiornate al di fuori di [!DNL Target] {#section_802B0D174E6A44E1A96F404CA81AAE44}

Se le attività create in [!DNL Target] vengono aggiornate dall&#39;esterno di [!DNL Target] (ad esempio tramite API), i seguenti attributi di attività vengono importati nuovamente in [!DNL Target]: `thirdpartyId`, `startDate`, `endDate`, `status`, `priority` e `marketingCloudMetadata(remoteModifiedBy)`.

Questo processo di importazione viene eseguito all&#39;apertura dell&#39;elenco [!UICONTROL Attività], con un ritardo massimo di dieci minuti.

