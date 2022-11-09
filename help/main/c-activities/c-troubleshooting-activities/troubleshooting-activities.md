---
keywords: risolvi problemi di Target;risoluzione problemi di Target;contenuto predefinito;test non live;attività non live;targeting non funzionante;visualizzazione esperienza precedente;impossibile creare attività;creare attività;struttura pagina modificata;struttura pagina cambiata;messaggio di errore;errore elimina script profilo;AJAX non funziona
description: Trova suggerimenti per la risoluzione dei problemi, qualora l’attività Adobe  [!DNL Target]  non venga visualizzata sul tuo sito.
title: Come posso risolvere i problemi relativi alle attività?
feature: Activities
exl-id: 6aa0486a-9ca3-4545-ae06-9b02e586d777
source-git-commit: f1cbc46323f71c2fa091cd2c9a3e49d34676e7a1
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 50%

---

# Risolvere i problemi relativi alle attività

Se l’attività [!DNL Adobe Target] non viene visualizzata sul sito, questi suggerimenti dovrebbero facilitare la risoluzione del problema.

>[!NOTE]
>
>Oltre alle seguenti informazioni sulla risoluzione di problemi, consulta [Risoluzione dei problemi di Target](/help/main/r-troubleshooting-target/troubleshooting-target.md#reference_A9DB82675D044BD8861F6752A4EE6839) per collegamenti ad ulteriori argomenti, domande frequenti e altre informazioni utili sulle attività di risoluzione dei problemi e altre funzionalità in [!DNL Adobe Target].

Le sezioni seguenti contengono problemi che potresti incontrare con le soluzioni suggerite.

## Ho creato un’attività utilizzando l’interfaccia utente di [!DNL Target] e non posso aggiornarla tramite API.

Attività create utilizzando [!DNL Target] L’interfaccia utente deve essere aggiornata tramite [!DNL Target] Interfaccia utente. Le attività create tramite API devono essere aggiornate tramite API. Se originariamente crei un’attività utilizzando l’API, ad esempio, ma successivamente modifichi l’attività tramite il [!DNL Target] Interfaccia utente, non tutte le modifiche vengono aggiornate. Tutte le modifiche sono memorizzate sul backend e possono essere aggiornate effettuando un’altra chiamata API.

Come best practice, prova ad aggiornare l’attività utilizzando lo stesso metodo (interfaccia utente o API) utilizzato per creare l’attività stessa.

## Viene visualizzato il contenuto predefinito.

Assicurati che l&#39;attività sia completa e sia stata attivata.

## L’attività non è live.

**Convalida:** Vai a [!UICONTROL Panoramica] controlla se il test è contrassegnato come inattivo o come bozza.

**Opzioni:**

* Attiva il test.
* Utilizza i collegamenti di anteprima per visualizzare il test inattivo.

## Non ti qualifichi per le condizioni di targeting del pubblico.

**Convalida:** rivedi le condizioni di targeting nella pagina della panoramica.

**Opzioni:**

* Fai in modo di soddisfare le condizioni e riprova.
* Utilizza i collegamenti di anteprima per ignorare le condizioni di targeting.

## La pagina non soddisfa le condizioni di targeting della pagina.

**Convalida:** Sulla [!UICONTROL Panoramica] , determina se la pagina non soddisfa le condizioni di targeting.

**Opzioni:**

* Vai a [!UICONTROL Compositore esperienza visivo], fai clic su URL > Avanzate > pagina corrente.

## Viene visualizzata un’esperienza precedente anziché quella nuova.

**Convalida:** prova ad applicare una delle opzioni qui di seguito e riprova a visualizzare l’esperienza.

**Opzioni:**

* Elimina il contenuto della cache e i cookie e riprova.
* Prova a utilizzare un altro browser.
* Utilizza la modalità Privata/Navigazione anonima.

## Sei stato aggiunto di recente a [!DNL Target] ma non puoi creare attività.

**Convalida:**[!UICONTROL  fai clic su Crea attività]. Se l’opzione non è disponibile, è molto probabile che non disponi delle autorizzazioni necessarie per creare un’attività.

**Opzioni:**

Dopo aver aggiunto come utente in [!DNL Target], è necessario disporre del [!UICONTROL Approvatore] per creare attività.

* Chiedi all&#39;amministratore del tuo account di renderti approvatore.
* Se sei l’amministratore, assegnati il [!UICONTROL Approvatore] ruolo da **[!UICONTROL Amministrazione]** > **[!UICONTROL Utenti]** in [!DNL Target].

   Consulta [Assegnare a se stessi il ruolo di Approvatore](/help/main/administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7).

## La struttura della pagina è cambiata dal momento della configurazione dell’attività.

**Convalida:**[!UICONTROL  apri Compositore esperienza visivo per l’attività esistente. ] Ricerca un messaggio di avviso che indica che i selettori (o la struttura) sono cambiati.

**Opzioni:**

* Ricrea l’attività.

Per ulteriori informazioni sull’effetto delle modifiche alle pagine [!DNL Target]la possibilità di visualizzare, vedere [Scenari di modifica delle pagine](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## La struttura della pagina viene modificata durante il caricamento (in fase di esecuzione).

**Convalida:** interpella lo sviluppatore.

**Nota:** Per [!DNL Target] per riconoscere dove devono essere applicate le modifiche all’attività, evita di inserire in modo dinamico un elemento con la stessa classe o di modificare in modo dinamico la classe di eventuali elementi di pari livello.

**Opzioni:**

* Aggiorna il codice della pagina in modo da identificare in modo univoco ogni elemento testato (utilizzando un id).
* Interrompi la modifica dinamica della classe o degli elementi di pari livello come descritto sopra.

Per ulteriori informazioni sull’effetto delle modifiche alle pagine [!DNL Target]la possibilità di visualizzare, vedere [Scenari di modifica delle pagine](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Altre attività sono in esecuzione sulla stessa pagina.

**Convalida:** Utilizza la [!UICONTROL Conflitti] per vedere se altre attività sono in esecuzione.

**Nota:**[!UICONTROL  la scheda Conflitti non funziona con il modulo Test modelli.]

**Opzioni:**

* Incrementa la priorità di questa attività.
* Riduci la priorità delle altre attività.
* Disattiva le altre attività.

## Quando elimini uno script di profilo, viene visualizzato un messaggio di errore.

**Convalida:**[!DNL Target] se elimini uno script di profilo da , viene visualizzato il messaggio di errore “Impossibile eliminare lo script del profilo”.

**Opzioni:**

Esegui una delle operazioni seguenti:

* Elimina nuovamente lo script del profilo. Viene visualizzato il messaggio di operazione eseguita correttamente.
* Attendi circa 10 minuti per la [!DNL Target] Importazione da eseguire. L’importazione aggiorna l’elenco degli script di profilo.

## Alcune chiamate AJAX di [!DNL Target] non funzionano.

**Nota:** Ajax multiplo [!DNL Target] le chiamate con lo stesso nome ma con parametri diversi non funzionano sulla stessa pagina. Viene effettuata solo la prima chiamata.

## Hai attivato un’attività utilizzando l’API di [!DNL Target], ma l’attività risulta [!UICONTROL inattiva] nell’interfaccia utente di [!DNL Target].

Quando esegui determinate azioni, ad esempio l’attivazione di un’attività al di fuori dell’interfaccia utente tramite la [!DNL Target] API, l’aggiornamento può richiedere fino a dieci minuti per propagarsi all’interfaccia utente.

## Dopo la conversione dell’attività, il visitatore non è in alcuna esperienza.

In rari casi, se la metrica di conversione dell’attività per qualificarsi per un’esperienza viene inviata nella stessa richiesta della qualifica dell’attività, il visitatore potrebbe non trovarsi in alcuna esperienza dopo l’invio della richiesta. In questa situazione, il visitatore visualizza il contenuto e l’ID esperienza predefiniti acquisiti tramite token pari a -1. [!DNL Adobe] non consiglia di inviare la qualifica e la conversione dell’attività nello stesso [!DNL Target] richiesta.

Se desideri inviare entrambe le metriche nella stessa richiesta, puoi utilizzare [!UICONTROL Impostazioni avanzate] per specificare che il visitatore rimane nella stessa esperienza dopo la conversione.
