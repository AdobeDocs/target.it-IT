---
description: mbox 3 rdpartyid è l'ID visitatore della tua società, ad esempio l'ID di iscrizione per il programma fedeltà della tua azienda.
keywords: mbox; mbox 3 rdpartyid; sincronizzazione profilo; sincronizzazione profilo; PCID
seo-description: 'Informazioni sul profilo in tempo reale '
seo-title: Sincronizzazione profilo in tempo reale per mbox 3 rdpartyid in Adobe Target
solution: Target
title: Sincronizzazione profilo in tempo reale per mbox 3 rdpartyid
topic: Standard
uuid: a88353d1-36e8-48b2-9b5e-71ed437c5b99
translation-type: tm+mt
source-git-commit: f54dba622e449fb8dac44cb37ff711419f8eda4b

---


# Real-time profile syncing for mbox3rdPartyId{#real-time-profile-syncing-for-mbox-rdpartyid}

mbox 3 rdpartyid è l'ID visitatore della tua società, ad esempio l'ID di iscrizione per il programma fedeltà della tua azienda.

Quando si accede al sito di una società, l’azienda generalmente crea un ID associato all’account del visitatore, alla carta fedeltà, al numero di iscrizione o ad altri identificatori validi per tale società.

When a visitor accesses a page on which [!DNL Target] is enabled, that visitor is assigned a [!DNL Target] PCID. If the visitor then logs in, and the implementation passes the mbox3rdPartyId to [!DNL Target], [!DNL Target] connects that visitor's mbox3rdPartyId with the [!DNL Target] PCID.

A intervalli regolari (da tre a cinque minuti), gli aggiornamenti vengono sincronizzati con il database. Quando il visitatore viene disconnesso, i dati uniti sostituiscono i dati precedenti associati alla mbox 3 rdpartyid, creando un record più completo delle azioni del visitatore. Se lo stesso attributo esiste in entrambi gli ID—ad esempio, il PCID dispone di categoria = hats e mbox 3 rdpartyid ha categoria = skis, oppure se il visitatore ha visto l'esperienza A prima di effettuare l'accesso, ma l'esperienza B è memorizzata nella mbox 3 rdpartyid—l'attributo memorizzato nella mbox 3 rdpartyid sovrascrive l'attributo dal PCID. Se il visitatore si trovava in un'attività o in un'esperienza prima di effettuare l'accesso, ma un'attività e un'esperienza diverse sono memorizzate nella mbox 3 rdpartyid, dopo l'accesso in quel visitatore viene inserita nell'attività e nell'esperienza mbox 3 rdpartyid.

| PCID (non connesso) | mbox 3 rdpartyid (accesso effettuato) | Unito e salvato in mbox 3 rdpartyid |
|---|---|---|
| category=hats | category=skis | category=skis |
|  | store=94103 | store=94103 |
| Attività 1, Esperienza A | Attività 1, Esperienza B | Attività 1, Esperienza B |
| Attività 1 |  | Attività 1 |

Quando il visitatore si disconnette, il profilo unito viene mantenuto.

>[!NOTE]
>
>[!DNL Adobe Analytics] gli obiettivi non vengono tracciati nei casi in cui l' [!DNL Adobe Experience Cloud] ID (MID) cambia (ad esempio, il visitatore cambia dispositivo), anche se [!DNL Target] il profilo potrebbe essere unito in base a mbox 3 rdpartyid e con informazioni sull'attività. Per i visitatori identificati con lo stesso MID (che accedono alla pagina con lo stesso dispositivo), [!DNL Analytics for Target] (A4T) funziona come previsto.

## Considerazioni {#considerations}

Se la pagina contiene diverse mbox e solo alcune di esse utilizzate 3 rdpartyid, Target non ha un profilo/contesto visitatore separato per ogni richiesta visitatore. Il contesto 3 rdpartyid ha priorità rispetto al contesto PCID. È sufficiente per passare 3 rdpartyid perché il suo contesto abbia priorità rispetto al PCID.

Ad esempio, se un visitatore accede a una pagina prima di accedere e visualizzare un'esperienza. La mbox globale non utilizza 3 rdpartyid. Dopo l'accesso, il visitatore visualizza una delle tre esperienze con mbox secondarie, alcune delle quali usano 3 rdpartyid. Il visitatore visita diverse pagine sul sito, quindi utilizza il pulsante Indietro per tornare alla pagina principale a cui accede prima di accedere e visualizzare un'esperienza diversa. In questo scenario, la mbox globale non passa 3 rdpartyid, ma una o più mbox secondarie hanno fatto. 3 Rdpartyid ha avuto priorità rispetto al PCID.
