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
source-git-commit: 5f05f218e5fdea26827b86cb7fbea05ac6349014

---


# Note sulla versione di Target (prerelease){#target-release-notes-prerelease}

Queste note sulla versione contengono informazioni su funzioni, miglioramenti e correzioni per le versioni più recenti o in arrivo di [!DNL Adobe Target].

**Ultimo aggiornamento: 31 ottobre 2019**

>[!NOTE]
>
>Queste note sulla versione contengono delle informazioni sulla versione prerelease. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso. Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali o possono essere diverse, a seconda della tempistica delle release.
>
>I codici tra parentesi sono per uso interno di [!DNL Adobe].

## Piattaforma Target (31 ottobre 2019)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| SDK Java | L’SDK [!DNL Target] Java consente di implementare il lato [!DNL Target] server. Questo SDK Java consente di integrarsi facilmente [!DNL Target] con altre [!DNL Adobe Experience Cloud] soluzioni, come il [!DNL Adobe Experience Cloud Identity Service], [!DNL Adobe Analytics]e [!DNL Adobe Audience Manager].<br>Java SDK introduce procedure ottimali e rimuove le complessità durante l'integrazione con [!DNL Target] tramite l'API di distribuzione, in modo che i team di progettazione possano concentrarsi sulla logica aziendale. Di seguito sono riportate alcune importanti funzioni introdotte nell’ultima versione:<ul><li>Supporto per preacquisizione e notifiche che consentono di ottimizzare le prestazioni tramite caching.</li><li>Supporto per l’ottimizzazione delle prestazioni in caso di integrazione ibrida tra [!DNL Target] le pagine Web e lato server. Stiamo introducendo un'impostazione chiamata `serverState` che viene popolata da esperienze recuperate tramite il lato server, in modo che at.js 2.2 non effettuerà più una chiamata server aggiuntiva per recuperare le esperienze. Questo approccio ottimizza le prestazioni di caricamento delle pagine.</li><li>Supporto per il recupero di attività create VEC tramite Java SDK, reso possibile dalla nuova API di consegna.</li><li>Aperto in modo che i vostri sviluppatori possano contribuire all'SDK [Java di](https://github.com/adobe/target-java-sdk)Target.</li></ul>Per ulteriori informazioni, vedi Note sulla [versione - Target Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md).<br>Per ulteriori informazioni su Target Java SDK, consulta Adobe Tech Blog - Ottimizzazione lato [server con la nuova SDK](https://medium.com/adobetech/server-side-optimization-with-the-new-target-java-sdk-421dc418a3f2)Java di Target. |

## Target Standard/Premium 19.10.2 (31 ottobre 2019)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| ![badge](/help/assets/premium.png) Premium Per gli attributi multivalore | A volte si desidera utilizzare un campo con più valori. Prendi in considerazione gli esempi seguenti:<ul><li>Potete offrire i filmati agli utenti. Un dato film ha più attori.</li><li>Vende biglietti per concerti. Un dato utente ha più bande preferite.</li><li>Vende vestiti. Una camicia è disponibile in diverse dimensioni.</li></ul>Per gestire le raccomandazioni in questi scenari, potete trasmettere dati con più valori a Target Recommendations e utilizzare operatori multivalore speciali. |

## Target Standard/Premium 20.1.1

La versione di Target Standard/Premium 20.1.1 sarà disponibile a gennaio 2020. La data esatta, le funzioni e i miglioramenti saranno annunciati qui.

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
