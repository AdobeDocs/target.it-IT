---
keywords: Recommendations;Recommendations criteria;recommendations algorithms;recommendations activity;criteria;recommendations targeting;recs
description: Le attività Recommendations in  Adobe Target visualizzano automaticamente prodotti o contenuti che potrebbero interessare i clienti sulla base dell'attività utente precedente o di altri algoritmi. I consigli aiutano a indirizzare i clienti verso elementi rilevanti di cui potrebbero non essere a conoscenza.
title: ' Adobe Target Recommendations'
feature: recommendations general
uuid: 2aefd118-8fec-493d-ae4e-c1139c877a3f
translation-type: tm+mt
source-git-commit: a4479a26873f39a41782e78651802899512b87fe
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 59%

---


# ![PREMIUM](/help/assets/premium.png) Consigli{#recommendations}

[!DNL Adobe Target Recommendations] le attività visualizzano automaticamente prodotti, servizi o contenuti che potrebbero interessare ai visitatori in base all&#39;attività utente, alle preferenze o ad altri criteri precedenti. [!DNL Target Recommendations] aiuta il visitatore diretto agli elementi rilevanti che altrimenti potrebbero ignorare. [!DNL Recommendations] consente di fornire ai visitatori contenuti pertinenti al momento giusto e nel posto giusto.

