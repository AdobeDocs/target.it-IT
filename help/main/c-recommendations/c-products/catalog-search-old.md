---
keywords: catalogo ricerca;catalogo;ricerca;esclusione;raccolta;filtro
description: Scopri come utilizzare la funzione Ricerca nel catalogo di Recommendations per individuare prodotti o contenuti, creare raccolte o esclusioni, rimuovere elementi dal catalogo e altro ancora.
title: Come si utilizza la ricerca nel catalogo di Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 925fea97-e2c5-4883-84e3-fd357a8ee8d9
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '993'
ht-degree: 21%

---

# Ricerca nel catalogo

La pagina [!UICONTROL Catalog Search] in [!DNL Adobe Recommendations] consente di individuare prodotti o contenuti nel catalogo. L&#39;operazione di base che è possibile eseguire in questa pagina è la ricerca di un elemento. Inoltre, puoi modificare l’ambiente, salvare i risultati della ricerca in raccolte o esclusioni, aggiungere facet di filtro e modificare le colonne della tabella, aggiungere nuovi facet di ricerca e altro ancora.

I cataloghi si riferiscono all’intero set di prodotti (entità). Il catalogo può contenere molte raccolte, un modo per organizzare i prodotti in contenitori logici.

## Accedi alla ricerca nel catalogo

Per accedere alla pagina [!UICONTROL Catalog Search], fare clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Catalog Search]**.

![Pagina di ricerca catalogo](/help/main/c-recommendations/c-products/assets/catalog-search.png)

## Cerca un elemento

Puoi utilizzare una ricerca semplice o una ricerca avanzata per individuare gli elementi nel catalogo.

### Eseguire una ricerca semplice

1. Digitare un termine nel campo **[!UICONTROL Search Products]**.

1. (Facoltativo) Puoi perfezionare la ricerca selezionando un’opzione di ricerca dal menu delle opzioni che viene visualizzato quando fai clic sulla freccia rivolta verso il basso nel campo di ricerca.

   ![ricercatiprosuumenu immagine](assets/searchproductsmenu.png)

   Le opzioni di ricerca includono:

   * ALL: esegue la ricerca in tutti gli altri criteri di ricerca, utilizzando l’operatore logico OR.
   * Nome
   * Marchio
   * Categoria
   * ID
   * Messaggio

1. È ora possibile scorrere gli elementi nei risultati della ricerca per visualizzare le miniature e altre informazioni sul prodotto.

   Nell&#39;illustrazione seguente vengono illustrati i risultati per &quot;bike&quot; utilizzando l&#39;opzione All.

   ![Ricerca catalogo per bici](/help/main/c-recommendations/c-products/assets/bike-results.png)

   Il numero visualizzato accanto a &quot;Prodotti&quot; è il numero di prodotti corrispondenti al termine di ricerca, sul totale disponibile nell’ambiente specificato.

   È possibile utilizzare la funzionalità di completamento automatico della ricerca. Nell&#39;illustrazione seguente, digitando &quot;bik&quot; vengono restituiti tutti i prodotti che contengono la parola &quot;bike&quot;.

   ![Ricerca automatica](/help/main/c-recommendations/c-products/assets/bike-results-2.png)

   >[!NOTE]
   >
   >Quando esegui sul catalogo la ricerca di un attributo personalizzato con un valore numerico, l’attributo personalizzato viene considerato come di tipo stringa anziché come valore numerico.
   >
   >Attualmente, non è disponibile alcuna funzionalità che consenta di modificare il tipo di un attributo. Per apportare una modifica, [apri un problema cliente](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) facendo riferimento agli attributi che richiedono la modifica del tipo da stringa a numerico.

1. Puoi anche utilizzare i filtri per trovare il prodotto desiderato. Nell&#39;esempio seguente, espandendo il facet [!UICONTROL Collections] e selezionando &quot;Bike Tools&quot;, vengono visualizzati tutti gli strumenti per bici presenti nel catalogo.

   ![Utensili per bici](/help/main/c-recommendations/c-products/assets/bike-results-3.png)

1. È possibile eseguire ulteriori ricerche nell&#39;elenco dei risultati immettendo un termine di ricerca, ad esempio &quot;catena&quot;.

   ![Cerca catena](/help/main/c-recommendations/c-products/assets/bike-results-4.png)

### Eseguire una ricerca avanzata {#advanced-search}

Puoi utilizzare [!UICONTROL Advanced Search] per perfezionare ulteriormente i risultati della ricerca o per salvarli come [raccolta](/help/main/c-recommendations/c-products/collections.md) o [esclusione](/help/main/c-recommendations/c-products/exclusions.md).

1. Fare clic sul collegamento **[!UICONTROL Advanced Search]**.

   ![Pagina Ricerca avanzata](/help/main/c-recommendations/c-products/assets/advances-search.png)

1. Utilizza gli elenchi a discesa per specificare il parametro, l’operatore e i valori per la ricerca.

1. (Facoltativo) Fare clic su **[!UICONTROL Add Rule]** per aggiungere una regola di ricerca aggiuntiva.

   Ogni regola di ricerca aggiuntiva viene unita all’operatore AND.

1. Fare clic su **[!UICONTROL Search]**.

