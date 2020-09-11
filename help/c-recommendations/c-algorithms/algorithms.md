---
keywords: recommendations;recommendations activity;criteria;algorithm;recommendation key;custom key;industry vertical;retail;eccommerce;lead generation;b2b;financial services;media;publishing
description: I criteri di  Adobe Target Recommendations sono regole che determinano quali prodotti raccomandare in base a un insieme predeterminato di comportamenti dei visitatori.
title: Criteri in  Adobe Target Recommendations
feature: criteria
uuid: 738db164-174b-45b8-bb8a-778f6494f1d7
translation-type: tm+mt
source-git-commit: 55f0791bb68fc98e319fa70a647e5168ac72ae1e
workflow-type: tm+mt
source-wordcount: '1135'
ht-degree: 69%

---


# ![PREMIUM](/help/assets/premium.png) Criteri

I criteri sono regole che determinano i prodotti da consigliare in base a un set predeterminato di comportamenti dei visitatori.

I criteri determinano quale azione provocherà quale consiglio. È possibile sottoporre e test più tipi di consigli tra loro aggiungendo più criteri.

## Settore verticale {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

Seleziona un settore verticale in base agli obiettivi dell&#39;attività consigliata. A seconda del settore verticale selezionato,

| Settore verticale | Obiettivo |
|--- |--- |
| Retail/E-commerce | Conversione con conseguente acquisto |
| Generazione di lead/B2B/servizi finanziari | Conversione senza acquisto |
| Media/Editoria | Coinvolgimento |

## Recommendation key {#section_885B3BB1B43048A88A8926F6B76FC482}

La chiave dei consigli selezionata determina il tipo di criterio. Esistono diversi tipi di criteri che vengono rappresentati come schede di criteri quando imposti un’attività di [!DNL Recommendations].

