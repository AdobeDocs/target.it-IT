---
description: Adobe Analytics for Target (A4T) è un’integrazione tra soluzioni che consente di creare attività basate su metriche di conversione e segmenti di pubblico di Analytics. Questa integrazione consente di utilizzare i rapporti di Analytics per esaminare i risultati. Se utilizzi Analytics come origine per la generazione di rapporti per un’attività, tutti i rapporti e le segmentazioni per tale attività si basano sulla raccolta di dati di Analytics.
keywords: a4t;Analytics;analytics for target;Analytics come origine per la generazione di rapporti;Adobe Analytics come origine di reporting per Target
seo-description: Adobe Analytics for Target (A4T) è un’integrazione tra soluzioni che consente di creare attività basate su metriche di conversione e segmenti di pubblico di Analytics. Questa integrazione consente di utilizzare i rapporti di Analytics per esaminare i risultati. Se utilizzi Analytics come origine per la generazione di rapporti per un’attività, tutti i rapporti e le segmentazioni per tale attività si basano sulla raccolta di dati di Analytics.
seo-title: Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)
solution: Target
subtopic: Test multivariato
title: Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)
topic: Standard
uuid: 616798a6-1587-410f-9ac6-473beb39e3fc
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T){#adobe-analytics-as-the-reporting-source-for-adobe-target-a-t}

Adobe Analytics for Target (A4T) è un’integrazione tra soluzioni che consente di creare attività basate su metriche di conversione e segmenti di pubblico di Analytics. L’integrazione di A4T consente di utilizzare i rapporti di Analytics per esaminare i risultati. Se utilizzi Analytics come origine per la generazione di rapporti per un’attività, tutti i rapporti e le segmentazioni per tale attività si basano sulla raccolta di dati di Analytics.

## Panoramica di A4T {#section_92B66069210C40DBA937790E8CC596CF}

L’integrazione Analytics for Target fornisce potenti strumenti di analisi per il programma di ottimizzazione, che consentono di risparmiare tempo prezioso.

L’utilizzo dei dati di Analytics in Target offre i tre vantaggi principali seguenti:

* Gli addetti al marketing possono applicare dinamicamente le metriche di successo di Analytics o i segmenti di reporting ai rapporti delle attività di Target in qualsiasi momento. Non è necessario specificare tutte le impostazioni prima di eseguire l’attività.
* Un’unica fonte di dati elimina la varianza che si verifica quando si raccolgono dati in due sistemi distinti.
* L’implementazione di Adobe Analytics esistente raccoglie tutti i dati necessari. Non è necessario implementare mbox sulle pagine al solo scopo di raccogliere dati per i rapporti. Tuttavia, è ancora consigliabile implementare una mbox per la conferma dell’ordine per le attività di Personalizzazione automatizzata (AP).

>[!IMPORTANT]
>
>Prima di iniziare a utilizzare A4T, è necessario richiedere che il tuo account sia predisposto per l’integrazione. Utilizza [questo modulo](https://www.adobe.com/go/audiences) per richiedere il provisioning.
>
>L’integrazione che consente ad Adobe Analytics di essere l’origine dati per Adobe Target (A4T) rappresenta la prossima generazione del plug-in Test&amp;Target per SiteCatalyst. Questo plug-in è stato dichiarato obsoleto, ma rimane supportato per i clienti che già lo utilizzano.

Se utilizzi Analytics come origine per la generazione di rapporti per un’attività, tutti i rapporti e le segmentazioni per tale attività si basano su Analytics.

Tutte le metriche di Analytics, incluse quelle calcolate, sono disponibili in Target Standard/Premium e nel rapporto di Attività Target in Analytics. Allo stesso modo, qualsiasi segmento disponibile in Analytics può essere applicato a entrambe le soluzioni. Puoi applicare la metrica o il pubblico al rapporto in Target Standard/Premium dopo che il test è iniziato, o anche dopo che è stato completato.

Ogni metrica è inclusa, comprese quelle personalizzate o calcolate che sono integrate in Analytics.

Dopo il periodo di classificazione, i dati sono visualizzati in questi rapporti circa un'ora dopo essere stati raccolti dal sito. Tutte le metriche, i segmenti e i valori nei rapporti provengono dalla suite di rapporti selezionata quando si configura l’attività.

Considerazioni importanti per l’utilizzo di A4T:

* Per utilizzare Adobe Analytics come origine di reporting per Adobe Target, è necessario che sia voi che la società abbiate accesso ad Adobe Analytics e ad Adobe Target. [Contatta il rappresentante del tuo account](../../cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) per accedere a queste soluzioni.
* L’origine per la generazione di rapporti è impostata per ogni attività. Target continua a raccogliere dati da utilizzare nelle attività di reportistica. Tali dati restano disponibili per consentirti di basare un’attività sui dati raccolti da Target.
* Per la generazione dei rapporti, è necessario utilizzare un’origine o l’altra. Non è possibile raccogliere dati per una singola attività da entrambe le origini.
* Con A4T tutte le metriche di successo disponibili per le attività sono metriche di Analytics. Tuttavia, la metrica obiettivo può essere basata su una chiamata mbox. Ad esempio, è possibile utilizzare le funzionalità di tracciamento dei clic predefinite di Target con A4T invece di implementare il codice di tracciamento dei clic di Analytics.
* I rapporti di un’attività A4T visualizzati nell’interfaccia utente di Target contengono i dati di Analytics. Ad esempio, la metrica Visitatore in Target corrisponde alla metrica Visitatore di Analytics e non alla metrica Visitatori di Target, che ora è chiamata Partecipanti. Questa differenza è particolarmente importante per le metriche relative al traffico di base (Visitatori, Visite, Visualizzazioni pagina) e per le metriche di conversione.
* Tutte le attività di Target esistenti continuano a raccogliere i dati di Target e non sono interessate dall’abilitazione di A4T.
* L’utilizzo di Analytics come origine per la generazione di rapporti consente una sola metrica basata su mbox.
* Una chiamata da server a server da Target ad Analytics invia informazioni ad Analytics sulle attività e sulle esperienze. Questa integrazione non comporta chiamate server aggiuntive per Target o Analytics.

## Tipi di attività supportate {#section_F487896214BF4803AF78C552EF1669AA}

La tabella seguente illustra i tipi di attività che supportano Analytics come origine per la generazione di rapporti (A4T):

| Tipi di attività | Compatibile con A4T? | Note, se applicabili |
|--- |--- |--- |
| Attività A/B con suddivisione manuale del traffico | Sì |  |
| Attività A/B con Allocazione automatica | No |  |
| Attività A/B con Targeting automatico | No |  |
| Targeting esperienza (XT) | Sì |  |
| Test multivariato (MVT) | Sì | Richiede metriche obiettivo basate su mbox per ottenere il rapporto sul contributo degli elementi.  Il rapporto sul contributo degli elementi non supporta attualmente le metriche di Analytics. |
| Attività di Personalizzazione automatizzata (AP) | No |  |
| Attività di Consigli | Sì |  |
| App mobile | Sì | Supportato con l’SDK di Mobile Services, versione 4.13.1 o successiva.  Per ulteriori informazioni, consulta la [documentazione di Mobile Services](https://marketing.adobe.com/resources/help/en_US/mobile/). |
| E-mail | No |  |
| API di consegna lato server | Sì | Per ulteriori informazioni, consulta [Lato server: implementare Target](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| SDK di NodeJS | Sì | Per ulteriori informazioni, consulta [Lato server: implementare Target](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| Integrazione del servizio Cloud di AEM 6.1 (o precedente) | No |  |
| Integrazione del servizio Cloud di AEM 6.2 (o successiva) | Sì | Per ulteriori informazioni, consulta [Integrazione con Adobe Target](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/target.html) nella documentazione di Adobe Experience Manager 6.2. |
| Qualsiasi attività con un’offerta di reindirizzamento | Sì | Ci sono requisiti minimi più severi per le offerte di reindirizzamento con A4T. Per ulteriori informazioni, consulta [Offerte di reindirizzamento - Domande frequenti su A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md). |
| Node.JS | Sì |  |

Poiché tutti i tipi di attività non supportano ancora A4T, è consigliabile mantenere o implementare importanti mbox di conversione, ad esempio la mbox “orderConfirmPage”.

## Esempi di rapporti A4T {#section_F0A43A1CB2F04E8282B909E4D7034361}

Per visualizzare i rapporti A4T in [!DNL Target]**, fai clic su[!UICONTROL Attività]**, fai clic sull’attività desiderata dall’elenco che utilizza [!DNL Analytics] come origine per la generazione di rapporti, quindi fai clic sulla scheda **[!UICONTROL Rapporti]**.

>[!NOTE]
>
>È possibile utilizzare l’elenco a discesa [!UICONTROL Origine per la generazione di rapporti] nella parte superiore della pagina [!UICONTROL Attività] per visualizzare solo le attività che utilizzano [!DNL Analytics] come origine per la generazione di rapporti.

Per passare dalla Vista tabella alla [!UICONTROL Vista grafico] del rapporto, fai clic sull’icona appropriata in alto a destra nel rapporto.

La figura seguente illustra la [!UICONTROL Vista grafico] di un rapporto A4T con l’elenco a discesa [!UICONTROL Metrica rapporto] contenente le metriche obiettivo di [!DNL Analytics] disponibili:

![](assets/a4t_report_graph1.png)

La figura seguente illustra la [!UICONTROL Vista grafico] di un rapporto A4T con l’elenco a discesa [!UICONTROL Pubblico] contenente i tipi di pubblico di [!DNL Analytics] disponibili:

![](assets/a4t_report_graph2.png)

La figura seguente illustra la [!UICONTROL Vista tabella] di un rapporto A4T:

![](assets/a4t_report_table.png)

Per visualizzare il rapporto in [!DNL Analytics] anziché in [!DNL Target], fai clic su **[!UICONTROL Visualizza in Analytics]** nella parte superiore del rapporto.

## Analytics &amp; Target: esercitazione sulle best practice per l'analisi {#section_3438E6E77A464424B717A4FD333B84B2}

Apri l'esercitazione [Analytics &amp; Target: esercitazione sulle best practice per l'analisi](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), fornita da Adobe Experience League.

## Video di formazione:

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Reporting di Analytics for Target (A4T) (4:32)

Questo video spiega come usare Adobe Analytics come origine per la generazione di rapporti in Adobe Target per l'analisi del tuo programma di ottimizzazione.

* Cosa è A4T e perché utilizzarlo
* Come funziona A4T
* Prerequisiti necessari prima di utilizzare A4T

>[!VIDEO](https://video.tv.adobe.com/v/17384?captions=ita)

### Integrazione di Analytics e Target (A4T) (40:33)

Questo video è una registrazione di “ [Office Hours](../../cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)”, un’iniziativa condotta dal team di assistenza clienti Adobe.

* Configurare e convalidare il funzionamento dell'integrazione
* Funzionamento dell'integrazione
* Informazioni sui rapporti ideali da utilizzare in Analytics
* Risposte alle domande più frequenti su A4T

>[!VIDEO](https://video.tv.adobe.com/v/22223/?captions=ita)