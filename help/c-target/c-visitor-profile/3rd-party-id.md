---
description: L’ID mbox3rdPartyID è l’ID visitatore della tua azienda, ad esempio l’D di registrazione al programma fedeltà.
keywords: mbox;mbox3rdPartyID;sincronizzazione profilo;sincronizzare profilo; PCID
seo-description: 'Informazioni sul profilo in tempo reale '
seo-title: Sincronizzazione profilo in tempo reale per mbox 3 rdpartyid in Adobe Target
solution: Target
title: Sincronizzazione dei profili in tempo reale per mbox3rdPartyID
topic: Standard
uuid: a88353d1-36e8-48b2-9b5e-71ed437c5b99
translation-type: tm+mt
source-git-commit: 647776170531230a0d0f0aa3d97565fbb75bc963

---


# Sincronizzazione dei profili in tempo reale per mbox3rdPartyID{#real-time-profile-syncing-for-mbox-rdpartyid}

L’ID mbox3rdPartyID è l’ID visitatore della tua azienda, ad esempio l’D di registrazione al programma fedeltà.

Quando si accede al sito di una società, l’azienda generalmente crea un ID associato all’account del visitatore, alla carta fedeltà, al numero di iscrizione o ad altri identificatori validi per tale società.

When a visitor accesses a page on which [!DNL Target] is enabled, that visitor is assigned a [!DNL Target] PCID. If the visitor then logs in, and the implementation passes the mbox3rdPartyID to [!DNL Target], [!DNL Target] connects that visitor's mbox3rdPartyID with the [!DNL Target] PCID.

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

## Considerazioni {#considerations}

Se la pagina contiene diverse mbox e solo alcune di esse utilizzate 3 rdpartyid, Target non ha un profilo/contesto visitatore separato per ogni richiesta visitatore. Il contesto 3 rdpartyid ha priorità rispetto al contesto PCID. È sufficiente per passare 3 rdpartyid perché il suo contesto abbia priorità rispetto al PCID.

Ad esempio, se un visitatore accede a una pagina prima di accedere e visualizzare un'esperienza. La mbox globale non utilizza 3 rdpartyid. Dopo l'accesso, il visitatore visualizza una delle tre esperienze con mbox secondarie, alcune delle quali usano 3 rdpartyid. Il visitatore visita diverse pagine sul sito, quindi utilizza il pulsante Indietro per tornare alla pagina principale a cui accede prima di accedere e visualizzare un'esperienza diversa. In questo scenario, la mbox globale non passa 3 rdpartyid, ma una o più mbox secondarie hanno fatto. 3 Rdpartyid ha avuto priorità rispetto al PCID.
