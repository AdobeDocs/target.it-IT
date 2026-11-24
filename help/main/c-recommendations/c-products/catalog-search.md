---
keywords: catalogo ricerca;catalogo;ricerca;esclusione;raccolta;filtro;consigli;catalog search;search;exclusion;collection;filter;recommendations
description: Scopri come utilizzare [!DNL Recommendations] [!UICONTROL Ricerca nel catalogo] per individuare prodotti o contenuti, rimuovere elementi dal catalogo e altro ancora.
title: Come si utilizza [!DNL Recommendations] [!UICONTROL Ricerca nel catalogo]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 925fea97-e2c5-4883-84e3-fd357a8ee8d9
TQID: 'https://experienceleague.adobe.com/en3hkFsDjEE86Tc-3vPSiZFy0K47SftZMN6RW0INNic'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 3883dc9752db0a2427f70cb3036fe060c440361a
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 7%
---
# [!UICONTROL Ricerca nel catalogo] {#catalog-search}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come cercare nel catalogo in [!DNL Adobe Recommendations] per individuare prodotti o contenuti e come filtrare, visualizzare e rimuovere elementi.

>[!ENDSHADEBOX]

La pagina **[!UICONTROL Ricerca nel catalogo]** in [!DNL Adobe Recommendations] viene utilizzata per individuare i prodotti o il contenuto nel catalogo. L’attività di base in questa pagina è quella di cercare un elemento. La pagina consente inoltre di modificare l’ambiente, filtrare i facet, modificare le colonne della tabella e altro ancora.

Il catalogo è l’intero set di prodotti (entità). Può contenere molte raccolte, che organizzano i prodotti in gruppi logici.

L&#39;indice del catalogo viene creato automaticamente al caricamento del primo feed e aggiornato in base alla [pianificazione specificata](/help/main/c-recommendations/c-products/feeds.md#steps).

Il catalogo viene aggiornato automaticamente quando si ricevono aggiornamenti tramite file di feed, API o aggiornamenti mbox. In genere, gli aggiornamenti vengono completati entro un’ora. Se sono in corso degli aggiornamenti, viene visualizzata l’ora di inizio dell’aggiornamento più recente. Se non vi sono aggiornamenti in corso, viene visualizzata l’ora di inizio e di fine dell’aggiornamento più recente.

## Ricerca nel catalogo

Utilizzare i risultati della ricerca per esaminare gli elementi nel catalogo e, se necessario, rimuoverne gli elementi.

1. Fai clic su **[!UICONTROL Consigli]** > **[!UICONTROL Ricerca nel catalogo]**.

1. (Facoltativo) Per filtrare i risultati, fai clic sull&#39;icona **[!UICONTROL Mostra filtri]** ( ![Mostra icona filtri](/help/main/assets/icons/Filter.svg) ), quindi seleziona i filtri da applicare. I filtri disponibili sono **[!UICONTROL Ambiente]**, **[!UICONTROL Raccolte]**, **[!UICONTROL Categoria]**, **[!UICONTROL Marchio]**, **[!UICONTROL Inventario]** e **[!UICONTROL Valore]**.

   [Ambienti](/help/main/administrating-target/environments.md) organizzano siti e ambienti di pre-produzione per la gestione e la generazione di rapporti separati. Per modificare l&#39;ambiente, selezionare l&#39;ambiente desiderato dall&#39;elenco a discesa **[!UICONTROL Ambiente]**.

   ![Pagina Ricerca nel catalogo con il pannello dei filtri evidenziato: Raccolte, Categoria, Marchio, Inventario, Valore e Ricerca avanzata](../assets/catalog_search.png)

1. Digitare un termine di ricerca nel campo **[!UICONTROL Cerca in]**.

1. (Facoltativo) Affina la ricerca selezionando un&#39;opzione di ricerca dal menu delle opzioni, che si apre dalla freccia giù nel campo **[!UICONTROL Cerca in]**.

   Le opzioni di ricerca includono:

   * ID
   * Nome
   * Messaggio

