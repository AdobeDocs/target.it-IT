---
keywords: traffico stimato;calcolatore del traffico;stima;traffico;affidabilità;potenza statistica;incremento;bonferroni;tasso di conversione;visitatori al giorno;durata
description: Scopri come utilizzare il Calcolatore del traffico che ti consente di sapere se disponi di traffico sufficiente per il completamento dell'attività [!DNL Adobe Target] [!UICONTROL Test multivariato].
title: Quanto traffico è necessario per un'attività [!UICONTROL Test multivariato] (MVT)?
feature: Multivariate Tests
exl-id: 2b32f4a7-b9b4-40bf-a17b-88225bc88787
TQID: 'https://experienceleague.adobe.com/XHBXV7Jtvp87ve4NTd-016E2dFkHTbPu-8-nY8GE-VM'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: b934e7cf-c07f-5a64-924b-3c9da8413e3d
    internal-label: Multivariate Tests
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 0ae6991a6a86854bd64a632070a1fcbe544cc606
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 8%
---
# Stimare il traffico necessario per un&#39;attività [!UICONTROL Test multivariato] completata {#traffic-estimator}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come utilizzare il **[!UICONTROL Calcolatore traffico]** per verificare se l&#39;attività **[!UICONTROL Test multivariato]** dispone di traffico sufficiente per il completamento.

>[!ENDSHADEBOX]

Un test multivariato confronta più esperienze, quindi è importante sapere quanto traffico è necessario per fornire risultati significativi. Il **[!UICONTROL Calcolatore del traffico]** utilizza le statistiche sulla pagina e sul numero di esperienze testate per stimare la quantità di traffico e la durata del test necessari per il successo del test. Fornisce inoltre un feedback che consente di sapere se disponi di traffico sufficiente per il test progettato per avere successo.

Il **[!UICONTROL Calcolatore del traffico]** prevede la dimensione del campione necessaria per garantire quanto segue:

* **Affidabilità 95%.** Questa statistica significa che la probabilità di segnalare un falso positivo in assenza di un incremento reale è del 5% (livello di affidabilità del 100%).
* **potenza statistica all&#39;80%.** Questa statistica significa che il test ha una probabilità dell’80% di individuare un incremento reale pari o superiore al 25%.
* Incremento rilevabile con affidabilità minima del **25%.** [!DNL Target] calcola la quantità di traffico necessaria per avere una probabilità dell&#39;80% di rilevare un incremento reale pari o superiore al 25%.

Il test utilizza la correzione di Bonferroni in caso di confronti multipli. Questo metodo è noto per essere di tipo conservativo, il che risulta controbilanciato dall&#39;imposizione di un incremento rilevabile con affidabilità minima relativamente ampio.

## Utilizzare il Calcolatore del traffico {#use-traffic-estimator}

Durante la progettazione di un **[!UICONTROL test multivariato]**, il **[!UICONTROL Calcolatore del traffico]** consente di verificare se il traffico verso la pagina è sufficiente per il numero di esperienze che si intende testare. L’esecuzione di questo controllo prima di avviare il test consente di evitare un test che non può raggiungere un numero sufficiente di visitatori per produrre risultati significativi e mostra come regolare il numero di combinazioni o la durata del test se il traffico non è sufficiente.

1. Dalla pagina **[!UICONTROL Esperienze]** del **[!UICONTROL Compositore esperienza visivo]** in un&#39;attività **[!UICONTROL Multivariato]**, fai clic sull&#39;icona **[!UICONTROL Traffico]** ( ![Icona Calcolatore traffico](/help/main/assets/icons/Gauge2.svg) ) nell&#39;angolo superiore sinistro della pagina.

   Verrà aperto **[!UICONTROL Calcolatore traffico]**. Per nasconderlo, fai di nuovo clic sull’icona.

   ![Interfaccia utente Calcolatore traffico](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt-est.png)

   Nella parte superiore del **[!UICONTROL Calcolatore traffico]**, vengono calcolati i valori immessi e visualizzati i risultati.

1. (Facoltativo) Fornisci il tasso di conversione tipico, i visitatori stimati al giorno e la durata del test.

   Il **[!UICONTROL Calcolatore del traffico]** utilizza queste statistiche per determinare le regolazioni necessarie per eseguire un test di successo.

   | Metrica | Descrizione |
   | --- | --- |
   | **[!UICONTROL Numero di combinazioni di contenuto]** | Questa metrica viene calcolata automaticamente, in base al numero di esperienze create come parte dell’attività, dopo eventuali esclusioni. |
   | **[!UICONTROL Tasso di conversione tipico]** | Questa metrica è espressa in percentuale, in base alla stima o ai dati passati derivati dal sistema di analisi. |
   | **[!UICONTROL Visitatori stimati al giorno]** | Questa metrica rappresenta il numero di visitatori che probabilmente visualizzeranno la pagina, in base ai criteri di targeting. Questo numero potrebbe essere basato sui dati di analisi. |
   | **[!UICONTROL Durata del test]** | Il numero di giorni desiderati per l’esecuzione dell’attività. |

1. Esamina i risultati. Modificando i valori, si modifica anche la stima.

   Ad esempio, se stai sottoponendo a test molte esperienze e il tasso di conversione e le impression sono troppo bassi, il **[!UICONTROL Calcolatore del traffico]** mostra quanto deve durare l&#39;esecuzione del test per avere successo. In alternativa, se il traffico è basso, il **[!UICONTROL Calcolatore del traffico]** potrebbe suggerire un numero inferiore di esperienze, in modo da poter eseguire il test per il numero di giorni desiderato.

1. Se non si dispone di traffico sufficiente, effettuare una o entrambe le operazioni seguenti:

   * Ridurre il numero di combinazioni di offerte e il numero di posizioni.
   * Impostare la durata del test.

1. Regola i numeri finché il **[!UICONTROL Calcolatore traffico]** non indica che hai traffico sufficiente, quindi progetta il test di conseguenza.
