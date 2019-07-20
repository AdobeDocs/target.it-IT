---
description: Selezionate un'esperienza da utilizzare come controllo durante la creazione di un'attività Automated Personalization (Personalizzazione automatizzata) o Auto-Target (Destinazione automatica).
keywords: esperienza; control; personalizzazione automatizzata; target automatico
seo-description: Selezionate un'esperienza da utilizzare come controllo durante la creazione di un'attività Automated Personalization (Personalizzazione automatizzata) o Auto-Target (Target automatico) in Adobe Target.
seo-title: Utilizzo di un'esperienza specifica come controllo in Adobe Target
solution: Target,Analytics
title: Utilizzo di un'esperienza specifica come controllo
uuid: c67901d2-19cd-47d3-b8c4-abdcb046f404
translation-type: tm+mt
source-git-commit: add895d353e7483dfcbe82f1bca55b277bc65f20

---


# ![PREMIUM](/help/assets/premium.png) Selezionate il controllo per l'attività Automated Personalization (Personalizzazione automatizzata) o Auto-Target (Destinazione automatica)

You can select a randomly served experience or a specific experience to be used as control while creating an [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) or [Auto-Target](/help/c-activities/auto-target-to-optimize.md) (AT) activity.

Questa funzione consente di indirizzare il traffico verso le esperienze pertinenti, in base alla percentuale di allocazione del traffico configurata nell'attività. Potete quindi valutare i rapporti sulle prestazioni del traffico personalizzato contro il controllo del traffico a tale controllo.

Le opzioni per l'impostazione di un controllo nelle attività AP e AT sono leggermente diverse da quelle di altri tipi di attività. In un test A/B manuale, potete modificare il tipo di controllo che mostra il vostro controllo e l'incremento è calcolato in base al tasso di conversione dell'esperienza di controllo. Potete effettuare questa modifica facilmente perché il traffico viene distribuito in modo casuale a ogni esperienza inclusa nell'attività, indipendentemente dal tipo iniziale di cui il controllo è stato impostato. In altre parole, la selezione del controllo non influisce sulle modalità di erogazione del traffico. Nelle attività AP e AT, la decisione su cosa scegliere in quanto controllo influisce su come viene distribuito il traffico dei visitatori. Di conseguenza, è necessario considerare più attentamente la decisione.

Sono disponibili due opzioni per il controllo nelle attività AP e AT: esperienze servite in modo casuale o un'esperienza specifica.

* **Servita in modo casuale**: Per un controllo casuale, la percentuale di controllo del traffico fornisce in modo casuale tutte le esperienze nell'attività, senza considerare il profilo del visitatore. Potete considerare il controllo come aiutare a rispondere alla domanda, «Se è sufficiente distribuire un'esperienza (o offerta) ai visitatori e non prendere in considerazione i loro profili, qual è il tasso di conversione per quell'esperienza (o offerta)? »» Il controllo è simile a un test A/B nell'attività AI. Avere queste informazioni sul tasso di conversione non personalizzato per ogni esperienza o offerta può essere utile per comprendere quando analizzare i risultati dell'attività.

* **Esperienza specifica**: Un controllo specifico delle esperienze consente di confrontare il traffico gestito dai modelli di personalizzazione di Target a una specifica esperienza definita dall'esperto di marketing (ad esempio, la pagina iniziale predefinita). Con questa opzione, la percentuale di controllo del traffico fornisce il traffico in modo casuale solo per quell'esperienza.

## Specifica di un'esperienza specifica come controllo

1. While creating an [AP activity](/help/c-activities/t-automated-personalization/create-ap-activity.md) or [AT activity](/help/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), configure the experiences as desired.
1. On the [!UICONTROL Targeting] page (step 2 of the three-part guided workflow), select the desired experience as the control.
1. Specificate l'allocazione del traffico per l'esperienza di controllo e le altre esperienze.

   Per un controllo delle esperienze specifico, si consiglia 10% a 30%.

1. Continue with the [!UICONTROL Goals &amp; Settings] page.

## Limitazioni e considerazioni noti

Considerate quanto segue quando utilizzate un'esperienza specifica come controllo:

* Non è consigliabile modificare l'esperienza di controllo in un'attività già live. L'ultima esperienza di controllo selezionata è denominata in reporting (anche se i rapporti precedenti sono basati su un'altra esperienza).
* Non si consiglia di eliminare l'esperienza di controllo.
* L'aggiunta di un numero elevato di nuove offerte/esperienze a un'attività live con un'esperienza specifica, in quanto il controllo non viene consigliato.
* Nelle attività AP, incluso il targeting sull'esperienza di controllo che potrebbe vincolare ulteriormente chi può vedere che l'esperienza non è consigliata.
* In AP activities, lift and confidence information is *NOT* available in the offer-level report if a specific experience is selected. Le informazioni Lift (Incremento) e confidence (confidenza) sono disponibili al livello di traffico "targeting" e "control" complessivo per l'attività AP. Le informazioni relative a incremento e confidenza sono disponibili se è selezionato "casuale" come controllo. In questo modo, il confronto tra il tasso di conversione di un'esperienza specifico e il tasso di conversione di un'offerta non è logico a causa della differenza in unità. Le informazioni disponibili in un'attività AT sono uguali, indipendentemente dal tipo di controllo selezionato.
* Poiché tutto il traffico passa a un'unica esperienza o a un set di offerte quando selezionate l'esperienza come controllo (rispetto a casuale, dove l'importo del traffico è suddiviso sul numero di esperienze o offerte nell'attività), in genere non avete bisogno di un traffico per passare al controllo. 10% è un buon punto di partenza.
* Se effettuate una delle seguenti operazioni a un'attività live con un'esperienza specifica come controllo, il controllo viene reimpostato automaticamente su esperienze servite casualmente (invece dell'esperienza specifica selezionata in precedenza):

   * Eliminare un'esperienza
   * Rimuovere una posizione o un'offerta (solo AP)
   * Escludere un'esperienza, manualmente, rimuovendo le offerte duplicate o tramite un gruppo di esclusione (solo AP)

