---
keywords: esclusioni
description: Scopri come creare esclusioni in [!DNL Target Recommendations] per evitare che prodotti o contenuti vengano consigliati ai visitatori.
title: Come si utilizzano le esclusioni in [!UICONTROL Recommendations] Attività?
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: 31cf23a52c331eabad0e5f6423eeeca84df87625
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 18%

---

# Esclusioni

Creare un’esclusione in [!DNL Adobe Target Recommendations] per evitare che prodotti o contenuti vengano consigliati ai visitatori. Un’esclusione è un sottoinsieme di prodotti o contenuti che non devono essere consigliati ai visitatori.

Le esclusioni sono disponibili a livello dell&#39;intero account. A differenza delle raccolte, in cui si specifica una raccolta specifica per ogni esperienza durante la creazione di un [!UICONTROL Recommendations] attività, le esclusioni si applicano a tutte le attività nell’account. Non è possibile assegnare un gruppo di esclusione durante la creazione dell’attività.

Alcuni esempi di utilizzo delle esclusioni includono:

* Prodotti che sono stati sospesi.
* Il catalogo Autunno e Inverno è ora l&#39;unico catalogo che dovrebbe essere presente online. Tutti gli articoli del catalogo estivo non sono più disponibili per l&#39;acquisto.
* Articoli che potrebbero essere inappropriati da consigliare sulla maggior parte delle pagine o schermate (prodotti per adulti, film NC-17 e così via).
* Prodotti con campi di metadati incompleti (miniatura, prezzo o altri metadati importanti mancanti).
* Prodotti che non dovrebbero mai essere consigliati (forse nel sistema esiste una SKU per qualcosa, ma non è un articolo acquistabile. O forse è un finto SKU per il team di QA simulare un acquisto senza effettivamente ordinare qualcosa, e così via).

>[!IMPORTANT]
>
>Le regole di esclusione vengono applicate a livello globale a tutti [ambienti](/help/main/administrating-target/environments.md).
>
>Le regole di esclusione statica e dinamica sono funzioni molto efficaci che possono esserti utili nelle iniziative di marketing. Per informazioni dettagliate, esempi e scenari di utilizzo, consulta [Utilizzare regole di inclusione dinamiche e statiche](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

## Creare un’esclusione

1. Clic **[!UICONTROL Recommendations]** > **[!UICONTROL Exclusions]** per visualizzare l’elenco delle esclusioni esistenti.

   ![immagine elenco_esclusioni](assets/exclusions-list.png)

   Il &quot;Numero di elementi&quot; segnalato per ogni esclusione sulla [!UICONTROL Exclusions] vista a elenco è il numero di prodotti che corrispondono alle regole per tale esclusione all’interno del Recommendations predefinito configurato [gruppo host](/help/main/administrating-target/hosts.md) (ambiente). Consulta [Pianificare e implementare [!DNL Recommendations]](https://experienceleague.adobe.com/en/docs/target-dev/developer/recommendations){target=_blank} nel *Guida per gli sviluppatori di Adobe Target* per informazioni su come modificare il gruppo host predefinito.

1. (Condizionale) Fai clic su [!UICONTROL Filter] , quindi scegli il [ambiente](/help/main/administrating-target/environments.md) dal **[!UICONTROL Environment]** durante la creazione (o l’aggiornamento) di un’esclusione per visualizzare in anteprima i contenuti dell’esclusione in tale ambiente. Per impostazione predefinita, sono visualizzati i risultati del gruppo di host predefinito.

   ![Creare un’esclusione](/help/main/c-recommendations/c-products/assets/choose-environment.png)

1. Clic **[!UICONTROL Create Exclusion]**.

   ![Finestra di dialogo Crea esclusione](/help/main/c-recommendations/c-products/assets/create-exclusion.png)

1. Digita un’esclusione **[!UICONTROL Name]** e inserisci una descrizione facoltativa.

1. Utilizza il generatore di regole per creare le esclusioni.

   Seleziona un parametro nell’elenco delle regole, seleziona un operatore, quindi immetti uno o più valori per identificare i prodotti. Separa i valori con le virgole.

1. Clic **[!UICONTROL Create]**.

<!-- ## Create an exclusion using Advanced Search

You can also create exclusions using [!UICONTROL Advanced Search] on the [Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]). 

![Save as dialog](/help/main/c-recommendations/c-products/assets/save-as.png)

After creating a search using "id > contains," for example, you can then click [!UICONTROL Save As] > [!UICONTROL Exclusion].

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create exclusions based on results using the Advanced Search functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create an exclusion with the intent to exclude products containing "holiday," only products containing "holiday" are excluded. Products containing "Holiday" are not excluded. -->

## Modificare, copiare o eliminare un’esclusione

Fai clic su **puntini di sospensione** accanto all’esclusione desiderata nell’elenco, quindi fai clic sull’icona appropriata: modifica, copia o elimina.

![Opzioni: modifica, copia ed elimina](/help/main/c-recommendations/c-products/assets/edit-copy-delete.png)

Puoi copiare un’esclusione esistente per creare un’esclusione duplicata che puoi quindi modificare. Questa opzione consente di creare un’esclusione simile con meno sforzo.

Tieni presente che le esclusioni sono disponibili in tutto l’account. Assicurati di considerare questa avvertenza prima di eliminare un’esclusione. Non è possibile recuperare le esclusioni eliminate.

## Video di formazione: Creare raccolte ed esclusioni in Recommendations (7:05) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video contiene le seguenti informazioni:

* Creare una raccolta
* Creare un’esclusione

>[!VIDEO](https://video.tv.adobe.com/v/27689)