1. Fai clic sull&#39;icona **[!UICONTROL Personalizza tabella]** ( ![Icona Personalizza tabella](/help/main/assets/icons/ColumnSetting.svg) ) per modificare le colonne attive nella pagina **[!UICONTROL Ricerca nel catalogo]**.

   ![Pagina Ricerca nel catalogo con l&#39;icona Personalizza tabella evidenziata](../assets/catalog_search_4.png)

1. Scorrere gli elementi nei risultati della ricerca per visualizzare miniature e altre informazioni sul prodotto.

   >[!NOTE]
   >
   >In una ricerca nel catalogo per un attributo personalizzato con un valore numerico, l’attributo personalizzato viene considerato come di tipo stringa anziché come valore numerico.
   >
   >Il tipo di un attributo non può essere modificato. Per richiedere una modifica, [apri un problema cliente](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) facendo riferimento agli attributi il cui tipo deve passare da stringa a numerico.

1. Fai clic su un elemento nei risultati della ricerca per visualizzarne i dettagli, tra cui ID, nome, messaggio, categoria e altro ancora.

   ![Dettagli di un elemento del catalogo con ID, categorie, margine e altri attributi](../assets/catalog_search_2.png)

1. Per rimuovere l&#39;elemento dal catalogo, fare clic su **[!UICONTROL Rimuovi dal catalogo]**.

   Tutte le informazioni sull&#39;elemento vengono quindi rimosse dall&#39;indice del catalogo. L’elemento viene incluso nuovamente nel catalogo solo se viene aggiunto nuovamente in un feed di dati. Anche un elemento eliminato deve essere eliminato separatamente dai feed.

   ![Dettagli di un elemento del catalogo con il pulsante Rimuovi dal catalogo evidenziato](../assets/catalog_search_3.png)

<!--
### Perform an advanced search {#advanced-search}

You can use [!UICONTROL Advanced Search] to further refine your search results or to save your search results as a [collection](/help/main/c-recommendations/c-products/collections.md) or [exclusion](/help/main/c-recommendations/c-products/exclusions.md).

1. Click the **[!UICONTROL Advanced Search]** link.

   ![Advanced Search page](/help/main/c-recommendations/c-products/assets/advances-search.png)

1. Use the drop-down lists to specify the parameter, operator, and values for your search.

1. (Optional) Click **[!UICONTROL Add Rule]** to add an additional search rule.

   Each additional search rule is joined with the AND operator.

1. Click **[!UICONTROL Search]**.

1. (Optional) Click **[!UICONTROL Save As]**, then click **[!UICONTROL Collection]** or **[!UICONTROL Exclusion]**.

   ![Save as options](/help/main/c-recommendations/c-products/assets/save-as.png)

   For more information, see [Create a collection or exclusion based on Advanced Search](#save-as) below.
-->

<!--
## Modify the Catalog Search page (filters and columns)

You can temporarily modify the available filters and columns on the [!UICONTROL Catalog Search] page for the current session.

### Modify filters

You can add additional filter facets to the [!UICONTROL Catalog Search] page.

1. In the **[!UICONTROL Filters]** panel, click **[!UICONTROL Modify]**.

   ![Modify filters link](/help/main/c-recommendations/c-products/assets/modify-filters.png)

1. Select the desired search facets (ID, name, message, etc.), then click **[!UICONTROL Save]**.

   ![Add filters](/help/main/c-recommendations/c-products/assets/add-filters.png)

Keep in mind that the additional filter facets are available in the current session only.
-->



<!--
## Create a collection or exclusion based on Advanced Search {#save-as}

You can create [collections](/help/main/c-recommendations/c-products/collections.md) or [exclusions](/help/main/c-recommendations/c-products/exclusions.md) using [!UICONTROL Advanced Search] on the [!UICONTROL Catalog Search] page ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

1. Perform an [advanced search](#advanced-search).

1. Click **[!UICONTROL Save As]**, then click **[!UICONTROL Collection]** or **[!UICONTROL Exclusion]**.

   ![Save as options](/help/main/c-recommendations/c-products/assets/save-as.png)

   >[!IMPORTANT]
   >
   >The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create collections or exclusions based on results using the [!UICONTROL Advanced Search] functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create a catalog with the intent to return products containing "holiday," only products containing "holiday" are returned. Products containing "Holiday" are not returned. Exclusions are handled in a similar fashion.
-->
