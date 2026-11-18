---
keywords: risolvere problemi target;risoluzione problemi target;contenuto predefinito;test non live;attività non live;targeting non funzionante;esperienza precedente visualizza;impossibile creare attività;creare attività;struttura pagina modificata;struttura pagina modificata;messaggio di errore;errore elimina script profilo;ajax non funziona
description: Trova suggerimenti per la risoluzione dei problemi, qualora l'attività Adobe [!DNL Target] non venga visualizzata sul tuo sito.
title: Come posso risolvere i problemi relativi alle attività?
feature: Activities
exl-id: 6aa0486a-9ca3-4545-ae06-9b02e586d777
TQID: 'https://experienceleague.adobe.com/L-011t7q6c3aICs0ZrM01m9pZByH86FKGiLG1A7Rl2s'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: 6efa6b7a-8062-5c41-aef4-b4853cc306ae
    internal-label: Activities
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9621044454d3e1b47c06cac2ad5d08cba8e482c0
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 7%
---
# Introduzione alle attività di risoluzione dei problemi {#troubleshooting-activities}

>[!BEGINSHADEBOX]

**In questa pagina:** Trova soluzioni ai problemi più comuni quando un&#39;attività [!DNL Adobe Target] non viene visualizzata sul tuo sito o non si comporta come previsto.

>[!ENDSHADEBOX]

Diverse cause possono impedire la visualizzazione di un&#39;attività [!DNL Adobe Target] sul sito. Utilizza i problemi seguenti e le soluzioni suggerite per identificare la causa e applicare la correzione.

>[!NOTE]
>
>Oltre alle seguenti informazioni sulla risoluzione dei problemi, consulta [Risoluzione dei problemi di Target](/help/main/r-troubleshooting-target/troubleshooting-target.md) per collegamenti ad ulteriori argomenti, domande frequenti e altre informazioni utili sulle attività di risoluzione dei problemi e altre funzionalità in [!DNL Adobe Target].

## L’attività non viene visualizzata come previsto {#not-displayed}

+++ Stai visualizzando il contenuto predefinito

Assicurati che l’attività sia stata completata e attivata.

+++

</br>

+++ L’attività non è live

**Convalida:** Nella scheda **[!UICONTROL Panoramica]**, verifica se l&#39;attività è contrassegnata come inattiva o bozza.

**Opzioni:**

* Attivare l&#39;attività.
* Utilizza i collegamenti di anteprima per visualizzare l’attività inattiva.

+++

</br>

+++ Non sei idoneo per le condizioni di targeting del pubblico

**Convalida:** Rivedi le condizioni di targeting nella pagina **[!UICONTROL Panoramica]**.

**Opzioni:**

* Assicurati di essere idoneo per il pubblico, quindi riprova.
* Utilizza i collegamenti di anteprima per ignorare le condizioni di targeting.

+++

</br>

+++ La pagina non è idonea per le condizioni di targeting della pagina

**Convalida:** Nella pagina **[!UICONTROL Panoramica]**, verifica se la pagina non soddisfa le condizioni di targeting.

**Opzioni:**

* Vai a **[!UICONTROL Compositore esperienza visivo]**, quindi fai clic su URL > Avanzate > pagina corrente.

+++

</br>

+++ Viene visualizzata un’esperienza precedente anziché la nuova esperienza

**Convalida:** Prova una delle opzioni seguenti, quindi prova a visualizzare di nuovo l&#39;esperienza.

**Opzioni:**

* Cancella la cache e i cookie, quindi riprova.
* Prova a utilizzare un altro browser.
* Utilizza la modalità privata o in incognito.

+++

</br>

+++ La struttura della pagina è cambiata dopo la configurazione dell’attività

**Convalida:** Vai al **[!UICONTROL Compositore esperienza visivo]** per l&#39;attività esistente e cerca un messaggio di avviso che indica che i selettori (o la struttura) sono cambiati.

**Opzioni:**

* Ricrea l’attività.

Per ulteriori informazioni su come le modifiche alla pagina influiscono sulla capacità di [!DNL Target] di visualizzare il contenuto, vedere [Scenari di modifica della pagina](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md).

+++

</br>

+++ La struttura della pagina viene modificata durante il caricamento della pagina (in fase di esecuzione)

**Convalida:** Chiedi al tuo sviluppatore.

**Nota:** affinché [!DNL Target] riconosca dove devono essere applicate le modifiche dell&#39;attività, evita di inserire dinamicamente un elemento con la stessa classe o di modificare dinamicamente la classe di qualsiasi elemento di pari livello.

**Opzioni:**

* Aggiorna il codice della pagina per identificare in modo univoco ogni elemento testato, utilizzando un ID.
* Interrompi la modifica dinamica della classe o degli elementi di pari livello come descritto sopra.

