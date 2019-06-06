---
description: Queste note sulla versione contengono informazioni su funzioni, miglioramenti, correzioni di problemi e problemi noti per le versioni più recenti o in arrivo di Target.
keywords: note sulla versione
seo-description: Queste note sulla versione contengono informazioni su funzioni, miglioramenti, correzioni di problemi e problemi noti per le versioni più recenti o in arrivo di Adobe Target
seo-title: Note di rilascio di Adobe Target (prerelease)
solution: Target
title: Note sulla versione di Target (prerelease)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 3a498a99e333acc92651eb94592af87cfc34c6e1

---


# Note sulla versione di Target (prerelease){#target-release-notes-prerelease}

Queste note sulla versione contengono informazioni su funzioni, miglioramenti e correzioni per le versioni più recenti o in arrivo di [!DNL Adobe Target].

**Ultimo aggiornamento: 6 giugno 2019**

>[!NOTE]
>
>Queste note sulla versione contengono delle informazioni in anteprima. Le date di rilascio, le funzioni e altre informazioni sono soggette a modifiche senza preavviso. Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali o possono essere diverse, a seconda della tempistica delle release.
>
>I numeri del problema tra parentesi [!DNL Adobe] sono a scopo interno.

## Target Standard/Premium 19.6.1 (25 giugno 2019) {#tgt-19-6-1}

Questa versione include le seguenti nuove funzionalità e miglioramenti:

### Compositore esperienza visivo

* **Nuove opzioni del menu VEC**: Quando fate clic su un elemento di pagina nella VEC, un menu mostra le opzioni disponibili per tale tipo di elemento.

   * **Stili &gt; Sfondo**: È ora possibile utilizzare l&#39;opzione [!UICONTROL Stili &gt; Sfondo] per modificare l&#39;immagine di sfondo e il colore dell&#39;elemento selezionato. (TGT-15001)

   * **[!UICONTROL Sostituisci con &gt; HTML]e[!UICONTROL Sostituisci con &gt; Frammento esperienza]**: Quando fate clic su un&#39;immagine e quindi su [!UICONTROL Sostituisci con], vengono visualizzate due nuove opzioni:

      * **HTML**: Potete sostituire un&#39;immagine con HTML per fornire un controllo completo dell&#39;elemento senza necessità di selezionare l&#39;elemento principale per accedere all&#39;opzione HTML.
      * **Frammento esperienza**: Puoi sostituire un&#39;immagine con un frammento [esperienza di Adobe Experience Manager (AEM)](/help/c-experiences/c-manage-content/aem-experience-fragments.md) per inserire rapidamente gli elementi creati in AEM in attività Target. (TGT-34097)

* **Miglioramenti del monitoraggio dei clic**: È stata migliorata la procedura per configurare il monitoraggio dei clic all&#39;interno della VEC e della VEC (Single Page Application).

   * Quando selezionate gli elementi da usare nel tracciamento dei clic, i nomi di tutti gli elementi disponibili vengono visualizzati nel pannello Modifiche a destra, rendendo più facile e veloce selezionare gli elementi desiderati.
   * La [!UICONTROL pagina Goals &amp; Settings] (Obiettivi e impostazioni) del flusso di lavoro Attività guidato in tre parti visualizza un numero che rappresenta il numero di elementi selezionati per il tracciamento dei clic. Potete passare il cursore sopra questo numero per visualizzare i nomi di tutti gli elementi selezionati. (TGT-33878)

### SPA VEC

* **Flusso di lavoro guidato**: Un nuovo flusso di lavoro guidato consente di comprendere in che modo le impostazioni della regola di consegna pagina devono essere configurate per eseguire ed eseguire un&#39;attività per l&#39;app singola pagina. (TGT-33718)

* **Modifiche clone**: Ora potete definire una modifica utilizzando la VEC di SPA e quindi clonarla per utilizzarla in altre viste nell&#39;app pagina singola. (TGT-33882)

### VEC Mobile

* **Più versioni app**: Ora puoi creare attività per più versioni della tua app mobile. In questo modo potrete risparmiare tempo e fatica quando le versioni sono simili e non dovete modificare in modo significativo l&#39;interfaccia utente dell&#39;app. (TGT-34231)

### Badge Automated Personalization (Personalizzazione automatizzata) &amp; Auto-Target ![Premium](/help/assets/premium.png)

* **Esperienza specifica come controllo**: Potete selezionare un&#39;esperienza da utilizzare come controllo durante la creazione di un&#39;attività AP o Auto-Target. Questa funzione consente di indirizzare l&#39;intero traffico di controllo a un&#39;esperienza specifica, in base alla percentuale di allocazione del traffico configurata nell&#39;attività. Potete quindi valutare i rapporti sulle prestazioni del traffico personalizzato contro il controllo del traffico verso quella singola esperienza. L&#39;opzione di controllo corrente (in modo casuale) continuerà a essere disponibile. (TGT-32801 e TGT-26572)

### Altri miglioramenti, correzioni e modifiche

* Il `<BODY>` tag ora viene visualizzato nel percorso DOM visualizzato nella parte inferiore della VEC quando si fa clic su un elemento della pagina, consentendo di eseguire azioni sul `<BODY>` tag. (TGT-33736)

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
