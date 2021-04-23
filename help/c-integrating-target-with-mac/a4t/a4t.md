---
keywords: a4t;Analytics;analytics for target;Analytics come origine per la generazione di rapporti;Adobe Analytics come origine di reporting per Target
description: Utilizza Analytics for [!DNL Target] (A4T) per creare attività basate su metriche di conversione e segmenti di pubblico di Analytics e utilizza i rapporti di Analytics per esaminare i risultati.
title: Cos’è Analytics for [!DNL Target] (A4T)?
feature: Analytics for Target (A4T)
exl-id: 5bb80b03-8209-4932-a838-0e11c5865133
translation-type: tm+mt
source-git-commit: cb42be6b0791711d3a9ddf5680cf6d6e32045579
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 39%

---

# Adobe Analytics come origine per la generazione di rapporti, ad Adobe [!DNL Target] (A4T)

[!DNL Adobe Analytics for Target] (A4T) è un’integrazione tra più soluzioni che consente di creare attività basate su metriche di  [!DNL Analytics] conversione e segmenti di pubblico. L’integrazione A4T consente di utilizzare i rapporti [!DNL Analytics] per esaminare i risultati. Se utilizzi [!DNL Analytics] come origine per la generazione di rapporti per un’attività, tutti i rapporti e le segmentazioni per tale attività si basano sulla raccolta dati [!DNL Analytics].

## Panoramica di A4T {#section_92B66069210C40DBA937790E8CC596CF}

L’ integrazione [!DNL Analytics for Target] tra [!DNL Analytics] e [!DNL Target] fornisce potenti strumenti di analisi e risparmio di tempo per il programma di ottimizzazione.

I tre vantaggi principali dell’utilizzo dei dati [!DNL Analytics] in [!DNL Target] sono:

* Gli addetti al marketing possono applicare dinamicamente le metriche di successo [!DNL Analytics] o i segmenti di reporting ai rapporti di attività [!DNL Target] in qualsiasi momento. Non è necessario specificare tutte le impostazioni prima di eseguire l’attività.
* Un’unica fonte di dati elimina la varianza che si verifica quando si raccolgono dati in due sistemi distinti.
* L&#39;implementazione [!DNL Analytics] esistente raccoglie tutti i dati richiesti. Non è necessario implementare mbox sulle pagine al solo scopo di raccogliere dati per i rapporti. Adobe consiglia ancora di implementare una mbox di conferma dell&#39;ordine per le attività [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP).

