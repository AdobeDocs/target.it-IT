---
keywords: analytics tracking server;A4T;analytics segments;report suites;incorrect data;orphaned;sdid;VisitorAPI.js;mboxMCSDID;phantom;unspecified
description: In questo argomento vengono descritti alcuni problemi che sono stati riscontrati durante l’utilizzo di Analytics come origine per la generazione di rapporti per Target (A4T).
title: Risolvere i problemi relativi all’integrazione di Analytics e Target (A4T)
feature: a4t troubleshooting
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 80%

---


# Risolvere i problemi relativi all’integrazione di Analytics e Target (A4T){#troubleshoot-the-analytics-and-target-integration-a-t}

In questo argomento vengono descritti alcuni problemi che sono stati riscontrati durante l’utilizzo di Analytics come origine per la generazione di rapporti per Target (A4T).

## Le attività non mostrano dati in Analytics, ma sono elencate come “non specificato”.{#unspecified}

Questo può accadere per diversi motivi:

* La classificazione in [!DNL Target] non è stata completamente elaborata.

   In genere la classificazione richiede tra 24 e 72 ore per classificare i rapporti dopo il primo salvataggio.

* La suite di rapporti non contiene dati, ma [!DNL Target] ha effettuato un tentativo di classificazione dei risultati. [!DNL Target] non può classificare i dati finché non si verifica il primo risultato.

   Assicurati che la suite di rapporti abbia avuto almeno un risultato.

* La chiamata di classificazione da [!DNL Target] ad [!DNL Analytics] non è riuscita.

   [Contatta l’Assistenza clienti](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

>[!NOTE]
>
>A volte i dati vengono visualizzati correttamente nei rapporti, ma successivamente vengono elencati come “non specificato” perché è stata aggiunta una nuova attività per la quale non è ancora stata completata la classificazione. Tieni presente che la classificazione richiede tra 24 e 72 ore per classificare i rapporti dopo il primo salvataggio.
>
>Quando compare la dicitura “non specificato” non viene perso alcun dato. I dati vengono assegnati correttamente all’attività o all’esperienza appropriata dopo l’esecuzione della classificazione.

## I miei dati di Analytics mostrano un conteggio di visite e visitatori gonfiato dall’avvio di A4T. {#section_4BE374E573D44FB7918611699B74F58E}

Per ulteriori informazioni, consulta [Minimizzare i conteggi gonfiati per visite e visitatori in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## L’incremento stimato nella metrica Ricavo non mostra dati corretti. {#section_35D766E5E4D347C39E15D08AA883FBB0}

I dettagli dell’incremento e dell’affidabilità di Target non sono disponibili in Analytics. Sono, tuttavia, disponibili nei rapporti di Target.

## Le attività non vengono visualizzate nei rapporti di Analytics. {#section_F7001EB4670F4B3497CC7DA60BBDA6D5}

Le attività A4T richiedono che sia stato specificato un server di tracciamento di Analytics. Consulta [Utilizzo di un server di tracciamento di Analytics](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) per assicurarti che il server di tracciamento di Analytics sia configurato correttamente.

>[!NOTE]
>
>Se utilizzi Adobe Analytics come origine per la generazione di rapporti dell’attività e la versione 61 (o successiva) di mbox.js o la versione 0.9.1 (o successiva) di at.js, non è necessario specificare un server di tracciamento durante la creazione di attività. La libreria mbox.js o at.js invia automaticamente i valori del server di tracciamento a [!DNL Target]. Durante la creazione di attività, puoi lasciare vuoto il campo [!UICONTROL Server di tracciamento] nella pagina [!UICONTROL Obiettivi e impostazioni].

## I miei segmenti di Analytics non compaiono in Target. {#section_DEE87F1557834F448E99381D3D02EEEF}

Assicurati di disporre delle autorizzazioni necessarie prima di iniziare a creare attività A4T:

* È necessario appartenere al gruppo di accesso ai servizi Web in Adobe Analytics per poter utilizzare Analytics come origine per la generazione di rapporti per Target.
* È necessario essere membri di uno o più gruppi Experience Cloud che hanno accesso ad Analytics e a Target.
* Verifica che Analytics e Target siano visualizzati nella sezione App marketing del menu di navigazione di sinistra.

## Le metriche per percentuale di mancato recapito, mancato recapito e uscite sembrano positive nei rapporti. {#section_B5C3D56EF0344407AE67ABEB93037F5A}

Questo è un problema noto.

Anche se queste metriche sono negative, nei rapporti di Target l’incremento è mostrato come se fossero positive. Ad esempio, anche se si desidera una percentuale di mancato recapito più bassa, la percentuale più elevata viene visualizzata come vincitore con l’incremento più alto. Considera queste metriche e ad altre simili, e se preferisci aumentare o diminuire i numeri, quando prendi decisioni in base ai rapporti.

## The report suite I need does not display. {#section_BD8F956E41D6475B98B7BF0C74CC387C}

The list of report suites that appears in [!DNL Target Standard/Premium] is the list of report suites that have been configured for [!DNL Analytics] as the reporting source for [!DNL Target] (A4T). Questo significa che potresti non vedere tutte le suite di rapporti di cui disponi.

Inoltre, se utilizzi più origini di reporting, le suite di rapporti devono essere presenti anche nell&#39;origine di reporting predefinita impostata in [!DNL Target] ; in caso contrario, le suite di rapporti non verranno visualizzate.

If you still don&#39;t see the report suite you are looking for, contact [Client Care](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) to get it enabled.

## Non trovo nei rapporti la quantità di dati che mi aspettavo. {#section_75002584FA63456D8D9086172925DD8D}

Esamina l’implementazione, in particolare nelle pagine in cui i visitatori possono qualificarsi per le esperienze, e assicurati che gli ID dei dati supplementari corrispondano alle chiamate di [!DNL Target] e [!DNL Analytics]. 

* **at.js 1.x**: Nella [!DNL Target] chiamata, l’ID supplementare è contenuto nel `mboxMCSDID` parametro. Nella chiamata di [!DNL Analytics], l’ID supplementare è contenuto nel parametro `sdid`.
* **at.js 2.x**: Nella [!DNL Target] chiamata, l’ID supplementare viene restituito nell’intestazione HTTP come valore per `experienceCloud.analytics.supplementalDataId`. Nella chiamata di [!DNL Analytics], l’ID supplementare è contenuto nel parametro `sdid`.

Il modo più semplice per esaminare l&#39;ID supplementare è utilizzare Adobe Experience Platform Debugger.

Se il debugger non è installato, vedere [Introduzione a Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html).

![Strumento di debug](/help/c-integrating-target-with-mac/a4t/assets/debugger.png)

Se nella chiamata di [!DNL Target] non è presente alcun ID di dati supplementare, verifica che il file [!DNL VisitorAPI.js] sia stato caricato prima di [!DNL at.js] o [!DNL mbox.js]. Se nella chiamata di [!DNL Analytics] non è presente alcun ID di dati supplementare, verifica che la chiamata di [!DNL Target] venga attivata prima della chiamata di [!DNL Analytics].

Per ulteriori informazioni, consulta [Implementazione di Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#concept_CE78750AC2A4487D8ACD9369B3EAC85A) o contatta l’[Assistenza clienti](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).
