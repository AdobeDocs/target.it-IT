---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti;aggiornamenti;aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 550fa1e8d4127babe02403708b73862505bf8c99
workflow-type: tm+mt
source-wordcount: '1772'
ht-degree: 15%

---

# Note sulla versione (corrente) di [!DNL Target]

Esplora le funzioni, i miglioramenti e le correzioni più recenti in [!DNL Adobe Target]. Queste note sulla versione descrivono anche gli aggiornamenti alle API [!DNL Target], agli SDK, a [!DNL Adobe Experience Platform Web SDK], at.js e ad altri componenti della piattaforma, se applicabili.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## Aggiornamenti urgenti da conoscere {#time-sensitive}

[!BADGE Importante]{type=Informative}

Per gli aggiornamenti sensibili al tempo relativi a [!DNL Adobe Target] e alla tua implementazione, [!DNL Adobe] fornisce note dettagliate sulla versione e documentazione tramite [!UICONTROL Experience League]. Di seguito sono riportate alcune caratteristiche principali relative all’implementazione:

### La versione dell&#39;interfaccia utente [!DNL Target] è deprecata

Per ulteriori informazioni, vedere [[!DNL Target] Domande frequenti sull&#39;aggiornamento dell&#39;interfaccia utente](/help/main/c-intro/updated-ui-faq.md).

## [!DNL Target Standard/Premium] 26.1.1 (18 gennaio 2026)

**Attività**

+++Vedi i dettagli

* **Impossibile copiare l&#39;attività. Input utente non valido.** È stato risolto il problema che causava la visualizzazione da parte degli utenti di un errore non utile di &quot;input utente non valido&quot; durante la copia di un&#39;attività. In precedenza, quando un’attività veniva duplicata, le assegnazioni di proprietà specifiche per l’area di lavoro non venivano mantenute, pertanto il backend rifiutava la richiesta di salvataggio perché ABActivity richiedeva almeno una proprietà appartenente a un’area di lavoro non predefinita. Questa mancata corrispondenza ha attivato un errore generico nell’interfaccia utente, lasciando gli utenti senza indicazioni. La correzione assicura che le assegnazioni dell’area di lavoro vengano mantenute correttamente durante le operazioni di copia, consentendo agli utenti di salvare l’attività copiata senza modifiche e impedendo errori di convalida fuorvianti. (TGT-54282)
* **Abilita la colonna dell&#39;area di lavoro nell&#39;offerta dell&#39;editor Web.** Questo aggiornamento risolve il problema di confusione causato dalle offerte di [!UICONTROL Default Workspace] che appaiono in altre aree di lavoro nell&#39;editor Web. Anche se questo comportamento funziona come previsto, le offerte [!UICONTROL Default Workspace] sono intenzionalmente visibili in tutte le aree di lavoro, i clienti hanno segnalato che l&#39;interfaccia utente non ha chiarito l&#39;origine dell&#39;area di lavoro, soprattutto quando si creano attività in un&#39;area di lavoro non predefinita, ad esempio &quot;Approvatori&quot;. Per migliorare la chiarezza, la colonna [!UICONTROL Workspace] è stata ora abilitata nell&#39;elenco delle offerte dell&#39;editor Web, consentendo agli utenti di distinguere facilmente l&#39;area di lavoro a cui appartiene ogni offerta e impedendo un&#39;interpretazione errata delle offerte aggiuntive visualizzate. (TGT-54138)
* **I collegamenti con target=&quot;_blank&quot; vengono aperti in una nuova scheda.** Questa correzione risolve un problema in cui i siti Web creati contenenti collegamenti con ~target=&quot;_blank&quot;~ verrebbero aperti in una nuova scheda del browser quando si fa clic su di essi in modalità [!UICONTROL Browse], interrompendo l&#39;esperienza di anteprima nell&#39;editor. Il comportamento si è verificato perché gli attributi di collegamento nativi della pagina creata non venivano intercettati dal JavaScript inserito dall’estensione, a differenza dell’interfaccia utente legacy in cui gli elementi di ancoraggio venivano trasformati e le loro destinazioni sostituite per mantenere la navigazione all’interno dell’editor. L&#39;aggiornamento garantisce che i collegamenti che utilizzano ~target=&quot;_blank&quot;~ siano ora gestiti correttamente nell&#39;editor Web, in modo che non aprano più schede esterne durante l&#39;authoring. (TGT-54134)
* **Avviso Deseleziona proprietà.** Questo aggiornamento introduce un avviso visivo per informare chiaramente gli utenti quando deselezionano una proprietà rilevata automaticamente nell&#39;Editor attività. In precedenza, la rimozione di una proprietà rilevata automaticamente non forniva alcuna indicazione che la proprietà sarebbe stata eliminata definitivamente, il che poteva causare la perdita accidentale della configurazione di targeting. La correzione aggiunge un’icona di avviso, coerente con il comportamento nell’interfaccia utente legacy, per avvisare gli utenti che deselezionando la proprietà la rimuove dall’attività. (TGT-54121)
* Il menu a discesa **[!UICONTROL Workspaces]è limitato a 20 nella sezione [!UICONTROL Users].** Questa correzione risolve un problema in cui il menu a discesa [!UICONTROL Workspaces] nella sezione [!UICONTROL Administration] > [!UICONTROL Users] mostrava solo 20 aree di lavoro, anche quando un utente aveva accesso a molte altre. Anche la chiamata GraphQL sottostante per `licenseGroups` era limitata a 20 risultati, pertanto l&#39;interfaccia utente mostrava un elenco incompleto nonostante l&#39;utente avesse accesso a più aree di lavoro nell&#39;organizzazione. L’aggiornamento rimuove questo limite rigido in modo che l’intero set di aree di lavoro disponibili ora venga restituito e visualizzato correttamente. (TGT-53820)
* **È stato risolto un problema a causa del quale la finestra modale delle offerte non mostrava la colonna dell&#39;area di lavoro.** È stato risolto un problema a causa del quale la finestra modale delle offerte non visualizzava la colonna dell&#39;area di lavoro nell&#39;interfaccia utente aggiornata. Ciò ha causato confusione per i clienti perché le offerte di [!UICONTROL Default Workspace] sono apparse insieme alle offerte dell&#39;area di lavoro selezionata senza alcuna indicazione della loro origine. La colonna dell’area di lavoro è ora abilitata in modo che i clienti possano identificare chiaramente a quale area di lavoro appartiene ogni offerta. (TGT-52320)

+++

**Proprietà**

+++Vedi i dettagli
* **La modifica dell&#39;attività non deve aggiungere la proprietà rilevata automaticamente se è già stata rimossa.** Questa correzione risolve un problema in cui la modifica di un&#39;attività reintrodurrebbe automaticamente una proprietà rilevata automaticamente che l&#39;utente aveva precedentemente rimosso. Quando si riapre un&#39;attività per la modifica, il sistema ha ripristinato in modo errato la proprietà rimossa, generando un comportamento incoerente e confusione in [!UICONTROL Properties List]. L’aggiornamento assicura che, una volta rimossa, la proprietà rilevata automaticamente rimanga rimossa durante tutte le modifiche successive e non venga nuovamente visualizzata a meno che l’utente non la aggiunga esplicitamente. (TGT-54182)
* **Non aggiungere proprietà rilevate automaticamente se sono già state rimosse.** Questa correzione assicura che, una volta che un utente rimuove manualmente una proprietà rilevata automaticamente da un&#39;attività, il sistema non la reintroduca più durante la successiva navigazione all&#39;interno dell&#39;editor attività. In precedenza, se un utente deselezionava una proprietà rilevata automaticamente, passava al passaggio [!UICONTROL Targeting] e poi ritornava a [!UICONTROL Experiences], l&#39;editor ripopolava la proprietà rimossa in base all&#39;elenco rilevato automaticamente memorizzato nella sezione di stato dell&#39;Editor attività. La logica aggiornata ora confronta le proprietà rilevate automaticamente con le proprietà correnti nella sezione ~ActivityState~ e impedisce la reaggiunta di eventuali proprietà rilevate automaticamente già rimosse dall&#39;utente. Questo determina un comportamento coerente tra i passaggi e rispetta le intenzioni dell’utente. (TGT-54181)
* **Aggiungere testo rilevato automaticamente all&#39;elenco delle proprietà.** Questo miglioramento aggiorna [!UICONTROL Properties List] per etichettare chiaramente qualsiasi proprietà rilevata automaticamente dal sistema. Quando una proprietà rilevata automaticamente è presente anche in [!UICONTROL Properties List] visibile all&#39;utente, ora viene visualizzato il testo &quot;(Rilevato automaticamente)&quot; accanto al nome, utilizzando il valore archiviato nello stato ~ActivityEditorSlice~. In questo modo viene rispecchiato il comportamento dell’interfaccia utente legacy e gli utenti possono distinguere facilmente tra le proprietà selezionate manualmente e quelle identificate automaticamente. (TGT-54120)
* **Aggiungi [!UICONTROL Properties] rilevato automaticamente allo stato.** Questo aggiornamento assicura che lo stato ~ActivityEditorSlice.ExperienceEditor~ mantenga costantemente un elenco aggiornato di tutti gli ID di proprietà rilevati automaticamente passati dall&#39;editor Web alla scheda Attività [!UICONTROL Experiences]. Ogni volta che l&#39;utente passa alla scheda [!UICONTROL Experiences], lo stato viene aggiornato con le nuove proprietà rilevate, evitando duplicati, garantendo un tracciamento accurato e un comportamento a valle affidabile. (TGT-54119)

+++

**Funzione Consigli**

+++Vedi i dettagli
* Il menu a discesa **[!UICONTROL Environment]mostra solo 100 risultati.** Questa correzione è valida per un limite in base al quale i clienti con più di 100 ambienti possono visualizzare solo le prime 100 voci del menu a discesa [!UICONTROL Environment] in [!UICONTROL Recommendations]. La query GraphQL sottostante (~getEnvironmentsV2~) è stata impaginata con una dimensione di pagina hardcoded pari a 100, causando la visualizzazione nell&#39;interfaccia utente di un elenco parziale anche quando erano disponibili pagine aggiuntive. Per i clienti che hanno più di 100 ambienti, questo problema causava opzioni mancanti e un’esperienza di selezione incompleta. L’aggiornamento aumenta il limite in modo che tutti gli ambienti vengano restituiti e visualizzati, garantendo la visibilità completa indipendentemente dal conteggio degli ambienti. (TGT-53903)

+++

**Rapporti**

+++Vedi i dettagli

* **È stato risolto un problema a causa del quale la freccia [!UICONTROL Reports] non indicava chiaramente le colonne espandibili.** È stato risolto un problema a causa del quale la tabella di reporting non mostrava chiaramente che era possibile espandere colonne aggiuntive nell&#39;interfaccia utente aggiornata. È stata aggiunta una descrizione comando che scompare alla freccia [!UICONTROL Reports] vicino alle intestazioni di colonna per aiutare i clienti a comprendere che sono disponibili più colonne.

+++

**Visualizzazioni**

+++Vedi i dettagli

* **Impossibile eliminare le modifiche applicate alle visualizzazioni.** Questa correzione risolve un problema che impediva agli utenti di eliminare le modifiche all&#39;interno di un&#39;attività, a meno che la modifica non fosse stata riapplicata ad altre viste. Durante la modifica di un’attività (ad esempio, 302467 ID attività), i tentativi di eliminazione di qualsiasi modifica non hanno avuto alcun effetto, impedendo agli utenti di rimuovere le modifiche indesiderate. Tuttavia, una volta riapplicata una modifica utilizzando &quot;Applica a più visualizzazioni&quot; e assegnata a un evento `Page Load`, l&#39;eliminazione ha improvvisamente funzionato come previsto. (TGT-54088)

+++

**[!UICONTROL Visual Experience Composer](VEC)**

+++Vedi i dettagli
* Il nome **[!UICONTROL Experience Fragment]è stato troncato nella nuova interfaccia utente VEC** (TGT-54312)
* **Impossibile utilizzare [!UICONTROL Advanced Settings] per la metrica [!UICONTROL Revenue].** Questa correzione risolve un problema in cui gli utenti hanno riscontrato un errore 403 &quot;Accesso negato&quot; durante la configurazione di [!UICONTROL Advanced Settings] per la metrica [!UICONTROL Revenue] in [!UICONTROL Goals & Settings]. Il problema si verificava quando si aggiungeva una condizione di dipendenza associata all’obiettivo principale; il backend richiedeva erroneamente il privilegio dell’editor anche per gli utenti che disponevano già di autorizzazioni sufficienti per creare e modificare le attività. Di conseguenza, il salvataggio dell’attività non è riuscito nonostante la configurazione valida. L’aggiornamento corregge il controllo delle autorizzazioni in modo che gli utenti con l’accesso appropriato possano aggiungere correttamente le dipendenze della metrica Ricavi senza attivare un errore di risorsa proibita. (TGT-54092)
* **È stato risolto un problema che impediva l&#39;applicazione del pulsante Aggiungi alle immagini selezionate.** È stato risolto un problema che impediva ai clienti di aggiungere determinate immagini durante la selezione o l&#39;aggiornamento di un&#39;immagine nel processo di creazione attività. Quando i clienti hanno cercato risorse specifiche, ad esempio immagini restituite durante la ricerca di &quot;ipp&quot;, facendo clic sul pulsante [!UICONTROL Add] non è stata applicata l&#39;immagine selezionata e non è stata creata alcuna modifica. La selezione di altre immagini, ad esempio `Homepage-banner-1-moz.jpg`, ha continuato a funzionare come previsto. Questo aggiornamento garantisce che tutte le immagini valide possano essere applicate in modo coerente nell’interfaccia utente aggiornata. (TGT-53610)
* **È stato risolto un problema che causava la reimpostazione della configurazione della metrica obiettivo da parte dell&#39;eliminazione di una condizione URL.** È stato risolto un problema che causava la rimozione di una condizione di URL singolo nella metrica [!UICONTROL Goal] e la reimpostazione dell&#39;intera configurazione nell&#39;interfaccia utente aggiornata. Quando i clienti hanno tentato di eliminare una condizione URL salvata in [!UICONTROL Conversion] > [!UICONTROL Viewed a Page], il tipo di obiettivo è passato in modo imprevisto a [!UICONTROL Viewed an Mbox] e tutte le impostazioni configurate in precedenza sono state rimosse. Questo aggiornamento assicura che solo la condizione URL selezionata venga eliminata e che tutte le impostazioni obiettivo rimanenti rimangano intatte. (TGT-53271)
* **È stato risolto un problema che impediva la ricerca nelle sottocartelle.** È stato risolto un problema che impediva alla ricerca di offerte di restituire i risultati dalle sottocartelle nell&#39;interfaccia utente aggiornata. I clienti potevano trovare un’offerta solo se passavano manualmente alla cartella in cui era memorizzata, rendendo il comportamento di ricerca incoerente con le funzionalità API. La funzione di ricerca ora supporta la ricerca ricorsiva nelle cartelle, in modo che i clienti possano individuare le offerte senza dover aprire ogni cartella singolarmente. (TGT-51954)

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
