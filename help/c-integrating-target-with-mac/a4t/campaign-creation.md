---
keywords: a4T;A4T;Analytics come fonte di origine per i rapporti per Target
description: Scopri come configurare un’attività in Adobe [!DNL Target] che utilizza Adobe Analytics come origine per la generazione di rapporti (A4T).
title: Come si crea un’attività che utilizza A4T?
feature: Analytics for Target (A4T)
exl-id: 6a09764a-8bf1-4f69-b871-fb23136f933e
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 35%

---

# Creare un’attività che utilizza Analytics come origine per la generazione di rapporti

Puoi configurare un’attività in [!DNL Adobe Target] per utilizzare [!DNL Adobe Analytics] come origine per la generazione di rapporti (A4T).

Prima di impostare un’attività che utilizza [!DNL Analytics] come origine per la generazione di rapporti, stabilisci l’obiettivo dell’attività, ad esempio il miglioramento dei ricavi per visitatore (RPV) o l’aumento dei clic sul carrello acquisti. Scegli una metrica di successo finale per l’attività. Anche se è possibile selezionare più metriche in qualsiasi momento in [!DNL Analytics], è comunque necessario specificare una metrica particolare che si prevede verrà interessata dal test.

## Crea l&#39;attività

La creazione di un’attività [!DNL Target] che utilizza [!DNL Analytics] come origine per la generazione di rapporti è simile alla configurazione di una normale attività [!DNL Target], con alcune importanti differenze. Ad esempio, non è possibile selezionare un segmento per il reporting durante la creazione dell’attività, perché tutti i segmenti disponibili in [!DNL Analytics] possono essere applicati durante la visualizzazione di un rapporto.

1. Fai clic su **[!UICONTROL Crea attività]**.

   >[!NOTE]
   >
   >Un nome di attività non può includere il carattere &quot;%&quot; se [!DNL Analytics] è utilizzato come origine per la generazione di rapporti.

1. Seleziona il tipo di attività e inizia a impostarla.

   Per ulteriori informazioni, se desideri creare un&#39;attività [!UICONTROL Allocazione automatica] o [!UICONTROL Targeting automatico], consulta [Supporto A4T per le attività di Allocazione automatica e Targeting automatico](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md) .

1. Una volta nella sezione **[!UICONTROL Impostazioni]** del flusso di creazione dell’attività, scegli **[!UICONTROL Adobe Analytics]** e specifica la società.
1. Seleziona una suite di rapporti.

   Puoi scegliere qualsiasi suite di rapporti disponibile in [!DNL Analytics]. La suite di rapporti definisce dove sono disponibili i dati raccolti. Le suite di rapporti virtuali non sono incluse nell&#39;elenco suite di rapporti.

   Possono verificarsi due eventuali errori durante la selezione della suite di rapporti:

   * Un errore che segnala che nessuna suite di rapporti è disponibile, ma l&#39;account è impostato correttamente.

      Controlla la tua [!DNL Analytics] azienda. Se il tuo account [!DNL Adobe Experience Cloud] è associato a più di una [!DNL Analytics] azienda, esci da [!DNL Target] e accedi a [!DNL Analytics] nella società giusta. Quindi torna a [!DNL Target] e le suite di rapporti vengono caricate.

   * Non è possibile visualizzare la suite di rapporti attesa.

      Puoi selezionare solo le suite di rapporti per le quali è stato eseguito il provisioning per la connessione a [!DNL Target]. Se non trovi le suite di rapporti previste, disconnettiti e accedi nuovamente a [!DNL Adobe Experience Cloud] per riprovare.
   Se nell&#39;elenco mancano ancora una o più suite di rapporti, [contatta l&#39;Assistenza clienti](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. Specifica il server di tracciamento.

   Consulta [Utilizzo di un server di tracciamento di Analytics](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

1. Definisci l’esperienza.
1. Specifica l&#39;obiettivo dell&#39;attività.

   È necessario selezionare una metrica di successo da utilizzare come obiettivo per ogni attività. L&#39;obiettivo è l&#39;attività di conversione che indica un&#39;attività di successo. È buona norma non eseguire mai un test senza un obiettivo da migliorare in modo specifico. Puoi scegliere qualsiasi metrica [!DNL Analytics] disponibile nel selettore di metriche [!DNL Analytics].

   >[!NOTE]
   >
   >Puoi inviare una metrica personalizzata basata su Target a [!DNL Analytics] anziché affidarti solo ai dati [!DNL Analytics]. Ad esempio, puoi monitorare i clic su una pagina, che in genere non viene tracciata da [!DNL Analytics]. Questa metrica personalizzata viene inviata automaticamente a [!DNL Analytics] dal server [!DNL Target] e viene visualizzata come metrica &quot;[!DNL Target] Conversion&quot; nel selettore delle metriche in [!DNL Analytics]. La metrica [!DNL Target] Conversione è vuota se scegli di utilizzare le metriche [!DNL Analytics].

   L&#39;impostazione di un obiettivo non impedisce di utilizzare un&#39;altra metrica per valutare i risultati dei test. L&#39;obiettivo, tuttavia, funge da promemoria rispetto all&#39;elemento da migliorare con l&#39;attività.

   Il visitatore resta nell&#39;attività dopo aver raggiunto l&#39;obiettivo. Il visitatore continua a visualizzare il contenuto dell&#39;attività ma non viene conteggiato come nuovo accesso all&#39;attività.

   >[!NOTE]
   >
   >Quando si configura un’attività dopo aver impostato [!DNL Analytics] come origine per la generazione di rapporti, non è possibile impostare tipi di pubblico per la generazione di rapporti. [!DNL Analytics] i segmenti sono disponibili nel rapporto  [!DNL Target] Attività .

1. Fai clic su **[!UICONTROL Salva]**.

## Attività A4T e di allocazione automatica e targeting automatico

Per ulteriori informazioni, consulta [Supporto A4T per attività di allocazione automatica e targeting automatico](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md).
