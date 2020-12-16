---
keywords: exclusions
description: Create un'esclusione in [!DNL Adobe Target Recommendations] per evitare che prodotti o contenuti vengano raccomandati ai visitatori.
title: Esclusioni in Adobe Target
feature: entities
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 45%

---


# Esclusioni{#exclusions}

Create un&#39;esclusione in [!DNL Adobe Target Recommendations] per evitare che prodotti o contenuti vengano raccomandati ai visitatori. Un&#39;esclusione è un sottoinsieme di prodotti o contenuti che non dovrebbero essere raccomandati ai visitatori.

Le esclusioni sono disponibili per l&#39;intero account. A differenza delle raccolte, dove si specifica una raccolta specifica per ogni esperienza durante la creazione di un&#39;attività [!UICONTROL Recommendations], le esclusioni si applicano a tutte le attività dell&#39;account. Non è disponibile alcuna opzione per assegnare un gruppo di esclusione durante la creazione dell&#39;attività.

Alcuni esempi di volte in cui si utilizzano le esclusioni:

* Prodotti che sono stati interrotti
* Il catalogo Autunno/Inverno è ora l&#39;unico catalogo che dovrebbe essere presente online. Qualsiasi articolo del catalogo Estate non è più disponibile per l&#39;acquisto.
* Elementi che potrebbero essere inopportuni da consigliare sulla maggior parte delle pagine/schermi (prodotti per adulti, film NC-17, ecc.)
* Prodotti con campi di metadati incompleti (miniatura mancante, prezzo o altri metadati importanti)
* Prodotti che non dovrebbero mai essere raccomandati (forse esiste uno SKU nel sistema per qualcosa, ma non è un articolo acquistabile, o forse è un falso SKU per il team di QA per simulare un acquisto senza ordinare qualcosa, ecc.)

>[!IMPORTANT]
>
>Le regole di esclusione statica e dinamica sono funzioni molto efficaci che possono esserti utili nelle iniziative di marketing. Per informazioni dettagliate, esempi e scenari di utilizzo, consulta [Utilizzare regole di inclusione dinamiche e statiche](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

## Creare un’esclusione

1. Fai clic su **[!UICONTROL Consigli]** > **[!UICONTROL Esclusioni]** per visualizzare l&#39;elenco delle esclusioni esistenti.

   ![](assets/exclusions_list.png)

   Il “Numero di elementi” segnalato per ogni esclusione nella visualizzazione elenco [!UICONTROL Esclusioni] è il numero di prodotti che corrispondono alle regole per tale esclusione all’interno del [gruppo di host](/help/administrating-target/hosts.md) Consigli (ambiente) predefinito configurato. Consulta [Impostazioni](/help/c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84) per modificare il gruppo host predefinito.

1. Fai clic su **[!UICONTROL Crea esclusione]**.

1. (Facoltativo) Scegli un ambiente dal filtro **[!UICONTROL Ambiente]** quando crei (o aggiorni) un’esclusione per visualizzare in anteprima i contenuti dell’esclusione tale ambiente. Per impostazione predefinita, sono visualizzati i risultati del gruppo di host predefinito.

   ![Creare un’esclusione](/help/c-recommendations/c-products/assets/CreateExclusion.png)

1. Digita un **[!UICONTROL Nome]** per l’esclusione e immetti una descrizione facoltativa.

1. Utilizza il generatore di regole per creare le esclusioni.

   Seleziona un parametro nell’elenco delle regole, seleziona un operatore, quindi immetti uno o più valori per identificare i prodotti. Separa i valori con le virgole.

1. Fai clic su **[!UICONTROL Salva]**.

## Creare un’esclusione utilizzando Ricerca avanzata

È inoltre possibile creare esclusioni utilizzando [!UICONTROL Ricerca avanzata] nella pagina [Ricerca nel catalogo](/help/c-recommendations/c-products/catalog-search.md#save-as) ( [!UICONTROL Recommendations] > [!UICONTROL Ricerca nel catalogo] > [!UICONTROL Ricerca avanzata]).

![Salva con nome, finestra di dialogo](/help/c-recommendations/c-products/assets/save-as.png)

Dopo aver creato una ricerca utilizzando “id > contiene”, ad esempio, è possibile fare clic su [!UICONTROL Salva con nome] > [!UICONTROL Esclusione].

>[!IMPORTANT]
>
>La funzionalità [!UICONTROL Ricerca avanzata] non fa distinzione tra maiuscole e minuscole; tuttavia, i prodotti restituiti al momento della consegna si basano su ricerche con distinzione tra maiuscole e minuscole. Questa mancata corrispondenza potrebbe creare confusione. Assicurati di considerare la distinzione tra maiuscole e minuscole quando crei esclusioni in base ai risultati utilizzando la funzionalità Ricerca avanzata. Ad esempio, se esegui una ricerca per “Vacanza”, i risultati della ricerca iniziale contengono “Vacanza” e “vacanza”. Se poi crei un’esclusione con l’intento di escludere i prodotti contenenti “vacanza”, verranno esclusi solo i prodotti contenenti “vacanza”. ma non quelli contenenti “Vacanza”.

## Modificare, copiare o eliminare un&#39;esclusione

Passate il puntatore del mouse sull&#39;esclusione desiderata nell&#39;elenco, quindi fate clic sull&#39;icona appropriata: modificare, copiare o eliminare.

![Icone al passaggio del mouse per un&#39;esclusione](/help/c-recommendations/c-products/assets/hover-exclusions.png)

È possibile copiare un&#39;esclusione esistente per creare una doppia esclusione da modificare. Questo consente di creare un&#39;esclusione simile con meno sforzi.

Tieni presente che le esclusioni sono disponibili per l&#39;intero account. Prima di eliminare un&#39;esclusione, è necessario tenere presente questo aspetto. Le esclusioni eliminate non possono essere recuperate.

## Video di formazione: Creare raccolte ed esclusioni in Recommendations (7:05) ![Logo delle esercitazioni](/help/assets/tutorial.png)

Questo video contiene le seguenti informazioni:

* Creare una raccolta
* Creare un’esclusione

>[!VIDEO](https://video.tv.adobe.com/v/27689)