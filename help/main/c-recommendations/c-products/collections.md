---
keywords: raccolta;Targeting
description: Scopri come utilizzare le raccolte di prodotti o elementi in [!DNL Target Recommendations].
title: Come si utilizzano le raccolte nelle attività Consigli?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: e62f501b-3521-4456-9ea1-e4b8a2b478c6
TQID: https://experienceleague.adobe.com/kdjl2cpjaRWYZRqHFqARHvbTaTuu0iAH7ZWbD2Lrs7o
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 16fb7a1902ea76cab56a93fa141a32a3c6bc4467
workflow-type: tm+mt
source-wordcount: 755
ht-degree: 27%

---

# Raccolte

Una raccolta è un insieme di prodotti o elementi che sono considerati idonei per essere proposti come consigli. Una raccolta viene definita specificando le condizioni che devono essere soddisfatte dagli elementi affinché ne facciano parte.

Solitamente, una raccolta è un insieme di elementi simili o correlati, come una raccolta di prodotti singoli. Tuttavia, puoi raggruppare qualsiasi elemento in una categoria adatta alla tua attività, ad esempio prodotti in una determinata fascia di prezzo o colore o articoli che potrebbero essere interessanti in una particolare area geografica.

Utilizza le raccolte per organizzare i prodotti in raggruppamenti logici. Ad esempio, se alcuni elementi sono disponibili in un’area ma non in un’altra, puoi creare una raccolta che escluda gli elementi non disponibili nell’area del visitatore. Puoi inoltre utilizzare le raccolte per organizzare gli elementi stagionali o qualsiasi altro parametro organizzativo applicabile al tuo business.

Anche i [consigli di backup](/help/main/c-recommendations/c-algorithms/backup-recs.md) generati per ogni criterio all&#39;interno del consiglio utilizzano questa raccolta, in modo che solo gli elementi della raccolta siano inclusi nel consiglio di backup. Le raccolte consentono di garantire la visualizzazione dei soli prodotti che ha senso mostrare in una determinata posizione.

Le raccolte vengono ricreate o aggiornate a ogni esecuzione di ciascun criterio.

Puoi raggruppare gli elementi in cataloghi e quindi creare consigli separati per ogni raccolta.

I criteri di inclusione consentono di eseguire operazioni simili su una raccolta, ma devono essere impostati ogni volta che si crea una attività. Le raccolte consentono di creare un insieme di elementi una sola volta e di utilizzarlo ogni volta che è opportuno senza doverlo impostare nuovamente.

Quando si crea o si modifica un&#39;attività [!DNL Recommendations], il nome della raccolta viene visualizzato accanto all&#39;etichetta [!UICONTROL Criteri] nel diagramma attività.

>[!NOTE]
>
>* Le regole di raccolta si applicano agli elementi di consigli generati dopo l’esecuzione dei criteri. Interessano solo i consigli di entità (ER) nell’output, non la chiave.
>
>* Le raccolte non vengono applicate quando si utilizza la chiave di consiglio [!UICONTROL Elementi visualizzati di recente].

## Creazione di una raccolta {#task_1256DFF6842141FCAADD9E1428EF7F08}

Crea una raccolta per organizzare i prodotti o i contenuti da mostrare nei consigli.

1. Fai clic su **[!UICONTROL Consigli]** > **[!UICONTROL Raccolte]** per visualizzare l&#39;elenco delle raccolte esistenti.

   Nella pagina [!UICONTROL Raccolte] viene visualizzato un elenco delle raccolte esistenti. Per creare nuove raccolte, fai clic sul pulsante [!UICONTROL Crea raccolta]. È inoltre possibile modificare, copiare ed eliminare raccolte esistenti facendo clic sull&#39;icona Altre azioni ( ![Icona Altre azioni](/help/main/assets/icons/MoreSmallList.svg) ) accanto alla raccolta desiderata e quindi facendo clic sull&#39;opzione desiderata.

   Il &quot;Numero di elementi&quot; segnalato per ogni raccolta nella visualizzazione elenco [!UICONTROL Raccolte] è il numero di prodotti che corrispondono alle regole per tale raccolta all&#39;interno del gruppo predefinito di consigli [host](/help/main/administrating-target/hosts.md) (ambiente) configurato. Consulta [Impostazioni](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} per modificare il gruppo host predefinito.

1. Fai clic su **[!UICONTROL Crea raccolta]**.

1. Digita un **[!UICONTROL Nome]** per la raccolta.

   È inoltre possibile immettere una **[!UICONTROL Descrizione]** facoltativa.

1. (Facoltativo) Scegli un [ambiente](/help/main/administrating-target/environments.md) dal filtro **[!UICONTROL ambiente]** durante la creazione (o l&#39;aggiornamento) di una raccolta per visualizzare in anteprima i contenuti della raccolta in tale ambiente. Per impostazione predefinita, sono visualizzati i risultati del gruppo di host predefinito.

1. Imposta le regole utilizzate per compilare la raccolta.

   Ad esempio, la raccolta potrebbe essere basata su un ID o categoria di prodotto, un margine, o qualsiasi altro parametro nell’elenco.

   È possibile aggiungere regole per utilizzare più parametri con cui definire una raccolta. Più regole sono unite con un operatore AND. Tutte le regole specificate devono essere soddisfatte perché la raccolta venga applicata.

1. Fai clic su **[!UICONTROL Crea]**.

<!--
## Create a collection using [!UICONTROL Advanced Search]

You can also create collections using [!UICONTROL Advanced Search] on the [Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ([!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]). 

![Save as dialog](/help/main/c-recommendations/c-products/assets/save-as.png)

After creating a search using "id > contains," for example, you can then click [!UICONTROL Save As] > [!UICONTROL Collection].

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create collections based on results using the [!UICONTROL Advanced Search] functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create a catalog with the intent to return products containing "holiday," only products containing "holiday" are returned. Products containing "Holiday" are not returned.
-->

## Modificare, copiare o eliminare una raccolta

Fai clic sull&#39;icona ( ![Altre azioni](/help/main/assets/icons/MoreSmallList.svg) ) accanto alla raccolta desiderata nell&#39;elenco, quindi fai clic sull&#39;icona appropriata: [!UICONTROL Modifica], [!UICONTROL Copia], o [!DNL Delete].

Puoi copiare una raccolta esistente per crearne una duplicata da modificare. Questo consente di creare una raccolta simile con meno sforzo.

Tieni presente che le raccolte sono disponibili a livello dell’intero account. Prima di eliminare una raccolta, tienilo in considerazione. Non è possibile recuperare le raccolte eliminate.

## Utilizzare una raccolta in un&#39;attività [!DNL Recommendations]

1. Crea una raccolta utilizzando uno dei metodi indicati sopra.

1. Fai clic su **[!UICONTROL Attività]** e [crea una nuova attività Consigli](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md) o modifica un&#39;attività esistente.

1. Dopo aver selezionato un criterio e una progettazione, nella pagina [!UICONTROL Opzioni] viene visualizzata la posizione in cui è stata selezionata la raccolta desiderata.

1. (Condizionale) Per modificare un&#39;impostazione di raccolta esistente, nella pagina **[!UICONTROL Esperienze]** (passaggio 1 del flusso di lavoro guidato in tre parti), fai clic su un percorso in cui hai inserito i consigli, fai clic su **[!UICONTROL Cambia raccolta]**, quindi seleziona la raccolta desiderata.
