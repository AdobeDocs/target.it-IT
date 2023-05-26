---
keywords: Anteprima esperienza;URL esperienza;generare URL;visualizzare gli URL esperienza
description: Scopri come utilizzare gli URL di anteprima dell’esperienza, ad Adobe [!DNL Target] Attività di Automated Personalization per visualizzare il contenuto dell’esperienza direttamente sul sito prima che l’attività sia live.
title: Come posso utilizzare gli URL di anteprima dell’esperienza nelle attività di Automated Personalization?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
exl-id: 9f329b8a-5f86-4cae-a3be-eed24fa0a9cd
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 51%

---

# Anteprima delle attività Automated Personalization con URL di anteprima dell’esperienza

Gli URL di anteprima dell’esperienza possono essere generati per [!DNL Target] [!UICONTROL Automated Personalization] attività per visualizzare il contenuto dell’esperienza direttamente sul sito prima che l’attività venga pubblicata, per scopi di anteprima e controllo qualità. Gli URL di anteprima esperienza ignorano il targeting per forzare la visualizzazione di una particolare esperienza.

>[!NOTE]
>
>Puoi creare URL di anteprima esperienza per altri tipi di [!DNL Target] attività. Tuttavia, il processo è leggermente diverso. Per ulteriori informazioni, consulta [Controllo qualità delle attività](/help/main/c-activities/c-activity-qa/activity-qa.md#preview).

Utilizza gli URL di anteprima dell’esperienza per condividere le esperienze con i membri del gruppo e per eseguire il controllo qualità delle esperienze tra browser e ambienti diversi, senza creare un’attività di controllo qualità separata. Questa funzione è particolarmente utile in caso di siti complessi o se le policy di sicurezza non consentono la visualizzazione del sito in un simulatore.

1. Crea un’[attività di personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9) oppure fai clic sull’attività per aprirla.

   L&#39;attività non deve essere live per visualizzare un&#39;anteprima dell&#39;esperienza.

1. Nella pagina Panoramica dell’attività, fai clic sui tre punti verticali e quindi su **[!UICONTROL Visualizza URL esperienza]**.

1. Rivedi e/o definisci gli URL.

   * Se utilizzi il [!UICONTROL Compositore esperienza visivo] (VEC), l’URL predefinito specificato per l’attività viene inserito automaticamente e viene generato un collegamento per ogni esperienza nell’attività. Se lo desideri, puoi modificare questo URL e aggiungerne altri.
   * Se utilizzi il [!UICONTROL Compositore esperienza basato su moduli], non viene immesso automaticamente alcun URL predefinito. Se non hai creato in precedenza gli URL di anteprima dell’esperienza, fai clic su **Aggiungi nuovo URL**. Devi specificare tutti gli URL che desideri visualizzare in anteprima e un nome per ognuno.

   Puoi aggiungere più URL, tale opzione è utile quando esegui un test a più pagine o un test modello e desideri visualizzare in anteprima l&#39;attività su più di una pagina.

   Una finestra modale mostra i collegamenti alle esperienze sul sito per ottenerne una &quot;anteprima fedele&quot; al di fuori di [!DNL Target] VEC Per condividere l’anteprima, è necessario condividere i collegamenti dal messaggio. Non è possibile fare clic su un collegamento e poi copiare l&#39;URL risultante direttamente dalla pagina, perché l&#39;URL contiene un parametro che visualizza la pagina correttamente solo quando si accede alla pagina dal collegamento nel messaggio. Invece, copia il testo nella finestra modale e invialo all&#39;intero team.

1. Fai clic su **[!UICONTROL Genera tutto]** e poi su ogni esperienza per visualizzarne l’anteprima.

   Se poi apporti modifiche all’esperienza, assicurati di generare nuovi collegamenti di anteprima per il team tornando alla finestra modale e facendo clic su **Rinnova collegamenti** per ottenere nuovi collegamenti.

   >[!NOTE]
   >
   >I collegamenti di anteprima si aprono in nuove schede e richiedono la disabilitazione del blocco dei popup nel browser.

1. Fai clic su ogni nome di esperienza per visualizzare l’anteprima dell’attività.

   L’attività viene visualizzata nella pagina.

1. Fai clic su **[!UICONTROL Fine]** per tornare al riepilogo delle attività.

## Considerazioni {#example_9F2B333BC63143FF99AE331F57E8BA4C}

**Generazione degli URL di anteprima dell’esperienza**

* L’URL di anteprima dell’esperienza non è interessato dalla divisione del traffico tra le esperienze.
* Il targeting a livello di pubblico non influisce sull’anteprima.
* Puoi generare automaticamente un massimo di 300 URL di esperienza per ogni attività. Dopo di che, dovrai generare gli URL manualmente.
* A seconda del numero di esperienze, la generazione degli URL può richiedere fino a cinque minuti. Non chiudere la finestra di dialogo altrimenti gli URL generati andranno persi.
* I collegamenti di anteprima generati sono validi per due mesi. Al termine di questo periodo, dovrai generarli di nuovo.
* Devi generare di nuovo URL ogni volta che un’esperienza viene cambiata.

**Condivisione degli URL di anteprima dell’esperienza**

* Puoi visualizzare in anteprima un esperienza anche se non fai parte del pubblico di destinazione.
* Puoi condividere gli URL di anteprima dell’esperienza con colleghi che non hanno accesso a [!DNL Adobe Target].

**Visualizzazione di esperienze con URL di anteprima esperienza**

* L’anteprima funziona per qualsiasi attività salvata, purché la pagina non venga modificata.
* L’URL di anteprima dell’esperienza è disponibile indipendentemente dal fatto che l’attività sia attiva o inattiva.
* Non puoi visualizzare in anteprima un’esperienza che si trova in [!UICONTROL Bozza] stato.
* La visualizzazione degli URL di anteprima dell’esperienza non influisce sul reporting.

**Risoluzione dei problemi degli URL di anteprima esperienza**

* Se non puoi visualizzare l’anteprima nella nuova scheda (a causa della cache del browser), prova ad aggiornare due o tre volte oppure copia il collegamento e aprilo in un nuovo browser, una nuova sessione o in modalità browser privato.
