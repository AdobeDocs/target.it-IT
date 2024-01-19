---
keywords: esclusioni
description: Scopri come creare esclusioni in Adobe [!DNL Target] Recommendations per impedire che prodotti o contenuti vengano consigliati ai visitatori.
title: Come si utilizzano le esclusioni nelle attività di Recommendations?
feature: Recommendations
exl-id: e41487c7-6d47-4958-8e4b-616a2ad56b3c
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 34%

---

# Esclusioni

Creare un’esclusione in [!DNL Adobe Target Recommendations] per evitare che prodotti o contenuti vengano consigliati ai visitatori. Un’esclusione è un sottoinsieme di prodotti o contenuti che non devono essere consigliati ai visitatori.

Le esclusioni sono disponibili a livello dell&#39;intero account. A differenza delle raccolte, in cui si specifica una raccolta specifica per ogni esperienza durante la creazione di un [!UICONTROL Recommendations] attività, le esclusioni si applicano a tutte le attività nell’account. Non è possibile assegnare un gruppo di esclusione durante la creazione dell’attività.

Alcuni esempi di utilizzo delle esclusioni includono:

* Prodotti che sono stati sospesi
* Il catalogo Autunno/Inverno è ora l&#39;unico catalogo che dovrebbe essere presente online. Tutti gli articoli del catalogo estivo non sono più disponibili per l&#39;acquisto.
* Articoli che potrebbero essere inappropriati da consigliare sulla maggior parte delle pagine/schermate (prodotti per adulti, film NC-17, ecc.)
* Prodotti con campi di metadati incompleti (miniatura, prezzo o altri metadati importanti mancanti)
* Prodotti che non dovrebbero mai essere consigliati (forse nel sistema esiste una SKU per qualcosa, ma non è un articolo acquistabile, o forse è una SKU falsa per il team di QA simulare un acquisto senza effettivamente ordinare qualcosa, ecc.)

>[!IMPORTANT]
>
>Le regole di esclusione vengono applicate a livello globale a tutti gli ambienti.
>
>Le regole di esclusione statica e dinamica sono funzioni molto efficaci che possono esserti utili nelle iniziative di marketing. Per informazioni dettagliate, esempi e scenari di utilizzo, consulta [Utilizzare regole di inclusione dinamiche e statiche](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

## Creare un’esclusione

1. Clic **[!UICONTROL Recommendations]** > **[!UICONTROL Esclusioni]** per visualizzare l’elenco delle esclusioni esistenti.

   ![immagine elenco_esclusioni](assets/exclusions_list.png)

   Il “Numero di elementi” segnalato per ogni esclusione nella visualizzazione elenco [!UICONTROL Esclusioni] è il numero di prodotti che corrispondono alle regole per tale esclusione all’interno del [gruppo di host](/help/main/administrating-target/hosts.md) Consigli (ambiente) predefinito configurato. Consulta [Impostazioni](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank} per modificare il gruppo host predefinito.

1. Clic **[!UICONTROL Crea esclusione]**.

1. (Condizionale) Scegli un ambiente dalla sezione **[!UICONTROL Ambiente]** filtrare durante la creazione (o l’aggiornamento) di un’esclusione per visualizzare in anteprima il contenuto dell’esclusione in tale ambiente. Per impostazione predefinita, sono visualizzati i risultati del gruppo di host predefinito.

   ![Creare un’esclusione](/help/main/c-recommendations/c-products/assets/CreateExclusion.png)

1. Digita un’esclusione **[!UICONTROL Nome]** e inserisci una descrizione facoltativa.

1. Utilizza il generatore di regole per creare le esclusioni.

   Seleziona un parametro nell’elenco delle regole, seleziona un operatore, quindi immetti uno o più valori per identificare i prodotti. Separa i valori con le virgole.

1. Fai clic su **[!UICONTROL Salva]**.

## Creare un’esclusione utilizzando Ricerca avanzata

Puoi anche creare esclusioni utilizzando [!UICONTROL Ricerca avanzata] il [Ricerca nel catalogo](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ( [!UICONTROL Recommendations] > [!UICONTROL Ricerca nel catalogo] > [!UICONTROL Ricerca avanzata]).

![Finestra di dialogo Salva con nome](/help/main/c-recommendations/c-products/assets/save-as.png)

Dopo aver creato una ricerca utilizzando “id > contiene”, ad esempio, è possibile fare clic su [!UICONTROL Salva con nome] > [!UICONTROL Esclusione].

>[!IMPORTANT]
>
>Il [!UICONTROL Ricerca avanzata] La funzionalità non distingue tra maiuscole e minuscole, tuttavia, i prodotti restituiti al momento della consegna si basano sulla ricerca con distinzione tra maiuscole e minuscole. Questa mancata corrispondenza potrebbe creare confusione. Assicurati di considerare la distinzione tra maiuscole e minuscole quando crei esclusioni in base ai risultati utilizzando la funzionalità Ricerca avanzata. Ad esempio, se esegui una ricerca per “Vacanza”, i risultati della ricerca iniziale contengono “Vacanza” e “vacanza”. Se poi crei un’esclusione con l’intento di escludere i prodotti contenenti “vacanza”, verranno esclusi solo i prodotti contenenti “vacanza”. ma non quelli contenenti “Vacanza”.

## Modificare, copiare o eliminare un’esclusione

Passa il cursore del mouse sull’esclusione desiderata nell’elenco, quindi fai clic sull’icona appropriata: modifica, copia o elimina.

![Icone al passaggio del mouse per un’esclusione](/help/main/c-recommendations/c-products/assets/hover-exclusions.png)

Puoi copiare un’esclusione esistente per creare un’esclusione duplicata che puoi quindi modificare. Questo consente di creare un’esclusione simile con meno sforzo.

Tieni presente che le esclusioni sono disponibili in tutto l’account. Prima di eliminare un’esclusione, tieni presente quanto segue. Non è possibile recuperare le esclusioni eliminate.

## Video di formazione: Creare raccolte ed esclusioni in Recommendations (7:05) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video contiene le seguenti informazioni:

* Creare una raccolta
* Creare un’esclusione

>[!VIDEO](https://video.tv.adobe.com/v/27689)
