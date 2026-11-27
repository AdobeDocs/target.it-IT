---
keywords: consigli;algoritmi consigli;attività consigli;recommendations classic
description: Rivedi le informazioni per comprendere le differenze tra le precedenti attività di Recommendations Classic e le attività Consigli in [!DNL Target] Premium.
title: Qual è la differenza tra Recommendations Classic e la funzione Consigli in [!DNL Target] Premium?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 07548155-9548-4870-b886-6cb4ff37a0bd
TQID: 'https://experienceleague.adobe.com/EoTkyY0kOwRKT52WIwOuTCoUziIJOnNtTo6llsTNpsM'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 19%
---
# Confronto tra Recommendations Classic e le attività Consigli di [!DNL Target] Premium {#classic-versus-activities}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri le differenze tra [!DNL Recommendations Classic] e [!DNL Recommendations] attività in [!DNL Target Premium], per scegliere tra di esse.

>[!ENDSHADEBOX]

>[!NOTE]
>
>Le attività di [!DNL Recommendations] sono disponibili come parte della soluzione [!DNL Target Premium]. Non sono disponibili in [!DNL Target Standard] senza una licenza [!DNL Target Premium].

Nel prodotto classico [!DNL Recommendations], la visualizzazione dei consigli passava attraverso la creazione di una mbox di raccolta dei dati su una pagina e l&#39;aggiunta di una mbox di visualizzazione in una posizione specifica della pagina. L&#39;attività [!DNL Recommendations] in [!DNL Target Premium] raccoglie le informazioni sui visitatori e crea i consigli in qualsiasi punto della pagina, senza una mbox per ogni posizione in cui sono consigliati prodotti o contenuti. Un riferimento JavaScript nell’intestazione della pagina consente di abilitare i consigli in qualsiasi punto della pagina. Questo riferimento passa le chiavi, come le chiavi `entity.id` e `entity.categoryId`, alla mbox [!DNL Target] globale.

[!DNL Recommendations Classic] ha la propria scheda nell’interfaccia utente di [!DNL Experience Cloud]. Un’attività di [!DNL Recommendations] è disponibile all’interno del flusso di lavoro di [!DNL Target Premium].

Gli utenti [!DNL Recommendations Classic] possono continuare a utilizzare le mbox [!DNL Recommendations] in [!DNL Target Recommendations]. È inoltre possibile combinare l&#39;approccio classico e quello [!DNL Target], mantenendo le mbox e utilizzando il codice JavaScript nell&#39;intestazione per attivare la funzionalità [!DNL Recommendations] per gli altri elementi della pagina. Per ottenere la funzionalità completa di [!DNL Target], tuttavia, [!DNL Recommendations Classic] utenti potrebbero preferire eliminare la vecchia mbox e affidarsi esclusivamente a [!DNL Target Recommendations].

L&#39;attività [!DNL Recommendations] in [!DNL Target] migliora [!DNL Recommendations Classic] nelle seguenti aree principali.

## Consigli come offerta {#recs-as-offer}

I consigli possono essere inclusi nelle attività [!UICONTROL Test A/B] (tra cui [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico]) e [!UICONTROL Targeting esperienza] (XT). Questo consente, tra l’altro, di testare e indirizzare contenuti di consigli e non di consigli all’interno della stessa attività. Per ulteriori informazioni, consulta [Consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md).

## Criteri {#criteria-comparison}

[!DNL Target Recommendations] include una libreria di criteri con insiemi preconfigurati di regole e configurazioni. In [!DNL Recommendations Classic] ogni consiglio è stato creato manualmente compilando un modulo e scegliendo da un lungo elenco di regole. Quando si crea un&#39;attività [!DNL Recommendations], viene scelto un set di criteri preconfigurato. È ancora possibile creare consigli personalizzati, ma la libreria di criteri contiene molte delle configurazioni più comuni, precompilate per semplificare il processo e utilizzando un linguaggio chiaro per tutti. I criteri precompilati possono essere utilizzati così come sono, oppure copiati e modificati per soddisfare esigenze specifiche.

![Diapositiva che mostra una scheda dei criteri, Up-Sell, con il linguaggio comprensibile, le regole e la logica, e la configurazione etichettata](assets/overview_criteria.png)

I criteri sono preconfigurati e ordinati per settori verticali, tipi di pagina e implementazione. Ad esempio, i criteri che si applicano al verticale di vendita al dettaglio possono essere trovati per l&#39;utilizzo in una pagina del prodotto, mostrando prodotti all&#39;interno di una particolare categoria (come definito dal parametro `entity.categoryID`).

Per ulteriori informazioni sull’utilizzo e la creazione dei criteri, vedi [Criteri](/help/main/c-recommendations/c-algorithms/algorithms.md).

## Flusso di lavoro {#workflow-comparison}

Il flusso di lavoro [!DNL Recommendations] è semplificato. Invece di moduli complicati, un flusso di lavoro visivo guida i passaggi seguenti:

1. Selezionare i criteri.
1. Seleziona una [progettazione](/help/main/c-recommendations/c-design-overview/create-design.md#create-design) preconfigurata.
1. Visualizzare in anteprima i consigli risultanti.

## Anteprima visiva {#visual-preview}

I consigli possono essere visualizzati in anteprima dopo la loro configurazione e dopo aver apportato le modifiche necessarie, senza creare i consigli nella pagina e testarli. Le anteprime sono disponibili all&#39;interno di [!DNL Target].

## Targeting {#targeting-comparison}

[!DNL Recommendations Classic] aveva sei opzioni di targeting. [!DNL Recommendations] attività utilizzano l&#39;intera gamma di [!DNL Target] opzioni di targeting. Un pubblico è definito utilizzando [!DNL Target] o altri tipi di pubblico [!DNL Adobe Experience Cloud] (ad esempio [!DNL Audience Manager] e [!DNL Analytics]). Viene quindi selezionata la percentuale di partecipanti all&#39;attività che visualizzano ogni progetto e la percentuale di partecipanti che visualizzano il controllo.

![Diagramma di flusso con il pubblico Tutti i visitatori, i criteri di up-selling, tre design con il 30% del traffico ciascuno e il gruppo di controllo Nessun consiglio](assets/overview_targeting.png)

## Generazione di rapporti {#reporting-comparison}

In [!DNL Target], [!DNL Recommendations] fornisce funzionalità migliorate di generazione rapporti che sfruttano le funzionalità di [!DNL Target] e [!DNL Experience Cloud]. Anziché mostrare solo l&#39;incremento fornito da [!DNL Recommendations] rispetto ai risultati senza di essi, i rapporti mostrano informazioni complete sull&#39;attività di [!DNL Recommendations].

