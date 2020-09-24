---
keywords: catalog;search
description: In Adobe Target la ricerca nel catalogo consente di individuare prodotti o contenuti all’interno del catalogo.
title: Ricerca nel catalogo in Adobe Target
feature: catalog
uuid: e0876963-5905-4850-a615-953e435f26e9
translation-type: tm+mt
source-git-commit: ae002d52aa98d20357b2efad4b008c22ea787aee
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 19%

---


# ![PREMIUM](/help/assets/premium.png) Ricerca nel catalogo {#catalog-search}

The [!UICONTROL Catalog Search] page helps you locate the products or content in your catalog.

I cataloghi si riferiscono all’intero set di prodotti (entità). Il catalogo può contenere molte raccolte, un modo per organizzare i prodotti in raggruppamenti logici.

To access the [!UICONTROL Catalog Search] page, click **[!UICONTROL Recommendations]** > **[!UICONTROL Catalog Search]**.

![Pagina di ricerca del catalogo](/help/c-recommendations/c-products/assets/catalog-search.png)

L&#39;attività più semplice che è possibile eseguire in questa pagina è la ricerca di un elemento. Inoltre, è possibile modificare l&#39;ambiente; salvare i risultati della ricerca nelle raccolte o nelle esclusioni; aggiungere, rimuovere o ridisporre le colonne nella tabella e aggiungere nuovi facet di ricerca al pannello [!UICONTROL Filtri] .

## Cercare un elemento

Potete usare una ricerca semplice o avanzata per individuare gli elementi presenti nel catalogo.

### Eseguire una ricerca semplice

1. Digitate un termine di ricerca nel campo **[!UICONTROL Cerca prodotti]** .

1. (Facoltativo) Per definire meglio la ricerca, selezionare un&#39;opzione di ricerca dal menu delle opzioni che viene visualizzata quando si fa clic sulla freccia rivolta verso il basso nel campo di ricerca.

   ![](assets/searchproductsmenu.png)

   Le opzioni di ricerca includono:

   * TUTTO - Esegue ricerche in tutti gli altri criteri di ricerca, utilizzando la logica OR.
   * Nome
   * Marchio
   * Categoria
   * ID
   * Messaggio

1. Ora puoi scorrere gli elementi nei risultati della ricerca per visualizzare le miniature e altre informazioni sui prodotti.

   L&#39;illustrazione seguente mostra i risultati per &quot;bike&quot; utilizzando l&#39;opzione All.

   ![Catalogo Ricerca bici](/help/c-recommendations/c-products/assets/bike-results.png)

   Il numero visualizzato accanto a &quot;Prodotti&quot; è il numero di prodotti corrispondenti al termine di ricerca, sul totale disponibile nell’ambiente specificato.

   È possibile utilizzare la funzionalità di completamento automatico della ricerca. Nell&#39;illustrazione seguente, digitando &quot;bik&quot; vengono restituiti tutti i prodotti che contengono la parola &quot;bike&quot;.

   ![Ricerca automatica](/help/c-recommendations/c-products/assets/bike-results-2.png)

1. Potete anche usare i filtri per trovare il prodotto desiderato. Nell&#39;esempio seguente, espandendo il facet [!UICONTROL Raccolte] e selezionando &quot;Strumenti bici&quot;, tutti gli strumenti ciclabili nel display del catalogo.

   ![Utensili per biciclette](/help/c-recommendations/c-products/assets/bike-results-3.png)

1. È possibile effettuare ricerche ulteriori nell’elenco dei risultati immettendo un termine di ricerca, ad esempio &quot;catena&quot;.

   ![Cerca catena](/help/c-recommendations/c-products/assets/bike-results-4.png)

### Eseguire una ricerca avanzata {#advanced-search}

Potete utilizzare la ricerca  avanzata per perfezionare ulteriormente i risultati della ricerca o per salvarli come [raccolta](/help/c-recommendations/c-products/collections.md) o [esclusione](/help/c-recommendations/c-products/exclusions.md).

1. Fate clic sul collegamento Ricerca **** avanzata.

   ![Pagina Ricerca avanzata](/help/c-recommendations/c-products/assets/advances-search.png)

1. Utilizzate gli elenchi a discesa per specificare il parametro, l&#39;operatore e i valori della ricerca.

1. (Facoltativo) Fai clic su **[!UICONTROL Aggiungi regola]** per aggiungere una regola di ricerca aggiuntiva.

   Ogni regola di ricerca aggiuntiva viene unita all&#39;operatore AND.

1. Fate clic su **[!UICONTROL Cerca]**.

