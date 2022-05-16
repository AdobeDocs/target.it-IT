---
keywords: server di tracciamento di analytics;A4T;segmenti di analytics;suite di rapporti;dati non corretti;orfani;sdid;VisitorAPI.js;mboxMCSDID;phantom;non specificata
description: Esplora i problemi comuni riscontrati dai clienti durante l’utilizzo di Analytics per  [!DNL Target]  (A4T).
title: Come posso risolvere i problemi relativi all’integrazione di Analytics e [!DNL Target]  (A4T)?
feature: Analytics for Target (A4T)
exl-id: 7d155cbe-e799-43b5-afc2-1aea43f432ba
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: ht
source-wordcount: '987'
ht-degree: 100%

---

# Risoluzione dei problemi relativi all’integrazione di Analytics e [!DNL Target] (A4T)

In questo argomento vengono descritti alcuni problemi che sono stati riscontrati durante l’utilizzo di [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Adobe Target] (A4T).

## Le attività non mostrano dati in Analytics, ma sono elencate come “non specificate”. {#unspecified}

Ci sono diversi motivi per cui i dati possono apparire come “non specificati”:

* La classificazione in [!DNL Target] non è stata completamente elaborata.

   In genere la classificazione impiega da 24 a 72 ore per classificare i rapporti dopo il primo salvataggio.

* La suite di rapporti non contiene dati, ma [!DNL Target] ha effettuato un tentativo di classificazione dei risultati. [!DNL Target] non può classificare i dati finché non si verifica il primo risultato.

   Assicurati che la suite di rapporti abbia avuto almeno un risultato.

