---
keywords: mbox;mbox3rdPartyId;profile syncing;profile synch;PCID
description: 'Informazioni sul profilo in tempo reale '
title: Sincronizzazione dei profili in tempo reale per mbox3rdPartyId in Adobe Target
feature: visitor profiles
topic: Standard
uuid: a88353d1-36e8-48b2-9b5e-71ed437c5b99
translation-type: tm+mt
source-git-commit: b2f80c89ecceb6f88a176db7a90e71a162a24641
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 81%

---


# Sincronizzazione dei profili in tempo reale per mbox3rdPartyId{#real-time-profile-syncing-for-mbox-rdpartyid}

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
>Se desiderate distinguere tra utenti autenticati (connessi) e utenti non autenticati, utilizzate il servizio Adobe Experience Cloud Identity Service (ECID) invece di mbox3rdPartyID. Dopo che un utente è associato a mbox3rdPartyID, rimane associato all&#39;utente anche dopo la disconnessione.

>[!NOTE]
>
>[!DNL Adobe Analytics] gli obiettivi non verranno tracciati nei casi in cui l&#39; [!DNL Adobe Experience Cloud] ID (EDID) cambia (ad esempio, il visitatore modifica i dispositivi), anche se il [!DNL Target] profilo potrebbe essere unito in base a mbox3rdPartyId e ancora dispone di informazioni sull&#39;attività. For visitors identified with the same EDID (those who access the page with the same device), [!DNL Analytics for Target] (A4T) should work as expected.

## Considerazioni {#considerations}

Se la pagina contiene più mbox e solo alcune di esse utilizzano 3rdPartyID, Target non ha un profilo/contesto visitatore separato per ogni richiesta visitatore. Il contesto 3rdPartyID ha priorità rispetto al contesto PCID. È sufficiente che una mbox passi un 3rdPartyID affinché il suo contesto abbia priorità rispetto al PCID.

Ad esempio, se un visitatore accede a una pagina prima di accedere e visualizza un’esperienza, la mbox globale non utilizza 3rdPartyID. Dopo che avrà eseguito l’accesso, il visitatore visualizza una di tre esperienze con mbox secondarie, alcune delle quali usano 3rdPartyID. Il visitatore visita diverse pagine sul sito, quindi utilizza il pulsante Indietro per tornare alla pagina principale che aveva visitato prima di eseguire l’accesso, e visualizza un’esperienza diversa. In questo scenario, la mbox globale non passa 3rdPartyID, che era invece stato passato da una o più delle mbox secondarie. 3rdPartyID ha quindi precedenza rispetto a PCID.
