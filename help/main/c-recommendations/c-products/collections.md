---
keywords: raccolta;Targeting
description: Scopri come utilizzare le raccolte di prodotti o elementi in [!DNL Target Recommendations].
title: Come si utilizzano le raccolte nelle attività Consigli?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: e62f501b-3521-4456-9ea1-e4b8a2b478c6
TQID: 'https://experienceleague.adobe.com/kdjl2cpjaRWYZRqHFqARHvbTaTuu0iAH7ZWbD2Lrs7o'
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
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 8%
---
# Raccolte {#collections}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come creare, gestire e utilizzare raccolte di elementi in [!DNL Adobe Target Recommendations].

>[!ENDSHADEBOX]

Una raccolta è un insieme di prodotti o elementi che sono considerati idonei per essere proposti come consigli. Una raccolta è definita dalle condizioni che gli elementi devono soddisfare per farne parte. Gli articoli possono essere raggruppati in qualsiasi modo utile per l&#39;azienda, come articoli simili o correlati, prodotti in una determinata fascia di prezzo o colore o articoli che possono essere interessanti in una particolare area geografica.

Le raccolte organizzano i prodotti in contenitori logici. Ad esempio, se alcuni elementi sono disponibili in un’area ma non in un’altra, una raccolta può escludere gli elementi non disponibili nell’area del visitatore. Le raccolte possono anche organizzare elementi stagionali o altri parametri organizzativi applicabili all’azienda. Gli elementi possono essere raggruppati in cataloghi ed è possibile creare consigli separati per ogni raccolta.

I punti seguenti descrivono il modo in cui le raccolte interagiscono con il resto di [!DNL Recommendations]:

* [I consigli di backup](/help/main/c-recommendations/c-algorithms/backup-recs.md) generati per ciascun criterio utilizzano anche la raccolta, pertanto solo gli elementi della raccolta vengono inclusi nel consiglio di backup. Di conseguenza, vengono visualizzati solo i prodotti che hanno senso per una posizione.
* Le raccolte vengono ricreate o aggiornate a ogni esecuzione di ciascun criterio.
* Le regole di raccolta si applicano agli elementi di consigli generati dopo l’esecuzione dei criteri. Interessano solo i consigli di entità (ER) nell’output, non la chiave.
* Le raccolte non vengono applicate quando si utilizza la chiave di consiglio **[!UICONTROL Elementi visualizzati di recente]**.
* I criteri di inclusione possono produrre risultati simili, ma devono essere impostati ogni volta che viene creata un’attività. Una raccolta viene creata una volta e può quindi essere riutilizzata senza essere configurata di nuovo.
* Quando si crea o si modifica un&#39;attività [!DNL Recommendations], il nome della raccolta viene visualizzato accanto all&#39;etichetta **[!UICONTROL Criteri]** nel diagramma attività.

## Creare una raccolta {#task_1256DFF6842141FCAADD9E1428EF7F08}

Le raccolte sono disponibili a livello dell&#39;intero account, pertanto una raccolta creata una volta può essere selezionata in qualsiasi attività di [!DNL Recommendations]. Le regole sono definite nell’insieme, pertanto non è necessario impostarle nuovamente per ogni attività.

1. Fai clic su **[!UICONTROL Consigli]** > **[!UICONTROL Raccolte]** per visualizzare l&#39;elenco delle raccolte esistenti.

   Per modificare, copiare o eliminare una raccolta esistente, fare clic sull&#39;icona Altre azioni ( ![Icona Altre azioni](/help/main/assets/icons/MoreSmallList.svg) ) accanto alla raccolta, quindi fare clic sull&#39;opzione desiderata.

   >[!NOTE]
   >
   >Il &quot;Numero di elementi&quot; segnalato per ogni raccolta nella visualizzazione elenco **[!UICONTROL Raccolte]** è il numero di prodotti che corrispondono alle regole per tale raccolta all&#39;interno del gruppo predefinito di consigli [host](/help/main/administrating-target/hosts.md) (ambiente) configurato. Consulta [Impostazioni](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} per modificare il gruppo host predefinito.

1. Fai clic su **[!UICONTROL Crea raccolta]**.

   ![Pagina Raccolte con il pulsante Crea raccolta](../assets/collection_1.png)

1. Digita un **[!UICONTROL Nome]** per la raccolta. È inoltre possibile immettere una **[!UICONTROL Descrizione]** facoltativa.

1. (Condizionale) Scegliere un [ambiente](/help/main/administrating-target/environments.md) dal filtro **[!UICONTROL Ambiente]** per visualizzare in anteprima il contenuto della raccolta in tale ambiente. Per impostazione predefinita, sono visualizzati i risultati del gruppo di host predefinito.

1. Imposta le regole utilizzate per compilare la raccolta.

   Una raccolta può essere creata intorno a un ID prodotto, una categoria, un margine o qualsiasi altro parametro nell’elenco. Aggiungi regole per utilizzare più parametri per definire una raccolta. Più regole sono unite con un operatore AND, pertanto tutte le regole specificate devono corrispondere affinché la raccolta venga applicata.

1. Fai clic su **[!UICONTROL Crea]**.

1. Dopo aver creato la raccolta, fare clic sull&#39;icona Altre azioni ( ![Icona Altre azioni](/help/main/assets/icons/MoreSmallList.svg) ) e selezionare l&#39;opzione appropriata: **[!UICONTROL Modifica]**, **[!UICONTROL Copia]** o **[!UICONTROL Elimina]**.

   ![Elenco delle raccolte con il menu Altre azioni aperto, che mostra Modifica, Copia ed Elimina](../assets/collection_2.png)

<!--
## Create a collection using [!UICONTROL Advanced Search]

You can also create collections using [!UICONTROL Advanced Search] on the [Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]). 

![Save as dialog](/help/main/c-recommendations/c-products/assets/save-as.png)

After creating a search using "id > contains," for example, you can then click [!UICONTROL Save As] > [!UICONTROL Collection].

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create collections based on results using the [!UICONTROL Advanced Search] functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create a catalog with the intent to return products containing "holiday," only products containing "holiday" are returned. Products containing "Holiday" are not returned.
-->

## Utilizzare una raccolta in un’attività {#use-collection}

Viene selezionata una raccolta per ogni esperienza di un&#39;attività [!DNL Recommendations]. La raccolta determina gli elementi idonei a essere visualizzati nei consigli di tale esperienza.

1. [Crea una raccolta](#task_1256DFF6842141FCAADD9E1428EF7F08).

   ![Creare una schermata della raccolta con le sezioni Dettagli raccolta e Regole](../assets/collection_3.png)

1. Fai clic su **[!UICONTROL Attività]** e [crea una nuova attività Consigli](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md) o modifica un&#39;attività esistente.

   ![Pagina Tutte le attività con Recommendations selezionata nel menu Crea attività](../assets/collection_4.png)

1. Dopo aver selezionato un criterio e una progettazione, seleziona la raccolta desiderata nella pagina **[!UICONTROL Opzioni]**.

1. (Condizionale) Per modificare la raccolta di un&#39;attività esistente, fai clic su una posizione di consigli nelle pagine **[!UICONTROL Esperienze]**, fai clic su **[!UICONTROL Cambia raccolta]**, quindi seleziona la raccolta desiderata.