>[!IMPORTANT]
>
>Prima di poter iniziare a utilizzare A4T, è necessario richiedere il provisioning dell’integrazione per il tuo account. Utilizza [questo modulo](https://www.adobe.com/go/audiences) per richiedere il provisioning.
>
>L’integrazione che abilita [!DNL Analytics] come origine dati per [!DNL Target] (A4T) rappresenta la nuova generazione del plug-in Test&amp;Target per il SiteCatalyst. Questo plug-in è stato dichiarato obsoleto, ma rimane supportato per i clienti che già lo utilizzano.

Se utilizzi [!DNL Analytics] come origine per la generazione di rapporti per un’attività, tutti i rapporti e le segmentazioni per tale attività si basano su [!DNL Analytics].

Tutte le metriche [!DNL Analytics], comprese le metriche calcolate, sono disponibili in [!DNL Target] e nel rapporto [!UICONTROL Attività di Target] in [!DNL Analytics]. Allo stesso modo, qualsiasi segmento disponibile in [!DNL Analytics] può essere applicato a entrambe le soluzioni. Puoi applicare la metrica o il pubblico al rapporto in [!DNL Target] dopo l’avvio dell’attività, o anche dopo il completamento dell’attività.

Ogni metrica è inclusa, comprese eventuali metriche personalizzate o calcolate integrate in [!DNL Analytics].

Dopo il periodo di classificazione, i dati sono visualizzati in questi rapporti circa un&#39;ora dopo essere stati raccolti dal sito. Tutte le metriche, i segmenti e i valori nei rapporti provengono dalla suite di rapporti selezionata quando si configura l’attività.

Considerazioni importanti per l’utilizzo di A4T:

* Per utilizzare [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target], sia tu che la tua azienda dovete avere accesso a [!DNL Analytics] e a [!DNL Target]. [Contatta il rappresentante del tuo account](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) per accedere a queste soluzioni.
* L’origine per la generazione di rapporti è impostata per ogni attività. [!DNL Target] continua a raccogliere i dati da utilizzare nei rapporti e  [!DNL Target] i dati sono ancora disponibili se preferisci basare un’attività sui dati raccolti da  [!DNL Target].
* Utilizzare un&#39;origine per la generazione di rapporti o l&#39;altra. Non è possibile raccogliere dati per una singola attività da entrambe le origini.
* Quando utilizzi A4T, tutte le metriche di successo disponibili per le attività sono metriche [!DNL Analytics]. Tuttavia, la metrica obiettivo può essere basata su una chiamata mbox. Ad esempio, puoi utilizzare le funzionalità di tracciamento dei clic predefinite di Target con A4T invece di dover implementare il codice di tracciamento dei clic [!DNL Analytics].
* Quando visualizzi il reporting di un’attività A4T nell’interfaccia utente [!DNL Target], stai visualizzando i dati [!DNL Analytics]. Ad esempio, se utilizzi la metrica [!UICONTROL Visitatore] in [!DNL Target], stai utilizzando la metrica [!DNL Analytics] [!UICONTROL Visitatore], non la metrica [!DNL Target] [!UICONTROL Visitatori], che è ora denominata [!UICONTROL Partecipanti]. Questa differenza è particolarmente importante per le metriche del traffico di base ([!UICONTROL Visitatori], [!UICONTROL Visite], [!UICONTROL Visualizzazioni pagina]) e le metriche di conversione.
* Tutte le attività [!DNL Target] esistenti continuano a utilizzare la raccolta dati [!DNL Target] e non vengono influenzate dall’abilitazione di A4T.
* È consentita una sola metrica basata su mbox quando si utilizza [!DNL Analytics] come origine per la generazione di rapporti.
* Una chiamata server-to-server da [!DNL Target] a [!DNL Analytics] invia informazioni sull&#39;attività e sull&#39;esperienza a [!DNL Analytics]. Questa integrazione non comporta più chiamate server per [!DNL Target] o [!DNL Analytics].

   In alcune situazioni, le classificazioni da [!DNL Target] a [!DNL Analytics] non riescono e le attività non mostrano dati in [!DNL Analytics]. Consulta [Risoluzione dei problemi relativi all’integrazione di Analytics e Target (A4T)](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md). Puoi anche [contattare l&#39;Assistenza clienti](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) per ulteriore assistenza.

## Tipi di attività supportati {#section_F487896214BF4803AF78C552EF1669AA}

La tabella seguente mostra quali tipi di attività supportano [!DNL Analytics] come origine per la generazione di rapporti in [!DNL Target] (A4T):

| Tipi di attività | Compatibile con A4T? | Note, se applicabili |
|--- |--- |--- |
| Attività A/B con suddivisione manuale del traffico | Sì |  |
| Attività A/B con Allocazione automatica | Sì | Consulta [Supporto A4T per le attività di allocazione automatica e targeting automatico](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md) |
| Attività A/B con Targeting automatico | Sì | Consulta [Supporto A4T per attività di allocazione automatica e targeting automatico](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md). |
| Targeting esperienza (XT) | Sì |  |
| Test multivariato (MVT) | Sì | Richiede metriche obiettivo basate su mbox per ottenere il rapporto [!UICONTROL Contributo elemento] . Il rapporto [!UICONTROL Contributo elemento] al momento non supporta le metriche [!DNL Analytics]. |
| Attività di Personalizzazione automatizzata (AP) | No |  |
| Attività di Consigli | Sì |  |
| App mobile | Sì | Supportato con l’SDK di Mobile Services, versione 4.13.1 o successiva. Per ulteriori informazioni, consulta la [documentazione di Mobile Services](https://experienceleague.adobe.com/docs/mobile-services/using/home.html). |
| E-mail | No |  |
| API di distribuzione lato server | Sì | Per ulteriori informazioni, consulta [Lato server: implementare Target](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| SDK di NodeJS | Sì | Per ulteriori informazioni, consulta [Lato server: implementare Target](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| Integrazione del servizio Cloud di AEM 6.1 (o precedente) | No |  |
| Integrazione del servizio Cloud di AEM 6.2 (o successiva) | Sì | Per ulteriori informazioni, consulta [Integrazione con Adobe Target](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/target.html) nella documentazione [!DNL Adobe Experience Manager] 6.2 . |
| Qualsiasi attività utilizzando un’offerta di reindirizzamento | Sì | Ci sono requisiti minimi più severi per le offerte di reindirizzamento con A4T. Per ulteriori informazioni, consulta [Offerte di reindirizzamento - Domande frequenti su A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md). |
| Node.JS | Sì | Per ulteriori informazioni, consulta [SDK di Node.js](https://adobetarget-sdks.gitbook.io/docs/sdk-reference-guides/nodejs-sdk) nella guida *SDK di Adobe Target* . |
| SDK per Java | Sì | Per ulteriori informazioni, consulta [Java SDK](https://adobetarget-sdks.gitbook.io/docs/sdk-reference-guides/java-sdk) nella guida *Adobe Target* SDK. |

Poiché tutti i tipi di attività non supportano ancora A4T, è consigliabile mantenere o implementare importanti mbox di conversione, ad esempio la mbox `orderConfirmPage` .

## Esempi di rapporti A4T {#section_F0A43A1CB2F04E8282B909E4D7034361}

Per visualizzare i rapporti A4T in [!DNL Target], fai clic su **[!UICONTROL Attività]**, fai clic sull’attività desiderata dall’elenco che utilizza [!DNL Analytics] come origine per la generazione di rapporti, quindi fai clic sulla scheda **[!UICONTROL Rapporti]** .

>[!NOTE]
>
>È possibile utilizzare l’elenco a discesa [!UICONTROL Origine per la generazione di rapporti] nella parte superiore della pagina [!UICONTROL Attività] per visualizzare solo le attività che utilizzano [!DNL Analytics] come origine per la generazione di rapporti.

Per passare dalla [!UICONTROL Vista tabella] alla [!UICONTROL Vista grafico] del rapporto, fai clic sull’icona appropriata in alto a destra nel rapporto.

La figura seguente illustra la [!UICONTROL Vista grafico] di un rapporto A4T con l’elenco a discesa [!UICONTROL Metrica rapporto] contenente le metriche obiettivo di [!DNL Analytics] disponibili:

![](assets/a4t_report_graph1.png)

La figura seguente illustra la [!UICONTROL Vista grafico] di un rapporto A4T con l’elenco a discesa [!UICONTROL Pubblico] contenente i tipi di pubblico di [!DNL Analytics] disponibili:

![](assets/a4t_report_graph2.png)

La figura seguente illustra la [!UICONTROL Vista tabella] di un rapporto A4T:

![](assets/a4t_report_table.png)

Per visualizzare il rapporto in [!DNL Analytics] anziché in [!DNL Target], fai clic su **[!UICONTROL Visualizza in Analytics]** nella parte superiore del rapporto.

## Analytics &amp; Target: esercitazione sulle best practice per l&#39;analisi {#section_3438E6E77A464424B717A4FD333B84B2}

Apri [Analytics &amp; Target: Esercitazione sulle best practice per l&#39;analisi](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), fornita da [!DNL Adobe Experience League].

## Video di formazione:

I video seguenti contengono ulteriori informazioni sui concetti discussi in questo argomento.

### Analytics for Adobe Target (A4T) (4:32) ![Badge panoramica](/help/assets/overview.png)

Questo video spiega come utilizzare [!DNL Analytics] come origine per la generazione di rapporti in [!DNL Target] per eseguire l&#39;analisi del programma di ottimizzazione.

* Cosa è A4T e perché utilizzarlo
* Come funziona A4T
* Prerequisiti necessari prima di utilizzare A4T

>[!VIDEO](https://video.tv.adobe.com/v/17384)

### Integrazione di Analytics/Adobe Target (A4T) (40:33) ![Badge tutorial](/help/assets/tutorial.png)

Questo video è una registrazione di “ [Office Hours](/help/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)”, un’iniziativa condotta dal team di assistenza clienti Adobe.

* Configurare e convalidare il funzionamento dell&#39;integrazione
* Funzionamento dell&#39;integrazione
* Informazioni sui rapporti ideali da utilizzare in Analytics
* Risposte alle domande più frequenti su A4T

[Office hours dell&#39;integrazione di Analytics e Target (A4T)](https://helpx.adobe.com/customer-care-office-hours/target/analytics-target-A4T-integration.html)
