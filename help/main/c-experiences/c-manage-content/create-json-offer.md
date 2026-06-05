---
keywords: offerta json;creare offerta json
description: Scopri come creare offerte JSON da utilizzare nel [!UICONTROL Compositore esperienza basato su moduli].
title: Come si creano le offerte JSON?
feature: Experiences and Offers
exl-id: 793665a4-4cd6-458f-8225-ba23e503a115
TQID: https://experienceleague.adobe.com/BI7N44iK4Ce2xOiz1vgh4O9efGZFAvK83RsL1368ItU
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: c93393a4-e558-47e1-992e-c91ed4d480ceid: f7c7de77-382f-4f48-8b36-61a170f06d3d
subfeature_v2: id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 506
ht-degree: 23%

---

# Creare offerte JSON

Crea offerte JSON nella [!UICONTROL Libreria di offerte] in [!DNL Adobe Target] da utilizzare nel [!UICONTROL Compositore esperienza basato su moduli].

Le offerte JSON possono essere utilizzate in attività basate su moduli per abilitare i casi d&#39;uso in cui è richiesto il decisioning di [!DNL Target] per inviare un&#39;offerta in formato JSON per l&#39;utilizzo in framework SPA (Single Page App) o integrazioni lato server.

## Considerazioni JSON

Quando lavori con le offerte JSON, considera quanto segue:

* Le offerte JSON sono attualmente disponibili solo per le attività [!UICONTROL Test A/B], [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Targeting esperienza] (XT).
* Le offerte JSON possono essere utilizzate solo in [attività basate su moduli](/help/main/c-experiences/form-experience-composer.md).
* Le offerte JSON possono essere recuperate direttamente quando si utilizzano le [API lato server e Mobile Node.js, Java, .NET e gli SDK Python](https://experienceleague.adobe.com/en/docs/target-dev/developer/server-side/server-side-overview){target=_blank}.
* Nel browser, le offerte JSON possono essere recuperate solo tramite at.js 1.2.3 (o versione successiva) e utilizzando [getOffer()](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffer){target=_blank} filtrando le azioni tramite l&#39;azione `setJson`.
* Le offerte JSON vengono consegnate come oggetti JSON nativi anziché come stringhe. I consumatori di questi oggetti non devono più gestire gli oggetti come stringhe e convertirli in oggetti JSON.
* Le offerte JSON non vengono applicate automaticamente, a differenza di altre offerte (come le offerte HTML), perché sono offerte non visive. Gli sviluppatori devono scrivere il codice per ottenere esplicitamente l&#39;offerta utilizzando [getOffer()](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffer){target=_blank}.

## Creare un’offerta JSON {#section_BB9C72D59DEA4EFB97A906AE7569AD7A}

1. Fai clic su **[!UICONTROL Offerte]** > **[!UICONTROL Offerte codice]**.
1. Fai clic su **[!UICONTROL Crea offerta]** > **[!UICONTROL Offerta JSON]**.
1. Digita un nome per l’offerta.
1. (Condizionale) Se hai un account [[!DNL Target] Premium](/help/main/c-intro/intro.md#premium), scegli l&#39;[area di lavoro](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#workspace) desiderata.
1. (Condizionale) Scegli gli attributi di profilo desiderati.
1. Digita o incolla il codice JSON nella casella **[!UICONTROL Codice]**.
1. Fai clic su **[!UICONTROL Crea]**.

## Esempio JSON {#section_A54F7BB2B55D4B7ABCD5002E0C72D8C9}

Le offerte JSON sono supportate solo nelle attività create utilizzando il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md). Attualmente l’unico modo per poter utilizzare le offerte JSON è tramite chiamate dirette API/SDK.

Di seguito è riportato un esempio:

![Finestra di dialogo Crea offerta JSON](/help/main/c-experiences/c-manage-content/assets/json-example.png)

Le azioni passate al callback di successo sono un array di oggetti. Supponendo di disporre di una singola offerta JSON, con questo contenuto:

```json
{ 
  "demo": {"a": 1, "b": 2} 
}
```

L’array di azioni presenta la seguente struttura:

```json
[ 
 { 
   action: "setJson", 
   content: [{ 
     "demo": {"a": 1, "b": 2} 
   }] 
 }  
]
```

Per estrarre l&#39;offerta JSON, è necessario eseguire iterazioni attraverso le azioni e trovare l&#39;azione con l&#39;azione `setJson`, quindi eseguire iterazioni attraverso l&#39;array di contenuto.

## Caso d’uso {#section_85B07907B51A43239C8E3498EF58B1E5}

Supponiamo che la seguente offerta JSON arrivi alla tua pagina web:

```json
{ 
    "_id": "5a65d24d8fafc966921e9169", 
    "index": 0, 
    "guid": "7c006504-c6f7-468d-a46f-f72531ea454c", 
    "isActive": true, 
    "balance": "$2,075.06", 
    "picture": "https://placehold.it/32x32", 
    "tags": [ 
      "esse", 
      "commodo", 
      "excepteur"
    ], 
    "friends": [ 
      { 
        "id": 0, 
        "name": "Carla Lyons" 
      }, 
      { 
        "id": 1, 
        "name": "Ollie Mooney" 
      } 
    ], 
    "greeting": "Hello, Stephenson Fernandez! You have 4 unread messages.", 
    "favoriteFruit": "strawberry" 
} 
  
```

Nel codice seguente viene illustrato come accedere all’attributo “greeting”:

```json
adobe.target.getOffer({   
  "mbox": "name_of_mbox", 
  "params": {}, 
  "success": function(offer) {           
        console.log(offer[0].content[0].greeting); 
  },   
  "error": function(status, error) {           
      console.log('Error', status, error); 
  } 
});
```

## Esempio di offerta JSON con attributi di profilo Real-time CDP

Gli attributi del profilo Real-Time CDP possono essere condivisi con [!DNL Target] per l&#39;utilizzo nelle offerte HTML e JSON.

Per ulteriori informazioni, consulta [Condividere gli attributi del profilo Real-time CDP con [!DNL Target]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#rtcdp-profile-attributes).

## Filtraggio delle offerte per tipo di offerta JSON {#section_52533555BCE6420C8A95EB4EB8907BDE}

Puoi filtrare la libreria [!UICONTROL Offerte] in base al tipo di offerta JSON facendo clic sull&#39;icona **[!UICONTROL Mostra filtri]** ( ![Mostra icona Filtri](/help/main/assets/icons/Filter.svg) ), quindi selezionando la casella di controllo **[!UICONTROL Offerte JSON]**.
