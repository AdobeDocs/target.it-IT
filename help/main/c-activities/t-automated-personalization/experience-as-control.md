---
keywords: esperienza;controllo;personalizzazione automatizzata;target automatico
description: Scopri come selezionare un’esperienza da utilizzare come controllo durante la creazione di un’ [!UICONTROL Automated Personalization] (AP) o [!UICONTROL Targeting automatico] attività in [!DNL Adobe Target].
title: Come posso utilizzare un’esperienza specifica come controllo in un [!UICONTROL Automated Personalization] Attività?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Automated Personalization, Auto-Target
solution: Target,Analytics
exl-id: a0a36ace-3cba-4d8d-9bbd-e35204ff6453
source-git-commit: a9508c4bc454faeb8d6763677cce17a264a4a70f
workflow-type: tm+mt
source-wordcount: '783'
ht-degree: 42%

---

# Selezionare il controllo per [!UICONTROL Automated Personalization] o [!UICONTROL Targeting automatico] attività

Puoi selezionare un’esperienza casuale o un’esperienza specifica da usare come controllo durante la creazione di un’ [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) o [[!UICONTROL Targeting automatico]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT).

Questa funzione ti permette di indirizzare tutto il traffico di controllo a una specifica esperienza, in base alla percentuale di allocazione del traffico configurata nell’attività. Puoi quindi valutare i rapporti sulle prestazioni del traffico personalizzato rispetto al traffico verso questa esperienza di controllo.

Opzioni per l&#39;impostazione di un controllo in [!UICONTROL Automated Personalization] e [!UICONTROL Targeting automatico] Le attività sono leggermente diverse da altri tipi di attività. In un manuale [!UICONTROL Test A/B], puoi modificare il contenuto del rapporto visualizzato come controllo e l’incremento viene calcolato in base al tasso di conversione dell’esperienza di controllo. Puoi effettuare facilmente questa modifica perché il traffico viene distribuito in modo casuale verso ogni esperienza inclusa nell’attività, indipendentemente dall’impostazione iniziale del controllo. In altre parole, la selezione del controllo non influisce sul modo in cui viene distribuito il traffico. In entrata [!UICONTROL Automated Personalization] e [!UICONTROL Targeting automatico] attività, la scelta del controllo influisce sul modo in cui viene distribuito il traffico del visitatore. Di conseguenza, devi riflettere più attentamente sulla tua decisione.

Sono disponibili due opzioni per il controllo nel [!UICONTROL Automated Personalization] e [!UICONTROL Targeting automatico] attività:

* **Distribuzione casuale**: per un controllo casuale, la percentuale di traffico del controllo viene utilizzata in modo casuale per tutte le esperienze dell’attività, senza considerare il profilo del visitatore. Puoi considerare il controllo come una risposta alla domanda: &quot;Se distribuisco un’esperienza (o offerta) in modo casuale ai visitatori e non considero i loro profili, qual è il tasso di conversione per tale esperienza (o offerta)?&quot; Il controllo è simile a un [!UICONTROL Test A/B] nell’attività di intelligenza artificiale. Queste informazioni sul tasso di conversione non personalizzato per ogni esperienza o offerta possono essere utili per comprendere quando analizzare i risultati dell’attività.

* **Esperienza specifica**: un controllo esperienza specifico consente di confrontare il traffico gestito da [!DNL Target] modelli di personalizzazione a un’esperienza specifica definita dall’addetto al marketing (ad esempio, la pagina home predefinita). Con questa opzione, la percentuale di traffico di controllo viene veicolata in modo casuale unicamente all’esperienza definita come controllo.

## Specificare come controllo un’esperienza specifica

1. Durante la creazione di un’ [[!UICONTROL Automated Personalization] attività](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) o [[!UICONTROL Targeting automatico] attività](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), configura le esperienze nel modo desiderato.
1. Nella pagina [!UICONTROL Targeting] (passaggio 2 del flusso di lavoro guidato in tre parti), seleziona l’esperienza da usare come controllo.
1. Specifica la percentuale di traffico da allocare all’esperienza di controllo e alle altre esperienze.

   Se usi come controllo una specifica esperienza, i valori consigliati sono dal 10% al 30%.

1. Procedi alla pagina [!UICONTROL Obiettivi e impostazioni].

## Limitazioni note e considerazioni

Quando utilizzi come controllo un’esperienza specifica, considera gli aspetti seguenti:

* Non è consigliabile cambiare l’esperienza di controllo per un’attività live. Nei rapporti si fa riferimento all’ultima esperienza di controllo selezionata, anche se i rapporti precedenti sono basati su un’altra esperienza.
* Non è consigliabile eliminare l’esperienza di controllo.
* Non è consigliabile aggiungere molte nuove offerte o esperienze a un’attività live con un’esperienza specifica come controllo.
* In entrata [!UICONTROL Automated Personalization] non è consigliabile eseguire attività, incluso il targeting sull’esperienza di controllo che potrebbe vincolare ulteriormente chi può vedere tale esperienza.
* In entrata [!UICONTROL Automated Personalization] attività, informazioni su incremento e affidabilità *NOT* disponibile nel rapporto a livello di offerta, se è selezionata un’esperienza specifica. Le informazioni di incremento e affidabilità sono disponibili a livello di traffico &quot;mirato&quot; complessivo rispetto a quello di &quot;controllo&quot; per [!UICONTROL Automated Personalization] attività. Le informazioni di incremento e affidabilità sono disponibili se si utilizza un controllo di tipo casuale. Tale differenza è dovuta al fatto che il confronto tra il tasso di conversione di un’esperienza specifica e quello di un’offerta non è logico a causa della differenza nelle unità. Le informazioni disponibili in un [!UICONTROL Targeting automatico] l&#39;attività è la stessa, indipendentemente dal tipo di controllo selezionato.
* In genere è richiesto meno traffico verso il controllo: infatti, quando si seleziona come controllo un’esperienza specifica, tutto il traffico viene veicolato verso un’unica esperienza o un set di offerte; nel caso di un controllo casuale, invece, il traffico allocato al controllo viene suddiviso tra le varie esperienze o offerte presenti nell’attività. Si consiglia di iniziare con un valore di 10%.
* Se le seguenti operazioni vengono effettuate su un’attività live e con il controllo impostato un’esperienza specifica, questo viene reimpostato automaticamente su esperienze casuali (anziché sull’esperienza specifica selezionata in precedenza):

   * Eliminare un’esperienza
   * Rimuovere una posizione o un’offerta ([!UICONTROL Automated Personalization] solo )
   * Escludere un’esperienza manualmente rimuovendo le offerte duplicate o tramite un gruppo di esclusione ([!UICONTROL Automated Personalization] solo )