| Tipo di criteri | Chiavi |
|--- |--- |
| Attività sulla pagina corrente | Consiglia gli elementi o articoli in base alle azioni degli utenti sulla pagina corrente. Ad esempio, i visitatori che visualizzano un particolare elemento potrebbero volerne consultare altri della stessa categoria.<ul><li>[Elemento corrente](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#current-item)</li><li>[Categoria corrente](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#current-category)</li></ul> |
| Personalizzato | Consiglia gli elementi o articoli in base agli attributi personalizzati.<ul><li>[Attributo personalizzato](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#custom)</li></ul>Quando basi i consigli su attributi personalizzati, seleziona l&#39;attributo personalizzato, quindi il tipo di consiglio. |
| Comportamento passato | Consiglia gli articoli in base alle reazioni passate dei visitatori a un articolo. Per esempio, chi ha già acquistato un articolo di una data marca sarà più propenso ad acquistare un altro articolo della stessa marca.<ul><li>[Ultimo articolo acquistato](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#last-purchased)</li><li>[Ultimo articolo visualizzato](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#last-viewed)</li><li>[Articolo più visualizzato](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#most-viewed-logic)</li><li>[Categoria preferita](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#favorite-category)</li></ul> |
| Popolarità | Consiglia gli articoli più popolari, ad esempio i video più popolari in una categoria correlata o i prodotti visualizzati più spesso sul sito.<ul><li>[Popolarità](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#popularity)</li></ul> |
| Articoli visualizzati di recente | Consiglia gli articoli che un visitatore ha visto più di recente, ad esempio gli articoli che ha guardato l&#39;ultima volta che ha visitato il tuo sito o gli articoli di tendenza in questo momento.<br>L’algoritmo di visualizzazione degli elementi visualizzati di recente restituisce i risultati specifici dell’attività di un visitatore in un [ambiente](/help/administrating-target/hosts.md). Se due siti appartengono a ambienti diversi e un visitatore passa tra i due siti, l&#39;algoritmo restituisce solo gli elementi visualizzati di recente dal sito appropriato.<br>Questo tipo di criteri non è limitato dalle raccolte.<ul><li>[Articoli visualizzati di recente](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#recently-viewed)</li></ul>**Nota:** non è possibile utilizzare il criterio Articoli visualizzati di recente per i consigli di backup.<br>Puoi filtrare gli articoli o i file multimediali visualizzati di recente in modo che vengano visualizzati solo quelli con uno specifico attributo.<ul><li>I criteri “visualizzati di recente” sono configurabili, come altri criteri nei consigli.</li><li>È possibile utilizzare [raccolte](/help/c-recommendations/c-products/collections.md), [esclusioni](/help/c-recommendations/c-products/exclusions.md) e [inclusioni](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) (incluse le regole speciali per Prezzo e Inventario) proprio come per tutti gli altri criteri.</li></ul>Eventuali casi di utilizzo includono:<ul><li>Una società multinazionale con più business potrebbe avere un visitatore che visualizza elementi in più proprietà digitali. In questo caso, puoi limitare gli articoli visualizzati di recente al solo sito su cui sono stati visualizzati. In tal modo gli articoli visualizzati di recente non saranno visualizzati sugli altri siti della stessa società.</li></ul> |

## Utilizzo di una chiave di raccomandazione personalizzata {#custom-key}

Potete anche basare le raccomandazioni sul valore di un attributo di profilo personalizzato.

>[!NOTE]
>
>I parametri di profilo personalizzati possono essere passati a Target tramite JavaScript, API o integrazioni. Per ulteriori informazioni sugli attributi di profilo personalizzati, consulta Profili [](/help/c-target/c-visitor-profile/visitor-profile.md)visitatore.

Ad esempio, se desiderate visualizzare i filmati consigliati in base al filmato aggiunto più di recente da un utente alla coda,

1. Select your custom profile attribute from the [!UICONTROL Recommendation Key] drop-down list (for example, [!UICONTROL Last Show Added to Watchlist]).

1. Select your [!UICONTROL Recommendation Logic] (for example, [!UICONTROL People Who Viewed This, Viewed That]).

   ![Crea nuovo criterio, finestra di dialogo](/help/c-recommendations/c-algorithms/assets/custom-key1.png)

If your custom profile attribute does not directly match to a single entity ID, it is necessary to explain to [!DNL Recommendations] how you want the match to an entity to occur.

Ad esempio, se desiderate visualizzare gli elementi più venduti dal marchio preferito di un utente,

1. Select your custom profile attribute from the [!UICONTROL Recommendation Key] drop-down list (for example, [!UICONTROL Favorite Brand]).

1. Select the [!UICONTROL Recommendation Logic] you want to use with this key (for example, [!UICONTROL Top Sellers]).

   Viene visualizzata l’opzione [!UICONTROL Raggruppa per valore univoco di].

1. Seleziona l’attributo di entità che corrisponde alla chiave scelta. In this case [!UICONTROL Favorite Brand] matches to `entity.brand`.

   [!DNL Recommendations] genera ora un elenco &quot;Top Sellers&quot; (Venditori principali) per ogni marchio e mostra all&#39;utente l&#39;elenco &quot;Top Sellers&quot; appropriato in base al valore memorizzato nell&#39;attributo del profilo del marchio [!UICONTROL Preferiti] .

   ![Attributo Top Sellers](/help/c-recommendations/c-algorithms/assets/custom-key2.png)

## Criteria/algorithms {#criteria-algorithms}

[!DNL Target Recommendations]In sono utilizzati algoritmi sofisticati per determinare quando le azioni di un visitatore soddisfano i criteri impostati nell&#39;attività. La Chiave consiglio determina le opzioni di logica disponibili.

| Criteri | Descrizione |
|--- |--- |
| [Articoli/Media con attributi simili](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#similar-attributes) | Consiglia articoli o media simili in base all’attività corrente o al comportamento passato del visitatore. |
| [Chi ha visualizzato questo ha visualizzato anche quello](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#viewed-viewed) | Consiglia gli elementi che vengono visualizzati più spesso nella stessa sessione in cui viene visualizzato l’elemento specificato. |
| [Chi ha visualizzato questo ha acquistato anche quello](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#viewed-bought) | Consiglia gli articoli che vengono acquistati più spesso nella stessa sessione in cui viene visualizzato l’articolo specificato. |
| [Chi ha comprato questo ha acquistato anche quello](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#bought-bought) | Consiglia gli articoli che sono acquistati più spesso dai clienti contemporaneamente all’articolo specificato. |
| [Affinità sito](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#site-affinity) | Consiglia gli articoli in base alla certezza di una relazione tra articoli diversi. |
| [Articoli più venduti](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#top-sellers) | Articoli inclusi nella maggioranza degli ordini completati. Più unità dello stesso articolo in un unico ordine vengono conteggiate come un ordine. |
| [Articoli più visualizzati](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#most-viewed) | Articoli o elementi multimediali visualizzati più spesso. |
| [Recommendations basato su utente](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#user-based) | Raccomanda gli elementi in base alla cronologia di navigazione, visualizzazione e acquisto di ogni visitatore. Tali elementi sono generalmente denominati &quot;Consigliati per l&#39;utente.&quot; |

>[!NOTE]
>
>Se modifichi i criteri di un consiglio attivo, i dati di rapporto relativi andranno persi.

Puoi anche utilizzare informazioni conosciute aggiuntive su un visitatore per migliorare i consigli.

Tutti i criteri di un giorno vengono eseguiti due volte al giorno. Tutti i criteri di una settimana e più vengono eseguiti una volta al giorno. I criteri di affinità per sito vengono eseguiti una volta al giorno. I criteri di backup vengono eseguiti due volte al giorno.

## Viewing criteria information {#section_7162DE58E4594FD688A4D7FDB829FD8B}

Per visualizzare i dettagli dei criteri su una scheda a comparsa, passa il mouse su una scheda e fai clic sull&#39;icona Informazioni sulla scheda dei criteri, senza aprirli.

![Passaggio del cursore sulla scheda Criteri](/help/c-recommendations/c-algorithms/assets/criteria_hover.png)

Fai clic sulla scheda **[!UICONTROL Informazioni algoritmo]** per visualizzare le informazioni generali sui criteri selezionati, tra cui Nome, Descrizione, Verticale, Tipo di pagina/e, Chiave/i, Logica Consiglio e ID algoritmo.

![Scheda Informazioni algoritmo](/help/c-recommendations/c-algorithms/assets/criteria_info.png)

Fai clic sulla scheda **[!UICONTROL Uso dell&#39;Algoritmo]** per visualizzare un elenco di attività che fanno riferimento ai criteri selezionati. La scheda elenca le attività attive, inattive e bozze. Fate clic sugli elenchi a discesa Attività live/Attività inattive/Attività bozza per visualizzare l&#39;intero elenco delle attività che fanno riferimento a tali criteri. Puoi fare clic sul link dell&#39;attività per aprire quella da modificare.

![Utilizzo algoritmo, scheda](/help/c-recommendations/c-algorithms/assets/criteria_usage.png)

>[!NOTE]
>
>Al momento la funzione Utilizzo  algoritmo è supportata solo per le attività Recommendations. Al momento questa funzione non è supportata per le attività Test A/B, allocazione automatica, targeting automatico e Targeting delle esperienze (XT) che includono [raccomandazioni come offerta](/help/c-recommendations/recommendations-as-an-offer.md).