1. (Facoltativo) Fate clic su **[!UICONTROL Salva con nome]**, quindi su **[!UICONTROL Raccolta]** o **[!UICONTROL Esclusione]**.

   ![Opzioni Salva con nome](/help/c-recommendations/c-products/assets/save-as.png)

   Per ulteriori informazioni, vedi [Creare una raccolta o un&#39;esclusione basata su Ricerca](#save-as) avanzata di seguito.

## Visualizzazione dei dettagli di un elemento

Puoi visualizzare i dettagli di un singolo elemento, inclusi ID, nome, messaggio, categoria e molto altro visualizzandone i dettagli.

1. Fate clic su un elemento nei risultati della ricerca per visualizzarne i dettagli.

   ![Dettagli del prodotto](/help/c-recommendations/c-products/assets/bike-results-5.png)

## Rimozione di un elemento dal catalogo

1. Fate clic su un elemento nei risultati della ricerca per visualizzarne i dettagli.

1. Fate clic su **[!UICONTROL Rimuovi dal catalogo]**.

1. Confermate la rimozione dell&#39;elemento.

Tutte le informazioni su tale elemento vengono rimosse dall’indice del catalogo. L’elemento verrà incluso nel catalogo solo se viene aggiunto di nuovo in un feed di dati. Un elemento eliminato deve essere eliminato separatamente dai feed.

## Aggiornare il catalogo

L’indice del catalogo viene creato automaticamente quando caricate il primo feed e aggiornato in base alla pianificazione [specificata](/help/c-recommendations/c-products/feeds.md#steps).

Il catalogo viene aggiornato automaticamente quando si ricevono aggiornamenti tramite file di feed, API o aggiornamenti di mbox. In genere, gli aggiornamenti vengono completati entro un’ora. Se sono in corso degli aggiornamenti, viene visualizzata l’ora di inizio dell’aggiornamento più recente. Se non vi sono aggiornamenti in corso, viene visualizzata l’ora di inizio e di fine dell’aggiornamento più recente.

## Creare una raccolta o un’esclusione in base alla ricerca avanzata {#save-as}

Puoi creare [raccolte](/help/c-recommendations/c-products/collections.md) o [esclusioni](/help/c-recommendations/c-products/exclusions.md) utilizzando la Ricerca avanzata nella pagina Ricerca nel catalogo ([!UICONTROL Consigli] > [!UICONTROL Ricerca nel catalogo] > [!UICONTROL Ricerca avanzata]).

1. Eseguire una ricerca [](#advanced-search)avanzata.

1. Fate clic su **[!UICONTROL Salva con nome]**, quindi su **[!UICONTROL Raccolta]** o **[!UICONTROL Esclusione]**.

   ![Opzioni Salva con nome](/help/c-recommendations/c-products/assets/save-as.png)

   >[!IMPORTANT]
   >
   >The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. Questa mancata corrispondenza potrebbe creare confusione. Ensure that you consider case-sensitivity when you create collections or exclusions based on results using the [!UICONTROL Advanced Search] functionality. Ad esempio, se esegui una ricerca per “Vacanza”, i risultati della ricerca iniziale contengono “Vacanza” e “vacanza”. Se poi crei un catalogo con l’intento di restituire i prodotti contenenti “vacanza”, verranno restituiti solo i prodotti contenenti “vacanza”. ma non quelli contenenti “Vacanza”. Le esclusioni sono gestite in modo simile.

## Cambiare l&#39;ambiente

[Gli ambienti](/help/administrating-target/environments.md) consentono di organizzare i siti e gli ambienti di pre-produzione per semplificare la gestione e la generazione di rapporti separati.

1. Fate clic sul collegamento Ambiente.

   ![Collegamento ambiente](/help/c-recommendations/c-products/assets/environment.png)

1. Selezionate l’ambiente desiderato.

## Modificare la pagina di ricerca del catalogo (filtri e colonne)

Potete modificare temporaneamente i filtri e le colonne disponibili nella pagina di ricerca [!UICONTROL del] catalogo per la sessione corrente.

### Modificare i filtri

Potete aggiungere altri facet di filtro alla pagina di ricerca [!UICONTROL del] catalogo.

1. Nel pannello **[!UICONTROL Filtri]** , fare clic su **[!UICONTROL Modifica]**.

   ![Collegamento Modifica filtri](/help/c-recommendations/c-products/assets/modify-filters.png)

1. Seleziona i facet di ricerca desiderati (ID, nome, messaggio, ecc.).

   ![Aggiungere filtri](/help/c-recommendations/c-products/assets/add-filters.png)

Tenete presente che i facet aggiuntivi del filtro sono disponibili solo nella sessione corrente.

### Modificare le colonne

Potete modificare temporaneamente le colonne attive nella pagina di ricerca [!UICONTROL del] catalogo.

1. Fare clic sul collegamento **[!UICONTROL Colonne]** .

   ![Opzioni Colonne](/help/c-recommendations/c-products/assets/columns.png)

1. (Condizionale) Per riordinare l&#39;ordine delle colonne attive, trascinare le colonne nella sezione Colonne **** attive nell&#39;ordine desiderato.

1. (Condizionale) Trascinate e rilasciate gli elementi dalle colonne **** attive alle colonne **** inattive (e viceversa), come desiderato.

   È inoltre possibile fare clic sull&#39;icona di eliminazione ( x ) accanto alla colonna da spostare dalla sezione attiva a quella inattiva.

Eventuali modifiche apportate si applicano solo alla sessione corrente.

## Domande frequenti {#faq}

Consultate le seguenti domande frequenti per informazioni sulla funzione di ricerca  nel catalogo:

### Perché Catalog Search non visualizza i risultati corretti quando si esegue una ricerca su un attributo personalizzato con un valore numerico?

Quando si esegue una ricerca di catalogo su un attributo personalizzato con un valore numerico, l&#39;attributo personalizzato viene considerato come tipo String anziché come valore numerico.

Al momento, non è disponibile alcuna funzionalità che consenta ai clienti di modificare il tipo di un attributo. Per apportare una modifica, [aprire un problema](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) del cliente che fa riferimento agli attributi che richiedono la modifica del tipo da stringa a numerico.
