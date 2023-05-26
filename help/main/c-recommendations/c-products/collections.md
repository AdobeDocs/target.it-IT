---
keywords: raccolta;Targeting
description: Scopri come utilizzare le raccolte in Adobe [!DNL Target] Recommendations. Una raccolta è un insieme di prodotti o elementi che sono considerati idonei per essere proposti come consigli.
title: Come si utilizzano le raccolte nelle attività di Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: e62f501b-3521-4456-9ea1-e4b8a2b478c6
source-git-commit: 2a25fdb42ce4470f9126b7e0e7f6fd9e60c350e5
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 60%

---

# Raccolte

Una raccolta è un insieme di prodotti o elementi che sono considerati idonei per essere proposti come consigli. Una raccolta viene definita specificando le condizioni che devono essere soddisfatte dagli elementi affinché ne facciano parte.

Solitamente, una raccolta è un insieme di elementi simili o correlati, come una raccolta di prodotti singoli. Tuttavia, puoi raggruppare qualsiasi elemento in una categoria adatta alla tua attività, ad esempio prodotti in una determinata fascia di prezzo o colore o articoli che potrebbero essere interessanti in una particolare area geografica.

Utilizza le raccolte per organizzare i prodotti in raggruppamenti logici. Ad esempio, se alcuni elementi sono disponibili in un’area ma non in un’altra, puoi creare una raccolta che escluda gli elementi non disponibili nell’area del visitatore. Puoi inoltre utilizzare le raccolte per organizzare gli elementi stagionali o qualsiasi altro parametro organizzativo applicabile al tuo business.

Anche i [consigli di backup](/help/main/c-recommendations/c-algorithms/backup-recs.md) generati per ogni criterio all’interno del consiglio utilizzano questa raccolta, in modo da includere nel consiglio di backup solo gli elementi della raccolta. Le raccolte consentono di garantire la visualizzazione dei soli prodotti che ha senso mostrare in una determinata posizione.

Le raccolte vengono ricreate o aggiornate a ogni esecuzione di ciascun criterio.

Puoi raggruppare gli elementi in cataloghi e quindi creare consigli separati per ogni raccolta.

I criteri di inclusione consentono di eseguire operazioni simili su una raccolta, ma devono essere impostati ogni volta che si crea una attività. Le raccolte consentono di creare un insieme di elementi e quindi di riutilizzarlo ogni volta che sia opportuno.

Quando crei o modifichi un’attività di [!DNL Recommendations], il nome della raccolta viene visualizzato accanto all’etichetta [!UICONTROL Criteri] sul diagramma dell’attività.

>[!NOTE]
>
>Le raccolte non vengono applicate quando si utilizza la chiave di consiglio [!UICONTROL Articoli visualizzati di recente].

## Creazione di una raccolta {#task_1256DFF6842141FCAADD9E1428EF7F08}

Crea una raccolta per organizzare i prodotti o i contenuti da mostrare nei consigli.

1. Fai clic su **[!UICONTROL Consigli]** > **[!UICONTROL Raccolte]** per visualizzare l&#39;elenco delle raccolte esistenti.

   ![Elenco Raccolte](assets/collections_list.png)

   Il [!UICONTROL Raccolte] In questa pagina viene visualizzato un elenco delle raccolte esistenti. Per creare nuove raccolte, fai clic su [!UICONTROL Crea raccolta] pulsante. Puoi anche modificare, copiare ed eliminare raccolte esistenti passando il cursore sopra la raccolta desiderata e facendo clic sull’icona desiderata.

   ![Icone al passaggio del mouse: modifica, copia ed elimina](/help/main/c-recommendations/c-products/assets/hover-icons.png)

   Il “Numero di elementi” segnalato per ogni raccolta nella visualizzazione elenco [!UICONTROL Raccolte] è il numero di prodotti che corrispondono alle regole per tale raccolta all’interno del [gruppo host](/help/main/administrating-target/hosts.md) Consigli (ambiente) predefinito configurato. Consulta [Impostazioni](https://experienceleague.corp.adobe.com/docs/target-dev/developer/recommendations.html?lang=it) per modificare il gruppo host predefinito.{target=_blank}

1. Fai clic su **[!UICONTROL Crea raccolta]**.

1. (Facoltativo) Scegli un ambiente dal filtro **[!UICONTROL Ambiente]** quando crei (o aggiorni) una raccolta per visualizzare in anteprima i contenuti della raccolta in tale ambiente. Per impostazione predefinita, sono visualizzati i risultati del gruppo di host predefinito.

   ![Creare una raccolta](/help/main/c-recommendations/c-products/assets/CreateCollection.png)

1. Digita un **[!UICONTROL Nome]** per la raccolta.

   È inoltre possibile immettere una **[!UICONTROL Descrizione facoltativa]**.

1. Imposta le regole utilizzate per compilare la raccolta.

   Ad esempio, la raccolta potrebbe essere basata su un ID o categoria di prodotto, un margine, o qualsiasi altro parametro nell’elenco.

   È possibile aggiungere regole per utilizzare più parametri con cui definire una raccolta. Più regole sono unite con un operatore AND. Tutte le regole specificate devono essere soddisfatte perché la raccolta venga applicata.

1. Fai clic su **[!UICONTROL Salva]**.

## Creare una raccolta utilizzando Ricerca avanzata

Puoi anche creare le raccolte mediante la funzione Ricerca avanzata nella pagina [Ricerca nel catalogo](/help/main/c-recommendations/c-products/catalog-search.md#save-as) ([!UICONTROL Consigli] > [!UICONTROL Ricerca nel catalogo] > [!UICONTROL Ricerca avanzata]).

![Finestra di dialogo Salva con nome](/help/main/c-recommendations/c-products/assets/save-as.png)

Dopo aver creato una ricerca utilizzando “id > contiene”, ad esempio, puoi fare clic su [!UICONTROL Salva come] > [!UICONTROL Raccolta].

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

1. Clic **[!UICONTROL Attività]** e [crea un nuovo Recommendations](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md) o modificare un&#39;attività esistente.

1. Dopo aver selezionato un criterio e una progettazione, [!UICONTROL Opzioni] quando selezioni la raccolta desiderata, viene visualizzata una pagina.

   ![Scegli l&#39;opzione di raccolta](/help/main/c-recommendations/c-products/assets/choose-collection.png)

1. (Condizionale) Per modificare un’impostazione di raccolta esistente, nella **[!UICONTROL Esperienze]** pagina (passaggio 2 del flusso di lavoro guidato in tre parti), fai clic sul percorso in cui hai inserito i consigli, quindi fai clic su **[!UICONTROL Cambia raccolta]**, quindi seleziona la raccolta desiderata.

   ![Opzione Cambia raccolta](/help/main/c-recommendations/c-products/assets/change-collection.png)

## Video di formazione: Creare raccolte ed esclusioni in Recommendations (7:05) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video contiene le seguenti informazioni:

* Creare una raccolta
* Creare un’esclusione

>[!VIDEO](https://video.tv.adobe.com/v/27689)
