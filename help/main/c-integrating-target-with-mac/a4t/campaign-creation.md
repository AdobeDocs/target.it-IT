---
keywords: a4T;A4T;Analytics come fonte di origine per i rapporti per Target
description: Scopri come configurare un’attività in Adobe [!DNL Target] che utilizza Adobe Analytics come origine di reporting (A4T).
title: Come si crea un’attività che utilizza A4T?
feature: Analytics for Target (A4T)
exl-id: 6a09764a-8bf1-4f69-b871-fb23136f933e
source-git-commit: 981cff428d9e8849b9bbcbf7bef389dad0fbb32a
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 30%

---

# Creare un’attività che utilizza Analytics come sorgente per la generazione di rapporti

Puoi configurare un’attività in [!DNL Adobe Target] da utilizzare [!DNL Adobe Analytics] come origine per la generazione di rapporti (A4T)

Prima di impostare un’attività che utilizza [!DNL Analytics] come origine per la generazione di rapporti, stabilisci l’obiettivo dell’attività, ad esempio il miglioramento dei ricavi per visitatore (RPV) o l’aumento dei clic sul carrello. Scegli una metrica di successo finale per l’attività. Anche se è possibile selezionare più metriche in qualsiasi momento in [!DNL Analytics], è comunque necessario specificare una particolare metrica su cui si prevede che il test abbia effetto.

## Creare l’attività

Creazione di un [!DNL Target] attività che utilizza [!DNL Analytics] poiché l’origine per la generazione di rapporti è simile alla configurazione di un’ [!DNL Target] con alcune importanti differenze. Ad esempio, non è possibile selezionare un segmento per il reporting durante la creazione dell’attività, perché tutti i segmenti disponibili in [!DNL Analytics] possono essere applicate quando si visualizza un rapporto.

1. Fai clic su **[!UICONTROL Crea attività]**.

   >[!NOTE]
   >
   >Un nome di attività non può includere il carattere &quot;%&quot; se [!DNL Analytics] viene utilizzato come origine per la generazione di rapporti.
   >
   >Non utilizzare lo stesso nome attività per due attività di [workspace](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) che utilizzano reporting A4T.

1. Seleziona il tipo di attività e inizia a impostarla.

   Se desideri creare un’ [!UICONTROL Allocazione automatica] o [!UICONTROL Targeting automatico] attività, vedi [Supporto A4T per attività di allocazione automatica e targeting automatico](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md) per ulteriori informazioni.

1. Quando si arriva al **[!UICONTROL Impostazioni]** parte del flusso di creazione dell’attività, seleziona **[!UICONTROL Adobe Analytics]** e specifica la tua azienda.
1. Seleziona una suite di rapporti.

   Puoi scegliere qualsiasi suite di rapporti disponibile in [!DNL Analytics]. La suite di rapporti definisce dove sono disponibili i dati raccolti. Le suite di rapporti virtuali non sono incluse nell&#39;elenco suite di rapporti.

   Possono verificarsi due eventuali errori durante la selezione della suite di rapporti:

   * Un errore che segnala che nessuna suite di rapporti è disponibile, ma l&#39;account è impostato correttamente.

     Controlla il tuo [!DNL Analytics] società. Se il [!DNL Adobe Experience Cloud] l&#39;account è associato a più account [!DNL Analytics] azienda, disconnetti da [!DNL Target], e accedi a [!DNL Analytics] sotto la giusta compagnia. Quindi torna a [!DNL Target]e le suite di rapporti vengono caricate.

   * Non è possibile visualizzare la suite di rapporti attesa.

     Solo le suite di rapporti per le quali è stato eseguito il provisioning [!DNL Target] sono disponibili per la selezione. Se non trovi le suite di rapporti previste, disconnettiti e accedi di nuovo al [!DNL Adobe Experience Cloud] per riprovare.

   Se una o più suite di rapporti non sono ancora presenti nell’elenco, [contatta l’Assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. Specifica il server di tracciamento.

   Consulta [Utilizzo di un server di tracciamento di Analytics](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

1. Definisci l’esperienza.
1. Specifica l’obiettivo dell’attività.

   È necessario selezionare una metrica di successo da utilizzare come obiettivo per ogni attività. L&#39;obiettivo è l&#39;attività di conversione che indica un&#39;attività di successo. È buona norma non eseguire mai un test senza un obiettivo da migliorare in modo specifico. Puoi scegliere qualsiasi [!DNL Analytics] metrica disponibile nella [!DNL Analytics] selettore delle metriche.

   >[!NOTE]
   >
   >Puoi inviare una metrica personalizzata basata su Target a [!DNL Analytics] anziché affidarsi solo a [!DNL Analytics] dati. Ad esempio, puoi monitorare il clic su una pagina, che in genere non viene tracciata da [!DNL Analytics]. Questa metrica personalizzata viene inviata a [!DNL Analytics] automaticamente dal [!DNL Target] e viene visualizzato come &quot;&quot;[!DNL Target] Conversione&quot; nel selettore delle metriche in [!DNL Analytics]. Il [!DNL Target] La metrica di conversione è vuota se scegli di utilizzare [!DNL Analytics] metriche.

   L&#39;impostazione di un obiettivo non impedisce di utilizzare un&#39;altra metrica per valutare i risultati dei test. L&#39;obiettivo, tuttavia, funge da promemoria rispetto all&#39;elemento da migliorare con l&#39;attività.

   Il visitatore resta nell&#39;attività dopo aver raggiunto l&#39;obiettivo. Il visitatore continua a visualizzare il contenuto dell&#39;attività ma non viene conteggiato come nuovo accesso all&#39;attività.

   >[!NOTE]
   >
   >Durante la configurazione di un’attività dopo la configurazione di [!DNL Analytics] come origine per la generazione di rapporti, non è possibile impostare tipi di pubblico per la generazione dei rapporti. [!DNL Analytics] i segmenti sono disponibili nel [!DNL Target] Rapporto sulle attività.

1. Fai clic su **[!UICONTROL Salva]**.

## Attività A4T e di allocazione automatica e targeting automatico

Per ulteriori informazioni, consulta [Supporto A4T per attività di allocazione automatica e targeting automatico](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).
