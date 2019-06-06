---
description: È possibile configurare un’attività in Target Standard/Premium per utilizzare Adobe Analytics come origine per la generazione di rapporti (A4T).
keywords: a4T;A4T;Analytics come fonte di origine per i rapporti per Target
seo-description: È possibile configurare un’attività in Target Standard/Premium per utilizzare Adobe Analytics come origine per la generazione di rapporti (A4T).
seo-title: Creazione di attività
solution: Target
title: Creazione di attività
topic: Advanced,Standard,Classic
uuid: b04ad535-62fb-4dd3-ab3f-23da60fbffbd
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Creazione di attività{#activity-creation}

È possibile configurare un’attività in Target Standard/Premium per utilizzare Adobe Analytics come origine per la generazione di rapporti (A4T).

Prima di impostare un’attività che utilizza Analytics come origine per la generazione di rapporti, stabilisci l’obiettivo dell’attività, ad esempio il miglioramento dei ricavi per visitatore (RPV) o l’aumento dei clic sul carrello acquisti. Scegli una metrica di successo finale per l’attività. Anche se in Analytics puoi selezionare metriche aggiuntive in qualsiasi momento, è comunque necessario indicare una metrica specifica che si prevede verrà interessata dal test.

La creazione di un&#39;attività di Target Standard che utilizza Analytics come origine di reporting è simile alla configurazione di una normale attività di Target Standard, ma con alcune importanti differenze. Ad esempio, non puoi selezionare un segmento per il reporting durante la creazione dell&#39;attività, perché tutti i segmenti disponibili in Analytics possono essere applicati quando si visualizza un rapporto.

1. Fai clic su **[!UICONTROL Crea attività]**.

   >[!NOTE]
   >
   >Un nome di attività non può includere il carattere “%”, se Analytics si utilizza come origine per i rapporti.

1. Seleziona il tipo di attività e inizia a impostarla.
1. Una volta nella sezione **[!UICONTROL Impostazioni]** del flusso di creazione dell’attività, scegli **[!UICONTROL Adobe Analytics]** e specifica la società.
1. Seleziona una suite di rapporti.

   Puoi scegliere qualsiasi suite di rapporti disponibile in Adobe Analytics. La suite di rapporti definisce dove trovare i dati raccolti disponibili. Le suite di rapporti virtuali non sono incluse nell&#39;elenco suite di rapporti.

   Possono verificarsi due eventuali errori durante la selezione della suite di rapporti:

   * Un errore che segnala che nessuna suite di rapporti è disponibile, ma l&#39;account è impostato correttamente.
   Potrebbe essere necessario controllare la società Analytics. Se l&#39;account Experience Cloud è legato a più di una società Analytics, esci da Target e accedi ad Analytics con la società giusta. Quindi, una volta tornati a Target, le suite di rapporti verranno caricate.

   * Non è possibile visualizzare la suite di rapporti attesa.
   Puoi selezionare solo le suite di rapporti impostate per la connessione ad Adobe Target. Se non visualizzi la suite di rapporti desiderata, disconnettiti, accedi di nuovo ad Adobe Experience Cloud e riprova.

   Se le suite di rapporti non sono ancora presenti nell’elenco, [contatta l’assistenza clienti](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).
1. Specifica il server di tracciamento.

   Consulta [Utilizzo di un server di tracciamento di Analytics](../../c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

   >[!NOTE]
   >
   >Se utilizzi Adobe Analytics come origine per la generazione di rapporti dell’attività e la versione 61 (o successiva) di mbox.js o la versione 0.9.1 (o successiva) di at.js, non è necessario specificare un server di tracciamento durante la creazione di attività. La libreria mbox.js o at.js invia automaticamente i valori del server di tracciamento a [!DNL Target]. Durante la creazione di attività, puoi lasciare vuoto il campo [!UICONTROL Server di tracciamento] nella pagina [!UICONTROL Obiettivi e impostazioni].

1. Definisci l&#39;esperienza.
1. Specifica l&#39;obiettivo dell&#39;attività.

   È necessario selezionare una metrica di successo da utilizzare come obiettivo per ogni test. L&#39;obiettivo è l&#39;attività di conversione che indica un&#39;attività di successo. È buona norma non eseguire mai un test senza un obiettivo da migliorare in modo specifico. È possibile scegliere qualsiasi metrica di Analytics disponibile nel selettore delle metriche di Analytics.

   >[!NOTE]
   >
   >È possibile inviare una metrica personalizzata basata su Target ad Analytics, invece di fare affidamento unicamente sui dati di Analytics. Ad esempio, è possibile monitorare i clic su una pagina, elemento solitamente non controllato da Analytics. Questa metrica personalizzata viene inviata automaticamente ad Analytics dal server di Target e viene visualizzata come metrica “Conversione Target”, nel selettore delle metriche in Analytics. Tale metrica è vuota se si sceglie di utilizzare le metriche di Analytics.

   L&#39;impostazione di un obiettivo non impedisce di utilizzare un&#39;altra metrica per valutare i risultati dei test. L&#39;obiettivo, tuttavia, funge da promemoria rispetto all&#39;elemento da migliorare con l&#39;attività.

   Il visitatore resta nell&#39;attività dopo aver raggiunto l&#39;obiettivo. Il visitatore continua a visualizzare il contenuto dell&#39;attività ma non viene conteggiato come nuovo accesso all&#39;attività.

   >[!NOTE]
   >
   >Durante l’impostazione di un’attività dopo aver impostato Analytics come origine per la generazione di rapporti, non è possibile impostare tipi di pubblico per la generazione dei rapporti. I segmenti di Analytics sono disponibili nel rapporto Attività di Target.

1. Fai clic su **[!UICONTROL Salva]**.