Per ulteriori informazioni su come le modifiche alla pagina influiscono sulla capacità di [!DNL Target] di visualizzare il contenuto, vedere [Scenari di modifica della pagina](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md).

+++

</br>

+++ Altre attività sono in esecuzione sulla stessa pagina

**Convalida:** Utilizza la scheda **[!UICONTROL Conflitti]** per verificare se altre attività sono in esecuzione.

**Nota:** la scheda **[!UICONTROL Conflitti]** non funziona con il modulo di test dei modelli.

**Opzioni:**

* Incrementa la priorità di questa attività.
* Diminuire la priorità delle altre attività.
* Disattiva le altre attività.

+++

## Utenti, API e interfaccia utente {#users-api-ui}

+++ Ho creato un&#39;attività utilizzando l&#39;interfaccia utente di [!DNL Target] e non posso aggiornarla tramite API

Le attività create utilizzando l&#39;interfaccia utente [!DNL Target] devono essere aggiornate tramite l&#39;interfaccia utente [!DNL Target]. Le attività create tramite API devono essere aggiornate tramite API. Ad esempio, se crei un&#39;attività utilizzando l&#39;API, ma successivamente la modifichi tramite l&#39;interfaccia utente [!DNL Target], non tutte le modifiche vengono aggiornate. Tutte le modifiche vengono memorizzate sul backend e possono essere aggiornate effettuando un’altra chiamata API.

Come best practice, aggiorna l’attività utilizzando lo stesso metodo (interfaccia utente o API) utilizzato per crearla.

+++

</br>

+++ Sei stato aggiunto di recente a [!DNL Target] ma non puoi creare attività

**Convalida:** Fai Clic Su **[!UICONTROL Crea Attività]**. Se l’opzione non è disponibile, è molto probabile che non disponi delle autorizzazioni necessarie per creare un’attività.

**Opzioni:**

Dopo essere stato aggiunto come utente in [!DNL Target], è necessario il ruolo **[!UICONTROL Approvatore]** per creare attività.

* Chiedi all&#39;amministratore del tuo account di renderti un approvatore.
* Se sei l&#39;amministratore, assegnati il ruolo **[!UICONTROL Approvatore]** da **[!UICONTROL Amministrazione]** > **[!UICONTROL Utenti]** in [!DNL Target]. Consulta [Assegnarsi il ruolo Approvatore](/help/main/administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7).

+++

</br>

+++ Hai attivato un&#39;attività utilizzando l&#39;API [!DNL Target], ma l&#39;attività risulta [!UICONTROL inattiva] nell&#39;interfaccia utente [!DNL Target]

Quando si eseguono determinate azioni, ad esempio l&#39;attivazione di un&#39;attività al di fuori dell&#39;interfaccia utente utilizzando l&#39;API [!DNL Target], l&#39;aggiornamento può richiedere fino a dieci minuti per propagarsi all&#39;interfaccia utente.

+++

</br>

+++ Quando si elimina uno script di profilo viene visualizzato un messaggio di errore

**Convalida:** L&#39;eliminazione di uno script di profilo da [!DNL Target] comporta la visualizzazione del messaggio di errore &quot;Impossibile eliminare lo script di profilo&quot;.

**Opzioni:**

Esegui una delle operazioni seguenti:

* Elimina nuovamente lo script del profilo. Viene visualizzato il messaggio di operazione eseguita correttamente.
* Attendere circa 10 minuti per l&#39;esecuzione dell&#39;importazione [!DNL Target]. L’importazione aggiorna l’elenco degli script di profilo.

+++

## Chiamate e conversione {#calls-and-conversion}

+++ Alcune chiamate AJAX [!DNL Target] non funzionano

**Nota:** più chiamate AJAX [!DNL Target] con lo stesso nome ma diversi parametri non funzionano sulla stessa pagina. Viene effettuata solo la prima chiamata.

+++

</br>

+++ Dopo la conversione dell’attività, il visitatore non si trova in alcuna esperienza

In rari casi, se la metrica di conversione dell’attività che qualifica un visitatore per un’esperienza viene inviata nella stessa richiesta della qualifica dell’attività, il visitatore potrebbe non trovarsi in alcuna esperienza dopo l’invio della richiesta. In questa situazione, il visitatore visualizza il contenuto predefinito e l&#39;ID esperienza acquisito tramite i token è -1. [!DNL Adobe] sconsiglia di inviare qualificazione e conversione attività nella stessa richiesta [!DNL Target].

Se desideri inviare entrambe le metriche nella stessa richiesta, puoi utilizzare **[!UICONTROL Impostazioni avanzate]** per specificare che il visitatore rimane nella stessa esperienza dopo la conversione.

+++
