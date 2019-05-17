---
description: Se l’attività non viene visualizzata sul sito, questi suggerimenti dovrebbero agevolare la risoluzione del problema.
keywords: risolvi problemi di Target;risoluzione problemi di Target;contenuto predefinito;test non live;attività non live;targeting non funzionante;visualizzazione esperienza precedente;impossibile creare attività;creare attività;struttura pagina modificata;struttura pagina cambiata;messaggio di errore;errore elimina script profilo;AJAX non funziona
seo-description: Se l’attività non viene visualizzata sul sito, questi suggerimenti dovrebbero agevolare la risoluzione del problema.
seo-title: Risolvere i problemi relativi alle attività
solution: Target
title: Risolvere i problemi relativi alle attività
topic: Advanced,Standard,Classic
uuid: 5b22c369-0efc-48c0-a0dc-0179b18536fe
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Risolvere i problemi relativi alle attività{#troubleshoot-activities}

Se l’attività non viene visualizzata sul sito, questi suggerimenti dovrebbero agevolare la risoluzione del problema.

>[!NOTE]
>
>Oltre alle seguenti informazioni sulla risoluzione di problemi, consulta [Risoluzione dei problemi di Target](../../r-troubleshooting-target/troubleshooting-target.md#reference_A9DB82675D044BD8861F6752A4EE6839) per collegamenti ad ulteriori argomenti, domande frequenti e altre informazioni utili sulle attività di risoluzione dei problemi e altre funzionalità in [!DNL Adobe Target].

Nelle seguenti sezioni sono descritti problemi che potresti incontrare con le soluzioni suggerite.

## Viene visualizzato il contenuto predefinito.

Assicurati che l’attività sia completa e che sia stata attivata.

## L’attività non è live.

**Convalida:** apri la scheda della panoramica per visualizzare se il test è contrassegnato come inattivo o come bozza.

**Opzioni:**

* Attiva il test.
* Utilizza i collegamenti di anteprima per visualizzare il test inattivo.

## L’utente non soddisfa le condizioni per il targeting del pubblico.

**Convalida:** rivedi le condizioni di targeting nella pagina della panoramica.

**Opzioni:**

* Fai in modo di soddisfare le condizioni e riprova.
* Utilizza i collegamenti di anteprima per ignorare le condizioni di targeting.

## La pagina non soddisfa le condizioni di targeting.

**Convalida:** nella pagina della panoramica verifica se la pagina non soddisfa le condizioni di targeting.

**Opzioni:**

* Apri il Compositore esperienza visivo e fai clic su URL\&gt; Avanzate\&gt;pagina corrente.

## Viene visualizzata un’esperienza precedente anziché quella nuova.

**Convalida:** prova ad applicare una delle opzioni qui di seguito e riprova a visualizzare l’esperienza.

**Opzioni:**

* Elimina il contenuto della cache e i cookie e riprova.

* Prova a utilizzare un altro browser.
* Utilizza la modalità Privata/Navigazione anonima.

## Sei stato aggiunto di recente a Target ma non puoi creare attività.

**Convalida:** fai clic su Crea attività. Se l’opzione non è disponibile, è molto probabile che non disponi delle autorizzazioni necessarie per creare un’attività.

**Opzioni:**

Una volta aggiunto come utente in Target, devi disporre del ruolo Approvatore per creare le attività.

* Chiedi all’amministratore del tuo account di assegnarti il ruolo Approvatore.
* Se sei l’amministratore, assegnati il ruolo Approvatore da Configurazione &gt; Utenti in Target Standard.

   Consulta [Assegnare a se stessi il ruolo di Approvatore](../../administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7).

## La struttura della pagina è cambiata dal momento della configurazione dell’attività.

**Convalida:** apri Compositore esperienza visivo per l’attività esistente. Ricerca un messaggio di avviso che indica che i selettori (o la struttura) sono cambiati.

**Opzioni:**

* Ricrea l’attività.

Per ulteriori informazioni su come le modifiche alla pagina influiscono sulla capacità di visualizzazione di Target, vedi  [Scenari di modifica delle pagine](../../c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## La struttura della pagina viene modificata durante il caricamento (in fase di esecuzione).

**Convalida:** interpella lo sviluppatore.

**Nota:** per consentire a Target di riconoscere dove dovrebbero essere applicate le modifiche all’attività, evita di inserire in modo dinamico elementi con la stessa classe o di modificare in modo dinamico la classe di eventuali elementi di pari livello.

**Opzioni:**

* Aggiorna il codice della pagina in modo da identificare in modo univoco ogni elemento che sarà oggetto di test (utilizzando un id).
* Interrompi la modifica dinamica della classe o degli elementi di pari livello come descritto sopra.

Per ulteriori informazioni su come le modifiche alla pagina influiscono sulla capacità di visualizzazione di Target, vedi  [Scenari di modifica delle pagine](../../c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Mbox.js estrae tutto il codice successivo dalla sezione head e nella sezione body.

**Convalida:** visualizza l’origine per determinare se una delle dichiarazioni segue il file mbox.js prima del tag di chiusura </body> .

**Opzioni:**

* Posiziona mbox.js come ultimo elemento all’interno della sezione `<head>` della pagina.
* Utilizza div id univoci per gli elementi di primo livello all’interno della sezione body.

## Altre attività sono in esecuzione sulla stessa pagina.

**Convalida:** utilizza la scheda Conflitti per vedere se altre attività sono in esecuzione.

**Nota:** la scheda Conflitti non funziona con il modulo Test modelli.

**Opzioni:**

* Incrementa la priorità di questa attività.
* Riduci la priorità delle altre attività.
* Disattiva le altre attività.

## Quando elimini uno script di profilo, viene visualizzato un messaggio di errore.

**Convalida:** se elimini uno script di profilo da Target Standard/Premium, viene visualizzato il messaggio di errore “Impossibile eliminare lo script del profilo”.

**Opzioni:**

Esegui una delle operazioni seguenti:

* Riprova a eliminarlo. Viene visualizzato il messaggio di operazione eseguita correttamente.
* Attendi circa 10 minuti per l’importazione di Target Standard/Premium. L’importazione aggiorna l’elenco degli script di profilo.

## Alcune chiamate AJAX mbox non funzionano.

**Nota:** se una stessa pagina contiene più chiamate mbox AJAX con lo stesso nome mbox ma diversi parametri, queste non funzioneranno correttamente. Viene effettuata solo la prima chiamata.

## Hai attivato un’attività utilizzando l’API di Target, ma l’attività risulta inattiva nell’interfaccia utente di Target.

Quando esegui determinate azioni, ad esempio l’attivazione di un’attività al di fuori dell’interfaccia utente utilizzando l’API di Target, l’aggiornamento può richiedere fino a dieci minuti per propagarsi all’interfaccia utente.