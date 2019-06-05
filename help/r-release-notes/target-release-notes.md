---
description: Queste note sulla versione contengono informazioni su funzioni, miglioramenti, correzioni di problemi e problemi noti per le versioni più recenti o in arrivo di Target.
keywords: note sulla versione
seo-description: Queste note sulla versione contengono informazioni su funzioni, miglioramenti, correzioni di problemi e problemi noti per le versioni più recenti o in arrivo di Adobe Target
seo-title: Note sulla versione di Target (pre-rilascio)
solution: Target
title: Note sulla versione di Target (pre-rilascio)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: aa2b6ec39ef0fa3effad74617235b003972859ec

---


# Note sulla versione di Target (pre-rilascio){#target-release-notes-prerelease}

Queste note sulla versione contengono informazioni su funzioni, miglioramenti e correzioni per le versioni più recenti o in arrivo di [!DNL Adobe Target].

**Ultimo aggiornamento: 28 maggio 2019**

>[!NOTE]
>
>Queste sulla versione contengono delle informazioni in anteprima. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti. Per visualizzare le informazioni sulla versione corrente, vedi [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali o possono essere diverse, a seconda della tempistica delle release.

## Target Standard/Premium 19.6.1 (25 giugno 2019) {#tgt-19-6-1}

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Compositore esperienza visivo | Quando fate clic su un elemento di pagina nella VEC, un menu mostra le opzioni disponibili per tale tipo di elemento. <ul><li>Ora potete utilizzare [!DNL Styles > Background] l&#39;opzione per cambiare l&#39;immagine di sfondo e il colore dell&#39;elemento selezionato. (TGT-15001)</li><li>Quando fate clic su un&#39;immagine, [!DNL Replace With]vengono visualizzate due nuove opzioni: [!DNL HTML] e [frammento esperienza](/help/c-experiences/c-manage-content/aem-experience-fragments.md).<br> La sostituzione di un&#39;immagine con HTML offre un controllo completo dell&#39;elemento, senza necessità di selezionare l&#39;elemento principale per accedere all&#39;opzione HTML.<br>I frammenti esperienza consentono di inserire rapidamente gli elementi creati in Adobe Experience Manager (AEM) nelle attivazioni di Target. (TGT-34097)</li></ul>È stata migliorata la procedura per configurare il monitoraggio dei clic all&#39;interno della VEC e del VEC applicazione singola.<br>Quando selezionate gli elementi da usare nel tracciamento dei clic, i nomi di tutti gli elementi disponibili vengono visualizzati nel pannello Modifiche a destra, rendendo più facile e veloce selezionare gli elementi desiderati.<br>La [!DNL Goals & Settings] pagina del flusso di lavoro attività guidato in tre parti visualizza un numero che rappresenta il numero di elementi selezionati per il tracciamento dei clic. Potete passare il cursore sopra questo numero per visualizzare i nomi di tutti gli elementi selezionati. (TGT-33878) |
| App singola (SPA) Visual Experience Composer (Compositore esperienza singola) | La VEC include i seguenti miglioramenti:<ul><li>Un nuovo flusso di lavoro guidato consente di comprendere in che modo le impostazioni della regola di consegna pagina devono essere configurate per eseguire ed eseguire un&#39;attività per l&#39;app singola pagina. (TGT-33718)</li><li>Ora potete definire una modifica utilizzando la VEC di SPA e quindi clonarla per utilizzarla in altre viste nell&#39;app pagina singola. (TGT-33882)</li></ul> |
| Mobile Visual Experience Composer (VEC) | Ora puoi creare attività per più versioni della tua app mobile. In questo modo potrete risparmiare tempo e fatica quando le versioni sono molto simili e non dovete modificare in modo significativo l&#39;interfaccia utente dell&#39;app. (TGT-34231) |
| ![Attività Premium badgeautomated](/help/assets/premium.png)<br>Personalization (Personalizzazione automatizzata) e Auto-Target (Target automatico): esperienza specifica come controllo | È possibile selezionare un’esperienza da utilizzare come controllo durante la creazione di un’attività AP o Target automatico. Questa funzione consente di indirizzare l&#39;intero traffico di controllo a un&#39;esperienza specifica, in base alla percentuale di allocazione del traffico configurata nell&#39;attività. Potete quindi valutare i rapporti sulle prestazioni del traffico personalizzato contro il controllo del traffico verso quella singola esperienza. L&#39;opzione di controllo corrente (in modo casuale) continuerà a essere disponibile. (TGT-32801 e TGT-26572) |

### Miglioramenti, correzioni e modifiche

* Il `<BODY>` tag ora viene visualizzato nel percorso DOM visualizzato nella parte inferiore della VEC quando si fa clic su un elemento della pagina, consentendo di eseguire azioni sul `<BODY>` tag. (TGT-33736)

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche anticipate sui miglioramenti dei prodotti in arrivo a Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
