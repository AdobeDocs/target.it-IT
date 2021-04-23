---
keywords: consigli;attività consigli;criteri;algoritmo;chiave consiglio;chiave personalizzata;settore verticale;retail;e-commerce;generazione di lead;b2b;servizi finanziari;media;pubblicazione
description: Scopri come utilizzare i criteri in Adobe [!DNL Target] Recommendations. I criteri sono regole che determinano il contenuto da consigliare in base a un set predeterminato di comportamenti dei visitatori.
title: Come si utilizzano i criteri in [!DNL Target] Recommendations?
feature: Consigli
exl-id: a6e4c857-f991-4293-9d33-8d7c2ca5dade
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 52%

---

# ![PREMIUM](/help/assets/premium.png) Criteri

I criteri in [!DNL Adobe Target] sono regole che determinano quali prodotti o contenuti consigliare in base a un set predeterminato di comportamenti dei visitatori. I criteri possono essere basati sulle tendenze popolari, sui comportamenti attuali e passati di un visitatore o su prodotti e contenuti simili. È possibile sottoporre e test più tipi di consigli tra loro aggiungendo più criteri.

Nelle sezioni seguenti vengono illustrate ulteriori informazioni sulle chiavi dei criteri e sulla logica dei consigli che è possibile utilizzare per ogni chiave. Fai clic sui collegamenti per ulteriori informazioni.

## Settore verticale {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

Durante la creazione di un criterio, seleziona un settore verticale in base agli obiettivi dell’attività di consigli.

| Settore verticale | Obiettivo |
|--- |--- |
| Retail/E-commerce | Conversione con conseguente acquisto |
| Generazione di lead/B2B/servizi finanziari | Conversione senza acquisto |
| Media/Editoria | Coinvolgimento |

Altre opzioni di criteri cambiano in base al verticale di settore selezionato. Puoi impostare il settore verticale predefinito nella pagina **[!UICONTROL Recommendations > Impostazioni]** oppure puoi specificare il settore verticale per ogni criterio.

## Chiave consiglio {#section_885B3BB1B43048A88A8926F6B76FC482}

La chiave dei consigli selezionata determina il tipo di criterio. Esistono diversi tipi di criteri che vengono rappresentati come schede di criteri quando imposti un’attività di [!DNL Recommendations].

![Pagina Criteri](/help/c-recommendations/c-algorithms/assets/criteria-page.png)

Nella tabella seguente sono illustrati i vari tipi di criteri e le relative chiavi di accompagnamento. Fai clic sui collegamenti per ulteriori informazioni su ciascuna chiave.

