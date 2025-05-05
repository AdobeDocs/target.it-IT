---
keywords: offerta json;creare offerta json
description: Scopri come creare offerte JSON da utilizzare in [!UICONTROL Form-Based Experience Composer].
title: Come si creano le offerte JSON?
feature: Experiences and Offers
exl-id: 793665a4-4cd6-458f-8225-ba23e503a115
source-git-commit: e8201198dc6ac36e803153d5c6b345a30716204a
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 24%

---

# Creare offerte JSON

Crea offerte JSON in [!UICONTROL Offer Library] in [!DNL Adobe Target] da utilizzare in [!UICONTROL Form-Based Experience Composer].

Le offerte JSON possono essere utilizzate in attività basate su moduli per abilitare i casi d&#39;uso in cui è richiesto il decisioning di [!DNL Target] per inviare un&#39;offerta in formato JSON da utilizzare nel framework SPA o nelle integrazioni lato server.

## Considerazioni JSON

Quando lavori con le offerte JSON, considera quanto segue:

* Le offerte JSON sono attualmente disponibili solo per [!UICONTROL A/B Test], [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Experience Targeting] (XT) attività.
* Le offerte JSON possono essere utilizzate solo in [attività basate su moduli](/help/main/c-experiences/form-experience-composer.md).
* Le offerte JSON possono essere recuperate direttamente quando si utilizzano le [API lato server e Mobile Node.js, Java, .NET e gli SDK Python](https://experienceleague.adobe.com/it/docs/target-dev/developer/server-side/server-side-overview){target=_blank}.
* Nel browser, le offerte JSON possono essere recuperate solo tramite at.js 1.2.3 (o versione successiva) e utilizzando [getOffer()](https://experienceleague.adobe.com/it/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffer){target=_blank} filtrando le azioni tramite l&#39;azione `setJson`.
* Le offerte JSON vengono consegnate come oggetti JSON nativi anziché come stringhe. I consumatori di questi oggetti non devono più gestire gli oggetti come stringhe e convertirli in oggetti JSON.
* Le offerte JSON non vengono applicate automaticamente, a differenza di altre offerte (come le offerte HTML), perché sono offerte non visive. Gli sviluppatori devono scrivere il codice per ottenere esplicitamente l&#39;offerta utilizzando [getOffer()](https://experienceleague.adobe.com/it/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffer){target=_blank}.

## Creare un’offerta JSON {#section_BB9C72D59DEA4EFB97A906AE7569AD7A}

1. Fare clic su **[!UICONTROL Offers]** > **[!UICONTROL Code Offers]**.
1. Fare clic su **[!UICONTROL Create Offer]** > **[!UICONTROL JSON Offer]**.
1. Digita un nome per l’offerta.
1. (Condizionale) Se hai un account [[!DNL Target] Premium](/help/main/c-intro/intro.md#premium), scegli l&#39;[area di lavoro](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#workspace) desiderata.
1. (Condizionale) Scegli gli attributi di profilo desiderati.
1. Digita o incolla il codice JSON nella casella **[!UICONTROL Code]**.
1. Fare clic su **[!UICONTROL Create]**.

## Esempio JSON {#section_A54F7BB2B55D4B7ABCD5002E0C72D8C9}

Le offerte JSON sono supportate solo nelle attività create utilizzando il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md). Attualmente l’unico modo per poter utilizzare le offerte JSON è tramite chiamate dirette API/SDK.

Ecco un esempio:

![Finestra di dialogo Crea offerta JSON](/help/main/c-experiences/c-manage-content/assets/json-example.png)

Le azioni passate al callback di successo sono una matrice di oggetti. Supponendo di disporre di una singola offerta JSON, con questo contenuto:

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

È possibile filtrare la libreria [!UICONTROL Offers] in base al tipo di offerta JSON facendo clic sull&#39;icona **[!UICONTROL Show filters]** ( ![icona Mostra filtri](/help/main/assets/icons/Filter.svg) ), quindi selezionando la casella di controllo **[!UICONTROL JSON Offers]**.
