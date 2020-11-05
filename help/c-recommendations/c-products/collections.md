---
keywords: collection;Targeting
description: Una raccolta è un insieme di prodotti o elementi in Adobe Target che sono considerati idonei per essere proposti come consigli.
title: Raccolte in Adobe Target
feature: entities
uuid: aa1afdcf-e51c-4e44-a229-3c21fc9d0514
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '868'
ht-degree: 61%

---


# ![PREMIUM](/help/assets/premium.png) Raccolte {#collections}

Una raccolta è un insieme di prodotti o elementi che sono considerati idonei per essere proposti come consigli. Una raccolta è definita specificando le condizioni che devono essere soddisfatte dagli elementi per farne parte.

Solitamente, una raccolta è un insieme di elementi simili o correlati, come una raccolta di prodotti singoli. Tuttavia, potete raggruppare qualsiasi elemento in una categoria che abbia senso per la vostra attività, ad esempio prodotti in una determinata fascia di prezzo o in un determinato colore o elementi che potrebbero essere interessanti in una particolare area geografica.

Utilizza le raccolte per organizzare i prodotti in raggruppamenti logici. Ad esempio, se alcuni elementi sono disponibili in un&#39;area, ma non in un&#39;altra, potete creare una raccolta che escluda gli elementi non disponibili nell&#39;area del visitatore. Puoi inoltre utilizzare le raccolte per organizzare gli elementi stagionali o qualsiasi altro parametro organizzativo applicabile al tuo business.

Anche i [consigli di backup](/help/c-recommendations/c-algorithms/backup-recs.md) generati per ogni criterio all’interno del consiglio utilizzano questa raccolta, in modo da includere nel consiglio di backup solo gli elementi della raccolta. Le raccolte consentono di garantire la visualizzazione dei soli prodotti che ha senso mostrare in una determinata posizione.

Le raccolte vengono ricreate o aggiornate a ogni esecuzione di ciascun criterio.

Puoi raggruppare gli elementi in cataloghi e quindi creare consigli separati per ogni raccolta.

I criteri di inclusione consentono di eseguire operazioni simili su una raccolta, ma devono essere impostati ogni volta che si crea una attività. Le raccolte consentono di creare un insieme di elementi e quindi di riutilizzarlo ogni volta che sia opportuno.

Quando crei o modifichi un’attività di [!DNL Recommendations], il nome della raccolta viene visualizzato accanto all’etichetta [!UICONTROL Criteri] sul diagramma dell’attività.

>[!NOTE]
>
>Le raccolte non vengono applicate quando si utilizza la chiave di consiglio [!UICONTROL Articoli visualizzati di recente].

## Creazione di una raccolta {#task_1256DFF6842141FCAADD9E1428EF7F08}

Create una raccolta per organizzare i prodotti o il contenuto da mostrare nelle raccomandazioni.

1. Fai clic su **[!UICONTROL Consigli]** > **[!UICONTROL Raccolte]** per visualizzare l&#39;elenco delle raccolte esistenti.

   ![Elenco Raccolte](assets/collections_list.png)

   Nella pagina [!UICONTROL Raccolte] viene visualizzato un elenco delle raccolte esistenti. Per creare nuove raccolte, fate clic sul pulsante [!UICONTROL Crea raccolta] . Potete inoltre modificare, copiare ed eliminare le raccolte esistenti posizionando il puntatore del mouse sulla raccolta desiderata e facendo clic sull&#39;icona desiderata.

   ![Icone al passaggio del mouse: modificare, copiare ed eliminare](/help/c-recommendations/c-products/assets/hover-icons.png)

   Il “Numero di elementi” segnalato per ogni raccolta nella visualizzazione elenco [!UICONTROL Raccolte] è il numero di prodotti che corrispondono alle regole per tale raccolta all’interno del [gruppo host](/help/administrating-target/hosts.md) Consigli (ambiente) predefinito configurato. Consulta [Impostazioni](/help/c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84) per modificare il gruppo host predefinito.

1. Fai clic su **[!UICONTROL Crea raccolta]**.

1. (Facoltativo) Scegli un ambiente dal filtro **[!UICONTROL Ambiente]** quando crei (o aggiorni) una raccolta per visualizzare in anteprima i contenuti della raccolta in tale ambiente. Per impostazione predefinita, sono visualizzati i risultati del gruppo di host predefinito.

   ![Creare una raccolta](/help/c-recommendations/c-products/assets/CreateCollection.png)

