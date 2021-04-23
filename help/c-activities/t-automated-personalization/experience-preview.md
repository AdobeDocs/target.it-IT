---
keywords: Anteprima esperienza;URL esperienza;generare URL;visualizzare gli URL esperienza
description: Scopri come utilizzare gli URL di anteprima dell’esperienza per Adobe [!DNL Target] attività Automated Personalization per visualizzare il contenuto dell’esperienza direttamente sul sito prima che l’attività sia attiva.
title: Come posso utilizzare gli URL di anteprima esperienza nelle attività di Automated Personalization?
feature: Personalizzazione automatizzata
exl-id: 9f329b8a-5f86-4cae-a3be-eed24fa0a9cd
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 65%

---

# ![](/help/assets/premium.png) PREMIUMPrassegna le attività Automated Personalization con URL di anteprima esperienza

Gli URL di anteprima dell’esperienza possono essere generati per le attività di Target Automated Personalization per visualizzare il contenuto dell’esperienza direttamente sul sito prima che l’attività sia attiva a scopo di anteprima e controllo qualità. Gli URL di anteprima dell’esperienza ignorano il targeting per forzare la visualizzazione di una particolare esperienza.

>[!NOTE]
>
>Gli URL di anteprima delle esperienze per Automated Personalization sono diversi dalla modalità di controllo qualità delle attività. La modalità di controllo qualità delle attività consente di creare URL per altri tipi di attività. Per ulteriori informazioni, consulta [Controllo qualità delle attività](/help/c-activities/c-activity-qa/activity-qa.md).
>
>Gli URL di anteprima delle esperienze per le attività di Personalizzazione automatizzata sono disponibili solo quando si utilizza at.js 1.x. Gli URL di anteprima delle esperienze per le attività di Personalizzazione automatizzata non sono attualmente supportati per at.js 2.x.

Utilizza gli URL di anteprima dell’esperienza per condividere esperienze con i membri del team e per eseguire il controllo qualità tra browser e ambienti, senza creare un’attività di controllo qualità separata. Questa funzione è particolarmente utile in caso di siti complessi o se le policy di sicurezza non consentono la visualizzazione del sito in un simulatore.

1. Crea un’[attività di personalizzazione automatizzata](/help/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9) oppure fai clic sull’attività per aprirla.

   L&#39;attività non deve essere live per visualizzare un&#39;anteprima dell&#39;esperienza.
1. Nella pagina di riepilogo attività, fai clic sui tre punti verticali, quindi scegli **[!UICONTROL Visualizza gli URL di esperienza]**.
1. Rivedi e/o definisci gli URL.

   * Se utilizzi il Compositore esperienza visivo, l&#39;URL predefinito specificato per l&#39;attività viene immesso automaticamente e viene generato un collegamento per ogni esperienza nell&#39;attività. Se lo desideri, puoi modificare questo URL e aggiungerne altri.
   * Se utilizzi il Compositore esperienza basato su moduli, non viene immesso automaticamente alcun URL predefinito. Se non hai creato gli URL di anteprima dell&#39;esperienza, fai clic su **Aggiungi nuovo URL**. Devi specificare tutti gli URL che desideri visualizzare in anteprima e un nome per ognuno.

   Puoi aggiungere più URL, tale opzione è utile quando esegui un test a più pagine o un test modello e desideri visualizzare in anteprima l&#39;attività su più di una pagina.

   Tramite una finestra modale, puoi visualizzare i collegamenti alle esperienze sul tuo sito per ottenere una “anteprima fedele” al di fuori del Compositore esperienza visivo. Per condividere l’anteprima, è necessario condividere i collegamenti dal messaggio. Non è possibile fare clic su un collegamento e poi copiare l&#39;URL risultante direttamente dalla pagina, perché l&#39;URL contiene un parametro che visualizza la pagina correttamente solo quando si accede alla pagina dal collegamento nel messaggio. Invece, copia il testo nella finestra modale e invialo all&#39;intero team.
1. Fai clic su **[!UICONTROL Genera tutto]** e poi su ogni esperienza per visualizzarne l’anteprima.

   Se apporti modifiche all’esperienza, assicurati di generare nuovi collegamenti di anteprima per il team tornando alla finestra modale e facendo clic su **Rinnova collegamenti** per ottenere nuovi collegamenti.

   **Nota:** i collegamenti di anteprima si aprono in nuove schede e richiedono che nel browser venga disattivato il blocco dei popup.

1. Fai clic su ogni nome di esperienza per visualizzare l’anteprima dell’attività.

   L’attività viene visualizzata nella pagina.
1. Fai clic su **[!UICONTROL Fine]** per tornare al riepilogo delle attività.

## Considerazioni {#example_9F2B333BC63143FF99AE331F57E8BA4C}

**Generazione degli URL di anteprima delle esperienze**

* L’URL di anteprima dell’esperienza non è interessato dalla suddivisione del traffico tra le esperienze.
* Il targeting a livello di pubblico non influisce sull’anteprima.
* Puoi generare automaticamente un massimo di 300 URL di esperienza per ogni attività. Dopo di che, dovrai generare gli URL manualmente.
* Puoi generare automaticamente un massimo di 300 URL di esperienza per ogni attività. Dopo di che, dovrai generare gli URL manualmente.
* A seconda del numero di esperienze, la generazione degli URL può richiedere fino a cinque minuti. Non chiudere la finestra di dialogo, altrimenti gli URL generati verranno persi.
* I collegamenti di anteprima generati sono validi per due mesi. Al termine di questo periodo, dovrai generarli di nuovo.
* Devi generare di nuovo URL ogni volta che un’esperienza viene cambiata.

**Condivisione degli URL di anteprima delle esperienze**

* Puoi visualizzare in anteprima un esperienza anche se non fai parte del pubblico di destinazione.
* Puoi condividere gli URL di anteprima dell’esperienza con i colleghi che non hanno accesso ad Adobe Target.

**Visualizzazione delle esperienze con gli URL di anteprima delle esperienze**

* L’anteprima funziona per qualsiasi attività salvata, purché la pagina non venga modificata.
* L’URL di anteprima dell’esperienza è disponibile sia se l’attività è attiva che inattiva.
* Non puoi visualizzare in anteprima un’esperienza in stato Bozza.
* La visualizzazione degli URL di anteprima dell’esperienza non influisce sul reporting.

**Risoluzione dei problemi relativi agli URL di anteprima delle esperienze**

* Se non puoi visualizzare l’anteprima nella nuova scheda (a causa della cache del browser), prova ad aggiornare due o tre volte oppure copia il collegamento e aprilo in un nuovo browser, una nuova sessione o in modalità browser privato.