| Tipo di criteri | Chiavi |
|--- |--- |
| Attività sulla pagina corrente | Consiglia gli elementi o articoli in base alle azioni degli utenti sulla pagina corrente. Ad esempio, i visitatori che visualizzano un particolare elemento potrebbero volerne consultare altri della stessa categoria.<ul><li>[Elemento corrente](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#current-item)</li><li>[Categoria corrente](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#current-category)</li></ul> |
| Personalizzato | Consiglia gli elementi o articoli in base agli attributi personalizzati.<ul><li>[Attributo personalizzato](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#custom)</li></ul>Quando basi i consigli su attributi personalizzati, seleziona l&#39;attributo personalizzato, quindi il tipo di consiglio. |
| Comportamento passato | Consiglia gli articoli in base alle reazioni passate dei visitatori a un articolo. Per esempio, chi ha già acquistato un articolo di una data marca sarà più propenso ad acquistare un altro articolo della stessa marca.<ul><li>[Ultimo articolo acquistato](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#last-purchased)</li><li>[Ultimo articolo visualizzato](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#last-viewed)</li><li>[Articolo più visualizzato](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#most-viewed-logic)</li><li>[Categoria preferita](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#favorite-category)</li></ul> |
| Popolarità | Consiglia gli articoli più popolari, ad esempio i video più popolari in una categoria correlata o i prodotti visualizzati più spesso sul sito.<ul><li>[Popolarità](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#popularity)</li></ul> |
| [Articoli visualizzati di recente](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#recently-viewed) | Consiglia gli articoli che un visitatore ha visualizzato più di recente, ad esempio gli articoli che un visitatore ha visualizzato l&#39;ultima volta che ha visitato il tuo sito o gli articoli che hanno la tendenza più elevata al momento. |

## Utilizzo di una chiave di raccomandazione personalizzata {#custom-key}

Puoi anche basare i consigli sul valore di un attributo di profilo personalizzato.

>[!NOTE]
>
>I parametri di profilo personalizzati possono essere trasmessi a Target tramite JavaScript, API o integrazioni. Per ulteriori informazioni sugli attributi di profilo personalizzati, consulta [Profili dei visitatori](/help/c-target/c-visitor-profile/visitor-profile.md).

Ad esempio, si supponga di voler visualizzare filmati consigliati in base al filmato che un utente ha aggiunto più di recente alla coda.

1. Seleziona l’attributo di profilo personalizzato dall’elenco a discesa [!UICONTROL Chiave consiglio] (ad esempio, [!UICONTROL Ultima visualizzazione aggiunta a watchlist]).

1. Seleziona la [!UICONTROL Logica consigli] (ad esempio, [!UICONTROL Persone che hanno visualizzato questo, l&#39;hanno visualizzato]).

   ![Finestra di dialogo Crea nuovo criterio](/help/c-recommendations/c-algorithms/assets/custom-key1.png)

Se l’attributo di profilo personalizzato non corrisponde direttamente a un singolo ID entità, è necessario spiegare a [!DNL Recommendations] come desideri che avvenga la corrispondenza a un’entità.

Ad esempio, supponi di voler visualizzare gli articoli più venduti del marchio preferito di un utente.

1. Seleziona l’attributo di profilo personalizzato dall’elenco a discesa [!UICONTROL Chiave consiglio] (ad esempio, [!UICONTROL Marchio preferito]).

1. Seleziona la [!UICONTROL Logica consigli] che desideri utilizzare con questa chiave (ad esempio, [!UICONTROL Più venduti]).

   Viene visualizzata l’opzione [!UICONTROL Raggruppa per valore univoco di].

1. Seleziona l’attributo di entità che corrisponde alla chiave scelta. In questo caso [!UICONTROL Marchio preferito] corrisponde a `entity.brand`.

   [!DNL Recommendations] ora genera un elenco &quot;Più venduti&quot; per ogni marchio e mostra all’utente l’elenco &quot;Più venduti&quot; appropriato in base al valore memorizzato nell’attributo  [!UICONTROL Favorite ] Brandprofile.

   ![Attributo Più venduti](/help/c-recommendations/c-algorithms/assets/custom-key2.png)

## Criteri/algoritmi {#criteria-algorithms}

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
| [Recommendations basato su utente](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#user-based) | Consiglia gli articoli in base alla cronologia di navigazione, visualizzazione e acquisto di ogni visitatore. Questi articoli sono generalmente denominati &quot;Consigliati per te&quot;. |

>[!NOTE]
>
>Se modifichi i criteri di un consiglio attivo, i dati di rapporto relativi andranno persi.

Puoi anche utilizzare informazioni conosciute aggiuntive su un visitatore per migliorare i consigli.

Tutti i criteri di un giorno vengono eseguiti due volte al giorno. Tutti i criteri di una settimana e più vengono eseguiti una volta al giorno. I criteri di affinità per sito vengono eseguiti una volta al giorno. I criteri di backup vengono eseguiti due volte al giorno.

## Visualizzazione delle informazioni sui criteri {#section_7162DE58E4594FD688A4D7FDB829FD8B}

Per visualizzare i dettagli dei criteri su una scheda a comparsa, passa il mouse su una scheda e fai clic sull&#39;icona Informazioni sulla scheda dei criteri, senza aprirli.

![Passaggio del cursore sulla scheda Criteri](/help/c-recommendations/c-algorithms/assets/criteria_hover.png)

Fai clic sulla scheda **[!UICONTROL Informazioni algoritmo]** per visualizzare le informazioni generali sui criteri selezionati, tra cui Nome, Descrizione, Verticale, Tipo di pagina/e, Chiave/i, Logica Consiglio e ID algoritmo.

![Scheda Informazioni algoritmo](/help/c-recommendations/c-algorithms/assets/criteria_info.png)

Fai clic sulla scheda **[!UICONTROL Uso dell&#39;Algoritmo]** per visualizzare un elenco di attività che fanno riferimento ai criteri selezionati. Nella scheda sono elencate le attività attive, inattive e bozze. Fai clic sugli elenchi a discesa Attività live/Attività inattive/Attività bozza per visualizzare l’intero elenco di attività che fanno riferimento a tali criteri. Puoi fare clic sul link dell&#39;attività per aprire quella da modificare.

![Scheda Utilizzo algoritmo](/help/c-recommendations/c-algorithms/assets/criteria_usage.png)

>[!NOTE]
>
>La funzione [!UICONTROL Uso dell&#39;algoritmo] è attualmente supportata solo per le attività Recommendations. Questa funzione non è attualmente supportata per le attività di test A/B, allocazione automatica, targeting automatico e targeting delle esperienze (XT) che includono [consigli come offerta](/help/c-recommendations/recommendations-as-an-offer.md).
