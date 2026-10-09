---
keywords: Informazioni sulla funzione IA;Experimentation Accelerator;opportunità;panoramica attività
description: Scopri come utilizzare le informazioni generate dall’intelligenza artificiale e le opportunità di ottimizzazione da Experimentation Accelerator nella Panoramica delle attività di Adobe Target.
title: Informazioni sull’intelligenza artificiale nella panoramica dell’attività
feature: Activities
badge: label="Beta" type="Informative"
source-git-commit: 8d2b3af9942acbf30519c1f7b32fe79bed1f2eaa
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 36%
---
# Informazioni sull’intelligenza artificiale

>[!AVAILABILITY]
>
>La funzione Informazioni sull’intelligenza artificiale è attualmente disponibile come funzione beta.
></br>
>La sezione **[!UICONTROL Informazioni IA]** è disponibile solo per le attività **[!UICONTROL Test A/B]** con allocazione del traffico **[!UICONTROL Manuale]**.

Il menu **[!UICONTROL Informazioni IA]** nella **[!UICONTROL Panoramica attività]** fornisce accesso alle informazioni e alle opportunità di ottimizzazione. Utilizza questa scheda per rivedere gli insegnamenti dell’esperimento, confrontare i trattamenti e identificare le modifiche che potrebbero migliorare i tassi di conversione.

## Configurazione per gli insight e le opportunità basati sull’IA

>[!CONTEXTUALHELP]
>id="target_ai_insights"
>title="Insight"
>abstract="Gli insight sono risultati generati dall’IA che diventano disponibili quando l’esperimento raggiunge la significatività statistica."

>[!CONTEXTUALHELP]
>id="target_ai_insights_primary_metric"
>title="Metrica primaria"
>abstract="La metrica primaria viene estratta in automatico dalle impostazioni di reporting. Per apportarvi modifiche, cambia la metrica dell’obiettivo in Obiettivi e impostazioni."

>[!CONTEXTUALHELP]
>id="target_ai_insights_hypothesis"
>title="Ipotesi"
>abstract="L’ipotesi è un’istruzione da te definita che spiega il risultato atteso dell’esperimento. Includi una descrizione di cosa viene modificato e dove, quindi specifica la metrica che dovrebbe cambiare, e il tipo di cambiamento che ti aspetti."

>[!CONTEXTUALHELP]
>id="target_ai_insights_treatment_details"
>title="Dettagli dell’esperienza"
>abstract="I dettagli dell’esperienza mostrano immagini di come si presenta un’esperienza quando un utente si qualifica per questa. Puoi rivedere queste immagini per tutti gli esperimenti. Per alcuni esperimenti potrebbe essere necessario confermare l’immagine o sostituirla."

>[!CONTEXTUALHELP]
>id="target_ai_insights_primary_metric"
>title="Metrica primaria"
>abstract="La metrica primaria viene estratta in automatico dalle impostazioni di reporting. Per apportarvi modifiche, cambia la metrica dell’obiettivo in Obiettivi e impostazioni."

>[!CONTEXTUALHELP]
>id="target_ai_insights_hypothesis"
>title="Ipotesi"
>abstract="L’ipotesi è un’istruzione da te definita che spiega il risultato atteso dell’esperimento. Includi una descrizione di cosa viene modificato e dove, quindi specifica la metrica che dovrebbe cambiare, e il tipo di cambiamento che ti aspetti."

>[!CONTEXTUALHELP]
>id="target_ai_insights_opportunities"
>title="Opportunità"
>abstract="Le opportunità dagli esperimenti sono idee di trattamento suggerite dall’IA in base ai pattern che l’IA rileva nei risultati e nelle schermate dell’esperimento."

>[!CONTEXTUALHELP]
>id="target_ai_insights_treatment_details"
>title="Dettagli del trattamento"
>abstract="I dettagli del trattamento mostrano immagini di come si presenta un trattamento agli utenti qualificati. Puoi rivedere queste immagini per tutti gli esperimenti. Per alcuni esperimenti potrebbe essere necessario confermare l’immagine o sostituirla."

Prima di poter accedere alle opportunità e agli approfondimenti generati dall’intelligenza artificiale, devi innanzitutto impostare l’attività confermando la metrica principale, le ipotesi e le schermate dell’esperienza.

