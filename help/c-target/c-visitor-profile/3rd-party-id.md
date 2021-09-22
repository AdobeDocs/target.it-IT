---
keywords: mbox;mbox3rdPartyId;sincronizzazione profilo;sincronizzare profilo;PCID
description: Scopri come utilizzare mbox3rdPartyId, ID visitatore dell’organizzazione, ad esempio l’ID di iscrizione o il programma fedeltà dell’organizzazione.
title: Come si utilizza la sincronizzazione dei profili in tempo reale per mbox3rdPartyId?
feature: Audiences
exl-id: ed409225-fa35-49da-87d1-1770221f2ae0
source-git-commit: f4b490c489427130e78d84b573b2d290a8a60585
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 24%

---

# Sincronizzazione dei profili in tempo reale per mbox3rdPartyId

Il `mbox3rdPartyId` in [!DNL Adobe Target] è l’ID visitatore della tua azienda, ad esempio l’ID di iscrizione al programma fedeltà.

Quando si accede al sito di una società, l’azienda generalmente crea un ID associato all’account del visitatore, alla carta fedeltà, al numero di iscrizione o ad altri identificatori validi per tale società.

Quando un visitatore accede a una pagina sulla quale è abilitato [!DNL Target], a tale visitatore viene assegnato un PCID di [!DNL Target]. Se il visitatore effettua l’accesso e l’implementazione passa il `mbox3rdPartyId` a [!DNL Target], [!DNL Target] connette il `mbox3rdPartyId` del visitatore con il PCID [!DNL Target].

A intervalli regolari (da tre a cinque minuti), gli aggiornamenti vengono sincronizzati con il database. Quando il visitatore si disconnette, i dati uniti sostituiscono i dati precedenti associati al `mbox3rdPartyId`, creando un record completo delle azioni del visitatore. Se lo stesso attributo esiste in entrambi gli ID, ad esempio, il PCID ha category=hats e il `mbox3rdPartyId` ha category=skis, o se il visitatore ha visualizzato l&#39;esperienza A prima di effettuare l&#39;accesso, ma l&#39;esperienza B è memorizzata nel `mbox3rdPartyId`, l&#39;attributo memorizzato in `mbox3rdPartyId` sovrascrive l&#39;attributo dal PCID. Se il visitatore si trovava in un’attività o esperienza prima di effettuare l’accesso, ma una diversa attività ed esperienza viene memorizzata in `mbox3rdPartyId`, dopo l’accesso, tale visitatore viene inserito nell’ attività ed esperienza `mbox3rdPartyId`.

| PCID (non connesso) | mbox3rdPartyId (connesso) | Uniti e salvati in mbox3rdPartyId  |
|---|---|---|
| category=hats | category=skis | category=skis |
|  | store=94103 | store=94103 |
| Attività 1, Esperienza A | Attività 1, Esperienza B | Attività 1, Esperienza B |
| Attività 1 |  | Attività 1 |

Quando il visitatore si disconnette, il profilo unito viene mantenuto.

>[!NOTE]
>
>Per distinguere tra utenti autenticati (connessi) e utenti non autenticati, utilizza il [!DNL Adobe Experience Cloud Identity Service] (ECID) invece di mbox3rdPartyID. Dopo che un utente è associato a mbox3rdPartyID, rimane associato all’utente anche dopo la disconnessione.

>[!NOTE]
>
>[!DNL Adobe Analytics] Gli obiettivi non vengono tracciati nei casi in cui l’ [!DNL Adobe Experience Cloud] ID (EDID) cambia (ad esempio, il visitatore cambia dispositivo), anche se il  [!DNL Target] profilo potrebbe essere unito in base al valore mbox3rdPartyId e contiene ancora informazioni sull’attività. Per i visitatori identificati con lo stesso EDID (che accedono alla pagina con lo stesso dispositivo), [!DNL Analytics for Target] (A4T) funziona come previsto.

## Considerazioni {#considerations}

* Se la pagina contiene diverse mbox e solo alcuni utilizzi `3rdPartyID`, [!DNL Target] non dispone di un profilo/contesto visitatore separato per ogni richiesta di visitatore. Il contesto `3rdPartyID` ha priorità rispetto al contesto PCID. È sufficiente che una mbox passi `3rdPartyId` affinché il suo contesto abbia la priorità rispetto a PCID.

   Ad esempio, supponiamo che un visitatore acceda a una pagina prima di effettuare l&#39;accesso e veda un&#39;esperienza. la mbox globale non utilizza `3rdPartyID`. Dopo che avrà eseguito l’accesso, il visitatore visualizza una di tre esperienze con mbox secondarie, alcune delle quali usano `3rdPartyID`. Il visitatore visita diverse pagine sul sito, quindi utilizza il pulsante Indietro per tornare alla pagina principale che aveva visitato prima di eseguire l’accesso, e visualizza un’esperienza diversa. In questo scenario, la mbox globale non passava `3rdPartyID`, ma lo faceva una o più delle mbox secondarie. `3rdPartyID` ha precedenza rispetto a PCID.

* Puoi inviare gli ID cliente dei visitatori a [!DNL Target] utilizzando due approcci:

   1. Usa la `mbox3rdPartyId`/`thirdPartyId`.

      * `mbox3rdPartyId` è il nome del parametro quando utilizzi  `targetPageParams` o  `targetPageParamsAll`
      * `thirdPartyId` è il nome del parametro impostato direttamente nel payload dell’API di consegna.
      * Puoi inviare un solo valore in questo parametro.
   1. Utilizzare la funzione `setCustomerId`/`customerIds` del servizio ECID.

      * `setCustomerId` è una funzione che puoi utilizzare sulle implementazioni lato client (browser) quando VisitorAPI.js è disponibile sulla pagina.
      * `customerIds` è il nome del parametro utilizzato quando lo si imposta direttamente nel payload dell’API di consegna e in genere viene eseguito su implementazioni lato server o IOT (Internet of Things).
      * A differenza di `mbox3rdPartyId`/`thirdPartyId`, in questo approccio è possibile inviare più ID come elenco, ma poiché [!DNL Target] supporta solo un singolo ID cliente per ogni ID TnT, utilizza il primo ID nell’elenco con un alias noto (alias configurato nell’interfaccia utente Attributi del cliente).

   >[!IMPORTANT]
   >
   > Utilizzando entrambi gli approcci menzionati in precedenza in modo intercambiabile per un singolo visitatore, è possibile che si verifichino unioni di profili non autenticati e autenticati [!DNL Target].
   >
   >Adobe consiglia di non utilizzare insieme `mbox3rdPartyId`/`thirdPartyId` e `setCustomerID`/`customerIds`.
   >
   >Se devi utilizzare entrambi gli approcci in modo intercambiabile, assicurati che il primo ID nell’elenco utilizzato da `setCustomerID`/`customerIds` sia quello utilizzato da `thirdPartyId`/`mbox3rdPartyId` e viceversa.

