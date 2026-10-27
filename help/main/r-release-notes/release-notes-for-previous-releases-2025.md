---
keywords: Note sulla versione;note sulla versione prerelease;miglioramenti futuri;correzioni future;funzioni future;prossima versione
description: Visualizza un elenco di funzioni, miglioramenti e correzioni inclusi nelle versioni precedenti di Adobe Target.
title: Quali funzioni sono incluse nelle versioni precedenti del 2025?
feature: Release Notes
TQID: 'https://experienceleague.adobe.com/cjheajZKokzwCNspfQckh6PHh5ecetdj7vZrrq9IqXw'
source-git-commit: 7f111df77c4b368dbe000a699ee19f5ff1ea266f
workflow-type: tm+mt
source-wordcount: '25402'
ht-degree: 5%
---
# Note sulla versione per le versioni precedenti

Note sulle versioni precedenti di [!DNL Adobe Target], incluse le note di rilascio per [!DNL Target Standard/Premium], la piattaforma [!DNL Target] e le librerie JavaScript (at.js) di [!DNL Target].

Le note sulla versione sono elencate in ordine decrescente per mese e anno di rilascio.

>[!NOTE]
>
>Consulta [Note sulla versione di Target (corrente)](/help/main/r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A) per informazioni sulle versioni di Target del mese corrente (piattaforma e Target Standard/Premium).

## Note sulla versione - 2025

### [!DNL Target Standard/Premium] 25.11.2 (14 novembre 2025)

**Offerte decisionali**

+++Vedi i dettagli

* **Decisioni di offerta con selettori nascosti o non validi non modificabili nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell’interfaccia utente aggiornata a causa del quale non era possibile modificare le decisioni sulle offerte associate a selettori nascosti o non validi, a meno che l’elemento non fosse visibile nel Compositore esperienza visivo. La modifica è ora supportata direttamente dal pannello, ripristinando le funzionalità disponibili nell’interfaccia utente legacy e garantendo che le decisioni sulle offerte possano essere modificate indipendentemente dalla visibilità del selettore. (TGT-53899)

+++

**Funzione Consigli**

+++Vedi i dettagli

* **La modifica dei criteri in un&#39;attività ha causato l&#39;arresto anomalo della pagina.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale la modifica dei criteri delle attività causava l&#39;arresto anomalo della pagina con errori della console relativi a `useCrudActionsCtx`. L’editor dei criteri ora carica e funziona correttamente, garantendo che le attività possano essere modificate senza interruzioni. (TGT-53971)
* La colonna **[!UICONTROL Messaggio] non è riuscita a intermittenza a visualizzare i dati dei prodotti nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata di [!UICONTROL Recommendations] a causa del quale la colonna [!UICONTROL Message] in [!UICONTROL Ricerca nel catalogo] non visualizzava in modo intermittente i dati del prodotto, anche se nel feed erano presenti valori. La colonna ora mostra in modo coerente i valori dei messaggi corretti in tutti i prodotti, garantendo una visibilità affidabile senza richiedere la riconfigurazione manuale delle colonne. (TGT-52777)
* **[!UICONTROL Il pulsante Scarica dati consigli] non è visibile dopo il salvataggio dell&#39;attività nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale il pulsante [!UICONTROL Scarica dati consigli] non veniva visualizzato per alcune attività salvate, anche dopo il nuovo salvataggio. Il pulsante ora viene visualizzato in modo coerente in tutte le attività, garantendo agli utenti di esportare in modo affidabile i dati dei consigli senza dover ricorrere a soluzioni alternative. (TGT-53802)
* **L&#39;apertura di alcuni prodotti da una raccolta ha restituito &quot;Impossibile trovare la risorsa richiesta&quot; e la finestra modale non aveva un&#39;opzione di chiusura.** È stato risolto un problema nell’interfaccia utente Recommendations aggiornata a causa del quale l’apertura di alcuni prodotti da una raccolta causava un errore di tipo &quot;Impossibile trovare la risorsa richiesta&quot; e mostrava un modale vuoto senza un’opzione di chiusura. La finestra modale ora carica correttamente i dettagli del prodotto ed è sempre disponibile un’opzione di chiusura per uscire correttamente. (TGT-53986)

+++

## [!DNL Target Standard/Premium] 25.11.1 (10 novembre 2025)


**Analytics for Target (A4T)**

+++Vedi i dettagli

* **[!UICONTROL Messaggio di errore Obiettivi e impostazioni] quando si utilizza [!DNL Adobe Analytics] come origine per la generazione di rapporti nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata di [!UICONTROL Panoramica] a causa del quale nella sezione Obiettivi veniva visualizzato l&#39;errore &quot;Si è verificato un errore. Impossibile completare la richiesta. Contattare [!DNL Adobe Client Care] se il problema persiste&quot; quando [!DNL Adobe Analytics] (A4T) è stato selezionato come origine per la generazione di rapporti. Gli obiettivi ora vengono visualizzati correttamente con le metriche [!UICONTROL Adobe Analytics], garantendo una visibilità coerente tra le origini di reporting. (TGT-54021)

+++

**Tipi di pubblico**

+++Vedi i dettagli

* **Impossibile selezionare più tipi di pubblico per reportistica nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell’interfaccia utente aggiornata a causa del quale gli utenti non potevano selezionare più tipi di pubblico di reporting appena creati contemporaneamente durante la modifica di un’attività. È ora possibile assegnare più tipi di pubblico contemporaneamente, migliorando la flessibilità e l’efficienza nella configurazione del reporting. (TGT-53253)

+++

**Offerte decisionali**

+++Vedi i dettagli

* **Impossibile modificare o sostituire le offerte di decisioning nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale non era possibile modificare o sostituire le offerte di decisioning tramite il pannello [!UICONTROL Modifiche] e i nomi delle offerte venivano visualizzati vuoti. Le offerte Decisioning sono ora completamente accessibili e modificabili, ripristinando la parità con l’interfaccia utente legacy e garantendo che i clienti possano gestirle direttamente all’interno delle attività. (TGT-53884)

+++

**Localizzazione**

+++Vedi i dettagli

* **Sono stati corretti diversi errori di localizzazione nell&#39;interfaccia utente coreana e giapponese.** (TGT-54003, TGT-54004, TGT-54006, TGT-54007 E TGT-54018)

+++

**[!UICONTROL Funzione Consigli]**

+++Vedi i dettagli

* **La promozione per attributo con corrispondenza attributo entità non è riuscita a caricare la chiave dei consigli dopo il salvataggio dell&#39;attività.** È stato risolto un problema a causa del quale le promozioni di tipo [!UICONTROL Promozione per attributo] con tipo di regola [!UICONTROL Corrispondenza attributo entità] non caricavano la chiave di consiglio quando veniva modificata dopo il salvataggio di un&#39;attività. Il problema è stato causato dalla mancata richiesta di `customKeyId` tramite GraphQL. Le chiavi di consiglio ora vengono caricate correttamente durante le modifiche di promozione. (TGT-53117)
* **Il consiglio persiste visivamente quando si passa da ExpB a ExpA.** È stato risolto un problema a causa del quale l’inserimento di un consiglio nell’Esperienza B e il successivo passaggio all’Esperienza A lasciavano visibile la casella delle offerte di consigli. Questa era solo un’incoerenza visiva; le modifiche ora vengono riprodotte correttamente quando si passa da un’esperienza all’altra, garantendo un comportamento accurato dell’interfaccia utente. (TGT-53911)
* **Chiave consiglio non caricata per [!UICONTROL Promozione per attributo] con [!UICONTROL Corrispondenza attributo entità].** È stato risolto un problema a causa del quale le promozioni di tipo [!UICONTROL Promozione per attributo] con tipo di regola [!UICONTROL Corrispondenza attributo entità] non caricavano la chiave di consiglio quando veniva modificata dopo il salvataggio di un&#39;attività. La chiave dei consigli ora viene recuperata correttamente tramite GraphQL, garantendo così la visualizzazione delle promozioni e il funzionamento previsto. (TGT-53917)
* **La modifica di consigli su elementi HTML nascosti non funziona nell&#39;interfaccia utente aggiornata.** È stato risolto un problema in [!UICONTROL Nuova creazione] e nell&#39;interfaccia utente del Compositore esperienza visivo a causa del quale non era possibile modificare le attività Consigli applicate agli elementi HTML nascosti. Questa funzionalità ora funziona come previsto, ripristinando la parità con l’interfaccia utente legacy e garantendo che i consigli possano essere modificati indipendentemente dalla visibilità degli elementi. (TGT-53953)
* **Impossibile modificare le attività di consigli sugli elementi HTML nascosti nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell’interfaccia utente aggiornata a causa del quale non era possibile modificare le attività Consigli applicate agli elementi HTML nascosti. Questa funzionalità ora funziona come previsto, ripristinando la parità con l’interfaccia utente legacy e garantendo che i consigli possano essere modificati indipendentemente dalla visibilità degli elementi. (TGT-53951)
* **Nel catalogo dei consigli mancano a intermittenza valori di attributi nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata di [!UICONTROL Recommendations] a causa del quale gli elenchi di ricerca nel catalogo non riuscivano a intermittenza a visualizzare alcuni valori di attributi (ad esempio, un messaggio) anche quando sono presenti nel feed del prodotto. I valori degli attributi ora vengono caricati in modo coerente nei risultati di ricerca senza richiedere la riconfigurazione delle colonne, migliorando l’affidabilità e l’efficienza per la gestione del catalogo. (TGT-52769)
* **[!UICONTROL Pulsante Scarica consigli] mancante per le attività [!DNL Recommendations] nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente [!DNL Recommendations] aggiornata a causa del quale il pulsante [!UICONTROL Scarica consigli] non era visibile per le attività A/B che utilizzavano i consigli. Il pulsante ora viene visualizzato correttamente, consentendo agli utenti di esportare i dati dei consigli come previsto, in linea con le funzionalità nell’interfaccia utente legacy. (TGT-53768)
* **[!UICONTROL Pulsante Scarica dati consigli] mancante nell&#39;interfaccia utente della panoramica aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata di [!UICONTROL Panoramica] a causa del quale il pulsante [!UICONTROL Scarica dati consigli] non era visibile per le attività contenenti consigli. Il pulsante ora viene visualizzato correttamente, garantendo che gli utenti possano esportare direttamente i dati dei consigli senza dover tornare all’interfaccia utente legacy. (TGT-53772)
* **La modifica dei criteri di attività a volte causava la visualizzazione di una schermata vuota nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale, se si faceva clic su [!UICONTROL Modifica criteri in esperienze], veniva occasionalmente visualizzata una schermata vuota per alcune attività. L’editor dei criteri ora viene caricato in modo affidabile in tutte le attività, garantendo agli utenti la possibilità di modificare senza interruzioni. (TGT-53961)
* **Impossibile modificare i criteri di sequenza nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale il tentativo di modificare [!UICONTROL i criteri di sequenza] causava il blocco della finestra a comparsa dei criteri durante il caricamento e la visualizzazione di una schermata vuota. L’editor dei criteri ora viene caricato correttamente, consentendo agli utenti di modificare e aggiornare i criteri della sequenza senza interruzioni. (TGT-53985)

+++

**[!UICONTROL Rapporti]**

+++Vedi i dettagli

* **[!UICONTROL Le posizioni di Test multivariato] (MVT) e il problema di reporting del grafico hanno impedito la generazione del rapporto.** È stato risolto un problema che impediva alle attività MVT di generare i rapporti [!UICONTROL Contributo posizione] e Grafico nell&#39;interfaccia utente di Target, causando la visualizzazione dell&#39;errore &quot;Si è verificato un errore. Non possiamo completare la tua richiesta.&quot; I rapporti ora vengono caricati correttamente nell’interfaccia utente, garantendo piena visibilità. (TGT-53654)
* **Impossibile caricare i report MVT a causa di un errore del report [!UICONTROL Elemento].** È stato risolto un problema che impediva il caricamento dei rapporti attività MVT nell’interfaccia utente di Target, causando la visualizzazione dell’errore &quot;Impossibile recuperare il rapporto sul contributo degli elementi&quot;. I rapporti ora vengono visualizzati correttamente, garantendo la piena visibilità dei contributi degli elementi. (TGT-53691)
* **Esporta i dettagli dell&#39;ordine in problema CSV per [!UICONTROL attività Targeting esperienza] (XT).** È stato risolto un problema a causa del quale l&#39;opzione [!UICONTROL Esporta dettagli ordine in CSV] non veniva visualizzata correttamente per le attività XT e restituiva un file vuoto. L’opzione ora viene visualizzata solo per le attività di Personalizzazione automatizzata, garantendo funzionalità di esportazione accurate e evitando confusione. (TGT-53798)

+++

**[!UICONTROL Compositore esperienza visivo] (VEC)**

+++Vedi i dettagli

* **[!UICONTROL Il problema del pulsante Elimina modifica] ha impedito la rimozione delle modifiche dell&#39;attività.** È stato risolto un problema a causa del quale il pulsante [!UICONTROL Elimina modifica] nell&#39;interfaccia utente [!DNL Target] non funzionava, impedendo agli utenti di rimuovere le modifiche all&#39;interno delle attività. Il pulsante ora funziona come previsto, consentendo la cancellazione delle modifiche in modo affidabile e senza ritardi. (TGT-53728)
* **I selettori preferiti non sono riconosciuti nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale i selettori preferiti, ad esempio `data-target-component-id`, non venivano visualizzati nell&#39;elenco dei selettori CSS nel Compositore esperienza visivo. Gli utenti possono ora selezionare in modo affidabile gli attributi preferiti invece dei nomi di classe generati in modo dinamico, garantendo un targeting stabile tra gli aggiornamenti della pagina delle applicazioni a pagina singola. (TGT-53908)
* **Allineamento posizione attività non corrispondente tra [!UICONTROL Modifica] e [!UICONTROL Panoramica] pagine.** È stato risolto un problema che impediva l&#39;allineamento della numerazione dei percorsi delle attività nella pagina [!UICONTROL Panoramica] con gli aggiornamenti apportati nella pagina[!UICONTROL &#x200B; Modifica esperienza]. Le posizioni ora rimangono coerenti tra le due viste, garantendo un allineamento accurato ed evitando posizioni mancanti o con numeri errati. (TGT-53960 e TGT-53954)
* **Impossibile tornare alla modalità [!UICONTROL Progettazione] nel Compositore esperienza visivo aggiornato** È stato risolto un problema nell&#39;interfaccia utente del Compositore esperienza visivo aggiornata a causa del quale gli utenti non potevano tornare alla modalità [!UICONTROL Progettazione] dopo essere passati a una nuova pagina in modalità [!UICONTROL Sfoglia]. L&#39;interruttore [!UICONTROL Progettazione] ora funziona correttamente, consentendo l&#39;applicazione delle modifiche direttamente tra le pagine. (TGT-53988 e TGT-53993)
* **Parametro query non visualizzato nella panoramica attività.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale i parametri di query non venivano visualizzati nella pagina [!UICONTROL Panoramica] per le attività, causando discrepanze tra la [!UICONTROL Panoramica] e gli URL di consegna della pagina. I parametri di query ora vengono visualizzati correttamente, garantendo che le posizioni delle attività siano completamente rappresentate e coerenti tra le viste. (TGT-53701)

+++

### [!DNL Target Standard/Premium] 25.10.1 (22 ottobre 2025)

Questa versione include i seguenti aggiornamenti e correzioni:

**Attività**

