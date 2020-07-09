---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Queste note sulla versione forniscono informazioni su funzioni, miglioramenti, correzioni e problemi noti per ciascuna versione di Adobe Target Standard e Target Premium.
title: 'Note sulla versione di Adobe Target (corrente) '
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 322b14629d420601b763fed7597c43a8458b7dbf
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 29%

---


# Note sulla versione di Target (corrente){#target-release-notes-current}

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di Target Standard e Target Premium. Inoltre, se applicabile, sono incluse anche le note sulla versione per le API Target, gli SDK, la libreria JavaScript (at.js) e altre modifiche alla piattaforma.

>[!NOTE]
>
>* **mbox.js obsoleto**: Il 30 agosto 2020  Adobe Target non supporterà più la libreria mbox.js. Dopo il 30 agosto 2020, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto positivo sulle pagine che hanno attività Target in esecuzione distribuendo contenuti predefiniti. È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della libreria at.js prima di tale data, in modo da evitare potenziali problemi con i siti. Per ulteriori informazioni, consulta [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) and [Adobe Target Experience Builder (Funzionamento di At.js e Generatore di competenze di ): Chat sviluppatore, migrate  Adobe Target  mbox.js in at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Sebbene mbox.js sia attualmente supportato, a partire da luglio 2017 non sono stati forniti aggiornamenti di funzionalità per questa libreria. Il più recente at.js offre molti vantaggi rispetto a mbox.js. Tra gli altri vantaggi, at.js migliora i tempi di caricamento delle pagine per le implementazioni Web, migliora la sicurezza e offre migliori opzioni di implementazione per le applicazioni a pagina singola.
   >
   >   
   Spostando tutti i clienti a at.js, i nostri tecnici e il nostro staff di supporto saranno in grado di fornirvi nuove funzionalità e di offrire il supporto che vi aspettate da Adobe.
   >
   >
* **Annunci** Target: Consultate la pagina degli annunci Target per informazioni sugli eventi in programma, comprese le sessioni di Target Experience Builder, le chat per sviluppatori, i webinar e le sessioni di Target Coffee Break. Per ulteriori informazioni, consultate Annunci [Target](/help/r-release-notes/target-announcements.md).


I codici tra parentesi sono per uso interno di [!DNL Adobe].

## Target Standard/Premium 20.5.1 (17 giugno 2020)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Analytics for Target (A4T) supporto per le attività di allocazione [!UICONTROL automatica] | [!UICONTROL Le attività di allocazione] automatica ora supportano [Analytics per Target](/help/c-integrating-target-with-mac/a4t/a4t.md).<br>Questa integrazione consente di utilizzare la funzionalità di allocazione [!UICONTROL automatica] dei bandi con più armi per indirizzare il traffico verso esperienze vincenti, utilizzando al tempo stesso una metrica di obiettivo Analytics  Adobe e/o funzionalità di reporting e analisi di [!UICONTROL Adobe  Analytics] .<br>Se avete già [implementato A4T](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) per l’utilizzo con le attività Test A/B e Targeting delle esperienze, siete tutti impostati!<br>Per ulteriori informazioni, consultate [supporto Analytics per Target (A4T) per le attività](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa) di allocazione automatica nella creazione *di* attività. |
| Token di risposta per il metodo di allocazione del traffico per le attività di Auto-Target e Automated Personalization (Personalizzazione automatizzata) | Sono stati aggiunti due token [di](/help/administrating-target/response-tokens.md) risposta alle attività [!UICONTROL Auto-Target] e [!UICONTROL Automated Personalization (Personalizzazione] automatizzata) per consentire di determinare se un visitatore ha ricevuto un&#39;esperienza particolare a seguito dell&#39;assegnazione di un &quot;controllo&quot; o di un traffico &quot;mirato&quot;.<ul><li>`experience.trafficAllocationId` restituisce 0 se un visitatore ha ricevuto un&#39;esperienza dal traffico &quot;controllato&quot; e 1 se ha ricevuto un&#39;esperienza dalla distribuzione del traffico &quot;con targeting&quot;.</li><li>`experience.trafficAllocationType` restituisce &quot;control&quot; o &quot;targeting&quot;.</li></ul>Per ulteriori informazioni sul controllo e sul traffico mirato, vedi [Selezionare il controllo per l&#39;attività](/help/c-activities/t-automated-personalization/experience-as-control.md)Automated Personalization (Personalizzazione automatizzata) o Auto-Target. |
| [!UICONTROL Ruolo Editore] | Questo nuovo ruolo è simile al ruolo [!UICONTROL Osservatore] corrente (può visualizzare le attività, ma non può crearle o modificarle). Tuttavia, il ruolo [!UICONTROL Editore] dispone dell&#39;autorizzazione aggiuntiva per attivare le attività.<br>Per ulteriori informazioni, vedi: <ul><li>**Utenti** Target Standard: [Specifica ruoli e autorizzazioni](/help/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Utenti*.</li><li>**Utenti** Target Premium: [Passaggio 6: Specificate ruoli e autorizzazioni](/help/administrating-target/c-user-management/property-channel/properties-overview.md#section_8C425E43E5DD4111BBFC734A2B7ABC80) in *Configura autorizzazioni* enterprise.</li></ul> |
| Supporto A4T nel 25 [!DNL Analysis Workspace]<br>giugno 2020 | [!UICONTROL Analytics per Target] (A4T) ora è supportato in [!DNL Analysis Workspace]. Il [!UICONTROL pannello] Analytics per Target (A4T) consente di analizzare le [!DNL Adobe Target] attività e le esperienze in [!DNL Analysis Workspace].<br>Per ulteriori informazioni, vedere [Rapporti in  Analytics](/help/c-integrating-target-with-mac/a4t/reporting.md) in *A4T reporting* e [pannello](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/a4t-panel.html) Analytics per Target (A4T) nella *Analytics Tools Guide*. |

### Miglioramenti, correzioni e modifiche

* È stato risolto un problema che causava la memorizzazione della metrica &quot;visitatori&quot; nella definizione dell&#39;attività invece di &quot;VisitatoriUnivoci&quot;. (TGT-37098)
* È stato risolto un problema nell&#39; [!DNL Target] interfaccia utente a causa del quale la barra di scorrimento verticale non funzionava correttamente nella pagina [!UICONTROL Audiences] . (TGT-36968)

## versioni at.js 1.8.2 e at.js 2.3.1 (15 giugno 2020)

Nelle librerie [!DNL Target] at.js sono stati apportati i seguenti miglioramenti e correzioni:

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Payload JSON di at.js 1.8.2 | Questa versione di at.js è una versione di manutenzione e include le seguenti correzioni:<ul><li>È stato risolto un problema che si verificava quando si utilizzavano CNAME e edge override, in at.js 1.*x* potrebbe creare in modo non corretto il dominio del server, causando il fallimento della [!DNL Target] richiesta. (TNT-35064)</li></ul>For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md). |
| Payload JSON di at.js 2.3.1 | Questa release di at.js è una versione di manutenzione e include i miglioramenti e le correzioni seguenti:<ul><li>L’impostazione `deviceIdLifetime` è stata sostituita tramite [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md). (TNT-36349)</li><li>È stato risolto un problema che si verificava quando si utilizzavano CNAME e edge override, in at.js 2.*x* potrebbe creare in modo non corretto il dominio del server, causando il fallimento della [!DNL Target] richiesta. (TNT-35065)</li><li>È stato risolto un problema che si verificava durante l’utilizzo dell’ [!DNL Target] estensione v2 e dell’ [!DNL Launch][!DNL Adobe Analytics] estensione, [!DNL Launch] causava il ritardo della [!DNL Target] chiamata [!DNL Analytics] `sendBeacon` . (TNT-36407, TNT-35990, TNT-36000)</li></ul>For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md). |

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione - API lato server di Target](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Note sulla versione relative  Adobe Target  API lato server. |
| [Note sulla versione - SDK Node.js di Target](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Note sulla versione relative a  SDK Node.js  Adobe Target. |
| [Note sulla versione - Target Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Note sulla versione relative  SDK Java  Adobe Target. |
| [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informazioni dettagliate sulle modifiche in ciascuna versione dell&#39;Adobe Target  in JavaScript library.js. |
| [Dettagli sulle versioni di mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md) | In questa pagina sono elencate le modifiche per ogni versione di mbox.js.<br>Tenete presente che la libreria mbox.js non è più in fase di sviluppo. Tutti i clienti devono migrare da mbox.js a at.js. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud {#section_1BC5F5208DA548E9B4344A0836E4B943}

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| Modifiche alla documentazione | Informazioni dettagliate sugli aggiornamenti apportati a questa guida che potrebbero non essere incluse nelle note sulla versione.<br>Per ulteriori informazioni, consulta [Modifiche alla documentazione](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Note sulla versione per le versioni precedenti | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium.<br>Per ulteriori informazioni, consulta [Note sulla versione per le versioni precedenti](../r-release-notes/release-notes-for-previous-releases.md). |
| Note sulla versione di Adobe Experience Cloud | Ultime note sulla versione per le soluzioni Adobe Experience Cloud.<br>Per ulteriori informazioni, consultate [Note](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html)sulla versione di Experience Cloud. |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| Adobe Priority Product Update | Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Note sulle prossime versioni | Per informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease, consulta la pagina [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md). |
