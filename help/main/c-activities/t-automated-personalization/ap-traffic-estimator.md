---
keywords: calcolatore di traffico;personalizzazione automatizzata;ap;stima traffico
description: Utilizzare  [!DNL Adobe Target] [!UICONTROL Traffic Estimator] per determinare se si dispone di traffico sufficiente per il completamento dell'attività [!UICONTROL Automated Personalization].
title: Quanto traffico è necessario per un'attività [!UICONTROL Automated Personalization] completata?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Automated Personalization
exl-id: 11f9e239-700b-45cd-bf77-39f7f8967a2e
source-git-commit: eacee6f353aa685d17b781ac82d3f79574384dfe
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 10%

---

# Stimare il traffico necessario per il successo

[!DNL Adobe Target] [!UICONTROL Traffic Estimator] fornisce un feedback che consente di sapere se si dispone di traffico sufficiente per il completamento dell&#39;attività di [!UICONTROL Automated Personalization] (AP).

Poiché le attività [!UICONTROL Automated Personalization] utilizzano più combinazioni di offerte, è importante sapere quanto traffico è necessario per fornire risultati significativi. [!UICONTROL Traffic Estimator] utilizza le statistiche sulla pagina e sul numero di esperienze testate per stimare la quantità di traffico e la durata del test necessari per il successo dell&#39;attività.

[!UICONTROL Traffic Estimator] determina se c&#39;è abbastanza traffico per generare modelli personalizzati confrontando le impression di pagina stimate e il tasso di conversione tipico per le pagine. Idealmente, per il successo di un&#39;attività, la corretta dimensione del campione garantisce che il contenuto personalizzato sia pronto entro il 50% della durata dell&#39;attività o in 14 giorni, a seconda del minore tra questi due valori. Questo processo consente di ottenere contenuti personalizzati e di imparare quali contenuti distribuire.

Ricorda che [!DNL Target] fornisce le esperienze in modo casuale finché non vengono generati gli algoritmi di personalizzazione. L&#39;icona con il segno di spunta accanto a ogni offerta indica quando il modello per l&#39;offerta è pronto e [!DNL Target] è in grado di iniziare a consegnare contenuti personalizzati. Poiché l’incremento è previsto solo dopo che i modelli sono pronti, l’indicazione visiva consente di impostare l’aspettativa corretta. Utilizza [!UICONTROL Traffic Estimator] nel [!UICONTROL Visual Experience Composer] (VEC) per ottenere le linee guida su quando i modelli sono pronti.

## Utilizzare il Calcolatore del traffico

1. Dalla pagina [!UICONTROL Experiences] di [!UICONTROL Visual Experience Composer] in un&#39;attività [!UICONTROL Automated Personalization], fare clic sull&#39;icona **[!UICONTROL Traffic]**.

   ![Icona Traffico](/help/main/c-activities/t-automated-personalization/assets/icon-traffic.png)

   Verrà aperto [!UICONTROL Traffic Estimator]. È possibile fare di nuovo clic su **[!UICONTROL Traffic]** per nascondere [!UICONTROL Traffic Estimator].

   ![Interfaccia utente Calcolatore traffico](assets/ap_est.png)

1. Specifica il tasso di conversione tipico (o il tasso di conversione previsto per questa attività), le impression di attività stimate al giorno e la durata del test.

   | Metrica | Descrizione |
   | --- | --- |
   | **[!UICONTROL Number of Offers]** | Questa metrica viene calcolata automaticamente in base al numero di esperienze create come parte dell’attività, dopo eventuali esclusioni. |
   | **[!UICONTROL Typical Conversion Rate]** | Questa metrica è espressa in percentuale, in base alla stima o ai dati passati derivati dal sistema di analisi. |
   | **[!UICONTROL Estimated Visits Per Day]** | Questa metrica rappresenta il numero di visite al giorno da parte dei visitatori che possono visualizzare l’attività, in base ai criteri di targeting. Questa metrica potrebbe essere basata sui dati di analisi. Questo numero deve essere costituito da visite, non da visitatori univoci. |
   | **[!UICONTROL Test Duration]** | Il numero di giorni desiderati per l’esecuzione dell’attività. |

   [!UICONTROL Traffic Estimator] utilizza queste metriche per determinare le regolazioni necessarie per eseguire un test di successo.

   Nella parte superiore di [!UICONTROL Traffic Estimator], i valori immessi vengono calcolati e vengono visualizzati i risultati.

   ![Stima traffico con valori e risultati visualizzati](assets/ap_est_no.png)

   Modificando i valori, si modifica anche la stima. Ad esempio, se si stanno testando molte combinazioni e il tasso di conversione e le impression sono troppo bassi, [!UICONTROL Traffic Estimator] mostra quanto deve durare l&#39;esecuzione del test per avere successo. In alternativa, se il traffico è basso, [!UICONTROL Traffic Estimator] potrebbe suggerire un numero inferiore di combinazioni di offerte, in modo da poter eseguire il test per il numero di giorni desiderato.

   Se non disponi di traffico sufficiente, considera quanto segue:

   * È consigliabile utilizzare un&#39;attività [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) invece di [!UICONTROL Automated Personalization] per creare esperienze con diverse modifiche all&#39;offerta in una variante di esperienza.
   * Ridurre il numero di combinazioni di offerte all&#39;interno dell&#39;attività [!UICONTROL Automated Personalization].
   * Aumenta la durata dell&#39;attività.

   Regola i numeri finché [!UICONTROL Traffic Estimator] non indica che hai traffico sufficiente, quindi progetta il test di conseguenza.

   ![Il Calcolatore del traffico mostra un messaggio di traffico sufficiente](assets/ap_est_yes.png)

   Se il traffico è sufficiente, l&#39;icona [!UICONTROL Traffic] mostra un segno di spunta verde. Se è insufficiente, l&#39;icona mostra un&#39;etichetta di avviso di colore rosso.

## Domande frequenti sul Calcolatore del traffico

Considera le seguenti domande frequenti mentre lavori con [!UICONTROL Traffic Estimator]:

### Perché i modelli personalizzati non vengono generati anche se la mia attività di Personalizzazione automatizzata ha abbastanza traffico?

In alcune circostanze, il traffico è abbastanza grande da consentire la creazione di un modello personalizzato, ma potrebbe informare [!DNL Target] che non c&#39;è alcuna differenza significativa tra il modello personalizzato e casuale. Anche se il modello è stato creato in [!DNL Target] e testato, non viene distribuito perché non è migliore del modello casuale.

Un possibile motivo per cui il modello non è migliore del casuale potrebbe essere che le offerte non sono abbastanza diverse tra loro. In tal caso, puoi provare a rendere le offerte più visivamente diverse se il messaggio è simile, oppure puoi provare a modificare il messaggio stesso.
