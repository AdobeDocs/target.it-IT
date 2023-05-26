---
keywords: catalogo ricerca;catalogo;ricerca;esclusione;raccolta;filtro
description: Scopri come utilizzare Recommendations Catalog Search per individuare prodotti o contenuti, creare raccolte o esclusioni, rimuovere elementi dal catalogo e altro ancora.
title: Come si utilizza la ricerca nel catalogo di Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 925fea97-e2c5-4883-84e3-fd357a8ee8d9
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '1040'
ht-degree: 22%

---

# Ricerca nel catalogo

Il [!UICONTROL Ricerca nel catalogo] pagina in [!DNL Adobe Recommendations] consente di individuare i prodotti o i contenuti nel catalogo. L&#39;operazione di base che è possibile eseguire in questa pagina è la ricerca di un elemento. Inoltre, puoi modificare l’ambiente, salvare i risultati della ricerca in raccolte o esclusioni, aggiungere facet di filtro e modificare le colonne della tabella, aggiungere nuovi facet di ricerca e altro ancora.

I cataloghi si riferiscono all’intero set di prodotti (entità). Il catalogo può contenere molte raccolte, un modo per organizzare i prodotti in contenitori logici.

## Accedi alla ricerca nel catalogo

Per accedere al [!UICONTROL Ricerca nel catalogo] pagina, fai clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Ricerca nel catalogo]**.

![Pagina Ricerca nel catalogo](/help/main/c-recommendations/c-products/assets/catalog-search.png)

## Cerca un elemento

Puoi utilizzare una ricerca semplice o una ricerca avanzata per individuare gli elementi nel catalogo.

### Eseguire una ricerca semplice

1. Digita un termine di ricerca nel **[!UICONTROL Cerca prodotti]** campo.

1. (Facoltativo) Puoi perfezionare la ricerca selezionando un’opzione di ricerca dal menu delle opzioni che viene visualizzato quando fai clic sulla freccia rivolta verso il basso nel campo di ricerca.

   ![ricercatiprodottiimmagine del menu](assets/searchproductsmenu.png)

   Le opzioni di ricerca includono:

   * TUTTO : esegue la ricerca in tutti gli altri criteri di ricerca, utilizzando l’operatore logico OR.
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

   ![Ricerca completamento automatico](/help/main/c-recommendations/c-products/assets/bike-results-2.png)

   >[!NOTE]
   >
   >Quando esegui sul catalogo la ricerca di un attributo personalizzato con un valore numerico, l’attributo personalizzato viene considerato come di tipo stringa anziché come valore numerico.
   >
   >Attualmente, non è disponibile alcuna funzionalità che consenta di modificare il tipo di un attributo. Per apportare una modifica, [apri un problema cliente](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) facendo riferimento agli attributi che richiedono la modifica del tipo da stringa a numerico.

1. Puoi anche utilizzare i filtri per trovare il prodotto desiderato. Nell&#39;esempio seguente, espandendo [!UICONTROL Raccolte] facet e selezionando &quot;Bike Tools&quot;, tutti gli strumenti per bici nel tuo catalogo.

   ![Utensili per bici](/help/main/c-recommendations/c-products/assets/bike-results-3.png)

1. È possibile eseguire ulteriori ricerche nell&#39;elenco dei risultati immettendo un termine di ricerca, ad esempio &quot;catena&quot;.

   ![Cerca catena](/help/main/c-recommendations/c-products/assets/bike-results-4.png)

### Eseguire una ricerca avanzata {#advanced-search}

È possibile utilizzare [!UICONTROL Ricerca avanzata] per perfezionare ulteriormente i risultati della ricerca o per salvarli come [raccolta](/help/main/c-recommendations/c-products/collections.md) o [esclusione](/help/main/c-recommendations/c-products/exclusions.md).

1. Fai clic su **[!UICONTROL Ricerca avanzata]** collegamento.

   ![Pagina Ricerca avanzata](/help/main/c-recommendations/c-products/assets/advances-search.png)

1. Utilizza gli elenchi a discesa per specificare il parametro, l’operatore e i valori per la ricerca.

1. (Facoltativo) Fai clic su **[!UICONTROL Aggiungi regola]** per aggiungere una regola di ricerca aggiuntiva.

   Ogni regola di ricerca aggiuntiva viene unita all’operatore AND.

1. Clic **[!UICONTROL Ricerca]**.

