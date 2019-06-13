---
description: Una raccolta è un insieme di prodotti o elementi che sono considerati idonei per essere proposti come consigli.
keywords: raccolta;Targeting
seo-description: Una raccolta è un insieme di prodotti o elementi che sono considerati idonei per essere proposti come consigli.
seo-title: Raccolte
solution: Target
title: Raccolte
title-outputclass: premium
topic: Premium
uuid: aa1afdcf-e51c-4e44-a229-3c21fc9d0514
badge: premium
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# ![PREMIUM](/help/assets/premium.png) Raccolte {#collections}

Una raccolta è un insieme di prodotti o elementi che sono considerati idonei per essere proposti come consigli.

## Raccolte {#concept_671BEFFB997D4F1282665BF3CAC00AC5}

Una raccolta è un insieme di prodotti o elementi che sono considerati idonei per essere proposti come consigli.

Solitamente, una raccolta è un insieme di elementi simili o correlati, come una raccolta di prodotti singoli. Tuttavia, puoi raggruppare qualsiasi elemento in una categoria adatta alla tua attività specifica, come prodotti in una determinata fascia di prezzo o colore o che possono essere di interesse in una particolare area geografica.

Utilizza le raccolte per organizzare i prodotti in raggruppamenti logici. Ad esempio, se alcuni elementi sono disponibili in un’area geografica ma non in un’altra, è possibile creare una raccolta che escluda gli elementi non disponibili nell’area del visitatore. Puoi inoltre utilizzare le raccolte per organizzare gli elementi stagionali o qualsiasi altro parametro organizzativo applicabile al tuo business.

Anche i consigli di backup generati per ogni criterio all’interno del consiglio utilizzano questa raccolta, in modo da includere nel consiglio di backup solo gli elementi della raccolta. Le raccolte consentono di garantire la visualizzazione dei soli prodotti che ha senso mostrare in una determinata posizione.

Le raccolte vengono ricreate o aggiornate a ogni esecuzione di ciascun criterio.

Puoi raggruppare gli elementi in cataloghi e quindi creare consigli separati per ogni raccolta.

I criteri di inclusione consentono di eseguire operazioni simili su una raccolta, ma devono essere impostati ogni volta che si crea una attività. Le raccolte consentono di creare un insieme di elementi e quindi di riutilizzarlo ogni volta che sia opportuno.

Quando crei o modifichi un’attività di [!DNL Recommendations], il nome della raccolta viene visualizzato accanto all’etichetta [!UICONTROL Criteri] sul diagramma dell’attività.

>[!NOTE]
>
>Le raccolte non vengono applicate quando si utilizza la chiave di consiglio [!UICONTROL Articoli visualizzati di recente].

## Creazione di una raccolta {#task_1256DFF6842141FCAADD9E1428EF7F08}

Crea una raccolta per organizzare i prodotti che desideri mostrare nei consigli.

1. Fai clic su **[!UICONTROL Consigli]** &gt; **[!UICONTROL Raccolte]** per visualizzare l’elenco delle raccolte esistenti.

   Il “Numero di elementi” segnalato per ogni raccolta nella visualizzazione elenco [!UICONTROL Raccolte] è il numero di prodotti che corrispondono alle regole per tale raccolta all’interno del [gruppo host](/help/administrating-target/hosts.md) Consigli (ambiente) predefinito configurato. Consulta [Impostazioni](../../c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84) per modificare il gruppo host predefinito.

   ![](assets/collections_list.png)

1. Fai clic su **[!UICONTROL Crea raccolta]**.

1. (Facoltativo) Scegli un ambiente dal filtro **[!UICONTROL Ambiente]** quando crei (o aggiorni) una raccolta per visualizzare in anteprima i contenuti della raccolta in tale ambiente. Per impostazione predefinita, sono visualizzati i risultati del gruppo di host predefinito.

   ![Creare una raccolta](/help/c-recommendations/c-products/assets/CreateCollection.png)

1. Digita un **[!UICONTROL Nome]** per la raccolta.

   È inoltre possibile immettere una **[!UICONTROL Descrizione facoltativa]**.

1. Imposta le regole utilizzate per compilare la raccolta.

   Ad esempio, la raccolta potrebbe essere basata su un ID o categoria di prodotto, un margine, o qualsiasi altro parametro nell’elenco.

   È possibile aggiungere regole per utilizzare più parametri con cui definire una raccolta. Le regole multiple sono collegate tra loro mediante l’operatore E. Tutte le regole specificate devono essere soddisfatte perché la raccolta venga applicata.

1. Fai clic su **[!UICONTROL Salva]**. 
Puoi anche creare raccolte utilizzando la Ricerca avanzata nella pagina Ricerca nel catalogo ([!UICONTROL Consigli] &gt; [!UICONTROL Ricerca nel catalogo] &gt; [!UICONTROL Ricerca avanzata]). Dopo aver creato una ricerca utilizzando “id &gt; contiene”, ad esempio, puoi fare clic su [!UICONTROL Salva come] &gt; [!UICONTROL Raccolta].

>[!IMPORTANT]
>
>La funzionalità di Ricerca avanzata non distingue tra maiuscole e minuscole, tuttavia, i prodotti restituiti al momento della consegna si basano sulla ricerca con distinzione tra maiuscole e minuscole. Questa mancata corrispondenza potrebbe creare confusione. Assicurati di considerare la distinzione tra maiuscole e minuscole quando crei raccolte in base ai risultati utilizzando la funzionalità Ricerca avanzata. Ad esempio, se esegui una ricerca per “Vacanza”, i risultati della ricerca iniziale contengono “Vacanza” e “vacanza”. Se poi crei un catalogo con l’intento di restituire i prodotti contenenti “vacanza”, verranno restituiti solo i prodotti contenenti “vacanza”. ma non quelli contenenti “Vacanza”.