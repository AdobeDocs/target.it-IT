---
keywords: a4t;A4T;Analytics as the reporting source for Target
description: È possibile configurare un’attività in Target Standard/Premium per utilizzare Adobe Analytics come origine per la generazione di rapporti (A4T).
title: Creare un'attività che utilizza A4T come origine di reporting
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 95e2ed4d9ca22e18b91533365624bcc001d09c34
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 43%

---


# Creare un&#39;attività che utilizza Analytics come origine di reporting

Potete configurare un&#39;attività in [!DNL Target] per utilizzare [!DNL Adobe Analytics] come origine di reporting (A4T).

Prima di impostare un&#39;attività che utilizza [!DNL Analytics] come origine di reporting, stabilire l&#39;obiettivo per l&#39;attività, ad esempio migliorare le entrate per visitatore (RPV) o aumentare i clic sul carrello. Scegli una metrica di successo finale per l’attività. Sebbene sia possibile selezionare metriche aggiuntive in qualsiasi momento in [!DNL Analytics], è comunque necessario specificare una metrica specifica che si prevede verrà interessata dal test.

## Crea l&#39;attività

La creazione di un&#39;attività [!DNL Target] che utilizza [!DNL Analytics] come origine di reporting è simile alla configurazione di un&#39;attività [!DNL Target] regolare, con alcune importanti differenze. Ad esempio, non è possibile selezionare un segmento per il reporting durante la creazione dell&#39;attività, perché tutti i segmenti disponibili in [!DNL Analytics] possono essere applicati quando si visualizza un rapporto.

1. Fai clic su **[!UICONTROL Crea attività]**.

   >[!NOTE]
   >
   >Un nome di attività non può includere il carattere &quot;%&quot; se [!DNL Analytics] viene utilizzato come origine di reporting.

1. Seleziona il tipo di attività e inizia a impostarla.

   Per creare un&#39;attività [!UICONTROL Auto-Allocate] o [!UICONTROL Auto-Target], consultate [A4T support for Auto-Allocate and Auto-Target activity](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md) per ulteriori informazioni.

1. Una volta nella sezione **[!UICONTROL Impostazioni]** del flusso di creazione dell’attività, scegli **[!UICONTROL Adobe Analytics]** e specifica la società.
1. Seleziona una suite di rapporti.

   Puoi scegliere qualsiasi suite di rapporti disponibile in [!DNL Analytics]. La suite di rapporti definisce dove trovare i dati raccolti disponibili. Le suite di rapporti virtuali non sono incluse nell&#39;elenco suite di rapporti.

   Possono verificarsi due eventuali errori durante la selezione della suite di rapporti:

   * Un errore che segnala che nessuna suite di rapporti è disponibile, ma l&#39;account è impostato correttamente.

      Potrebbe essere necessario controllare la società [!DNL Analytics]. Se l&#39;account [!DNL Adobe Experience Cloud] è associato a più società [!DNL Analytics], disconnettetevi da [!DNL Target] ed effettuate l&#39;accesso a [!DNL Analytics] nella società giusta. Quindi tornate a [!DNL Target] e le suite di rapporti verranno caricate.

   * Non è possibile visualizzare la suite di rapporti attesa.

      Solo le suite di rapporti per le quali è stato eseguito il provisioning per la connessione a [!DNL Target] saranno disponibili per la selezione. Se non visualizzi le suite di rapporti previste, prova prima a disconnettersi ed eseguire nuovamente il login a [!DNL Adobe Experience Cloud] per riprovare.
   Se le suite di rapporti non sono ancora presenti nell’elenco, [contatta l’assistenza clienti](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. Specifica il server di tracciamento.

   Consulta [Utilizzo di un server di tracciamento di Analytics](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

1. Definite l&#39;esperienza.
1. Specifica l&#39;obiettivo dell&#39;attività.

   È necessario selezionare una metrica di successo da utilizzare come obiettivo per ogni attività. L&#39;obiettivo è l&#39;attività di conversione che indica un&#39;attività di successo. È buona norma non eseguire mai un test senza un obiettivo da migliorare in modo specifico. Potete scegliere qualsiasi metrica [!DNL Analytics] disponibile nel selettore delle metriche [!DNL Analytics].

   >[!NOTE]
   >
   >Puoi inviare una metrica personalizzata basata su Target a [!DNL Analytics] anziché affidarti solo ai dati [!DNL Analytics]. Ad esempio, è possibile monitorare i clic su una pagina, elemento solitamente non controllato da [!DNL Analytics]. Questa metrica personalizzata viene inviata automaticamente a [!DNL Analytics] dal server [!DNL Target] e viene visualizzata come metrica &quot;[!DNL Target] Conversion&quot; nel selettore delle metriche in [!DNL Analytics]. La metrica di conversione [!DNL Target] è vuota se si sceglie di utilizzare le metriche [!DNL Analytics].

   L&#39;impostazione di un obiettivo non impedisce di utilizzare un&#39;altra metrica per valutare i risultati dei test. L&#39;obiettivo, tuttavia, funge da promemoria rispetto all&#39;elemento da migliorare con l&#39;attività.

   Il visitatore resta nell&#39;attività dopo aver raggiunto l&#39;obiettivo. Il visitatore continua a visualizzare il contenuto dell&#39;attività ma non viene conteggiato come nuovo accesso all&#39;attività.

   >[!NOTE]
   >
   >Quando si configura un&#39;attività dopo aver configurato [!DNL Analytics] come origine di reporting, non è disponibile alcuna opzione per impostare audience per il reporting. [!DNL Analytics] i segmenti sono disponibili nel rapporto  [!DNL Target] Attività.

1. Fai clic su **[!UICONTROL Salva]**.

