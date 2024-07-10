---
keywords: catalogo ricerca;catalogo;ricerca;esclusione;raccolta;filtro;consigli;catalog search;search;exclusion;collection;filter;recommendations
description: Scopri come utilizzare il [!DNL Recommendations] [!UICONTROL Catalog Search] per individuare prodotti o contenuti, rimuovi elementi dal catalogo e altro ancora.
title: Come si utilizza [!DNL Recommendations] [!UICONTROL Catalog Search]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Recommendations
hide: true
hidefromtoc: true
exl-id: 6b0175b1-0eee-498d-8a08-513cf6695114
source-git-commit: 16a7c11e8b9b1a08b1e467519f997d0b05e47529
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 21%

---

# [!UICONTROL Catalog Search]

Il [!UICONTROL Catalog Search] pagina in [!DNL Adobe Recommendations] consente di individuare i prodotti o i contenuti nel catalogo. L&#39;operazione di base che è possibile eseguire in questa pagina è la ricerca di un elemento. Inoltre, puoi modificare l’ambiente, filtrare i facet, modificare le colonne della tabella, aggiungere nuovi facet di ricerca e altro ancora.

I cataloghi si riferiscono all’intero set di prodotti (entità). Il catalogo può contenere molte raccolte, un modo per organizzare i prodotti in contenitori logici.

## Accesso [!UICONTROL Catalog Search]

Per accedere al [!UICONTROL Catalog Search] pagina, fai clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Catalog Search]**.

![Pagina Ricerca nel catalogo](/help/main/c-recommendations/c-products/assets/catalog-search-new.png)

## Eseguire una ricerca semplice

1. Digita un termine di ricerca nel **[!UICONTROL Search In]** campo.

1. (Facoltativo) Per perfezionare la ricerca, seleziona un’opzione di ricerca dal menu delle opzioni che viene visualizzato quando fai clic sulla freccia rivolta verso il basso nel [!UICONTROL Search In] campo.

   Le opzioni di ricerca includono:

   * ID
   * Nome
   * Messaggio

1. Scorrere gli elementi nei risultati della ricerca per visualizzare miniature e altre informazioni sul prodotto.

   >[!NOTE]
   >
   > Quando esegui sul catalogo la ricerca di un attributo personalizzato con un valore numerico, l’attributo personalizzato viene considerato come di tipo stringa anziché come valore numerico.
   >
   >Al momento non è disponibile alcuna funzionalità che consenta di modificare il tipo di un attributo. Per apportare una modifica, [apri un problema cliente](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) facendo riferimento agli attributi che richiedono la modifica del tipo da stringa a numerico.

   Puoi anche utilizzare i filtri per trovare i prodotti desiderati. Ad esempio, facendo clic su **[!UICONTROL Show Filters]** icona ( ![Icona Mostra filtri](/help/main/c-recommendations/c-products/assets/icon-show-filters.png) ), espansione della [!UICONTROL Collections] facet, quindi selezionando una o più raccolte, vengono visualizzati tutti i prodotti appartenenti alle raccolte selezionate nel catalogo.

<!-- ### Perform an advanced search {#advanced-search}

You can use [!UICONTROL Advanced Search] to further refine your search results or to save your search results as a [collection](/help/main/c-recommendations/c-products/collections.md) or [exclusion](/help/main/c-recommendations/c-products/exclusions.md).

1. Click the **[!UICONTROL Advanced Search]** link.

   ![Advanced Search page](/help/main/c-recommendations/c-products/assets/advances-search.png)

1. Use the drop-down lists to specify the parameter, operator, and values for your search.

1. (Optional) Click **[!UICONTROL Add Rule]** to add an additional search rule.

   Each additional search rule is joined with the AND operator.

1. Click **[!UICONTROL Search]**.

