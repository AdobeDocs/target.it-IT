---
keywords: experience;control;automated personalization;auto-target
description: Puoi selezionare un’esperienza da usare come controllo durante la creazione di un’attività di Personalizzazione automatizzata o Targeting automatico in Adobe Target.
title: Utilizzare un’esperienza specifica come controllo in Adobe Target
feature: Automated Personalization
solution: Target,Analytics
translation-type: tm+mt
source-git-commit: 4adade56529fb95e4400e06d04d3c6c69e120edc
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 100%

---


# ![PREMIUM](/help/assets/premium.png) Selezionare il controllo per un’attività di Personalizzazione automatizzata o Targeting automatico

Durante la creazione di un’attività [Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/automated-personalization.md) o [Targeting automatico](/help/c-activities/auto-target/auto-target-to-optimize.md), puoi scegliere di usare come controllo un’esperienza casuale o selezionarne una specifica.

Questa funzione ti permette di indirizzare tutto il traffico di controllo a una specifica esperienza, in base alla percentuale di allocazione del traffico configurata nell’attività. Puoi quindi valutare i rapporti sulle prestazioni del traffico personalizzato rispetto al traffico verso questa esperienza di controllo.

Le opzioni per l’impostazione di un controllo nelle attività di personalizzazione automatizzata o targeting automatico sono leggermente diverse da quelle di altri tipi di attività. In un test A/B manuale, puoi modificare il tipo di rapporto visualizzato come controllo e l’incremento viene calcolato in base al tasso di conversione dell’esperienza di controllo. Puoi effettuare facilmente questa modifica perché il traffico viene distribuito in modo casuale verso ogni esperienza inclusa nell’attività, indipendentemente dall’impostazione iniziale del controllo. In altre parole, la selezione del controllo non influisce sul modo in cui viene distribuito il traffico. Nelle attività di personalizzazione automatizzata e targeting automatico, la scelta del controllo influisce su come viene distribuito il traffico di visitatori. È quindi importante considerare attentamente questa scelta.

Nelle attività di personalizzazione automatizzata e targeting automatico sono disponibili due opzioni per il controllo: esperienze distribuite in modo casuale o un’esperienza specifica.

* **Distribuzione casuale**: tutte le esperienze presenti nell’attività vengono distribuite in modo casuale, senza considerare il profilo del visitatore, in base alla percentuale di traffico del controllo. Questo è utile per rispondere ad esempio alla domanda: “Se un’esperienza o offerta viene distribuita in modo casuale ai visitatori, senza prendere in considerazione i loro profili, qual è il tasso di conversione per tale esperienza o offerta?” Il controllo è simile a un test A/B nell’attività AI. Queste informazioni sul tasso di conversione non personalizzato per ogni esperienza o offerta possono essere utili per comprendere quando analizzare i risultati dell’attività.

* **Esperienza specifica**: è possibile confrontare il traffico distribuito dai modelli di personalizzazione di Target rispetto a una specifica esperienza definita dall’addetto al marketing (ad esempio, la pagina home predefinita). Con questa opzione, la percentuale di traffico di controllo viene veicolata in modo casuale unicamente all’esperienza definita come controllo.

## Specificare come controllo un’esperienza specifica

1. Durante la creazione di un’attività di [Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/create-ap-activity.md) o [Targeting automatico](/help/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), configura le esperienze in base alle tue esigenze.
1. Nella pagina [!UICONTROL Targeting] (passaggio 2 del flusso di lavoro guidato in tre parti), seleziona l’esperienza da usare come controllo.
1. Specifica la percentuale di traffico da allocare all’esperienza di controllo e alle altre esperienze.

   Se usi come controllo una specifica esperienza, i valori consigliati sono dal 10% al 30%.

1. Procedi alla pagina [!UICONTROL Obiettivi e impostazioni].

## Limitazioni note e considerazioni

Quando usi come controllo un’esperienza specifica, considera gli aspetti seguenti:

* Non è consigliabile cambiare l’esperienza di controllo per un’attività live. Nei rapporti si fa riferimento all’ultima esperienza di controllo selezionata, anche se i rapporti precedenti sono basati su un’altra esperienza.
* Non è consigliabile eliminare l’esperienza di controllo.
* Non è consigliabile aggiungere un numero elevato di nuove offerte o esperienze a un’attività live quando il controllo è impostato su un’esperienza specifica.
* Nelle attività di personalizzazione automatizzata, non è consigliabile includere nell’esperienza di controllo un targeting che potrebbe vincolare ulteriormente chi può vedere tale esperienza.
* Nelle attività di personalizzazione automatizzata, le informazioni su incremento e affidabilità *NON* sono disponibili nel report a livello di offerta se è selezionata un’esperienza specifica. Per queste attività, le informazioni di incremento e affidabilità sono disponibili a livello di traffico “con targeting” complessivo, e non a livello di traffico “di controllo”. Le informazioni di incremento e affidabilità sono disponibili se si utilizza un controllo di tipo casuale. Tale differenza è dovuta al fatto che il confronto tra il tasso di conversione di un’esperienza specifica e quello di un’offerta non è logico a causa della differenza nelle unità. Le informazioni disponibili in un’attività di targeting automatico sono uguali, indipendentemente dal tipo di controllo selezionato.
* In genere è richiesto meno traffico verso il controllo: infatti, quando si seleziona come controllo un’esperienza specifica, tutto il traffico viene veicolato verso un’unica esperienza o un set di offerte; nel caso di un controllo casuale, invece, il traffico allocato al controllo viene suddiviso tra le varie esperienze o offerte presenti nell’attività. Si consiglia di iniziare con un valore di 10%.
* Se le seguenti operazioni vengono effettuate su un’attività live e con il controllo impostato un’esperienza specifica, questo viene reimpostato automaticamente su esperienze casuali (anziché sull’esperienza specifica selezionata in precedenza):

   * Eliminare un’esperienza
   * Rimuovere una posizione o un’offerta (solo Personalizzazione automatizzata)
   * Escludere un’esperienza, manualmente, rimuovendo le offerte duplicate o tramite un gruppo di esclusione (solo Personalizzazione automatizzata)

