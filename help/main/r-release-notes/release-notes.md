---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti;aggiornamenti;aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 098415849152065b734cbebbab8dcf1d0805e202
workflow-type: tm+mt
source-wordcount: '1779'
ht-degree: 14%

---

# Note sulla versione (corrente) di [!DNL Target]

Esplora le funzioni, i miglioramenti e le correzioni più recenti in [!DNL Adobe Target]. Queste note sulla versione descrivono anche gli aggiornamenti alle API [!DNL Target], agli SDK, a [!DNL Adobe Experience Platform Web SDK], at.js e ad altri componenti della piattaforma, se applicabili.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## Aggiornamenti urgenti da conoscere {#time-sensitive}

[!BADGE Importante]{type=Informative}

Per aggiornamenti sensibili al tempo relativi a [!DNL Adobe Target] e alla tua implementazione, [!DNL Adobe]fornisce note dettagliate sulla versione e documentazione tramite [!UICONTROL Experience League]. Di seguito sono riportate alcune caratteristiche principali relative all’implementazione:

### La versione dell&#39;interfaccia utente [!DNL Target] è deprecata

+++Vedi i dettagli
Il team [!DNL Target] offre una funzionalità temporanea che consente di passare dall&#39;interfaccia utente [!DNL Target] aggiornata alla versione precedente utilizzando un pulsante di attivazione/disattivazione. Questa opzione è disponibile solo durante la fase finale del rollout dell’interfaccia utente.

![Attivazione/disattivazione versione interfaccia utente di Target](/help/main/r-release-notes/assets/toggle.png)

Una volta completato il rollout, l’interruttore viene rimosso e tutti gli utenti passano definitivamente all’interfaccia utente aggiornata. [!DNL Adobe] consiglia di pianificare in anticipo, in quanto questa funzione verrà gradualmente eliminata a breve.

#### Timeline obsoleto

A causa dei problemi recenti identificati, principalmente correlati a complesse personalizzazioni dei clienti, il team [!DNL Target] ha regolato la timeline di obsolescenza:

* **17 giugno 2025**: tutte le organizzazioni IMS sono state abilitate per l&#39;interfaccia utente [!DNL Target] aggiornata, per utenti specifici o a livello di organizzazione, per iniziare a testare la nuova esperienza.

* **30 giugno 2025**: l&#39;esperienza [aggiornata [!DNL Target] interfaccia utente](/help/main/c-intro/understand-the-target-ui.md) è diventata predefinita per tutte le organizzazioni IMS che hanno attivato l&#39;interruttore della versione dell&#39;interfaccia utente.

   * Per impostazione predefinita, i clienti che attualmente vedono l’interfaccia utente legacy visualizzano ora l’interfaccia utente aggiornata al momento dell’accesso.
   * L’interruttore della versione dell’interfaccia utente rimane disponibile fino alla fine di luglio e consente agli utenti di tornare indietro se necessario.

  >[!IMPORTANT]
  >
  > [!DNL Adobe] consiglia vivamente di utilizzare l&#39;interfaccia utente [!DNL Target] aggiornata. Torna all&#39;interfaccia utente legacy solo se si verifica un problema di blocco, a causa di [limitazioni del comportamento di attivazione/disattivazione](#limitations).

* **dal 15 luglio al 30 luglio 2025**: l&#39;attivazione/disattivazione della versione dell&#39;interfaccia utente verrà disabilitata in modo permanente in più fasi. Le organizzazioni IMS interessate non sono più in grado di ripristinare l’interfaccia utente legacy.

   * Le eccezioni vengono esaminate caso per caso.
   * I ritardi nell’attivazione/disattivazione dell’impostazione obsoleta vengono concessi solo brevemente (alcuni giorni), mentre i problemi di blocco vengono risolti.

Contatta l&#39;[Assistenza clienti Adobe](/help/main/cmp-resources-and-contact-information.md#/help/main/cmp-resources-and-contact-information.md) per qualsiasi problema o se prevedi problemi durante questa transizione.

#### Limitazioni del comportamento di attivazione/disattivazione dell’interfaccia utente {#limitations}

Le informazioni seguenti descrivono i limiti di cui tenere conto quando si sceglie di utilizzare l’interruttore di versione:

