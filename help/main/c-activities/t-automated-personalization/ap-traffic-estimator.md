---
keywords: calcolatore di traffico;personalizzazione automatizzata;ap;stima traffico;targeting automatico
description: Utilizza l’Adobe [!DNL Target] Calcolatore del traffico per determinare se disponi di traffico sufficiente per il successo dell’attività Automated Personalization.
title: Quanto traffico è necessario per un'attività di successo?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
exl-id: 11f9e239-700b-45cd-bf77-39f7f8967a2e
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 14%

---

# Stimare il traffico necessario per il successo

Il [!DNL Adobe Target] [!UICONTROL Calcolatore del traffico] fornisce un feedback che ti consente di sapere se disponi di traffico sufficiente per il tuo [!UICONTROL Automated Personalization] attività per il completamento.

Perché un [!UICONTROL Automated Personalization] l’attività utilizza più combinazioni di offerte, è importante sapere quanto traffico è necessario per fornire risultati significativi. Il [!UICONTROL Calcolatore del traffico] utilizza le statistiche sulla pagina e sul numero di esperienze testate per stimare la quantità di traffico e la durata del test necessari per il successo dell’attività.

Il [!UICONTROL Calcolatore del traffico] determina se il traffico è sufficiente per generare modelli personalizzati confrontando le impression di pagina stimate e il tasso di conversione tipico per le pagine. Idealmente, per il successo di un&#39;attività, la corretta dimensione del campione garantisce che il contenuto personalizzato sia pronto entro il 50% della durata dell&#39;attività o in 14 giorni, a seconda del minore tra questi due valori. Questo processo consente di ottenere contenuti personalizzati e di imparare quali contenuti distribuire.

Ricorda che [!DNL Target] fornisce le esperienze in modo casuale, fino a quando non vengono generati gli algoritmi di personalizzazione. L’icona a forma di segno di spunta posta accanto a ciascuna offerta mostra quando il modello è pronto e [!DNL Target] è in grado di iniziare a consegnare contenuti personalizzati. Poiché l&#39;incremento è previsto solo una volta che i modelli sono pronti, l&#39;indicazione visiva consente di stabilire la giusta previsione. Utilizza il [!UICONTROL Calcolatore del traffico] nel [!UICONTROL Compositore esperienza visivo] (VEC) per ottenere indicazioni su quando i modelli sono pronti.

## Utilizzare il Calcolatore del traffico

1. Dalla sezione [!UICONTROL Compositore esperienza visivo], fai clic su **[!UICONTROL Traffico]**.

   ![Icona Traffico](/help/main/c-activities/t-automated-personalization/assets/icon-traffic.png)

   Il [!UICONTROL Calcolatore del traffico] viene aperto. Fai di nuovo clic su **[!UICONTROL Traffico]**[!UICONTROL  per nascondere il Calcolatore del traffico].

   ![Interfaccia utente del Calcolatore del traffico](assets/ap_est.png)

1. Specifica il tasso di conversione tipico (o il tasso di conversione previsto per questa attività), le impression di attività stimate al giorno e la durata del test.

   | Metrica | Descrizione |
   | --- | --- |
   | **[!UICONTROL Numero di offerte]** | Questa metrica viene calcolata automaticamente in base al numero di esperienze create come parte dell’attività, dopo eventuali esclusioni. |
   | **[!UICONTROL Tasso di conversione tipico]** | Questa metrica è espressa in percentuale, in base alla stima o ai dati passati derivati dal sistema di analisi. |
   | **[!UICONTROL Visite stimate al giorno]** | Questa metrica rappresenta il numero di visite al giorno da parte dei visitatori che possono visualizzare l’attività, in base ai criteri di targeting. Questa metrica potrebbe essere basata sui dati di analisi. Questo numero deve essere costituito da visite, non da visitatori univoci. |
   | **[!UICONTROL Durata del test]** | Il numero di giorni desiderati per l’esecuzione dell’attività. |

   Il [!UICONTROL Calcolatore del traffico] utilizza queste metriche per determinare le regolazioni necessarie per eseguire un test di successo.

   Vicino alla parte superiore del [!UICONTROL Calcolatore del traffico], vengono calcolati i valori immessi e visualizzati i risultati.

   ![Stima traffico con valori e risultati visualizzati](assets/ap_est_no.png)

   Modificando i valori, si modifica anche la stima. Ad esempio, se stai sottoponendo a test molte combinazioni e il tasso di conversione e le impression sono troppo bassi, il [!UICONTROL Calcolatore del traffico] mostra quanto tempo deve essere eseguito il test per avere successo. Oppure, se il traffico è basso, il [!UICONTROL Calcolatore del traffico] potrebbe suggerire un numero inferiore di combinazioni di offerte in modo da poter eseguire il test per il numero di giorni desiderato.

   Se non disponi di traffico sufficiente, considera quanto segue:

   * Valuta l’utilizzo di un’ [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) attività invece di [!UICONTROL Automated Personalization] per creare esperienze con diverse modifiche all’offerta in una variante di esperienza.
   * Riduci il numero di combinazioni di offerte all’interno del [!UICONTROL Automated Personalization] attività.
   * Aumenta la durata dell&#39;attività.

   Regola i numeri fino a quando [!UICONTROL Calcolatore del traffico] indica che disponi di traffico sufficiente, quindi progetta il test di conseguenza.

   ![Calcolatore del traffico che mostra un messaggio di traffico sufficiente](assets/ap_est_yes.png)

   Se il traffico è sufficiente, il [!UICONTROL Traffico] mostra una spunta verde. Se è insufficiente, l&#39;icona mostra un&#39;etichetta di avviso di colore rosso.

## Domande frequenti sul Calcolatore del traffico

Considera le seguenti domande frequenti mentre lavori con [!UICONTROL Calcolatore del traffico]:

### Perché i modelli personalizzati non vengono generati anche se la mia attività di Personalizzazione automatizzata ha abbastanza traffico?

In alcune circostanze, il traffico è abbastanza grande da consentire la creazione di un modello personalizzato, ma potrebbe informare [!DNL Target] che non vi sia alcuna differenza significativa tra il modello personalizzato e casuale. Anche se il modello è incorporato [!DNL Target] e testato, non viene distribuito perché il modello non è migliore del casuale.

Un possibile motivo per cui il modello non è migliore del casuale potrebbe essere che le offerte non sono abbastanza diverse tra loro. In tal caso, puoi provare a rendere le offerte più visivamente diverse se il messaggio è simile, oppure puoi provare a modificare il messaggio stesso.
