---
keywords: calcolatore del traffico;personalizzazione automatizzata;ap;stimare il traffico;targeting automatico
description: Utilizza l’Adobe [!DNL Target] Calcolatore del traffico per determinare se il traffico dell’attività Automated Personalization è sufficiente per il successo.
title: Quanto traffico è necessario per un'attività di successo?
feature: Automated Personalization
exl-id: 11f9e239-700b-45cd-bf77-39f7f8967a2e
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 14%

---

# ![PREMIUM](/help/main/assets/premium.png) Stimare il traffico necessario per il successo

La [!DNL Adobe Target] [!UICONTROL Calcolatore del traffico] fornisce un feedback che ti permette di sapere se disponi di traffico sufficiente per il tuo [!UICONTROL Automated Personalization] attività per il successo.

Perché [!UICONTROL Automated Personalization] l’attività utilizza più combinazioni di offerta, è importante sapere quanto traffico è necessario per fornire risultati significativi. La [!UICONTROL Calcolatore del traffico] utilizza le statistiche sulla pagina e il numero di esperienze sottoposte a test per stimare la quantità di traffico e la durata del test necessarie per il successo dell’attività.

La [!UICONTROL Calcolatore del traffico] determina se il traffico è sufficiente per generare modelli personalizzati confrontando le impression di pagina stimate e il tasso di conversione tipico per le pagine. Idealmente, per il successo di un&#39;attività, la corretta dimensione del campione garantisce che il contenuto personalizzato sia pronto entro il 50% della durata dell&#39;attività o in 14 giorni, a seconda del minore tra questi due valori. Questo processo consente di avere tempo sufficiente per ottenere contenuti personalizzati e per imparare quali contenuti distribuire.

Ricorda [!DNL Target] distribuisce in modo casuale le esperienze fino a quando non vengono generati gli algoritmi di personalizzazione. L’icona del segno di spunta accanto a ogni offerta mostra quando il modello per quell’offerta è pronto e [!DNL Target] è in grado di iniziare a distribuire contenuti personalizzati. Poiché l&#39;incremento è previsto solo una volta che i modelli sono pronti, l&#39;indicazione visiva consente di stabilire la giusta previsione. Utilizza la [!UICONTROL Calcolatore del traffico] in [!UICONTROL Compositore esperienza visivo] (Compositore esperienza visivo) per ottenere una linea guida su quando i modelli sono pronti.

## Utilizza il Calcolatore del traffico

1. Da [!UICONTROL Compositore esperienza visivo], fai clic su **[!UICONTROL Traffico]**.

   ![Icona Traffico](/help/main/c-activities/t-automated-personalization/assets/icon-traffic.png)

   La [!UICONTROL Calcolatore del traffico] si apre. Fai di nuovo clic su **[!UICONTROL Traffico]**[!UICONTROL  per nascondere il Calcolatore del traffico].

   ![Interfaccia utente del Calcolatore del traffico](assets/ap_est.png)

1. Specifica il tasso di conversione tipico (o il tasso di conversione previsto per questa attività), le impression di attività stimate al giorno e la durata del test.

   | Metrica | Descrizione |
   | --- | --- |
   | **[!UICONTROL Numero di offerte]** | Questa metrica viene calcolata automaticamente in base al numero di esperienze create come parte dell’attività, dopo eventuali esclusioni. |
   | **[!UICONTROL Tasso di conversione tipico]** | Questa metrica è espressa in percentuale, in base alla stima o ai dati passati derivati dal sistema di analisi. |
   | **[!UICONTROL Visite stimate al giorno]** | Questa metrica è il numero di visite al giorno effettuate dai visitatori che possono visualizzare l’attività, in base ai criteri di targeting. Questa metrica potrebbe essere basata sui dati di analisi. Questo numero deve essere costituito da visite, non da visitatori univoci. |
   | **[!UICONTROL Durata del test]** | Il numero di giorni desiderati per l’esecuzione dell’attività. |

   La [!UICONTROL Calcolatore del traffico] utilizza queste metriche per determinare quali regolazioni sono necessarie per eseguire un test di successo.

   Vicino alla parte superiore della [!UICONTROL Calcolatore del traffico], i valori immessi vengono calcolati e i risultati vengono visualizzati.

   ![Stima del traffico con valori e risultati visualizzati](assets/ap_est_no.png)

   Modificando i valori, si modifica anche la stima. Ad esempio, se stai sottoponendo a test molte combinazioni e il tasso di conversione e le impression sono troppo ridotti, il [!UICONTROL Calcolatore del traffico] mostra per quanto tempo deve essere eseguito il test per essere eseguito con successo. Oppure, se il traffico è limitato, il [!UICONTROL Calcolatore del traffico] potrebbe suggerire un numero inferiore di combinazioni di offerta in modo da poter eseguire il test per il numero desiderato di giorni.

   Se il traffico non è sufficiente, considera quanto segue:

   * Considera l&#39;utilizzo di un [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) attività invece di [!UICONTROL Automated Personalization] per creare esperienze con diverse modifiche di offerta in una variante di esperienza.
   * Riduci il numero di combinazioni di offerte all’interno del tuo [!UICONTROL Automated Personalization] attività.
   * Aumenta la durata dell&#39;attività.

   Regolare i numeri fino al [!UICONTROL Calcolatore del traffico] indica che il traffico è sufficiente, quindi progetta il test di conseguenza.

   ![Calcolatore del traffico che mostra un messaggio di traffico sufficiente](assets/ap_est_yes.png)

   Se il traffico è sufficiente, il [!UICONTROL Traffico] l’icona mostra un segno di spunta verde. Se è insufficiente, l&#39;icona mostra un&#39;etichetta di avviso di colore rosso.

## Domande frequenti sul Calcolatore del traffico

Quando lavori con le [!UICONTROL Calcolatore del traffico]:

### Perché i modelli personalizzati non vengono generati anche se la mia attività di Personalizzazione automatizzata ha abbastanza traffico?

In alcune circostanze, il traffico è sufficientemente ampio da consentire la creazione di un modello personalizzato, ma il traffico potrebbe informare [!DNL Target] che non vi sia alcuna differenza significativa tra il modello personalizzato e quello casuale. Anche se il modello è incorporato [!DNL Target] e testato, non viene distribuito perché il modello non è migliore di casuale.

Una possibile ragione per cui il modello non è migliore del casuale potrebbe essere che le offerte non sono abbastanza diverse l’una dall’altra. In tal caso, puoi provare a rendere le offerte più diverse dal punto di vista visivo se la messaggistica è simile, oppure provare a cambiare la messaggistica stessa.