* **Visibilità delle nuove attività**: le attività create nell&#39;interfaccia utente aggiornata non saranno visibili se si torna all&#39;interfaccia precedente.
* **Modifica di attività esistenti**: le modifiche apportate alle attività esistenti (originariamente create nell&#39;interfaccia utente legacy) durante l&#39;utilizzo dell&#39;interfaccia utente aggiornata vengono pubblicate nel sito Web. Tuttavia, se passi all’interfaccia precedente, questi aggiornamenti non sono visibili; in questa finestra vengono visualizzati solo gli ultimi aggiornamenti apportati dall’interfaccia precedente.
* **Coerenza dei dettagli dell&#39;attività**: le modifiche più recenti, indipendentemente dall&#39;interfaccia utente utilizzata, si riflettono sul sito Web attivo. Tuttavia, nell’interfaccia utente legacy vengono visualizzate solo le modifiche più recenti apportate all’interno di tale versione. Questa situazione potrebbe causare confusione se le attività modificate nell’interfaccia utente aggiornata hanno un aspetto diverso da quello visualizzato nell’interfaccia utente precedente.

#### Altre risorse sull’interfaccia utente aggiornata

* [[!DNL Target] Domande frequenti sull&#39;aggiornamento dell&#39;interfaccia utente](/help/main/c-intro/updated-ui-faq.md): queste domande frequenti riguardano le domande comuni sulla nuova interfaccia utente [!DNL Target] e sul nuovo Compositore esperienza visivo [!UICONTROL Visual Experience Composer], incluse le modifiche alla navigazione, le posizioni delle funzioni e la rimozione dell&#39;opzione di versione temporanea dell&#39;interfaccia utente. Che tu sia un addetto marketing, uno sviluppatore o un amministratore, queste domande frequenti consentono una transizione fluida e di sfruttare al massimo l’interfaccia utente aggiornata.
* [[!DNL Target Standard/Premium] 25.2.1 (17 febbraio 2025) - Note sulla versione](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): fornisce un riepilogo delle modifiche principali apportate all&#39;interfaccia utente in [!DNL Target] per [!UICONTROL Activities], [!UICONTROL Recommendations] e [!UICONTROL Visual Experience Composer] (Compositore esperienza visivo).
* [[!DNL Target Standard/Premium] 25.1.1 (9 gennaio 2025) - Note sulla versione](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): fornisce un riepilogo delle modifiche principali apportate all&#39;interfaccia utente in [!DNL Target] per [!UICONTROL Offers Library].
* [Comprendere l&#39;interfaccia utente [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md): fornisce una breve panoramica per acquisire familiarità con [!DNL Target] e fornisce collegamenti per informazioni più approfondite e istruzioni dettagliate.
* [[!UICONTROL Visual Experience Composer] modifiche](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): la versione di [!DNL Adobe Target Standard/Premium] 25.2.1 (17 febbraio 2015) introduce una versione aggiornata di [!UICONTROL Visual Experience Composer] (VEC). Questo articolo spiega le differenze tra le versioni legacy e aggiornata del Compositore esperienza visivo.
* [[!UICONTROL Visual Experience Composer] opzioni](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): questo articolo illustra l&#39;interfaccia utente del Compositore esperienza visivo aggiornata e le relative opzioni.

+++

## Aggiornamenti Datastream (19 settembre 2025)

La combinazione di ID e sandbox dello stream di dati deve essere univoca per [!DNL Adobe Target] connessioni di destinazione.

È stata aggiornata la logica di convalida per le connessioni di destinazione [!DNL Target] per fare in modo che la combinazione di ID dello stream di dati e nome della sandbox sia univoca all’interno di un’organizzazione IMS. Ciò significa che:

* Impossibile riutilizzare la stessa coppia ID dello stream di dati + nome sandbox in più connessioni di destinazione [!DNL Target].
* Lo stesso ID dello stream di dati può essere utilizzato per connessioni diverse solo se sono configurate in sandbox diverse.
* Questa regola si applica a tutte le selezioni dello stream di dati, anche quando si seleziona &quot;Nessuno&quot;.

Questo aggiornamento garantisce una configurazione coerente e impedisce conflitti tra ambienti con più sandbox. Per ulteriori informazioni, vedere [Connessione Adobe Target](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection){target=_blank} nella *Guida delle destinazioni Experience Platform*.

## [!DNL Target Standard/Premium] 25.9.1 (5 settembre 2025)

Questa versione include i seguenti aggiornamenti e correzioni:

**[!UICONTROL Experience Fragments]**

+++Vedi i dettagli
* **Attribuzione utente migliorata per le offerte [!UICONTROL AEM Experience Fragment].** È stato risolto un problema nel Compositore esperienza visivo in cui il campo &quot;[!UICONTROL Last updated]&quot; per le offerte [!UICONTROL AEM Experience Fragment] (XF) mostrava in modo errato un ID di codice invece del nome utente. Questa discrepanza si è verificata durante la selezione delle offerte nell’interfaccia utente aggiornata, creando un’incoerenza con l’interfaccia utente legacy e le offerte HTML, in cui veniva visualizzato correttamente il nome dell’ultimo editor. Questa correzione garantisce un’attribuzione utente coerente tra i tipi di offerta, migliorando la trasparenza e l’allineamento al comportamento previsto. (TGT-52880 e TGT-52898)

+++

**Offer Decisioning**

+++Vedi i dettagli
* **L&#39;errore di decisione dell&#39;offerta è stato risolto per le offerte ODE.** È stato risolto un problema a causa del quale le offerte ODE (Offer Decision Engine) inserite tramite [!DNL Target] restituivano un errore 400 a causa di metadati di formato mancanti. Il messaggio di errore indicava che il tipo MIME era nullo, impedendo l’elaborazione corretta delle decisioni sulle offerte. Questa correzione assicura la corretta gestione dei metadati dell’offerta, ripristinando la funzionalità per la distribuzione personalizzata dei contenuti e consentendo l’esecuzione ininterrotta delle campagne di marketing. (TGT-53635)
* **Problema di rendering dell&#39;offerta ODS risolto.** È stato risolto un problema che impediva il rendering delle offerte [!DNL Offer Decision Service] (ODS) create tramite [!DNL Adobe Journey Optimizer] (AJO) durante la generazione delle attività tramite il Compositore esperienza visivo nell&#39;interfaccia utente aggiornata. La stessa configurazione funzionava correttamente nell’interfaccia utente legacy, creando confusione e bloccando l’esecuzione della campagna. Questa correzione assicura la distribuzione coerente delle offerte in entrambe le versioni dell’interfaccia utente, ripristinando il comportamento previsto per la personalizzazione basata su AJO.

+++

**Rapporti**

+++Vedi i dettagli
* **Opzione Download ripristinata nella sezione dei report dell&#39;interfaccia utente aggiornata per la panoramica dei report.** È stato risolto un problema nella nuova interfaccia utente della panoramica a causa del quale il pulsante [!UICONTROL Download] non era presente nella sezione Rapporti, impedendo agli utenti di esportare i punteggi di importanza degli attributi. Questo aggiornamento ripristina la funzionalità di esportazione completa, consentendo un accesso semplificato ai dati scaricabili a scopo di analisi e reporting. (TGT-53222)
* Pulsante **[!UICONTROL Download full CSV report]ripristinato nella visualizzazione [!UICONTROL Important attributes].** È stato risolto un problema nell&#39;interfaccia utente aggiornata per la creazione di attività in cui il pulsante [!UICONTROL Download full CSV report] non era presente nella sezione [!UICONTROL Important Attributes] della visualizzazione Report. Questa correzione consente di ripristinare l’accesso alle informazioni scaricabili, garantendo funzionalità coerenti sia nell’interfaccia utente aggiornata che in quella legacy. (TGT-53238)
* **Sono stati risolti dei problemi relativi alla generazione di rapporti per [!UICONTROL Auto Target] nell&#39;interfaccia utente aggiornata della panoramica.** Sono stati risolti diversi problemi relativi all&#39;interfaccia utente nell&#39;interfaccia di panoramica aggiornata che interessavano il reporting delle attività di [!UICONTROL Auto Target]. Queste correzioni includono:

   * Metriche di incremento e affidabilità mancanti nei rapporti di riepilogo
   * Indicatore di colore errato per la casella di controllo &quot;Modelli generati&quot;
   * Rapporto grafico non funzionale nonostante la varianza dei dati in [!DNL Analytics]
   * Collegamento di download mancante per i report [!UICONTROL Automated Segments] e [!UICONTROL Important Attributes]
   * Visualizzazione report [!UICONTROL Automated Segments] interrotto

  Queste correzioni ripristinano il comportamento di reporting previsto e migliorano la visibilità delle prestazioni di [!UICONTROL Auto Target] nell&#39;interfaccia utente aggiornata. (TGT-53484)

+++

**[!UICONTROL Visual Experience Composer]**

+++Vedi i dettagli
* **La convalida del modulo è stata corretta per le condizioni di presenza dei parametri nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata in cui la selezione di &quot;[!UICONTROL Custom mbox parameter value is present]&quot; o &quot;[!UICONTROL Parameter is present]&quot; richiedeva erroneamente ai clienti di immettere un valore. Questo comportamento è in conflitto con la logica prevista, che si limita a verificare l’esistenza di un parametro indipendentemente dal suo valore. La correzione allinea la convalida del modulo al comportamento previsto, consentendo una configurazione dell’attività più fluida e supportando l’adozione completa dell’interfaccia utente aggiornata. (TGT-53638)
* **Logica del modulo corretta per le regole di presenza dei parametri nella consegna delle pagine.&quot;** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale la selezione delle regole di consegna pagine come &quot;[!UICONTROL Parameter is present],&quot; &quot;[!UICONTROL Parameter is not present],&quot;[!UICONTROL Parameter value is present]&quot; o &quot;[!UICONTROL Parameter value is not present]&quot; richiedeva erroneamente agli utenti di immettere un valore di parametro aggiuntivo. Questo comportamento non era coerente con l’interfaccia utente legacy e contraddiceva la logica prevista di rilevamento della presenza di parametri senza specificare un valore. Questa correzione ripristina il comportamento di configurazione previsto delle regole, semplificando la configurazione delle attività e migliorando l’usabilità. (TGT-53640)
* **Logica di convalida migliorata per il generatore di regole con più pagine nell&#39;interfaccia utente aggiornata.** Sono stati risolti diversi problemi di convalida nel generatore di regole con più pagine nell&#39;interfaccia utente aggiornata. Queste correzioni includono:

   * Impedire la creazione di regole quando il parametro mbox è vuoto
   * Visualizzazione dei messaggi di errore appropriati per gli stati di regola non validi
   * Correzione della logica di convalida per gli operatori unari e basati su parametri che non richiedono valori di operando
   * Abilitazione delle regole dei frammenti hash con operatori unari ripristinando la funzionalità di salvataggio

  Questi aggiornamenti garantiscono una configurazione precisa delle regole e migliorano l’usabilità in scenari di consegna pagine complessi. (TGT-53722)
* **Problema di ridenominazione percorso risolto nelle attività A/B e MVT.** È stato corretto un bug nell&#39;interfaccia utente aggiornata a causa del quale la ridenominazione di un percorso in un&#39;attività [!UICONTROL A/B Test] o [!UICONTROL Multivariate Test] (MVT) non persisteva dopo la navigazione tra l&#39;elenco dei percorsi, il targeting e il back. Questo aggiornamento garantisce che le modifiche al nome della posizione vengano salvate e applicate in modo coerente in tutto il flusso di lavoro dell’attività. (TGT-52367)
* **È stata corretta la persistenza del nome della posizione per le attività MVT e AP nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale i nomi di percorso modificati nelle attività [!UICONTROL Multivariate Test] (MVT) e [!UICONTROL Automated Personalization] (AP) non venivano salvati correttamente. Dopo aver rinominato una posizione, lo spostamento tra le schede, ad esempio [!UICONTROL Targeting] e [!UICONTROL Experiences], ha ripristinato lo stato precedente dei nomi. Questa correzione assicura una denominazione della posizione coerente tra le schede e migliora l’affidabilità durante la configurazione dell’attività. (TGT-52927)
* **L&#39;etichettatura della posizione è stata corretta nel pannello Gestione esperienze per le attività MVT.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale il pannello [!UICONTROL Manage Experiences] nelle attività [!UICONTROL Multivariate Test] (MVT) mostrava una numerazione dei percorsi incoerente. Questa correzione assicura che le etichette di posizione siano sequenziali e correttamente allineate con le modifiche definite dall’utente, migliorando la chiarezza e l’usabilità durante la configurazione dell’esperienza. (TGT-52929)

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

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| [Adobe Priority Product Update](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Notifiche anticipate sui miglioramenti dei prodotti in arrivo per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud]. |
| [Note sulla versione di Target: prerelease](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease. |
