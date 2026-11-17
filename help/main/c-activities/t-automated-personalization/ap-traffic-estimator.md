---
keywords: calcolatore di traffico;personalizzazione automatizzata;ap;stima traffico
description: Utilizza [!UICONTROL Calcolatore traffico] per valutare se disponi di traffico sufficiente per il completamento di un'attività [!UICONTROL Automated Personalization].
title: Quanto traffico è necessario per un'attività [!UICONTROL Automated Personalization] riuscita?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Automated Personalization
exl-id: 11f9e239-700b-45cd-bf77-39f7f8967a2e
TQID: 'https://experienceleague.adobe.com/rLjNgDlAWK-r9Zv7083vo-PdWTPy3aHGS4fXEGeTdnY'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: ddd4fa83540294ee229b87f041bc2245ba9a3464
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 8%
---
# Stimare il traffico necessario per il successo {#traffic-estimator}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come utilizzare il **[!UICONTROL Calcolatore traffico]** per verificare se l&#39;attività **[!UICONTROL Automated Personalization]** dispone di traffico sufficiente per il completamento.

>[!ENDSHADEBOX]

Il [!DNL Adobe Target] **[!UICONTROL Calcolatore traffico]** fornisce un feedback che consente di sapere se disponi di traffico sufficiente per il completamento dell&#39;attività **[!UICONTROL Automated Personalization]** (AP). Le attività di Personalizzazione automatizzata utilizzano più combinazioni di offerte, pertanto è importante sapere quanto traffico è necessario per fornire risultati significativi. Il **[!UICONTROL Calcolatore del traffico]** utilizza le statistiche sulla pagina e sul numero di esperienze testate per stimare la quantità di traffico e la durata del test necessari per il successo dell&#39;attività.

Il **[!UICONTROL Calcolatore del traffico]** determina se c&#39;è abbastanza traffico per generare modelli personalizzati confrontando le impression di pagina stimate e il tasso di conversione tipico per le pagine. Idealmente, per il successo di un&#39;attività, la corretta dimensione del campione garantisce che il contenuto personalizzato sia pronto entro il 50% della durata dell&#39;attività o in 14 giorni, a seconda del minore tra questi due valori. Questo processo consente di ottenere contenuti personalizzati e di imparare quali contenuti distribuire.

[!DNL Target] invia le esperienze in modo casuale fino alla generazione degli algoritmi di personalizzazione. L&#39;icona con il segno di spunta accanto a ogni offerta indica quando il modello per l&#39;offerta è pronto e [!DNL Target] è in grado di iniziare a consegnare contenuti personalizzati. L’incremento è previsto solo dopo che i modelli sono pronti, pertanto l’indicazione visiva consente di impostare l’aspettativa corretta. Utilizza **[!UICONTROL Calcolatore del traffico]** nel **[!UICONTROL Compositore esperienza visivo]** per ottenere le linee guida per la preparazione dei modelli.

>[!NOTE]
>
>Un modello personalizzato non viene sempre distribuito, anche quando il traffico è sufficiente. [!DNL Target] crea ed esegue il test del modello, ma distribuisce il modello solo se funziona meglio di una selezione casuale di esperienze. Se il modello non è migliore di casuale, le offerte probabilmente non sono abbastanza diverse tra loro. In tal caso, se i messaggi sono simili, rendi le offerte più visivamente diverse, oppure modifica i messaggi stessi.

## Utilizzare il Calcolatore del traffico {#use-traffic-estimator}

Durante la creazione di un&#39;attività **[!UICONTROL Automated Personalization]**, il **[!UICONTROL Calcolatore traffico]** consente di verificare se il traffico verso la pagina è sufficiente per rendere i modelli personalizzati pronti in tempo. L’esecuzione di questo controllo prima di avviare l’attività ti aiuta a evitare un test che non riesce a raggiungere un numero sufficiente di visitatori per consegnare contenuti personalizzati e mostra come regolare il numero di combinazioni di offerte o la durata dell’attività se il traffico non è sufficiente.

1. Dall&#39;attività **[!UICONTROL Automated Personalization]**, accedi alla pagina **[!UICONTROL Esperienze]** del **[!UICONTROL Compositore esperienza visivo].

1. Fai clic sull&#39;icona **[!UICONTROL Traffico]** (![Icona Calcolatore traffico](/help/main/assets/icons/Gauge2.svg)).

   Verrà aperto **[!UICONTROL Calcolatore traffico]**. Per uscire dalla finestra, fai di nuovo clic sull’icona.

   ![Interfaccia utente Calcolatore traffico](assets/ap-est.png)

1. Specifica il tasso di conversione tipico (o il tasso di conversione previsto per questa attività), le impression stimate dell’attività al giorno e la durata del test.

   Il **[!UICONTROL Calcolatore del traffico]** utilizza queste metriche per determinare le regolazioni necessarie per eseguire un test di successo.

   | Metrica | Descrizione |
   | --- | --- |
   | **[!UICONTROL Numero di offerte]** | Questa metrica viene calcolata automaticamente in base al numero di esperienze create come parte dell’attività, dopo eventuali esclusioni. |
   | **[!UICONTROL Tasso di conversione tipico]** | Questa metrica è espressa in percentuale, in base alla stima o ai dati passati derivati dal sistema di analisi. |
   | **[!UICONTROL Visite stimate al giorno]** | Questa metrica rappresenta il numero di visite al giorno da parte dei visitatori che possono visualizzare l’attività, in base ai criteri di targeting. Questa metrica potrebbe essere basata sui dati di analisi. Questo numero deve essere costituito da visite, non da visitatori univoci. |
   | **[!UICONTROL Durata del test]** | Il numero di giorni desiderati per l’esecuzione dell’attività. |



1. Esamina i risultati. Modificando i valori, si modifica anche la stima.

   Ad esempio, se stai sottoponendo a test molte combinazioni e il tasso di conversione e le impression sono troppo bassi, il **[!UICONTROL Calcolatore del traffico]** mostra quanto deve durare l&#39;esecuzione del test per avere successo. Oppure, se il tuo traffico è basso, il **[!UICONTROL Calcolatore del traffico]** potrebbe suggerire un numero inferiore di combinazioni di offerte, in modo da poter eseguire il test per il numero di giorni desiderato.

   ![Stima traffico con valori e risultati visualizzati](assets/ap-est-no.png)

1. Se non disponi di traffico sufficiente, considera le seguenti opzioni:

   * Utilizza un&#39;attività [**[!UICONTROL Targeting automatico]**](/help/main/c-activities/auto-target/auto-target-to-optimize.md) invece di **[!UICONTROL Automated Personalization]** per creare esperienze con diverse modifiche all&#39;offerta in una variante di esperienza.
   * Riduci il numero di combinazioni di offerte nell&#39;attività **[!UICONTROL Automated Personalization]**.
   * Aumenta la durata dell&#39;attività.

1. Regola i numeri finché il **[!UICONTROL Calcolatore traffico]** non indica che hai traffico sufficiente, quindi progetta il test di conseguenza.

   Se il traffico è sufficiente, l&#39;icona **[!UICONTROL Traffico]** mostra un segno di spunta verde. Se è insufficiente, l&#39;icona mostra un&#39;etichetta di avviso di colore rosso.

   ![Il Calcolatore del traffico mostra un messaggio di traffico sufficiente](assets/ap-est-yes.png)
