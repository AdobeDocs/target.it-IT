---
keywords: calcolatore di traffico;personalizzazione automatizzata;ap;stima traffico
description: Utilizza [!UICONTROL Calcolatore traffico] per valutare se disponi di traffico sufficiente per il completamento di un'attività [!UICONTROL Automated Personalization].
title: Quanto traffico è necessario per un'attività [!UICONTROL Automated Personalization] riuscita?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Automated Personalization
exl-id: 11f9e239-700b-45cd-bf77-39f7f8967a2e
TQID: https://experienceleague.adobe.com/rLjNgDlAWK-r9Zv7083vo-PdWTPy3aHGS4fXEGeTdnY
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 794
ht-degree: 8%

---

# Stimare il traffico necessario per il successo

Il [!DNL Adobe Target] [!UICONTROL Calcolatore traffico] fornisce un feedback che consente di sapere se disponi di traffico sufficiente per il completamento dell&#39;attività [!UICONTROL Automated Personalization] (AP).

Poiché le attività di [!UICONTROL Automated Personalization] utilizzano più combinazioni di offerte, è importante sapere quanto traffico è necessario per fornire risultati significativi. Il [!UICONTROL Calcolatore del traffico] utilizza le statistiche sulla pagina e sul numero di esperienze testate per stimare la quantità di traffico e la durata del test necessari per il successo dell&#39;attività.

Il [!UICONTROL Calcolatore del traffico] determina se c&#39;è abbastanza traffico per generare modelli personalizzati confrontando le impression di pagina stimate e il tasso di conversione tipico per le pagine. Idealmente, per il successo di un&#39;attività, la corretta dimensione del campione garantisce che il contenuto personalizzato sia pronto entro il 50% della durata dell&#39;attività o in 14 giorni, a seconda del minore tra questi due valori. Questo processo consente di ottenere contenuti personalizzati e di imparare quali contenuti distribuire.

Ricorda che [!DNL Target] fornisce le esperienze in modo casuale finché non vengono generati gli algoritmi di personalizzazione. L&#39;icona con il segno di spunta accanto a ogni offerta indica quando il modello per l&#39;offerta è pronto e [!DNL Target] è in grado di iniziare a consegnare contenuti personalizzati. Poiché l’incremento è previsto solo dopo che i modelli sono pronti, l’indicazione visiva consente di impostare l’aspettativa corretta. Utilizza [!UICONTROL Calcolatore del traffico] nel [!UICONTROL Compositore esperienza visivo] per ottenere le linee guida per la preparazione dei modelli.

## Utilizzare il Calcolatore del traffico

1. Dalla pagina [!UICONTROL Esperienze] del [!UICONTROL Compositore esperienza visivo] in un&#39;attività [!UICONTROL Automated Personalization], fai clic sull&#39;icona **[!UICONTROL Traffico]** ( ![Icona Calcolatore traffico](/help/main/assets/icons/Gauge2.svg) ) nell&#39;angolo superiore sinistro della pagina [!UICONTROL Esperienze].

   Verrà aperto [!UICONTROL Calcolatore traffico].

   ![Interfaccia utente Calcolatore traffico](assets/ap-est.png)

   Fai di nuovo clic sull&#39;icona per nascondere il [!UICONTROL Calcolatore del traffico].

1. Specifica il tasso di conversione tipico (o il tasso di conversione previsto per questa attività), le impression di attività stimate al giorno e la durata del test.

   | Metrica | Descrizione |
   | --- | --- |
   | **[!UICONTROL Numero di offerte]** | Questa metrica viene calcolata automaticamente in base al numero di esperienze create come parte dell’attività, dopo eventuali esclusioni. |
   | **[!UICONTROL Tasso di conversione tipico]** | Questa metrica è espressa in percentuale, in base alla stima o ai dati passati derivati dal sistema di analisi. |
   | **[!UICONTROL Visite stimate al giorno]** | Questa metrica rappresenta il numero di visite al giorno da parte dei visitatori che possono visualizzare l’attività, in base ai criteri di targeting. Questa metrica potrebbe essere basata sui dati di analisi. Questo numero deve essere costituito da visite, non da visitatori univoci. |
   | **[!UICONTROL Durata del test]** | Il numero di giorni desiderati per l’esecuzione dell’attività. |

   Il [!UICONTROL Calcolatore del traffico] utilizza queste metriche per determinare le regolazioni necessarie per eseguire un test di successo.

   Nella parte superiore del [!UICONTROL Calcolatore traffico], vengono calcolati i valori immessi e visualizzati i risultati.

   ![Stima traffico con valori e risultati visualizzati](assets/ap-est-no.png)

   Modificando i valori, si modifica anche la stima. Ad esempio, se stai sottoponendo a test molte combinazioni e il tasso di conversione e le impression sono troppo bassi, il [!UICONTROL Calcolatore del traffico] mostra quanto deve durare l&#39;esecuzione del test per avere successo. Oppure, se il tuo traffico è basso, il [!UICONTROL Calcolatore del traffico] potrebbe suggerire un numero inferiore di combinazioni di offerte, in modo da poter eseguire il test per il numero di giorni desiderato.

   Se non disponi di traffico sufficiente, considera quanto segue:

   * Valuta l&#39;utilizzo di un&#39;attività [[!UICONTROL Targeting automatico]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) invece di [!UICONTROL Automated Personalization] per creare esperienze con diverse modifiche all&#39;offerta in una variante di esperienza.
   * Riduci il numero di combinazioni di offerte nell&#39;attività [!UICONTROL Automated Personalization].
   * Aumenta la durata dell&#39;attività.

   Regola i numeri finché il [!UICONTROL Calcolatore traffico] non indica che hai traffico sufficiente, quindi progetta il test di conseguenza.

   ![Il Calcolatore del traffico mostra un messaggio di traffico sufficiente](assets/ap-est-yes.png)

   Se il traffico è sufficiente, l&#39;icona [!UICONTROL Traffico] mostra un segno di spunta verde. Se è insufficiente, l&#39;icona mostra un&#39;etichetta di avviso di colore rosso.

## Domande frequenti sul Calcolatore del traffico

Considera le seguenti domande frequenti mentre lavori con [!UICONTROL Calcolatore traffico]:

### Perché i modelli personalizzati non vengono generati anche se la mia attività di Personalizzazione automatizzata ha abbastanza traffico?

In alcune circostanze, il traffico è abbastanza grande da consentire la creazione di un modello personalizzato, ma potrebbe informare [!DNL Target] che non c&#39;è alcuna differenza significativa tra il modello personalizzato e casuale. Anche se il modello è stato creato in [!DNL Target] e testato, non viene distribuito perché non è migliore del modello casuale.

Un possibile motivo per cui il modello non è migliore del casuale potrebbe essere che le offerte non sono abbastanza diverse tra loro. In tal caso, puoi provare a rendere le offerte più visivamente diverse se il messaggio è simile, oppure puoi provare a modificare il messaggio stesso.
