---
description: L’ID mbox3rdPartyID è l’ID visitatore della tua azienda, ad esempio l’D di registrazione al programma fedeltà.
keywords: mbox;mbox3rdPartyID;sincronizzazione profilo;sincronizzare profilo
seo-description: L’ID mbox3rdPartyID è l’ID visitatore della tua azienda, ad esempio l’D di registrazione al programma fedeltà.
seo-title: Sincronizzazione dei profili in tempo reale per mbox3rdPartyID
solution: Target
title: Sincronizzazione dei profili in tempo reale per mbox3rdPartyID
topic: Standard
uuid: a88353d1-36e8-48b2-9b5e-71ed437c5b99
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

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
>Gli obiettivi [!DNL Adobe Analytics] non vengono tracciati nei casi in cui l’ID [!DNL Adobe Experience Cloud] (MID) cambia (ad esempio, il visitatore cambia dispositivo), anche se il profilo [!DNL Target] potrebbe essere unito in base al valore mbox3rdPartyID e contiene ancora informazioni sull’attività. Per i visitatori identificati con lo stesso MID (che accedono alla pagina con lo stesso dispositivo), [!DNL Analytics for Target] (A4T) funziona come previsto.
