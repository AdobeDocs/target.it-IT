---
keywords: offerta remota;creazione di offerta remota
description: Scopri come creare offerte JSON in Adobe [!DNL Target] da utilizzare nel Compositore esperienza basato su moduli.
title: Come si creano le offerte JSON?
feature: Experiences and Offers
exl-id: 793665a4-4cd6-458f-8225-ba23e503a115
source-git-commit: 7c15a0795e94b6c6317cb5b4018899be71f03a40
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 28%

---

# Creare offerte JSON

Creare offerte JSON in [!UICONTROL Libreria di offerte] in [!DNL Adobe Target] per l&#39;utilizzo in [!UICONTROL Compositore esperienza basato su moduli].

Le offerte JSON possono essere utilizzate in attività basate su moduli per casi di utilizzo in cui [!DNL Target] È necessario prendere decisioni per inviare un’offerta in formato JSON da utilizzare nel framework SPA o nelle integrazioni lato server.

## Considerazioni JSON

Quando lavori con le offerte JSON, considera quanto segue:

* Le offerte JSON sono attualmente disponibili solo per [!UICONTROL Test A/B], Automated Personalization (AP) e [!UICONTROL Targeting esperienza] (XT) attività.
* Le offerte JSON possono essere utilizzate in [attività basate su moduli](/help/main/c-experiences/form-experience-composer.md) solo.
* L&#39;offerta JSON può essere recuperata direttamente quando utilizzi il [API lato server e SDK Node.js per dispositivi mobili, Java, .NET e Python](https://experienceleague.corp.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html){target=_blank}.
* Nel browser, le offerte JSON possono essere recuperate SOLO tramite at.js 1.2.3 (o versione successiva) e utilizzando [getOffer()](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffer.html){target=_blank} filtrando le azioni tramite `setJson` azione.
* Le offerte JSON vengono consegnate come oggetti JSON nativi anziché come stringhe. I consumatori di questi oggetti non devono più gestire gli oggetti come stringhe e convertirli in oggetti JSON.
* Le offerte JSON non vengono applicate automaticamente, a differenza di altre offerte (come le offerte HTML), perché sono offerte non visive. Gli sviluppatori devono scrivere il codice per ottenere l’offerta in modo esplicito utilizzando [getOffer()](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffer.html){target=_blank}.

## Creare un’offerta JSON {#section_BB9C72D59DEA4EFB97A906AE7569AD7A}

1. Clic **[!UICONTROL Offerte]** > **[!UICONTROL Offerte di codice]**.

   ![Offerte > scheda Offerte di codice](/help/main/c-experiences/c-manage-content/assets/code-offers-tab.png)

1. Fai clic su **[!UICONTROL Crea]** > **[!UICONTROL Offerta JSON]**.

   ![immagine offer-json](assets/offer-json.png)

1. Digita un nome per l’offerta.
1. Digita o incolla il codice JSON nella casella **[!UICONTROL Codice]**.
1. Fai clic su **[!UICONTROL Salva]**.

## Esempio JSON {#section_A54F7BB2B55D4B7ABCD5002E0C72D8C9}

Le offerte JSON sono supportate solo nelle attività create utilizzando [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md). Attualmente l’unico modo per poter utilizzare le offerte JSON è tramite chiamate dirette API/SDK.

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

Per estrarre l’offerta JSON, è necessario eseguire iterazioni attraverso le azioni e trovare l’azione con `setJson` e quindi scorrere l&#39;array di contenuto.

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

## Esempio di offerta JSON con attributi di profilo Real-time CDP

Gli attributi del profilo Real-time CDP possono essere condivisi con [!DNL Target] da utilizzare nelle offerte HTML e JSON. Questa funzione è attualmente in versione beta.

Caso d’uso di esempio: in qualità di esperto di marketing online, Grace desidera che il profilo AEP/unificato condivida i valori degli attributi con [!DNL Target] per fornire una personalizzazione in tempo reale. Utilizzando Real-time CDP Profile Attributes (Attributi del profilo di Real-time CDP), Grace può visualizzare il valore dell’attributo AEP in una [!DNL Target] offerta tramite sostituzione token. Ad esempio, può personalizzare in base al colore preferito di un cliente utilizzando `${aep.profile.favoriteColor}`, o il loro livello di fedeltà e il valore del punto di fedeltà utilizzando i token `${aep.loyalty.tier}` e `${aep.loyalty.points}`.

![immagine offer-json-aep-shared-attribute](assets/offer-json-aep-shared-attribute.png)

L’assegnazione di valori predefiniti è facoltativa.

## Filtraggio delle offerte per tipo di offerta JSON {#section_52533555BCE6420C8A95EB4EB8907BDE}

Puoi filtrare i [!UICONTROL Offerte] libreria in base al tipo di offerta JSON, facendo clic sul pulsante **[!UICONTROL Tipo]** , quindi selezionando il pulsante **[!UICONTROL JSON]** casella di controllo.

![immagine offer-json-filter](assets/offer-json-filter.png)
