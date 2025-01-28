---
keywords: consigli;consigli attività;criteri;algoritmo;chiave consiglio;chiave personalizzata;settore verticale;commercio al dettaglio;eccommerce;generazione lead;b2b;servizi finanziari;media;publishing;recommendations activity;criteria;algorithm;recommendations key;custom key;industry vertical;retail;eccommerce;lead generation;b2b;financial services;media;publishing
description: Scopri come utilizzare i criteri in Adobe [!DNL Target] [!DNL Recommendations].
title: Come si utilizzano i criteri in  [!DNL Target] Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
hide: true
hidefromtoc: true
exl-id: 7809984d-259d-4b99-93cd-3073e2fcf8bb
source-git-commit: b7c7e8d85f7f39024ed5e57177e5c9f628460e9c
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 5%

---

# [!UICONTROL Criteria]

[!UICONTROL Criteria] in [!DNL Adobe Target] [!DNL Recommendations] sono regole che determinano quali prodotti o contenuti consigliare in base a un set predeterminato di comportamenti dei visitatori. I criteri possono essere basati sulle tendenze popolari, sui comportamenti attuali e passati di un visitatore o su prodotti e contenuti simili. È possibile sottoporre e test più tipi di consigli tra loro aggiungendo più criteri.

Nelle sezioni seguenti vengono fornite ulteriori informazioni sulle chiavi di criteri e sulla logica per i consigli che è possibile utilizzare per ogni chiave. Fai clic sui collegamenti per ulteriori informazioni.

## Settore verticale {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

Durante la creazione di un criterio, selezioni un settore verticale in base agli obiettivi dell’attività Consigli.

| Settore verticale | Obiettivo |
|--- |--- |
| [!UICONTROL Retail/Ecommerce] | Conversione con conseguente acquisto |
| [!UICONTROL Lead Generation/B2B/Financial Services] | Conversione senza acquisto |
| [!UICONTROL Media/Publishing] | Coinvolgimento |

Altre opzioni di criteri cambiano in base al settore verticale selezionato. È possibile impostare il settore verticale predefinito nella pagina **[!UICONTROL Administration]>[!UICONTROL Recommendations]** oppure specificare il settore verticale per ciascun criterio.

## Tipo di algoritmo {#section_885B3BB1B43048A88A8926F6B76FC482}

Il tipo di algoritmo selezionato determina quelli disponibili.

Nella tabella seguente sono illustrati i vari tipi di algoritmi e i relativi algoritmi.

| Tipo di algoritmo | Quando utilizzare | Algoritmi disponibili |
| --- | --- | --- |
| [!UICONTROL Cart-Based] | Creare consigli in base al contenuto del carrello dell’utente. | <ul><li>[!UICONTROL People Who Viewed These, Also Viewed]</li><li>[!UICONTROL People Who Viewed These, Also Bought]</li><li>[!UICONTROL People Who Bought These, Also Bought]</li></ul>Per ulteriori informazioni, vedi [In base al carrello](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#cart-based) in *Basare il consiglio su una chiave consiglio*. |
| [!UICONTROL Popularity-Based] | Puoi formulare raccomandazioni in base alla popolarità complessiva di un elemento nel tuo sito o in base alla popolarità degli elementi nella categoria, nel brand, nel genere e così via preferiti o più visualizzati di un utente. | <ul><li>[!UICONTROL Most Viewed Across the Site]</li><li>[!UICONTROL Most Viewed by Category]</li><li>[!UICONTROL Most Viewed by Item Attribute]</li><li>[!UICONTROL Top Sellers Across the Site]</li><li>[!UICONTROL Top Sellers by Category]</li><li>[!UICONTROL Top Sellers by Item Attribute]</li><li>[!UICONTROL Top by Analytics Metric]</li></ul> |
| [!UICONTROL Item-Based] | Creare consigli in base alla ricerca di elementi simili a quelli di un elemento attualmente visualizzato dall’utente o che è stato recentemente visualizzato. | <ul><li>[!UICONTROL People Who Viewed This, Viewed That]</li><li>[!UICONTROL People Who Viewed This, Bought That]</li><li>[!UICONTROL People Who Bought This, Bought That]</li><li>[!UICONTROL Items with Similar Attributes]</li></ul> |
| [!UICONTROL User-Based] | Creare consigli in base al comportamento dell’utente. | <ul><li>[!UICONTROL Recently Viewed Items]</li><li>[!UICONTROL Recommended for You]</li></ul> |
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

## Visualizzazione delle informazioni sui criteri {#section_7162DE58E4594FD688A4D7FDB829FD8B}

È possibile visualizzare i dettagli dei criteri facendo clic sui criteri desiderati nella colonna [!UICONTROL Name].

Le sezioni **[!UICONTROL Attributes]** e Details consentono di visualizzare informazioni generali sui criteri selezionati, incluse le informazioni relative a [!UICONTROL Name], [!UICONTROL Description], [!UICONTROL Industry Vertical], [!UICONTROL Page Types], [!UICONTROL Recommendation Key], [!UICONTROL Recommendation Logic], [!UICONTROL Algorithm ID] e Ultima modifica (data e autore della modifica dell&#39;algoritmo).

La sezione **[!UICONTROL Usage]** ti consente di visualizzare un elenco di attività che fanno riferimento ai criteri selezionati.

>[!NOTE]
>
>La funzionalità [!UICONTROL Algorithm Usage] è attualmente supportata solo per le attività [!DNL Recommendations]. Questa funzionalità non è attualmente supportata per le attività [!UICONTROL A/B Test], [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target] e [!UICONTROL Experience Targeting] (XT) che includono [consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md).