1. Digita un **[!UICONTROL Nome]** per la raccolta.

   È inoltre possibile immettere una **[!UICONTROL Descrizione facoltativa]**.

1. Imposta le regole utilizzate per compilare la raccolta.

   Ad esempio, la raccolta potrebbe essere basata su un ID o categoria di prodotto, un margine, o qualsiasi altro parametro nell’elenco.

   È possibile aggiungere regole per utilizzare più parametri con cui definire una raccolta. Regole multiple sono collegate con un operatore AND. Tutte le regole specificate devono essere soddisfatte perché la raccolta venga applicata.

1. Fai clic su **[!UICONTROL Salva]**.

## Creare una raccolta utilizzando Ricerca avanzata

Puoi anche creare le raccolte mediante la funzione Ricerca avanzata nella pagina [Ricerca nel catalogo](/help/c-recommendations/c-products/catalog-search.md#save-as) ([!UICONTROL Consigli] > [!UICONTROL Ricerca nel catalogo] > [!UICONTROL Ricerca avanzata]).

![Salva con nome, finestra di dialogo](/help/c-recommendations/c-products/assets/save-as.png)

Dopo aver creato una ricerca utilizzando “id > contiene”, ad esempio, puoi fare clic su [!UICONTROL Salva come] > [!UICONTROL Raccolta].

>[!IMPORTANT]
>
>La funzionalità di Ricerca avanzata non distingue tra maiuscole e minuscole, tuttavia, i prodotti restituiti al momento della consegna si basano sulla ricerca con distinzione tra maiuscole e minuscole. Questa mancata corrispondenza potrebbe creare confusione. Assicurati di considerare la distinzione tra maiuscole e minuscole quando crei raccolte in base ai risultati utilizzando la funzionalità Ricerca avanzata. Ad esempio, se esegui una ricerca per “Vacanza”, i risultati della ricerca iniziale contengono “Vacanza” e “vacanza”. Se poi crei un catalogo con l’intento di restituire i prodotti contenenti “vacanza”, verranno restituiti solo i prodotti contenenti “vacanza”. ma non quelli contenenti “Vacanza”.

## Modificare, copiare o eliminare una raccolta

Passate il puntatore del mouse sulla raccolta desiderata nell&#39;elenco, quindi fate clic sull&#39;icona appropriata: modificare, copiare o eliminare.

![Icone al passaggio del mouse per una raccolta](/help/c-recommendations/c-products/assets/hover-collections.png)

Potete copiare una raccolta esistente per creare una raccolta duplicata da modificare. Questo consente di creare un&#39;esclusione simile con meno sforzi.

Tenete presente che le raccolte sono disponibili nell&#39;intero account. Considerate questo aspetto prima di eliminare una raccolta. Le raccolte eliminate non possono essere recuperate.

## Utilizzo di una raccolta in un&#39;attività Recommendations

1. Create una raccolta utilizzando uno dei metodi indicati in precedenza.

1. Fate clic su **[!UICONTROL Attività]** e [create una nuova attività Recommendations](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md) o modificate un&#39;attività esistente.

1. Dopo aver selezionato un criterio e una progettazione, la pagina [!UICONTROL Opzioni] viene visualizzata quando selezionate la raccolta desiderata.

   ![Scegli opzione raccolta](/help/c-recommendations/c-products/assets/choose-collection.png)

1. (Condizionale) Per modificare un&#39;impostazione di raccolta esistente, nella pagina **[!UICONTROL Esperienze]** (passaggio 2 del flusso di lavoro guidato in tre parti), fate clic su un percorso in cui avete inserito le raccomandazioni, fate clic su **[!UICONTROL Modifica raccolta]**, quindi selezionate la raccolta desiderata.

   ![Cambia raccolta, opzione](/help/c-recommendations/c-products/assets/change-collection.png)

## Training video: Create collections and exclusions in Recommendations (7:05) ![Tutorial badge](/help/assets/tutorial.png)

Questo video contiene le seguenti informazioni:

* Creare una raccolta
* Creare un’esclusione

>[!VIDEO](https://video.tv.adobe.com/v/27689)