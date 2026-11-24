---
keywords: consigli;consigli attività;criteri;algoritmo;chiave consiglio;chiave personalizzata;settore verticale;commercio al dettaglio;eccommerce;generazione lead;b2b;servizi finanziari;media;publishing;recommendations activity;criteria;algorithm;recommendations key;custom key;industry vertical;retail;eccommerce;lead generation;b2b;financial services;media;publishing
description: Scopri come utilizzare i criteri in Adobe [!DNL Target] [!DNL Recommendations].
title: Come si utilizzano i criteri nei consigli di [!DNL Target]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: a6e4c857-f991-4293-9d33-8d7c2ca5dade
TQID: 'https://experienceleague.adobe.com/Wo7I3piBQ7zwYF7kqRphDeWjcBCpyvIvTkwKK0t0f9U'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f7c7de77-382f-4f48-8b36-61a170f06d3d
    internal-label: Integrations
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 5%
---
# Introduzione a [!UICONTROL Criteri] {#get-started-criteria}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come funzionano i criteri in [!DNL Adobe Target Recommendations] e quali sono le opzioni di settore verticale, algoritmo e chiave consiglio disponibili.

>[!ENDSHADEBOX]

**[!UICONTROL I criteri]** in [!DNL Adobe Target] [!DNL Recommendations] sono regole che determinano quali prodotti o contenuti consigliare in base a un set predeterminato di comportamenti dei visitatori. I criteri possono essere basati sulle tendenze popolari, sui comportamenti attuali e passati di un visitatore o su prodotti e contenuti simili. È possibile aggiungere più criteri a un’attività per sottoporre a test reciproci più tipi di consigli.

Il settore verticale e il tipo di algoritmo selezionati determinano le opzioni disponibili al momento della creazione dei criteri.

## Settore verticale {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

Quando si creano i criteri, viene selezionata una verticale di settore in base agli obiettivi dell’attività Consigli.

| Settore verticale | Obiettivo |
|--- |--- |
| **[!UICONTROL Vendita al dettaglio/e-commerce]** | Conversione con conseguente acquisto |
| **[!UICONTROL Generazione lead/B2B/Servizi finanziari]** | Conversione senza acquisto |
| **[!UICONTROL File multimediali/Pubblicazione]** | Coinvolgimento |

Altre opzioni di criteri cambiano in base al settore verticale selezionato. Il settore verticale predefinito può essere impostato nella pagina **[!UICONTROL Amministrazione]** > **[!UICONTROL Consigli]** oppure è possibile specificare il settore verticale per ciascun criterio.

## Tipo di algoritmo {#section_885B3BB1B43048A88A8926F6B76FC482}

Il tipo di algoritmo selezionato determina quelli disponibili. Nella tabella seguente sono illustrati i tipi di algoritmo e i relativi algoritmi.