1. (Facoltativo) Fare clic su **[!UICONTROL Save As]**, quindi su **[!UICONTROL Collection]** o **[!UICONTROL Exclusion]**.

   ![Opzioni Salva con nome](/help/main/c-recommendations/c-products/assets/save-as.png)

   Per ulteriori informazioni, vedere [Creare una raccolta o un&#39;esclusione in base alla ricerca avanzata](#save-as) di seguito.

## Visualizzare i dettagli di un elemento

Puoi visualizzare i dettagli di un singolo elemento, tra cui ID, nome, messaggio, categoria e altro ancora, visualizzandone i dettagli.

1. Fare clic su un elemento nei risultati della ricerca per visualizzarne i dettagli.

   ![Dettagli prodotto](/help/main/c-recommendations/c-products/assets/bike-results-5.png)

## Rimuovere un elemento dal catalogo

1. Fare clic su un elemento nei risultati della ricerca per visualizzarne i dettagli.

1. Fare clic su **[!UICONTROL Remove from Catalog]**.

1. Confermare la rimozione dell&#39;elemento.

Tutte le informazioni sull&#39;elemento vengono rimosse dall&#39;indice del catalogo. L’elemento verrà incluso nel catalogo solo se viene aggiunto nuovamente in un feed di dati. Un elemento eliminato deve essere eliminato separatamente dai feed.

## Aggiorna il catalogo

L&#39;indice del catalogo viene creato automaticamente al caricamento del primo feed e aggiornato in base alla [pianificazione specificata](/help/main/c-recommendations/c-products/feeds.md#steps).

Il catalogo viene aggiornato automaticamente quando si ricevono aggiornamenti tramite file di feed, API o aggiornamenti di mbox. In genere, gli aggiornamenti vengono completati entro un’ora. Se sono in corso degli aggiornamenti, viene visualizzata l’ora di inizio dell’aggiornamento più recente. Se non vi sono aggiornamenti in corso, viene visualizzata l’ora di inizio e di fine dell’aggiornamento più recente.

## Creare una raccolta o un’esclusione in base alla ricerca avanzata {#save-as}

È possibile creare [raccolte](/help/main/c-recommendations/c-products/collections.md) o [esclusioni](/help/main/c-recommendations/c-products/exclusions.md) utilizzando [!UICONTROL Advanced Search] nella pagina [!UICONTROL Catalog Search] ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

1. Esegui una [ricerca avanzata](#advanced-search).

1. Fare clic su **[!UICONTROL Save As]**, quindi su **[!UICONTROL Collection]** o **[!UICONTROL Exclusion]**.

   ![Opzioni Salva con nome](/help/main/c-recommendations/c-products/assets/save-as.png)

   >[!IMPORTANT]
   >
   >La funzionalità [!UICONTROL Advanced Search] non distingue tra maiuscole e minuscole. Tuttavia, i prodotti restituiti al momento della consegna si basano sulla ricerca con distinzione tra maiuscole e minuscole. Questa mancata corrispondenza potrebbe creare confusione. Assicurarsi di considerare la distinzione tra maiuscole e minuscole quando si creano raccolte o esclusioni in base ai risultati utilizzando la funzionalità [!UICONTROL Advanced Search]. Ad esempio, se esegui una ricerca per “Vacanza”, i risultati della ricerca iniziale contengono “Vacanza” e “vacanza”. Se poi crei un catalogo con l’intento di restituire i prodotti contenenti “vacanza”, verranno restituiti solo i prodotti contenenti “vacanza”. ma non quelli contenenti “Vacanza”. Le esclusioni sono gestite in modo simile.

## Modificare l’ambiente

[Ambienti](/help/main/administrating-target/environments.md) consente di organizzare i siti e gli ambienti di pre-produzione per semplificare la gestione e la creazione di rapporti separati.

1. Fai clic sul collegamento Ambiente.

   ![Collegamento ambiente](/help/main/c-recommendations/c-products/assets/environment.png)

1. Seleziona l’ambiente desiderato.

## Modificare la pagina Ricerca nel catalogo (filtri e colonne)

È possibile modificare temporaneamente i filtri e le colonne disponibili nella pagina [!UICONTROL Catalog Search] per la sessione corrente.

### Modificare i filtri

È possibile aggiungere altri facet di filtro alla pagina [!UICONTROL Catalog Search].

1. Nel pannello **[!UICONTROL Filters]**, fai clic su **[!UICONTROL Modify]**.

   ![Modifica collegamento filtri](/help/main/c-recommendations/c-products/assets/modify-filters.png)

1. Selezionare i facet di ricerca desiderati (ID, nome, messaggio, ecc.), quindi fare clic su **[!UICONTROL Save]**.

   ![Aggiungi filtri](/help/main/c-recommendations/c-products/assets/add-filters.png)

Tieni presente che i facet di filtro aggiuntivi sono disponibili solo nella sessione corrente.

### Modifica colonne

È possibile modificare temporaneamente le colonne attive nella pagina [!UICONTROL Catalog Search].

1. Fare clic sul collegamento **[!UICONTROL Columns]**.

   ![Opzioni colonne](/help/main/c-recommendations/c-products/assets/columns.png)

1. (Condizionale) Per riordinare l&#39;ordine delle colonne attive, trascinare e rilasciare le colonne nella sezione **[!UICONTROL Active Columns]** nell&#39;ordine desiderato.

1. (Condizionale) Trascinare gli elementi da **[!UICONTROL Active Columns]** a **[!UICONTROL Inactive Columns]** (e viceversa), come desiderato.

   Puoi anche fare clic sull’icona Elimina ( x ) accanto alla colonna da attiva a inattiva.

Eventuali modifiche apportate vengono applicate solo alla sessione corrente.
