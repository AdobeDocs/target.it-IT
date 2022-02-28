---
keywords: mbox;mbox3rdPartyId;sincronizzazione profilo;sincronizzare profilo;PCID
description: Scopri come utilizzare mbox3rdPartyId, che corrisponde all’ID visitatore dell’organizzazione, ad esempio l’ID di iscrizione o del programma fedeltà.
title: Come si utilizza la sincronizzazione dei profili in tempo reale per mbox3rdPartyId?
feature: Audiences
exl-id: ed409225-fa35-49da-87d1-1770221f2ae0
source-git-commit: 8969b3b04b8f02a4ae9860bafe4b0a1c80a6f35e
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 84%

---

# Sincronizzazione dei profili in tempo reale per mbox3rdPartyId

`mbox3rdPartyId` in [!DNL Adobe Target] è l’ID visitatore della tua azienda, ad esempio l’D di iscrizione al programma fedeltà.

Quando si accede al sito di una società, l’azienda generalmente crea un ID associato all’account del visitatore, alla carta fedeltà, al numero di iscrizione o ad altri identificatori validi per tale società.

Quando un visitatore accede a una pagina sulla quale è abilitato [!DNL Target], a tale visitatore viene assegnato un PCID di [!DNL Target]. Se il visitatore effettua l’accesso e l’implementazione passa il valore `mbox3rdPartyId` a [!DNL Target], [!DNL Target] collega il valore `mbox3rdPartyId` del visitatore al PCID di [!DNL Target].

A intervalli regolari (da tre a cinque minuti), gli aggiornamenti vengono sincronizzati con il database. Quando il visitatore si disconnette, i dati uniti sostituiscono quelli precedenti associati al valore `mbox3rdPartyId`, creando un record più completo delle azioni del visitatore. Se lo stesso attributo esiste in entrambi gli ID (per esempio, il PCID ha category=hats e `mbox3rdPartyId` ha category=skis, oppure se il visitatore ha visualizzato l’esperienza A prima di effettuare l’accesso, ma l’esperienza B è memorizzata in `mbox3rdPartyId`) l’attributo memorizzato in `mbox3rdPartyId` sovrascrive quello proveniente da PCID. Se il visitatore si trovava in un’attività o esperienza prima di effettuare l’accesso, ma l’attività e l’esperienza memorizzate in `mbox3rdPartyId` risultano diverse, dopo l’accesso tale visitatore viene inserito nell’attività ed esperienza di `mbox3rdPartyId`.

| PCID (non connesso) | mbox3rdPartyId (connesso) | Uniti e salvati in mbox3rdPartyId  |
|---|---|---|
| category=hats | category=skis | category=skis |
|  | store=94103 | store=94103 |
| Attività 1, Esperienza A | Attività 1, Esperienza B | Attività 1, Esperienza B |
| Attività 1 |  | Attività 1 |

Quando il visitatore si disconnette, il profilo unito viene mantenuto.

>[!NOTE]
>
>Per distinguere tra utenti autenticati (connessi) e utenti non autenticati, utilizza il servizio [!DNL Adobe Experience Cloud Identity Service] (ECID) invece di mbox3rdPartyID. Dopo che un utente è associato a mbox3rdPartyID, questo rimane associato all’utente anche dopo la disconnessione.

>[!NOTE]
>
>[!DNL Adobe Analytics] gli obiettivi non vengono tracciati nei casi in cui la [!DNL Adobe Experience Cloud] L’ID (ECID) cambia (ad esempio, il visitatore cambia dispositivo), anche se il [!DNL Target] potrebbe essere unito in base al valore mbox3rdPartyId e contiene ancora informazioni sull’attività. Per i visitatori identificati con lo stesso ECID (coloro che accedono alla pagina con lo stesso dispositivo), [!DNL Analytics for Target] (A4T) funziona come previsto.

## Considerazioni {#considerations}

* Se la pagina contiene più mbox e solo alcune di esse utilizzano `3rdPartyID`, [!DNL Target] non ha un profilo/contesto visitatore separato per ogni richiesta visitatore. Il contesto `3rdPartyID` ha priorità rispetto al contesto PCID. È sufficiente che una mbox passi un `3rdPartyId` affinché il suo contesto abbia priorità rispetto al PCID.

   Ad esempio, se un visitatore visita una pagina prima di aver eseguito l’accesso e visualizza un’esperienza, la mbox globale non utilizza `3rdPartyID`. Dopo che avrà eseguito l’accesso, il visitatore visualizza una di tre esperienze con mbox secondarie, alcune delle quali usano `3rdPartyID`. Il visitatore visita diverse pagine sul sito, quindi utilizza il pulsante Indietro per tornare alla pagina principale che aveva visitato prima di eseguire l’accesso, e visualizza un’esperienza diversa. In questo scenario, la mbox globale non passa `3rdPartyID`, che era invece stato passato da una o più delle mbox secondarie. `3rdPartyID` ha quindi precedenza rispetto a PCID.

* Puoi inviare gli ID cliente dei visitatori a [!DNL Target] utilizzando due approcci:

   1. Usa la `mbox3rdPartyId`/`thirdPartyId`.

      * `mbox3rdPartyId` è il nome del parametro quando utilizzi `targetPageParams` o `targetPageParamsAll`
      * `thirdPartyId` è il nome del parametro impostato direttamente nel payload dell’API di consegna.
      * Puoi inviare un solo valore in questo parametro.
   1. Utilizza la funzione `setCustomerId`/`customerIds` del servizio ECID.

      * `setCustomerId` è una funzione che puoi utilizzare sulle implementazioni lato client (browser) quando VisitorAPI.js è disponibile sulla pagina.
      * `customerIds` è il nome del parametro utilizzato quando lo si imposta direttamente nel payload dell’API di consegna e in genere viene eseguito su implementazioni lato server o IoT (Internet of Things).
      * A differenza di `mbox3rdPartyId`/`thirdPartyId`, in questo approccio è possibile inviare più ID come elenco, ma poiché [!DNL Target] supporta solo un singolo ID cliente per ogni ID TnT, utilizza il primo ID nell’elenco con un alias noto (alias configurato nell’interfaccia di Attributi del cliente).

   È possibile utilizzare `mbox3rdPartyId`/`thirdPartyId` if [!DNL Target] è la tua unica [!DNL Adobe Experience Cloud] e non desideri utilizzare Attributi del cliente. Per tutti gli altri casi, si consiglia di utilizzare `setCustomerId`/`customerIds` per l’invio degli ID cliente.

   >[!IMPORTANT]
   >
   > Utilizzando entrambi gli approcci menzionati qui sopra in modo intercambiabile per un singolo visitatore, è possibile che si verifichino unioni di profili [!DNL Target] non autenticati e autenticati.
   >
   >Adobe consiglia di non utilizzare insieme `mbox3rdPartyId`/`thirdPartyId` e `setCustomerID`/`customerIds`.
   >
   >Se devi utilizzare entrambi gli approcci in modo intercambiabile, assicurati che il primo ID nell’elenco utilizzato da `setCustomerID`/`customerIds` è utilizzato da `thirdPartyId`/`mbox3rdPartyId` e viceversa.

