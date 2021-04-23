---
keywords: mbox;mbox3rdPartyId;sincronizzazione profilo;sincronizzare profilo;PCID
description: Scopri come utilizzare mbox3rdPartyId, ID visitatore dell’organizzazione, ad esempio l’ID di iscrizione o il programma fedeltà dell’organizzazione.
title: Come si utilizza la sincronizzazione dei profili in tempo reale per mbox3rdPartyId?
feature: Tipi di pubblico
exl-id: ed409225-fa35-49da-87d1-1770221f2ae0
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 76%

---

# Sincronizzazione dei profili in tempo reale per mbox3rdPartyId

L’ID mbox3rdPartyId l’ID visitatore della tua azienda, ad esempio l’D di registrazione al programma fedeltà.

Quando si accede al sito di una società, l’azienda generalmente crea un ID associato all’account del visitatore, alla carta fedeltà, al numero di iscrizione o ad altri identificatori validi per tale società.

Quando un visitatore accede a una pagina sulla quale è abilitato [!DNL Target], a tale visitatore viene assegnato un PCID di [!DNL Target]. Se il visitatore effettua l’accesso e l’implementazione passa il codice mbox3rdPartyId a [!DNL Target], [!DNL Target] collegata l’ID mbox3rdPartyId del visitatore con il PCID di [!DNL Target].

A intervalli regolari (da tre a cinque minuti), gli aggiornamenti vengono sincronizzati con il database. Quando il visitatore si disconnette, i dati uniti sostituiscono quelli precedenti associati all’ID mbox3rdPartyId, creando un record più completo delle azioni del visitatore. Se lo stesso attributo esiste in entrambi gli ID (per esempio, l’ID PCID ha category=hats e l’ID mbox3rdPartyId ha category=skis, oppure se il visitatore ha visualizzato l’esperienza A prima di effettuare l’accesso, ma l’esperienza B è memorizzata in mbox3rdPartyId) l’attributo memorizzato nell’ID mbox3rdPartyId sovrascrive quello proveniente da PCID. Se il visitatore si trovava in un’attività o esperienza prima di effettuare l’accesso, ma l’attività e l’esperienza memorizzate in mbox3rdPartyId risultano diverse, dopo l’accesso tale visitatore viene inserito nell’attività ed esperienza di mbox3rdPartyId.

| PCID (non connesso) | mbox3rdPartyId (connesso) | Uniti e salvati in mbox3rdPartyId  |
|---|---|---|
| category=hats | category=skis | category=skis |
|  | store=94103 | store=94103 |
| Attività 1, Esperienza A | Attività 1, Esperienza B | Attività 1, Esperienza B |
| Attività 1 |  | Attività 1 |

Quando il visitatore si disconnette, il profilo unito viene mantenuto.

>[!NOTE]
>
>Per distinguere tra utenti autenticati (connessi) e utenti non autenticati, utilizza il servizio Adobe Experience Cloud Identity (ECID) invece di mbox3rdPartyID. Dopo che un utente è associato a mbox3rdPartyID, rimane associato all’utente anche dopo la disconnessione.

>[!NOTE]
>
>[!DNL Adobe Analytics] Gli obiettivi non vengono tracciati nei casi in cui l’ [!DNL Adobe Experience Cloud] ID (EDID) cambia (ad esempio, il visitatore cambia dispositivo), anche se il  [!DNL Target] profilo potrebbe essere unito in base al valore mbox3rdPartyId e contiene ancora informazioni sull’attività. Per i visitatori identificati con lo stesso EDID (che accedono alla pagina con lo stesso dispositivo), [!DNL Analytics for Target] (A4T) funziona come previsto.

## Considerazioni {#considerations}

Se la pagina contiene più mbox e solo alcune di esse utilizzano 3rdPartyID, Target non ha un profilo/contesto visitatore separato per ogni richiesta visitatore. Il contesto 3rdPartyID ha priorità rispetto al contesto PCID. È sufficiente che una mbox passi un 3rdPartyID affinché il suo contesto abbia priorità rispetto al PCID.

Ad esempio, se un visitatore accede a una pagina prima di accedere e visualizza un’esperienza, la mbox globale non utilizza 3rdPartyID. Dopo che avrà eseguito l’accesso, il visitatore visualizza una di tre esperienze con mbox secondarie, alcune delle quali usano 3rdPartyID. Il visitatore visita diverse pagine sul sito, quindi utilizza il pulsante Indietro per tornare alla pagina principale che aveva visitato prima di eseguire l’accesso, e visualizza un’esperienza diversa. In questo scenario, la mbox globale non passa 3rdPartyID, che era invece stato passato da una o più delle mbox secondarie. 3rdPartyID ha quindi precedenza rispetto a PCID.
