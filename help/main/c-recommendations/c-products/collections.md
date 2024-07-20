---
keywords: raccolta;Targeting
description: Scopri come utilizzare le raccolte di prodotti o elementi in [!DNL Target Recommendations].
title: Come si utilizzano le raccolte nelle attività di Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Recommendations
exl-id: e62f501b-3521-4456-9ea1-e4b8a2b478c6
source-git-commit: c8bd2bb45ee8ef1a849fd9091554caec77effba0
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 40%

---

# Raccolte

Una raccolta è un insieme di prodotti o elementi che sono idonei per essere proposti come consigli. Una raccolta viene definita specificando le condizioni che devono essere soddisfatte dagli elementi affinché ne facciano parte.

Solitamente, una raccolta è un insieme di elementi simili o correlati, come una raccolta di prodotti singoli. Tuttavia, puoi raggruppare qualsiasi elemento in una categoria adatta alla tua attività, ad esempio prodotti in una determinata fascia di prezzo o colore o articoli che potrebbero essere interessanti in una particolare area geografica.

Utilizza le raccolte per organizzare i prodotti in raggruppamenti logici. Ad esempio, se alcuni elementi sono disponibili in un’area ma non in un’altra, puoi creare una raccolta che escluda gli elementi non disponibili nell’area del visitatore. Puoi inoltre utilizzare le raccolte per organizzare gli elementi stagionali o qualsiasi altro parametro organizzativo applicabile al tuo business.

Anche i [consigli di backup](/help/main/c-recommendations/c-algorithms/backup-recs.md) generati per ogni criterio all’interno del consiglio utilizzano questa raccolta, in modo da includere nel consiglio di backup solo gli elementi della raccolta. Le raccolte consentono di garantire la visualizzazione dei soli prodotti che ha senso mostrare in una determinata posizione.

Le raccolte vengono ricreate o aggiornate a ogni esecuzione di ciascun criterio.

Puoi raggruppare gli elementi in cataloghi e quindi creare consigli separati per ogni raccolta.

I criteri di inclusione consentono di eseguire operazioni simili su una raccolta, ma devono essere impostati ogni volta che si crea una attività. Le raccolte consentono di creare un insieme di elementi e quindi di riutilizzarlo ogni volta che sia opportuno.

Quando si crea o si modifica un&#39;attività [!DNL Recommendations], il nome della raccolta viene visualizzato accanto all&#39;etichetta [!UICONTROL Criteria] nel diagramma attività.

>[!NOTE]
>
>Le raccolte non vengono applicate quando si utilizza la chiave di consiglio [!UICONTROL Recently Viewed Items].

## Creazione di una raccolta {#task_1256DFF6842141FCAADD9E1428EF7F08}

Crea una raccolta per organizzare i prodotti o i contenuti da mostrare nei consigli.

1. Fare clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Collections]** per visualizzare l&#39;elenco delle raccolte esistenti.

   ![Elenco Raccolte](assets/collections_list.png)

   Nella pagina [!UICONTROL Collections] viene visualizzato un elenco delle raccolte esistenti. Per creare nuove raccolte, fare clic sul pulsante [!UICONTROL Create Collection]. Puoi anche modificare, copiare ed eliminare raccolte esistenti passando il cursore sopra la raccolta desiderata e facendo clic sull’icona desiderata.

   ![Icone al passaggio del mouse: modifica, copia ed elimina](/help/main/c-recommendations/c-products/assets/hover-icons.png)

   Il &quot;Numero di elementi&quot; segnalato per ogni raccolta nella visualizzazione elenco [!UICONTROL Collections] è il numero di prodotti che corrispondono alle regole per tale raccolta all&#39;interno del gruppo predefinito di Recommendations [host](/help/main/administrating-target/hosts.md) (ambiente) configurato. Consulta [Impostazioni](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} per modificare il gruppo host predefinito.

1. Fare clic su **[!UICONTROL Create Collection]**.

