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


# ![PREMIUM](/help/assets/premium.png) Utilizzo di un&#39;esperienza specifica come controllo

You can select an experience to be used as control while creating an [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) or [Auto-Target](/help/c-activities/auto-target-to-optimize.md) (AT) activity.

Questa funzione consente di indirizzare l&#39;intero traffico di controllo a un&#39;esperienza specifica, in base alla percentuale di allocazione del traffico configurata nell&#39;attività. Potete quindi valutare i rapporti sulle prestazioni del traffico personalizzato contro il controllo del traffico verso quella singola esperienza.

È inoltre disponibile l&#39;opzione di controllo per distribuire in modo casuale le esperienze.

Utilizzando un&#39;esperienza specifica come controllo, i rapporti possono aiutare a rispondere alla domanda. «L&#39;esecuzione di un&#39;attività AP/AT meglio di quanto avrei fatto?» Un vantaggio delle attività AP/AT è che potete creare più opzioni che potrebbero non essere più rilevanti per tutti gli utenti, ma essere potenti per l&#39;utente giusto. Questo significa che confrontare il nostro algoritmo con casuale non è equo; non esegui mai tutte le opzioni a tutti i visitatori del tuo sito.

## Specifica di un&#39;esperienza specifica come controllo

1. While creating an [AP activity](/help/c-activities/t-automated-personalization/create-ap-activity.md) or [AT activity](/help/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), configure the experiences as desired.
1. On the [!UICONTROL Targeting] page (step 2 of the three-part guided workflow), select the desired experience as the control.
1. Specificate l&#39;allocazione del traffico per l&#39;esperienza di controllo e le altre esperienze.
1. Continue with the [!UICONTROL Goals &amp; Settings] page.

## Limitazioni note

Di seguito sono indicati i limiti noti quando si utilizza un&#39;esperienza specifica come controllo:

* Non è consigliabile modificare l&#39;esperienza di controllo in un&#39;attività già live. L&#39;ultima esperienza di controllo selezionata è denominata in reporting (anche se i rapporti precedenti sono basati su un&#39;altra esperienza).
* Non si consiglia di eliminare l&#39;esperienza di controllo.
* Nelle attività AP, incluso il targeting sull&#39;esperienza di controllo non si consiglia di vincolare ulteriormente chi può visualizzare tale esperienza.
* In AP activities, lift and confidence information is *NOT* available in the offer-level report if a specific experience is selected. Le informazioni relative a incremento e confidenza sono disponibili se è selezionato &quot;casuale&quot; come controllo.

   Lift and confidence information *is* available at the overall &quot;targeted&quot; vs. &quot;control&quot; traffic level for the activity. In questo modo, il confronto tra il tasso di conversione di un&#39;esperienza specifico e il tasso di conversione di un&#39;offerta non è logico a causa della differenza in unità.

## Risoluzione dei problemi relativi al

In caso di problemi, prendere in considerazione i seguenti suggerimenti per la risoluzione di problemi:

* Poiché tutto il traffico passa a un&#39;unica esperienza o serie di offerte quando selezionate l&#39;esperienza come controllo (rispetto a casuale, dove l&#39;importo del traffico di controllo viene suddiviso sul numero di esperienze/offerte nell&#39;attività), in genere non avete bisogno di un traffico per passare al controllo. 10% è un buon punto di partenza.
* Se effettuate una delle operazioni seguenti a un&#39;attività live, il controllo viene reimpostato automaticamente su esperienze servite casualmente (invece dell&#39;esperienza specifica selezionata in precedenza):

   * Eliminare un&#39;esperienza
   * Rimuovere una posizione o un&#39;offerta (solo AP)
   * Escludere un&#39;esperienza, manualmente, rimuovendo le offerte duplicate o tramite un gruppo di esclusione (solo AP)
