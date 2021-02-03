---
keywords: raccomandazioni;attività di raccomandazione;criteri;algoritmo;chiave di raccomandazione;chiave personalizzata;settore verticale;retail;e-commerce;generazione di lead;b2b;servizi finanziari;media;pubblicazione
description: I criteri in  Adobe Target sono regole che determinano quali prodotti o contenuti consigliare in base a un insieme predeterminato di comportamenti dei visitatori.
title: Criteri in Target Recommendations
feature: Recommendations
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 52%

---


# ![PREMIUM](/help/assets/premium.png) Criteri

I criteri in [!DNL Adobe Target] sono regole che determinano quali prodotti o contenuti consigliare in base a un insieme predeterminato di comportamenti dei visitatori. I criteri possono essere basati sulle tendenze popolari, sui comportamenti attuali e passati di un visitatore o su prodotti e contenuti simili. È possibile sottoporre e test più tipi di consigli tra loro aggiungendo più criteri.

Nelle sezioni seguenti vengono spiegate ulteriori informazioni sulle chiavi dei criteri e sulla logica delle raccomandazioni che potete utilizzare per ogni chiave. Fate clic sui collegamenti per ulteriori informazioni.

## Settore verticale {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

Durante la creazione di un criterio, potete selezionare un settore verticale in base agli obiettivi dell&#39;attività delle raccomandazioni.

| Settore verticale | Obiettivo |
|--- |--- |
| Retail/E-commerce | Conversione con conseguente acquisto |
| Generazione di lead/B2B/servizi finanziari | Conversione senza acquisto |
| Media/Editoria | Coinvolgimento |

Le altre opzioni dei criteri vengono modificate in base al settore verticale selezionato. È possibile impostare il settore verticale predefinito sulla pagina **[!UICONTROL Recommendations > Settings]** oppure specificare il settore verticale per ogni criterio.

## Chiave raccomandazione {#section_885B3BB1B43048A88A8926F6B76FC482}

La chiave dei consigli selezionata determina il tipo di criterio. Esistono diversi tipi di criteri che vengono rappresentati come schede di criteri quando imposti un’attività di [!DNL Recommendations].

![Pagina Criteri](/help/c-recommendations/c-algorithms/assets/criteria-page.png)

Nella tabella seguente sono illustrati i vari tipi di criteri e le relative chiavi di accompagnamento. Fate clic sui collegamenti per ulteriori informazioni su ciascuna chiave.