1. (Facoltativo) Scegliere un ambiente dal filtro **[!UICONTROL Environment]** durante la creazione o l&#39;aggiornamento di una raccolta per visualizzare in anteprima i contenuti della raccolta in tale ambiente. Per impostazione predefinita, sono visualizzati i risultati del gruppo di host predefinito.

   ![Creare una raccolta](/help/main/c-recommendations/c-products/assets/CreateCollection.png)

1. Digitare **[!UICONTROL Name]** per la raccolta.

   È inoltre possibile immettere un valore facoltativo **[!UICONTROL Description]**.

1. Imposta le regole utilizzate per compilare la raccolta.

   Ad esempio, la raccolta potrebbe essere basata su un ID o categoria di prodotto, un margine, o qualsiasi altro parametro nell’elenco.

   È possibile aggiungere regole per utilizzare più parametri con cui definire una raccolta. Più regole sono unite con un operatore AND. Tutte le regole specificate devono essere soddisfatte perché la raccolta venga applicata.

1. Fare clic su **[!UICONTROL Save]**.

## Creare una raccolta utilizzando Ricerca avanzata

Puoi anche creare raccolte utilizzando la Ricerca avanzata nella pagina [Ricerca nel catalogo](/help/main/c-recommendations/c-products/catalog-search.md#save-as) ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

![Finestra di dialogo Salva con nome](/help/main/c-recommendations/c-products/assets/save-as.png)

Dopo aver creato una ricerca utilizzando &quot;id > contiene&quot;, ad esempio, è possibile fare clic su [!UICONTROL Save As] > [!UICONTROL Collection].

>[!IMPORTANT]
>
>La funzionalità di Ricerca avanzata non distingue tra maiuscole e minuscole, tuttavia, i prodotti restituiti al momento della consegna si basano sulla ricerca con distinzione tra maiuscole e minuscole. Questa mancata corrispondenza potrebbe creare confusione. Assicurati di considerare la distinzione tra maiuscole e minuscole quando crei raccolte in base ai risultati utilizzando la funzionalità Ricerca avanzata. Ad esempio, se esegui una ricerca per “Vacanza”, i risultati della ricerca iniziale contengono “Vacanza” e “vacanza”. Se poi crei un catalogo con l’intento di restituire i prodotti contenenti “vacanza”, verranno restituiti solo i prodotti contenenti “vacanza”. ma non quelli contenenti “Vacanza”.

## Modificare, copiare o eliminare una raccolta

Passa il cursore del mouse sulla raccolta desiderata nell’elenco, quindi fai clic sull’icona appropriata: modifica, copia o elimina.

![Icone al passaggio del mouse per una raccolta](/help/main/c-recommendations/c-products/assets/hover-collections.png)

Puoi copiare una raccolta esistente per crearne una duplicata da modificare. Questo consente di creare un’esclusione simile con meno sforzo.

Tieni presente che le raccolte sono disponibili a livello dell’intero account. Prima di eliminare una raccolta, tienilo in considerazione. Non è possibile recuperare le raccolte eliminate.

## Utilizzare una raccolta in un’attività di Recommendations

1. Crea una raccolta utilizzando uno dei metodi indicati sopra.

1. Fai clic su **[!UICONTROL Activities]** e [crea una nuova attività Recommendations](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md) o modifica un&#39;attività esistente.

1. Dopo aver selezionato un criterio e una progettazione, viene visualizzata la pagina [!UICONTROL Options] in cui si seleziona la raccolta desiderata.

   ![Scegliere l&#39;opzione di raccolta](/help/main/c-recommendations/c-products/assets/choose-collection.png)

1. (Condizionale) Per modificare un&#39;impostazione di raccolta esistente, nella pagina **[!UICONTROL Experiences]** (passaggio 2 del flusso di lavoro guidato in tre parti) fare clic in un percorso in cui sono stati inseriti i consigli, fare clic su **[!UICONTROL Change Collection]**, quindi selezionare la raccolta desiderata.

   ![Modifica opzione raccolta](/help/main/c-recommendations/c-products/assets/change-collection.png)

## Video di formazione: Creare raccolte ed esclusioni in Recommendations (7:05) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video contiene le seguenti informazioni:

* Creare una raccolta
* Creare un’esclusione

>[!VIDEO](https://video.tv.adobe.com/v/27689)
