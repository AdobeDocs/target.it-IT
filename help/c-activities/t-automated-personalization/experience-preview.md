---
keywords: experience preview;experience urls;generate urls;view experience urls
description: Gli URL di anteprima esperienza possono essere generati per le attività di Target  Automated Personalization per visualizzare il contenuto dell'esperienza direttamente sul sito prima che l'attività sia live a scopo di anteprima e di QA. Gli URL di anteprima esperienza aggirano il targeting per forzare la visualizzazione di una particolare esperienza.
title: Anteprima delle attività Personalizzazione automatizzata con URL di anteprima dell’esperienza
feature: Automated Personalization
translation-type: tm+mt
source-git-commit: 4adade56529fb95e4400e06d04d3c6c69e120edc
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 65%

---


# ![](/help/assets/premium.png) PREMIUMPreview  attività Automated Personalization con URL di anteprima esperienza

Gli URL di anteprima esperienza possono essere generati per le attività di Target  Automated Personalization per visualizzare il contenuto dell&#39;esperienza direttamente sul sito prima che l&#39;attività sia live a scopo di anteprima e di QA. Gli URL di anteprima esperienza aggirano il targeting per forzare la visualizzazione di una particolare esperienza.

>[!NOTE]
>
>Gli URL di anteprima esperienza per  Automated Personalization sono diversi dalla modalità di QA dell&#39;attività. La modalità di controllo qualità delle attività consente di creare URL per altri tipi di attività. Per ulteriori informazioni, consulta [Controllo qualità delle attività](/help/c-activities/c-activity-qa/activity-qa.md).
>
>Gli URL di anteprima esperienza per le attività AP sono disponibili solo quando si utilizza at.js 1.x. Gli URL di anteprima esperienza per le attività AP non sono attualmente supportati per at.js 2.x.

Utilizzate gli URL di anteprima esperienza per condividere esperienze con i membri del team e per esperienze di QA tra browser e ambienti, senza creare un&#39;attività di QA separata. Questa funzione è particolarmente utile in caso di siti complessi o se le policy di sicurezza non consentono la visualizzazione del sito in un simulatore.

1. Crea un’[attività di personalizzazione automatizzata](/help/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9) oppure fai clic sull’attività per aprirla.

   L&#39;attività non deve essere live per visualizzare un&#39;anteprima dell&#39;esperienza.
1. Nella pagina di riepilogo attività, fai clic sui tre punti verticali, quindi scegli **[!UICONTROL Visualizza gli URL di esperienza]**.
1. Rivedi e/o definisci gli URL.

   * Se utilizzi il Compositore esperienza visivo, l&#39;URL predefinito specificato per l&#39;attività viene immesso automaticamente e viene generato un collegamento per ogni esperienza nell&#39;attività. Se lo desideri, puoi modificare questo URL e aggiungerne altri.
   * Se utilizzi il Compositore esperienza basato su moduli, non viene immesso automaticamente alcun URL predefinito. Se non avete creato precedentemente gli URL di anteprima dell&#39;esperienza, fate clic su **Aggiungi nuovo URL**. Devi specificare tutti gli URL che desideri visualizzare in anteprima e un nome per ognuno.

   Puoi aggiungere più URL, tale opzione è utile quando esegui un test a più pagine o un test modello e desideri visualizzare in anteprima l&#39;attività su più di una pagina.

   Tramite una finestra modale, puoi visualizzare i collegamenti alle esperienze sul tuo sito per ottenere una “anteprima fedele” al di fuori del Compositore esperienza visivo. Per condividere l’anteprima, è necessario condividere i collegamenti dal messaggio. Non è possibile fare clic su un collegamento e poi copiare l&#39;URL risultante direttamente dalla pagina, perché l&#39;URL contiene un parametro che visualizza la pagina correttamente solo quando si accede alla pagina dal collegamento nel messaggio. Invece, copia il testo nella finestra modale e invialo all&#39;intero team.
1. Fai clic su **[!UICONTROL Genera tutto]** e poi su ogni esperienza per visualizzarne l’anteprima.

   Se modificate l&#39;esperienza, accertatevi di generare nuovi collegamenti di anteprima per il team tornando alla finestra modale e facendo clic su **Rinnova collegamenti** per ottenere nuovi collegamenti.

   **Nota:** i collegamenti di anteprima si aprono in nuove schede e richiedono che nel browser venga disattivato il blocco dei popup.

1. Fai clic su ogni nome di esperienza per visualizzare l’anteprima dell’attività.

   L’attività viene visualizzata nella pagina.
1. Fai clic su **[!UICONTROL Fine]** per tornare al riepilogo delle attività.

## Considerazioni {#example_9F2B333BC63143FF99AE331F57E8BA4C}

**Generazione degli URL di anteprima esperienza**

* L&#39;URL di anteprima dell&#39;esperienza non viene influenzato dalla divisione del traffico tra le esperienze.
* Il targeting a livello di pubblico non influisce sull’anteprima.
* Puoi generare automaticamente un massimo di 300 URL di esperienza per ogni attività. Dopo di che, dovrai generare gli URL manualmente.
* Puoi generare automaticamente un massimo di 300 URL di esperienza per ogni attività. Dopo di che, dovrai generare gli URL manualmente.
* A seconda del numero di esperienze, la generazione degli URL può richiedere fino a cinque minuti. Non chiudere la finestra di dialogo, altrimenti gli URL generati verranno persi.
* I collegamenti di anteprima generati sono validi per due mesi. Al termine di questo periodo, dovrai generarli di nuovo.
* Devi generare di nuovo URL ogni volta che un’esperienza viene cambiata.

**Condivisione degli URL di anteprima esperienza**

* Puoi visualizzare in anteprima un esperienza anche se non fai parte del pubblico di destinazione.
* Potete condividere gli URL di anteprima dell&#39;esperienza con colleghi che non hanno accesso a  Adobe Target.

**Visualizzazione delle esperienze con gli URL di anteprima esperienza**

* L’anteprima funziona per qualsiasi attività salvata, purché la pagina non venga modificata.
* L&#39;URL di anteprima esperienza è disponibile sia che l&#39;attività sia attiva che inattiva.
* Non potete visualizzare in anteprima un&#39;esperienza con stato Bozza.
* I rapporti non vengono influenzati dalla visualizzazione degli URL di anteprima dell&#39;esperienza.

**Risoluzione dei problemi relativi agli URL di Experience Preview**

* Se non puoi visualizzare l’anteprima nella nuova scheda (a causa della cache del browser), prova ad aggiornare due o tre volte oppure copia il collegamento e aprilo in un nuovo browser, una nuova sessione o in modalità browser privato.
