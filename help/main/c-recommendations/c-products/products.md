---
keywords: prodotto;collezioni
description: Informazioni sulle entità in Consigli di Adobe [!DNL Target]. Le entità si riferiscono agli elementi che si desidera consigliare utilizzando [!DNL Target], ad esempio articoli, film o prodotti.
title: Come si utilizzano le entità?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: ffe23eea-b914-4c86-ad54-c63c1cc1c0d7
TQID: 'https://experienceleague.adobe.com/zfISb59XJ5qrD1-FA0syglPPswIL8cA0N0pBpY4tgIE'
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
source-git-commit: 5ed511322cc9f04c349471f8ad84a17526d4925f
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%
---
# Introduzione alle entità {#get-started-entities}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri le entità presenti in [!DNL Adobe Target Recommendations] e dove gestirle.

>[!ENDSHADEBOX]

Le entità sono gli elementi che [!DNL Recommendations] può consigliare. Un’entità può essere un prodotto, un contenuto (ad esempio un articolo, una presentazione di diapositive, un’immagine, un film o un programma TV), un’offerta di lavoro, un ristorante e così via.

[!DNL Recommendations] visualizza gli elementi delle raccolte in base ai criteri impostati.

## Come le entità raggiungono i consigli

Le informazioni sulle entità possono essere passate a [!DNL Recommendations] in diversi modi, tra cui:

* Con [attributi di entità](/help/main/c-recommendations/c-products/entity-attributes.md) inviati dalle pagine, utilizzando una mbox o `targetPageParams`.
* Con [feed](/help/main/c-recommendations/c-products/feeds.md), che può utilizzare file CSV, il formato di feed [!DNL Google Product Search] o le classificazioni di prodotto [!DNL Adobe Analytics].
* Con l’API di consegna.

Se [!DNL Target] raccoglie dati per un elemento sia da un feed che da una mbox, vengono utilizzati i dati più recenti.

I valori delle entità e degli attributi di entità caricati scadono dopo 61 giorni. Invia di nuovo ogni elemento almeno una volta ogni 60 giorni. In caso contrario, [!DNL Target] considera l&#39;elemento non più rilevante e lo rimuove dal catalogo.

## Gestire le entità

Utilizza le pagine seguenti per lavorare con le entità:

* [Attributi di entità](/help/main/c-recommendations/c-products/entity-attributes.md) e [Attributi di entità personalizzati](/help/main/c-recommendations/c-products/custom-entity-attributes.md): definire le informazioni sul prodotto o sul contenuto passate a [!DNL Recommendations].
* [Feed](/help/main/c-recommendations/c-products/feeds.md): inserisci informazioni su entità o contenuto nei consigli.
* [Ricerca nel catalogo](/help/main/c-recommendations/c-products/catalog-search.md): individua gli elementi nel catalogo.
* [Raccolte](/help/main/c-recommendations/c-products/collections.md): configura le raccolte. Quando si crea un&#39;attività [!DNL Recommendations], viene selezionata una raccolta per ogni esperienza.
* [Esclusioni](/help/main/c-recommendations/c-products/exclusions.md): impedisce la visualizzazione di alcuni elementi nei consigli. Le esclusioni si applicano a tutte le attività nell’account.