1. (Facoltativo) Fai clic su **[!UICONTROL Salva con nome]**, quindi fai clic su **[!UICONTROL Raccolta]** o **[!UICONTROL Esclusione]**.

   ![Opzioni Salva con nome](/help/main/c-recommendations/c-products/assets/save-as.png)

   Per ulteriori informazioni, consulta [Creare una raccolta o un’esclusione in base alla ricerca avanzata](#save-as) di seguito.

## Visualizzare i dettagli di un elemento

Puoi visualizzare i dettagli di un singolo elemento, tra cui ID, nome, messaggio, categoria e altro ancora, visualizzandone i dettagli.

1. Fare clic su un elemento nei risultati della ricerca per visualizzarne i dettagli.

   ![Dettagli prodotto](/help/main/c-recommendations/c-products/assets/bike-results-5.png)

## Rimuovere un elemento dal catalogo

1. Fare clic su un elemento nei risultati della ricerca per visualizzarne i dettagli.

1. Clic **[!UICONTROL Rimuovi dal catalogo]**.

1. Confermare la rimozione dell&#39;elemento.

Tutte le informazioni sull&#39;elemento vengono rimosse dall&#39;indice del catalogo. L’elemento verrà incluso nel catalogo solo se viene aggiunto nuovamente in un feed di dati. Un elemento eliminato deve essere eliminato separatamente dai feed.

## Aggiorna il catalogo

L’indice del catalogo viene creato automaticamente al caricamento del primo feed e aggiornato in base al [pianificazione specificata](/help/main/c-recommendations/c-products/feeds.md#steps).

Il catalogo viene aggiornato automaticamente quando si ricevono aggiornamenti tramite file di feed, API o aggiornamenti di mbox. In genere, gli aggiornamenti vengono completati entro un’ora. Se sono in corso degli aggiornamenti, viene visualizzata l’ora di inizio dell’aggiornamento più recente. Se non vi sono aggiornamenti in corso, viene visualizzata l’ora di inizio e di fine dell’aggiornamento più recente.

## Creare una raccolta o un’esclusione in base alla ricerca avanzata {#save-as}

Puoi creare [raccolte](/help/main/c-recommendations/c-products/collections.md) o [esclusioni](/help/main/c-recommendations/c-products/exclusions.md) utilizzando la Ricerca avanzata nella pagina Ricerca nel catalogo ([!UICONTROL Consigli] > [!UICONTROL Ricerca nel catalogo] > [!UICONTROL Ricerca avanzata]).

1. Esegui una [ricerca avanzata](#advanced-search).

1. Clic **[!UICONTROL Salva con nome]**, quindi fai clic su **[!UICONTROL Raccolta]** o **[!UICONTROL Esclusione]**.

   ![Opzioni Salva con nome](/help/main/c-recommendations/c-products/assets/save-as.png)

   >[!IMPORTANT]
   >
   >Il [!UICONTROL Ricerca avanzata] La funzionalità non distingue tra maiuscole e minuscole, tuttavia, i prodotti restituiti al momento della consegna si basano sulla ricerca con distinzione tra maiuscole e minuscole. Questa mancata corrispondenza potrebbe creare confusione. Assicurati di considerare la distinzione tra maiuscole e minuscole quando crei raccolte o esclusioni in base ai risultati utilizzando [!UICONTROL Ricerca avanzata] funzionalità. Ad esempio, se esegui una ricerca per “Vacanza”, i risultati della ricerca iniziale contengono “Vacanza” e “vacanza”. Se poi crei un catalogo con l’intento di restituire i prodotti contenenti “vacanza”, verranno restituiti solo i prodotti contenenti “vacanza”. ma non quelli contenenti “Vacanza”. Le esclusioni sono gestite in modo simile.

## Modificare l’ambiente

[Ambienti](/help/main/administrating-target/environments.md) consente di organizzare i siti e gli ambienti di preproduzione per gestirli facilmente e generare rapporti separati.

1. Fai clic sul collegamento Ambiente.

   ![Collegamento all’ambiente](/help/main/c-recommendations/c-products/assets/environment.png)

1. Seleziona l’ambiente desiderato.

## Modificare la pagina Ricerca nel catalogo (filtri e colonne)

Puoi modificare temporaneamente i filtri e le colonne disponibili nella sezione [!UICONTROL Ricerca nel catalogo] per la sessione corrente.

### Modificare i filtri

Puoi aggiungere altri facet di filtro al [!UICONTROL Ricerca nel catalogo] pagina.

1. In **[!UICONTROL Filtri]** , fare clic su **[!UICONTROL Modifica]**.

   ![Collegamento Modifica filtri](/help/main/c-recommendations/c-products/assets/modify-filters.png)

1. Seleziona i facet di ricerca (ID, nome, messaggio, ecc.), quindi fai clic su **[!UICONTROL Salva]**.

   ![Aggiungere filtri](/help/main/c-recommendations/c-products/assets/add-filters.png)

Tieni presente che i facet di filtro aggiuntivi sono disponibili solo nella sessione corrente.

### Modifica colonne

È possibile modificare temporaneamente le colonne attive nel [!UICONTROL Ricerca nel catalogo] pagina.

1. Fai clic su **[!UICONTROL Colonne]** collegamento.

   ![Opzioni colonne](/help/main/c-recommendations/c-products/assets/columns.png)

1. (Condizionale) Per riordinare l’ordine delle colonne attive, trascina e rilascia le colonne nella **[!UICONTROL Colonne attive]** nell&#39;ordine desiderato.

1. (Condizionale) Trascina gli elementi dalla sezione **[!UICONTROL Colonne attive]** al **[!UICONTROL Colonne inattive]** (e viceversa), come desiderato.

   Puoi anche fare clic sull’icona Elimina ( x ) accanto alla colonna da attiva a inattiva.

Eventuali modifiche apportate vengono applicate solo alla sessione corrente.
