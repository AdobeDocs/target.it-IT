---
keywords: consigli;consigli attività;criteri;algoritmo;chiave consiglio;chiave personalizzata;settore verticale;commercio al dettaglio;eccommerce;generazione lead;b2b;servizi finanziari;media;publishing;recommendations activity;criteria;algorithm;recommendations key;custom key;industry vertical;retail;eccommerce;lead generation;b2b;financial services;media;publishing
description: Scopri come utilizzare i criteri in Adobe [!DNL Target] [!DNL Recommendations].
title: Come si utilizzano i criteri in  [!DNL Target] Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: a6e4c857-f991-4293-9d33-8d7c2ca5dade
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 15%

---

# Criteri

I criteri in [!DNL Adobe Target] [!DNL Recommendations] sono regole che determinano quali prodotti o contenuti consigliare in base a un set predeterminato di comportamenti dei visitatori. I criteri possono essere basati sulle tendenze popolari, sui comportamenti attuali e passati di un visitatore o su prodotti e contenuti simili. È possibile sottoporre e test più tipi di consigli tra loro aggiungendo più criteri.

Nelle sezioni seguenti vengono fornite ulteriori informazioni sulle chiavi di criteri e sulla logica per i consigli da utilizzare per ogni chiave. Fai clic sui collegamenti per ulteriori informazioni.

## Settore verticale {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

Durante la creazione di un criterio, selezioni un settore verticale in base agli obiettivi dell’attività Consigli.

| Settore verticale | Obiettivo |
|--- |--- |
| Retail/E-commerce | Conversione con conseguente acquisto |
| Generazione di lead/B2B/servizi finanziari | Conversione senza acquisto |
| Media/Editoria | Coinvolgimento |

Altre opzioni di criteri cambiano in base al settore verticale selezionato. È possibile impostare il settore verticale predefinito nella pagina **[!UICONTROL Recommendations > Settings]** oppure specificare il settore verticale per ciascun criterio.

## Tipo di algoritmo {#section_885B3BB1B43048A88A8926F6B76FC482}

Il tipo di algoritmo selezionato determina quelli disponibili. Esistono diversi tipi di algoritmo che vengono rappresentati come schede di criteri quando si imposta un&#39;attività [!DNL Recommendations].

![Pagina criteri](assets/criteria-page.png)

Nella tabella seguente sono illustrati i vari tipi di algoritmi e i relativi algoritmi.

| Tipo di algoritmo | Quando utilizzare | Algoritmi disponibili |
| --- | --- | --- |
| [!UICONTROL Cart-Based] | Creare consigli in base al contenuto del carrello dell’utente. | <ul><li>Chi ha visualizzato questi ha visualizzato anche quelli</li><li>Chi ha visualizzato questi ha acquistato anche quelli</li><li>Chi ha comprato questi ha acquistato anche quelli</li></ul>Per ulteriori informazioni, vedi [In base al carrello](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#cart-based) in *Basare il consiglio su una chiave consiglio*. |
| [!UICONTROL Popularity-Based] | Puoi formulare raccomandazioni in base alla popolarità complessiva di un elemento nel tuo sito o in base alla popolarità degli elementi nella categoria, nel brand, nel genere e così via preferiti o più visualizzati di un utente. | <ul><li>Articoli più visualizzati nel sito</li><li>Più visualizzati per categoria</li><li>Più visualizzati per attributo articolo</li><li>Articoli più venduti in tutto il sito</li><li>Articoli più venduti per categoria</li><li>Attributo Articoli più venduti</li><li>Primi per metrica di Analytics</li></ul> |
| [!UICONTROL Item-Based] | Creare consigli in base alla ricerca di elementi simili a quelli di un elemento attualmente visualizzato dall’utente o che è stato recentemente visualizzato. | <ul><li>Chi ha visualizzato questo ha visualizzato anche quello</li><li>Chi ha visualizzato questo ha acquistato anche quello</li><li>Chi ha comprato questo ha acquistato anche quello</li><li>Articoli con attributi simili</li></ul> |
| [!UICONTROL User-Based] | Creare consigli in base al comportamento dell’utente. | <ul><li>Articoli visualizzati di recente</li><li>Consigliato per te</li></ul> |
| [!UICONTROL Custom Criteria] | Formulare raccomandazioni in base a un file personalizzato caricato. | <ul><li>Algoritmo personalizzato</li></ul> |

Per ulteriori informazioni su ciascun algoritmo, vedere [Basare il consiglio su una chiave di consiglio](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

## Utilizzo di una chiave di consiglio personalizzata {#custom-key}

Puoi anche basare i consigli sul valore di un attributo di profilo personalizzato.

>[!NOTE]
>
>I parametri di profilo personalizzati possono essere passati a [!DNL Target] tramite JavaScript, API o integrazioni. Per ulteriori informazioni sugli attributi di profilo personalizzati, consulta [Profili dei visitatori](/help/main/c-target/c-visitor-profile/visitor-profile.md).

Si supponga, ad esempio, di voler visualizzare i filmati consigliati in base all&#39;ultimo filmato aggiunto alla coda da un utente.

1. Fare clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Fare clic su **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**.

1. Compila le informazioni nella [sezione Informazioni di base](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info).

1. Nella sezione [Algoritmo consigliato](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#rec-algo), selezionare **[!UICONTROL Item Based]** dall&#39;elenco **[!UICONTROL Algorithm Type]**.

1. Selezionare **[!UICONTROL People Who Viewed This, Viewed That]** dall&#39;elenco **[!UICONTROL Algorithm]**.

1. Selezionare l&#39;attributo di profilo personalizzato dall&#39;elenco **[!UICONTROL Recommendation Key]** (ad esempio, [!UICONTROL Last Show Added to Watchlist]).

   ![Finestra di dialogo Crea nuovo criterio](assets/custom-key1.png)

## Visualizzazione delle informazioni sui criteri {#section_7162DE58E4594FD688A4D7FDB829FD8B}

Per visualizzare i dettagli dei criteri su una scheda a comparsa, passa il mouse su una scheda e fai clic sull&#39;icona Informazioni sulla scheda dei criteri, senza aprirli.

![Passaggio del cursore sulla scheda Criteri](/help/main/c-recommendations/c-algorithms/assets/criteria_hover.png)

Fare clic sulla scheda **[!UICONTROL Algorithm Info]** per visualizzare informazioni generali sui criteri selezionati, tra cui Nome, Descrizione, Verticale, Tipo di pagina/e, Chiave/i, Logica Consiglio e ID algoritmo.

![Scheda Informazioni algoritmo](/help/main/c-recommendations/c-algorithms/assets/criteria_info.png)

Fare clic sulla scheda **[!UICONTROL Algorithm Usage]** per visualizzare un elenco di attività che fanno riferimento ai criteri selezionati. Nella scheda sono elencate le attività attive, inattive e bozze. Fai clic sugli elenchi a discesa Attività live/Attività inattive/Attività bozza per visualizzare l’intero elenco di attività che fanno riferimento a tali criteri. Puoi fare clic sul link dell&#39;attività per aprire quella da modificare.

![Scheda Utilizzo algoritmo](/help/main/c-recommendations/c-algorithms/assets/criteria_usage.png)

>[!NOTE]
>
>La funzionalità [!UICONTROL Algorithm Usage] è attualmente supportata solo per le attività di Recommendations. Questa funzione non è attualmente supportata per attività di test A/B, allocazione automatica, targeting automatico e targeting delle esperienze (XT) che includono [consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md).
