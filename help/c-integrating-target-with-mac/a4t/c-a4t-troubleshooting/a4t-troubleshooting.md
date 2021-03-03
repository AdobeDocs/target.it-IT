---
keywords: server di tracciamento di analytics;A4T;segmenti di analytics;suite di rapporti;dati non corretti;orfani;sdid;VisitorAPI.js;mboxMCSDID;phantom;non specificato
description: Esplorare i problemi comuni riscontrati dai clienti durante l’utilizzo di Analytics for Target (A4T).
title: Come posso risolvere i problemi relativi all’integrazione di Analytics e Target (A4T)
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: f48c54eb12a416312c3ceb6c1b36c3fc43496e78
workflow-type: tm+mt
source-wordcount: '1003'
ht-degree: 42%

---


# Risolvere i problemi relativi all’integrazione di Analytics e Target (A4T)

Questo argomento tratta alcuni problemi comuni che sono stati riscontrati durante l’utilizzo di [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Adobe Target] (A4T).

## Le attività non mostrano dati in Analytics, ma sono elencate come “non specificato”.{#unspecified}

Ci sono diversi motivi per cui i dati possono verificarsi come &quot;non specificato&quot;:

* La classificazione in [!DNL Target] non è stata completamente elaborata.

   La classificazione richiede generalmente da 24 a 72 ore per classificare i rapporti dopo il primo salvataggio.

* La suite di rapporti non contiene dati, ma [!DNL Target] ha effettuato un tentativo di classificazione dei risultati. [!DNL Target] non può classificare i dati finché non si verifica il primo risultato.

   Assicurati che la suite di rapporti abbia avuto almeno un risultato.

