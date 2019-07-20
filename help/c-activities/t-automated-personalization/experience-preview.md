---
description: Gli URL di esperienza possono essere generati per le attività di Personalizzazione automatizzata di Target per visualizzare il contenuto dell’esperienza direttamente sul sito prima che l’attività venga pubblicata, per scopi di anteprima e controllo qualità. Gli URL di esperienza ignorano il targeting per forzare la visualizzazione di una particolare esperienza.
keywords: Anteprima esperienza;URL esperienza;generare URL;visualizzare gli URL esperienza
seo-description: Gli URL di esperienza possono essere generati per le attività di Personalizzazione automatizzata di Target per visualizzare il contenuto dell’esperienza direttamente sul sito prima che l’attività venga pubblicata, per scopi di anteprima e controllo qualità. Gli URL di esperienza ignorano il targeting per forzare la visualizzazione di una particolare esperienza.
seo-title: Condividere gli URL di esperienza per visualizzare in anteprima la personalizzazione automatizzata al di fuori di Target
solution: Target
title: Condividere gli URL di esperienza per visualizzare in anteprima la personalizzazione automatizzata al di fuori di Target
title-outputclass: premium
topic: Standard
uuid: 2ef07b6c-086d-43ac-bf02-efe217652a3a
badge: premium
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# ![PREMIUM](/help/assets/premium.png) Condividere gli URL di esperienza per visualizzare in anteprima la personalizzazione automatizzata al di fuori di Target{#share-experience-urls-to-preview-automated-personalization-outside-of-target}

Gli URL di esperienza possono essere generati per le attività di Personalizzazione automatizzata di Target per visualizzare il contenuto dell’esperienza direttamente sul sito prima che l’attività venga pubblicata, per scopi di anteprima e controllo qualità. Gli URL di esperienza ignorano il targeting per forzare la visualizzazione di una particolare esperienza.

>[!NOTE]
>
>La modalità di controllo qualità delle attività consente di creare URL per altri tipi di attività. Per ulteriori informazioni, consulta [Controllo qualità delle attività](../../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40)

.

Per utilizzare gli URL di esperienza, devi condividere i collegamenti generati da Target, non l'URL finale di destinazione in cui visualizzi l'esperienza. Inoltre, se il contenuto cambia, è necessario generare nuovi URL. Se si generano nuovi URL, i vecchi potrebbero non funzionare.

Tramite gli URL di esperienza, non solo puoi condividere esperienze con i membri del gruppo, ma anche esperienze di controllo qualità attraverso i browser e gli ambienti, senza creare un'attività di controllo qualità distinta. Questa funzione è particolarmente utile in caso di siti complessi o se le policy di sicurezza non consentono la visualizzazione del sito in un simulatore.

1. Crea un’[attività di personalizzazione automatizzata](../../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9) oppure fai clic sull’attività per aprirla.

   L'attività non deve essere live per visualizzare un'anteprima dell'esperienza.
1. Nella pagina di riepilogo attività, fai clic sui tre punti verticali, quindi scegli **[!UICONTROL Visualizza gli URL di esperienza]**.
1. Rivedi e/o definisci gli URL.

   * Se utilizzi il Compositore esperienza visivo, l'URL predefinito specificato per l'attività viene immesso automaticamente e viene generato un collegamento per ogni esperienza nell'attività. Se lo desideri, puoi modificare questo URL e aggiungerne altri.
   * Se utilizzi il Compositore esperienza basato su moduli, non viene immesso automaticamente alcun URL predefinito. Se non hai creato gli URL di esperienza, fai clic su **Aggiungi nuovo URL**. Devi specificare tutti gli URL che desideri visualizzare in anteprima e un nome per ognuno.
   Puoi aggiungere più URL, tale opzione è utile quando esegui un test a più pagine o un test modello e desideri visualizzare in anteprima l'attività su più di una pagina.

   Tramite una finestra modale, puoi visualizzare i collegamenti alle esperienze sul tuo sito per ottenere una “anteprima fedele” al di fuori del Compositore esperienza visivo. Per condividere l’anteprima, è necessario condividere i collegamenti dal messaggio. Non è possibile fare clic su un collegamento e poi copiare l'URL risultante direttamente dalla pagina, perché l'URL contiene un parametro che visualizza la pagina correttamente solo quando si accede alla pagina dal collegamento nel messaggio. Invece, copia il testo nella finestra modale e invialo all'intero team.
1. Fai clic su **[!UICONTROL Genera tutto]** e poi su ogni esperienza per visualizzarne l’anteprima.

   Se apporti modifiche all'esperienza, assicurati di generare nuovi collegamenti di anteprima per il team. Torna alla finestra modale e fai clic su **Genera tutto** per ottenere nuovi collegamenti.

   **Nota:** i collegamenti di anteprima si aprono in nuove schede e richiedono che nel browser venga disattivato il blocco dei popup.

1. Fai clic su ogni nome di esperienza per visualizzare l’anteprima dell’attività.

   L’attività viene visualizzata nella pagina.
1. Fai clic su **[!UICONTROL Fine]** per tornare al riepilogo delle attività.

## Considerazioni {#example_9F2B333BC63143FF99AE331F57E8BA4C}

**Generazione degli URL delle esperienze**

* L’URL dell’esperienza non è interessato dalla suddivisione del traffico tra le varie esperienze.
* Il targeting a livello di pubblico non influisce sull’anteprima.
* Puoi generare automaticamente un massimo di 300 URL di esperienza per ogni attività. Dopo di che, dovrai generare gli URL manualmente.
* Puoi generare automaticamente un massimo di 300 URL di esperienza per ogni attività. Dopo di che, dovrai generare gli URL manualmente.
* A seconda del numero di esperienze, la generazione degli URL può richiedere fino a cinque minuti. Non chiudere la finestra di dialogo, altrimenti gli URL generati verranno persi.
* I collegamenti di anteprima generati sono validi per due mesi. Al termine di questo periodo, dovrai generarli di nuovo.
* Devi generare di nuovo URL ogni volta che un’esperienza viene cambiata.

**Condivisione degli URL delle esperienze**

* Puoi visualizzare in anteprima un esperienza anche se non fai parte del pubblico di destinazione.
* Puoi condividere gli URL delle esperienze con i colleghi che non hanno accesso ad Adobe Target.

**Visualizzazione delle esperienze con gli URL delle esperienze**

* L’anteprima funziona per qualsiasi attività salvata, purché la pagina non venga modificata.
* L’URL dell’esperienza è disponibile se l'attività è attiva o inattiva.
* Non puoi visualizzare in anteprima un’esperienza in stato Bozza
* La visualizzazione in anteprima con gli URL delle esperienze non ha alcun impatto sui rapporti.

**Risoluzione dei problemi relativi agli URL delle esperienza**

* Se non puoi visualizzare l’anteprima nella nuova scheda (a causa della cache del browser), prova ad aggiornare due o tre volte oppure copia il collegamento e aprilo in un nuovo browser, una nuova sessione o in modalità browser privato.
* Sia che tu esegua direttamente il controllo qualità per la tua attività sia che inoltri i collegamenti a un altro team, puoi visualizzare facilmente un’anteprima delle esperienze specifiche, senza configurare test separati.

