---
keywords: calcolatore del traffico;personalizzazione automatizzata;ap;stimare il traffico;targeting automatico
description: Utilizza il Calcolatore del traffico di Adobe Target per determinare se disponi di traffico sufficiente per il successo dell’attività Automated Personalization.
title: Quanto traffico è necessario per un'attività di successo?
feature: Personalizzazione automatizzata
exl-id: 11f9e239-700b-45cd-bf77-39f7f8967a2e
translation-type: tm+mt
source-git-commit: 094756ac64e2740e81834fde4b07d4b643ac39b9
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 14%

---

# ![PREMIUM](/help/assets/premium.png) Stimare il traffico necessario per il successo

Il [!DNL Adobe Target] [!UICONTROL Calcolatore del traffico] fornisce un feedback che ti consente di sapere se disponi di traffico sufficiente affinché l&#39;attività [!UICONTROL Automated Personalization] abbia successo.

Poiché un&#39;attività [!UICONTROL Automated Personalization] utilizza più combinazioni di offerta, è importante sapere quanto traffico è necessario per fornire risultati significativi. Il [!UICONTROL Calcolatore del traffico] utilizza le statistiche sulla pagina e il numero di esperienze sottoposte a test per stimare la quantità di traffico e la durata del test necessarie per il successo dell&#39;attività.

Il [!UICONTROL Calcolatore del traffico] determina se il traffico è sufficiente per generare modelli personalizzati confrontando le impression di pagina stimate e il tasso di conversione tipico per le pagine. Idealmente, per il successo di un&#39;attività, la corretta dimensione del campione garantisce che il contenuto personalizzato sia pronto entro il 50% della durata dell&#39;attività o in 14 giorni, a seconda del minore tra questi due valori. Questo processo consente di avere tempo sufficiente per ottenere contenuti personalizzati e per imparare quali contenuti distribuire.

Ricorda che [!DNL Target] fornisce le esperienze in modo casuale fino a quando non vengono generati gli algoritmi di personalizzazione. L’icona del segno di spunta accanto a ogni offerta mostra quando il modello per quell’offerta è pronto e [!DNL Target] è in grado di iniziare a consegnare contenuti personalizzati. Poiché l&#39;incremento è previsto solo una volta che i modelli sono pronti, l&#39;indicazione visiva consente di stabilire la giusta previsione. Utilizza il [!UICONTROL Calcolatore del traffico] nel [!UICONTROL Compositore esperienza visivo] (VEC) per ottenere una linea guida su quando i modelli sono pronti.

## Utilizza il Calcolatore del traffico

1. Dal [!UICONTROL Compositore esperienza visivo], fai clic su **[!UICONTROL Traffico]**.

   ![Icona Traffico](/help/c-activities/t-automated-personalization/assets/icon-traffic.png)

   Viene visualizzato il [!UICONTROL Calcolatore del traffico]. Fai di nuovo clic su **[!UICONTROL Traffico]**[!UICONTROL  per nascondere il Calcolatore del traffico].

   ![Interfaccia utente del Calcolatore del traffico](assets/ap_est.png)

1. Specifica il tasso di conversione tipico (o il tasso di conversione previsto per questa attività), le impression di attività stimate al giorno e la durata del test.

   | Metrica | Descrizione |
   | --- | --- |
   | **[!UICONTROL Numero di offerte]** | Questa metrica viene calcolata automaticamente in base al numero di esperienze create come parte dell’attività, dopo eventuali esclusioni. |
   | **[!UICONTROL Tasso di conversione tipico]** | Questa metrica è espressa in percentuale, in base alla stima o ai dati passati derivati dal sistema di analisi. |
   | **[!UICONTROL Visite stimate al giorno]** | Questa metrica è il numero di visite al giorno effettuate dai visitatori che possono visualizzare l’attività, in base ai criteri di targeting. Questa metrica potrebbe essere basata sui dati di analisi. Questo numero deve essere costituito da visite, non da visitatori univoci. |
   | **[!UICONTROL Durata del test]** | Il numero di giorni desiderati per l’esecuzione dell’attività. |

   Il [!UICONTROL Calcolatore del traffico] utilizza queste metriche per determinare quali regolazioni sono necessarie per eseguire un test di successo.

   Vicino alla parte superiore del [!UICONTROL Calcolatore del traffico], i valori inseriti vengono calcolati e i risultati visualizzati.

   ![Stima del traffico con valori e risultati visualizzati](assets/ap_est_no.png)

   Modificando i valori, si modifica anche la stima. Ad esempio, se stai sottoponendo a test molte combinazioni e il tasso di conversione e le impression sono troppo ridotti, il [!UICONTROL Calcolatore del traffico] mostra per quanto tempo il test deve essere eseguito per essere eseguito con successo. Oppure, se il traffico è limitato, il [!UICONTROL Calcolatore del traffico] potrebbe suggerire un numero inferiore di combinazioni di offerta in modo da poter eseguire il test per il numero desiderato di giorni.

   Se il traffico non è sufficiente, considera quanto segue:

   * Prendi in considerazione l&#39;utilizzo di un&#39;attività [Targeting automatico](/help/c-activities/auto-target/auto-target-to-optimize.md) invece di [!UICONTROL Automated Personalization] per creare esperienze con diverse modifiche di offerta in una variante di esperienza.
   * Riduci il numero di combinazioni di offerte all&#39;interno dell&#39;attività [!UICONTROL Automated Personalization].
   * Aumenta la durata dell&#39;attività.

   Regola i numeri finché il [!UICONTROL Calcolatore del traffico] indica che il traffico è sufficiente, quindi progetta il test di conseguenza.

   ![Calcolatore del traffico che mostra un messaggio di traffico sufficiente](assets/ap_est_yes.png)

   Se il traffico è sufficiente, l&#39;icona [!UICONTROL Traffico] mostra un segno di spunta verde. Se è insufficiente, l&#39;icona mostra un&#39;etichetta di avviso di colore rosso.

## Domande frequenti sul Calcolatore del traffico

Quando lavori con [!UICONTROL Calcolatore del traffico], considera le seguenti domande frequenti:

### Perché [!DNL Target] non crea modelli personalizzati quando la mia attività di Personalizzazione automatizzata ha abbastanza traffico?

In alcune circostanze, il traffico è sufficientemente ampio da consentire la creazione di un modello personalizzato, ma tale traffico potrebbe informare [!DNL Target] che non esiste alcuna differenza significativa tra il modello personalizzato e quello casuale. Anche se il modello è costruito in [!DNL Target] e testato, non viene distribuito perché il modello non è migliore di casuale.

Una possibile ragione per cui il modello non è migliore del casuale potrebbe essere che le offerte non sono abbastanza diverse l’una dall’altra. In tal caso, puoi provare a rendere le offerte più diverse dal punto di vista visivo se la messaggistica è simile, oppure provare a modificarla direttamente.