* La chiamata di classificazione da [!DNL Target] ad [!DNL Analytics] non è riuscita.

   [Contatta l’Assistenza clienti](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

Se suddividi la riga &quot;non specificato&quot; per la dimensione &quot;Analytics for Target&quot; e non è costituita da ID attività, significa che tutto viene classificato correttamente. Se gli ID attività sono elencati lì, funge da indicazione per un problema di classificazione.

>[!NOTE]
>
>A volte i dati vengono visualizzati correttamente nei rapporti, ma poi vengono ripristinati come &quot;non specificato&quot; perché è stata aggiunta una nuova attività che non ha completato la classificazione. Ricorda che in genere la classificazione dei rapporti dopo il primo salvataggio richiede da 24 a 72 ore.
>
>Quando compare la dicitura “non specificato” non viene perso alcun dato. I dati vengono assegnati correttamente all’attività o all’esperienza appropriata dopo l’esecuzione della classificazione.

## I rapporti sulle attività di A4T includono una riga con molti eventi &quot;non specificati&quot;. {#added_unspecified_events}

Nel rapporto potrebbe essere visualizzata una riga di eventi &quot;[!UICONTROL Non specificato]&quot;, a seconda della metrica con cui vengono visualizzati i dati.

In genere, questa riga viene visualizzata se scegli una metrica comune nel rapporto che non è specifica di [!DNL Target] (ad esempio, [!UICONTROL Visualizzazioni pagina], [!UICONTROL Visite], [!UICONTROL Visitatori unici] e così via). In questo caso, la riga [!UICONTROL &quot;Non specificato&quot;] include tutte le [!UICONTROL Visualizzazioni di pagina], [!UICONTROL Visite] e [!UICONTROL Visitatori unici] non associate alle attività [!DNL Target].

A tale riga non saranno associate [!DNL Target] informazioni (ad esempio, nessun visitatore, visita o impression). Per ulteriori informazioni, consulta [&quot;Non specificato&quot;, &quot;Nessuno&quot;, &quot;Altro&quot; e &quot;Sconosciuto&quot; nel reporting](https://experienceleague.adobe.com/docs/analytics/technotes/unspecified.html?lang=en) nelle *note tecniche di Analytics*.

Se scegli una metrica specifica [!DNL Target] nel rapporto, la riga [!UICONTROL &quot;Non specificato&quot;] non viene visualizzata. L&#39;unico modo per evitare di averlo completamente nel rapporto è quello di impostare una chiamata [!DNL Target] su ogni richiesta inviata da quella pagina, che non è comune o necessaria.

## I miei dati di Analytics mostrano un conteggio di visite e visitatori gonfiato dall’avvio di A4T. {#section_4BE374E573D44FB7918611699B74F58E}

Per ulteriori informazioni, consulta [Minimizzare i conteggi gonfiati per visite e visitatori in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## L’incremento stimato nella metrica Ricavo non mostra dati corretti. {#section_35D766E5E4D347C39E15D08AA883FBB0}

I dettagli dell’incremento e dell’affidabilità di Target non sono disponibili in Analytics. Sono, tuttavia, disponibili nei rapporti di Target.

## Le attività non vengono visualizzate nei rapporti di Analytics.  {#section_F7001EB4670F4B3497CC7DA60BBDA6D5}

Le attività A4T richiedono che sia stato specificato un server di tracciamento di Analytics. Consulta  [Utilizzo di un ](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) server di tracciamento di Analytics per assicurarti che il server di tracciamento di Analytics sia configurato correttamente.

>[!NOTE]
>
>Non è necessario specificare un server di tracciamento durante la creazione dell’attività se si utilizza mbox.js versione 61 (o successiva) o at.js versione 0.9.1 (o successiva). La libreria mbox.js o at.js invia automaticamente i valori del server di tracciamento a [!DNL Target]. Durante la creazione di attività, puoi lasciare vuoto il campo [!UICONTROL Server di tracciamento] nella pagina [!UICONTROL Obiettivi e impostazioni].

## I miei segmenti di Analytics non compaiono in Target.  {#section_DEE87F1557834F448E99381D3D02EEEF}

Assicurati di disporre delle autorizzazioni necessarie prima di iniziare a creare attività A4T:

* Appartenere al gruppo Accesso ai servizi Web in Adobe Analytics per poter utilizzare Analytics come origine per la generazione di rapporti per Target
* È membro di uno o più gruppi Experience Cloud con accesso ad Analytics e Target.
* Verifica che Analytics e Target siano visualizzati nella sezione App marketing del menu di navigazione di sinistra.

## Le metriche per percentuale di mancato recapito, mancato recapito e uscite sembrano positive nei rapporti.  {#section_B5C3D56EF0344407AE67ABEB93037F5A}

Queste metriche che appaiono positive nei rapporti sono un problema noto.

Anche se queste metriche sono negative, nei rapporti di Target l’incremento è mostrato come se fossero positive. Ad esempio, anche se si desidera una percentuale di mancato recapito più bassa, la percentuale più elevata viene visualizzata come vincitore con l’incremento più alto. Considera queste metriche e ad altre simili, e se preferisci aumentare o diminuire i numeri, quando prendi decisioni in base ai rapporti.

## La suite di rapporti di cui ho bisogno non viene visualizzata. {#section_BD8F956E41D6475B98B7BF0C74CC387C}

L’elenco delle suite di rapporti visualizzate in [!DNL Target Standard/Premium] è l’elenco delle suite di rapporti configurate per [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target] (A4T). Potresti non visualizzare tutte le suite di rapporti disponibili.

Se utilizzi più origini di reporting, le suite di rapporti devono essere presenti anche nell’origine di reporting predefinita impostata in [!DNL Target]. Se le suite di rapporti non sono nell’origine di reporting predefinita, le suite di rapporti non vengono visualizzate.

Se la suite di rapporti che stai cercando non viene ancora visualizzata, contatta l’ [Assistenza clienti](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) per abilitarla.

## Non trovo nei rapporti la quantità di dati che mi aspettavo.  {#section_75002584FA63456D8D9086172925DD8D}

Esamina l’implementazione, in particolare nelle pagine in cui i visitatori possono qualificarsi per le esperienze, e assicurati che gli ID dei dati supplementari corrispondano alle chiamate di [!DNL Target] e [!DNL Analytics]. 

* **at.js 1.x**: Nella  [!DNL Target] chiamata , l’ID supplementare è contenuto nel  `mboxMCSDID` parametro . Nella chiamata di [!DNL Analytics], l’ID supplementare è contenuto nel parametro `sdid`.
* **at.js 2.x**: Nella  [!DNL Target] chiamata , l’ID supplementare viene restituito nell’intestazione HTTP come valore per  `experienceCloud.analytics.supplementalDataId`. Nella chiamata di [!DNL Analytics], l’ID supplementare è contenuto nel parametro `sdid`.

Il modo più semplice per esaminare l’ID supplementare è utilizzare il debugger di Adobe Experience Platform.

Se non hai installato il debugger, consulta [Introduzione al debugger di Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html).

![Strumento di debug](/help/c-integrating-target-with-mac/a4t/assets/debugger.png)

Se nella chiamata di [!DNL Target] non è presente alcun ID di dati supplementare, verifica che il file [!DNL VisitorAPI.js] sia stato caricato prima di [!DNL at.js] o [!DNL mbox.js]. Se nella chiamata di [!DNL Analytics] non è presente alcun ID di dati supplementare, verifica che la chiamata di [!DNL Target] venga attivata prima della chiamata di [!DNL Analytics].

Per ulteriori informazioni, consulta [Implementazione di Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#concept_CE78750AC2A4487D8ACD9369B3EAC85A) o contatta l’[Assistenza clienti](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).
