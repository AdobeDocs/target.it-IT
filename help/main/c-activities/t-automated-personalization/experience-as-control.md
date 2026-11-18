---
keywords: esperienza;controllo;personalizzazione automatizzata;target automatico
description: Scopri come selezionare un'esperienza da utilizzare come controllo durante la creazione di un'attività [!UICONTROL Automated Personalization] (AP) o [!UICONTROL Targeting automatico] in [!DNL Adobe Target].
title: Come posso utilizzare un'esperienza specifica come controllo in un'attività [!UICONTROL Automated Personalization]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Automated Personalization, Auto-Target
solution: Target,Analytics
exl-id: a0a36ace-3cba-4d8d-9bbd-e35204ff6453
TQID: 'https://experienceleague.adobe.com/a-lIVDWxeAi-VCp7-lLD-zaClCDCKJGfa25XMKF0vZA'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
  - id: db15a02f-03cd-46fe-a53e-02064cdeadfa
    internal-label: Auto target
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 44c6bdd4ab818226e76477782d7e4238b49d5cdc
workflow-type: tm+mt
source-wordcount: '801'
ht-degree: 3%
---
# Seleziona l’esperienza di controllo {#experience-as-control}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come scegliere il controllo di un&#39;attività **[!UICONTROL Automated Personalization]** o **[!UICONTROL Targeting automatico]** e cosa considerare quando utilizzi come controllo un&#39;esperienza specifica.

>[!ENDSHADEBOX]

Durante la creazione di un&#39;attività di [**[!UICONTROL Automated Personalization]**](/help/main/c-activities/t-automated-personalization/automated-personalization.md#automated-personalization-overview) (AP) o [**[!UICONTROL Targeting automatico]**](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) puoi selezionare un&#39;esperienza casuale o un&#39;esperienza specifica da utilizzare come controllo. Il traffico di controllo viene indirizzato alle esperienze rilevanti in base alla percentuale di allocazione del traffico configurata nell’attività, in modo da poter valutare i rapporti sulle prestazioni del traffico personalizzato rispetto al traffico di controllo.

In un **[!UICONTROL Test A/B]** manuale, è possibile modificare ciò che il reporting mostra come controllo e l&#39;incremento viene calcolato da tale esperienza, perché il traffico viene distribuito in modo casuale a tutte le esperienze, indipendentemente dal controllo. Nelle attività **[!UICONTROL Automated Personalization]** e **[!UICONTROL Targeting automatico]**, il controllo influisce sul modo in cui viene distribuito il traffico del visitatore, quindi scegline attentamente.

Per il controllo sono disponibili due opzioni:

* **Distribuzione casuale:** La percentuale di traffico del controllo viene distribuita in modo casuale a tutte le esperienze dell&#39;attività, senza considerare il profilo del visitatore. Funziona come un **[!UICONTROL Test A/B]** all&#39;interno dell&#39;attività e mostra il tasso di conversione non personalizzato di ogni esperienza o offerta, per aiutarti ad analizzare i risultati.

* **Esperienza specifica:** La percentuale di traffico del controllo viene distribuita in modo casuale solo a quella esperienza. Questa opzione consente di confrontare il traffico gestito dai modelli di personalizzazione [!DNL Target] con un&#39;esperienza specifica definita, ad esempio la pagina home predefinita.

## Considerazioni {#considerations}

Quando utilizzi come controllo un’esperienza specifica, considera gli aspetti seguenti:

* Non è consigliabile modificare l’esperienza di controllo in un’attività live. Nella generazione rapporti viene denominato l’ultima esperienza di controllo selezionata, anche se i rapporti precedenti sono basati su un’altra esperienza.

* Non è consigliabile eliminare l’esperienza di controllo.

* Non è consigliabile aggiungere molte nuove offerte o esperienze a un’attività live con un’esperienza specifica come controllo.

* Nelle attività di **[!UICONTROL Automated Personalization]**, non è consigliabile includere nell&#39;esperienza di controllo un targeting che potrebbe limitare ulteriormente chi può vedere tale esperienza.

* Nelle attività di **[!UICONTROL Automated Personalization]**, le informazioni su incremento e affidabilità sono *non* disponibili nel report a livello di offerta se è selezionata un&#39;esperienza specifica. Questo perché il confronto tra il tasso di conversione di un’esperienza specifica e il tasso di conversione di un’offerta non è logico a causa della differenza nelle unità. Le informazioni di incremento e affidabilità sono disponibili a livello di traffico &quot;mirato&quot; complessivo rispetto al livello di traffico &quot;di controllo&quot; per l’attività e a tutti i livelli se come controllo viene selezionato &quot;casuale&quot;. Le informazioni disponibili in un&#39;attività di **[!UICONTROL Targeting automatico]** sono uguali, indipendentemente dal tipo di controllo selezionato.

* Quando selezioni un’esperienza specifica come controllo, tutto il traffico viene indirizzato a un’unica esperienza o a un set di offerte. Con un controllo casuale, il traffico di controllo viene suddiviso sul numero di esperienze o offerte nell’attività. Di conseguenza, in genere non è necessario trasportare tanto traffico verso il controllo con un’esperienza specifica. Si consiglia di iniziare con un valore di 10%.

* Se esegui una delle operazioni seguenti su un’attività live e il controllo è impostato su un’esperienza specifica, questo viene reimpostato automaticamente su esperienze casuali (anziché sull’esperienza specifica selezionata in precedenza):

  * Eliminare un’esperienza.
  * Rimuovi una posizione o un&#39;offerta (**[!UICONTROL solo Automated Personalization]**).
  * Escludi un&#39;esperienza manualmente, rimuovendo le offerte duplicate o tramite un gruppo di esclusione (**[!UICONTROL Automated Personalization]** only).


## Specificare come controllo un’esperienza specifica {#specify-control}

Specificando come controllo un’esperienza specifica, nei rapporti dell’attività si assegna al traffico personalizzato un’esperienza nota da confrontare, ad esempio l’esperienza predefinita corrente.

1. Durante la creazione o la modifica di un&#39;attività [**[!UICONTROL Automated Personalization ]**](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#create-ap-activity) o di un&#39;attività [**[!UICONTROL Targeting automatico]**](/help/main/c-activities/auto-target/create-auto-target.md#create-auto-target-activity), configura le esperienze nel modo desiderato.

1. Nella pagina **[!UICONTROL Targeting]** (passaggio 2 del flusso di lavoro guidato in tre parti), fai clic sull&#39;esperienza di controllo per visualizzare le opzioni **[!UICONTROL Controllo]** nel riquadro a destra.

   ![Riquadro di controllo](/help/main/c-activities/t-automated-personalization/assets/control.png)

1. Dall&#39;elenco a discesa **[!UICONTROL Controllo]**, selezionare **[!UICONTROL Esperienza casuale]** oppure selezionare l&#39;esperienza che si desidera utilizzare come controllo.

1. Fai clic sul controllo **[!UICONTROL Allocazione traffico]**, quindi specifica l&#39;allocazione del traffico per l&#39;esperienza di controllo e le altre esperienze.

   ![Barra di allocazione traffico](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation.png)

   Se usi come controllo una specifica esperienza, i valori consigliati sono dal 10% al 30%.

1. Continua con la pagina **[!UICONTROL Obiettivi e impostazioni]**.

Una volta che l’attività è live, i relativi rapporti confrontano il traffico personalizzato con l’esperienza di controllo selezionata. Rivedi le [considerazioni](#considerations) prima di modificare un&#39;attività live, poiché alcune modifiche reimpostano automaticamente il controllo su esperienze distribuite in modo casuale.
