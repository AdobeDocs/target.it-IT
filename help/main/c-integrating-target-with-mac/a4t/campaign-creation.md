---
keywords: a4T;A4T;Analytics come fonte di origine per i rapporti per Target
description: Scopri come configurare un’attività in Adobe [!DNL Target] che utilizza Adobe Analytics come origine per la generazione di rapporti (A4T).
title: Come si crea un’attività che utilizza A4T?
feature: Analytics for Target (A4T)
exl-id: 6a09764a-8bf1-4f69-b871-fb23136f933e
source-git-commit: 981cff428d9e8849b9bbcbf7bef389dad0fbb32a
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 29%

---

# Creare un’attività che utilizza Analytics come sorgente per la generazione di rapporti

È possibile configurare un&#39;attività in [!DNL Adobe Target] per utilizzare [!DNL Adobe Analytics] come origine per la generazione di rapporti (A4T).

Prima di impostare un&#39;attività che utilizza [!DNL Analytics] come origine per la generazione di rapporti, stabilisci l&#39;obiettivo dell&#39;attività, ad esempio il miglioramento dei ricavi per visitatore (RPV) o l&#39;aumento dei clic sul carrello. Scegli una metrica di successo finale per l’attività. Sebbene sia possibile selezionare più metriche in qualsiasi momento in [!DNL Analytics], è necessario specificare una particolare metrica che si prevede verrà influenzata dal test.

## Creare l’attività

La creazione di un&#39;attività [!DNL Target] che utilizza [!DNL Analytics] come origine per la generazione di rapporti è simile alla configurazione di un&#39;attività [!DNL Target] regolare, con alcune importanti differenze. Ad esempio, non è possibile selezionare un segmento per il reporting durante la creazione dell&#39;attività perché tutti i segmenti disponibili in [!DNL Analytics] possono essere applicati durante la visualizzazione di un report.

1. Fare clic su **[!UICONTROL Create Activity]**.

   >[!NOTE]
   >
   >Un nome di attività non può includere il carattere &quot;%&quot; se [!DNL Analytics] viene utilizzato come origine per la generazione di rapporti.
   >
   >Non utilizzare lo stesso nome attività per due attività di [aree di lavoro](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) separate che utilizzano la generazione di rapporti A4T.

1. Seleziona il tipo di attività e inizia a impostarla.

   Se desideri creare un&#39;attività [!UICONTROL Auto-Allocate] o [!UICONTROL Auto-Target], consulta [Supporto A4T per attività di allocazione automatica e targeting automatico](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md) per ulteriori informazioni.

1. Una volta raggiunta la parte **[!UICONTROL Settings]** del flusso di creazione dell&#39;attività, scegli **[!UICONTROL Adobe Analytics]** e specifica la tua società.
1. Seleziona una suite di rapporti.

   Puoi scegliere qualsiasi suite di rapporti disponibile in [!DNL Analytics]. La suite di rapporti definisce dove sono disponibili i dati raccolti. Le suite di rapporti virtuali non sono incluse nell&#39;elenco suite di rapporti.

   Possono verificarsi due eventuali errori durante la selezione della suite di rapporti:

   * Un errore che segnala che nessuna suite di rapporti è disponibile, ma l&#39;account è impostato correttamente.

     Controlla la tua società [!DNL Analytics]. Se l&#39;account [!DNL Adobe Experience Cloud] è associato a più società [!DNL Analytics], disconnettersi da [!DNL Target] e accedere a [!DNL Analytics] nella società corretta. Quindi torna a [!DNL Target] e le suite di rapporti vengono caricate.

   * Non è possibile visualizzare la suite di rapporti attesa.

     È possibile selezionare solo le suite di rapporti predisposte per la connessione a [!DNL Target]. Se le suite di rapporti previste non sono visualizzate, disconnettersi e accedere di nuovo a [!DNL Adobe Experience Cloud] per riprovare.

   Se una o più suite di rapporti non sono ancora presenti nell&#39;elenco, [contatta l&#39;Assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. Specifica il server di tracciamento.

   Consulta [Utilizzo di un server di tracciamento di Analytics](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

1. Definisci l’esperienza.
1. Specifica l’obiettivo dell’attività.

   È necessario selezionare una metrica di successo da utilizzare come obiettivo per ogni attività. L&#39;obiettivo è l&#39;attività di conversione che indica un&#39;attività di successo. È buona norma non eseguire mai un test senza un obiettivo da migliorare in modo specifico. Puoi scegliere qualsiasi metrica [!DNL Analytics] disponibile nel selettore delle metriche [!DNL Analytics].

   >[!NOTE]
   >
   >È possibile inviare una metrica personalizzata basata su Target a [!DNL Analytics] anziché basarsi solo sui dati di [!DNL Analytics]. Ad esempio, è possibile monitorare il clic su una pagina, che in genere non viene tracciata da [!DNL Analytics]. Questa metrica personalizzata viene inviata automaticamente a [!DNL Analytics] dal server [!DNL Target] e viene visualizzata come metrica &quot;[!DNL Target] Conversion&quot; nel selettore delle metriche in [!DNL Analytics]. La metrica di conversione [!DNL Target] è vuota se si sceglie di utilizzare [!DNL Analytics] metriche.

   L&#39;impostazione di un obiettivo non impedisce di utilizzare un&#39;altra metrica per valutare i risultati dei test. L&#39;obiettivo, tuttavia, funge da promemoria rispetto all&#39;elemento da migliorare con l&#39;attività.

   Il visitatore resta nell&#39;attività dopo aver raggiunto l&#39;obiettivo. Il visitatore continua a visualizzare il contenuto dell&#39;attività ma non viene conteggiato come nuovo accesso all&#39;attività.

   >[!NOTE]
   >
   >Durante l&#39;impostazione di un&#39;attività dopo aver impostato [!DNL Analytics] come origine per la generazione di rapporti, non è possibile impostare tipi di pubblico per la generazione dei rapporti. [!DNL Analytics] segmenti sono disponibili nel rapporto Attività [!DNL Target].

1. Fare clic su **[!UICONTROL Save]**.

## Attività A4T e di allocazione automatica e targeting automatico

Per ulteriori informazioni, consulta [Supporto A4T per attività di allocazione automatica e targeting automatico](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).
