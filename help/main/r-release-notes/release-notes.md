---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti;aggiornamenti;aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 693b862bc39fc3b1b7d93988bd80cdd51657354b
workflow-type: tm+mt
source-wordcount: '1430'
ht-degree: 19%

---

# Note sulla versione (corrente) di [!DNL Target]

Esplora le funzioni, i miglioramenti e le correzioni più recenti in [!DNL Adobe Target]. Queste note sulla versione descrivono anche gli aggiornamenti alle API [!DNL Target], agli SDK, a [!DNL Adobe Experience Platform Web SDK], at.js e ad altri componenti della piattaforma, se applicabili.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## Aggiornamenti urgenti da conoscere {#time-sensitive}

[!BADGE Importante]{type=Informative}

Per gli aggiornamenti sensibili al tempo relativi a [!DNL Adobe Target] e alla tua implementazione, [!DNL Adobe] fornisce note dettagliate sulla versione e documentazione tramite [!UICONTROL Experience League]. Di seguito sono riportate alcune caratteristiche principali relative all’implementazione:

### La versione dell&#39;interfaccia utente [!DNL Target] è deprecata

Per ulteriori informazioni, vedere [[!DNL Target] Domande frequenti sull&#39;aggiornamento dell&#39;interfaccia utente](/help/main/c-intro/updated-ui-faq.md).

## [!DNL Target Standard/Premium] 25.11.1 (10 novembre 2025)


**Analytics for Target (A4T)**

+++Vedi i dettagli
* **[!UICONTROL Goals & Settings]messaggio di errore quando si utilizza [!DNL Adobe Analytics] come origine per la generazione di rapporti nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente [!UICONTROL Overview] aggiornata in cui nella sezione Obiettivi veniva visualizzato l&#39;errore &quot;Si è verificato un errore. Impossibile completare la richiesta. Contattare [!DNL Adobe Client Care] se il problema persiste&quot; quando [!DNL Adobe Analytics] (A4T) è stato selezionato come origine per la generazione di rapporti. Gli obiettivi ora vengono visualizzati correttamente con [!UICONTROL Adobe Analytics] metriche, garantendo una visibilità coerente tra le origini di reporting. (TGT-54021)

+++

**Tipi di pubblico**

+++Vedi i dettagli
* **Impossibile selezionare più tipi di pubblico per reportistica nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale gli utenti non potevano selezionare più tipi di pubblico di reportistica creati contemporaneamente durante la modifica di un&#39;attività. È ora possibile assegnare più tipi di pubblico contemporaneamente, migliorando la flessibilità e l’efficienza nella configurazione del reporting. (TGT-53253)

+++

**Offerte decisionali**

+++Vedi i dettagli
* **Impossibile modificare o sostituire le offerte di decisioning nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale non era possibile modificare o sostituire le offerte di decisioning tramite il pannello [!UICONTROL Modifications] e i nomi delle offerte apparivano vuoti. Le offerte Decisioning sono ora completamente accessibili e modificabili, ripristinando la parità con l’interfaccia utente legacy e garantendo che i clienti possano gestirle direttamente all’interno delle attività. (TGT-53884)

+++

**Localizzazione**

+++Vedi i dettagli
* **Sono stati corretti diversi errori di localizzazione nell&#39;interfaccia utente coreana e giapponese.** (TGT-54003, TGT-54004, TGT-54006, TGT-54007 E TGT-54018)

+++

**[!UICONTROL Recommendations]**

+++Vedi i dettagli
* **La promozione per attributo con corrispondenza attributo entità non è riuscita a caricare la chiave di consiglio dopo il salvataggio dell&#39;attività.** È stato risolto un problema a causa del quale le promozioni di tipo [!UICONTROL Promotion by Attribute] con tipo di regola [!UICONTROL Entity Attribute Matching] non caricavano la chiave di consiglio quando veniva modificata dopo il salvataggio di un&#39;attività. Il problema è stato causato dalla mancata richiesta di `customKeyId` tramite GraphQL. Le chiavi di consiglio ora vengono caricate correttamente durante le modifiche di promozione. (TGT-53117)
* **Il consiglio persiste visivamente quando si passa da ExpB a ExpA.** È stato risolto un problema a causa del quale l&#39;inserimento di un consiglio nell&#39;Esperienza B e il successivo passaggio all&#39;Esperienza A lasciavano visibile la casella dell&#39;offerta di consiglio. Questa era solo un’incoerenza visiva; le modifiche ora vengono riprodotte correttamente quando si passa da un’esperienza all’altra, garantendo un comportamento accurato dell’interfaccia utente. (TGT-53911)
* **Chiave consiglio non caricata per [!UICONTROL Promotion by Attribute] con [!UICONTROL Entity Attribute] corrispondente.** È stato risolto un problema a causa del quale le promozioni di tipo [!UICONTROL Promotion by Attribute] con tipo di regola [!UICONTROL Entity Attribute Matching] non caricavano la chiave di consigli quando venivano modificate dopo il salvataggio di un&#39;attività. La chiave dei consigli ora viene recuperata correttamente tramite GraphQL, garantendo così la visualizzazione delle promozioni e il funzionamento previsto. (TGT-53917)
* **La modifica di consigli su elementi HTML nascosti non funziona nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente di [!UICONTROL New Create] e del Compositore esperienza visivo a causa del quale non era possibile modificare le attività di consigli applicate agli elementi HTML nascosti. Questa funzionalità ora funziona come previsto, ripristinando la parità con l’interfaccia utente legacy e garantendo che i consigli possano essere modificati indipendentemente dalla visibilità degli elementi. (TGT-53953)
* **Impossibile modificare le attività di consigli su elementi HTML nascosti nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale non era possibile modificare le attività di consigli applicate agli elementi HTML nascosti. Questa funzionalità ora funziona come previsto, ripristinando la parità con l’interfaccia utente legacy e garantendo che i consigli possano essere modificati indipendentemente dalla visibilità degli elementi. (TGT-53951)
* **Nel catalogo dei consigli mancano a intermittenza valori di attributi nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente [!UICONTROL Recommendations] aggiornata a causa del quale le inserzioni di ricerca catalogo non riuscivano a intermittenza a visualizzare alcuni valori di attributo (ad esempio, un messaggio) anche quando presenti nel feed del prodotto. I valori degli attributi ora vengono caricati in modo coerente nei risultati di ricerca senza richiedere la riconfigurazione delle colonne, migliorando l’affidabilità e l’efficienza per la gestione del catalogo. (TGT-52769)
* Pulsante **[!UICONTROL Download Recommendations]mancante per le attività [!DNL Recommendations] nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente [!DNL Recommendations] aggiornata in cui il pulsante [!UICONTROL Download Recommendations] non era visibile per le attività A/B che utilizzano i consigli. Il pulsante ora viene visualizzato correttamente, consentendo agli utenti di esportare i dati dei consigli come previsto, in linea con le funzionalità nell’interfaccia utente legacy. (TGT-53768)
* Pulsante **[!UICONTROL Download Recommendation Data]mancante nell&#39;interfaccia utente Panoramica aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata di [!UICONTROL Overview] a causa del quale il pulsante [!UICONTROL Download Recommendation Data] non era visibile per le attività che contenevano consigli. Il pulsante ora viene visualizzato correttamente, garantendo che gli utenti possano esportare direttamente i dati dei consigli senza dover tornare all’interfaccia utente legacy. (TGT-53772)
* **La modifica dei criteri di attività a volte causava la visualizzazione di una schermata vuota nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata in cui se si faceva clic su [!UICONTROL Edit Criteria in Experiences] veniva occasionalmente visualizzata una schermata vuota per alcune attività. L’editor dei criteri ora viene caricato in modo affidabile in tutte le attività, garantendo agli utenti la possibilità di modificare senza interruzioni. (TGT-53961)
* **Impossibile modificare i criteri di sequenza nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale il tentativo di modificare [!UICONTROL Sequence Criteria] causava il blocco della finestra a comparsa dei criteri durante il caricamento, con la visualizzazione di una schermata vuota. L’editor dei criteri ora viene caricato correttamente, consentendo agli utenti di modificare e aggiornare i criteri della sequenza senza interruzioni. (TGT-53985)

+++

**[!UICONTROL Reports]**

+++Vedi i dettagli
* Le posizioni di **[!UICONTROL Multivariate Test] (MVT) e il problema di generazione dei rapporti sui grafici hanno impedito la generazione dei rapporti.** È stato risolto un problema che impediva alle attività MVT di generare i report [!UICONTROL Location Contribution] e Graph nell&#39;interfaccia utente di Target, causando la visualizzazione dell&#39;errore &quot;Si è verificato un errore. Non possiamo completare la tua richiesta.&quot; I rapporti ora vengono caricati correttamente nell’interfaccia utente, garantendo piena visibilità. (TGT-53654)
* **Impossibile caricare i report MVT a causa di [!UICONTROL Element] errore di report dei contributi.** È stato risolto un problema che impediva il caricamento dei rapporti attività MVT nell&#39;interfaccia utente di Target, mostrando l&#39;errore &quot;Impossibile recuperare il rapporto sul contributo degli elementi&quot;. I rapporti ora vengono visualizzati correttamente, garantendo la piena visibilità dei contributi degli elementi. (TGT-53691)
* **Esporta i dettagli dell&#39;ordine in problema CSV per [!UICONTROL Experience Targeting] attività (XT).** È stato risolto un problema che causava la visualizzazione errata dell&#39;opzione [!UICONTROL Export Order Details to CSV] per le attività XT e la restituzione di un file vuoto. L’opzione ora viene visualizzata solo per le attività di Personalizzazione automatizzata, garantendo funzionalità di esportazione accurate e evitando confusione. (TGT-53798)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Vedi i dettagli
* Il problema del pulsante **[!UICONTROL Delete Modification]ha impedito la rimozione delle modifiche dell&#39;attività.** È stato risolto un problema che impediva il funzionamento del pulsante [!UICONTROL Delete Modification] nell&#39;interfaccia utente di [!DNL Target], impedendo agli utenti di rimuovere le modifiche all&#39;interno delle attività. Il pulsante ora funziona come previsto, consentendo la cancellazione delle modifiche in modo affidabile e senza ritardi. (TGT-53728)
* **Selettori preferiti non riconosciuti nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale i selettori preferiti, ad esempio `data-target-component-id`, non venivano visualizzati nell&#39;elenco dei selettori CSS nel Compositore esperienza visivo. Gli utenti possono ora selezionare in modo affidabile gli attributi preferiti invece dei nomi di classe generati in modo dinamico, garantendo un targeting stabile tra gli aggiornamenti della pagina delle applicazioni a pagina singola. (TGT-53908)
* **Allineamento posizione attività non corrispondente tra [!UICONTROL Edit] e [!UICONTROL Overview] pagine.** È stato risolto un problema che impediva l&#39;allineamento della numerazione dei percorsi delle attività nella pagina [!UICONTROL Overview] con gli aggiornamenti effettuati nella pagina [!UICONTROL &#x200B; Edit Experience]. Le posizioni ora rimangono coerenti tra le due viste, garantendo un allineamento accurato ed evitando posizioni mancanti o con numeri errati. (TGT-53960 e TGT-53954)
* **Impossibile tornare alla modalità [!UICONTROL Design] nel Compositore esperienza visivo aggiornato.** è stato risolto un problema nell&#39;interfaccia utente del Compositore esperienza visivo aggiornata a causa del quale gli utenti non potevano tornare alla modalità [!UICONTROL Design] dopo essere passati a una nuova pagina in modalità [!UICONTROL Browse]. L&#39;interruttore [!UICONTROL Design] ora funziona correttamente e consente di applicare le modifiche in modo semplice su più pagine. (TGT-53988 e TGT-53993)
* **Parametro query non visualizzato nella panoramica attività.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale i parametri di query non venivano visualizzati nella pagina [!UICONTROL Overview] per le attività, causando discrepanze tra [!UICONTROL Overview] e gli URL di consegna della pagina. I parametri di query ora vengono visualizzati correttamente, garantendo che le posizioni delle attività siano completamente rappresentate e coerenti tra le viste. (TGT-53701)

+++

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| [Modifiche alla documentazione](/help/main/r-release-notes/doc-change.md) | Consulta le informazioni dettagliate sugli aggiornamenti di questa guida che non sono inclusi nelle presenti note sulla versione. |
| [Note sulla versione per le versioni precedenti](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium. |
| [Note sulla versione di Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=it){target=_blank} | Ultime note sulla versione per le soluzioni Adobe Experience Cloud. |

## Informazioni pre-release {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| [Adobe Priority Product Update](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Notifiche anticipate sui miglioramenti dei prodotti in arrivo per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud]. |
| [Note sulla versione di Target: pre-release](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informazioni sulle versioni di Target del mese corrente, incluse le informazioni pre-release. |
