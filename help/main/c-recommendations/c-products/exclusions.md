---
keywords: esclusioni
description: Scopri come creare esclusioni in [!DNL Target Recommendations] per impedire che prodotti o contenuti vengano consigliati ai visitatori.
title: Come si utilizzano le esclusioni nelle attività [!UICONTROL Recommendations]?
feature: Recommendations
exl-id: e41487c7-6d47-4958-8e4b-616a2ad56b3c
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 13%

---

# Esclusioni

Crea un&#39;esclusione in [!DNL Adobe Target Recommendations] per impedire che prodotti o contenuti vengano consigliati ai visitatori. Un’esclusione è un sottoinsieme di prodotti o contenuti che non devono essere consigliati ai visitatori.

Le esclusioni sono disponibili a livello dell&#39;intero account. A differenza delle raccolte, in cui si specifica una raccolta specifica per ogni esperienza durante la creazione di un&#39;attività [!UICONTROL Recommendations], le esclusioni si applicano a tutte le attività dell&#39;account. Non è possibile assegnare un gruppo di esclusione durante la creazione dell’attività.

Alcuni esempi di utilizzo delle esclusioni includono:

* Prodotti che sono stati sospesi.
* Il catalogo Autunno e Inverno è ora l&#39;unico catalogo che dovrebbe essere presente online. Tutti gli articoli del catalogo estivo non sono più disponibili per l&#39;acquisto.
* Articoli che potrebbero essere inappropriati da consigliare sulla maggior parte delle pagine o schermate (prodotti per adulti, film NC-17 e così via).
* Prodotti con campi di metadati incompleti (miniatura, prezzo o altri metadati importanti mancanti).
* Prodotti che non dovrebbero mai essere consigliati (forse nel sistema esiste una SKU per qualcosa, ma non è un articolo acquistabile. O forse è un finto SKU per il team di QA simulare un acquisto senza effettivamente ordinare qualcosa, e così via).

>[!IMPORTANT]
>
>Le regole di esclusione vengono applicate globalmente a tutti i [ambienti](/help/main/administrating-target/environments.md).
>
>Le regole di esclusione statica e dinamica sono funzioni molto efficaci che possono esserti utili nelle iniziative di marketing. Per informazioni dettagliate, esempi e scenari di utilizzo, consulta [Utilizzare regole di inclusione dinamiche e statiche](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

## Creare un’esclusione

1. Fai clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Exclusions]** per visualizzare l&#39;elenco delle esclusioni esistenti.

   Il &quot;Numero di elementi&quot; segnalato per ogni esclusione nella visualizzazione elenco [!UICONTROL Exclusions] è il numero di prodotti che corrispondono alle regole per tale esclusione all&#39;interno del gruppo Recommendations [host](/help/main/administrating-target/hosts.md) (ambiente) predefinito configurato. Per informazioni su come modificare il gruppo host predefinito, vedere [Pianificare e implementare [!DNL Recommendations]](https://experienceleague.adobe.com/en/docs/target-dev/developer/recommendations){target=_blank} nella *Guida per gli sviluppatori di Adobe Target*.

1. (Facoltativo) Fai clic sull&#39;icona **[!UICONTROL Show Filters]** ( ![icona Mostra filtri](/help/main/assets/icons/Filter.svg) ), quindi scegli l&#39;[ambiente](/help/main/administrating-target/environments.md) desiderato dall&#39;elenco a discesa **[!UICONTROL Environment]** durante la creazione (o l&#39;aggiornamento) di un&#39;esclusione per visualizzare in anteprima i contenuti dell&#39;esclusione in tale ambiente. Per impostazione predefinita, sono visualizzati i risultati del gruppo di host predefinito.

1. Fare clic su **[!UICONTROL Create Exclusion]**.

1. Digitare un&#39;esclusione **[!UICONTROL Name]** e immettere una descrizione facoltativa.

1. Utilizza il generatore di regole per creare le esclusioni.

   Selezionare un parametro nell&#39;elenco [!UICONTROL Rules], selezionare un operatore, quindi immettere uno o più valori per identificare i prodotti. Separa i valori con le virgole.

1. Fare clic su **[!UICONTROL Create]**.

<!-- ## Create an exclusion using Advanced Search

You can also create exclusions using [!UICONTROL Advanced Search] on the [Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]). 

![Save as dialog](/help/main/c-recommendations/c-products/assets/save-as.png)

After creating a search using "id > contains," for example, you can then click [!UICONTROL Save As] > [!UICONTROL Exclusion].

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create exclusions based on results using the Advanced Search functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create an exclusion with the intent to exclude products containing "holiday," only products containing "holiday" are excluded. Products containing "Holiday" are not excluded. -->

## Modificare, copiare o eliminare un’esclusione

Fai clic sull&#39;icona Altre azioni ( ![Icona Altre azioni](/help/main/assets/icons/MoreSmallList.svg) ) accanto all&#39;esclusione desiderata nell&#39;elenco, quindi fai clic sull&#39;icona appropriata: [!UICONTROL Edit], [!UICONTROL Copy] o [!UICONTROL Delete].

Puoi copiare un’esclusione esistente per creare un’esclusione duplicata che puoi quindi modificare. Questa opzione consente di creare un’esclusione simile con meno sforzo.

Tieni presente che le esclusioni sono disponibili in tutto l’account. Assicurati di considerare questa avvertenza prima di eliminare un’esclusione. Non è possibile recuperare le esclusioni eliminate.

## Video di formazione: Creare raccolte ed esclusioni in Recommendations (7:05) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video contiene le seguenti informazioni:

* Creare una raccolta
* Creare un’esclusione

>[!VIDEO](https://video.tv.adobe.com/v/27689)