+++ Vedi i dettagli
* **È stato risolto un problema di usabilità nell&#39;interfaccia utente aggiornata**. [!UICONTROL Gli osservatori] ora possono visualizzare in anteprima le attività utilizzando l&#39;opzione [!UICONTROL Visualizza attività], proprio come nell&#39;interfaccia utente legacy. (TGT-51741)
* **[!UICONTROL Gli utenti dell&#39;osservatore] possono ora visualizzare il contenuto delle attività nell&#39;interfaccia utente aggiornata.** È stata ripristinata la visibilità per gli utenti del ruolo Osservatore nell’interfaccia utente aggiornata dell’attività. In precedenza, gli osservatori non erano in grado di visualizzare modifiche, offerte e modifiche al contenuto, funzionalità disponibile nell’interfaccia utente legacy. (TGT-53785)
* **[!UICONTROL L&#39;approvatore] ora gli utenti possono modificare gli obiettivi dell&#39;attività senza l&#39;errore di privilegio dell&#39;editor.** È stato risolto un problema di autorizzazioni nell&#39;interfaccia utente di Creazione attività che impediva agli utenti a livello di Approvatore di salvare le modifiche alle impostazioni avanzate dell&#39;obiettivo. Gli utenti interessati hanno ricevuto un errore `403 Forbidden.Resource` che richiede i privilegi dell&#39;editor, pur disponendo di un accesso sufficiente. (TGT-53819)

+++

**Tipi di pubblico**

+++Vedi i dettagli

* **Selezione di più tipi di pubblico ripristinata nel reporting &quot;Solo questa attività&quot;.** È stato risolto un problema nell&#39;interfaccia utente di creazione attività che impediva agli utenti di selezionare più tipi di pubblico nella sezione [!UICONTROL Solo questa attività] in [!UICONTROL Obiettivi e impostazioni]. (TGT-53283)
* **I grafici di reporting basati sul pubblico ora visualizzano correttamente i dati di conversione.** È stato risolto un problema nella scheda [!UICONTROL Rapporti] che causava errori nei grafici durante la selezione di tipi di pubblico non predefiniti. Anche se i dati e le metriche di affidabilità erano disponibili, il grafico visivo mostrava solo una linea continua, rendendo l’analisi difficile. (TGT-53769)
* **L&#39;interfaccia utente [!UICONTROL Targeting] indica chiaramente le regole del pubblico escluse.** È stato risolto un problema nella sezione [!UICONTROL Targeting] dell&#39;interfaccia utente di creazione attività in cui le regole del pubblico impostate su [!UICONTROL Escludi] non venivano visualizzate chiaramente. Ciò ha portato a confusione durante la revisione della logica di targeting, in particolare per i tipi di pubblico che escludevano URL specifici. (TGT-53809)
* **I valori di definizione del pubblico ora sono selezionabili e copiabili nella scheda [!UICONTROL Targeting].** È stato risolto un problema nell&#39;interfaccia di Creazione attività che impediva agli utenti di selezionare e copiare i valori delle regole del pubblico nella scheda [!UICONTROL Targeting]. Questa funzionalità era disponibile nell’interfaccia utente legacy ma non nell’interfaccia utente aggiornata. (TGT-53856)

+++

**Localizzazione**

+++Vedi i dettagli

* **Corretta traduzione errata di &quot;quote&quot; nel contesto dell&#39;editor pagina zh_CN.** È stato corretto un errore di traduzione contestuale nella lingua zh_CN in cui il termine &quot;preventivo&quot; veniva tradotto in modo inesatto come &quot;报价&quot;, implicando un prezzo commerciale. Nella sezione Composizione tipografica > Stile intestazione > Virgolette, il significato desiderato si riferisce a un elemento di formattazione, ovvero un blocco di quotazione, e non alla determinazione dei prezzi. (TGT-53841)
* **Correzione della traduzione errata di &quot;virgolette rimosse&quot; nel contesto dell&#39;editor pagina zh_CN.** È stato corretto un errore di traduzione nella lingua zh_CN in cui &quot;citazione rimossa&quot; veniva erroneamente visualizzato come &quot;移除了报价&quot;, implicando un prezzo commerciale. Nella sezione Composizione tipografica > Stile intestazione > Citazioni bloccate, il termine si riferisce a un elemento di formattazione, ovvero un blocco di quotazione, e non alla determinazione del prezzo. (TGT-53843)
* **Correzione della traduzione errata di &quot;virgolette ridisposte&quot; nel contesto dell&#39;editor pagina zh_CN.** È stato corretto un errore di traduzione contestuale nelle impostazioni locali zh_CN in cui le &quot;quotazioni riorganizzate&quot; venivano inaccuratamente tradotte come &quot;重新排列了报价&quot;, il che implicava un prezzo commerciale. Nella sezione Composizione tipografica > Stile intestazione > Citazioni bloccate, il termine si riferisce a un elemento di formattazione, ovvero un blocco di quotazione, e non alla determinazione del prezzo. (TGT-53844)
* **Correzione della traduzione errata di &quot;virgolette modificate&quot; nel contesto dell&#39;editor pagina zh_CN.** È stato corretto un errore di traduzione nella lingua zh_CN in cui &quot;quote modificate&quot; veniva erroneamente visualizzato come &quot;更改了报价&quot;, suggerendo un prezzo commerciale. Nella sezione Composizione tipografica > Stile intestazione > Citazioni bloccate, il termine si riferisce a un elemento di formattazione, ovvero un blocco di quotazione, e non alla determinazione del prezzo. (TGT-53845)

+++

**Funzione Consigli**

+++Vedi i dettagli

* **Le modifiche del selettore CSS per i consigli ora vengono salvate correttamente.** È stato risolto un problema nell’interfaccia utente di Creazione attività che impediva agli utenti di aggiornare il selettore CSS per i posizionamenti dei consigli. Le modifiche sono state ripristinate dopo il salvataggio, bloccando gli aggiornamenti ai contenitori di targeting. (TGT-53835)
* **La selezione dell&#39;evento di caricamento pagina ora persiste nelle modifiche dei consigli.** È stato risolto un problema nell&#39;interfaccia utente di creazione attività che impediva agli utenti di salvare le modifiche quando cambiavano il tipo di evento di un consiglio da [!UICONTROL Visualizza] a [!UICONTROL Caricamento pagina]. Anche se la selezione sembrava riuscita, è tornata dopo essere uscita, bloccando la pubblicazione dell’attività. (TGT-53957)

+++

**Rapporti**

+++Vedi i dettagli

* **&quot;[!UICONTROL Esporta i dettagli dell&#39;ordine in CSV]&quot; ora scarica i dati completi.** È stato risolto un problema nell&#39;interfaccia utente aggiornata di [!UICONTROL Panoramica] a causa del quale l&#39;opzione &quot;[!UICONTROL Esporta dettagli ordine in CSV]&quot; scaricava file vuoti, anche quando erano presenti dati di report validi. (TGT-53787)

+++

**Sicurezza**

+++Vedi i dettagli

* **È stato aggiunto il prefiltro IMS per proteggere gli endpoint GQL dall&#39;esposizione di dati tra organizzazioni diverse.** È stata risolta una vulnerabilità di sicurezza nella scheda Amministratore che interessava gli endpoint di GraphQL licenseGroups e targetProperties. Il problema è stato causato dall’utilizzo dell’API JIL con un token client amministratore che poteva essere sfruttato per accedere ai dati di prodotto tra organizzazioni diverse. (TGT-53837)

+++

**Compositore esperienza visivo**

+++Vedi i dettagli

* **Stabilità di authoring ripristinata nell&#39;interfaccia utente di creazione attività.** È stato risolto un problema intermittente nell’interfaccia utente del Compositore esperienza visivo che impediva l’authoring e rendeva i collegamenti selezionabili in modo imprevisto, con reindirizzamento degli utenti fuori dalla pagina. (TGT-53153)
* **Modifica ripristinata per le attività salvate nell&#39;interfaccia utente di creazione attività.** È stato risolto un problema che impediva agli utenti di modificare le attività dopo il salvataggio delle modifiche. Le attività interessate sono rimaste bloccate in &quot;[!UICONTROL Applicazione delle modifiche iniziali]&quot;, bloccando ulteriori aggiornamenti e nascondendo il pulsante [!UICONTROL Annulla]. (TGT-53631)
* **Il Compositore esperienza visivo non si blocca più su &quot;[!UICONTROL Applicazione delle modifiche iniziali].&quot;** È stato risolto un problema di prestazioni nel Compositore esperienza visivo che causava lunghi ritardi durante il caricamento di esperienze con un numero elevato di modifiche. Gli utenti interessati hanno visto l&#39;interfaccia utente bloccata in &quot;[!UICONTROL Applicazione delle modifiche iniziali]&quot; per alcuni minuti, soprattutto negli scenari dell&#39;esperienza B. (TGT-53727)
* **Il Compositore esperienza visivo carica le modifiche senza elementi radice.**
È stato risolto un problema nel Compositore esperienza visivo che causava l&#39;arresto delle esperienze durante il caricamento di modifiche prive di un elemento principale chiaro. In precedenza, a causa di queste modifiche, l&#39;interfaccia utente si bloccava indefinitamente su &quot;A[!UICONTROL applicazione delle modifiche iniziali]&quot;. (TGT-53799)
* **Il salvataggio delle modifiche nelle attività ora funziona come previsto.** È stato risolto un problema relativo alle autorizzazioni nella nuova interfaccia utente di creazione che impediva agli utenti di salvare le modifiche durante la modifica degli obiettivi e delle impostazioni avanzate nelle attività. Gli utenti interessati hanno visualizzato una barra multifunzione di errore rossa e un messaggio &quot;Forbidden.Resource&quot;, pur disponendo dell’accesso appropriato. (TGT-53816)
* **L&#39;interfaccia utente del Compositore esperienza visivo mantiene le modifiche dell&#39;esperienza in tutte le visualizzazioni.** Sono stati risolti diversi problemi nel Compositore esperienza visivo aggiornato che hanno interessato lo sviluppo dell’esperienza. Le modifiche non persistevano correttamente, soprattutto quando si utilizzavano le offerte HTML o si passava da una visualizzazione all’altra. (TGT-53825)
* **Tutte le visualizzazioni ora vengono visualizzate correttamente quando una modifica si estende su più esperienze.** È stato risolto un problema nell&#39;interfaccia utente di Creazione attività a causa del quale veniva visualizzata una sola visualizzazione quando veniva applicata una modifica tra più visualizzazioni. La descrizione del passaggio del mouse non elencava tutte le viste associate, anche se la modifica era stata applicata correttamente. (TGT-53827)
* **Il Compositore esperienza visivo non si arresta più in modo intermittente su &quot;[!UICONTROL Applicazione delle modifiche iniziali].&quot;** È stato risolto un problema intermittente nel Compositore esperienza visivo a causa del quale le esperienze non venivano caricate correttamente e rimanevano bloccate in &quot;[!UICONTROL Applicazione delle modifiche iniziali].&quot; Questo comportamento era incoerente e talvolta attivava loop di reindirizzamento o richiedeva la cancellazione manuale della cache. (TGT-53916)
* **Impossibile riprodurre il problema di caricamento del Compositore esperienza visivo.** Abbiamo esaminato un problema segnalato in cui il Compositore esperienza visivo rimaneva bloccato su &quot;[!UICONTROL Applicazione delle modifiche iniziali]&quot; durante la modifica di attività esistenti. Si sospettava che il comportamento fosse correlato al contenuto HTML privo di un elemento principale. Continueremo a monitorare la ricorrenza e consiglieremo di utilizzare contenitori strutturati per le offerte HTML per garantire la stabilità. (TGT-53972)
* La modalità **[!UICONTROL Progettazione] nel Compositore esperienza visivo non si comporta più come la modalità [!UICONTROL Sfoglia] in modo intermittente.** È stato risolto un problema nell&#39;interfaccia utente a causa del quale la modalità [!UICONTROL Progettazione] si comportava in modo intermittente come la modalità [!UICONTROL Sfoglia], consentendo collegamenti `<a>` cliccabili e impedendo la selezione di elementi. Questo causava la scomparsa della casella di passaggio del mouse e bloccava i flussi di lavoro di modifica. (TGT-53136)
* **I clic dei pulsanti in modalità [!UICONTROL Compositore] non attivano più il reindirizzamento delle pagine.** È stato risolto un problema nell&#39;interfaccia utente del Compositore esperienza visivo aggiornata a causa del quale facendo clic su un pulsante in modalità [!UICONTROL Compositore] si verificava un reindirizzamento imprevisto all&#39;URL di destinazione del pulsante. Questo impediva agli utenti di modificare elementi di call-to-action (CTA) e interrompeva il flusso di lavoro di authoring. (TGT-53137)
* **Gli aggiornamenti del codice offerta nelle attività di personalizzazione automatizzata ora vengono salvati senza errori.** È stato risolto un problema nella nuova interfaccia utente di creazione che causava un errore &quot;[!UICONTROL Input utente non valido]&quot; durante l&#39;aggiornamento del codice offerta nelle attività [!UICONTROL Automated Personalization]. L’errore ha impedito agli utenti di salvare le modifiche, anche quando l’input era valido. (TGT-53586)
* La modalità **[!UICONTROL Progettazione] nel Compositore esperienza visivo ora blocca la navigazione dei collegamenti per i componenti modificabili.** È stato risolto un problema nel Compositore esperienza visivo aggiornato a causa del quale gli elementi selezionabili, come pulsanti e collegamenti, attivavano il reindirizzamento delle pagine anche in modalità [!UICONTROL Progettazione]. Questo comportamento simula la modalità [!UICONTROL Sfoglia] e impedisce agli utenti di modificare i componenti chiave. (TGT-53696)
* La metrica **&quot;[!UICONTROL Selezionata da un elemento]&quot; ora funziona senza reindirizzamento o errore.** È stato risolto un problema nella nuova interfaccia utente di creazione che causava reindirizzamenti imprevisti e schermate vuote durante la selezione della metrica di conversione &quot;[!UICONTROL Clic su un elemento]&quot;. Facendo clic su un pulsante durante l&#39;installazione è stata attivata la navigazione invece di registrare l&#39;elemento, con conseguente errore &quot;[!UICONTROL elemento non trovato]&quot;. (TGT-53817)
* **Le attività esistenti non si bloccano più in un ciclo di caricamento infinito durante la modifica.** È stato risolto un problema nella nuova interfaccia utente di creazione a causa del quale la modifica di un’attività esistente nel Compositore esperienza visivo rimaneva bloccata in un ciclo di caricamento infinito. Questo problema non ha interessato le attività appena create ed è stato attivato da modifiche preesistenti sulla pagina. (TGT-53913)
* **Le pagine di attività esistenti con modifiche ora vengono caricate correttamente nel Compositore esperienza visivo** È stato risolto un problema nel Compositore esperienza visivo aggiornato che causava il blocco delle pagine nella fase di caricamento durante la modifica di un’attività esistente con modifiche salvate. Nuove attività caricate senza problema, ma il rendering delle attività configurate in precedenza non è riuscito. (TGT-53967)

+++

### [!DNL Target Standard/Premium] 25.9.3 (30 settembre 2025)

Questa versione include i miglioramenti e le correzioni seguenti.

+++[!UICONTROL Tipi di pubblico]

* **Le regole di esclusione del pubblico non sono state visualizzate correttamente come inclusione nell&#39;interfaccia utente di [!DNL Target].** I tipi di pubblico configurati con regole di esclusione venivano visualizzati come inclusi durante la modifica del targeting all’interno di un’attività. Anche se la logica di esclusione è stata applicata correttamente durante l’esecuzione, l’interfaccia utente non è riuscita a riflettere la regola in modo preciso, omettendo l’etichetta &quot;esclusione&quot;. L&#39;interfaccia utente di [!DNL Target] visualizza ora correttamente le regole di esclusione sia nella configurazione del pubblico che nei flussi di lavoro di targeting, garantendo chiarezza e coerenza per la configurazione della campagna. (TGT-53808)
* **La sezione [!UICONTROL Targeting] non indica che una regola di pubblico è stata impostata per l&#39;esclusione.** I tipi di pubblico configurati con logica di esclusione non venivano visualizzati correttamente come inclusione nella sezione [!UICONTROL Targeting] dell&#39;interfaccia utente per la creazione di attività. Sebbene il backend abbia applicato correttamente la regola di esclusione, l’interfaccia utente non è riuscita a rappresentarla visivamente, omettendo l’etichetta &quot;Escludi&quot; e creando confusione durante la configurazione della campagna. Nella sezione [!UICONTROL Targeting] sono ora visualizzate chiaramente le regole di esclusione, garantendo la coerenza tra la configurazione del pubblico e la visualizzazione del targeting. (TGT-53809)

+++

+++Localizzazione

* **È stata risolta un&#39;incoerenza terminologica nella traduzione in cinese semplificato della visualizzazione Dettagli completi.**
In precedenza, il termine &quot;Dettagli&quot; veniva erroneamente tradotto come &quot;详情&quot; nella lingua cinese semplificato (zh_CN), violando le linee guida terminologiche stabilite. Questo è stato corretto in &quot;详细信息&quot; per garantire la coerenza con il database terminologico. (TGT-53741)

+++

+++[!UICONTROL Funzione Consigli]

* **Impossibile individuare e selezionare le caselle dei consigli nel Compositore esperienza visivo** Dopo aver aggiunto un’offerta di consigli nel (VEC), facendo clic sulla modifica nel pannello a sinistra non veniva evidenziata né scorreva la casella corrispondente dei consigli nella pagina. Questo rendeva difficile individuare e modificare l’offerta, soprattutto se nascosta sotto i selettori o con uno stile minimo. Facendo clic su una modifica dei consigli, ora viene evidenziato e scorre correttamente l’elemento associato, migliorando l’usabilità e l’efficienza nella modifica del processo aggiornato di creazione delle attività. (TGT-52571)
* **I selettori di consigli non sono stati riscritti correttamente dopo il salvataggio di un&#39;attività.** Quando si aggiungeva un consiglio a un elemento nel Compositore esperienza visivo, il selettore era inizialmente corretto, ma dopo aver salvato e riaperto l’attività è diventato un selettore generico. I tentativi di ripristinare manualmente il selettore originale hanno generato errori di convalida. I selettori per consigli ora persistono accuratamente dopo il salvataggio, garantendo un targeting e una modificabilità affidabili nel processo aggiornato di creazione delle attività. (TGT-53709)
* **Impossibile modificare il contenuto dei criteri durante la modifica di un&#39;attività esistente.** Durante la modifica di un&#39;attività, la sezione del contenuto [!UICONTROL Criteri] è apparsa disabilitata, con i pulsanti disattivati e non rispondenti. Questo problema è stato risolto assicurandosi che le configurazioni di [!UICONTROL Criteri] siano completamente modificabili durante gli aggiornamenti dell&#39;attività. I clienti possono ora modificare il contenuto di [!UICONTROL Criteri] senza dover cambiare le selezioni o utilizzare soluzioni alternative, migliorando la flessibilità e l&#39;usabilità nel processo di creazione attività aggiornato. (TGT-53812)
* **Impossibile modificare i criteri all&#39;interno di un&#39;attività.** Le opzioni [!UICONTROL Modifica criterio]e [!UICONTROL Rimuovi criterio] sono state disabilitate durante l&#39;accesso ai criteri da un&#39;attività. Tuttavia, è possibile modificare gli stessi criteri tramite la scheda [!UICONTROL Recommendations]. I criteri sono ora completamente modificabili sia dal flusso di lavoro di modifica delle attività che dalla scheda [!UICONTROL Consigli], garantendo un&#39;esperienza di modifica coerente ed efficiente. (TGT-53814)

+++

+++[!UICONTROL Rapporti]

* **La generazione di offerte ad hoc nelle attività A[!UICONTROL automatizzate di Personalization] ha causato incongruenze nei rapporti.** L&#39;utilizzo della funzionalità Genera offerte ad hoc nelle attività di [!UICONTROL Automated Personalization] (AP) ha portato a rapporti non accurati. In particolare, gli ID offerta venivano riutilizzati tra le posizioni, causando l’erronea attribuzione o la sovrascrittura dei dati di reporting. Le offerte ad hoc ora vengono generate con identificatori distinti per posizione, garantendo un tracciamento e un reporting accurati per tutte le esperienze configurate. (TGT-53757)
* **Impossibile caricare i report attività a causa di un errore di JavaScript.** I clienti hanno riscontrato un messaggio di errore durante l&#39;accesso alla scheda [!UICONTROL Report] per alcune attività. L&#39;errore è stato causato da un&#39;eccezione JavaScript: impossibile leggere le proprietà di non definito (lettura di &#39;indexOf&#39;), attivato durante la chiamata GraphQL `getAnalyticsReportSummary`. I rapporti ora vengono caricati correttamente e la gestione degli errori è stata migliorata per evitare errori simili nel flusso di lavoro aggiornato per la creazione di attività. (TGT-53797)
* **Si è verificato un arresto anomalo dei report dopo l&#39;interazione con la barra di scorrimento.** Facendo clic sulla barra di scorrimento nella scheda [!UICONTROL Rapporti] si è verificato un arresto anomalo della pagina, accompagnato da un errore di JavaScript:
  `SyntaxError: Failed to execute 'querySelector' on 'Element': '[data-key="a-currentcopy"hiretalent""]' is not a valid selector.` I report ora vengono caricati e scorrono correttamente senza generare errori o arresti anomali. (TGT-53828)
* **Nei report non è stata visualizzata la metrica principale.** La metrica principale, configurata come metrica di conversione utilizzando una mbox, era mancante nei rapporti delle attività. La ricerca per nome metrica o nome mbox non ha prodotto risultati, impedendo la visibilità nei dati delle prestazioni chiave. Le metriche primarie ora vengono visualizzate correttamente nella scheda [!UICONTROL Rapporti], garantendo un tracciamento e un&#39;analisi accurati delle prestazioni della campagna. (TGT-53773)
* **La scheda [!UICONTROL Rapporti] nell&#39;interfaccia utente aggiornata si è bloccata durante l&#39;interazione con la barra di scorrimento orizzontale.** Si è verificato un arresto anomalo della visualizzazione [!UICONTROL Report] a intermittenza con un errore &quot;Si è verificato un errore&quot; quando si utilizza la barra di scorrimento orizzontale per accedere alle metriche fuori visualizzazione. La barra di scorrimento ora funziona in modo affidabile, consentendo ai clienti di visualizzare e analizzare tutte le metriche senza necessità di soluzioni quali ingrandire o utilizzare lo scorrimento con spostamento. (TGT-53824)

+++

+++[!UICONTROL Compositore esperienza visivo] (VEC)

* **Se si fa clic su breadcrumb nel Compositore esperienza visivo, il menu Modifica non veniva visualizzato in modo coerente.**
Quando si selezionano gli elementi di HTML tramite le breadcrumb nel Compositore esperienza visivo, il menu Modifica a intermittenza non viene visualizzato o scompare rapidamente, rendendo la selezione degli elementi inaffidabile. Il menu Modifica ora viene visualizzato in modo coerente quando si naviga tramite breadcrumb, migliorando il flusso di lavoro di selezione degli elementi nel processo aggiornato di creazione delle attività. (TGT-52873)
* **Impossibile visualizzare in modo intermittente il menu di scelta rapida nel Compositore esperienza visivo** Il menu di scelta rapida nell’interfaccia utente del Compositore esperienza visivo aggiornata non veniva visualizzato in modo coerente quando si faceva clic sugli elementi, rendendo difficile l’accesso alle opzioni di modifica. Il menu di scelta rapida ora viene visualizzato in modo affidabile sulla selezione degli elementi, migliorando il flusso di lavoro di modifica e l’usabilità complessiva nel processo aggiornato di creazione delle attività. (TGT-53015)
* **Impossibile visualizzare il menu di scelta rapida per alcuni elementi nel Compositore esperienza visivo** Il menu di scelta rapida non veniva visualizzato quando si selezionavano elementi specifici nel Compositore esperienza visivo aggiornato, rendendo difficile l’applicazione delle modifiche. Il menu di scelta rapida ora viene visualizzato in modo coerente per tutti gli elementi supportati, migliorando l’affidabilità e la facilità d’uso dell’esperienza di modifica nel flusso di lavoro aggiornato per la creazione di attività. (TGT-53248)
* **Il menu di scelta rapida è scomparso al primo clic quando si utilizzano breadcrumb nel Compositore esperienza visivo** Selezionando un elemento padre tramite le breadcrumb nel Compositore esperienza visivo, il menu di scelta rapida veniva visualizzato brevemente e poi scompariva, rendendo difficile l’accesso alle opzioni di modifica. Il menu di scelta rapida ora rimane visibile e funzionale durante la navigazione degli elementi attraverso le breadcrumb, migliorando l’affidabilità del flusso di lavoro di selezione degli elementi nel processo aggiornato di creazione delle attività. (TGT-53424)
* **Il menu di scelta rapida non è stato visualizzato per gli elementi di primo livello nel Compositore esperienza visivo** La selezione degli elementi di primo livello, ad esempio i tag `<div>` o `<main>`, tramite le breadcrumb nel Compositore esperienza visivo non ha attivato il menu di scelta rapida, impedendo ulteriori azioni di modifica. Il menu di scelta rapida ora viene visualizzato in modo coerente per tutti gli elementi supportati, inclusi i contenitori di primo livello, migliorando la flessibilità e l’usabilità del flusso di lavoro per la creazione di attività. (TGT-53770)
* **Impossibile modificare gli elementi in una pagina specifica nel Compositore esperienza visivo** Non è stato possibile selezionare o modificare alcuni elementi nella pagina nel Compositore esperienza visivo aggiornato. Questo problema era isolato in quella pagina e non interessava altre pagine all’interno dello stesso account. Tutti gli elementi della pagina ora sono selezionabili e modificabili come previsto, ripristinando la funzionalità completa nel flusso di lavoro per la creazione di attività. (TGT-53353)
* **È stato migliorato il flusso di lavoro durante la visualizzazione degli elementi figlio durante la selezione degli elementi nel Compositore esperienza visivo** Per migliorare l’usabilità e la precisione durante la creazione di attività, il Compositore esperienza visivo ora visualizza gli elementi secondari quando si passa il puntatore del mouse su un elemento HTML principale o lo si seleziona. Questo miglioramento consente ai clienti di comprendere meglio la struttura della pagina e apportare modifiche più precise, semplificando il flusso di lavoro di modifica nell’interfaccia utente aggiornata. (TGT-53416)
* **Impossibile modificare gli elementi nelle attività esistenti utilizzando la barra delle modifiche.** Durante la modifica delle attività create in precedenza, la barra di modifica non veniva attivata per alcuni elementi della pagina, impedendo gli aggiornamenti. Questo problema è stato osservato principalmente nelle attività modificate ed era difficile riprodurlo in quelle di nuova creazione. La barra di modifica ora mostra in modo coerente e consente di modificare tutti gli elementi supportati, migliorando l’affidabilità e la facilità d’uso nel flusso di lavoro aggiornato per la creazione di attività. (TGT-53013)

+++

+++[!UICONTROL Aree di lavoro]

* **La clonazione di un&#39;attività in un&#39;area di lavoro diversa ha generato un errore di tipo &quot;Input utente non valido&quot;.** Errore durante il tentativo di clonare un&#39;attività da un&#39;area di lavoro a un&#39;altra: &quot;InvalidProperty.Json - Nome di proprietà non riconosciuto &#39;content&#39;.&quot; Questo problema è stato causato da una gestione non corretta dei metadati dell’attività durante il processo di clonazione. È ora possibile clonare correttamente le attività in più aree di lavoro senza attivare errori di convalida, garantendo flussi di lavoro di distribuzione delle attività più fluidi. (TGT-53731 e TGT-53736)

+++

### [!DNL Target Standard/Premium] 25.9.2 (22 settembre 2025)

Questa versione include le seguenti correzioni e miglioramenti:

**[!UICONTROL Tipi di pubblico]**

+++Vedi i dettagli

* **È stato risolto un problema che impediva la copia delle attività a causa di ID di pubblico non validi.** I clienti che tentavano di copiare le attività nel processo di creazione attività aggiornato hanno riscontrato un errore causato da ID di pubblico non validi (ad esempio, -1752722444307). Questo problema di convalida del back-end impediva la duplicazione delle attività all’interno della stessa area di lavoro. Questo problema è stato risolto e le attività possono essere copiate correttamente senza errori relativi al pubblico. (TGT-53717)
* **È stato risolto un problema che causava la visualizzazione di errori di input utente non validi per i tipi di pubblico per sola attività nelle attività [!UICONTROL Automated Personalization] e nel modale [!UICONTROL Gestisci contenuto].** I clienti hanno riscontrato errori di input utente non validi durante la configurazione dei tipi di pubblico per sola attività nella finestra modale Gestione contenuto di  per le attività di Personalizzazione automatizzata. Questo problema si verificava nonostante il pubblico fosse stato precedentemente utilizzato correttamente. Le configurazioni del pubblico combinato ora vengono salvate correttamente senza attivare errori di convalida. (TGT-53749)

+++

**Documentazione**

+++Vedi i dettagli

* **Le pagine della documentazione di Web SDK specifiche di Target sono state spostate nell&#39;archivio Adobe Target.** Nell&#39;ambito della ristrutturazione della documentazione di Web SDK, è stata effettuata la migrazione del contenuto specifico di [!DNL Target] dai documenti generali di Web SDK alla [!DNL Adobe Target] [Guida per gli sviluppatori](https://experienceleague.adobe.com/it/docs/target-dev/developer/a4t/overview-a4t?lang=en){target=_blank}. Questa modifica migliora la reperibilità dei contenuti e garantisce che il team di prodotto appropriato mantenga le indicazioni specifiche per la soluzione. (TGT-53374)

+++

**[!UICONTROL Decisioni Di Offerta]**

+++Vedi i dettagli

* **L&#39;opzione Decisione offerta è ora visibile in modo coerente durante la creazione dell&#39;attività iniziale.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale l&#39;opzione [!UICONTROL Decisione offerta] non veniva visualizzata durante il primo flusso di creazione per le attività A/B, in particolare quando si accedeva in modalità in incognito ai tenant con Decisioni di offerta abilitati. L&#39;opzione è stata visualizzata solo dopo essere passati al passaggio [!UICONTROL Targeting] e essere tornati a [!UICONTROL Esperienze]. Questa correzione assicura che l&#39;opzione [!UICONTROL Decisione offerta] sia immediatamente disponibile durante la configurazione iniziale, migliorando l&#39;usabilità e riducendo la confusione. (TGT-51888)

+++

**[!UICONTROL Offerte]**

+++Vedi i dettagli

* **È stato risolto un problema a causa del quale le offerte di reindirizzamento non includevano `redirectOptions` nel payload quando `includeContent=true`.** Ai clienti che recuperavano offerte di reindirizzamento con `includeContent=true ` mancava il campo `redirectOptions` nel payload di risposta. Questa incoerenza ha interessato i flussi di lavoro, ad esempio la copia delle offerte e la creazione di attività. Le offerte di reindirizzamento ora includono correttamente `redirectOptions` quando il contenuto viene richiesto. (TGT-53737)

+++

**[!DNL Recommendations]**

+++Vedi i dettagli

* **Tracciamento dei clic ripristinato per le attività [!UICONTROL Recommendations] create nell&#39;interfaccia utente aggiornata.** È stato risolto un problema che impediva alle attività [!UICONTROL Recommendations] create nell&#39;interfaccia utente aggiornata di registrare il tracciamento dei clic, causando la mancata segnalazione di conversioni. Le attività create nell’interfaccia utente legacy hanno tracciato correttamente i clic e segnalato le conversioni come previsto. Questa correzione assicura che le attività Consigli create nell’interfaccia utente aggiornata includano ora gli attributi di tracciamento corretti, il ripristino dei rapporti di conversione e l’allineamento con le metriche A4T. (TGT-53287)
* **Tracciamento dei clic ripristinato per le attività Consigli.** È stato risolto un problema che impediva alle attività [!UICONTROL Recommendations] create nell&#39;interfaccia utente aggiornata di registrare il tracciamento dei clic, causando la mancata segnalazione di conversioni. L&#39;interfaccia utente legacy ha applicato correttamente un ID di tracciamento (`at-track-click`) al contenuto di [!UICONTROL Recommendations], mentre l&#39;interfaccia utente aggiornata ha inserito erroneamente un segnaposto (`__recsClickTrackIdPlaceholder__`), impedendo il tracciamento del back-end. Questa correzione assicura che il contenuto di [!DNL Recommendations] includa ora l&#39;ID di tracciamento corretto, ripristinando i rapporti di conversione e l&#39;allineamento con le metriche A4T. (TGT-53496)
* **Arresto anomalo dell&#39;editor della raccolta risolto nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata del [!UICONTROL Compositore esperienza visivo] a causa del quale l&#39;apertura di una raccolta dal pannello Editor causava l&#39;arresto anomalo della pagina con un errore di tipo: impossibile leggere le proprietà di non definito (lettura di &#39;customLocale&#39;). Questo errore si è verificato in più tipi di attività, inclusi [!UICONTROL Recommendations] e test A/B. (TGT-53703)
* **Opzione per rimuovere la raccolta selezionata ripristinata nel Compositore esperienza visivo** È stato risolto un problema nel Compositore esperienza visivo a causa del quale gli utenti potevano sostituire solo una raccolta selezionata in un&#39;attività [!UICONTROL Recommendations], ma non potevano rimuoverla completamente. Questa limitazione bloccava i casi d’uso che richiedevano una rimozione pulita della raccolta senza sostituzione. Questa correzione introduce una chiara opzione per rimuovere la raccolta selezionata, consentendo una maggiore flessibilità nella configurazione delle attività e nell’allineamento con il comportamento precedente dell’interfaccia utente. (TGT-53652)
* **Le raccolte di criteri personalizzati ora vengono visualizzate correttamente nell&#39;interfaccia utente di [!UICONTROL Recommendations].** È stato risolto un problema nell’interfaccia Recommendations (Consigli) a causa del quale le raccolte create utilizzando criteri personalizzati non visualizzavano i risultati del prodotto. Mentre le raccolte standard basate su attributi funzionavano come previsto, quelle che utilizzavano filtri personalizzati restituivano &quot;Nessun risultato trovato&quot; nonostante corrispondenze di catalogo valide. Questa correzione assicura che le raccolte che utilizzano attributi personalizzati ora vengano compilate correttamente nella scheda [!UICONTROL Prodotto], ripristinando la funzionalità completa per i flussi di lavoro di consigli personalizzati. (TGT-53653)
* **È stato risolto un problema a causa del quale le raccolte non visualizzavano i prodotti alla prima apertura della pagina [!UICONTROL Prodotti].** I clienti che accedono alle raccolte nella sezione [!UICONTROL Recommendations] hanno riscontrato risultati di prodotto vuoti alla prima apertura della pagina [!UICONTROL Products]. Questo problema è stato causato da un errore di back-end nella query GraphQL, che non è riuscito a caricare i dati di prodotto per le raccolte con criteri personalizzati. Il problema è stato risolto e i prodotti ora vengono visualizzati correttamente senza la necessità di cambiare ambiente. (TGT-53694)
* **È stato risolto un problema che impediva la rimozione delle raccolte nelle attività [!UICONTROL Recommendations] basate su moduli.** I clienti che hanno creato [!UICONTROL attività Consigli] utilizzando [!UICONTROL Compositore esperienza basato su moduli] non sono stati in grado di deselezionare una raccolta scelta in precedenza. L’interfaccia utente richiedeva la selezione di una raccolta prima del salvataggio, impedendo agli utenti di ripristinare &quot;Tutte le raccolte&quot;. Questo comportamento è stato aggiornato per corrispondere alla funzionalità del Compositore esperienza visivo, consentendo ai clienti di salvare senza una raccolta selezionata e di impostare come predefinito &quot;Tutte le raccolte&quot;, come previsto. (TGT-53708)
* **È stato risolto un problema che impediva l&#39;impostazione delle promozioni per attributo a causa di valori di raccolta o di regole di filtro mancanti.** I clienti che configurano le promozioni per attributo nel processo di creazione attività hanno riscontrato un errore che indica che in una promozione manca un ID raccolta o valori di regole di filtro. Questo problema di convalida bloccava la progressione anche quando la configurazione sembrava completa. Le promozioni possono ora essere salvate correttamente se configurate per attributo. (TGT-53750)
* **È stato risolto un problema che impediva il salvataggio delle attività a causa di nomi di esperienza duplicati.** I clienti hanno riscontrato un errore di input utente non valido durante il salvataggio di attività che includevano combinazioni specifiche di criteri e progettazioni. L’errore è stato attivato da nomi di esperienza duplicati, anche quando la configurazione sembrava valida. È ora possibile salvare le attività con configurazioni distinte senza conflitti di denominazione. (TGT-53805)
* **È stato risolto un problema a causa del quale la convalida rimaneva non valida per le promozioni configurate dall&#39;attributo.** I clienti hanno riscontrato errori di convalida persistenti durante la configurazione di promozioni per attributo nel processo di creazione dell’attività, anche quando tutti i campi obbligatori erano compilati correttamente. Il problema è stato causato da una logica di convalida errata nel flusso di lavoro [!UICONTROL Recommendations]. Le promozioni basate su attributi ora vengono convalidate e salvate come previsto. (TGT-53811)
* **È stato risolto un problema a causa del quale l&#39;applicazione di una promozione a un&#39;attività [!UICONTROL Recommendations] attiva generava un errore.** I clienti hanno riscontrato l&#39;errore &quot;A Promotion is missing an Collection ID or filtering rule values&quot; (&quot;A Promotion non dispone di un ID raccolta o di valori di regole di filtro&quot;) durante il tentativo di applicare una promozione iniziale a un&#39;attività [!UICONTROL Recommendations] attiva, anche dopo aver fornito dettagli di configurazione validi. È ora possibile applicare le promozioni alle attività live senza attivare gli errori di convalida, garantendo un’esperienza più fluida nell’interfaccia utente aggiornata per la creazione delle attività. (TGT-53738)
* **È stato risolto un problema a causa del quale i prodotti non erano visibili nelle raccolte all&#39;interno dell&#39;interfaccia utente di [!UICONTROL Recommendations].** I clienti di un singolo tenant hanno segnalato che non è stato possibile caricare gli elenchi di prodotti durante la visualizzazione di alcune raccolte nella sezione [!UICONTROL Recommendations] della nuova interfaccia utente. Il problema è stato temporaneamente risolto cambiando gli ambienti, ma questa soluzione alternativa ha portato a una scarsa esperienza utente. Le entità prodotto ora vengono caricate in modo coerente senza richiedere l’attivazione dell’ambiente. (TGT-53783)
* **È stato risolto un problema che impediva la visualizzazione di criteri e progettazioni in una riga dell&#39;interfaccia utente per la creazione di attività.** In precedenza, i criteri e le progettazioni nel processo di creazione delle attività venivano mostrati in un formato compresso, rendendo difficile per i clienti visualizzare e gestire i singoli elementi. Ogni criterio e progettazione viene ora visualizzato sulla propria riga, migliorando la leggibilità e l’usabilità nell’interfaccia utente aggiornata. (TGT-53818)

+++

**Rapporti**

+++Vedi i dettagli

* La metrica **[!UICONTROL Ricavi totali] è ora inclusa nelle esportazioni CSV dai rapporti attività.** È stato risolto un problema nell&#39;interfaccia utente aggiornata di [!UICONTROL Panoramica] a causa del quale i ricavi totali venivano visualizzati correttamente nella visualizzazione dei rapporti attività, ma non nell&#39;esportazione CSV, visualizzati come $0. Questa discrepanza ha impedito agli utenti di fare affidamento sui dati esportati per l’analisi e il reporting offline. (TGT-53325)
* La metrica **[!UICONTROL Vendite totali] è ora inclusa nelle esportazioni CSV dai rapporti attività.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale la metrica [!UICONTROL Vendite totali] veniva visualizzata correttamente nella vista dei rapporti attività ma non era presente nell&#39;esportazione CSV. Questa discrepanza impediva agli utenti di accedere a dati completi sulle prestazioni nei rapporti scaricati. Questa correzione assicura che i valori [!UICONTROL Vendite totali] siano ora inclusi con precisione nelle esportazioni CSV, ripristinando la coerenza tra reporting in-app e analisi offline. (TGT-53330)
* **Messaggi di errore migliorati per [!UICONTROL Visualizzazione grafico] quando le metriche non sono abilitate.** È stato risolto un problema nel Compositore esperienza visivo a causa del quale la [!UICONTROL Visualizzazione grafico] visualizzava un messaggio generico di tipo &quot;Si è verificato un errore&quot; quando una metrica richiesta non era abilitata nella suite di rapporti [!DNL Analytics] associata. Questo problema è stato attivato da un errore `not_enabled_metric` nella risposta GraphQL back-end. Questa correzione sostituisce il vago errore con un messaggio più informativo che aiuta gli utenti a identificare i problemi di configurazione in [!DNL Analytics], riducendo confusione e inutili escalation di supporto. (TGT-53577)
* **È stato risolto un problema a causa del quale la durata del report superava il limite supportato di 90 giorni.** I clienti che utilizzano il filtro &quot;[!UICONTROL Ultimi X giorni]&quot; nella sezione [!UICONTROL Rapporti] hanno potuto selezionare durate superiori a 90 giorni, il che poteva causare problemi di prestazioni e dati incompleti. Il filtro è stato aggiornato per applicare un intervallo massimo di 90 giorni, garantendo una generazione di rapporti coerente e affidabile. (TGT-53795)
* **È stato risolto un problema per cui i rapporti CSV delle prestazioni venivano generati utilizzando l&#39;ambiente predefinito invece di quello selezionato.** In precedenza, quando i clienti modificavano l’ambiente nelle impostazioni dei rapporti e generavano un rapporto sulle prestazioni, il CSV risultante conteneva dati provenienti dall’ambiente predefinito anziché da quello selezionato.  L&#39;interfaccia utente ora passa correttamente il parametro `environmentId`, assicurandosi che il rapporto rifletta l&#39;ambiente scelto. Inoltre, è stata migliorata la gestione degli errori. Se si verificano errori GraphQL durante la generazione del file CSV, l’interfaccia utente visualizza ora un messaggio di errore chiaro invece di produrre un file CSV vuoto. (TGT-53064)
* **È stato risolto un problema che impediva la visualizzazione dei dati nella [!UICONTROL Vista grafico] da parte del reporting di Analytics for Target (A4T).** I clienti che utilizzano [!DNL Target] con integrazione A4T hanno riscontrato un errore di tipo &quot;Si è verificato un errore&quot; quando si è passati alla visualizzazione grafico nella scheda Reporting delle attività di test A/B. Anche se la [!UICONTROL Vista tabella] è stata caricata correttamente, la [!UICONTROL Vista grafico] non è riuscita a eseguire il rendering delle tendenze delle metriche nell&#39;intervallo di tempo selezionato. [!UICONTROL Vista grafico] ora visualizza i dati sulle prestazioni come previsto per tutte le metriche supportate, migliorando la visibilità e la precisione di reporting nell&#39;interfaccia utente aggiornata. (TGT-53573)

+++

**Compositore esperienza visivo**

+++Vedi i dettagli

* **I metadati degli elementi sono ora visibili al passaggio del mouse nel menu delle breadcrumb.** È stato migliorato il menu delle breadcrumb nel Compositore esperienza visivo per visualizzare ulteriori dettagli dell’elemento come ID, classe e nome quando si passa il puntatore su un elemento. Questo miglioramento consente agli utenti di identificare e differenziare gli elementi più facilmente durante la configurazione dell’attività. (TGT-53409)
* **Il passaggio del cursore Breadcrumb evidenzia l&#39;elemento corrispondente nel Compositore esperienza visivo** È stato migliorato il [!UICONTROL Compositore esperienza visivo] per evidenziare l&#39;elemento corrispondente nell&#39;editor quando si passa il puntatore sugli elementi nel menu delle breadcrumb. Viene visualizzato anche il tipo di elemento, ad esempio contenitore, testo in grassetto o pulsante. Questo comportamento si applica agli elementi di pari livello ed esclude i tipi non supportati come SVG, in base all’elenco di convalida. (TGT-53411)
* **È stato ripristinato l&#39;avviso di modifiche non salvate nei flussi di lavoro di modifica del Compositore esperienza visivo.** È stato risolto un problema nel Compositore esperienza visivo a causa del quale gli utenti non venivano più informati in merito alle modifiche del codice personalizzato non salvate. A differenza dell’interfaccia utente legacy, nella nuova esperienza non sono presenti prompt quando si esce o si chiude l’editor di personalizzazione, con conseguente perdita accidentale di avanzamento. Con questa correzione vengono ripristinati gli avvisi per tutti i tipi di modifica, incluso il codice personalizzato, e viene garantito che gli utenti vengano avvisati prima di uscire senza salvare. (TGT-53435).
* **Le modifiche al codice personalizzato ora persistono durante l&#39;aggiornamento della pagina nel Compositore esperienza visivo** È stato risolto un problema nel Compositore esperienza visivo a causa del quale le modifiche al codice personalizzato andavano perse durante gli aggiornamenti del sito web. Questo problema si verificava su pagine con più ricaricamenti, causando la reimpostazione e il ripristino delle modifiche non salvate da parte dell’editor. La correzione assicura che le modifiche del codice personalizzato rimangano intatte anche se la pagina viene ricaricata durante la modifica, evitando la perdita accidentale di avanzamento. (TTGT-53501)
* **Problema di accesso risolto per l&#39;accesso al sito nel Compositore esperienza visivo** È stato risolto un problema che impediva agli utenti di accedere al loro sito durante l’accesso tramite il Compositore esperienza visivo. Il flusso di accesso reindirizzava ripetutamente gli utenti alla pagina di accesso, impedendo la configurazione e l’anteprima dell’attività. Questa correzione assicura che il Compositore esperienza visivo non interferisca più con il comportamento di accesso, ripristinando l’accesso previsto per gli utenti autenticati. (TGT-53524)
* **Problema di duplicazione dei cookie risolto nell&#39;estensione VEC Helper.** È stato risolto un problema a causa del quale l&#39;estensione [!UICONTROL Adobe Experience Cloud Visual Editing Helper] duplicava il cookie `at_qa_mode` durante il controllo qualità tramite collegamenti di anteprima. Quando si cambiavano manualmente gli indici di anteprima, venivano creati più cookie con valori in conflitto tra i domini, impedendo ai tester di cambiare in modo affidabile le varianti. Questo comportamento è stato osservato anche al di fuori dell’interfaccia utente di Target e ha interessato sia gli account interni che quelli client. Questa correzione assicura una gestione coerente dei cookie impedendo le voci duplicate e allineando l’ambito del dominio, consentendo un passaggio continuo delle varianti senza richiedere la pulizia manuale dei cookie. (TGT-53579)
* **È stato risolto un problema che causava perdite di memoria a causa del clic sugli elementi in una determinata home page.** I clienti che creano attività in questa home page hanno riscontrato perdite di memoria durante l’interazione con gli elementi della pagina. Il problema era legato a un numero eccessivo di avvisi nella console e a un utilizzo crescente della memoria nei sottoframe, in particolare a causa di attributi di srcset non corretti. L’utilizzo della memoria rimane ora stabile durante l’interazione. (TGT-53761)
* **È stato risolto un problema che causava l&#39;arresto anomalo del Compositore esperienza visivo e la visualizzazione di una schermata vuota durante il caricamento di alcune attività.** I clienti di un tenant specifico hanno segnalato che l’editor non è riuscito a caricare attività specifiche. Il Compositore esperienza visivo rimaneva bloccato su &quot;Applicazione delle modifiche iniziali&quot; prima dell’arresto anomalo e della visualizzazione di una schermata vuota. Il Compositore esperienza visivo ora carica le attività interessate senza errori nel processo aggiornato di creazione delle attività. (TGT-52932)
* **È stato risolto un problema che causava la visualizzazione di etichette di posizione incoerenti nella barra [!UICONTROL Gestione contenuto] delle attività [!UICONTROL Automated Personalization].** I clienti hanno segnalato che la barra [!UICONTROL Gestione contenuto] mostrava numeri di posizione non corrispondenti nelle schede [!UICONTROL Esperienze] e [!UICONTROL Offerte]. (ad esempio, Posizione 2 e Posizione 4 in Esperienze e Posizione 1 e Posizione 2 in Offerta) anche quando erano configurate solo due posizioni. Le etichette di posizione ora sono coerenti e mappate con precisione alle modifiche, migliorando la chiarezza e l’usabilità nel processo di creazione delle attività. (TGT-52934)
* **È stato risolto un problema che causava la perdita di modifiche nel Compositore esperienza visivo dopo il salvataggio.** I clienti hanno segnalato che dopo aver salvato una modifica nel Compositore esperienza visivo, la pagina veniva aggiornata e la modifica veniva ripristinata alla versione precedente. Questo problema causava la perdita degli aggiornamenti più recenti a meno che l’intera attività non venisse salvata immediatamente. Le modifiche ora persistono correttamente dopo il salvataggio e l’editor non ripristina più le modifiche in modo imprevisto, garantendo un’esperienza affidabile nel flusso di lavoro per la creazione di attività. (TGT-53500)
* **È stata migliorata la selezione degli elementi nel Compositore esperienza visivo tramite la visualizzazione del tipo di elemento al passaggio del mouse e nella selezione.** Per migliorare l’usabilità durante la creazione di attività, il Compositore esperienza visivo ora decora gli elementi HTML con il loro tipo quando vengono passati con il mouse sopra di essi o selezionati. Questo miglioramento consente ai clienti di identificare e selezionare più facilmente gli elementi corretti. Gli elementi selezionati vengono evidenziati con un colore distinto e gli elementi al passaggio del mouse sono evidenziati in blu. Viene visualizzato anche il tipo di elemento, che fornisce un contesto più chiaro durante la modifica. (TGT-53502)

+++

### Aggiornamenti Datastream (19 settembre 2025)

La combinazione di ID e sandbox dello stream di dati deve essere univoca per [!DNL Adobe Target] connessioni di destinazione.

È stata aggiornata la logica di convalida per le connessioni di destinazione [!DNL Target] per fare in modo che la combinazione di ID dello stream di dati e nome della sandbox sia univoca all’interno di un’organizzazione IMS. Ciò significa che:

* Impossibile riutilizzare la stessa coppia ID dello stream di dati + nome sandbox in più connessioni di destinazione [!DNL Target].
* Lo stesso ID dello stream di dati può essere utilizzato per connessioni diverse solo se sono configurate in sandbox diverse.
* Questa regola si applica a tutte le selezioni dello stream di dati, anche quando si seleziona &quot;Nessuno&quot;.

Questo aggiornamento garantisce una configurazione coerente e impedisce conflitti tra ambienti con più sandbox. Per ulteriori informazioni, vedere [Connessione Adobe Target](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection){target=_blank} nella *Guida delle destinazioni Experience Platform*.

### [!DNL Target Standard/Premium] 25.9.1 (5 settembre 2025)

Questa versione include i seguenti aggiornamenti e correzioni:

**[!UICONTROL Frammenti esperienza]**

+++Vedi i dettagli

* **Attribuzione utente migliorata per [!UICONTROL Offerte di Frammenti esperienza AEM].** È stato risolto un problema nel Compositore esperienza visivo a causa del quale il campo &quot;[!UICONTROL Ultimo aggiornamento]&quot; per le offerte del [!UICONTROL Frammento esperienza AEM] (XF) mostrava erroneamente un ID codice invece del nome utente. Questa discrepanza si è verificata durante la selezione delle offerte nell’interfaccia utente aggiornata, creando un’incoerenza con l’interfaccia utente legacy e le offerte HTML, in cui veniva visualizzato correttamente il nome dell’ultimo editor. Questa correzione garantisce un’attribuzione utente coerente tra i tipi di offerta, migliorando la trasparenza e l’allineamento al comportamento previsto. (TGT-52880 e TGT-52898)

+++

**Offer Decisioning**

+++Vedi i dettagli

* **Errore di decisione dell&#39;offerta risolto per le offerte ODE.** È stato risolto un problema a causa del quale le offerte ODE (Offer Decision Engine) inserite tramite [!DNL Target] restituivano un errore 400 a causa di metadati di formato mancanti. Il messaggio di errore indicava che il tipo MIME era nullo, impedendo l’elaborazione corretta delle decisioni sulle offerte. Questa correzione assicura la corretta gestione dei metadati dell’offerta, ripristinando la funzionalità per la distribuzione personalizzata dei contenuti e consentendo l’esecuzione ininterrotta delle campagne di marketing. (TGT-53635)
* **Problema di rendering dell&#39;offerta ODS risolto.** È stato risolto un problema che impediva il rendering delle offerte [!DNL Offer Decision Service] (ODS) create tramite [!DNL Adobe Journey Optimizer] (AJO) durante la generazione delle attività tramite il Compositore esperienza visivo nell&#39;interfaccia utente aggiornata. La stessa configurazione funzionava correttamente nell’interfaccia utente legacy, creando confusione e bloccando l’esecuzione della campagna. Questa correzione assicura la distribuzione coerente delle offerte in entrambe le versioni dell’interfaccia utente, ripristinando il comportamento previsto per la personalizzazione basata su AJO.

+++

**Rapporti**

+++Vedi i dettagli

* **Opzione di download ripristinata nella sezione dei report dell&#39;interfaccia utente aggiornata per la panoramica dei report.** È stato risolto un problema nella nuova interfaccia utente della panoramica a causa del quale il pulsante [!UICONTROL Scarica] non era presente nella sezione Rapporti, impedendo agli utenti di esportare i punteggi di importanza degli attributi. Questo aggiornamento ripristina la funzionalità di esportazione completa, consentendo un accesso semplificato ai dati scaricabili a scopo di analisi e reporting. (TGT-53222)
* **[!UICONTROL Il pulsante Scarica rapporto CSV completo] è stato ripristinato nella visualizzazione [!UICONTROL Attributi importanti].** È stato risolto un problema nell&#39;interfaccia utente di creazione attività aggiornata a causa del quale il pulsante [!UICONTROL Scarica rapporto CSV completo] non era presente nella sezione [!UICONTROL Attributi importanti] della visualizzazione dei rapporti. Questa correzione consente di ripristinare l’accesso alle informazioni scaricabili, garantendo funzionalità coerenti sia nell’interfaccia utente aggiornata che in quella legacy. (TGT-53238)
* **Sono stati risolti dei problemi relativi alla generazione di rapporti per [!UICONTROL Targeting automatico] nell&#39;interfaccia utente della panoramica aggiornata.** Sono stati risolti diversi problemi di interfaccia utente nell&#39;interfaccia di panoramica aggiornata che interessavano la generazione di rapporti sulle attività di [!UICONTROL Targeting automatico]. Queste correzioni includono:

  * Metriche di incremento e affidabilità mancanti nei rapporti di riepilogo
  * Indicatore di colore errato per la casella di controllo &quot;Modelli generati&quot;
  * Rapporto grafico non funzionale nonostante la varianza dei dati in [!DNL Analytics]
  * Collegamento di download mancante per i report [!UICONTROL Segmenti automatizzati] e [!UICONTROL Attributi importanti]
  * Visualizzazione report [!UICONTROL Segmenti automatizzati] interrotti

  Queste correzioni ripristinano il comportamento di reporting previsto e migliorano la visibilità delle prestazioni di [!UICONTROL Targeting automatico] nell&#39;interfaccia utente aggiornata. (TGT-53484)

+++

**[!UICONTROL Compositore esperienza visivo]**

+++Vedi i dettagli

* **Convalida del modulo corretta per le condizioni di presenza dei parametri nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale la selezione di &quot;[!UICONTROL Valore del parametro mbox personalizzato è presente]&quot; o &quot;[!UICONTROL Parametro è presente]&quot; richiedeva erroneamente ai clienti di immettere un valore. Questo comportamento è in conflitto con la logica prevista, che si limita a verificare l’esistenza di un parametro indipendentemente dal suo valore. La correzione allinea la convalida del modulo al comportamento previsto, consentendo una configurazione dell’attività più fluida e supportando l’adozione completa dell’interfaccia utente aggiornata. (TGT-53638)
* **Logica del modulo corretta per le regole di presenza dei parametri nella consegna delle pagine.&quot;** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale la selezione delle regole di consegna pagine, ad esempio &quot;[!UICONTROL Parametro presente]&quot;, &quot;[!UICONTROL Parametro non presente]&quot;[!UICONTROL Valore parametro presente]&quot; o &quot;[!UICONTROL Valore parametro non presente]&quot;, richiedeva erroneamente agli utenti di immettere un valore parametro aggiuntivo. Questo comportamento non era coerente con l’interfaccia utente legacy e contraddiceva la logica prevista di rilevamento della presenza di parametri senza specificare un valore. Questa correzione ripristina il comportamento di configurazione previsto delle regole, semplificando la configurazione delle attività e migliorando l’usabilità. (TGT-53640)
* **Logica di convalida migliorata per il generatore di regole con più pagine nell&#39;interfaccia utente aggiornata.** Sono stati risolti diversi problemi di convalida nel generatore di regole per più pagine nell’interfaccia utente aggiornata. Queste correzioni includono:

  * Impedire la creazione di regole quando il parametro mbox è vuoto
  * Visualizzazione dei messaggi di errore appropriati per gli stati di regola non validi
  * Correzione della logica di convalida per gli operatori unari e basati su parametri che non richiedono valori di operando
  * Abilitazione delle regole dei frammenti hash con operatori unari ripristinando la funzionalità di salvataggio

  Questi aggiornamenti garantiscono una configurazione precisa delle regole e migliorano l’usabilità in scenari di consegna pagine complessi. (TGT-53722)
* **Il problema di ridenominazione della posizione è stato risolto nelle attività A/B e MVT.** È stato corretto un bug nell&#39;interfaccia utente aggiornata a causa del quale la ridenominazione di una posizione in un&#39;attività [!UICONTROL Test A/B] o [!UICONTROL Test multivariato] (MVT) non persisteva dopo la navigazione tra l&#39;elenco delle posizioni, il targeting e il back. Questo aggiornamento garantisce che le modifiche al nome della posizione vengano salvate e applicate in modo coerente in tutto il flusso di lavoro dell’attività. (TGT-52367)
* **Persistenza nome posizione corretta per le attività MVT e AP nell&#39;interfaccia utente aggiornata.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale i nomi delle posizioni modificati in [!UICONTROL Test multivariato] (MVT) e [!UICONTROL Automated Personalization] (AP) non venivano salvati correttamente. Dopo aver rinominato una posizione, lo spostamento tra le schede, ad esempio [!UICONTROL Targeting] e [!UICONTROL Esperienze], ha causato il ripristino dello stato precedente dei nomi. Questa correzione assicura una denominazione della posizione coerente tra le schede e migliora l’affidabilità durante la configurazione dell’attività. (TGT-52927)
* **L&#39;etichettatura della posizione è stata corretta nel pannello di gestione esperienze per le attività MVT.** È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale il pannello [!UICONTROL Gestione esperienze] in [!UICONTROL Attività test multivariato] (MVT) mostrava una numerazione delle posizioni incoerente. Questa correzione assicura che le etichette di posizione siano sequenziali e correttamente allineate con le modifiche definite dall’utente, migliorando la chiarezza e l’usabilità durante la configurazione dell’esperienza. (TGT-52929)

+++

### [!DNL Target Standard/Premium] 25.8.4 (1° settembre 2025)

Questa versione include i seguenti aggiornamenti e correzioni:

**[!UICONTROL Attività]**

+++Vedi i dettagli

* **I clienti non potevano copiare i nomi di attività o documenti dalla [!UICONTROL Panoramica attività]**: in precedenza, i clienti non potevano copiare il nome di un&#39;attività o dell&#39;offerta/documento associato direttamente dalla [!UICONTROL Panoramica attività] nel processo aggiornato di creazione attività. Questa limitazione ha influito sull’usabilità, in particolare sugli schermi più piccoli. I clienti possono ora copiare facilmente sia i nomi delle attività che i nomi dei documenti senza soluzioni alternative. (TGT-51850)
* **Acquisizione proattiva dei dati dei clienti [!DNL Target] curati durante la creazione dell&#39;attività**: il processo di creazione dell&#39;attività è stato migliorato abilitando la raccolta proattiva di report, contenuti e schermate da [!DNL Target] clienti. Questo miglioramento risolve le lacune nei dati identificate nei casi di utilizzo esistenti e aiuta a garantire informazioni più precise durante la configurazione di attività e esperimenti. (TGT-52415)
* **Le attività di Personalizzazione automatizzata non hanno recuperato i dati pronti per il modello nella sezione [!UICONTROL Rapporti]**: i clienti che visualizzavano le attività di Automated Personalization (AP) nella sezione [!UICONTROL Rapporti] non sono stati in grado di visualizzare gli indicatori pronti per il modello a livello di gruppo di rapporti e di offerta. Questo problema si verificava perché i dati pronti per il modello non venivano recuperati correttamente dal backend. La funzionalità è stata ripristinata e ora vengono visualizzati i dati pronti per il modello come previsto. (TGT-53600 e TGT-53601)
* **Le attività pianificate per il futuro visualizzavano erroneamente lo stato &quot;[!UICONTROL Live]&quot; nella [!UICONTROL Panoramica attività]**: i clienti hanno rilevato che le attività pianificate per iniziare in futuro non erano contrassegnate correttamente come &quot;[!UICONTROL Live]&quot; nella panoramica [!UICONTROL Attività]. Questa mancata corrispondenza di stato è stata risolta e le attività pianificate ora vengono visualizzate correttamente come &quot;[!UICONTROL Pianificate]&quot; senza richiedere un aggiornamento della pagina. (TGT-52835)

+++

**[!UICONTROL Funzione Consigli]**

+++Vedi i dettagli

* **Elenco prodotti non visibile nella finestra di dialogo [!UICONTROL Visualizza raccolta]:** In precedenza, i clienti non potevano visualizzare l&#39;elenco prodotti quando visualizzavano una raccolta nella scheda [!UICONTROL Consigli]. La finestra di dialogo [!UICONTROL Visualizza raccolta] visualizza correttamente i prodotti associati, migliorando la trasparenza e l&#39;usabilità nell&#39;interfaccia utente [!UICONTROL Recommendations] aggiornata. (TGT-50531)
* **È stato risolto un problema che causava un filtro con distinzione tra maiuscole e minuscole in [!UICONTROL Ricerca nel catalogo prodotti] ricerca avanzata**: il filtro di ricerca avanzata nella pagina [!UICONTROL Ricerca nel catalogo prodotti] ora ignora correttamente la distinzione tra maiuscole e minuscole, in linea con il comportamento dei servizi back-end e GraphQL. Questo aggiornamento garantisce risultati coerenti e precisi per i suggerimenti per i clienti indipendentemente dall’involucro di testo. (TGT-53585)
* **La ricerca avanzata nell&#39;interfaccia utente aggiornata di [!UICONTROL Ricerca nel catalogo prodotti] non ha fornito suggerimenti**: i clienti che utilizzano la funzionalità di ricerca avanzata nell&#39;interfaccia utente aggiornata di [!UICONTROL Ricerca nel catalogo prodotti] dovevano immettere valori esatti con l&#39;ortografia corretta, poiché non venivano visualizzati suggerimenti. Questo problema rendeva difficile individuare i prodotti in modo efficiente. I suggerimenti vengono ora visualizzati come previsto durante l’input della ricerca avanzata. (TGT-52008)
* **Alcuni approvatori non sono stati in grado di visualizzare i prodotti in [!UICONTROL Ricerca nel catalogo prodotti]**: i clienti con autorizzazioni [!UICONTROL Approvatore] non sono stati in grado di visualizzare alcun prodotto in [!UICONTROL Ricerca nel catalogo prodotti], nonostante altri utenti con ruoli identici abbiano accesso. Questo problema era causato da un’incoerenza delle autorizzazioni che influiva sulla visibilità del catalogo. Tutti gli approvatori ora possono visualizzare i prodotti nella sezione [!UICONTROL Recommendations] come previsto. (TGT-53617)

+++ 

**[!UICONTROL Rapporti]**

+++Vedi i dettagli

* **Impossibile caricare i report per il pubblico desktop a causa di un errore di nome del pubblico non valido**: si è verificato un errore di GraphQL durante il tentativo di visualizzare i report per il solo pubblico nel processo di creazione attività. Il sistema ha restituito un messaggio di tipo &quot;Nome pubblico non valido: XXXXX&quot; che impediva l’accesso ai dati di reporting. I rapporti ora vengono caricati correttamente per il pubblico del desktop. (TGT-53371)
* **Il passaggio a un altro pubblico nella pagina Rapporti ha causato errori nell&#39;interfaccia utente di Target**: si sono verificati errori durante la selezione di alcuni tipi di pubblico nella sezione [!UICONTROL Rapporti]. Questo problema era causato da una gestione non valida del pubblico nelle chiamate GraphQL back-end, che causava errori imprevisti e dati mancanti. Il problema è stato risolto e i tipi di pubblico desktop ora vengono caricati senza errori, anche quando non sono disponibili dati. (TGT-53370)
* **[!UICONTROL La vista Grafico] nella sezione [!UICONTROL Rapporti] non ha visualizzato i valori di[!DNL Analytics]**: i clienti che accedono alla [!UICONTROL vista Grafico] nella sezione Reporte hanno rilevato dati mancanti, con tutti i valori visualizzati come zero. Il problema è stato causato da un recupero di dati errato da [!UICONTROL Analytics]. [!UICONTROL Nella visualizzazione Grafico] sono ora visualizzati valori precisi come previsto. (TGT-52792)
+++

**[!UICONTROL Compositore esperienza visivo] (VEC)**

+++Vedi i dettagli

* **Impossibile fare clic su &quot;Accetta cookie&quot; con il [!UICONTROL Compositore esperienza avanzato] (EEC) a causa di una funzione mancante**: i clienti hanno segnalato che il tentativo di accettare i cookie tramite il EEC ha restituito un errore della console: `handleclickAcceptAllButton is not defined`. La funzionalità di accettazione dei cookie ora funziona come previsto, garantendo un’esperienza più fluida durante la creazione dell’attività nell’interfaccia utente aggiornata. (TGT-52794)
* **La nuova interfaccia utente Compositore esperienza avanzato non è riuscita a caricare alcune pagine precedentemente supportate nell&#39;interfaccia utente legacy**: i clienti hanno segnalato che il nuovo Compositore esperienza avanzato non poteva caricare alcune pagine accessibili nell&#39;interfaccia utente legacy nonostante il codice non compatibile con iframe presente sul sito. Il processo aggiornato di creazione delle attività ora supporta il caricamento di queste pagine, ripristinando la compatibilità per i flussi di lavoro di creazione delle attività. (TGT-53061)
* **Il Compositore esperienza visivo mostrava una schermata bianca vuota durante la modifica delle esperienze**: i clienti di un determinato tenant segnalavano che la schermata del Compositore esperienza visivo era vuota quando si tentava di modificare le esperienze nel Compositore esperienza visivo aggiornato. Questo problema interessava sia le attività nuove che quelle precedenti, impedendo la continuità del flusso di lavoro. Il Compositore esperienza visivo ora si carica correttamente, consentendo ai clienti di modificare le esperienze senza interruzioni. (TGT-53547)
* **Il Compositore esperienza visivo si è verificato un arresto anomalo ed è stata visualizzata una schermata vuota durante il caricamento di alcune attività**: i clienti di un determinato tenant hanno segnalato che il Compositore esperienza visivo non è riuscito a caricare attività specifiche. L’editor esperienze rimaneva bloccato su &quot;Applicazione delle modifiche iniziali&quot; prima dell’arresto anomalo e della visualizzazione di una schermata vuota. Gli errori della console indicano un errore durante la lettura delle proprietà non definite. L’editor ora carica le attività interessate senza errori nel Compositore esperienza visivo aggiornato. (TGT-53548)
* **La cancellazione di tutti i valori di data con Backspace ha causato l&#39;arresto anomalo della pagina**: le attività di pianificazione dei clienti nella sezione [!UICONTROL Obiettivi e impostazioni] hanno subito un arresto anomalo durante l&#39;utilizzo di Backspace per cancellare tutti i valori dai campi &quot;[!UICONTROL Data e ora specificata]&quot;. Questo problema è stato causato da un errore di riferimento null nella logica di gestione delle date. La pagina ora gestisce gli input di date vuoti senza arresti anomali. (TGT-53624)
* **Nessun prodotto è stato visualizzato in [!UICONTROL Ricerca nel catalogo prodotti] a causa di un payload non valido**: i clienti che accedono alla sezione [!UICONTROL Consigli] in [!UICONTROL Ricerca nel catalogo prodotti] hanno rilevato risultati vuoti a causa di un payload di GraphQL non valido. Questo errore di back-end ha impedito il caricamento corretto dei dati del prodotto. I prodotti ora vengono visualizzati come previsto nell’interfaccia utente aggiornata. (TGT-53630)
* **[!DNL Scene7]immagini sono state salvate con una risoluzione inferiore nel Compositore esperienza visivo aggiornato**: i clienti che modificano le esperienze nel Compositore esperienza visivo aggiornato hanno notato che [!UICONTROL gli URL immagine Scene7] sono stati salvati senza parametri di risoluzione, con conseguente consegna di immagini di qualità inferiore (400×400 invece del previsto 800×800). Gli URL delle immagini ora mantengono i parametri corretti per garantire la risoluzione corretta. (TGT-52631)
* **le attività live potevano ancora essere modificate nel Compositore esperienza visivo**: i clienti potevano accedere alle opzioni di modifica per le attività live nel Compositore esperienza visivo aggiornato, il che poteva causare modifiche non desiderate. Questo problema è stato risolto disabilitando la funzionalità di modifica per le attività live. I pulsanti di modifica ora sono nascosti nell’elenco delle attività e nella panoramica per gli editor, mentre gli approvatori e gli altri ruoli rimangono invariati. (TGT-53055)
* **Disattivazione della sezione delle attività [!UICONTROL Non riuscito] e [!UICONTROL Bozza] nel Compositore esperienza visivo aggiornato**: le opzioni delle attività [!UICONTROL Non riuscito] e [!UICONTROL Bozza] sono state rimosse dal Compositore esperienza visivo aggiornato. La nuova interfaccia utente non supporta più gli stati di bozza e le campagne con errori non vengono memorizzate nel backend. Queste opzioni non sono più rilevanti. Anche i filtri correlati e i campi back-end (ad esempio, `uiSyncFailed`, `errorMessage`) sono stati rimossi per semplificare la gestione delle attività. (TGT-53150)
* **Impossibile accedere al Compositore esperienza visivo per un&#39;attività**: i clienti che hanno tentato di accedere al proprio sito tramite il Compositore esperienza visivo sono stati ripetutamente reindirizzati alla pagina di accesso, impedendo l&#39;accesso alla modifica dell&#39;attività. Questo problema non era riproducibile internamente e potrebbe essere correlato alla gestione delle sessioni lato sito. Il flusso di accesso è stato stabilizzato e i clienti possono ora accedere al Compositore esperienza visivo senza errori di reindirizzamento. (TGT-53524)
* **Se si preme due volte il pulsante Indietro nella modalità [!UICONTROL Sfoglia], si è verificato un arresto anomalo del Compositore esperienza visivo**: se si preme due volte il pulsante Indietro del browser, si sono verificati arresti anomali durante la navigazione nella modalità [!UICONTROL Sfoglia] nel Compositore esperienza visivo. Questo problema causava il blocco dell’editor e richiedeva un aggiornamento della pagina. L’editor ora gestisce la navigazione posteriore in modo affidabile senza arresti anomali. (GT-53568)
* **Impossibile modificare le attività a causa di mappature di posizione non definite**: si è verificato un errore durante il tentativo di modifica delle attività, causato da ID di posizione non definiti nella logica `LocationMapping.behaviorTargetedActivity`. Questo problema causava un errore 400 e bloccava gli aggiornamenti delle attività. È ora possibile modificare le attività senza errori di convalida relativi alla posizione. (TGT-53607)
* **Il salvataggio delle attività ha provocato un errore di input utente non valido**: si è verificato un errore di input utente non valido durante il tentativo di salvare le attività dopo aver apportato modifiche minori nel Compositore esperienza visivo aggiornato. L’errore è stato causato da mappature di posizione non corrispondenti nella logica di convalida back-end. Ora è possibile salvare le attività senza attivare errori relativi alla posizione. (TGT-53603)

+++

### [!DNL Target Standard/Premium] 25.8.3 (21 agosto 2025)

Questa versione include i seguenti aggiornamenti e correzioni:

**[!UICONTROL Attività]**

+++Vedi i dettagli

* **È stato risolto un problema a causa del quale il salvataggio delle attività causava un errore di input dell&#39;utente non valido a causa di dati di proprietà non validi**: si è verificato un errore critico durante il tentativo di salvare le attività esistenti. Il messaggio di errore indica un input utente non valido, in particolare un riferimento a un contenuto di nome proprietà non riconosciuto nel payload JSON. In particolare, le nuove attività che utilizzano la stessa proprietà sono state salvate correttamente, suggerendo che il problema fosse isolato nei dati delle attività legacy. Il processo di creazione delle attività ora gestisce correttamente le configurazioni delle proprietà legacy, evitando errori di input non validi e garantendo un comportamento di salvataggio coerente tra le attività nuove ed esistenti. (TGT-53507)
* **È stato risolto un problema che impediva ai clienti di salvare un&#39;attività a causa di un errore InvalidProperty.Json**: si è verificato un errore durante il tentativo di salvare un&#39;attività nell&#39;interfaccia utente aggiornata, anche senza apportare modifiche. Il messaggio di errore indica una struttura JSON non valida: &quot;Json non valido. Nome di proprietà &#39;content&#39; non riconosciuto. Posizione: riga - 1, colonna - 432.&quot; Questo problema era causato da una proprietà non riconosciuta nel payload della richiesta ed è stato ora risolto. I clienti possono salvare le attività senza riscontrare questo errore. (TGT-53513)
* **È stato risolto un problema che impediva alle attività pianificate di visualizzare in modo errato lo stato [!UICONTROL Live] fino all&#39;aggiornamento della pagina**: i clienti hanno osservato che quando si pianificava un&#39;attività per andare live in una data e un&#39;ora future, lo stato appariva immediatamente come [!UICONTROL Live] invece di [!UICONTROL Scheduled]. Ciò causava confusione, anche se il messaggio di conferma indicava correttamente che l’attività era pianificata. L&#39;aggiornamento della pagina ha corretto la visualizzazione dello stato. Questo problema è stato risolto e le attività pianificate mostrano correttamente lo stato Pianificato senza richiedere un aggiornamento. (TGT-52937)

+++

**[!UICONTROL Analytics per Target] (A4T)**

+++Vedi i dettagli

* **È stato risolto un problema che impediva ai clienti di digitare i nomi delle suite di rapporti durante il processo di creazione attività**: i clienti che utilizzavano [!DNL Adobe Analytics] come origine per la generazione di rapporti durante il processo di creazione attività non potevano digitare nell&#39;elenco a discesa [!UICONTROL Suite di rapporti] per cercare suite di rapporti specifiche. Questo ha interessato i flussi di lavoro delle organizzazioni con un numero elevato di suite di rapporti, in cui lo scorrimento manuale ha ritardato notevolmente la configurazione. L’elenco a discesa non era ordinato alfabeticamente e non rispondeva in modo coerente all’input digitato, rendendo difficile individuare suite di rapporti come &quot;Office + Store - Web - Prod&quot;. Questo problema è stato risolto e i clienti possono ora eseguire ricerche in modo efficiente digitando i nomi delle suite di rapporti. (TGT-53345)

+++

**[!UICONTROL Tipi di pubblico]**

+++Vedi i dettagli

* **È stato risolto un problema che impediva ai tipi di pubblico con &quot;intervallo di tempo&quot; scaduti di salvare le attività anche dopo la rimozione**: i clienti non potevano salvare le attività nell&#39;interfaccia utente aggiornata a causa di un errore relativo ai tipi di pubblico con &quot;intervallo di tempo&quot; scaduti. Anche dopo aver rimosso il pubblico interessato, il messaggio di errore persisteva: &quot;L’attività contiene un pubblico con un intervallo di tempo non valido&quot;. Questo problema si verificava perché il sistema continuava a convalidare il pubblico per sola attività, anche quando non era più in uso. Il comportamento è stato ulteriormente complicato dalle discrepanze di fuso orario. La logica di convalida è stata corretta e i clienti ora possono salvare le attività senza incontrare questo errore. (TGT-53517)

+++

**[!UICONTROL Frammento esperienza]s**

+++Vedi i dettagli

* **È stato risolto un problema che impediva ai clienti di inserire frammenti di esperienza tramite [!UICONTROL Inserisci prima] o [!UICONTROL Inserisci dopo] nell&#39;interfaccia utente**. Si è verificato un errore durante il tentativo di inserire [!UICONTROL frammenti di esperienza] in un&#39;attività tramite le opzioni &quot;Inserisci prima&quot; o &quot;Inserisci dopo&quot; nell&#39;interfaccia utente aggiornata. Il messaggio di errore visualizzato era: &quot;Il contenuto dell’offerta deve contenere esattamente un elemento HTML&quot;. Questo problema era specifico dell’interfaccia utente aggiornata e non si verificava nella versione precedente. Il problema è stato risolto e i clienti possono inserire [!UICONTROL Frammenti esperienza] senza incontrare questo errore. (TGT-53442)

+++

**[!UICONTROL Decisioni di offerta]**

+++Vedi i dettagli

* **È stato risolto un problema che impediva ai clienti di modificare le offerte decisionali e di selezionare elementi di pagina specifici nell&#39;interfaccia utente aggiornata**: Nel processo di creazione attività aggiornato, i clienti non potevano modificare le offerte decisionali esistenti o selezionare elementi di pagina specifici nel Compositore esperienza visivo. Le offerte relative alle decisioni non venivano visualizzate correttamente come offerte HTML e le modifiche apportate durante la modifica non venivano salvate. Inoltre, alcuni URL regionali, come il sito Giappone, non venivano caricati correttamente nel Compositore esperienza visivo, bloccando la creazione e gli aggiornamenti dell’attività. Le offerte decisionali ora vengono visualizzate correttamente, gli elementi di pagina sono selezionabili come previsto e gli URL regionali vengono caricati correttamente nel Compositore esperienza visivo, ripristinando la funzionalità di modifica completa. (TGT-53425)
* **È stato risolto un problema che impediva la modifica imprevista dei selettori [!UICONTROL Decisione offerta] dopo il salvataggio**: nel processo di creazione attività aggiornato, i clienti non potevano modificare il selettore [!UICONTROL Decisione offerta] come previsto. Tentativi di modifica del selettore non riusciti e il selettore è tornato a un valore errato dopo il salvataggio. Questo comportamento ha causato la scomparsa dell’offerta decisionale dal Compositore esperienza visivo, bloccando ulteriori modifiche. Le modifiche del selettore ora vengono mantenute correttamente e le offerte di decisione rimangono visibili e modificabili nel Compositore esperienza visivo dopo il salvataggio. (TGT-53433)
* **È stato risolto un problema che causava la scomparsa di [!UICONTROL Decisioni di offerta] dall&#39;attività dopo il salvataggio**: [!UICONTROL Le decisioni di offerta] aggiunte durante il processo di creazione dell&#39;attività non venivano mantenute dopo il salvataggio e la riapertura dell&#39;attività. Questo problema si verificava durante la modifica del contenuto dinamico e l&#39;inserimento di [!UICONTROL Decisioni di offerta]con selettori e proprietà specifici. [!UICONTROL Le decisioni sulle offerte] ora persistono correttamente dopo il salvataggio e i selettori rimangono intatti, garantendo un comportamento di targeting e modifica coerente. (TGT-53434)

+++

**[!DNL Recommendations]**

+++Vedi i dettagli

* **È stato risolto un problema nell&#39;interfaccia utente di [!DNL Recommendations] a causa del quale il download del file CSV dei criteri personalizzati restituiva l&#39;errore 404**: è stato risolto un problema che impediva ai clienti di scaricare il file CSV dei criteri personalizzati nel processo di creazione delle attività. Il collegamento per il download ora funziona correttamente, consentendo ai clienti di esportare i criteri personalizzati come previsto. (TGT-51966)
* **È stato corretto il caricamento incoerente delle immagini in [!UICONTROL Ricerca nel catalogo]**: è stato risolto un problema che impediva il caricamento coerente di miniature e immagini in[!UICONTROL &#x200B; Ricerca nel catalogo] nel processo di creazione attività. Le immagini non venivano visualizzate a meno che la colonna &quot;URL miniatura&quot; non fosse visibile e alcune immagini di prodotto venivano caricate parzialmente o non completamente dopo le azioni di navigazione o ricerca. Il comportamento di caricamento delle immagini è stato stabilizzato e le miniature ora vengono visualizzate in modo affidabile, indipendentemente dalla visibilità delle colonne o dalle azioni di navigazione. (TGT-52778)
* **È stato risolto un problema a causa del quale la modifica di un consiglio in un&#39;esperienza duplicata influiva sull&#39;esperienza originale**: i clienti segnalavano che la modifica di un consiglio in un&#39;esperienza duplicata alterava involontariamente l&#39;esperienza originale. In particolare, dopo aver duplicato l’esperienza B nel processo di creazione delle attività e averne modificato la progettazione o i criteri, le stesse modifiche sono state applicate all’esperienza B originale, nonostante fossero entità separate. Le esperienze duplicate ora mantengono configurazioni separate, garantendo che le modifiche apportate a un’esperienza non influiscano sull’originale. (TGT-53369)
* **È stato risolto un problema a causa del quale le modifiche apportate a un&#39;esperienza duplicata influivano involontariamente sull&#39;esperienza originale in un&#39;attività**: i clienti hanno segnalato che quando si duplicava un&#39;esperienza all&#39;interno di un&#39;attività e si assegnava un nuovo pubblico, qualsiasi modifica apportata alla progettazione o ai criteri dell&#39;esperienza duplicata veniva riportata anche nell&#39;esperienza originale. Questo problema si verificava anche se non venivano apportate modifiche direttamente alla versione originale, con conseguente impatto sulla possibilità di creare varianti indipendenti all’interno della stessa attività. Il processo di creazione attività ora isola correttamente le esperienze duplicate, garantendo che le modifiche apportate a un’esperienza non influiscano sull’originale. (TGT-53361)
* **È stato risolto un problema che impediva a intermittenza al [!UICONTROL Catalogo consigli] di visualizzare i dati completi degli attributi del prodotto**: nell&#39;interfaccia utente [!DNL Recommendations] aggiornata, si è verificato un problema a causa del quale alcuni attributi del prodotto, ad esempio il messaggio, non venivano visualizzati in modo coerente nei risultati della [!UICONTROL Ricerca nel catalogo], anche se i dati erano presenti nel feed. Questo problema richiedeva ai clienti di riconfigurare manualmente la visibilità delle colonne per recuperare i valori mancanti. [!UICONTROL Ricerca nel catalogo] visualizza ora in modo affidabile tutti gli attributi configurati, eliminando la necessità di reimpostare manualmente le colonne. (TGT-52769)
* **È stato risolto un problema che impediva la disabilitazione di una [!UICONTROL promozione prima] in un&#39;attività live**: i tentativi di disabilitare una [!UICONTROL promozione prima] in un&#39;attività live non sono stati salvati. Dopo aver selezionato [!UICONTROL Modifica promozione] e averla disabilitata, la promozione è rimasta attiva durante la modifica dell&#39;attività, impedendo gli aggiornamenti alle configurazioni dei consigli. Le impostazioni della promozione ora vengono salvate correttamente, consentendo ai clienti di disabilitare o modificare le promozioni nelle attività live come previsto. (TGT-53231)
* **È stato risolto un problema che causava l&#39;attivazione di [!DNL Recommendations] [!UICONTROL Promozione] senza dati causando un messaggio di errore non chiaro**: l&#39;attivazione di [!UICONTROL Promozione prima] o [!UICONTROL Promozione dopo] in un&#39;attività [!DNL Recommendations] senza specificare i valori richiesti generava un messaggio generico di errore di input non valido. Il problema di base era un campo di configurazione mancante, ma il messaggio di errore non indicava chiaramente la causa, rendendo difficile la risoluzione dei problemi. Il processo di creazione attività fornisce ora un messaggio di errore chiaro e actionable quando mancano campi obbligatori, come `collectionId` o regole, che consente ai clienti di identificare e risolvere rapidamente i problemi di configurazione. (TGT-52616)
* **È stato risolto un problema che impediva la visualizzazione dell&#39;elenco [!UICONTROL Prodotto] nella finestra modale [!UICONTROL Modifica] all&#39;interno della scheda [!UICONTROL Consigli]**: i clienti non potevano visualizzare l&#39;elenco di prodotti filtrato durante la modifica di una [!UICONTROL raccolta] o [!UICONTROL esclusione] nella scheda [!UICONTROL Consigli]. L’elenco doveva essere aggiornato in tempo reale in base alle regole applicate, ma non veniva visualizzato come previsto. Questo problema è stato risolto e l’elenco dei prodotti ora viene visualizzato correttamente e viene aggiornato in modo dinamico man mano che le regole vengono modificate. (TGT-53481)
* **È stato risolto un problema con il layout della finestra di dialogo Visualizza dettagli nell&#39;interfaccia utente aggiornata**: il layout della finestra modale Visualizza dettagli nell&#39;interfaccia utente aggiornata è stato modificato per migliorarne la chiarezza e l&#39;usabilità. La finestra di dialogo ora include due schede:
  * [!UICONTROL Dettagli] scheda: visualizza tutte le informazioni rilevanti per l&#39;elemento selezionato.
  * Scheda [!UICONTROL Inventario]: mostra tutti i prodotti filtrati in base alle regole di raccolta ed esclusione correnti.

  Questo miglioramento consente ai clienti di navigare e comprendere più facilmente i dati specifici degli articoli e il contesto dell’inventario all’interno del processo di creazione delle attività. (TGT-53503)

  * **È stato risolto un problema che causava la ricomparsa delle promozioni rimosse nelle attività di consigli dopo il salvataggio**: i clienti segnalavano che quando le promozioni [!UICONTROL front] o [!UICONTROL back] venivano rimosse dalle attività [!DNL Recommendations] e l&#39;attività veniva salvata, le promozioni continuavano a essere visualizzate alla riapertura. Questo problema si verificava sia negli ambienti di staging che in quelli di produzione e interessava il processo aggiornato di creazione delle attività. Il problema è stato risolto. Le promozioni rimosse da un&#39;attività ora persistono correttamente dopo il salvataggio. (TGT-53490)

+++

**Rapporti**

+++Vedi i dettagli

* **È stato risolto un problema che causava la visualizzazione di valori di pubblico nulli da parte del report [!UICONTROL Segmenti automatizzati]**: i clienti hanno segnalato che [!UICONTROL Segmenti automatizzati] nei report attività mostravano valori nulli per i dati di pubblico, impedendo un&#39;analisi accurata delle prestazioni dei segmenti. Questo problema si verificava quando si accedeva alla sezione [!UICONTROL Rapporti] e si selezionavano [!UICONTROL Segmenti automatizzati], anche se erano previsti dati di pubblico validi. [!UICONTROL Segmenti automatizzati] ora visualizza correttamente i valori del pubblico, garantendo reporting affidabile e informazioni sulla segmentazione. (TGT-52793)

+++

**Applicazioni a pagina singola (SPA)**

+++Vedi i dettagli

* **È stato risolto un problema che causava il passaggio tra le modalità [!UICONTROL Sfoglia] e [!UICONTROL Progettazione] e la reimpostazione dello stato dell&#39;applicazione a pagina singola nell&#39;interfaccia utente aggiornata**: i clienti hanno segnalato che il passaggio tra le modalità [!UICONTROL Sfoglia] e [!UICONTROL Progettazione] nell&#39;interfaccia utente aggiornata causava il ricaricamento dell&#39;editor Web e il ripristino dello stato dell&#39;applicazione a pagina singola. Questo problema ha interrotto i flussi di lavoro e ha richiesto ai clienti di inserire nuovamente le informazioni. Il problema è stato risolto. Lo stato di un’applicazione a pagina singola viene ora mantenuto quando si passa da una modalità all’altra, garantendo un’esperienza più fluida e coerente durante la creazione di attività. (TGT-53074)

+++

**[!UICONTROL Compositore esperienza visivo] (VEC)**

+++Vedi i dettagli

* **È stato risolto un problema nel processo di creazione attività che bloccava la progressione al passaggio [!UICONTROL Targeting] nelle attività di Personalizzazione automatizzata**: è stato risolto un problema nel processo di creazione attività a causa del quale i clienti non potevano procedere al passaggio [!UICONTROL Targeting] nelle attività [!UICONTROL Automated Personalization] (Personalizzazione automatizzata) a meno che non fossero state aggiunte due posizioni. Questo comportamento era diverso dall’esperienza precedente, in cui era sufficiente una singola posizione con più offerte. Il requisito è stato corretto, consentendo ai clienti di continuare a utilizzare le impostazioni per una singola posizione come parte dei flussi di lavoro di Personalizzazione automatizzata. (TGT-53426)
* **È stato risolto un problema che impediva al nuovo processo di creazione attività di impostare il parametro fmt=png-alpha per le immagini trasparenti**: nell&#39;interfaccia utente aggiornata, le immagini inserite durante il processo di creazione attività non includevano più il parametro `fmt=png-alpha` per impostazione predefinita, con conseguente perdita di trasparenza. Questo comportamento era diverso dalla precedente interfaccia utente, che aggiungeva automaticamente il parametro agli URL delle immagini, mantenendo gli sfondi trasparenti. Il processo di creazione attività ora applica correttamente il parametro `fmt=png-alpha` agli URL immagine quando è richiesta la trasparenza, garantendo il rendering coerente delle risorse trasparenti. (TGT-52615)
* **È stato risolto un problema che impediva ai clienti di cercare le suite di rapporti nell&#39;interfaccia utente aggiornata**: nell&#39;interfaccia utente aggiornata, l&#39;elenco a discesa [!UICONTROL Suite di rapporti] nella sezione [!UICONTROL Obiettivi e impostazioni] non consentiva ai clienti di digitare e cercare, rendendo difficile individuare suite di rapporti specifiche, in particolare per i tenant con un numero elevato di voci. A differenza dell’interfaccia utente precedente, l’elenco non era ordinato e mancava di filtri basati sugli input. Questo problema è stato risolto. Ora i clienti possono digitare per cercare e filtrare le suite di rapporti, ripristinando le funzionalità disponibili nell’interfaccia utente legacy. (TGT-53514)

+++

**[!UICONTROL Aree di lavoro]**

+++Vedi i dettagli

* **È stato risolto un problema che consentiva a un cliente limitato a una sola area di lavoro di visualizzare le attività da altre aree di lavoro**: i clienti con accesso limitato a una sola area di lavoro potevano visualizzare in modo imprevisto le attività in tutte le aree di lavoro selezionando [!UICONTROL Tutte le aree di lavoro] nel processo di creazione attività. Questa visibilità comportava il rischio di modifiche non intenzionali alle attività live in altre aree di lavoro, con un potenziale impatto sulle prestazioni del sito web. I controlli di accesso a Workspace sono stati rafforzati per garantire che i clienti possano visualizzare e interagire solo con le attività all’interno dell’area di lavoro assegnata. (TGT-53101)
* **È stato risolto un problema che consentiva a un cliente di visualizzare le attività da [!UICONTROL Workspace predefinito] senza avere accesso:** Un cliente con accesso limitato all&#39;area di lavoro di gestione temporanea poteva visualizzare le attività da [!UICONTROL Workspace predefinito] tramite il processo di creazione attività. Questo comportamento si è verificato nonostante la configurazione di back-end e i diritti di accesso corretti. I controlli di accesso a Workspace sono stati rafforzati per garantire che i clienti possano visualizzare le attività solo all’interno dell’area di lavoro assegnata.(TGT-53297)

+++

### [!DNL Target Standard/Premium] 25.8.2 (14 agosto 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

**[!UICONTROL Attività]**

+++Vedi i dettagli

* **È stato risolto un problema relativo al caricamento delle attività nell&#39;interfaccia utente [!DNL Target] aggiornata**: è stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale alcune attività non venivano caricate durante il tentativo di modifica. Questo problema causava la partenza degli utenti da una schermata di caricamento indefinita. Questo problema ha interessato più attività ed è stato segnalato come incoerente tra i clienti. Con questa correzione, le attività interessate ora vengono caricate correttamente, consentendo una modifica diretta e riducendo le interruzioni dei flussi di lavoro delle attività. (TGT-53209)
* **È stato corretto un errore di salvataggio nel processo di creazione attività a causa della convalida `optionLocalId`**: è stato risolto un problema nel processo di creazione attività che impediva ai clienti di salvare le modifiche a causa di un errore di convalida del back-end: `OptionLocalIdReferentialIntegrity.ABActivity - Invalid optionLocalIds:` Questo problema si verificava durante la modifica di elementi specifici all&#39;interno di un&#39;attività, causando un&#39;operazione di salvataggio non riuscita. La correzione assicura che `optionLocalId` riferimenti siano ora convalidati correttamente, consentendo ai clienti di salvare le attività senza incontrare questo errore. (TGT-53293)
* **È stato corretto un arresto anomalo nel processo di creazione attività causato da riferimenti di opzione non validi durante il passaggio da una pagina all&#39;altra**: è stato risolto un problema nel processo di creazione attività che causava l&#39;arresto anomalo dell&#39;interfaccia utente dopo il passaggio da una pagina all&#39;altra tre volte durante la modifica. L&#39;arresto anomalo è stato attivato da riferimenti di opzione non validi, causando errori della console quali &quot;Impossibile trovare l&#39;opzione con localId &#39;7&#39;.&quot; Con questo aggiornamento, i clienti possono passare da una pagina all’altra e applicare le modifiche senza incontrare errori o interruzioni del sistema. (TGT-53295)
* **È stato corretto un errore di salvataggio nel processo di creazione attività causato da un input utente non valido durante la modifica delle esperienze**: è stato risolto un problema nel processo di creazione attività a causa del quale i clienti non potevano salvare le modifiche apportate a un&#39;attività a causa di un errore di input utente non valido. L’errore si è verificato durante la modifica delle esperienze nell’interfaccia utente aggiornata, impedendo il commit degli aggiornamenti. L’attività ora può essere salvata correttamente, consentendo ai clienti di modificarla e pubblicarla senza interruzioni. (TGT-53267)
* **È stato risolto un problema di caricamento nel processo di creazione attività che impediva la modifica nell&#39;interfaccia utente aggiornata**: è stato risolto un problema nel processo di creazione attività a causa del quale i clienti non potevano modificare le attività nell&#39;interfaccia utente aggiornata a causa di una schermata di caricamento continuo. Ora i clienti possono aprire e modificare le attività senza riscontrare errori di caricamento. (TGT-53415)
* **È stato risolto un problema relativo ai requisiti di esperienza nel processo di creazione attività per le attività di Personalizzazione automatizzata nell&#39;interfaccia utente aggiornata**: è stato risolto un problema nel processo di creazione attività in cui [!UICONTROL le attività di Automated Personalization] (Personalizzazione automatizzata) richiedevano due posizioni invece di due esperienze nell&#39;interfaccia utente aggiornata. Questo comportamento ha bloccato i casi di utilizzo in cui i clienti configuravano una singola posizione con più offerte, precedentemente supportate. Il requisito è stato corretto per corrispondere alla funzionalità originale, consentendo ai clienti di procedere con le attività di Personalizzazione automatizzata utilizzando due esperienze indipendentemente dal conteggio delle posizioni. (TGT-53429)
* **È stato corretto il comportamento del campo degli elementi tracciati in modalità Traccia clic per evitare input non salvati e migliorare la chiarezza**: è stato risolto un problema nel processo di creazione attività in cui il campo [!UICONTROL Elemento tracciato] in modalità [!DNL Click Track] era modificabile ma non manteneva il nome immesso, generando confusione per i clienti. Il campo è ora disabilitato per evitare input non salvati e la denominazione degli elementi selezionati è stata chiarita per migliorare la configurazione dell&#39;obiettivo e la precisione del tracciamento.** (TGT-53458)
* **È stato risolto un problema nel processo di creazione attività che bloccava la denominazione dei componenti tracciati in modalità [!UICONTROL ClickTrack]**: è stato risolto un problema nel processo di creazione attività a causa del quale i clienti non potevano assegnare un nome ai componenti tracciati in modalità [!UICONTROL ClickTrack]. Dopo aver immesso un nome, il campo appariva modificabile ma non manteneva l’input; in modalità di modifica venivano utilizzate per impostazione predefinita etichette generiche come &quot;OBIETTIVO PRIMARIO 0&quot;. Il campo degli elementi tracciati è ora disabilitato e il comportamento di denominazione è stato chiarito per migliorare la configurazione degli obiettivi e la precisione del tracciamento. (TGT-51396)

+++

**Frammenti esperienza (XF)**

+++Vedi i dettagli

* **È stato risolto un problema nel processo di creazione attività che consentiva la modifica non intenzionale da parte di HTML dei frammenti esportati da AEM**: è stato risolto un problema nel processo di creazione attività che consentiva ai clienti di modificare il HTML di [!DNL Experience Fragments] (XF) esportati da [!DNL Adobe Experience Manager] (AEM) in [!DNL Target]. Questo comportamento non era intenzionale, poiché gli XF dovrebbero rimanere bloccati per la modifica dopo la pubblicazione da AEM. La correzione assicura che l’opzione &quot;Modifica HTML&quot; non sia più disponibile per i frammenti esportati da AEM, mantenendo l’integrità dei contenuti e la governance prevista. (TGT-53286)
* **È stato risolto un problema di anteprima intermittente per il contenuto XF nel processo di creazione attività nell&#39;interfaccia utente aggiornata**: è stato risolto un problema nel processo di creazione attività a causa del quale il rendering del contenuto XF in modalità anteprima non riusciva a intermittenza nell&#39;interfaccia utente aggiornata. Anche se il contenuto consegnato correttamente, l’anteprima non veniva visualizzata in modo coerente, rendendo difficile per i clienti convalidare la configurazione delle offerte. Le anteprime XF ora vengono caricate in modo affidabile, migliorando l’affidabilità e l’efficienza durante la configurazione dell’attività. (TGT-53318)

+++

**Modalità Controllo di qualità**

+++Vedi i dettagli

* **È stato risolto un problema nel processo di creazione attività a causa del quale gli spazi iniziali negli URL causavano l&#39;interruzione dei collegamenti di controllo qualità**: è stato risolto un problema nel processo di creazione attività a causa del quale gli spazi iniziali nell&#39;URL attività non venivano tagliati correttamente durante il salvataggio. Questo causava collegamenti QA non validi e formattazione errata nel back-end. Dopo l’aggiornamento, gli URL vengono ora salvati correttamente, evitando collegamenti interrotti e migliorando l’affidabilità dei flussi di lavoro di controllo qualità per i clienti. (TGT-53427)

+++

**[!UICONTROL Funzione Consigli]**

+++Vedi i dettagli

* **È stato risolto un problema nell&#39;interfaccia utente di ricerca del catalogo a causa del quale la ricerca avanzata non riusciva a fornire suggerimenti**: è stato risolto un problema nella nuova interfaccia utente di [!UICONTROL Ricerca nel catalogo] a causa del quale la funzionalità di [!UICONTROL Ricerca avanzata] non riusciva a fornire suggerimenti. Gli utenti dovevano immettere valori esatti con un’ortografia precisa, rendendo l’esperienza di ricerca complicata e soggetta a errori. Con questa correzione, [!UICONTROL Ricerca avanzata] offre ora suggerimenti rilevanti per la digitazione degli utenti, migliorando l&#39;usabilità e riducendo l&#39;attrito nella ricerca dei prodotti. (TGT-52008)
* **Sono stati risolti diversi problemi relativi all&#39;interfaccia utente e ai filtri per migliorare la reattività e l&#39;interazione dell&#39;entità**: sono stati risolti diversi problemi, tra cui la scarsa reattività dei dettagli dei criteri su dispositivi con schermo ridotto, la mancanza di risultati durante la selezione di &quot;Tutti i gruppi host&quot; nel filtro Ambiente e l&#39;impossibilità di interagire con entità senza nome. Queste correzioni migliorano l’usabilità tra le dimensioni dello schermo, garantiscono un filtraggio accurato e consentono la piena interazione con tutte le entità prodotto, migliorando l’esperienza complessiva per gli utenti. (TGT-52992)
* **Sono stati corretti gli ID di prodotto mancanti nella visualizzazione dei dettagli dei consigli durante la creazione dell&#39;attività**: è stato risolto un problema nel processo di creazione delle attività [!DNL Recommendations] a causa del quale gli ID di prodotto mancavano dalla schermata dei dettagli del prodotto, rendendo difficile per i clienti copiare o fare riferimento agli ID di prodotto durante i flussi di lavoro. Gli ID prodotto vengono ora visualizzati chiaramente nella visualizzazione dettagliata, migliorando la visibilità e supportando una gestione più efficiente dei prodotti per i clienti. (TGT-51964)
* **È stato risolto un problema nel processo di creazione attività a causa del quale i messaggi di prodotto non venivano visualizzati nella visualizzazione Consigli**: è stato risolto un problema nel processo di creazione attività a causa del quale la colonna [!UICONTROL Messaggio] nella visualizzazione [!DNL Recommendations] non visualizzava i dati di prodotto, anche se i messaggi erano presenti. I clienti hanno dovuto rimuovere manualmente e aggiungere nuovamente la colonna per visualizzare temporaneamente il contenuto, che spesso scompariva nuovamente durante lo scorrimento o la ricerca. Questo aggiornamento ripristina una visibilità coerente dei messaggi dei prodotti, migliorando la navigazione del catalogo e i flussi di lavoro di revisione. (TGT-52777)
* **È stato risolto un problema nel processo di creazione attività a causa del quale la selezione di &#39;Tutti i gruppi di host&#39; non restituiva alcun risultato nella visualizzazione Consigli**: è stato risolto un problema nel processo di creazione attività a causa del quale la selezione dell&#39;ambiente &quot;Tutti i gruppi di host&quot; nella visualizzazione [!DNL Recommendations] non restituiva alcun risultato. Ora i clienti possono visualizzare i dati dei prodotti in tutti i gruppi di host come previsto, migliorando la visibilità e la precisione dei filtri durante la configurazione dell’attività. (TGT-53006)
* **È stato risolto un problema nel processo di creazione attività a causa del quale l&#39;attivazione/disattivazione della promozione iniziale non persisteva dopo il salvataggio**: è stato risolto un problema nel processo di creazione attività a causa del quale la disattivazione dell&#39;attivazione/disattivazione della promozione iniziale nelle impostazioni attività non persisteva dopo il salvataggio. I clienti che tentavano di rimuovere la promozione iniziale hanno riscontrato che l’interruttore era stato riattivato al momento della revisione dell’attività, impedendo la corretta personalizzazione. Questo aggiornamento consente di salvare le modifiche in modo affidabile, offrendo ai clienti pieno controllo sulle impostazioni di promozione. (TGT-53215)
* **È stato corretto un ordinamento incoerente in base a [!UICONTROL Ultimo aggiornamento] colonna:** È stato risolto un problema nel processo di creazione attività a causa del quale l&#39;ordinamento del catalogo in base alla colonna [!UICONTROL Ultimo aggiornamento] generava risultati incoerenti. I clienti non erano in grado di organizzare in modo affidabile i dati dei prodotti in base alle marche temporali degli aggiornamenti, rendendo più difficile la revisione e la gestione del catalogo. L’ordinamento ora funziona come previsto, migliorando precisione e usabilità nell’interfaccia utente aggiornata. (TGT-53116)

+++

**Compositore esperienza visivo**

+++Vedi i dettagli

* **Sono stati risolti i problemi relativi al caricamento dell&#39;attività e al pulsante [!UICONTROL Annulla] nel processo di creazione attività**: è stato risolto un problema nel processo di creazione attività a causa del quale alcune attività non venivano caricate, impedendo ai clienti di accedere alle modifiche. Inoltre, il pulsante [!UICONTROL Annulla] non rispondeva, impedendo ai clienti di interrompere il processo di caricamento o uscire dalla visualizzazione di modifica. Questa correzione assicura che le attività ora vengano caricate in modo affidabile e che il pulsante [!UICONTROL Annulla] funzioni come previsto, migliorando la stabilità complessiva e l&#39;esperienza utente nel Compositore esperienza visivo. (VEC)(TGT-53218)
* **È stato risolto un problema di cambio di esperienza nell&#39;interfaccia utente del Compositore esperienza visivo aggiornata che impediva la modifica e disabilitava il pulsante [!UICONTROL Annulla]**: è stato risolto un problema nell&#39;interfaccia utente del Compositore esperienza visivo aggiornata in cui non veniva possibile caricare le modifiche quando si passava da un&#39;esperienza all&#39;altra in un&#39;attività Targeting esperienza. I clienti non sono stati in grado di modificare le esperienze oltre a quella immessa inizialmente e il pulsante [!UICONTROL Annulla] risulta mancante o non risponde. Questa correzione assicura che le modifiche ora vengano caricate correttamente in tutte le esperienze e che il pulsante [!UICONTROL Annulla] funzioni in modo affidabile, anche senza l&#39;estensione Helper, migliorando i flussi di lavoro di modifica e riducendo la frustrazione. (TGT-53256)
* **È stato risolto un problema relativo alla schermata bianca durante il passaggio tra più esperienze nel processo di creazione attività**: è stato risolto un problema che causava la visualizzazione di una schermata bianca durante il passaggio tra più esperienze. È stato inoltre risolto un problema nel processo di creazione delle attività a causa del quale i clienti riscontravano una schermata bianca durante il tentativo di modificare più esperienze all’interno di un’attività. Questo problema si verificava dopo aver applicato le modifiche a due esperienze e aver selezionato una terza esperienza, impedendo ulteriori modifiche. L’aggiornamento garantisce una transizione fluida tra le esperienze, consentendo ai clienti di apportare modifiche senza interruzioni. (TGT-53266)
* **È stato risolto un problema nel Compositore esperienza visivo a causa del quale le modifiche al codice personalizzato non venivano salvate in modo affidabile nelle sessioni di modifica**: è stato risolto un problema a causa del quale le modifiche al codice personalizzato apportate nel Compositore esperienza visivo non venivano salvate in modo affidabile in un singolo tentativo. I clienti hanno segnalato che le modifiche, come gli aggiornamenti degli stili o le modifiche di HTML, mancavano in modo intermittente dal sito Web e dagli URL di controllo qualità, anche dopo aver utilizzato sia il pulsante [!UICONTROL Modifica contenuto] che il pulsante [!UICONTROL Salva] finale. Questa regressione è stata risolta, garantendo che tutte le modifiche al codice personalizzato persistano come previsto tra le sessioni di modifica.** (TGT-53418)
* **Correzione di `triggerViews` mancante nell&#39;interfaccia utente aggiornata durante la creazione dell&#39;attività**: è stato risolto un problema nel processo di creazione dell&#39;attività a causa del quale `triggerViews` non venivano visualizzati nell&#39;interfaccia utente aggiornata, anche se erano stati implementati correttamente nella pagina. Questo problema ha interessato più clienti e ha reso difficile convalidare i trigger basati sulla visualizzazione durante la configurazione dell’attività. `TriggerViews` ora viene visualizzato come previsto, consentendo ai clienti di completare e testare le proprie configurazioni in modo affidabile. (TGT-53239)
* **È stato risolto un problema nel caricamento delle visualizzazioni nel processo di creazione attività per pagine Web specifiche nell&#39;interfaccia utente aggiornata**: è stato risolto un problema nel processo di creazione attività a causa del quale le visualizzazioni non venivano caricate nell&#39;interfaccia utente aggiornata per pagine Web specifiche, nonostante fossero correttamente implementate e visibili nelle chiamate di consegna o di interazione. Questo problema interessava più clienti e rendeva difficile convalidare il targeting basato sulla visualizzazione. Le visualizzazioni ora si compilano in modo coerente tra le pagine supportate, migliorando l’affidabilità durante la configurazione dell’attività. (TGT-53246)
* **È stato risolto un problema relativo al caricamento intermittente delle visualizzazioni nel processo di creazione attività nell&#39;interfaccia utente aggiornata**: è stato risolto un problema nel processo di creazione attività a causa del quale le visualizzazioni non venivano visualizzate in modo intermittente nell&#39;interfaccia utente aggiornata durante la modifica delle attività. Anche se il nome della visualizzazione corretto era presente nel payload di rete, non veniva riconosciuto in modo coerente nell’interfaccia, influendo sulla capacità dei clienti di configurare la personalizzazione basata sulla visualizzazione. Le visualizzazioni ora vengono visualizzate in modo affidabile, supportando una configurazione e flussi di lavoro di convalida più fluidi. (TGT-53223)
* **È stato risolto un problema nel processo di creazione attività a causa del quale i nomi delle azioni tracciate non venivano salvati nell&#39;interfaccia utente aggiornata**: è stato risolto un problema nel processo di creazione attività a causa del quale le metriche delle azioni tracciate non potevano essere salvate nell&#39;interfaccia utente aggiornata. Dopo aver assegnato un nome a un elemento tracciato e aver salvato l’attività, quando viene riaperto il nome viene reimpostato su un’etichetta predefinita, creando confusione e interrompendo la configurazione dell’obiettivo. Le azioni tracciate ora mantengono i nomi assegnati, consentendo ai clienti di impostare e gestire con precisione le metriche di conversione. (TGT-53453)

+++

### [!DNL Target Standard/Premium] 25.8.1 (7 agosto 2025)

Questa versione di include i miglioramenti e le correzioni seguenti:

**Attività**

+++Vedi i dettagli

* Sono stati risolti diversi problemi relativi all’interfaccia utente aggiornata, tra cui errori durante l’eliminazione dei tipi di pagina a causa della spaziatura nei valori di input, della copia di attività inaffidabile tra aree di lavoro e del malfunzionamento delle regole di consegna pagine negli ambienti di controllo qualità. (TGT-52703)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale gli utenti con ruolo [!UICONTROL Editor] potevano accedere e tentare di modificare le attività live, che dovevano essere limitate. Le schermate elenco attività e panoramica mostravano erroneamente le opzioni di modifica per le attività live, con possibili modifiche non desiderate. (TGT-53055)
* È stato risolto un problema nell&#39;interfaccia utente di [!UICONTROL Ricerca avanzata] a causa del quale la selezione di &quot;valore presente&quot; o &quot;valore non presente&quot; richiedeva agli utenti di immettere un operando, che non dovrebbe essere richiesto per queste condizioni. (TGT-51961)
* È stato risolto un problema nell’interfaccia utente aggiornata a causa del quale i tentativi di copiare le attività dall’area di lavoro di staging all’area di lavoro di produzione continuavano a non riuscire, anche negli ambienti sandbox. I clienti hanno riscontrato diversi messaggi di errore, tra cui &quot;Pubblico anonimo già utilizzato dall’attività&quot; e &quot;ID pubblico non valido&quot;, nonostante l’utilizzo di configurazioni valide e l’esistenza di autorizzazioni Workspace appropriate. (TGT-52394)

+++

**Frammenti esperienza (XF)**

+++Vedi i dettagli

* È stato risolto un problema che impediva il rendering del contenuto del frammento di esperienza (XF) nell&#39;anteprima del [!UICONTROL Compositore esperienza visivo], nonostante il corretto funzionamento nella distribuzione dei contenuti. (TGT-53318)

+++

**Localizzazione**

+++Vedi i dettagli

* È stato risolto un problema di localizzazione a causa del quale il pulsante &quot;Aggiungi promozione&quot; nella sezione &quot;Promozioni&quot; appariva non localizzato in più ambienti di lingua nel tenant QA. (TGT-53263)

+++

**Offerte**

+++Vedi i dettagli

* È stato risolto un problema a causa del quale la modifica di un’offerta HTML esistente tramite il Compositore esperienza visivo causava la rimozione di tutte le modifiche dalla distribuzione del contenuto. Le modifiche vengono visualizzate in grigio nella scheda delle modifiche e non vengono riportate nelle anteprime di controllo qualità, anche se vengono applicate correttamente nell’interfaccia utente precedente. (TGT-52863)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale le modifiche apportate alle offerte HTML nel [!UICONTROL Compositore esperienza visivo] non persistevano dopo essere tornate dalla scheda [!UICONTROL Targeting] a [!UICONTROL Esperienze]. (TGT-52874)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale l&#39;inserimento di un&#39;offerta HTML prima e un&#39;offerta dopo lo stesso selettore causava una generazione errata della posizione. Quando i clienti sono tornati dalla scheda [!UICONTROL Targeting] alla scheda [!UICONTROL Esperienza], è stato mantenuto un solo selettore, con conseguente perdita di modifiche e mancata distribuzione dei contenuti. Questo comportamento è diverso dall’interfaccia utente legacy, che mantiene correttamente entrambe le modifiche con identificatori di posizione distinti. (TGT-52891)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale facendo clic su un&#39;offerta aggiunta nella barra [!UICONTROL Modifiche] il pannello [!UICONTROL Configurazione] di destra veniva visualizzato e scompariva in modo intermittente, rendendo difficile l&#39;interazione con le impostazioni dell&#39;offerta. (TGT-53288)
* È stato risolto un problema a causa del quale le offerte HTML aggiunte alle varianti specifiche per il pubblico all’interno di un’attività non venivano salvate o visualizzate in modo coerente nella sezione delle modifiche. Dopo il passaggio da un pubblico all’altro durante la modifica, le offerte applicate in precedenza a volte scomparivano o non venivano riprodotte, interrompendo la convalida e ritardando la preparazione dell’attività. (TGT-53440)
* È stato risolto un problema che causava la creazione di offerte duplicate nella nuova attività durante la copia di un’attività che includeva offerte. Questo comportamento ha causato confusione e confusione inutili, in particolare durante lo spostamento di attività tra aree di lavoro. La correzione assicura che le offerte [!DNL Target] vengano ora copiate correttamente nell&#39;area di lavoro di destinazione senza duplicazioni, semplificando la gestione delle attività e migliorando l&#39;efficienza del flusso di lavoro. (TGT-53454)

+++

**Applicazioni a pagina singola**

+++Vedi i dettagli

* È stato risolto un problema nel Compositore esperienza visivo aggiornato che impediva ai clienti di applicare modifiche alle [!UICONTROL visualizzazioni delle applicazioni a pagina singola] (SPA). Le attività create nella vecchia interfaccia supportavano il targeting specifico della vista, ma la nuova interfaccia non riusciva a rilevare o consentire modifiche a tali viste, con i controlli per il cambio di vista disabilitati. (TGT-52556)

+++

**Compositore esperienza visivo**

+++Vedi i dettagli

* È stato risolto un problema a causa del quale le modifiche apportate alle esperienze all&#39;interno del [!UICONTROL Compositore esperienza visivo] non erano visibili o risultavano incoerenti nell&#39;interfaccia utente. (TGT-TGT-53381)
* È stato risolto un problema nel Compositore esperienza visivo aggiornato a causa del quale nella sezione [!UICONTROL Gestione contenuto] non veniva visualizzato il testo alternativo per le miniature dell&#39;esperienza. Questo problema rendeva difficile per gli utenti identificare i documenti, soprattutto quando i nomi dei file erano lunghi o troncati. (TGT-52291)
* È stato corretto un errore a causa del quale i clienti riscontravano errori di convalida non corretti durante la configurazione delle regole di [!UICONTROL consegna pagine] nelle attività del Compositore esperienza visivo. In particolare, operatori come &quot;è uguale a&quot; e &quot;è diverso da&quot; hanno attivato &quot;Input non valido per il tipo di operatore&quot; durante l’immissione di valori di testo, anche se il testo dovrebbe essere supportato. (TGT-52629)
* Sono stati risolti diversi problemi che causavano un comportamento incoerente nel pannello [!UICONTROL Modifiche] dell&#39;interfaccia utente aggiornata durante la selezione delle offerte tramite il pulsante &quot;Seleziona un&#39;offerta&quot;. Invece di sostituire l&#39;offerta esistente, l&#39;interfaccia utente ha aggiunto un duplicato e ha tentato di interagire con una delle offerte causando errori della console come `selectorNotFound`. Inoltre, alcune offerte non visualizzano il pulsante &quot;Seleziona un’offerta&quot;, che mostra solo le proprietà modificabili. (TGT-53321)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale le modifiche al codice HTML apportate durante la configurazione dell&#39;attività non persistevano nelle pagine delle varianti, anche se venivano salvate correttamente per i gruppi di controllo. Nonostante diversi tentativi di ricreare i test senza raggruppamenti di pagine, le pagine delle varianti non sono riuscite a mantenere le modifiche, con un conseguente impatto sulla distribuzione dei contenuti e sulla convalida del controllo qualità. (TGT-53436)
* È stato risolto un problema nel Compositore esperienza visivo aggiornato a causa del quale l’operatore &quot;è uguale a qualsiasi di&quot; nelle regole di consegna pagina non accettava i valori di input. Durante la configurazione dei parametri del cliente in tutte le mbox, la selezione di questo operatore causava un errore di &quot;Input non valido&quot;, impedendo la creazione della regola. (TGT-52623)

+++

**Aree di lavoro**

+++Vedi i dettagli

* È stato migliorato il flusso di lavoro durante la copia delle attività tra aree di lavoro. Le attività di copia tra aree di lavoro prima causavano errori di sincronizzazione a causa di tipi di pubblico mancanti e proprietà non assegnate. Questo aggiornamento introduce un flusso di lavoro più intelligente e intuitivo che garantisce che le attività copiate siano configurate correttamente e pronte per la pubblicazione. (TGT-47094)
* È stato risolto un problema che impediva ai clienti di copiare le attività tra aree di lavoro a causa di un errore nella mutazione `copyActivityBatchOperations`. I tentativi di duplicare le attività hanno restituito un errore del server (500) e un payload di risposta nullo. (TGT-52405)
* È stato risolto un problema che impediva la sincronizzazione delle attività quando le offerte a cui si faceva riferimento nella configurazione non erano accessibili all’interno dell’area di lavoro selezionata. Ciò causava errori di pubblicazione e lasciava le attività in uno stato di errore. (TGT-52535)
* Sono stati risolti diversi problemi che si verificavano durante la copia di attività tra aree di lavoro nell&#39;interfaccia utente [!DNL Target] aggiornata. I clienti hanno riscontrato errori relativi all&#39;accesso ai tipi di pubblico, in particolare con le attività live, e una convalida dei privilegi non corretta, anche quando l&#39;utente aveva &quot;[!UICONTROL Approvatore]&quot; ruoli nelle aree di lavoro di origine e di destinazione. (TGT-53002)
* È stato risolto un problema nell’interfaccia utente aggiornata a causa del quale la copia delle attività all’interno della stessa area di lavoro duplicava inutilmente le offerte e i tipi di pubblico associati. (TGT-53457)
* È stato risolto un problema per risolvere i casi in cui i tipi di pubblico ad hoc (anonimi) non venivano copiati correttamente tra aree di lavoro non predefinite o da aree di lavoro non predefinite a predefinite. Anche se gli aggiornamenti precedenti garantivano la duplicazione corretta per gli scenari predefiniti-non-predefiniti e same-Workspace, questo miglioramento si concentra sul mantenimento di configurazioni di pubblico combinate che si estendono su più aree di lavoro. La correzione garantisce un comportamento coerente del pubblico e un targeting accurato in tutte le transizioni dell’area di lavoro. (TGT-53268)

+++

### [!DNL Target Standard/Premium] 25.7.4 (1 agosto 2025)

Questa versione risolve i problemi recenti, causati principalmente da complesse personalizzazioni dei clienti, e include le correzioni e i miglioramenti seguenti:

**Attività**

+++Vedi i dettagli

* È stato risolto un problema a causa del quale un cliente riscontrava un errore di tipo &quot;Input utente non valido&quot; durante il tentativo di salvare un’attività live, anche senza apportare modifiche. La risposta di GraphQL indica un problema LocalId duplicato. (TGT-53329, TGT-53373 e TGT-53195)
* È stato risolto un problema che impediva la creazione di un’esperienza di reindirizzamento nel Compositore esperienza visivo aggiornato. L’URL di reindirizzamento è stato ignorato ed è stata visualizzata la pagina originale. (TGT-53306)

+++

**Localizzazione**

+++Vedi i dettagli

* È stato risolto un problema di localizzazione nella finestra modale [!UICONTROL Crea criterio] quando si selezionava l&#39;opzione &quot;tra i seguenti valori&quot; nell&#39;elenco a discesa [!UICONTROL Scegli regola prezzo], la stringa &quot;a&quot; veniva slocalizzata nella sezione [!UICONTROL Regole di inclusione]. (TGT-49754)
* È stato risolto un problema di localizzazione con la stringa &quot;[!UICONTROL Tutti i gruppi di host]&quot; nell&#39;elenco a discesa [!UICONTROL Ambiente] della procedura guidata di creazione dei feed non localizzati correttamente. (TGT-46737)

+++

**QA**

+++Vedi i dettagli

* È stato risolto un problema che impediva all’ambiente di controllo qualità di caricare i dati in più schede, rendendo l’interfaccia inutilizzabile. (TGT-53377)
* È stato risolto un problema che impediva la creazione di un’attività nell’ambiente di controllo qualità. Il processo è stato reindirizzato alla pagina [!UICONTROL Attività] invece di essere completato correttamente. (TGT-53328)

+++

**Funzione Consigli**

+++Vedi i dettagli

* È stato risolto un problema che causava l&#39;arresto anomalo della pagina quando si passava il mouse sull&#39;operando di &quot;apprendimento profondo&quot; durante la creazione di una raccolta in [!DNL Recommendations]. (TGT-53305)
* È stato risolto un problema a causa del quale i suggerimenti del filtro in [!UICONTROL Ricerca nel catalogo] nell&#39;interfaccia utente aggiornata non erano accurati. (TGT-52007)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Recommendations] a causa del quale veniva visualizzato il filtro Operandi quando si utilizzavano gli operatori &quot;value is present&quot; (valore presente) o &quot;value is not present&quot; (valore non presente), anche se doveva essere nascosto. (TGT-53012)

+++

**Compositore esperienza visivo**

+++Vedi i dettagli

* È stato risolto un problema che si verificava quando un utente faceva clic su [!UICONTROL Gestisci contenuto] e poi su [!UICONTROL Fine] durante la modifica di un&#39;attività di Automated Personalization (AP), la pagina restava vuota e non rispondeva. (TGT-53047 e TGT-52993)
* È stato risolto un problema che causava l&#39;arresto anomalo della pagina a causa della selezione della metrica di conversione [!UICONTROL Visualizzazione di una mbox] in [!UICONTROL Obiettivi e impostazioni]. (TGT-53346, TGT-53343, TGT-53348)
* È stato risolto un problema che impediva il funzionamento previsto della funzione [!UICONTROL Reindirizza all&#39;URL]. Il reindirizzamento non viene eseguito anche con URL validi. (TGT-53307)

+++

**Aree di lavoro**

+++Vedi i dettagli

* È stato risolto un problema che si verificava durante la copia di attività tra aree di lavoro causava la duplicazione di voci &quot;Copia pubblico&quot; e conflitti di ID. I tipi di pubblico vengono ora copiati con ID univoci, contesto dell’area di lavoro e gestione ricorsiva per i tipi di pubblico combinati (fino a 5 livelli). (TGT-53081)
* È stato risolto un problema che si verificava se l&#39;area di lavoro era impostata su &quot;[!UICONTROL Tutte le aree di lavoro]&quot;. La copia di un&#39;attività già esistente nell&#39;area di lavoro predefinita generava un errore errato:

  &quot;È necessario includere almeno una proprietà per le aree di lavoro non predefinite.&quot;

  Poiché la copia si trova nell’area di lavoro predefinita, non è richiesta alcuna proprietà. Se si tenta di aggiungere una proprietà e salvare, viene generato un secondo errore:

  &quot;Input utente non valido&quot;

+++

### [!DNL Target Standard/Premium] 25.7.3 (venerdì 24 luglio 2025)

A causa dei problemi recenti identificati, principalmente correlati a complesse personalizzazioni dei clienti, questa versione include le correzioni e gli aggiornamenti seguenti:

**Attività**

+++Vedi i dettagli

* È stato risolto un problema a causa del quale il metodo `buildViews` nella classe del generatore impostava erroneamente `viewMaxLocalId` sul numero totale di visualizzazioni, anziché sul numero massimo di `viewLocalId` assegnate. (TGT-53207)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale le offerte eliminate nelle attività [!UICONTROL Automated Personalization] (AP) venivano visualizzate come `Deleted option with ID: X` invece dei nomi originali (ad esempio, `Offer Name [Deleted]` come mostrato nell&#39;interfaccia utente legacy). Questa correzione ripristina un’etichettatura significativa per le offerte eliminate, migliorando la chiarezza e rendendo il reporting più preciso e intuitivo. (TGT-52921)
* È stato risolto un problema a causa del quale alcune attività migrate dal front-end [!DNL Target] a [!DNL Target] Central presentavano configurazioni di metriche incoerenti a causa di un bug di sincronizzazione precedentemente corretto. In particolare, le attività che originariamente utilizzavano una metrica di conversione e successivamente venivano aggiornate a una metrica basata su Analytics mantenevano valori obsoleti nei campi `primaryMetricType` e `successCriteria`. (TGT-52643)
* È stato risolto un problema che rendeva modificabile l&#39;intero contenuto di una pagina di anteprima Controllo di qualità a causa dell&#39;inclusione involontaria dell&#39;attributo `contentEditable` nelle modifiche di HTML. Questo consentiva agli utenti di fare clic e modificare qualsiasi testo nella pagina, causando potenzialmente problemi di layout e confusione durante il controllo qualità. (TGT-53247)
* È stato risolto un problema a causa del quale lo spostamento di una modifica da [!DNL Page Load] a [!UICONTROL Visualizzazione] causava la duplicazione della modifica, che rimaneva in [!UICONTROL Caricamento pagina] pur comparendo in [!UICONTROL Visualizzazione]. Inoltre, se si rimuove la modifica dalla [!UICONTROL Visualizzazione], questa verrà rimossa erroneamente anche dal [!UICONTROL Caricamento pagina]. (TGT-53270)

+++

**API**

+++Vedi i dettagli

* È stato risolto un problema nel livello di persistenza back-end a causa del quale le opzioni eliminate venivano memorizzate correttamente ma non erano accessibili tramite gli endpoint API esistenti. Di conseguenza, le applicazioni front-end non sono state in grado di recuperare nomi significativi per le opzioni eliminate, con un impatto sulle visualizzazioni cronologiche dei rapporti. Questa correzione assicura che i dati delle opzioni eliminati conservati possano ora essere visualizzati correttamente nell’interfaccia utente. (TGT-52973)
* È stato implementato un nuovo endpoint di migrazione per supportare il trasferimento delle opzioni di attività eliminate dalle attività basate su JCR a [!DNL Target] Central. Questa funzionalità consente di eseguire il tracciamento e il reporting in modo coerente tra i sistemi. Questa funzione garantisce che le opzioni eliminate vengano mantenute e sincronizzate nel front-end e nel back-end di [!DNL Target], migliorando l&#39;integrità dei dati e dei report cronologici. (TGT-53217)
* È stato introdotto un nuovo endpoint API che consente agli utenti di ripristinare da un database secondario le opzioni delle attività precedentemente eliminate. Questa funzionalità sfrutta l&#39;infrastruttura esistente fornita dalle classi `RemovedCampaignElements` e `RemovedOptionInfo`, garantendo la perfetta reintegrazione delle opzioni eliminate nelle attività attive. (TGT-52903)
* È stato risolto un problema che impediva l&#39;apertura o la modifica di [!DNL Recommendations] attività contenenti nomi di metriche con più di 25 caratteri a causa di limitazioni API. Questa correzione assicura la compatibilità con i nomi delle metriche che superano il limite di caratteri, ripristinando l’accesso completo alle attività interessate. (TGT-52839)

+++

**Compositore esperienza basato su moduli**

+++Vedi i dettagli

* È stato risolto un problema in [!UICONTROL Compositore esperienza basato su moduli] che causava l&#39;arresto anomalo dell&#39;editor dopo aver fatto clic sull&#39;icona **[!UICONTROL Gestisci contenuto]** ( ![icona Gestisci contenuto](/help/main/assets/icons/Experience.svg) ) durante la creazione o la modifica di un&#39;attività [!UICONTROL Automated Personalization] (AP). (TGT-53047)

+++

**Funzione Consigli**

+++Vedi i dettagli

* È stato risolto un problema che impediva a [!UICONTROL Ricerca nel catalogo] di caricare risultati aggiuntivi durante lo scorrimento alla fine dell&#39;elenco, ripristinando un comportamento coerente con l&#39;interfaccia utente legacy. (TGT-53088)
* È stato risolto un problema che impediva l&#39;eliminazione di elementi dalla finestra di dialogo [!UICONTROL Dettagli criteri]. (TGT-53245)
* È stato risolto un problema che impediva l’apertura o l’interazione con prodotti senza nome. Questo problema si verificava durante la selezione di ambienti che restituivano risultati senza nome, impedendo l’accesso ai dettagli del prodotto. (TGT-53007)
* È stato risolto un problema che causava l&#39;arresto anomalo della pagina [!UICONTROL Ricerca nel catalogo] e la visualizzazione di una schermata vuota durante la selezione di alcuni prodotti. (TGT-53087)
* È stato risolto un problema che impediva agli utenti di modificare l&#39;attività site_cart_z1 [!DNL Recommendation] nell&#39;interfaccia utente [!DNL Target]. Il tentativo di aprire l&#39;attività ha generato un errore nella pagina [!UICONTROL Panoramica], bloccando l&#39;accesso all&#39;editor. (TGT-53221)

+++

**Generazione di rapporti**

+++Vedi i dettagli

* È stato risolto un problema che impediva la cancellazione del campo sandbox nel database delle attività quando si cambiava l&#39;origine per la generazione di rapporti da [!DNL Customer Journey Analytics] o [!DNL Analytics] a [!DNL Target]. In precedenza, l’interfaccia utente inviava correttamente sandbox: null, ma il backend ignorava questo valore, lasciando sul posto i dati sandbox obsoleti. Il backend ora cancella correttamente il campo sandbox quando viene ricevuto null. (TGT-52798)
* È stato reimplementato il livello di persistenza delle opzioni eliminate nel backend di Target per supportare rapporti cronologici accurati nelle attività [!UICONTROL Automated Personalization] (AP). In precedenza, quando un’opzione veniva eliminata, il suo nome andava perso, rendendo difficile l’interpretazione dei dati sulle prestazioni passati.

  **Miglioramenti chiave**:

  * Le opzioni eliminate vengono ora tracciate utilizzando l&#39;infrastruttura esistente `RemovedCampaignElements` e `RemovedOptionInfo`.
  * Quando un’opzione viene rimossa da un’attività di Personalizzazione automatizzata, i relativi metadati (ad esempio, ID e nome) vengono mantenuti.
  * L&#39;interfaccia utente di reporting può ora visualizzare il nome dell&#39;opzione originale (ad esempio, `Option Name [Deleted]`) insieme alle metriche cronologiche, migliorando la chiarezza e l&#39;usabilità.

  Questo aggiornamento assicura rapporti coerenti e significativi, anche dopo la rimozione di opzioni da un’attività. (TGT-52986)

+++

**Compositore esperienza visivo**

+++Vedi i dettagli

* È stato risolto un problema nel Compositore esperienza visivo a causa del quale l’applicazione di una modifica a una visualizzazione causava la duplicazione e attivava un errore di tipo &quot;Input utente non valido&quot;. (TGT-52886)
* È stato risolto un problema relativo alla funzionalità [!UICONTROL Annulla] per le opzioni [!UICONTROL Inserisci prima] e [!UICONTROL Inserisci dopo] durante la configurazione delle offerte di immagini nel Compositore esperienza visivo.

  In precedenza, l&#39;annullamento di un&#39;azione [!UICONTROL Inserisci prima] o [!UICONTROL Inserisci dopo] sulle offerte di immagini causava un comportamento incoerente o il mancato ripristino corretto della modifica, in particolare nelle attività create nell&#39;interfaccia utente legacy di [!DNL Target]. Questo problema è stato risolto per garantire che le azioni di annullamento ora funzionino in modo affidabile per queste modifiche. (TGT-52809)

* È stato risolto un problema che causava l&#39;impostazione involontaria dell&#39;attributo `contentEditable` su true e persisteva nel contenuto HTML salvato. Questo aggiornamento garantisce un output HTML più pulito e atteso senza un comportamento di modifica non intenzionale. (TGT-52319)
* Per evitare la perdita permanente delle opzioni eliminate e garantire un comportamento coerente tra i servizi, è stata implementata la funzionalità di eliminazione temporanea per le opzioni nell’interfaccia utente e nei microservizi correlati.

  **Modifiche chiave**:

  * Le opzioni non vengono più eliminate definitivamente. Vengono invece contrassegnati con un nuovo flag eliminato: true nell&#39;oggetto XML dei parametri.
  * Questo flag viene utilizzato solo dall&#39;interfaccia utente [!DNL Target] aggiornata per escludere dal rendering le opzioni eliminate e per impedire che vengano inviate ai servizi Edge.
  * Le opzioni eliminate rimangono parte del payload dell’attività durante le modifiche, garantendo la tracciabilità ed evitando la consegna ai clienti di opzioni inesistenti.

  Questo aggiornamento migliora l’integrità dei dati e si allinea alle best practice per la gestione delle eliminazioni nei sistemi distribuiti. (TGT-52726)

+++

**Aree di lavoro**

+++Vedi i dettagli

* È stato risolto un problema che si verificava durante la copia di un’attività da un’area di lavoro non predefinita a quella predefinita o tra aree di lavoro non predefinite. Le offerte ora sono duplicate con funzioni avanzate di tracciamento e denominazione per evitare conflitti.

  **Miglioramenti chiave**:
  * Le offerte vengono ricreate nell’area di lavoro di destinazione con ID e metadati aggiornati.
  * Le offerte copiate vengono rinominate utilizzando il formato: &quot;Copia nome offerta&quot; più un numero casuale o una marca temporale per garantire l’univocità.
  * Il sistema aggiorna gli stati dell’offerta e dell’attività in modo da riflettere i nuovi ID.
  * Questa funzionalità evita gli errori causati da più nomi identici di &quot;Copia offerta&quot; durante le azioni di copia ripetute.
  * Le offerte potrebbero non essere visualizzate immediatamente nell’elenco delle offerte dell’area di lavoro di destinazione, ma vengono elaborate e visualizzate in modo appropriato.

  Questo aggiornamento migliora l’affidabilità e la tracciabilità durante la gestione delle offerte in più aree di lavoro. (TGT-53080)

+++

### [!DNL Target Standard/Premium] 25.7.2 (sabato 18 luglio 2025)

A causa dei problemi recenti identificati, principalmente correlati a complesse personalizzazioni dei clienti, questa versione include le correzioni e gli aggiornamenti seguenti:

**Attività**

+++Vedi i dettagli

* È stato aggiunto un ulteriore avviso di conferma durante l’annullamento delle modifiche dell’attività con modifiche non salvate: &quot;Desideri salvare questa attività? Se non esegui il salvataggio, tutte le modifiche andranno perse.&quot; Questo messaggio consente di evitare la perdita accidentale di dati. (TGT-52865)
* È stata ripristinata la funzionalità legacy nel cursore [!UICONTROL Priority] in [!UICONTROL Obiettivi e impostazioni], consentendo ai clienti di immettere direttamente un valore numerico, come supportato nell&#39;interfaccia utente legacy. (TGT-53185 e TGT-53219)

+++

**Tipi di pubblico**

+++Vedi i dettagli

* È stato risolto un problema che impediva il salvataggio o la modifica di attività contenenti tipi di pubblico personalizzati. I clienti hanno riscontrato un messaggio di errore di tipo &quot;Impossibile completare la richiesta. Se il problema persiste, contattare [!DNL Adobe Client Care].&quot; quando si tenta di salvare le modifiche apportate a determinate attività, o anche se non le si salva. (TGT-53189)

+++

**[!UICONTROL Analytics per Target] (A4T)**

+++Vedi i dettagli

* È stato risolto un problema che si verificava quando i clienti visualizzavano i rapporti per attività specifiche nella pagina [!UICONTROL Obiettivi e impostazioni]. Il collegamento [!UICONTROL Visualizza in Analytics] puntava erroneamente all&#39;ambiente di controllo qualità invece che all&#39;ambiente di produzione. (TGT-53163)

+++

**[!UICONTROL Esperienze] e [!UICONTROL Offerte]**

+++Vedi i dettagli

* È stato risolto un problema che causava un ciclo infinito quando si richiamava `triggerView` tramite codice personalizzato. (TGT-52885)
* È stato risolto un problema che causava incongruenze tra `LocalIds` definiti per le attività e `LocalIds` utilizzati nelle definizioni delle esperienze. (TGT-52669)
* È stato risolto un problema a causa del quale nella pagina dell&#39;attività [!UICONTROL Panoramica] mancavano dei nomi delle metriche. Veniva visualizzato solo &quot;Offerta&quot; invece del nome della metrica corretto. (TGT-53054)

+++

**Compositore esperienza basato su moduli**

+++Vedi i dettagli

* È stato risolto un problema in [!UICONTROL Compositore esperienza basato su moduli] che impediva il salvataggio delle attività e attivava il messaggio di errore: &quot;Impossibile leggere le proprietà di non definito (lettura di &#39;map&#39;)&quot;. (TGT-53145)

+++

**Funzione Consigli**

+++Vedi i dettagli

* È stato risolto un problema che causava la visualizzazione dell&#39;errore &quot;Impossibile recuperare i dettagli del prodotto&quot; in seguito a un clic su un prodotto da [!UICONTROL Ricerca nel catalogo] e l&#39;apertura di un modale senza un&#39;opzione di chiusura. (TGT-53082)
* È stato risolto un problema che impediva l&#39;aggiornamento corretto di [consigli come offerte](/help/main/c-recommendations/recommendations-as-an-offer.md) nelle attività [!UICONTROL Test A/B] durante la modifica di raccolte o promozioni. (TGT-52884)
* È stato risolto un problema nell’ambiente di produzione a causa del quale, facendo clic su un’entità nell’interfaccia utente aggiornata, veniva visualizzato l’errore: &quot;Impossibile recuperare i dettagli del prodotto. Se il problema persiste, contattare [!DNL Adobe Client Care].&quot; (TGT-53071)

+++

**Rapporti**

+++Vedi i dettagli

* È stato risolto un problema a causa del quale il salvataggio dei dettagli dell’ordine in un file CSV generava un file vuoto. (TGT-52225)

+++

**[!UICONTROL Compositore esperienza visivo] (VEC)**

+++Vedi i dettagli

* È stato risolto un problema nella pagina [!UICONTROL Obiettivi e impostazioni] a causa del quale i selettori utilizzati in più esperienze non venivano evidenziati in modo coerente come selezionati. (TGT-53062)
* È stato risolto un problema che impediva la modifica dell’attività e attivava il messaggio di errore: &quot;Impossibile leggere le proprietà di non definito (lettura di &quot;map&quot;)&quot;. (TGT-53161)

+++

**Aree di lavoro**

+++Vedi i dettagli

* È stata migliorata la gestione delle offerte ad hoc quando si passa da un’area di lavoro a un’altra.
  * Quando si passa dall’area di lavoro predefinita a un’area di lavoro non predefinita (o tra aree di lavoro non predefinite), le offerte ad hoc vengono ora copiate correttamente. Durante l’inizializzazione, il contesto dell’area di lavoro viene aggiornato e all’offerta viene assegnato un nuovo ID per garantirne l’univocità.
  * Non si verificano modifiche quando si rimane all’interno della stessa area di lavoro. (TGT-53079)
* È stato risolto un problema che impediva ai clienti di [copiare attività tra aree di lavoro diverse](/help/main/c-activities/edit-activity.md#section_45A92E1DD3934523B07E71EF90C4F8B6). (TGT-52753 e TGT-47094)
* È stato risolto un problema che si verificava durante la modifica delle proprietà tra le aree di lavoro.
  * Quando si passa dall&#39;area di lavoro predefinita a un&#39;area di lavoro non predefinita, se la proprietà corrente esiste nell&#39;area di lavoro di destinazione, la proprietà viene mantenuta.
  * Se nell&#39;elenco [!UICONTROL Proprietà] viene visualizzato un avviso (è probabile che alcune proprietà non siano compatibili) e il cliente fa clic su [!UICONTROL Aggiungi] o [!UICONTROL Rimuovi] e quindi fa clic su [!UICONTROL Salva], tutte le proprietà non presenti nell&#39;area di lavoro di destinazione verranno rimosse. Se il cliente fa clic su [!UICONTROL Annulla], tutte le proprietà rimangono, anche se non esistono nell&#39;area di lavoro di destinazione. (TGT-47094)
  * Se rimani nella stessa area di lavoro o passi da un’area di lavoro non predefinita a quella predefinita o a un’altra, tutto rimane invariato. (TGT-53078)
* È stata aggiornata la logica di convalida dell’entità in modo da rispettare il contesto dell’area di lavoro originale dell’attività. Entità come [!UICONTROL Frammenti di esperienza] (XFs) ora vengono convalidate in base all&#39;area di lavoro in cui è stata creata l&#39;attività. Ad esempio, se nel workspace di default esiste un file XF e l&#39;attività viene copiata dal workspace X al workspace Y, la convalida viene comunque eseguita finché il file XF è valido nel workspace originale (predefinito). (TGT-53196)
* Supporto migliorato per la copia di tipi di pubblico ad hoc durante la duplicazione delle attività.
  * I tipi di pubblico ad hoc, tra cui metriche, rapporti, pagine e tipi di sola attività, vengono ora copiati automaticamente nei seguenti scenari:
    * Quando si copia un’attività dall’area di lavoro predefinita a un’area di lavoro non predefinita.
    * Quando copi un’attività all’interno della stessa area di lavoro. (TGT-53197)

+++

### [!DNL Target Standard/Premium] 25.7.1 (sabato 11 luglio 2025)

A causa dei problemi recenti identificati, principalmente correlati a complesse personalizzazioni dei clienti, questa versione include le correzioni e gli aggiornamenti seguenti:

**Attività**

+++Vedi i dettagli

* È stato risolto un problema a causa del quale l&#39;URL [!UICONTROL Controllo qualità attività] includeva un parametro di query non necessario: `at_preview_evaluate_as_true_audience_ids`. (TGT-52907)
* È stato risolto un problema a causa del quale gli URL di anteprima includevano erroneamente tipi di pubblico aggiuntivi oltre a quello esplicitamente digitato dall’utente. Questo comportamento è stato corretto per garantire che solo il pubblico specificato venga applicato durante la generazione di un collegamento di controllo qualità o di anteprima. (TGT-52912)
* È stato risolto un problema che impediva agli utenti di creare [!UICONTROL attività Targeting automatico] (AT) se [!UICONTROL Allocazione automatica] (AA) era selezionato per primo durante la configurazione dell&#39;allocazione del traffico. Questo problema causava un errore di convalida del back-end e impediva il salvataggio dell’attività. (TGT-53096)

+++

**Tipi di pubblico**

+++Vedi i dettagli

* È stato risolto un problema che impediva agli utenti con il ruolo [!UICONTROL Approvatore] di aggiungere o salvare perfezionamenti del pubblico per sola attività. Il tentativo di eseguire questa operazione ha generato un errore 403 Forbidden, che indica che il privilegio &quot;[editor]&quot; è obbligatorio, anche se l&#39;utente dispone di autorizzazioni sufficienti per approvare e gestire le attività. (TGT-52984)
* È stato risolto un problema che si verificava quando un pubblico specifico per l&#39;attività veniva rimosso utilizzando l&#39;opzione [!UICONTROL Rimuovi perfezionamento pubblico] e il pubblico non veniva più visualizzato nell&#39;elenco dei tipi di pubblico per essere riselezionato all&#39;interno della stessa attività. Questo comportamento impediva agli utenti di aggiungere nuovamente lo stesso pubblico, a meno che non venga ricreato da zero. (TGT-52979)
* È stato risolto un problema a causa del quale i perfezionamenti del pubblico per sola attività scomparivano dall’interfaccia utente subito dopo essere stati rimossi da una posizione, anche prima del salvataggio dell’attività. Questo comportamento contraddiceva le funzionalità previste e le linee guida con la descrizione comando, che recita: &quot;Tutti i tipi di pubblico non utilizzati da questa libreria verranno eliminati una volta salvata l’attività&quot;. (TGT-52982)
* È stato risolto un problema che si verificava durante il tentativo di assegnare un pubblico diverso da [!UICONTROL Tutti i visitatori] a un&#39;attività. Al momento del salvataggio, veniva visualizzato il seguente messaggio di errore: &quot;Impossibile completare la richiesta. Se il problema persiste, contatta l&#39;[!UICONTROL Assistenza clienti Adobe].&quot; (TGT-53008)
* È stato risolto un problema che impediva il salvataggio di un’attività dopo la creazione e l’assegnazione di un nuovo pubblico all’interno dell’editor attività. Il messaggio di errore visualizzato era: &quot;Impossibile completare la richiesta. Se il problema persiste, contatta l&#39;[!UICONTROL Assistenza clienti Adobe].&quot; (TGT-52977)

+++

**[!UICONTROL Analytics per Target] (A4T)**

+++Vedi i dettagli

* È stato risolto un problema che causava un errore &quot;Input utente non valido&quot; durante la copia di un&#39;attività esistente e la modifica dell&#39;origine per la generazione di rapporti in [!DNL Adobe Analytics] (A4T). L&#39;errore è stato attivato quando alcune azioni di metrica incompatibili con il reporting di [!DNL Analytics], come `restart_same_experience`, `restart_random_experience` e `restart_new_experience`, sono state mantenute dall&#39;attività originale. (TGT-52900)
* È stato risolto un problema che impediva ai clienti di creare o salvare un&#39;attività selezionando [!DNL Adobe Analytics] (A4T) come origine per la generazione di rapporti nel passaggio [!UICONTROL Obiettivi e impostazioni]. Il problema si è verificato in modo specifico durante la selezione di una metrica [!UICONTROL Evento personalizzato] (ad esempio, &quot;Evento personalizzato 16&quot;), causando il seguente errore: &quot;Input utente non valido&quot;. (TGT-52910)
* È stato risolto un problema a causa del quale facendo clic sul collegamento &quot;[!UICONTROL Visualizza in Analytics]&quot; gli utenti venivano reindirizzati alla home page anziché alla dashboard [!DNL Analytics] prevista. (TGT-53092 e TGT-53093)
  <!-- * Fixed an issue when cloning an existing activity and changing the reporting source from [!DNL Target] to [!DNL Adobe Analytics], users encounter a "400 - Invalid User Input" error, preventing the activity from being saved. (TGT-52875)-->
* È stato risolto un problema che si verificava durante la visualizzazione di un&#39;attività [!DNL Recommendations] nell&#39;interfaccia utente [!UICONTROL Panoramica] aggiornata. Impossibile caricare la sezione [!UICONTROL Obiettivi e impostazioni] se [!DNL Adobe Analytics] (A4T) è selezionato come origine per la generazione di rapporti. Veniva visualizzato il seguente messaggio di errore: &quot;Si è verificato un errore. Impossibile completare la richiesta. Se il problema persiste, contatta l’Assistenza clienti Adobe.” (TGT-52999)

+++

**[!UICONTROL Esperienze] e [!UICONTROL Offerte]**

+++Vedi i dettagli
<!-- * Fixed an issue where using the [!UICONTROL Manage Content] feature in [!UICONTROL Automated Personalization] (AP) activities caused the page to crash and remain blank. This issue occurred after clicking [!UICONTROL Done] in the content manager, particularly in activities created or edited in the updated UI. (TGT-53047)-->
* È stato risolto un problema che impediva alla funzionalità [!UICONTROL Gestione contenuto] di convalidare correttamente lo stato di una posizione dopo la rimozione di tutte le opzioni di contenuto. Questo problema poteva causare un comportamento incoerente o errori durante il tentativo di salvare o procedere con la configurazione dell’attività. (TGT-52801)
* È stato risolto un problema che causava la visualizzazione di un errore di tipo &quot;Input non valido&quot; durante l’aggiunta di una nuova pagina e l’eliminazione di elementi specifici in diverse esperienze. L&#39;errore viene attivato dalla generazione del duplicato `LocalIds` durante la manipolazione dell&#39;elemento, in particolare quando si passa da un&#39;esperienza all&#39;altra e si modificano le strutture di pagina condivise. (TGT-52720)
* È stato risolto un problema che causava la visualizzazione di posizioni non definite nel pannello [!UICONTROL Gestione contenuto] in seguito all&#39;utilizzo della funzione [!UICONTROL Genera offerta ad hoc]. (TGT-53076 e TGT-53070)
* È stato chiarito il comportamento del cliente in cui le modifiche apportate utilizzando un&#39;offerta HTML potrebbero sembrare mancanti quando si passa dal passaggio [!UICONTROL Targeting] a [!UICONTROL Esperienze]. Per questo cliente, il sito web interessato ha generato in modo dinamico più selettori DOM modificati a ogni caricamento di pagina. Di conseguenza, il selettore originariamente utilizzato per la modifica non viene trovato quando l’editor viene riaperto, causando la visualizzazione della modifica come mancante o non valida. Questo scenario funziona come previsto. Per garantire che le modifiche persistano visivamente nell’editor, si consiglia ai client di utilizzare selettori stabili e coerenti che non cambiano tra i ricaricamenti delle pagine. (TGT-52874)
* È stato risolto un problema a causa del quale il tentativo di eliminare o disattivare un’offerta che faceva parte di un’esperienza esclusa generava un errore di tipo &quot;Input utente non valido&quot;. Questo problema si verificava anche se l’offerta non veniva utilizzata attivamente nelle esperienze incluse. (TGT-52917)

+++

**Compositore esperienza basato su moduli**

+++Vedi i dettagli

* È stato risolto un problema nelle attività basate su moduli a causa del quale la duplicazione di un’esperienza e la modifica del codice personalizzato in una delle esperienze duplicate applicavano involontariamente tali modifiche a tutte le esperienze duplicate. Dopo la duplicazione, ora ogni esperienza conserva il proprio codice personalizzato in modo indipendente. (TGT-51600)

+++

**Localizzazione**

+++Vedi i dettagli

* Sono state aggiornate le stringhe di localizzazione nella nuova interfaccia utente per francese (fr_FR), tedesco (de_DE), italiano (it_IT), coreano (ko_KO) e cinese semplificato (zh_CN).

+++

**[!DNL Recommendations]**

+++Vedi i dettagli

* È stato aggiunto un nuovo feed [!DNL Recommendations] [status](/help/main/c-recommendations/c-products/feeds.md#status): [!UICONTROL Importazione parziale non riuscita]. (KB-2215)
* È stato risolto un problema che interessava il flusso di lavoro di creazione attività durante l&#39;aggiunta di [!DNL Recommendations] con [!UICONTROL promozioni]. Quando gli utenti hanno selezionato &quot;[!UICONTROL Promuovi per attributo]&quot; e aggiunto una regola di filtro (ad esempio, [!UICONTROL Corrispondenza parametro]), il tipo di regola e i valori dell&#39;operando selezionati non sono stati mantenuti dopo il salvataggio e la modifica dell&#39;attività. Alla riapertura, il tipo di regola di filtro cambiava in modo imprevisto e mancavano i valori dell’operando. (TGT-53059)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Recommendations] a causa del quale qualsiasi promozione creata con una singola regola veniva erroneamente interpretata e visualizzata come un tipo di promozione &quot;Elenco di elementi&quot;, indipendentemente dalla logica della regola. (TGT-53063)
* È stato risolto un problema che si verificava durante l&#39;utilizzo dell&#39;interfaccia utente [!UICONTROL Panoramica]aggiornata. Il pulsante &quot;[!UICONTROL Scarica dati consigli]&quot; era mancante per le attività [!UICONTROL Targeting esperienza] (XT) che includono [!DNL Recommendations]. (TGT-52730 e TGT-52756)
* In precedenza, nell’interfaccia utente Consigli veniva visualizzato solo il numero di entità importate correttamente da un feed. Tuttavia, il formato del messaggio di back-end include sia il numero di entità importate che il numero totale di entità nel formato: `# of entities imported / # of total entities`. A causa di questa discrepanza, gli utenti visualizzavano solo il primo valore (conteggio importato) nell’interfaccia utente, creando confusione. Ora l’interfaccia utente visualizza entrambi i numeri. (TGT-53073)
* È stato risolto un problema che impediva ai clienti di salvare una regola di filtro durante la configurazione di una promozione &quot;[!UICONTROL Promuovi per attributo]&quot; in un&#39;attività A/B basata su modulo con consigli. Dopo il salvataggio e la riapertura dell’attività, la regola di filtro risultava mancante e l’attività non poteva essere salvata correttamente. (TGT-53057)

  +++

**Rapporti**

+++Vedi i dettagli

* È stato risolto un problema che causava il download di un file vuoto durante la selezione di &quot;[!UICONTROL Esporta dettagli ordine in CSV]&quot; dalla pagina [!UICONTROL Rapporti]. Questo problema si verificava anche quando nell’attività erano presenti dati di ordine validi. (TGT-52225)
* È stato risolto un problema che si verificava durante il tentativo di salvare un’attività dopo la creazione e l’assegnazione di un nuovo pubblico di reportistica. Il messaggio di errore restituito era: &quot;Accesso negato. Per eseguire questa operazione, sono necessari tutti i privilegi seguenti: [editor].&quot; Questo problema si verificava nonostante l’utente avesse accesso a livello di approvatore. (TGT-53103)

+++

**[!UICONTROL Compositore esperienza visivo] (VEC)**

+++Vedi i dettagli

* È stato risolto un problema a causa del quale l’applicazione di una modifica a una vista determinava la duplicazione della vista e l’attività restituiva un errore di tipo &quot;Input utente non valido&quot;. Questa correzione assicura che le modifiche della visualizzazione vengano applicate correttamente senza causare errori di duplicazione o convalida. (TGT-52886)
* È stato risolto un problema che impediva la corretta visualizzazione delle modifiche al codice personalizzato in caso di esperienza errata. In particolare, le modifiche progettate per un’esperienza sono state mostrate in un’esperienza diversa, generando confusione e potenziale configurazione errata delle attività live. (TGT-52776)
* È stato risolto un problema che impediva la modifica o il salvataggio delle modifiche del codice personalizzato nella nuova interfaccia utente del Compositore esperienza visivo. In particolare:

  * Dopo aver modificato un blocco di codice personalizzato e aver salvato, le modifiche non venivano riportate nell’interfaccia utente o nell’anteprima Controllo qualità.
  * In alcuni casi, non è stato possibile eliminare le modifiche a meno che l’attività non sia stata chiusa e riaperta.
  * Come soluzione alternativa, gli utenti dovevano copiare il codice, eliminare la modifica e ricrearla manualmente con il contenuto aggiornato. (TGT-53072)

* È stato risolto un problema che causava la mancata risposta del pannello [!UICONTROL Modifiche] a causa della modifica e del salvataggio del codice personalizzato. (TGT-53075)
* È stato risolto un problema a causa del quale le modifiche apportate al codice personalizzato nelle esperienze di varianti venivano applicate involontariamente all&#39;esperienza [!UICONTROL Controllo]. Questo causava modifiche non intenzionali nel comportamento di consegna. L&#39;esperienza [!UICONTROL Controllo] ora rimane isolata dalle modifiche al codice personalizzato apportate ad altre esperienze. (TGT-52413)
* È stato risolto un problema a causa del quale le modifiche apportate a un’esperienza (ad esempio, Esperienza B) venivano duplicate involontariamente a un’altra esperienza (Esperienza A) se l’utente faceva clic sulla seconda esperienza prima del caricamento completo dell’editor. Questo comportamento potrebbe anche causare la perdita di modifiche se l’esperienza selezionata inizialmente non avesse subito modifiche. (TGT-52597)
* È stato risolto un problema a causa del quale le modifiche apportate nel passaggio [!UICONTROL Modifiche] della creazione dell&#39;attività non venivano salvate in modo coerente. In alcuni casi, dopo aver completato tutti i passaggi e aver fatto clic su [!UICONTROL Salva], lo script personalizzato aggiunto nella sezione [!UICONTROL Modifiche] non si rifletterebbe sul sito attivo, nonostante nessun errore visibile durante il processo di salvataggio. (TGT-52661)
* È stato risolto un problema a causa del quale le modifiche al codice personalizzato non venivano salvate correttamente e venivano involontariamente applicate a più esperienze all’interno della stessa attività. Inoltre, si sono verificati problemi di accesso all’apertura o all’aggiornamento di alcune attività, con la conseguente visualizzazione di schermate vuote. Questi problemi sono stati risolti per garantire una modifica stabile delle attività e un isolamento accurato delle esperienze. (TGT-52594)
* È stato risolto un problema che impediva agli utenti di passare a un URL diverso in [!UICONTROL Modalità Sfoglia]. Ciò impediva ai tester e agli editor di convalidare o visualizzare in anteprima pagine alternative all’interno della stessa sessione di attività. (TGT-53052)
* È stato risolto un problema che causava l&#39;apertura simultanea di più istanze del [!UICONTROL Compositore esperienza visivo] durante la creazione dell&#39;attività. Questo problema si verificava quando gli utenti disabilitavano il [!UICONTROL Compositore esperienza avanzato] e rimuovevano la barra finale dall&#39;URL del sito Web nel passaggio [!UICONTROL Consegna pagine]. (TGT-52782)
* È stato risolto un problema a causa del quale il menu a discesa della metrica [!UICONTROL Ricavi] nel passaggio [!UICONTROL Obiettivi e impostazioni] impostava erroneamente il valore predefinito [!UICONTROL Ricavi per visita] (RPVISIT), anche dopo che l&#39;utente aveva selezionato una metrica diversa.  Il problema si verificava durante la compressione e la nuova espansione del pannello di configurazione della metrica, causando il ripristino del valore selezionato in precedenza. (TGT-52811 e TGT-52878)
* Sono stati risolti diversi problemi nel flusso di lavoro di creazione attività relativi alla denominazione delle offerte e alla traduzione del contenuto in [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Multivariate Testing] (MVT) attività:

  Problemi chiave risolti:

  * La creazione di più offerte HTML con lo stesso nome (ad esempio, &quot;Esperienza&quot;) ha attivato l’errore &quot;I nomi di offerta duplicati non sono consentiti&quot;, ma l’interfaccia utente non indicava chiaramente quali offerte causavano il conflitto.
  * La ridenominazione delle offerte tramite il pannello di destra ha aggiornato il nome nell&#39;interfaccia utente, ma la modifica non si è riflessa nella scheda [!UICONTROL Gestisci contenuto] o nella scheda [!UICONTROL Offerte], causando errori di convalida persistenti.
  * Nelle attività MVT, anche se l’errore di nome duplicato non persisteva dopo la ridenominazione, l’interfaccia utente non riusciva ancora a riflettere i nomi delle offerte aggiornati in modo coerente tra le schede. (TGT-52933)

  +++

### [!DNL Target Standard/Premium] 25.6.4 (sabato 27 giugno 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stata aggiunta l&#39;opzione [!UICONTROL Ridisponi] all&#39;interfaccia utente aggiornata del [!UICONTROL Compositore esperienza visivo] per allinearla alle funzionalità disponibili nel Compositore esperienza visivo legacy. (TGT-46957 e TGT-52876)
* È stato risolto un problema che impediva il mantenimento delle modifiche apportate alle esperienze delle varianti (ad esempio, Esperienza B) in un&#39;attività [!UICONTROL A/B Test]. Dopo il passaggio da un’esperienza all’altra, le modifiche apportate alla variante scompaiono. Questo problema non ha influito sull’esperienza di controllo. (TGT-52664)
* È stato risolto un problema che impediva ad alcuni clienti di creare o salvare attività, mentre altri potevano eseguire le stesse azioni senza alcun problema. Il problema era incoerente tra gli account.(TGT-52842)
* È stato risolto un problema che impediva agli utenti del Compositore esperienza visivo aggiornato di spostare le modifiche all&#39;[!UICONTROL evento Caricamento pagina], una funzionalità già presente nell&#39;interfaccia utente legacy. (TGT-52617)
* È stato risolto un problema nell&#39;interfaccia utente aggiornata a causa del quale [!UICONTROL gli eventi di caricamento pagina] non erano visibili in [!DNL Target] durante la creazione di modifiche; gli aggiornamenti sono stati applicati solo alle visualizzazioni. (TGT-52604)
* È stato risolto un problema che impediva la corretta visualizzazione di alcune modifiche dell’attività nel Compositore esperienza visivo aggiornato. (TGT-52818)
* È stata corretta un&#39;eccezione Null Pointer che si verificava durante il recupero dei dati di reporting per le attività di [!UICONTROL Automated Personalization] (AP). (TGT-52362)
* È stato risolto un problema che impediva la visualizzazione dei dettagli a livello di offerta nel file .CSV per [!UICONTROL attività Automated Personalization] (AP). (TGT-52675)
* È stato risolto un problema che si verificava durante l&#39;applicazione di modifiche nel Compositore esperienza visivo aggiornato, a causa del quale le modifiche inizialmente venivano visualizzate correttamente, incluso il [!UICONTROL frammento di esperienza] previsto. Tuttavia, quando si passa da un’esperienza all’altra o si apportano ulteriori modifiche, alcune modifiche non vengono applicate a causa di problemi del selettore. (TGT-52679)
* È stato risolto un problema a causa del quale, quando veniva creata una nuova attività clonandone una esistente, i collegamenti di controllo qualità nell’attività clonata mantenevano erroneamente gli URL della pagina dall’attività originale. (TGT-52775)
* È stato risolto un problema che impediva involontariamente a [!UICONTROL Decisioning sul dispositivo] di essere disponibile nel Compositore esperienza visivo aggiornato. (TGT-52371)
* È stato risolto un problema che impediva la modifica di un&#39;attività di prodotto [!DNL Recommendations]. Quando si tenta di accedere al Compositore esperienza visivo tramite l&#39;interfaccia utente di Target, nella pagina [!UICONTROL Panoramica] viene visualizzato un errore che impedisce qualsiasi modifica. (TGT-52823)
* È stato risolto un problema che impediva il salvataggio di un&#39;attività [!DNL Recommendations] quando i nomi delle esperienze superavano i 50 caratteri. (TGT-52619)
* È stato risolto un problema che impediva ai clienti di salvare un’attività Consigli dopo la modifica dei criteri nella nuova interfaccia utente. Il problema sembra essere relativo alle autorizzazioni e non influisce su tutti gli utenti con ruoli simili. (TGT-52816)
* È stato risolto un problema che impediva agli utenti con il ruolo [!UICONTROL Editor] di modificare un&#39;attività [!DNL Recommendations]. Il tentativo di modificare la progettazione e salvare l&#39;attività ha restituito un errore 403 Forbidden, che indica che il privilegio &quot;[editor]&quot; era obbligatorio, anche se l&#39;utente aveva già quel ruolo nell&#39;area di lavoro pertinente. (TGT-52836)

### [!DNL Target Standard/Premium] 25.6.3 (sabato 20 giugno 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema a causa del quale la copia di un’attività da un’area di lavoro a un’altra causava errori quali &quot;non deve essere null&quot; o &quot;Si è verificato un errore&quot;. (TGT-52474)
* È stato risolto un problema che impediva la generazione di rapporti [!UICONTROL Segmenti automatizzati] e [!UICONTROL Attributi importanti] per alcune attività. (TGT-52904)
* È stato risolto un problema nel Compositore esperienza visivo aggiornato a causa del quale la gestione del contenuto predefinito nelle attività [!UICONTROL Automated Personalization] (AP) non corrispondeva all&#39;interfaccia utente legacy. Il sistema ora aggiunge automaticamente un `optionGroup` predefinito denominato &quot;Contenuto predefinito&quot; con `optionGroupLocalId = 0` quando nessun gruppo viene aggiunto in modo esplicito. Questo gruppo include l&#39;opzione predefinita, ad esempio `optionLocalId: 0`. Se il contenuto predefinito viene rimosso, viene rimosso anche il gruppo di opzioni corrispondente. (TGT-52651)
* È stato risolto un problema nelle attività [!UICONTROL Test multivariato] (MVT) a causa del quale il riutilizzo di un `experienceLocalId` da esperienze precedentemente rimosse non era consentito correttamente. (TGT-52672)
* È stato risolto un problema che impediva la copia o la modifica delle attività contenenti un frammento di esperienza. Questo ha attivato l&#39;errore: `Enum "AemOfferType" cannot represent value: "html"`. (TGT-52635)
* È stato risolto un problema che impediva agli URL nei percorsi di attività di visualizzare i parametri di query a causa di caratteri non validi, ad esempio barre (/). (TNT52845)
* È stato migliorato il messaggio di errore di convalida per gli aggiornamenti dell&#39;attività [!DNL A/B Test] tramite l&#39;API di back-end. Quando sono presenti nomi di posizione duplicati, il messaggio ora indica chiaramente: &quot;I nomi duplicati non sono consentiti&quot; per `locations.selectors`. (TGT-52589)
* È stato corretto un errore che si verificava durante l&#39;aggiornamento di un&#39;attività [!UICONTROL Recommendations] attiva a causa di una proprietà non riconosciuta nel payload della richiesta. Il sistema ora gestisce correttamente il codice JSON &quot;Non valido&quot;. Errore &quot;Nome proprietà non riconosciuto&quot;. (TGT-52723)
* È stato risolto un problema che impediva la creazione di una progettazione [!DNL Recommendations]. Facendo clic su [!UICONTROL Crea] è stato attivato il messaggio: &quot;Deve essere utilizzata almeno 1 variabile di entità nello script.&quot; (TGT-52395 e TGT-52899)
* È stato risolto un problema che impediva il salvataggio di una progettazione [!DNL Recommendations] senza modifiche. (TGT-52879)
* È stato corretto un errore di convalida del back-end che causava un errore &quot;400 Richiesta non valida&quot; durante il salvataggio di un&#39;attività [!UICONTROL Recommendations]. (TGT-52716)
* È stato risolto un problema in [!UICONTROL Compositore esperienza basato su moduli] a causa del quale, passando il puntatore del mouse su una mbox con caratteri speciali nell&#39;elenco a discesa [!UICONTROL Posizione], l&#39;editor diventava vuoto e si attivava un messaggio di tipo &quot;Impossibile eseguire &#39;querySelector&#39; su &#39;Elemento&#39;.&quot; errore. (TGT-52717)
* È stata migliorata la precisione dello stato di avanzamento con un nuovo indicatore &quot;PARTIALLY_IMPORTED&quot;. In precedenza, i feed venivano contrassegnati come &quot;riusciti&quot; anche quando non venivano importate tutte le righe di un file, il che era fuorviante. (TGT-52892)
* È stato corretto un errore a causa del quale, dopo la migrazione ad AP V2, alcune chiamate API a `/admin/rest/ui/v1/campaigns` restituivano errori lato client (HTTP 4xx). (TGT-52721)

### [!DNL Target Standard/Premium] 25.6.2 (venerdì 12 giugno 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato aggiunto un [nuovo articolo di domande frequenti](/help/main/c-intro/updated-ui-faq.md) per risolvere le domande comuni sull&#39;interfaccia utente [!DNL Target] e sul [!UICONTROL Compositore esperienza visivo] aggiornati.
* È stato risolto un problema che impediva il funzionamento della regola &quot;[!UICONTROL URL - does not contain]&quot; in [!UICONTROL Consegna pagine], consentendo la visualizzazione del contenuto anche quando avrebbe dovuto essere bloccato. (TGT-52754)
* È stato risolto un problema che impediva la corretta visualizzazione del messaggio di errore [!UICONTROL Consegna pagine]: &quot;Non sono consentiti URL di pagina duplicati. (TGT-52765)
* È stato risolto un problema che causava la creazione di tipi di pubblico per [!UICONTROL URL di consegna pagine] contenenti frammenti di esperienza, con # che veniva erroneamente aggiunto. (TGT-52786)
* È stato risolto un problema che causava la mancata risposta dell&#39;interfaccia utente di [!DNL Target] a causa della copia di un&#39;attività e della modifica delle impostazioni nella pagina [!UICONTROL Obiettivi e impostazioni]. (TGT-52797)
* È stato risolto un problema nel [!UICONTROL Compositore esperienza visivo] (VEC) aggiornato che consentiva erroneamente il reindirizzamento di una pagina aggiuntiva in un&#39;attività [!UICONTROL A/B Test] allo stesso URL. (TGT-51838)
* È stato risolto un problema che impediva il salvataggio delle modifiche alle metriche nella pagina [!UICONTROL Obiettivi e impostazioni] durante la modifica di un&#39;attività. (TGT-52799)
* È stato risolto un problema a causa del quale l’aggiunta di una nuova esperienza durante il caricamento dell’editor web causava la duplicazione del contenuto dell’esperienza precedente. (TGT-51397)
* È stata ripristinata la possibilità di utilizzare codice personalizzato all&#39;esterno del tag `<head>`, una funzione precedentemente disponibile nell&#39;interfaccia utente di Target precedente. (TGT-52304 e TGT-52300)
* È stata rimossa la convalida non necessaria durante la selezione dell’area di lavoro predefinita durante la creazione dell’attività. La convalida obbligatoria delle proprietà non si applica più all’area di lavoro predefinita, ma rimane attiva per le aree di lavoro non predefinite. (TGT-52449)
* È stato risolto un problema nel [!UICONTROL Compositore esperienza visivo] (VEC) aggiornato a causa del quale non venivano rilevate `triggerView()` chiamate. (TGT-52575)
* È stato risolto un problema nel [!UICONTROL Compositore esperienza visivo] (VEC) aggiornato che impediva agli utenti di aggiungere modifiche alle [!UICONTROL visualizzazioni delle applicazioni a pagina singola] (SPA). (TGT-52556)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata che impediva ai clienti di visualizzare i dettagli delle offerte. (TGT-52607)
* È stato risolto un problema a causa del quale gli aggiornamenti apportati alle offerte nella [!UICONTROL Libreria offerte] non venivano inclusi nel [!UICONTROL Compositore esperienza visivo] (VEC) aggiornato. (TGT-52637)
* È stato risolto un problema che impediva la corretta visualizzazione della sezione Offerte durante la creazione di un’attività. (TGT-52773)
* È stata aggiunta la convalida per garantire che tutti i `optionLocalIds` a cui si fa riferimento in `optionGroups` siano presenti nell&#39;array delle opzioni. I riferimenti non validi vengono rimossi automaticamente durante la creazione dell’attività. (TGT-52687)
* È stato risolto un problema a causa del quale i gruppi di reporting e le esclusioni non venivano mantenuti dopo l’aggiunta di una nuova offerta. (TGT-52728)
* È stato risolto un problema che causava la visualizzazione di un selettore di opzioni vuoto nelle attività senza un pulsante di controllo qualità [!UICONTROL Attività]. (TGT-52733)
* È stato risolto un problema che impediva il corretto rendering del contenuto dei collegamenti di controllo qualità. (TGT-52718)
* È stato risolto un problema a causa del quale la sostituzione di un elemento con un frammento di esperienza non rifletteva correttamente le modifiche nell’ambiente di controllo qualità. (TGT-52762)
* È stato risolto un problema nel [!UICONTROL Compositore esperienza visivo] (VEC) aggiornato che causava un errore &quot;Input non valido&quot; quando gli utenti tentavano di aggiungere frammenti esperienza. (TGT-52701)
* È stato risolto un problema che causava la visualizzazione del modale &quot;Modifica pubblico&quot; vuoto durante la modifica del targeting del pubblico nel [!UICONTROL Compositore esperienza visivo] (VEC) aggiornato. (TGT-52749)
* È stato aggiunto un messaggio per informare gli utenti quando un’entità non è accessibile nell’area di lavoro selezionata. (TGT-52767)
* È stato risolto un problema che impediva all’interfaccia utente di consentire l’assegnazione manuale di un ID ambiente a un criterio. Viene invece impostato automaticamente sull&#39;ID per il gruppo host [!UICONTROL Ricerca nel catalogo prodotti]. Questa correzione assicura che le modifiche ai criteri vengano ora applicate in tutti gli ambienti, non solo a quello predefinito. (TGT-52817)
* È stato risolto un problema che causava l&#39;assenza dell&#39;opzione &quot;[!UICONTROL Scarica dati Consigli]&quot; per [!UICONTROL attività Targeting esperienza] (XT) con consigli. (TGT-52730 e TGT-52756)

### [!DNL Target Standard/Premium] 25.6.1 (sabato 6 giugno 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema a causa del quale i collegamenti di controllo qualità non fornivano l’esperienza corretta per l’attività associata. (TGT-52163 e TGT-52790)
* È stato risolto un problema che causava la mancanza dell’ID del pubblico associato nei collegamenti di controllo qualità. (TGT-52722)
* È stato risolto un problema per garantire che le esperienze vengano consegnate solo quando le condizioni URL di consegna pagina configurate vengono soddisfatte con precisione. (TGT-52696)
* È stato risolto un problema che impediva ai clienti di creare un modello struttura [!DNL Recommendations]. Il tentativo di creare un modello ha attivato l’errore: &quot;Deve essere utilizzata almeno 1 variabile di entità nello script&quot;. (TGT-52395)
* È stato risolto un problema che impediva il salvataggio delle progettazioni di [!DNL Recommendations] tramite gli array Velocity. Il messaggio di errore &quot;Deve essere utilizzata almeno 1 variabile di entità nello script&quot; è stato attivato in modo errato. (TGT-52734)
* È stato risolto un problema che impediva l&#39;accesso alle modifiche nel [!UICONTROL Compositore esperienza visivo] (VEC) quando non era possibile caricare la pagina per le pagine Web interne. (TGT-52488 &amp;TGT-52470)
* È stato risolto un problema che impediva la visualizzazione del pannello [!UICONTROL Modifiche] nel Compositore esperienza visivo su schermi di dimensioni inferiori. (TGT-52470)
* È stato risolto un problema nel Compositore esperienza visivo aggiornato a causa del quale il passaggio dalla modalità [!UICONTROL Sfoglia] alla modalità [!UICONTROL Progettazione] causava un errore della console e impediva ulteriori interazioni. (TGT-52532)
* È stato risolto un problema nel Compositore esperienza visivo a causa del quale, facendo clic su alcuni elementi, le dimensioni venivano involontariamente estese. (TGT-52497)
* È stato risolto un problema che impediva il caricamento o il riconoscimento di alcuni elementi di pagina nel Compositore esperienza visivo, impedendo interazioni quali la selezione di pulsanti o banner e l’interruzione del tracciamento accurato degli eventi nelle attività. (TGT-52663)
* È stato risolto un problema che impediva ai clienti di eliminare o rimuovere le offerte nelle attività [!UICONTROL Automated Personalization] (AP). (TGT-52690)
* È stato risolto un problema che causava un comportamento incoerente di qualificazione delle attività nelle attività multipagina. (TGT-52694)
* È stato risolto un problema che causava la visualizzazione di un URL non valido per la [!UICONTROL Posizione attività] nella pagina [!UICONTROL Panoramica] dell&#39;attività. (TGT-52695)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata che causava la visualizzazione di voci duplicate per i percorsi attività. (TGT-52693)
* È stato risolto un problema che attivava un errore `getAudiencesV3`, impedendo ai clienti di modificare o copiare le attività. (TGT-52709)
* È stato risolto un problema che causava un errore di payload non valido durante l&#39;aggiunta di [!UICONTROL Frammenti di esperienza] o offerte HTML a un&#39;attività. (TGT-52779 e TGT-52773)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale E[!UICONTROL Frammenti esperienza] non venivano visualizzati correttamente a causa di un errore di input non valido. (TGT-52701)
* È stato risolto un problema che impediva ai clienti di modificare le attività nel [!UICONTROL Compositore esperienza basato su moduli] a causa di un errore utente non valido. (TGT-52470)
* È stato risolto un problema di localizzazione nella lingua coreana a causa del quale le traduzioni precedenti utilizzavano caratteri al di fuori del piano multilingue di base. La traduzione aggiornata utilizza caratteri appropriati che trasmettono con precisione il significato previsto. (TGT-52508 e TGT-52509)
* È stato risolto un problema di localizzazione nella lingua coreana a causa del quale la traduzione di &quot;date&quot; risultava incoerente quando si selezionavano le date di inizio e di fine per un’attività. (TGT-52510)

### [!DNL Target Standard/Premium] 25.5.4 (29 maggio 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva l’aggiunta o la modifica di URL in modalità di controllo qualità. (TGT-51941)
* È stata aggiunta un&#39;impostazione di traffico in modalità Controllo di qualità in [!UICONTROL Report] > [!UICONTROL Impostazioni report] ( ![Icona Impostazioni report](/help/main/assets/icons/Setting.svg) ) per allinearla alle funzionalità dell&#39;interfaccia utente legacy di [!DNL Target]. (TGT-52228 e TGT-52329)
* È stato risolto un problema che causava la generazione di collegamenti di controllo qualità errati da parte dell’attività basata su moduli. L’URL/posizione dell’attività includeva un &quot;1&quot; non voluto alla fine, che ora è stato rimosso per garantire un collegamento accurato. (TGT-52355 e TGT-52358)
* È stato risolto un problema che causava la generazione di collegamenti di controllo qualità errati da parte dell’attività basata su moduli. L&#39;URL attività includeva un `http://pid-ppc` non previsto all&#39;inizio dell&#39;URL, che ora è stato rimosso per garantire un collegamento accurato. (TGT-52557)
* È stato risolto un problema a causa del quale [!DNL Target] generava collegamenti di controllo qualità non validi per le attività basate su moduli. (TGT-52528 e TGT-52603)
* È stato risolto un problema che causava l&#39;elaborazione del salvataggio di un&#39;attività modificata, ma mai completata, e nessun messaggio di errore veniva visualizzato in [!DNL Target]. (TGT-52461)
* È stato risolto un problema che impediva al [!UICONTROL Compositore esperienza visivo] (VEC) aggiornato di rilevare automaticamente il valore `at_property`. (TGT-52347)
* È stato risolto un problema che causava la registrazione di due modifiche quando ne era prevista solo una dopo il passaggio dalle modalità [!UICONTROL Sfoglia] alle modalità [!UICONTROL Progettazione] nel Compositore esperienza visivo durante l&#39;interazione con un elemento modulo. (TGT-52455)
* È stato risolto un problema che impediva la selezione dell&#39;impostazione [!UICONTROL Clic su un elemento] nel Compositore esperienza visivo aggiornato a causa di un errore che indicava che il selettore non era valido, era già in uso o non era visibile. (TGT-52467)
* È stato risolto un problema che causava la visualizzazione di caselle duplicate (ghost) a causa dell&#39;aggiunta di una casella [!UICONTROL Offerta consigli] nel Compositore esperienza visivo aggiornato. Il passaggio tra l’Esperienza A e B ha aggiunto ripetutamente più caselle fantasma. (TGT-52505 e TGT-52519)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale le modifiche apportate a un&#39;offerta HTML tramite il menu [!UICONTROL Offerta] non venivano riportate nell&#39;attività associata e viceversa. Questo comportamento ora corrisponde all&#39;interfaccia utente legacy, in cui gli aggiornamenti vengono sincronizzati correttamente tra il menu [!UICONTROL Offerta] e l&#39;attività. (TGT-52540 e TGT-52541)
* È stato risolto un problema a causa del quale gli aggiornamenti recenti di [!UICONTROL Frammenti di esperienza] nella [!UICONTROL Libreria offerte] non venivano riflessi durante il tentativo di utilizzarli all&#39;interno di un&#39;attività. (TGT-52659)
* È stato risolto un problema di localizzazione nella traduzione in cinese semplificato di un messaggio di conferma. Nella versione precedente mancavano le virgolette intorno al nome della posizione e utilizzava un linguaggio informale, contrariamente a quanto previsto dalla guida di stile del cliente. La traduzione aggiornata ora utilizza la punteggiatura corretta e un tono formale. (TGT-52364)

### [!DNL Target Standard/Premium] 25.5.3 (22 maggio 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva il corretto funzionamento della funzione di ricerca per nome nell&#39;elenco [!UICONTROL Attività] con query con più parole. (TGT-52529)
* È stato risolto un problema che impediva l&#39;esclusione delle esperienze dalle attività [!UICONTROL Automated Personalization] (AP). (TGT-52383)
* È stato risolto un problema che causava l&#39;assenza dell&#39;opzione &quot;[!UICONTROL Contains]&quot; nelle [!UICONTROL Regole filtro] durante la gestione del contenuto nelle attività di Personalizzazione automatizzata. (TGT-52384)
* È stata risolta un&#39;incoerenza nei rapporti nelle attività [!UICONTROL Automated Personalization] (AP), in particolare per quanto riguarda il modo in cui vengono tracciate e segnalate le offerte predefinite utilizzando i valori `optionLocalId` del sistema interno di [!DNL Target].
* È stato risolto un problema che impediva ai collegamenti di controllo qualità di fornire l’esperienza di attività desiderata. (TGT-52163)
* È stato risolto un problema che impediva agli utenti con autorizzazioni [!UICONTROL Approvatore] di modificare le attività live in modo errato, ricevendo un messaggio di errore &quot;Accesso negato&quot;. (TGT-52416)
* È stato risolto un problema che impediva la visualizzazione dei perfezionamenti del pubblico per alcune attività nell&#39;interfaccia utente [!DNL Target] aggiornata. (TGT-52057)
* È stato risolto un problema che causava l’inversione dei perfezionamenti del pubblico e dei tipi di pubblico dell’attività nell’interfaccia utente aggiornata. (TGT-52158)
* È stato risolto un problema a causa del quale la generazione di offerte ad hoc generava offerte duplicate. (TGT-51938)
* È stato risolto un problema che bloccava gli aggiornamenti delle offerte e causava la visualizzazione errata di un errore &quot;Utente non valido&quot;. (TGT-52361)
* È stato risolto un problema che impediva il salvataggio delle attività esistenti, causando un errore di tipo &quot;Input utente non valido&quot;. (TGT-52422)
* È stato risolto un problema che impediva la modifica delle offerte HTML esistenti, causando un errore di tipo &quot;Input utente non valido&quot; al momento del salvataggio, anche quando non venivano apportate modifiche al codice. (TGT-52351)
* È stato risolto un problema che impediva a [!DNL Target] di riconoscere il carattere &quot;#&quot; nell&#39;URL di un sito Web. (TGT-52093)
* È stato risolto un problema che impediva la modifica delle attività [!DNL Recommendations] per aggiungere o aggiornare promozioni, causando errori di salvataggio e promozioni duplicate. (TGT-52343)
* È stato risolto un problema che impediva la modifica di criteri o progettazioni nelle attività [!DNL Recommendations], causando un errore &quot;JSON non valido: nome proprietà non riconosciuto&quot;. (TGT-52375)
* È stato risolto un problema che impediva la corretta visualizzazione dei criteri di sequenza nel [!UICONTROL Compositore esperienza visivo] (VEC) per le attività [!DNL Recommendations]. (TGT-52435)
* È stato risolto un problema che impediva la corretta identificazione delle visualizzazioni nelle pagine di applicazioni a pagina singola quando si utilizzava [!DNL Adobe Experience Platform Web SDK]. (TGT-52106)
* È stato risolto un problema a causa del quale i dettagli di On-Device Decisioning (ODS) non venivano salvati correttamente, nonostante fossero inclusi nel payload dell’operazione batch. (TGT-52406)
* Alle attività è stato aggiunto un campo `audienceMetadata` che consente di leggerlo e aggiornarlo durante la modifica. (TGT-51004)
* È stato aggiunto un messaggio di errore per avvisare gli utenti quando un arco temporale del pubblico non è valido. (TGT52522)
* È stata aggiornata la struttura delle attività per supportare tipi di pubblico duplicati di diversi tipi. (TGT-51200)

<!--
### [!DNL Adobe Target] [!DNL AI Assistant] release (May 16, 2025)

We are thrilled to announce the launch of the [!DNL AI Assistant] in [!DNL Adobe Target]! This powerful user interface feature is designed to help you navigate and understand [!DNL Target] concepts with ease. Available across multiple products in [!DNL Adobe Experience Cloud], including [!DNL Target], [!DNL AI Assistant] is here to revolutionize your experience.

[!DNL AI Assistant] in [!UICONTROL Target] is a conversational tool that you can use to accelerate your workflows with [!DNL Experience Platform] applications and services. Use [!DNL AI Assistant] to boost your overall productivity and amplify your understanding of product knowledge

In [!DNL Target], the first phase of [!DNL AI Assistant] provides invaluable product knowledge grounded in [!DNL Experience League] documentation. Whether you are setting up a profile script, troubleshooting errors, or considering an upgrade to the AEP Web SDK, [!DNL AI Assistant] has you covered.

For more information, see [Coworker skills for Adobe Target](/help/main/c-intro/coworker-skills.md).
-->

### [!DNL Target Standard/Premium] 25.5.2 (8 maggio 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* [!DNL Target] utenti con i diritti di [!UICONTROL Amministratore di prodotto] e [!UICONTROL Amministratore di sistema] possono ora modificare tutte le impostazioni nelle pagine [!UICONTROL Amministrazione], indipendentemente dal loro ruolo in [!DNL Target]. Gli utenti senza queste autorizzazioni dispongono di accesso in sola lettura a queste impostazioni. Questo aggiornamento garantisce un controllo dell&#39;accesso più rigoroso sulle [impostazioni di amministrazione](/help/main/administrating-target/administrating-target.md). (TGT-48179)
* È stato risolto un problema di caching che impediva il salvataggio dell&#39;attività [Preferenze sito](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#settings). (TGT-52213)
* È stato risolto un problema che impediva ai clienti di abilitare la selezione per ID e classe nella sezione [!UICONTROL Preferenze sito] dopo il caricamento del sito nel Compositore esperienza visivo. L&#39;impostazione [!UICONTROL Preferenze sito] è stata automaticamente disabilitata anche dopo l&#39;abilitazione. (TGT-52207)
* È stato risolto un problema che impediva al [!UICONTROL Compositore esperienza visivo] (VEC) di visualizzare la pagina corretta quando [URL di consegna pagine](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#settings) terminavano con una barra (/). (TGT-52237)
* È stato risolto un problema che impediva la rimozione delle modifiche al codice personalizzato durante la modifica delle esperienze. (TGT-52240)
* È stato risolto un problema a causa del quale le modifiche HTML nel Compositore esperienza visivo sovrapponevano gli elementi di pagina esistenti. (TGT-52265)
* È stato risolto un problema che impediva la modifica del codice personalizzato nel Compositore esperienza visivo aggiornato a causa del fatto che il codice personalizzato esistente non era visibile nell’editor. (TGT-52272)
* È stato risolto un problema che causava il messaggio di errore &quot;I nomi duplicati non sono consentiti&quot; durante il salvataggio di un’attività Consigli. (TGT-52318)
* È stato risolto un problema nel Compositore esperienza visivo aggiornato che impediva ai clienti di modificare elementi di testo o rimuovere oggetti contenitore. (TGT-52348)
* È stato risolto un problema che impediva la corretta visualizzazione di [!DNL Customer Journey Analytics] in una pagina attività [!UICONTROL Panoramica]. (TGT-52359)
* È stato risolto un problema che impediva la persistenza dei gruppi di reporting nelle attività [!UICONTROL Automated Personalization] (AP). (TGT-52368)
* È stato risolto un problema che impediva il salvataggio di attività che includevano offer decisioning. (TGT-52390)
* È stato risolto un problema che causava la selezione dell&#39;offerta predefinita ma la visualizzazione di altri contenuti dell&#39;offerta nelle attività [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Test multivariato] (MVT). (TGT-52372)
* È stata corretta la logica delle autorizzazioni GET per verificare con OR tra l’accesso completo all’organizzazione e l’accesso specifico per organizzazione + utente. (TGT-52374)
* È stato risolto un problema che impediva la visualizzazione dei nomi dei tipi di pubblico dopo la selezione di un pubblico per [!UICONTROL Contenuto gestito] e [!UICONTROL Tipi di pubblico per reportistica], anche se l&#39;opzione [!UICONTROL Mostra solo selezionati] era abilitata. (TGT-52393)

### [!DNL Target Standard/Premium] 25.5.1 (5 maggio 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva la visualizzazione di perfezionamenti del pubblico per alcune attività nell’interfaccia utente aggiornata. (TGT-52057)
* È stato risolto un problema che impediva l’utilizzo di tipi di pubblico combinati nelle attività di. (TGT-52346)
* È stato risolto un problema che impediva la creazione di una nuova attività in un’area di lavoro non predefinita utilizzando un pubblico per sola attività dalla stessa area di lavoro. (TGE-52349)
* È stato risolto un problema che causava la scomparsa dei tipi di pubblico per sola attività dall’interfaccia utente aggiornata dopo la creazione e la selezione di un nuovo pubblico. (TGT=52091)
* È stato risolto un problema che impediva l’utilizzo di tipi di pubblico duplicati nelle attività di. (TGT-51200 e TGT-52057)
* È stato risolto un problema che causava l’inversione dei perfezionamenti del pubblico e dei tipi di pubblico dell’attività nell’interfaccia utente aggiornata. (TGT-52158)
* È stato risolto un problema che impediva la creazione di una nuova attività a causa dell’errore di inserimento dell’utente: &quot;area di lavoro non predefinita non consentita per questo utente&quot;. (TGT-52267)
* È stato risolto un problema che impediva la visualizzazione delle offerte nell’interfaccia utente aggiornata per le aree di lavoro predefinite e non predefinite. [!DNL Target] ora visualizza le offerte da entrambe le aree di lavoro. (TGT-52339)
* È stato risolto un problema a causa del quale [!DNL Target] non avvisava i clienti quando modificava un&#39;attività e modificava un elemento del sito Web modificato. (TGT-52100)
* È stato risolto un problema a causa del quale la modifica di un’offerta con offerte ad hoc creava una nuova offerta invece di aggiornare quella esistente. (TGT-52135)
* È stato risolto un problema che causava un errore di payload non valido durante lo spostamento delle offerte nelle cartelle. (TGT-52325)
* È stato risolto un problema che causava un errore di inserimento dell’utente durante lo spostamento delle offerte nelle cartelle. (TGT-52296)
* È stato aggiunto un campo `audienceMetadata` per ogni attività, per assicurarti che venga letto e aggiornato durante la modifica dell&#39;attività. (TGT-51004)

### [!DNL Target Standard/Premium] 25.4.5 (25 aprile 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che causava discrepanze nelle inserzioni del pubblico tra la pagina delle impostazioni [!UICONTROL Attività] e la pagina della panoramica [!UICONTROL Reporting]. (TGT-52203)
* È stato risolto un problema che impediva l’aggiunta di una nuova pagina a un’attività a causa di un errore di input dell’utente non valido. (TGT-52263)
* È stato risolto un problema che causava l&#39;incremento errato di `OptionLocalIDs` quando l&#39;opzione rimaneva invariata. (TGT-52187)
* È stato risolto un problema che causava l&#39;incremento errato di `location` e `OptionLocalIDs` quando l&#39;opzione rimaneva invariata. (TGT-52188)
* È stato risolto un problema che causava un errore nella posizione della pagina [!UICONTROL Panoramica] dell&#39;attività. (TGT-52182)
* È stato risolto un problema che impediva la visualizzazione di un avviso di selezione non valido per una posizione non valida. (TGT-52110)
* È stato risolto un problema a causa del quale i file di reporting scaricati mostravano correttamente i dati presenti nell’interfaccia utente di reporting. (TGT-52068)
* È stato risolto un problema che impediva il corretto funzionamento delle operazioni batch dopo l’aggiunta delle regole di consegna della pagina. (TGT-52097)
* È stato risolto un problema a causa del quale [!DNL Target] eliminava tutti i parametri di query dall&#39;URL del sito Web. (TGT-52100)
* È stato risolto un errore della console che impediva ai clienti di creare attività nell&#39;interfaccia utente [!DNL Target] legacy e aggiornata. (TGT-52181)
* È stato risolto un problema che impediva ai clienti di aggiungere nuove pagine, causando un errore di input dell’utente non valido. (TGT-52258)
* È stato risolto un problema che causava la scomparsa delle modifiche dopo l&#39;aggiunta di ulteriori pagine e il ritorno alla scheda [!UICONTROL Esperienze]. (TGT-52264)
* È stato risolto un problema che impediva ai clienti di modificare il pubblico in un&#39;attività [!UICONTROL Targeting esperienza] (XT). (TGT-52191)
* È stato corretto un errore che impediva la modifica di un’attività XT a causa di una regola dell’interfaccia utente non supportata. (TGT-52273)
* È stato risolto un problema nel [!UICONTROL Compositore esperienza visivo] (VEC) aggiornato a causa del quale le breadcrumb non venivano sempre visualizzate nella parte inferiore dell&#39;editor, causando difficoltà nella selezione precisa degli elementi. (TGT-52169)
* È stato risolto un problema che impediva all&#39;elenco a discesa [!UICONTROL Pubblico] di visualizzare tutti i tipi di pubblico a causa dell&#39;impaginazione. (TGT-52204)
* È stato risolto un problema che causava un messaggio di input utente non valido durante l&#39;aggiunta di nuove offerte nelle attività [!UICONTROL Automated Personalization] (AP). (TGT-52210)
* È stato risolto un problema a causa del quale [!UICONTROL Analytics for Target] (A4T) veniva erroneamente selezionato come origine per la generazione di rapporti, anche se il cliente non aveva accesso ad A4T. (TGT-52226)
* È stato risolto un problema che impediva il salvataggio di un&#39;attività con la metrica URL [!UICONTROL Visualizza una pagina]. (TGT-52260)
* È stato risolto un problema che impediva ai clienti di selezionare aree di lavoro durante la creazione di offerte all’interno di un’attività. (TGT-52289)
* È stato risolto un problema che impediva ai clienti di creare attività in tutte le aree di lavoro. (Tgt-52218)
* È stato risolto un problema che causava la visualizzazione errata delle modifiche da un’esperienza quando si passava a un’altra. (TGT-52184)
* È stato risolto un problema che impediva la corretta visualizzazione dell&#39;offerta predefinita nell&#39;interfaccia utente [!DNL Target] all&#39;apertura dell&#39;attività. (TGT-52198)

### Aggiornamento delle autorizzazioni di Target (22 aprile 2025)

Questo aggiornamento futuro migliora il controllo dell&#39;organizzazione sulle configurazioni delle istanze [!DNL Target], impedendo aggiornamenti accidentali che potrebbero influire sulla distribuzione delle attività tra i vari team di test e personalizzazione.

A decorrere dal 22 aprile 2025, solo gli amministratori di [!UICONTROL Prodotto] e [!UICONTROL Soluzioni] potranno aggiornare le impostazioni nelle sezioni [!UICONTROL Amministrazione], indipendentemente dai ruoli che ricoprono nelle [!DNL Target] aree di lavoro. Gli utenti senza questa autorizzazione avranno accesso in sola lettura alle sezioni [!UICONTROL Amministrazione].

Per ulteriori informazioni, vedere [Amministrare Target](/help/main/administrating-target/start-target.md).

### [!DNL Target Standard/Premium] 25.4.4 (17 aprile 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato aggiunto un messaggio di errore per guidare gli utenti nella risoluzione delle opzioni duplicate in un’attività. (TGT-51927)
* È stato risolto un problema che impediva la rimozione di `ClickTrack` selettori durante l&#39;eliminazione di pagine o esperienze con offerte di reindirizzamento. (TGT-51952)
* È stato risolto un problema che causava l&#39;autorizzazione di selettori `ClickTrack` vuoti. [!DNL Target] ora richiede che il campo del selettore non sia vuoto. (TGT-52107)
* È stato risolto un problema che consentiva erroneamente le metriche con nomi duplicati. Le metriche ora richiedono nomi univoci. (TGT-52201)
* È stato risolto un problema a causa del quale le definizioni dei tipi di pubblico non erano visibili durante la modifica del targeting a livello di offerta nelle attività [!UICONTROL Automated Personalization] (AP). (TGT-52148)
* È stato risolto un problema che impediva ai clienti con diritti di [!UICONTROL Editor] di salvare le attività. (TGT-52227)
* `OptionLocalIDs` non incrementa più in modo errato quando l&#39;opzione rimane invariata. (TGT-52139)
* È stato risolto un problema che causava un messaggio &quot;Non valido `optionLocalIds`&quot; durante il tentativo di creare un&#39;attività. (TGT-52154)
* Sono state corrette le discrepanze tra `OptionLocalIDs` definiti per un&#39;attività e quelli utilizzati per definire le esperienze. (TGT-52215)
* È stato risolto un problema che causava un errore di convalida durante il tentativo di creazione di un’attività A/B. (TGT-51923)

### [!DNL Target Standard/Premium] 25.4.3 (11 aprile 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato corretto un errore che impediva ai clienti di aprire il pop-up di informazioni sul pubblico per alcune attività [!UICONTROL Targeting esperienza] (XT). (TGT-52049)
* È stato risolto un problema che causava il ripristino dell&#39;impostazione relativa al pubblico su &quot;[!UICONTROL Tutti i visitatori]&quot; in seguito alle modifiche apportate nel [!UICONTROL Compositore esperienza visivo]. (TGT-52132)
* È stato risolto un problema che impediva la visualizzazione di perfezionamenti del pubblico per attività specifiche (TGT-52057)
* È stato risolto un problema che impediva ai clienti di inserire un [!UICONTROL frammento di esperienza] nell&#39;area di lavoro predefinita. (TGT-52073)
* È stato risolto un problema che causava la visualizzazione di un&#39;offerta come &quot;Contenuto non trovato&quot; e non nella pagina [!UICONTROL Offerte] per un&#39;attività [!UICONTROL Automated Personalization] (AP). (TGT-52150)
* È stata aggiunta la possibilità di consentire la duplicazione dei tipi di pubblico all’interno di un’attività. (TGT-51200)
* È stato risolto un problema che causava la visualizzazione del nome mbox errato nella pagina [!UICONTROL Obiettivi e impostazioni] per un&#39;attività XT dopo la modifica. (TGT-52026)
* È stato risolto un problema che causava la visualizzazione di `defaultContent` nelle opzioni nonostante non fosse in `experiences/optionLocations`. (TGT-52036)
* È stato risolto un problema per garantire che le stringhe vuote non vengano convertite in valori Null. (TGT-52037)
* È stato risolto un problema che richiedeva ai clienti di riconfigurare l&#39;[!UICONTROL Obiettivo di ottimizzazione] in [!UICONTROL Impostazioni reporting] nella pagina [!UICONTROL Obiettivi e impostazioni] dopo le modifiche. (TGT-52071)
* È stato risolto un problema a causa del quale un&#39;attività senza regole di consegna pagine visualizzava più regole nella pagina [!UICONTROL Panoramica]. (TGT-52084)
* È stato aggiunto un messaggio di errore per gli utenti che tentano di salvare un’offerta con caratteri al di fuori del piano multilingue di base, ad esempio emoji. (TGT-52105)
* È stato risolto un problema a causa del quale l’apertura di un’attività attivava il messaggio di errore: &quot;Questa attività utilizza uno o più tipi di pubblico eliminati alla sorgente&quot;. (TGT-52120)
* È stato risolto un problema che impediva la visualizzazione delle metriche ClickTrack nel [!UICONTROL Compositore esperienza visivo] (VEC) aggiornato durante la modifica. (TGT-52152)
* È stato risolto un problema a causa del quale un URL con un parametro di query come percorso dell&#39;attività non visualizzava il parametro di query nella pagina [!UICONTROL Panoramica] dell&#39;attività. (TGT-51635)
* È stato risolto un problema che impediva la visualizzazione dell&#39;intero URL dell&#39;esperienza in [!UICONTROL modalità Sfoglia] nel [!UICONTROL Compositore esperienza visivo]. (TGT-52101)
* È stato risolto un problema a causa del quale la modifica di un’attività causava l’aggiunta di &quot;/&quot; alla fine dell’URL da parte della consegna della pagina, che ne causava l’invalidità. (TGT-52114)
* È stato risolto un problema che causava il reindirizzamento errato del collegamento [!UICONTROL Controllo di qualità attività] in [!UICONTROL Compositore esperienza basato su moduli] alla home page di [!DNL Adobe Experience Cloud]. (TGT-52055)
* È stato risolto un problema che impediva il mantenimento delle pagine aggiuntive aggiunte all&#39;attività [!UICONTROL Test A/B] dopo il salvataggio e la riapertura. (TGT-51994)
* È stato risolto un problema che impediva ai clienti di eliminare gli stili nella sezione stile in linea. (TGT-52070)
* È stato ripristinato l&#39;accesso alle [schede di definizione del pubblico](/help/main/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) nella finestra di dialogo [!UICONTROL Controllo qualità attività], in modo simile all&#39;interfaccia utente legacy. (TGT-52056)
* L’interfaccia utente aggiornata non salvava pagine o tipi di pubblico senza modifiche. Se i clienti hanno aggiunto nuove pagine o tipi di pubblico a un&#39;attività ma non vi apportano modifiche, [!DNL Target] ha eliminato i tipi di pubblico non modificati al momento del salvataggio. Le notifiche sono state aggiunte in posizioni rilevanti per informare gli utenti di questo comportamento. (TGT-52104)

### [!DNL Target Standard/Premium] 25.4.1 (2 aprile 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che causava la scomparsa dei tipi di pubblico dell’esperienza dalle attività di. (TGT-52003)
* È stato risolto un problema che causava elementi imprevisti durante la consegna. (TGT-52011)
* È stato risolto un problema che impediva ai clienti di visualizzare il pubblico nel grafico di targeting nella pagina Ove[!UICONTROL r]view e durante la modifica dell&#39;attività. (TGT-52050)
* È stato risolto un problema che impediva ai clienti di riordinare le esperienze in ordine di priorità nelle attività [!UICONTROL Targeting esperienza] (XT). (TGT-52054)
* È stato risolto un problema che causava un rendering errato quando si annullavano le modifiche allo stile del testo. (TGT-51876)
* È stato risolto un problema a causa del quale durante la modifica di un&#39;offerta di reindirizzamento, [!DNL Target] rimuove anche i selettori [!UICONTROL ClickTrack] associati all&#39;offerta. (TGT-51936)
* È stato risolto un problema che causava il salvataggio errato del selettore da parte di [!DNL Target] durante l&#39;annullamento di [!UICONTROL ClickTrack]. (TGT-51937)
* È stato risolto un problema che causava un errore di nome non valido dopo l&#39;apertura e la chiusura del selettore mbox nella pagina [!UICONTROL Obiettivi e impostazioni] senza apportare modifiche. (TGT-51983)
* È stato risolto un problema che impediva la modifica delle offerte ad hoc create nell&#39;interfaccia utente legacy di [!DNL Target]. (TGT-51984)
* È stato risolto un problema che bloccava le attività di modifica con offerte ad hoc contenenti codice personalizzato. (TGT-51995)
* È stato risolto un problema che causava la visualizzazione delle regole di esclusione come regole di inclusione durante la modifica delle definizioni di pubblico combinato. (TGT-51999)
* È stato risolto un problema che impediva la corretta visualizzazione del codice personalizzato durante la modifica dell’esperienza. (TGT-52005)
* È stato risolto un problema che rendeva l&#39;opzione [!UICONTROL Inserisci prima] non disponibile per l&#39;inserimento di contenuto prima della barra di navigazione. (TGT-52031)
* È stato risolto un problema che impediva la corretta evidenziazione dell’esperienza predefinita nel reporting. (TGT-51716)
* È stato risolto un problema che attivava un messaggio `default message [Invalid optionLocalIds: xx]]` durante la creazione di un&#39;attività. (TGT-52038)

### at.js versione 2.11.8 (31 marzo 2025)

* È stata risolta una vulnerabilità identificata da CodeQL nella convalida del suffisso di stringa per evitare casi edge durante le operazioni di ridimensionamento e spostamento. (TNT-51516)

### [!DNL Target Standard/Premium] 25.3.8 (28 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che causava il caricamento lento della pagina [!UICONTROL Attività]. (TGT-51151)

### [!DNL Target Standard/Premium] 25.3.7 (26 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva il salvataggio di attività multipagina se una pagina veniva eliminata dopo le modifiche. (TGT-51988)
* È stato risolto un errore che si verificava durante la modifica di un&#39;attività: `default message [Invalid optionLocalIds: xx]]`. (TGT-51985)
* È stato risolto un problema a causa del quale l’aggiunta di nuove modifiche a un’attività rimuoveva le modifiche esistenti. (TGT-51981)
* È stato risolto un problema a causa del quale la sostituzione di un pubblico con &quot;[!UICONTROL Tutti i visitatori]&quot; durante la creazione o la modifica dell&#39;attività causava un errore &quot;I tipi di pubblico duplicati non sono consentiti&quot;. (TGT-51978)
* È stato risolto un problema che causava un errore &quot;Input utente non valido&quot; durante il salvataggio di un&#39;attività [!UICONTROL Test A/B]. (TGT-51976)
* È stato risolto un problema che impediva la corretta visualizzazione delle metriche calcolate nella pagina [!UICONTROL Obiettivi e impostazioni]. (TGT-51975)
* È stato risolto un problema che impediva la corrispondenza tra `companyName` e `reportSuite` nella configurazione [!DNL Analytics] per la metrica `pageviews`. (TGT-51965)
* È stato risolto un problema che causava la rimozione delle modifiche dal passaggio a un’esperienza in un’attività. (TGT-51945)
* È stato risolto un problema a causa del quale la rimozione di un pubblico di pagina causava anche la rimozione di [!UICONTROL selettori ClickTrack]. (TGT-51935)
* È stato risolto un problema che impediva la modifica di un&#39;attività dopo l&#39;apertura della relativa pagina [!UICONTROL Panoramica]. (TGT-51931)
* È stato risolto un problema che causava un errore `[Unused optionLocalIds: 0]]` durante la creazione dell&#39;attività. (TGT-51920)
* È stato risolto un problema a causa del quale alcune modifiche non venivano tradotte correttamente dopo la rimozione delle modifiche allo stile del testo. (TGT-51876)
* È stato risolto un problema che impediva il corretto aggiornamento dei tipi di pubblico di destinazione nel [!UICONTROL Compositore esperienza basato su moduli]. (TGT-51845)
* È stato risolto un problema che impediva l&#39;aggiornamento corretto dell&#39;URL nel [!UICONTROL Compositore esperienza visivo] durante la navigazione dell&#39;attività. (TGT-51832)
* È stato risolto un problema che impediva la visualizzazione delle offerte nell&#39;interfaccia utente [!UICONTROL Offerte], nonostante la corretta visualizzazione durante la creazione di un&#39;attività e l&#39;aggiunta di offerte. (TGT-51805)
* È stato risolto un problema a causa del quale alcune attività non disponevano di una schermata di fallback per visualizzare il contenuto predefinito quando non era possibile distribuire contenuto personalizzato o mirato. (TGT-51638)
* È stato risolto un problema che impediva la corretta visualizzazione delle offerte live e di alcune cartelle nell&#39;interfaccia utente [!UICONTROL Offerte]. (TGT-51628)
* È stato risolto un problema che impediva la corretta localizzazione di alcune stringhe URL e goURL. (TGT-35741)
* È stato risolto un problema che impediva la corretta localizzazione dei ruoli ([!UICONTROL Approvatore], [!UICONTROL Editor] e [!UICONTROL Osservatore]) nell&#39;interfaccia utente [!DNL Target]. (TGT-29925)

### [!DNL Target Standard/Premium] 25.3.6 (14 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto l&#39;errore &quot;Input utente non valido&quot; nelle attività del [!UICONTROL Compositore esperienza visivo] con [!UICONTROL Tracciamento dei clic] abilitato quando lo stesso selettore [!UICONTROL ClickTrack] viene utilizzato più volte. (TGT-51921)
* È stato corretto l’errore &quot;Input utente non valido&quot; nelle attività del Compositore esperienza visivo con posizioni condivise (ad esempio, il selettore HEAD) e offerte identiche. (TGT-51879)
* È stato risolto un problema che causava la condivisione delle modifiche dell’esperienza tra i vari tipi di pubblico. (TGT-51815)
* Sono stati risolti degli errori di convalida durante la creazione di attività a causa di conflitti di ID segmento. Gli errori si sono verificati quando [!DNL Target] ha rilevato attività esistenti utilizzando segmenti anonimi. (TGT-51784)
* È stato risolto un problema che impediva a [!DNL Target] di salvare attività con regole di esclusione in un pubblico. (TGT-51581)
* È stato risolto un problema che impediva ai clienti di creare, eliminare o spostare cartelle senza accedere all’area di lavoro predefinita. (TGT-51499)
* È stato risolto un problema che causava un errore nelle richieste GET durante il recupero dell&#39;elenco delle metriche [!DNL Analytics]. (TGT-51106)

### [!DNL Target Standard/Premium] 25.3.5 (11 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva agli utenti di modificare le offerte nel pannello [!UICONTROL Modifiche]. (TGT-51800)
* È stato risolto un problema che impediva la corretta visualizzazione delle azioni nel pannello sinistro per esperienze e tipi di pubblico, incluso nella modalità [!UICONTROL ClickTrack]. (TGT-51895)
* È stato risolto un problema a causa del quale i selettori [!UICONTROL ClickTrack] non venivano applicati alla pagina del pubblico corretta. (TGT-51871)

### [!DNL Target Standard/Premium] 25.3.4 (7 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva la modifica o il riutilizzo dei tipi di pubblico per sola attività nel pannello [!UICONTROL Tipi di pubblico]. (TGT-51860)
* È stato risolto un problema che impediva ai clienti [!DNL Target Standard] di creare attività utilizzando il reporting di [!UICONTROL Analytics for Target] (A4T). (TGT-51854)
* È stato risolto un problema che escludeva i contatori degli ID locali dal payload durante le operazioni di creazione e modifica in batch. (TGT-51867)

### [!DNL Target Standard/Premium] 25.3.2 (6 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva la creazione di una nuova attività in seguito alla copia di un’attività con un pubblico per sola attività, utilizzando erroneamente il pubblico dell’attività originale. (TGT-51855)
* È stato risolto un problema che impediva la modifica di [!UICONTROL attività Targeting esperienza] (XT) con tipi di pubblico per sola attività. (TGT-51846)
* È stato risolto un problema che impediva al [!UICONTROL Compositore esperienza visivo] di applicare correttamente le modifiche a un&#39;esperienza alla prima modifica. (TGT-51843)
* È stato risolto un problema che attivava un errore &quot;ID&quot; quando si faceva clic su alcuni elementi all’interno del Compositore esperienza visivo. (TGT-51814)
* È stata aggiornata la gestione degli errori nel Compositore esperienza visivo durante la creazione dell’attività. (TGT-51759)
* È stato risolto un problema che causava un errore di &quot;input utente non valido&quot; durante il salvataggio dell&#39;attività a causa di una visualizzazione mancante nel pannello [!UICONTROL Modifiche]. (TGT-51827)
* È stato risolto un problema che impediva la creazione di criteri per i consigli. (TGT-51834)
* È stato aggiunto un messaggio di conferma prima del reindirizzamento a un URL diverso. (TGT-51703)
* Sono stati risolti dei problemi relativi ai test di integrazione di GraphQL in offerte e cartelle. (TGT-51839)

### [!DNL Target Standard/Premium] 25.3.1 (3 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* Un pubblico combinato può includere sottogruppi, ciascuno contenente più tipi di pubblico. Questa versione ha risolto un problema che impediva la visualizzazione dei tipi di pubblico dei sottogruppi nella finestra di dialogo [!UICONTROL Regole]. (TGT-51813)
* È stato risolto un problema a causa del quale alcuni tipi di pubblico di esperienza venivano sostituiti con [!UICONTROL Tutti i visitatori] all&#39;apertura di attività precedenti. (TGT-51812)
* È stato risolto un problema che impediva la modifica di attività con tipi di pubblico per sola attività. (TGT-51807)
* È stato risolto un problema che impediva la modifica delle modifiche dell&#39;intestazione della pagina nell&#39;interfaccia utente [!DNL Target] aggiornata. (TGT-51797)
* È stato risolto un errore Null che si verificava durante la duplicazione di un’esperienza, l’eliminazione di un’altra esperienza e il tentativo di salvare l’attività. (TGT-51796)
* È stato risolto un problema che impediva la visualizzazione delle regole di esclusione del pubblico nel pannello informazioni del pubblico durante il passaggio [!UICONTROL Targeting] della creazione di attività. (TGT-51579)
* Aggiornati messaggi di errore localizzati in coreano. (TGT-51701 e TGT-51699)

### [!DNL Target Standard/Premium] 25.2.3 (26 febbraio 2025)

Questa versione include i seguenti aggiornamenti:

* È stato risolto un problema che impediva aggiornamenti delle attività dopo la versione 25.2.1 di [!DNL Target] per alcune attività. (TGT-51781)
* È stato risolto un problema che causava la rimozione di tutte le modifiche apportate al pubblico nello stato in seguito all&#39;annullamento del processo di creazione attività (selezionando [!UICONTROL Annulla] invece di [!UICONTROL Aggiungi pubblico]). (TGT-51769 e TGT-51770)
* È stato risolto un problema che impediva il caricamento del [!UICONTROL Compositore esperienza visivo] per alcune attività, in particolare quando è stato utilizzato un codice personalizzato.  Il problema ha portato il Compositore esperienza visivo a visualizzare una schermata vuota o a ripristinare la versione precedente dell&#39;interfaccia utente [!DNL Target]. (TGT-51758)
* È stato risolto un problema a causa del quale le modifiche venivano eliminate dopo la modifica della distribuzione delle pagine per i tipi di pubblico. (TGT-51756)
* È stato risolto un problema che causava la rimozione di tutti i tipi di pubblico non metrici (pubblico pagina e pubblico esperienza) dalle attività in seguito alla modifica di un tipo di metrica nella pagina [!UICONTROL Obiettivi e impostazioni]. (TGT-51753)
* È stato risolto un problema per cui facendo clic su [!UICONTROL Annulla] durante la modifica di un&#39;attività l&#39;interfaccia utente di Target passava all&#39;[!UICONTROL Elenco attività] invece della pagina [!UICONTROL Dettagli attività]. (TGT-51731)
* È stato risolto un problema che impediva ai clienti di scaricare i rapporti tramite l&#39;opzione [!UICONTROL Esporta rapporti in CSV]. (TGT-51708)
* È stato risolto un problema nel Compositore esperienza basato su moduli a causa del quale [!DNL Target Standard] clienti venivano erroneamente visualizzati per l&#39;utilizzo di [!UICONTROL Proprietà], una funzionalità di [!DNL Target Premium]. (TGT-51678)
* È stato risolto un problema che impediva la visualizzazione degli attributi [!DNL Adobe Experience Platform] durante la creazione di nuove offerte. (TGT-51665)
* Tutti i filtri attivi per l&#39;inventario [!DNL Recommendations] sono stati spostati nella ricerca rapida, allineando l&#39;interfaccia utente con [!UICONTROL Ricerca nel catalogo] invece della barra [!UICONTROL Filtro]. (TGT-50723)

### at.js versione 2.11.7 (26 febbraio 2025)

Questa versione include i seguenti aggiornamenti:

* È stata corretta la registrazione di telemetria quando `localStorage` non è disponibile. La telemetria causava problemi ad alcuni clienti che avevano disabilitato `localStorage` nei loro browser.

Per informazioni su questa versione e sulle versioni precedenti di at.js, consulta [Dettagli sulla versione di at.js](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions){target=_blank}.

### Target Standard/Premium 25.2.1 (martedì 17 febbraio 2025) {#ui-update-2}

Questa versione include i seguenti aggiornamenti:

* [!UICONTROL Attività] aggiornamento interfaccia utente
* Aggiornamento dell&#39;interfaccia utente di [!DNL Recommendations]

#### [!UICONTROL Attività] aggiornamento interfaccia utente

Mentre il tentativo di modernizzazione dell&#39;interfaccia utente di [!DNL Adobe Target] continua, siamo lieti di annunciare la disponibilità generale dell&#39;interfaccia utente aggiornata di [!UICONTROL Attività].

>[!NOTE]
>
>A partire dal 17 febbraio, i clienti avranno gradualmente accesso alla nuova interfaccia utente [!UICONTROL Attività]. Per garantire un rollout senza soluzione di continuità per tutti i clienti, questa versione verrà implementata in fasi controllate. La prima fase aggiornerà il gruppo iniziale di [!DNL Target] clienti alla nuova interfaccia utente [!UICONTROL Attività]. Le fasi successive aggiorneranno i clienti rimanenti.

>[!IMPORTANT]
>
>Per informazioni importanti sul piano di fine del ciclo di vita per l&#39;attivazione/disattivazione della versione dell&#39;interfaccia utente [!DNL Target], vedere [[!DNL Target] Impostazione/disattivazione della versione dell&#39;interfaccia utente](/help/main/r-release-notes/release-notes.md#toggle).

In base al sistema di progettazione [!DNL Adobe Spectrum] più recente, l&#39;aggiornamento standardizza i modelli di progettazione precedentemente incoerenti, aggiungendo nuovi miglioramenti, ad esempio:

* [Generazione rapporti riprogettata](/help/main/administrating-target/reporting.md) per ottenere informazioni più approfondite sui risultati delle attività.
* [[!UICONTROL È stata aggiornata la pagina del log delle modifiche]](/help/main/c-activities/change-log.md), che ora riceve le informazioni da [[!DNL Audit Query API]](https://experienceleague.adobe.com/it/docs/experience-platform/landing/governance-privacy-security/audit-logs/audit-api/overview){target=_blank} per approfondimenti in tempo reale.
* [Viste elenco personalizzabili](/help/main/c-activities/activities.md) per una maggiore flessibilità tra le diverse esigenze del team.
* [Sono state migliorate le schermate di informazioni rapide e dettagli](/help/main/c-activities/activities.md) per un accesso più semplice alle informazioni.
* [Opzioni di ricerca e filtro persistenti alla sessione](/help/main/c-activities/activities.md).
* Completamente [ricompilato [!UICONTROL Visual Editing Composer]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) con il supporto per gli ultimi aggiornamenti di sicurezza dai provider del browser e una moderna interfaccia utente.

  Per informazioni sulle differenze tra il Compositore esperienza visivo aggiornato e la versione precedente, vedi:

  * [Modifiche al Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md)
  * [Opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)

* [Aggiornamento [!DNL Chrome] dell&#39;estensione](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) che supporta Manifest V3 per una maggiore sicurezza e un migliore supporto per i cookie di prime parti.

![Aggiornamento attività](/help/main/r-release-notes/assets/activities-refresh.png)

#### Aggiornamento dell&#39;interfaccia utente di [!DNL Recommendations]

Mentre il tentativo di modernizzazione dell&#39;interfaccia utente [!DNL Adobe Target] continua, è possibile annunciare la disponibilità generale dell&#39;interfaccia utente [!DNL Recommendations] aggiornata.

>[!NOTE]
>
>A partire dal 17 febbraio, i clienti avranno gradualmente accesso alla nuova interfaccia utente [!UICONTROL Consigli]. Per garantire un rollout senza soluzione di continuità per tutti i clienti, questa versione verrà implementata in fasi controllate. La prima fase aggiornerà il gruppo iniziale di [!DNL Target] clienti alla nuova interfaccia utente [!UICONTROL Attività]. Le fasi successive aggiorneranno i clienti rimanenti.

In base al sistema di progettazione [!DNL Adobe Spectrum] più recente, l&#39;aggiornamento standardizza i modelli di progettazione precedentemente incoerenti, aggiungendo nuovi miglioramenti, ad esempio:

* La [ricerca nel catalogo prodotti](/help/main/c-recommendations/c-products/catalog-search.md) ora include un database aggiornato che consente la sincronizzazione in tempo reale dei prodotti.
* Gli oggetti [!UICONTROL Recommendations] ([!UICONTROL Criteri], [!UICONTROL Progettazioni], [!UICONTROL Raccolte] e [!UICONTROL Esclusioni]) [creati tramite API sono ora disponibili nell&#39;interfaccia utente](/help/main/c-recommendations/c-recommendations-faq/recommendations-faq.md).
* [Le impostazioni dei consigli](/help/main/administrating-target/recommendations-settings.md) sono state consolidate nella sezione [!UICONTROL Amministrazione].
* Visualizzazioni elenco personalizzabili per una maggiore flessibilità tra le diverse esigenze del team.
* Aggiornati editor di codice HTML e JSON con [evidenziazione della sintassi e numerazione delle righe](/help/main/c-experiences/c-manage-content/create-json-offer.md).
* Sono state migliorate le schermate di informazioni rapide e dettagli per un accesso più semplice alle informazioni.
* Opzioni di ricerca e filtro persistenti nella sessione.

![Aggiornamento dell&#39;interfaccia utente Recommendations](/help/main/r-release-notes/assets/recs-ui-refresh.png)

### Target Standard/Premium 25.1.1 (venerdì 9 gennaio 2025) {#ui-update-1}

Questa versione include i seguenti aggiornamenti:

#### Aggiornamento dell&#39;interfaccia utente della [!UICONTROL Libreria offerte]

Per migliorare l&#39;esperienza utente per [!DNL Adobe Target] utenti, questa versione aggiorna l&#39;interfaccia utente della [!UICONTROL Libreria offerte].

>[!NOTE]
>
>Per garantire un rollout senza soluzione di continuità per tutti i clienti, questa versione verrà implementata in fasi controllate. La prima fase ha aggiornato il gruppo iniziale di clienti Target alla nuova interfaccia utente Offerte. Le fasi successive aggiorneranno i clienti rimanenti.

>[!IMPORTANT]
>
>Per informazioni importanti sul piano di fine del ciclo di vita per l&#39;attivazione/disattivazione della versione dell&#39;interfaccia utente [!DNL Target], vedere [[!DNL Target] Impostazione/disattivazione della versione dell&#39;interfaccia utente](/help/main/r-release-notes/release-notes.md#toggle).

Utilizzando il più recente sistema di progettazione [!DNL Adobe Spectrum], questo aggiornamento standardizza i modelli di progettazione incoerenti e introduce nuovi miglioramenti, tra cui i seguenti:

* **Gestione delle offerte in blocco**: seleziona ed elimina o sposta più offerte contemporaneamente.

* **[!UICONTROL L&#39;editor di codice] aggiorna**: gli editor HTML e JSON sono stati aggiornati con l&#39;evidenziazione della sintassi e la numerazione delle righe.

* **Schede offerte migliorate**: informazioni rapide e schede dettagli migliorate per un accesso più semplice alle informazioni.

* **Ricerca e filtri persistenti**: aggiunge opzioni di ricerca e filtro persistenti nella sessione.

Per ulteriori informazioni, vedere [Offerte](/help/main/c-experiences/c-manage-content/manage-content.md) e i sottoarticoli in questa sezione. Tutti gli articoli sulle offerte in questa sezione sono stati aggiornati per riflettere queste modifiche dell’interfaccia utente.

Di seguito un breve video che evidenzia le modifiche apportate a questa versione:

![Video di aggiornamento dell&#39;interfaccia utente delle offerte](/help/main/r-release-notes/assets/offers-video-v2.gif)
