---
description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per le versioni più recenti o imminenti di Adobe Target.
keywords: note sulla versione;rilasci;aggiornamenti;release futura;miglioramenti;nuove funzioni;correzioni
seo-description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per le versioni DNL Adobe Target più recenti o imminenti.
seo-title: Note sulla versione prerelease di Adobe Target
solution: Target
title: Note sulla versione di Target (prerelease)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 285a09503ba6abaf2bfe19fc2b214c32ebd2de3a

---


# Note sulla versione di Target (prerelease){#target-release-notes-prerelease}

Queste note sulla versione contengono informazioni su funzioni, miglioramenti e correzioni per le versioni più recenti o in arrivo di [!DNL Adobe Target].

**Ultimo aggiornamento: 2 ottobre 2019**

>[!NOTE]
>
>Queste note sulla versione contengono delle informazioni sulla versione prerelease. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso. Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali o possono essere diverse, a seconda della tempistica delle release.
>
>I codici tra parentesi sono per uso interno di [!DNL Adobe].

## Piattaforma di destinazione (date da determinare)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Node.js SDK versione 1.0 | L’SDK Node.js di Target consente di distribuire Target lato server.<br>Questo SDK Node.js consente di integrare facilmente Target con altre soluzioni Experience Cloud, come Adobe Experience Cloud Identity Service, Adobe Analytics e Adobe Audience Manager.<br>L’SDK Node.js introduce procedure ottimali e rimuove le complessità durante l’integrazione con Adobe Target tramite la nostra API di distribuzione, in modo che i team tecnici possano concentrarsi sulla logica aziendale. Di seguito sono riportate alcune importanti funzioni introdotte nell’ultima versione:<ul><li>Supporto per preacquisizione e notifiche che consentono di ottimizzare le prestazioni tramite caching.</li><li>Supporto per l'ottimizzazione delle prestazioni in caso di integrazione ibrida di Target sia sulle pagine Web che sul lato server. We are introducing a setting called `serverState` that will be populated by experiences retrieved via the server-side so that at.js 2.2 will no longer make an additional server call to retrieve the experiences. This approach optimizes page load performance.</li><li> Support for retrieving VEC-created activities via the Node.js SDK, which is made possible by the new Delivery API.</li><li>Open sourced so your developers can contribute to the Node.js SDK.</li></ul> |
| Delivery API | An entirely new delivery API endpoint (/v1/delivery) will be available in production. Notable features are:<ul><li>One endpoint to retrieve experiences for one or more mboxes.</li><li>Retrieve VEC-created activities via the API.</li><li>Support for an entirely new object called Views that is used for Single Page Applications (SPAs) and Mobile applications.</li></ul> |
| at.js version 2.2andat.js version 1.8<br><br> | These versions of at.js provide:<ul><li>Improved performance when using both Experience Cloud ID Service (ECID) v4.4 and at.js 2.2 or at.js 1.8 on your web pages.</li><li>In precedenza, l'ECID effettuava due chiamate di blocco prima che at.js potesse recuperare le esperienze. È stato ridotto a una singola chiamata, il che migliora notevolmente le prestazioni.</li></ul> Per trarre vantaggio da questi miglioramenti in termini di prestazioni, effettua l’aggiornamento a at.js 2.2 o at.js 1.8 insieme alla libreria ECID v4.4. |


## Target Standard/Premium 19.10.1 (22 ottobre 2019)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| ![Premium badge](/help/assets/premium.png) - Raccomandazioni basate sull'utente | Recommends items based off of each visitor's browsing, viewing, and purchasing history. Tali elementi sono generalmente denominati "Consigliati per l'utente."<br>Questo criterio consente di fornire contenuti ed esperienze personalizzati sia ai visitatori nuovi che di ritorno. L'elenco delle raccomandazioni è ponderato per l'attività più recente del visitatore, viene aggiornato in sessione e diventa più personalizzato man mano che il visitatore naviga nel sito. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
