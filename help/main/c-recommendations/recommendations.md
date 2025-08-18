---
keywords: Recommendations;consigli;criteri Recommendations;criteri consigli;algoritmi Recommendations;algoritmi consigli:attività;criteri;recommendations targeting;targeting consigli
description: Scopri le attività Consigli in Adobe [!DNL Target] che consentono di visualizzare automaticamente contenuti che potrebbero interessare ai clienti in base alle precedenti attività dell’utente o ad altri algoritmi.
title: Cos’è la funzione Consigli di  [!DNL Target] ?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 0d986e17-bc99-4c08-a963-7f9a6619609a
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 97%

---

# Recommendations

Le attività [!DNL Adobe Target Recommendations] consentono di visualizzare automaticamente prodotti, servizi o contenuti che potrebbero interessare i visitatori in base alle loro attività precedenti, preferenze o ad altri algoritmi. [!DNL Target Recommendations] permette di indirizzare i clienti verso elementi rilevanti di cui potrebbero non essere a conoscenza. [!DNL Recommendations] consente di fornire ai visitatori contenuti pertinenti al momento giusto e nel posto giusto.

>[!NOTE]
>
>Le attività [!DNL Recommendations] sono disponibili come parte della soluzione [Target Premium](/help/main/c-intro/intro.md#premium). Non sono disponibili in [!DNL Target Standard] senza una licenza [!DNL Target Premium].
>
>Se al momento disponi di [!DNL Recommendations Classic], consulta [Confronto tra Recommendations Classic e le attività Consigli di Target Premium](/help/main/c-recommendations/c-recommendations-faq/recommendations-classic-versus-recommendations-activities-target-premium.md#concept_A80223EF66634EA380580C2823A581C5) per ulteriori informazioni sulle due soluzioni.

[!DNL Recommendations] ti consente di ottimizzare e personalizzare suggerimenti in tempo reale per diversi canali, applicazioni, pagine, messaggi di posta elettronica e altre opzioni di recapito per aumentare il coinvolgimento e la conversione riducendo il carico di gestione.

[!DNL Recommendations] consente di:

* Creare criteri sofisticati (regole) per automatizzare i consigli
* Visualizzare automaticamente i consigli utilizzando alcuni snippet JavaScript
* Sottoporre a test e ottimizzare i criteri di consiglio e i progetti che visualizzano i consigli
* Generare rapporti sui risultati dell’attività collegata ai consigli

Nella figura seguente vengono illustrati i consigli in una pagina web:

![immagine velocity_example](assets/velocity_example.png)

Un consiglio determina in che modo un prodotto viene suggerito a un visitatore, in base alle sue attività sul sito. Ad esempio:

| Azione desiderata | Consiglio |
|--- |--- |
| Incoraggiare chi acquista uno zaino a considerare l’acquisto di scarpe e bastoncini da trekking. | Creare un consiglio che mostra gli elementi acquistati spesso insieme, utilizzando i criteri “Chi ha acquistato questo ha acquistato anche”. |
| Aumentare il tempo che i visitatori passano su un sito multimediale consigliando contenuti simili a quelli che stanno guardando. | Creare un consiglio che suggerisce altri video, utilizzando i criteri “Chi ha visualizzato questo ha visualizzato anche”. |
| Suggerire ai clienti che hanno visualizzato informazioni su piani di risparmio di una banca di consultare anche le informazioni sui conti IRA. | Mostrare altri elementi acquistati dai visitatori dopo aver visualizzato un prodotto, senza mostrare il primo prodotto nei consigli, utilizzando i criterio “Chi ha visualizzato questo ha acquistato anche”. |

Per ulteriori informazioni su questi e altri criteri di [!DNL Recommendations], consulta [Criteri](/help/main/c-recommendations/c-algorithms/algorithms.md).

## Termini

Prima di iniziare a utilizzare [!DNL Recommendations] (Consigli), è utile acquisire familiarità con alcuni termini utilizzati in questa sezione. Non preoccuparti se ancora non comprendi perfettamente questi termini, acquisirai maggiore familiarità durante la configurazione delle attività [!DNL Recommendations] (Consigli).

| Termine | Definizione |
| --- | --- |
| Attività | Le attività in [!DNL Target] ti consentono di personalizzare il contenuto per tipi di pubblico specifici e di testare le progettazioni di pagine. [!DNL Recommendations] (Consigli) è solo uno dei molti tipi di attività disponibili in [!DNL Target]. Per ulteriori informazioni, consulta [Tipi di attività di Target](/help/main/c-activities/target-activities-guide.md). |
| Entità | Le entità si riferiscono agli elementi che desideri consigliare. Le entità possono essere qualsiasi cosa, ad esempio prodotti, contenuti (articoli, presentazioni, immagini, filmati e programmi TV), annunci di lavoro, ristoranti e così via. Per ulteriori informazioni, consulta [Entità](/help/main/c-recommendations/c-products/products.md). |
| Feed | I feed vengono utilizzati per importare le entità in [!DNL Recommendations]. Le entità possono essere inviate tramite file CSV, il formato feed di Google Product Search e le classificazioni di prodotto Adobe Analytics. Per ulteriori informazioni, consulta [Feed](/help/main/c-recommendations/c-products/feeds.md). |
| Catalogo | I cataloghi si riferiscono all’intero set di prodotti (entità). Il catalogo può contenere molte raccolte, e consente di organizzare i prodotti in contenitori logici. |
| Raccolta | Le raccolte si riferiscono a un insieme di elementi simili o correlati, ad esempio una singola categoria di prodotti. Tuttavia, puoi raggruppare qualsiasi elemento in una categoria adatta alla tua attività specifica, come prodotti in una determinata fascia di prezzo o colore o che possono essere di interesse in una particolare area geografica. Per ulteriori informazioni, consulta [Raccolte](/help/main/c-recommendations/c-products/collections.md). |
| Criteri | I criteri sono regole che determinano i prodotti da consigliare in base a un set predeterminato di comportamenti dei visitatori.<br>Alcuni esempi di criteri includono: <ul><li>Chi ha comprato questo ha acquistato anche quello</li><li>Chi ha visualizzato questo ha visualizzato anche quello</li><li>Articoli con attributi simili</li><li>Ultimo articolo acquistato</li><li>Categoria preferita</li></ul>  Per ulteriori informazioni, consulta [Criteri](/help/main/c-recommendations/c-algorithms/algorithms.md). |
| Progettazioni | Le progettazioni definiscono l’aspetto dei consigli in un’attività [!DNL Recommendations], ad esempio una riga, una colonna, una tabella o una griglia. L’illustrazione nella parte superiore di questo articolo mostra una progettazione 4x1. Per ulteriori informazioni, consulta [Creare una progettazione](/help/main/c-recommendations/c-design-overview/create-design.md). |
| Posizioni | Le posizioni si riferiscono a un’area di contenuto specifica su una pagina web, un’app mobile o un’e-mail in cui esegui un’attività a scopo di personalizzazione e ottimizzazione. |
| Tipi di pubblico | I tipi di pubblico sono gruppi di partecipanti simili a un’attività che visualizzeranno un’attività mirata. Un pubblico è un gruppo di persone con le stesse caratteristiche, ad esempio nuovi visitatori, visitatori di ritorno o visitatori provenienti da una specifica area geografica. La funzione Pubblico consente di indirizzare contenuti ed esperienze diversi a tipi di pubblico specifici per ottimizzare le attività di marketing digitale presentando al momento giusto i messaggi più appropriati ai vari visitatori. Per ulteriori informazioni, consulta [Tipi di pubblico](/help/main/c-target/target.md). |
| Consigli come offerta | Funzione che consente di includere i consigli all’interno di attività di test A/B (tra cui Allocazione automatica e Targeting automatico) e di Targeting esperienza (XT). Per ulteriori informazioni, consulta [Consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md). |

## Video di formazione: Tipi di attività ![Icona Panoramica](/help/main/assets/overview.png)

Questo video spiega i tipi di attività disponibili in [!DNL Target Standard/Premium]. [!DNL Recommendations] è discusso a partire dal 7:20.

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/17386)

## Webinar sulle nozioni di base di Adobe Target: introduzione alla funzione Consigli ![Icona esercitazione](/help/main/assets/tutorial.png) {#intro-to-recs}

Il webinar *Introduzione alla funzione Consigli* include una descrizione approfondita di come sfruttare il valore di [!DNL Adobe Target Recommendations]. Scopri in che modo questa attività [!DNL Target] visualizza automaticamente prodotti o contenuti che potrebbero interessare ai clienti ottimizzando i suggerimenti in tempo reale basati sulle visite precedenti. Inoltre, immergiti nell’interfaccia utente [!DNL Target] per una panoramica dettagliata su come creare un’attività [!DNL Recommendations].

[Introduzione alla funzione Consigli](https://adobecustomersuccess.adobeconnect.com/p8gt31drhs3e/?OWASP_CSRFTOKEN=4bd6cac5d0806167ee0a5449ba93d6300548d09c922bcb751c38973897a5703a)
