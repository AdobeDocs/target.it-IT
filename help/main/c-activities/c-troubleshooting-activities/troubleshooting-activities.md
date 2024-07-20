---
keywords: risolvi problemi di Target;risoluzione problemi di Target;contenuto predefinito;test non live;attività non live;targeting non funzionante;visualizzazione esperienza precedente;impossibile creare attività;creare attività;struttura pagina modificata;struttura pagina cambiata;messaggio di errore;errore elimina script profilo;AJAX non funziona
description: Trova suggerimenti per la risoluzione dei problemi, qualora l’attività Adobe  [!DNL Target]  non venga visualizzata sul tuo sito.
title: Come posso risolvere i problemi relativi alle attività?
feature: Activities
exl-id: 6aa0486a-9ca3-4545-ae06-9b02e586d777
source-git-commit: f1cbc46323f71c2fa091cd2c9a3e49d34676e7a1
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 44%

---

# Risolvere i problemi relativi alle attività

Se l’attività [!DNL Adobe Target] non viene visualizzata sul sito, questi suggerimenti dovrebbero facilitare la risoluzione del problema.

>[!NOTE]
>
>Oltre alle seguenti informazioni sulla risoluzione di problemi, consulta [Risoluzione dei problemi di Target](/help/main/r-troubleshooting-target/troubleshooting-target.md#reference_A9DB82675D044BD8861F6752A4EE6839) per collegamenti ad ulteriori argomenti, domande frequenti e altre informazioni utili sulle attività di risoluzione dei problemi e altre funzionalità in [!DNL Adobe Target].

Nelle sezioni seguenti sono riportati problemi che potresti incontrare con le soluzioni suggerite.

## Ho creato un’attività utilizzando l’interfaccia utente di [!DNL Target] e non posso aggiornarla tramite API.

Le attività create utilizzando l&#39;interfaccia utente [!DNL Target] devono essere aggiornate tramite l&#39;interfaccia utente [!DNL Target]. Le attività create tramite API devono essere aggiornate tramite API. Se, ad esempio, crei un&#39;attività utilizzando l&#39;API ma successivamente la modifichi tramite l&#39;interfaccia utente [!DNL Target], non tutte le modifiche vengono aggiornate. Tutte le modifiche vengono memorizzate sul backend e possono essere aggiornate effettuando un’altra chiamata API.

Come best practice, prova ad aggiornare l’attività utilizzando lo stesso metodo (interfaccia utente o API) utilizzato per creare l’attività stessa.

## Viene visualizzato il contenuto predefinito.

Assicurati che l’attività sia stata completata e attivata.

## L’attività non è live.

**Convalida:** Vai alla scheda [!UICONTROL Overview] e controlla se il test è contrassegnato come inattivo o come bozza.

**Opzioni:**

* Attiva il test.
* Utilizza i collegamenti di anteprima per visualizzare il test inattivo.

## Non sei idoneo per le condizioni di targeting del pubblico.

**Convalida:** rivedi le condizioni di targeting nella pagina della panoramica.

**Opzioni:**

* Fai in modo di soddisfare le condizioni e riprova.
* Utilizza i collegamenti di anteprima per ignorare le condizioni di targeting.

## La pagina non è idonea per le condizioni di targeting della pagina.

**Convalida:** Nella pagina [!UICONTROL Overview], verifica se la pagina non soddisfa le condizioni di targeting.

**Opzioni:**

* Vai a [!UICONTROL Visual Experience Composer], fai clic su URL > Avanzate > pagina corrente.

## Viene visualizzata un’esperienza precedente anziché quella nuova.

**Convalida:** prova ad applicare una delle opzioni qui di seguito e riprova a visualizzare l’esperienza.

**Opzioni:**

* Elimina il contenuto della cache e i cookie e riprova.
* Prova a utilizzare un altro browser.
* Utilizza la modalità Privata/Navigazione anonima.

## Sei stato aggiunto di recente a [!DNL Target] ma non puoi creare attività.

**Convalida:** Fare clic su [!UICONTROL Create Activity]. Se l’opzione non è disponibile, è molto probabile che non disponi delle autorizzazioni necessarie per creare un’attività.

**Opzioni:**

Dopo essere stato aggiunto come utente in [!DNL Target], è necessario disporre del ruolo [!UICONTROL Approver] per creare attività.

* Chiedi all&#39;amministratore del tuo account di renderti un approvatore.
* Se sei l&#39;amministratore, assegnati il ruolo [!UICONTROL Approver] da **[!UICONTROL Administration]** > **[!UICONTROL Users]** in [!DNL Target].

  Consulta [Assegnare a se stessi il ruolo di Approvatore](/help/main/administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7).

## La struttura della pagina è cambiata dal momento della configurazione dell’attività.

**Convalida:** Vai a [!UICONTROL Visual Experience Composer] per l&#39;attività esistente. Ricerca un messaggio di avviso che indica che i selettori (o la struttura) sono cambiati.

**Opzioni:**

* Ricrea l’attività.

Per ulteriori informazioni su come le modifiche di pagina influiscono sulla capacità di visualizzazione di [!DNL Target], vedere [Scenari di modifica delle pagine](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## La struttura della pagina viene modificata durante il caricamento (in fase di esecuzione).

**Convalida:** interpella lo sviluppatore.

**Nota:** affinché [!DNL Target] riconosca dove applicare le modifiche all&#39;attività, evita di inserire dinamicamente un elemento con la stessa classe o di modificare dinamicamente la classe di qualsiasi elemento di pari livello.

**Opzioni:**

* Aggiorna il codice della pagina per identificare in modo univoco ogni elemento testato (utilizzando un ID).
* Interrompi la modifica dinamica della classe o degli elementi di pari livello come descritto sopra.

Per ulteriori informazioni su come le modifiche di pagina influiscono sulla capacità di visualizzazione di [!DNL Target], vedere [Scenari di modifica delle pagine](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Altre attività sono in esecuzione sulla stessa pagina.

**Convalida:** Utilizzare la scheda [!UICONTROL Collisions] per verificare se sono in esecuzione altre attività.

**Nota:** la scheda [!UICONTROL Collisions] non funziona con il modulo Test modello.

**Opzioni:**

* Incrementa la priorità di questa attività.
* Riduci la priorità delle altre attività.
* Disattiva le altre attività.

## Quando elimini uno script di profilo, viene visualizzato un messaggio di errore.

**Convalida:** L&#39;eliminazione di uno script di profilo da [!DNL Target] comporta la visualizzazione del messaggio di errore &quot;Impossibile eliminare lo script di profilo&quot;.

**Opzioni:**

Esegui una delle operazioni seguenti:

* Elimina nuovamente lo script del profilo. Viene visualizzato il messaggio di operazione eseguita correttamente.
* Attendere circa 10 minuti per l&#39;esecuzione dell&#39;importazione [!DNL Target]. L’importazione aggiorna l’elenco degli script di profilo.

## Alcune chiamate AJAX di [!DNL Target] non funzionano.

**Nota:** più chiamate AJAX [!DNL Target] con lo stesso nome ma diversi parametri non funzionano sulla stessa pagina. Viene effettuata solo la prima chiamata.

## Hai attivato un&#39;attività utilizzando l&#39;API [!DNL Target], ma l&#39;attività mostra uno stato di [!UICONTROL Inactive] nell&#39;interfaccia utente [!DNL Target].

Quando si eseguono determinate azioni, ad esempio l&#39;attivazione di un&#39;attività al di fuori dell&#39;interfaccia utente tramite l&#39;API [!DNL Target], l&#39;aggiornamento può richiedere fino a dieci minuti per propagarsi all&#39;interfaccia utente.

## Dopo la conversione dell’attività, il visitatore non si trova in alcuna esperienza.

In rari casi, se la metrica di conversione dell’attività per qualificarsi per un’esperienza viene inviata nella stessa richiesta di qualificazione dell’attività, il visitatore potrebbe non trovarsi in alcuna esperienza dopo l’invio della richiesta. In questa situazione, il visitatore vede che il contenuto predefinito e l&#39;ID esperienza acquisito tramite i token sarebbe -1. [!DNL Adobe] non consiglia di inviare qualificazione e conversione attività nella stessa richiesta [!DNL Target].

Se desideri inviare entrambe le metriche nella stessa richiesta, puoi utilizzare [!UICONTROL Advanced Settings] per specificare che il visitatore rimane nella stessa esperienza dopo la conversione.