| Tipo di algoritmo | Quando utilizzare | Algoritmi disponibili |
| --- | --- | --- |
| **[!UICONTROL Basato su carrello]** | Creare consigli in base al contenuto del carrello dell’utente. | <ul><li>**[!UICONTROL Persone Che Hanno Visualizzato Questi, Hanno Visualizzato Anche]**</li><li>**[!UICONTROL Chi ha visualizzato questi elementi ha acquistato anche]**</li><li>**[!UICONTROL Chi ha acquistato questi, ha acquistato anche]**</li></ul>Per ulteriori informazioni, vedi [In base al carrello](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#cart-based) in *Basare il consiglio su una chiave consiglio*. |
| **[!UICONTROL Basato Sulla Popolarità]** | Puoi formulare raccomandazioni in base alla popolarità complessiva di un elemento nel sito o alla popolarità degli elementi nella categoria, nel brand, nel genere e così via preferiti o più visualizzati dall’utente. | <ul><li>**[!UICONTROL Più visualizzati nel sito]**</li><li>**[!UICONTROL Più visualizzati per categoria]**</li><li>**[!UICONTROL Più visualizzati per attributo elemento]**</li><li>**[!UICONTROL Più visualizzati per attributo profilo]**</li><li>**[!UICONTROL Più venduti nel sito]**</li><li>**[!UICONTROL Più venduti per categoria]**</li><li>**[!UICONTROL Più venduti per attributo articolo]**</li><li>**[!UICONTROL Più venduti per attributo profilo]**</li><li>**[!UICONTROL Primi per metrica di Analytics]**</li></ul> |
| **[!UICONTROL Basato su elemento]** | Creare consigli in base a elementi simili a un elemento attualmente visualizzato o visualizzato di recente dall’utente. | <ul><li>**[!UICONTROL Chi ha visualizzato questo ha visualizzato anche quello]**</li><li>**[!UICONTROL Chi ha visualizzato questo ha acquistato anche quello]**</li><li>**[!UICONTROL Chi ha acquistato questo ha acquistato anche quello]**</li><li>**[!UICONTROL Elementi con attributi simili]**</li></ul> |
| **[!UICONTROL Basato su utente]** | Creare consigli in base al comportamento dell’utente. | <ul><li>**[!UICONTROL Elementi visualizzati di recente]**</li><li>**[!UICONTROL Consigliato per te]**</li></ul> |
| **[!UICONTROL Criteri personalizzati]** | Formulare raccomandazioni in base a un file personalizzato caricato. | <ul><li>Algoritmo personalizzato</li></ul> |

Per ulteriori informazioni su ciascun algoritmo, vedere [Basare il consiglio su una chiave di consiglio](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

## Utilizzare una chiave di consiglio personalizzata {#custom-key}

I consigli possono anche essere basati sul valore di un attributo di profilo personalizzato. Ad esempio, i filmati consigliati possono essere visualizzati in base all’ultimo filmato aggiunto alla coda da un utente.

1. Fai clic su **[!UICONTROL Consigli]** > **[!UICONTROL Criteri]**.

1. Fai clic su **[!UICONTROL Crea criterio]** > **[!UICONTROL Crea criterio]**.

   ![Pagina Criteri con il menu Crea criteri aperto, che mostra Crea criteri e Crea sequenza criteri](../assets/criteria_1.png)

1. Compila le informazioni nella [sezione Informazioni di base](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info).

1. Nella sezione [Algoritmo consigliato](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#rec-algo), seleziona **[!UICONTROL Basato su elemento]** dall&#39;elenco **[!UICONTROL Tipo di algoritmo]**.

1. Seleziona **[!UICONTROL Persone che hanno visualizzato questo/a, che hanno visualizzato]** dall&#39;elenco **[!UICONTROL Algoritmo]**.

1. Seleziona l&#39;attributo di profilo personalizzato dall&#39;elenco **[!UICONTROL Chiave consiglio]** (ad esempio, **[!UICONTROL Ultimo spettacolo aggiunto alla watchlist]**).

   >[!NOTE]
   >
   >I parametri di profilo personalizzati possono essere passati a [!DNL Target] tramite JavaScript, API o integrazioni. Per ulteriori informazioni sugli attributi di profilo personalizzati, consulta [Profili dei visitatori](/help/main/c-target/c-visitor-profile/visitor-profile.md).

   ![Finestra di dialogo Crea criterio che visualizza la sezione Algoritmo di Recommendations con gli elenchi Tipo di algoritmo, Algoritmo e Chiave consiglio](../assets/criteria_2.png)

## Visualizza informazioni sui criteri {#section_7162DE58E4594FD688A4D7FDB829FD8B}

I dettagli dei criteri mostrano come è configurato un criterio e quali attività lo utilizzano.

1. Fai clic su **[!UICONTROL Consigli]** > **[!UICONTROL Criteri]** per visualizzare l&#39;elenco dei criteri.

1. Fare clic sui criteri desiderati nella colonna **[!UICONTROL Nome]**.

1. Visualizza informazioni generali sui criteri selezionati nelle sezioni **[!UICONTROL Attributi]** e Dettagli, inclusi **[!UICONTROL Nome]**, **[!UICONTROL Descrizione]**, **[!UICONTROL Settore verticale]**, **[!UICONTROL Tipi di pagina]**, **[!UICONTROL Chiave consiglio]**, **[!UICONTROL Logica consiglio]**, **[!UICONTROL ID algoritmo]** e Informazioni ultima modifica (data e chi ha modificato l&#39;algoritmo).

1. Visualizza l&#39;elenco delle attività che fanno riferimento ai criteri selezionati nella sezione **[!UICONTROL Utilizzo]**.

   >[!NOTE]
   >
   >La funzionalità **[!UICONTROL Utilizzo algoritmo]** è attualmente supportata solo per [!DNL Recommendations] attività. Questa funzionalità non è attualmente supportata per **[!UICONTROL Test A/B]**, **[!UICONTROL Allocazione automatica]**, **[!UICONTROL Targeting automatico]** e **[!UICONTROL Attività di Targeting esperienza]** (XT) che includono [consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md).

   ![Dettagli dei criteri con le sezioni Attributi e dettagli ed evidenziata la sezione Utilizzo](../assets/criteria_3.png)
