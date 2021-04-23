---
keywords: esclusioni
description: Scopri come creare esclusioni in Adobe [!DNL Target] Recommendations per evitare che prodotti o contenuti vengano consigliati ai visitatori.
title: Come si utilizzano le esclusioni nelle attività di Recommendations?
feature: Consigli
exl-id: e41487c7-6d47-4958-8e4b-616a2ad56b3c
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 44%

---

# Esclusioni

Crea un’esclusione in [!DNL Adobe Target Recommendations] per evitare che prodotti o contenuti vengano consigliati ai visitatori. Un’esclusione è un sottoinsieme di prodotti o contenuti che non devono essere consigliati ai visitatori.

Le esclusioni sono disponibili nell’intero account. A differenza delle raccolte, dove si specifica una raccolta specifica per ogni esperienza durante la creazione di un&#39;attività [!UICONTROL Recommendations], le esclusioni si applicano a tutte le attività in tutto l&#39;account. Non è possibile assegnare un gruppo di esclusione durante la creazione dell’attività.

Alcuni esempi di utilizzo delle esclusioni includono:

* Prodotti che sono stati interrotti
* Il catalogo Autunno/Inverno è ora l&#39;unico catalogo che dovrebbe essere presente online. Qualsiasi articolo del catalogo Estate non è più disponibile per l&#39;acquisto.
* Articoli che potrebbero essere inappropriati da consigliare sulla maggior parte delle pagine/schermi (prodotti per adulti, film NC-17, ecc.)
* Prodotti con campi di metadati incompleti (miniatura mancante, prezzo o altri metadati importanti)
* Prodotti che non dovrebbero mai essere raccomandati (forse esiste una SKU nel sistema per qualcosa ma non è un articolo acquistabile, o forse è una SKU falsa per il team QA simulare un acquisto senza ordinare effettivamente qualcosa, ecc,)

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

Puoi anche creare esclusioni utilizzando [!UICONTROL Ricerca avanzata] nella pagina [Ricerca nel catalogo](/help/c-recommendations/c-products/catalog-search.md#save-as) ( [!UICONTROL Recommendations] > [!UICONTROL Ricerca nel catalogo] > [!UICONTROL Ricerca avanzata]).

![Finestra di dialogo Salva con nome](/help/c-recommendations/c-products/assets/save-as.png)

Dopo aver creato una ricerca utilizzando “id > contiene”, ad esempio, è possibile fare clic su [!UICONTROL Salva con nome] > [!UICONTROL Esclusione].

>[!IMPORTANT]
>
>La funzionalità [!UICONTROL Ricerca avanzata] non distingue tra maiuscole e minuscole; tuttavia, i prodotti restituiti al momento della consegna si basano sulla ricerca con distinzione tra maiuscole e minuscole. Questa mancata corrispondenza potrebbe creare confusione. Assicurati di considerare la distinzione tra maiuscole e minuscole quando crei esclusioni in base ai risultati utilizzando la funzionalità Ricerca avanzata. Ad esempio, se esegui una ricerca per “Vacanza”, i risultati della ricerca iniziale contengono “Vacanza” e “vacanza”. Se poi crei un’esclusione con l’intento di escludere i prodotti contenenti “vacanza”, verranno esclusi solo i prodotti contenenti “vacanza”. ma non quelli contenenti “Vacanza”.

## Modificare, copiare o eliminare un’esclusione

Passa il puntatore del mouse sull’esclusione desiderata nell’elenco, quindi fai clic sull’icona appropriata: modificare, copiare o eliminare elementi.

![Icone al passaggio del mouse per un’esclusione](/help/c-recommendations/c-products/assets/hover-exclusions.png)

È possibile copiare un’esclusione esistente per creare un’esclusione duplicata da modificare. Questo ti consente di creare un’esclusione simile con meno sforzo.

Tieni presente che le esclusioni sono disponibili nell’intero account. Considera questo aspetto prima di eliminare un’esclusione. Le esclusioni eliminate non possono essere recuperate.

## Video di formazione: Creare raccolte ed esclusioni in Recommendations (7:05) ![Badge tutorial](/help/assets/tutorial.png)

Questo video contiene le seguenti informazioni:

* Creare una raccolta
* Creare un’esclusione

>[!VIDEO](https://video.tv.adobe.com/v/27689)