* La chiamata di classificazione da [!DNL Target] ad [!DNL Analytics] non è riuscita.

   [Contatta l’Assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

Se suddividi la riga “Non specificata” per la dimensione “Analytics for Target” e non presenta alcun ID attività, significa che tutto è classificato correttamente. Se sono elencati gli ID attività, ciò indica un problema di classificazione.

>[!NOTE]
>
>A volte i dati vengono visualizzati correttamente nei rapporti, ma successivamente vengono elencati come “non specificati” perché è stata aggiunta una nuova attività per la quale non è ancora stata completata la classificazione. Tieni presente che in genere la classificazione impiega da 24 a 72 ore per classificare i rapporti dopo il primo salvataggio.
>
>Quando compare la dicitura “non specificato” non viene perso alcun dato. I dati vengono assegnati correttamente all’attività o all’esperienza appropriata dopo l’esecuzione della classificazione.

## I rapporti sulle attività A4T includono una riga con molti eventi “non specificati”. {#added_unspecified_events}

Nel rapporto potrebbe essere visualizzata una riga di eventi con dicitura “[!UICONTROL Non specificata]”, a seconda della metrica con cui visualizzi i dati.

Solitamente, questa riga viene visualizzata se si sceglie una metrica comune nel rapporto che non è specifica di [!DNL Target] (ad esempio, [!UICONTROL Visualizzazioni di pagina], [!UICONTROL Visite], [!UICONTROL Visitatori unici] e così via). In questo caso, la riga con dicitura [!UICONTROL “Non specificata”] include tutte le [!UICONTROL Visualizzazioni di pagina], le [!UICONTROL Visite] e i [!UICONTROL Visitatori unici] non associati ad attività [!DNL Target].

Quella riga non includerà alcuna informazione associata a [!DNL Target] (ad esempio, nessun visitatore, visita o impression). Per ulteriori informazioni, consulta [“Unspecified”, “None”, “Other”, and “Unknown” in reporting](https://experienceleague.adobe.com/docs/analytics/technotes/unspecified.html?lang=it) (“Non specificata”, “Nessuno,” “Altro,” e “Sconosciuto” nel reporting) in *Note tecniche di Analytics*.

Se scegli una metrica specifica di [!DNL Target] nel rapporto, la riga con dicitura [!UICONTROL “Non specificata”] non viene visualizzata. L’unico modo per evitare di averla nel rapporto è impostare una chiamata [!DNL Target] dietro ogni richiesta inviata da quella pagina, che non è comune o necessaria.

## I miei dati di Analytics mostrano un conteggio di visite e visitatori gonfiato dall’avvio di A4T. {#section_4BE374E573D44FB7918611699B74F58E}

Per ulteriori informazioni, consulta [Minimizzare i conteggi gonfiati per visite e visitatori in A4T](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## L’incremento stimato nella metrica delle entrate non mostra dati corretti. {#section_35D766E5E4D347C39E15D08AA883FBB0}

I dettagli dell’incremento e dell’affidabilità di Target non sono disponibili in Analytics. Sono, tuttavia, disponibili nei rapporti di Target.

## Le attività non vengono visualizzate nei rapporti di Analytics. {#section_F7001EB4670F4B3497CC7DA60BBDA6D5}

Le attività A4T richiedono che sia stato specificato un server di tracciamento di Analytics. Consulta  [Using an Analytics Tracking Server](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) (Utilizzo di un server di tracciamento di Analytics) per assicurarti che il server di tracciamento di Analytics sia configurato correttamente.

>[!NOTE]
>
>Se utilizzi la versione 0.9.1 (o successiva) di at.js, non devi specificare un server di tracciamento durante la creazione dell’attività. La libreria at.js invia automaticamente i valori del server di tracciamento a [!DNL Target]. Durante la creazione di attività, puoi lasciare vuoto il campo [!UICONTROL Server di monitoraggio] nella pagina [!UICONTROL Obiettivi e impostazioni].

## I miei segmenti di Analytics non compaiono in Target. {#section_DEE87F1557834F448E99381D3D02EEEF}

Assicurati di disporre delle autorizzazioni necessarie prima di iniziare a creare attività A4T:

* Devi appartenere al gruppo di accesso ai servizi web in Adobe Analytics per poter utilizzare Analytics come origine per la generazione di rapporti per Target
* Devi essere membro di uno o più gruppi Experience Cloud che hanno accesso ad Analytics e a Target.
* Verifica che Analytics e Target siano visualizzati nella sezione App marketing del menu di navigazione di sinistra.

## Le metriche per percentuale di mancato recapito, mancato recapito e uscite sembrano positive nei rapporti. {#section_B5C3D56EF0344407AE67ABEB93037F5A}

Queste metriche che sembrano positive nei rapporti sono un problema noto.

Anche se queste metriche sono negative, nei rapporti di Target l’incremento è mostrato come se fossero positive. Ad esempio, anche se si desidera una percentuale di mancato recapito più bassa, la percentuale più elevata viene visualizzata come vincitore con l’incremento più alto. Considera queste metriche e ad altre simili, e se preferisci aumentare o diminuire i numeri, quando prendi decisioni in base ai rapporti.

## La suite di rapporti di cui ho bisogno non viene visualizzata. {#section_BD8F956E41D6475B98B7BF0C74CC387C}

L’elenco delle suite di rapporti visualizzate in [!DNL Target Standard/Premium] corrisponde alle suite di rapporti configurate per [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target] (A4T). Potresti non visualizzare tutte le suite di rapporti disponibili.

Se utilizzi più origini per la generazione di rapporti, le suite di rapporti devono essere presenti anche nell’origine predefinita impostata in [!DNL Target]. Le suite di rapporti non vengono visualizzate se non sono presenti nell’origine per la generazione di rapporti predefinita.

Se ancora non trovi la suite di rapporti che stai cercando, contatta l’[Assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) per abilitarla.

## Nei rapporti non trovo la quantità di dati che mi aspettavo. {#section_75002584FA63456D8D9086172925DD8D}

Controlla l’implementazione, in particolare nelle pagine in cui i visitatori possono qualificarsi per le esperienze, e assicurati che gli ID dei dati supplementari corrispondano alle chiamate di [!DNL Target] e [!DNL Analytics].

* **at.js 1.x**: nella chiamata di [!DNL Target], l’ID supplementare è contenuto nel parametro `mboxMCSDID`. Nella chiamata di [!DNL Analytics], l’ID supplementare è contenuto nel parametro `sdid`.
* **at.js 2.x**: nella chiamata [!DNL Target], l’ID supplementare viene restituito nell’intestazione HTTP come valore di `experienceCloud.analytics.supplementalDataId`. Nella chiamata di [!DNL Analytics], l’ID supplementare è contenuto nel parametro `sdid`.

Il modo più semplice per esaminare l’ID supplementare è utilizzare Adobe Experience Platform Debugger.

Se non hai installato il debugger, consulta la pagina di [introduzione ad Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html?lang=it).

![Strumento di debug](/help/main/c-integrating-target-with-mac/a4t/assets/debugger.png)

Se nella chiamata [!DNL Target] non è presente alcun ID di dati supplementare, verifica che il file [!DNL VisitorAPI.js] sia stato caricato prima di [!DNL at.js]. Se nella chiamata di [!DNL Analytics] non è presente alcun ID di dati supplementare, verifica che la chiamata di [!DNL Target] venga attivata prima della chiamata di [!DNL Analytics].

Per ulteriori informazioni, consulta [Implementazione di Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md#concept_CE78750AC2A4487D8ACD9369B3EAC85A) o contatta l’[Assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).