| Tipo di criteri | Chiavi |
|--- |--- |
| Attività sulla pagina corrente | Consiglia gli elementi o articoli in base alle azioni degli utenti sulla pagina corrente. Ad esempio, i visitatori che visualizzano un particolare elemento potrebbero volerne consultare altri della stessa categoria.<ul><li>[Elemento corrente](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#current-item)</li><li>[Categoria corrente](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#current-category)</li></ul> |
| Personalizzato | Consiglia gli elementi o articoli in base agli attributi personalizzati.<ul><li>[Attributo personalizzato](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#custom)</li></ul>Quando basi i consigli su attributi personalizzati, seleziona l&#39;attributo personalizzato, quindi il tipo di consiglio. |
| Comportamento passato | Consiglia gli articoli in base alle reazioni passate dei visitatori a un articolo. Per esempio, chi ha già acquistato un articolo di una data marca sarà più propenso ad acquistare un altro articolo della stessa marca.<ul><li>[Ultimo articolo acquistato](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#last-purchased)</li><li>[Ultimo articolo visualizzato](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#last-viewed)</li><li>[Articolo più visualizzato](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#most-viewed-logic)</li><li>[Categoria preferita](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#favorite-category)</li></ul> |
| Popolarità | Consiglia gli articoli più popolari, ad esempio i video più popolari in una categoria correlata o i prodotti visualizzati più spesso sul sito.<ul><li>[Popolarità](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#popularity)</li></ul> |
| [Articoli visualizzati di recente](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#recently-viewed) | Raccomanda gli elementi che un visitatore ha visualizzato più di recente, ad esempio gli elementi che un visitatore ha visualizzato l&#39;ultima volta che ha visitato il sito, o gli articoli con tendenze più elevate al momento. |

## Utilizzo di una chiave di raccomandazione personalizzata {#custom-key}

Potete anche basare le raccomandazioni sul valore di un attributo di profilo personalizzato.

>[!NOTE]
>
>I parametri di profilo personalizzati possono essere passati a Target tramite JavaScript, API o integrazioni. Per ulteriori informazioni sugli attributi di profilo personalizzati, vedere [Profili visitatore](/help/c-target/c-visitor-profile/visitor-profile.md).

Ad esempio, se desiderate visualizzare i filmati consigliati in base al filmato aggiunto più di recente da un utente alla coda,

1. Selezionate l&#39;attributo di profilo personalizzato dall&#39;elenco a discesa [!UICONTROL Chiave raccomandazione] (ad esempio, [!UICONTROL Ultima visualizzazione aggiunta a Elenco di controllo]).

1. Selezionare la logica [!UICONTROL di raccomandazione] (ad esempio, [!UICONTROL Chi ha visualizzato questo, l&#39;ha visualizzata]).

   ![Crea nuovo criterio, finestra di dialogo](/help/c-recommendations/c-algorithms/assets/custom-key1.png)

Se l&#39;attributo di profilo personalizzato non corrisponde direttamente a un singolo ID entità, è necessario spiegare a [!DNL Recommendations] in che modo si desidera che venga rilevata la corrispondenza con un&#39;entità.

Ad esempio, se desiderate visualizzare gli elementi più venduti dal marchio preferito di un utente,

1. Selezionate l&#39;attributo di profilo personalizzato dall&#39;elenco a discesa [!UICONTROL Chiave raccomandazione] (ad esempio, [!UICONTROL Marchio preferito]).

1. Selezionare la [!UICONTROL Logica raccomandazione] che si desidera utilizzare con questa chiave (ad esempio, [!UICONTROL Top Sellers]).

   Viene visualizzata l’opzione [!UICONTROL Raggruppa per valore univoco di].

1. Seleziona l’attributo di entità che corrisponde alla chiave scelta. In questo caso [!UICONTROL Il marchio preferito] corrisponde a `entity.brand`.

   [!DNL Recommendations] genera ora un elenco &quot;Top Sellers&quot; (Venditori principali) per ogni marchio e mostra all&#39;utente l&#39;elenco &quot;Top Sellers&quot; appropriato in base al valore memorizzato nell&#39;attributo  [!UICONTROL Favorite ] Brandprofile (Preferito Branprofile).

   ![Attributo Top Sellers](/help/c-recommendations/c-algorithms/assets/custom-key2.png)

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
| [Recommendations basato su utente](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#user-based) | Raccomanda gli elementi in base alla cronologia di navigazione, visualizzazione e acquisto di ogni visitatore. Tali elementi sono generalmente denominati &quot;Consigliati per l&#39;utente.&quot; |

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

Fai clic sulla scheda **[!UICONTROL Uso dell&#39;Algoritmo]** per visualizzare un elenco di attività che fanno riferimento ai criteri selezionati. La scheda elenca le attività attive, inattive e bozze. Fate clic sugli elenchi a discesa Attività live/Attività inattive/Attività bozza per visualizzare l&#39;intero elenco delle attività che fanno riferimento a tali criteri. Puoi fare clic sul link dell&#39;attività per aprire quella da modificare.

![Utilizzo algoritmo, scheda](/help/c-recommendations/c-algorithms/assets/criteria_usage.png)

>[!NOTE]
>
>La funzione [!UICONTROL Uso dell&#39;algoritmo] è attualmente supportata solo per le attività Recommendations. Al momento questa funzione non è supportata per le attività Test A/B, Allocazione automatica, Destinazione automatica e Targeting delle esperienze (XT) che includono [raccomandazioni come offerta](/help/c-recommendations/recommendations-as-an-offer.md).
