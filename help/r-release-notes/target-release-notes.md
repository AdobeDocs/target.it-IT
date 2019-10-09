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
source-git-commit: 9fa095b910b85f244b626c34cacdf9f4a13a6929

---


# Note sulla versione di Target (prerelease){#target-release-notes-prerelease}

Queste note sulla versione contengono informazioni su funzioni, miglioramenti e correzioni per le versioni più recenti o in arrivo di [!DNL Adobe Target].

**Ultimo aggiornamento: 2 ottobre 2019**

>[!NOTE]
>
>Queste note sulla versione contengono delle informazioni sulla versione prerelease. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso. Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali o possono essere diverse, a seconda della tempistica delle release.
>
>I codici tra parentesi sono per uso interno di [!DNL Adobe].

## Piattaforma Target

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Node.js SDK versione 1.0<br>(9 ottobre 2019) | L’SDK Node.js di Target consente di distribuire Target lato server.<br>Questo SDK Node.js consente di integrare facilmente Target con altre soluzioni Experience Cloud, come Adobe Experience Cloud Identity Service, Adobe Analytics e Adobe Audience Manager.<br>L’SDK Node.js introduce procedure ottimali e rimuove le complessità durante l’integrazione con Adobe Target tramite la nostra API di distribuzione, in modo che i team tecnici possano concentrarsi sulla logica aziendale. Di seguito sono riportate alcune importanti funzioni introdotte nell’ultima versione:<ul><li>Supporto per preacquisizione e notifiche che consentono di ottimizzare le prestazioni tramite caching.</li><li>Supporto per l'ottimizzazione delle prestazioni in caso di integrazione ibrida di Target sia sulle pagine Web che sul lato server. Stiamo introducendo un'impostazione denominata `serverState` che verrà compilata dalle esperienze recuperate tramite il lato server, in modo che at.js 2.2 non effettuerà più una chiamata server aggiuntiva per recuperare le esperienze. Questo approccio ottimizza le prestazioni di caricamento delle pagine.</li><li> Supporto per il recupero di attività create VEC tramite Node.js SDK, reso possibile dalla nuova API di consegna.</li><li>Apri in origine in modo che i tuoi sviluppatori possano contribuire all’SDK Node.js.</li></ul>Per ulteriori informazioni, vedi Note sulla [versione - SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md)Target Node.js. |
| API<br>di distribuzione (9 ottobre 2019) | In produzione sarà disponibile un endpoint API di distribuzione completamente nuovo (/v1/delivery). Le funzioni principali sono:<ul><li>Un endpoint per recuperare le esperienze per una o più mbox.</li><li>Recuperate le attività create VEC tramite l'API.</li><li>Supporto per un oggetto completamente nuovo, denominato Views (Visualizzazioni), utilizzato per le applicazioni SPA (Single Page Applications) e per le applicazioni mobili.</li></ul>Per ulteriori informazioni, consultate Note sulla [versione - API](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md)lato server di Target. |
| at.js versione 2.2<br><br>andat.js versione 1.8<br>(date da determinare) | Queste versioni di at.js forniscono:<ul><li>Sono state migliorate le prestazioni quando si utilizzano sia il servizio Experience Cloud ID (ECID) v4.4 che at.js 2.2 o at.js 1.8 sulle pagine Web.</li><li>In precedenza, l'ECID effettuava due chiamate di blocco prima che at.js potesse recuperare le esperienze. È stato ridotto a una singola chiamata, il che migliora notevolmente le prestazioni.</li></ul> Per trarre vantaggio da questi miglioramenti in termini di prestazioni, effettua l’aggiornamento a at.js 2.2 o at.js 1.8 insieme alla libreria ECID v4.4. |


## Target Standard/Premium 19.10.1 (22 ottobre 2019)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| ![Premium badge](/help/assets/premium.png) - Raccomandazioni basate sull'utente | Raccomanda gli elementi in base alla cronologia di navigazione, visualizzazione e acquisto di ogni visitatore. Tali elementi sono generalmente denominati "Consigliati per l'utente."<br>Questo criterio consente di fornire contenuti ed esperienze personalizzati sia ai visitatori nuovi che di ritorno. L'elenco delle raccomandazioni è ponderato per l'attività più recente del visitatore, viene aggiornato in sessione e diventa più personalizzato man mano che il visitatore naviga nel sito. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