1. (Optional) Click **[!UICONTROL Save As]**, then click **[!UICONTROL Collection]** or **[!UICONTROL Exclusion]**.

   ![Save as options](/help/main/c-recommendations/c-products/assets/save-as.png)

   For more information, see [Create a collection or exclusion based on Advanced Search](#save-as) below.-->

## Visualizzare i dettagli di un elemento

Puoi visualizzare i dettagli di un singolo elemento, tra cui ID, nome, messaggio, categoria e altro ancora, visualizzandone i dettagli.

1. Fare clic su un elemento nei risultati della ricerca per visualizzarne i dettagli.

## Rimuovere un elemento dal catalogo

1. Fare clic su un elemento nei risultati della ricerca per visualizzarne i dettagli.

1. Clic **[!UICONTROL Remove from Catalog]**.

1. Confermare la rimozione dell&#39;elemento.

Tutte le informazioni sull&#39;elemento vengono rimosse dall&#39;indice del catalogo. L’elemento verrà incluso nel catalogo solo se viene aggiunto nuovamente in un feed di dati. Un elemento eliminato deve essere eliminato separatamente dai feed.

## Aggiorna il catalogo

L’indice del catalogo viene creato automaticamente al caricamento del primo feed e aggiornato in base al [pianificazione specificata](/help/main/c-recommendations/c-products/feeds.md#steps).

Il catalogo viene aggiornato automaticamente quando si ricevono aggiornamenti tramite file di feed, API o aggiornamenti di mbox. In genere, gli aggiornamenti vengono completati entro un’ora. Se sono in corso degli aggiornamenti, viene visualizzata l’ora di inizio dell’aggiornamento più recente. Se non vi sono aggiornamenti in corso, viene visualizzata l’ora di inizio e di fine dell’aggiornamento più recente.

<!-- ## Create a collection or exclusion based on Advanced Search {#save-as}

You can create [collections](/help/main/c-recommendations/c-products/collections.md) or [exclusions](/help/main/c-recommendations/c-products/exclusions.md) using [!UICONTROL Advanced Search] on the [!UICONTROL Catalog Search] page ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

1. Perform an [advanced search](#advanced-search).

1. Click **[!UICONTROL Save As]**, then click **[!UICONTROL Collection]** or **[!UICONTROL Exclusion]**.

   ![Save as options](/help/main/c-recommendations/c-products/assets/save-as.png)

   >[!IMPORTANT]
   >
   >The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create collections or exclusions based on results using the [!UICONTROL Advanced Search] functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create a catalog with the intent to return products containing "holiday," only products containing "holiday" are returned. Products containing "Holiday" are not returned. Exclusions are handled in a similar fashion.-->

## Modificare l’ambiente

[Ambienti](/help/main/administrating-target/environments.md) consente di organizzare i siti e gli ambienti di preproduzione per gestirli facilmente e generare rapporti separati.

1. Fai clic sull’icona Mostra filtri ( ![Icona Mostra filtri](/help/main/c-recommendations/c-products/assets/icon-show-filters.png) ).

1. Seleziona l’ambiente desiderato da **[!UICONTROL Environment]** elenco a discesa.

<!-- ## Modify the Catalog Search page (filters and columns)

You can temporarily modify the available filters and columns on the [!UICONTROL Catalog Search] page for the current session.

### Modify filters

You can add additional filter facets to the [!UICONTROL Catalog Search] page.

1. In the **[!UICONTROL Filters]** panel, click **[!UICONTROL Modify]**.

   ![Modify filters link](/help/main/c-recommendations/c-products/assets/modify-filters.png)

1. Select the desired search facets (ID, name, message, etc.), then click **[!UICONTROL Save]**.

   ![Add filters](/help/main/c-recommendations/c-products/assets/add-filters.png)

Keep in mind that the additional filter facets are available in the current session only.-->

## Modifica colonne

È possibile modificare temporaneamente le colonne attive nel [!UICONTROL Catalog Search] pagina.

1. Fai clic su **[!UICONTROL Customize Table]** icona (  ![Icona Personalizza tabella](/help/main/c-recommendations/c-products/assets/icon-customize-table.png) ).

1. Seleziona o deseleziona le colonne desiderate da visualizzare o nascondere.

Eventuali modifiche apportate vengono applicate solo alla sessione corrente.