La metrica principale viene estratta automaticamente dalle impostazioni di reporting e dipende da come hai impostato Obiettivi e impostazioni. Devi creare l’ipotesi nel pannello Approfondimenti intelligenza artificiale. [Ulteriori informazioni](../c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md)

1. Apri l&#39;attività in [!DNL Adobe Target].

1. Seleziona il menu **[!UICONTROL Informazioni IA]** per aprire il pannello di configurazione.

1. Fai clic su ![](assets/do-not-localize/Smock_Edit_18_N.svg) per creare un&#39;ipotesi per l&#39;esperimento.

   ![](assets/ai-insights-7.png)

1. Digita nella tua ipotesi descrivendo le modifiche apportate e il modo in cui influiranno sulla metrica principale.

   Fai clic su **[!UICONTROL Salva]**.

1. In **[!UICONTROL Dettagli esperienza]**, fai clic su una scheda per aggiungere uno screenshot per le esperienze.

   >[!NOTE]
   >Alcune immagini potrebbero già essere acquisite automaticamente. In tal caso, confermare la schermata facendo clic su **[!UICONTROL Conferma]**.

   ![](assets/ai-insights-1.png)

1. Seleziona **[!UICONTROL Carica immagine]** per caricare uno screenshot preferito dai file locali per ogni esperienza.

   ![](assets/ai-insights-2.png)

1. Copia il collegamento di anteprima o aprilo direttamente per visualizzare l’anteprima dell’esperienza.

1. Una volta che ogni esperienza ha uno screenshot, rivedi i dettagli e fai clic su **[!UICONTROL Conferma]** per completare l&#39;installazione.

Una volta completata la configurazione, l’attività è pronta per generare opportunità. Gli insights diventano disponibili dopo che l’esperimento dispone di dati sufficienti per la convalida statistica e i dettagli dell’esperimento richiesti sono stati confermati.

## Insight {#insights}

>[!CONTEXTUALHELP]
>id="target_ai_insights_insights"
>title="Insight"
>abstract="Gli insight sugli esperimenti sono informazioni apprese generate dall’IA che diventano disponibili quando l’esperimento raggiunge la significatività statistica."

Le informazioni sugli esperimenti sono informazioni generate dall’intelligenza artificiale derivate da questo esperimento. Queste informazioni diventano disponibili quando l’esperimento raggiunge una rilevanza statistica e forniscono un contesto su ciò che ha contribuito al suo successo. Evidenziano gli attributi chiave presenti nell’esperienza vincente che sono distinti dal controllo e che probabilmente hanno influenzato il risultato.

1. Fai clic sulla scheda per accedere al menu **[!UICONTROL Informazioni]**.

   ![](assets/ai-insights-3.png)

1. Sfoglia le informazioni generate dall’intelligenza artificiale per rivedere l’apprendimento dell’esperimento e confrontare l’esperienza vincente con il controllo.

   ![](assets/ai-insights-4.png)

1. In **[!UICONTROL Cosa ha portato a vincere questa esperienza?]**, controlla i dettagli che spiegano perché questa esperienza ha superato il controllo.

## Opportunità

>[!CONTEXTUALHELP]
>id="target_ai_insights_opportunities"
>title="Opportunità"
>abstract="Le opportunità dagli esperimenti sono idee di esperienze suggerite dall’IA in base ai pattern che l’IA rileva nei risultati e nelle schermate dell’esperimento."

Il pannello **[!UICONTROL Opportunità]** mostra i consigli generati dall&#39;intelligenza artificiale progettati per migliorare le prestazioni dei test e allinearsi a obiettivi di business e KPI più ampi.

1. Sfoglia le opportunità suggerite e seleziona quella che desideri rivedere.

   ![](assets/ai-insights-5.png)

1. Seleziona un’opportunità per aprire la finestra Dettagli opportunità, che illustra un’esperienza o una variante specifica. Questa visualizzazione include:

   * L’immagine dell’esperienza corrente utilizzata per generare l’opportunità.

   * Un’ipotesi generata dall’intelligenza artificiale che spiega il risultato previsto dell’esperienza suggerita e il motivo per cui può migliorare le prestazioni.

   * Linee guida su come implementare il consiglio nella tua esperienza e misurare l’effetto sulla metrica selezionata.

   ![](assets/ai-insights-6.png)

