---
keywords: offerta remota;creazione di offerta remota
description: Scopri come creare offerte JSON in Adobe [!DNL Target] da utilizzare nel Compositore esperienza basato su moduli. Le offerte JSON sono utili per i framework SPA o le integrazioni lato server.
title: Come si creano offerte JSON?
feature: Experiences and Offers
exl-id: 793665a4-4cd6-458f-8225-ba23e503a115
source-git-commit: a0a20b99a76ba0346f00e3841a345e916ffde8ea
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 49%

---

# Creare offerte JSON

Creare offerte JSON in [!UICONTROL Libreria offerte] in [!DNL Adobe Target] per l&#39;utilizzo in [!UICONTROL Compositore esperienza basato su moduli].

Le offerte JSON possono essere utilizzate in attività basate su moduli per casi d’uso in cui [!DNL Target]Il processo decisionale di è necessario per inviare un’offerta in formato JSON da utilizzare in SPA framework o integrazioni lato server.

## Considerazioni JSON

Quando lavori con le offerte JSON, considera quanto segue:

* Le offerte JSON sono attualmente disponibili solo per [!UICONTROL Test A/B] e [!UICONTROL Targeting esperienza] Attività (XT).
* Le offerte JSON possono essere utilizzate in [attività basate su moduli](/help/main/c-experiences/form-experience-composer.md) solo.
* L’offerta JSON può essere recuperata direttamente quando utilizzi API lato server, SDK per dispositivi mobili o SDK per NodeJS.
* Nel browser, le offerte JSON possono essere recuperate SOLO tramite at.js 1.2.3 (o versione successiva) e utilizzando [getOffer()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffer/){target=_blank} filtrando le azioni utilizzando `setJson` azione.
* Le offerte JSON vengono consegnate come oggetti JSON nativi anziché come stringhe. I consumatori di questi oggetti non devono più gestire gli oggetti come stringhe e convertirli in oggetti JSON.
* Le offerte JSON non vengono applicate automaticamente, a differenza di altre offerte (come le offerte HTML), perché sono offerte non visive. Gli sviluppatori devono scrivere il codice per ottenere l’offerta in modo esplicito utilizzando [getOffer()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffer/).

## Creare un’offerta JSON {#section_BB9C72D59DEA4EFB97A906AE7569AD7A}

1. Fai clic su **[!UICONTROL Offerte]** > **[!UICONTROL Offerte di codice]**.

   ![Offerte > scheda Offerte codice](/help/main/c-experiences/c-manage-content/assets/code-offers-tab.png)

1. Fai clic su **[!UICONTROL Crea]** > **[!UICONTROL Offerta JSON]**.

   ![](assets/offer-json.png)

1. Digita un nome per l’offerta.
1. Digita o incolla il codice JSON nella casella **[!UICONTROL Codice]**.
1. Fai clic su **[!UICONTROL Salva]**.

## Esempio JSON {#section_A54F7BB2B55D4B7ABCD5002E0C72D8C9}

Le offerte JSON sono supportate solo nelle attività create utilizzando [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md). Attualmente le offerte JSON possono essere utilizzate solo tramite chiamate API dirette.

Di seguito è riportato un esempio:

```json
adobe.target.getOffer({ 
  mbox: "some-mbox", 
  success: function(actions) { 
    console.log('Success', actions); 
  }, 
  error: function(status, error) { 
    console.log('Error', status, error); 
  } 
});
```

Le azioni passate al callback di successo sono una matrice di oggetti. Supponiamo di avere una singola offerta JSON, con il seguente contenuto:

```json
{ 
  "demo": {"a": 1, "b": 2} 
}
```

La matrice di azioni avrà questa struttura:

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

Per estrarre l’offerta JSON, è necessario eseguire iterazioni attraverso le azioni e trovare l’azione con `setJson` e quindi eseguire iterazioni attraverso la matrice del contenuto.

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
      "excepteur", 
    ], 
    "friends": [ 
      { 
        "id": 0, 
        "name": "Carla Lyons" 
      }, 
      { 
        "id": 1, 
        "name": "Ollie Mooney" 
      }, 
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

## Filtraggio delle offerte per tipo di offerta JSON {#section_52533555BCE6420C8A95EB4EB8907BDE}

Puoi filtrare il [!UICONTROL Offerte] libreria in base al tipo di offerta JSON, facendo clic sul pulsante **[!UICONTROL Tipo]** elenco a discesa, quindi selezionando la **[!UICONTROL JSON]** casella di controllo.

![](assets/offer-json-filter.png)
