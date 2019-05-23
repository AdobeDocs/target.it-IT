---
description: L’ID mbox3rdPartyID è l’ID visitatore della tua azienda, ad esempio l’D di registrazione al programma fedeltà.
keywords: mbox;mbox3rdPartyID;sincronizzazione profilo;sincronizzare profilo
seo-description: L’ID mbox3rdPartyID è l’ID visitatore della tua azienda, ad esempio l’D di registrazione al programma fedeltà.
seo-title: Sincronizzazione dei profili in tempo reale per mbox3rdPartyID
solution: Target
title: Sincronizzazione dei profili in tempo reale per mbox3rdPartyID
topic: Standard
uuid: a88353d1-36e8-48b2-9b5e-71ed437c5b99
translation-type: tm+mt
source-git-commit: 17f0612559bae335d261ebc7654bc5d7fe3c0d12

---


# Sincronizzazione dei profili in tempo reale per mbox3rdPartyID{#real-time-profile-syncing-for-mbox-rdpartyid}

L’ID mbox3rdPartyID è l’ID visitatore della tua azienda, ad esempio l’D di registrazione al programma fedeltà.

Quando si accede al sito di una società, l’azienda generalmente crea un ID associato all’account del visitatore, alla carta fedeltà, al numero di iscrizione o ad altri identificatori validi per tale società.

Quando un visitatore accede a una pagina sulla quale è abilitato Target, a tale visitatore viene assegnato un PCID di Target. Se il visitatore effettua l’accesso e l’implementazione passa il codice mbox3rdPartyID a Target, Target collegata l’ID ’mbox3rdPartyID del visitatore con il PCID di Target.

A intervalli regolari (da tre a cinque minuti), gli aggiornamenti vengono sincronizzati con il database. Quando il visitatore si disconnette, i dati uniti sostituiscono quelli precedenti associati all’ID mbox3rdPartyID, creando un record più completo delle azioni del visitatore. Se lo stesso attributo esiste in entrambi gli ID (per esempio, il PCID ha category=hats e il mbox3rdPartyID ha category=skis, oppure se il visitatore ha visualizzato l’esperienza A prima di effettuare l’accesso, ma l’esperienza B è memorizzata in mbox3rdPartyID) l’attributo memorizzato in mbox3rdPartyID sovrascrive l’attributo proveniente da PCID. Se il visitatore si trovava in un’attività o esperienza prima di effettuare l’accesso, ma l’attività e l’esperienza memorizzate in mbox3rdPartyID risultano diverse, dopo l’accesso tale visitatore viene inserito nell’attività ed esperienza di mbox3rdPartyID.

| PCID (non connesso) | mbox3rdPartyID (connesso) | Uniti e salvati in mbox3rdPartyID |
|---|---|---|
| category=hats | category=skis | category=skis |
|  | store=94103 | store=94103 |
| Attività 1, Esperienza A | Attività 1, Esperienza B | Attività 1, Esperienza B |
| Attività 1 |  | Attività 1 |

Quando il visitatore si disconnette, il profilo unito viene mantenuto.

>[!NOTE]
>
>[!DNL Adobe Analytics] gli obiettivi non vengono tracciati nei casi in cui l&#39; [!DNL Adobe Experience Cloud] ID (MID) cambia (ad esempio, il visitatore cambia dispositivo), anche se [!DNL Target] il profilo potrebbe essere unito in base a mbox 3 rdpartyid e con informazioni sull&#39;attività. Per i visitatori identificati con lo stesso MID (quelli che accedono alla pagina con lo stesso dispositivo), [!DNL Analytics for Target] (A 4 T) funziona come previsto.