>[!NOTE]
>
>Le attività [!DNL Recommendations] sono disponibili come parte della soluzione [Target Premium](/help/c-intro/intro.md#premium). Non sono disponibili in [!DNL Target Standard] senza una licenza [!DNL Target Premium].
>
>Se al momento disponi di [!DNL Recommendations Classic], consulta [Confronto tra Recommendations Classic e le attività Consigli di Target Premium](../c-recommendations/c-recommendations-faq/recommendations-classic-versus-recommendations-activities-target-premium.md#concept_A80223EF66634EA380580C2823A581C5) per ulteriori informazioni sulle due soluzioni.

[!DNL Recommendations] ti consente di ottimizzare e personalizzare suggerimenti in tempo reale per diversi canali, applicazioni, pagine, messaggi di posta elettronica e altre opzioni di recapito per aumentare il coinvolgimento e la conversione riducendo il carico di gestione.

[!DNL Recommendations] consente di:

* Creare criteri sofisticati (regole) per automatizzare i consigli
* Visualizzare automaticamente i consigli utilizzando alcuni snippet JavaScript
* Sottoporre a test e ottimizzare i criteri di consiglio e i progetti che visualizzano i consigli
* Generare rapporti sui risultati dell’attività collegata ai consigli

Nella figura seguente vengono illustrati i consigli in una pagina web:

![](assets/velocity_example.png)

Una raccomandazione determina il modo in cui un prodotto viene suggerito a un visitatore, a seconda delle attività del visitatore sul sito. Ad esempio:

| Azione desiderata | Consiglio |
|--- |--- |
| Incoraggiare chi acquista uno zaino a considerare l’acquisto di scarpe e bastoncini da trekking. | Creare un consiglio che mostra gli elementi acquistati spesso insieme, utilizzando i criteri “Chi ha acquistato questo ha acquistato anche”. |
| Aumentare il tempo che i visitatori passano su un sito multimediale consigliando contenuti simili a quelli che stanno guardando. | Creare un consiglio che suggerisce altri video, utilizzando i criteri “Chi ha visualizzato questo ha visualizzato anche”. |
| Suggerire ai clienti che hanno visualizzato informazioni su piani di risparmio di una banca di consultare anche le informazioni sui conti IRA. | Mostrare altri elementi acquistati dai visitatori dopo aver visualizzato un prodotto, senza mostrare il primo prodotto nei consigli, utilizzando i criterio “Chi ha visualizzato questo ha acquistato anche”. |

Per ulteriori informazioni su questi e altri criteri di [!DNL Recommendations], consulta [Criteri](../c-recommendations/c-algorithms/algorithms.md).

## Termini

Prima di iniziare a utilizzare [!DNL Recommendations], è utile acquisire familiarità con alcuni termini utilizzati in questa sezione. Non preoccuparti se non hai ancora capito completamente questi termini, potrai conoscerli meglio durante la configurazione delle tue [!DNL Recommendations] attività.

| Termine | Definizione |
| --- | --- |
| Attività | Le attività in [!DNL Target] consentono di personalizzare il contenuto per audience specifiche e di sottoporre a test le progettazioni di pagina. [!DNL Recommendations] è solo uno dei molti tipi di attività disponibili in [!DNL Target]. Per ulteriori informazioni, vedete Tipi [di attività](/help/c-activities/target-activities-guide.md)Target. |
| Entità | Le entità si riferiscono agli elementi che desideri consigliare. Le entità possono essere prodotti, contenuti (articoli, presentazioni, immagini, filmati e programmi televisivi), elenchi di lavoro, ristoranti e così via. For more information, see [Entities](/help/c-recommendations/c-products/products.md). |
| Feed | I feed vengono utilizzati per importare le entità in [!DNL Recommendations]. Le entità possono essere inviate tramite file CSV, il formato feed di Google Product Search e le classificazioni di prodotto Adobe Analytics. Per ulteriori informazioni, consulta [Feed](/help/c-recommendations/c-products/feeds.md). |
| Catalogo | I cataloghi si riferiscono all’intero set di prodotti (entità). Il catalogo può contenere molte raccolte, un modo per organizzare i prodotti in raggruppamenti logici. |
| Raccolta | Le raccolte fanno riferimento a un insieme di elementi simili o correlati, ad esempio una singola categoria di prodotti. Tuttavia, puoi raggruppare qualsiasi elemento in una categoria adatta alla tua attività specifica, come prodotti in una determinata fascia di prezzo o colore o che possono essere di interesse in una particolare area geografica. For more information, see [Collections](/help/c-recommendations/c-products/collections.md). |
| Criteri | I criteri sono regole che determinano i prodotti da consigliare in base a un set predeterminato di comportamenti dei visitatori.<br>Alcuni esempi di criteri includono: <ul><li>Chi ha comprato questo ha acquistato anche quello</li><li>Chi ha visualizzato questo ha visualizzato anche quello</li><li>Articoli con attributi simili</li><li>Ultimo articolo acquistato</li><li>Categoria preferita</li></ul>  Per ulteriori informazioni, consulta [Criteri](/help/c-recommendations/c-algorithms/algorithms.md). |
| Progettazione | Le progettazioni definiscono l&#39;aspetto delle raccomandazioni in un&#39; [!DNL Recommendations] attività, ad esempio una riga, una colonna, una tabella o una griglia. L&#39;illustrazione nella parte superiore di questo articolo mostra un design 4 x 1. For more information, see [Create a design](/help/c-recommendations/c-design-overview/create-design.md). |
| Posizioni | Le posizioni fanno riferimento a un&#39;area di contenuto specifica su una pagina Web, un&#39;app mobile o un&#39;e-mail in cui viene eseguita un&#39;attività a scopo di personalizzazione e ottimizzazione. |
| Tipi di pubblico | I tipi di pubblico sono gruppi di partecipanti con attività simili che visualizzeranno un&#39;attività con targeting. Un pubblico è un gruppo di persone con le stesse caratteristiche, ad esempio nuovi visitatori, visitatori di ritorno o visitatori provenienti da una specifica area geografica. La funzione Pubblico consente di indirizzare contenuti ed esperienze diversi a tipi di pubblico specifici per ottimizzare le attività di marketing digitale presentando al momento giusto i messaggi più appropriati ai vari visitatori. Per ulteriori informazioni, consulta [Tipi di pubblico](/help/c-target/target.md). |
| Consigli come offerta | Funzione che consente di includere raccomandazioni all&#39;interno di test A/B (inclusi allocazioni automatiche e targeting automatico) e di targeting delle esperienze (XT). Per ulteriori informazioni, consulta [Consigli come offerta](/help/c-recommendations/recommendations-as-an-offer.md). |

## Video di formazione: Scheda ![Panoramica sui tipi di attività](/help/assets/overview.png)

Questo video spiega i tipi di attività disponibili in [!DNL Target Standard/Premium]. L’argomento di [!DNL Recommendations] è trattato a partire dal minuto 7:20.

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/17386)

## Webinar sulle nozioni di base di Adobe Target: introduzione alla funzione consigli ![Badge di esercitazione](/help/assets/tutorial.png) {#intro-to-recs}

Il webinar *Introduzione alla funzione Consigli* include una descrizione approfondita di come sfruttare il valore di [!DNL Adobe Target Recommendations]. Scopri in che modo questa attività [!DNL Target] visualizza automaticamente prodotti o contenuti che potrebbero interessare ai clienti ottimizzando i suggerimenti in tempo reale basati sulle visite precedenti. Inoltre, immergiti nell’interfaccia utente [!DNL Target] per una panoramica dettagliata su come creare un’attività [!DNL Recommendations].

[Introduzione alla funzione Consigli](https://adobecustomersuccess.adobeconnect.com/p8gt31drhs3e/?OWASP_CSRFTOKEN=4bd6cac5d0806167ee0a5449ba93d6300548d09c922bcb751c38973897a5703a)