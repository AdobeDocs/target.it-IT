---
keywords: esperienza;json;aem;adobe experience manager;esportare in adobe target;frammenti di contenuto;frammenti;CF;cf
description: Scopri come utilizzare [!DNL Adobe Experience Manager] [!UICONTROL Frammenti di contenuto] in [!DNL Adobe Target] attività.
title: Come si utilizza [!DNL Adobe Experience Manager] (AEM) [!UICONTROL Frammenti di contenuto]?
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip="What are Target Beta release features?"
feature: Integrations
source-git-commit: cbbaea46460b298cbff5015fcf60c37a8aff7751
workflow-type: tm+mt
source-wordcount: '748'
ht-degree: 4%

---

# AEM [!UICONTROL Frammenti di contenuto]

Utilizzo [!UICONTROL Frammenti di contenuto] (CF) creati in [!DNL Adobe Experience Manager] AEM [!DNL Target] attività per facilitare l’ottimizzazione o la personalizzazione.

>[!NOTE]
>
>Questa funzione verrà rilasciata il 6 aprile 2023.


>[!NOTE]
>
>Quando lavori con AEM, considera quanto segue [!UICONTROL Frammenti di contenuto] in [!DNL Target]:
> 
>* Questa funzione richiede che [!DNL Adobe Experience Manager] (AEM) cliente. Per ulteriori informazioni, consulta [Requisiti](#section_AE6F0971E1574B3AA324003599B96E5A) sotto.
>
>* Questa funzione è disponibile per i seguenti tipi di attività: [!UICONTROL Test A/B], [!UICONTROL Allocazione automatica], [!UICONTROL Targeting automatico], [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Targeting esperienza] (XT). Questa funzione non è disponibile in [!UICONTROL Test multivariato] (MVT) e [!UICONTROL Recommendations] attività.
>
>* Puoi consumare [!UICONTROL Frammenti di contenuto] in [!DNL Target] attività che utilizzano [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md) solo. Non puoi consumare [!UICONTROL Frammenti di contenuto] utilizzando [!UICONTROL Compositore esperienza visivo] (Compositore esperienza visivo).


Per saperne di più su AEM [!UICONTROL Frammenti di contenuto] e [!UICONTROL Frammenti esperienza], vedi [AEM [!UICONTROL Frammenti esperienza] e [!UICONTROL Frammenti di contenuto] panoramica](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Requisiti {#requirements}

È necessario effettuare il provisioning con il [!UICONTROL Frammenti di contenuto] funzionalità di [!DNL Target]. Inoltre, devi utilizzare [!DNL AEM] as a Cloud Service. Il rappresentante del tuo account può aiutarti a rispettare i requisiti per utilizzare questa funzione:

Per abilitare l’integrazione e ottenere i dettagli di autenticazione, contatta l’[Assistenza clienti per Adobe Target](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Configurazione e utilizzo [!UICONTROL Frammenti di contenuto] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Per esportare [!UICONTROL Frammenti di contenuto] per utilizzare in [!DNL Target] attività, devi eseguire alcuni passaggi preliminari in AEM. Per ulteriori informazioni, consulta [Esportazione di frammenti di contenuto in Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/content-fragments-target.html){target=_blank} in *Experience Manager di documentazione as a Cloud Service*. Questo collegamento sarà disponibile il giorno della versione (6 aprile 2023)

Per informazioni sulla progettazione, la creazione, la cura e la pubblicazione [!UICONTROL Frammenti di contenuto], vedi [[!UICONTROL Frammenti di contenuto]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/content-fragments.html?lang=en){target=_blank} and [Working with Content Fragments](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments.html){target=_blank} in the [Experience Manager as a Cloud Service documentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/home.html){target=_blank}.

## Utilizzo [!UICONTROL Frammenti di contenuto] in [!DNL Target] attività {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Dopo aver eseguito le attività precedenti, la [!UICONTROL Frammento di contenuto] viene visualizzato sul [!UICONTROL Offerte] in [!DNL Target].

[!DNL Target] cerca attualmente [!UICONTROL Frammenti di contenuto] per importare ogni dieci minuti. Importazione [!UICONTROL Frammento di contenuto] devono essere disponibili in [!DNL Target] entro dieci minuti, ma questo intervallo di tempo dovrebbe accorciarsi andando avanti.

La [!UICONTROL Frammento di contenuto] viene importato in [!DNL Target] come offerta JSON. che [!UICONTROL Frammento di contenuto] La versione &quot;principale&quot; rimane in [!DNL AEM]. Non è possibile modificare il [!UICONTROL Frammento di contenuto] in [!DNL Target].

Puoi filtrare ed eseguire ricerche per [!UICONTROL XF di HTML], [!UICONTROL XF JSON]e [!UICONTROL Frammenti di contenuto] per distinguere tra diversi tipi di offerte esportati in [!DNL Target].

![Filtrare per tipi di frammento di contenuto: HTML o JSON nell’interfaccia utente di Target](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

Puoi passare il cursore sopra un [!UICONTROL Frammento di contenuto] nell’elenco, quindi fai clic su [!UICONTROL Visualizza] icona ![Icona Info](/help/main/c-integrating-target-with-mac/aem/assets/icon-info.png) per visualizzare informazioni aggiuntive sul [!UICONTROL Frammento di contenuto], compresi i [!UICONTROL AEM] e [!UICONTROL Collegamento profondo AEM]. Fai clic sul pulsante [!UICONTROL Utilizzo dell’offerta] per visualizzare le attività che fanno riferimento a questa offerta.

![Informazioni a comparsa sui frammenti di contenuto](/help/main/c-integrating-target-with-mac/aem/assets/cf-info-popup.png)

Puoi consumare [!UICONTROL Frammenti di contenuto] in [!DNL Target] attività che utilizzano [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md) solo. You *impossibile* consumare [!UICONTROL Frammenti di contenuto] in [!DNL Target] attività che utilizzano [Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (Compositore esperienza visivo). [!UICONTROL Frammenti di contenuto] vengono esportati come JSON in [!DNL Target] e non può essere utilizzato nelle attività create utilizzando il Compositore esperienza visivo.

>[!TIP]
>
>Utilizzare intelligenza artificiale, apprendimento automatico e consigli con [!UICONTROL Frammenti di contenuto]:
>
>* Per utilizzare completamente le [!DNL Target] Funzionalità AI e ML, puoi selezionare [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) o [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) durante la creazione di un test A/B.
>
>* [!UICONTROL Frammenti di contenuto] non sono supportati in [!DNL Recommendations] attività. Tuttavia, da utilizzare [!UICONTROL Frammenti di contenuto] per i consigli è possibile creare un [!UICONTROL Test A/B] attività [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico]) o un [!UICONTROL Targeting esperienza] (XT) e [includere consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md).


**Per consumare [!UICONTROL Frammenti di contenuto] utilizzando [!UICONTROL Compositore esperienza basato su moduli]:**

1. In [!DNL Target], durante la creazione o la modifica di un’esperienza nel [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E), seleziona la posizione nella pagina in cui desideri inserire [!DNL AEM] contenuto, quindi seleziona **[!UICONTROL Modifica frammento di contenuto]** per visualizzare [!UICONTROL Scegliere un frammento di contenuto] elenco.

   ![immagine content_fragment_list](/help/main/c-integrating-target-with-mac/aem/assets/choose-content-fragment.png)

   La [!UICONTROL Frammento di contenuto] visualizza il contenuto creato in [!DNL AEM] che ora è disponibile in modo nativo da [!DNL Target].

1. Seleziona il [!UICONTROL Frammento di contenuto], quindi fai clic su **[!UICONTROL Salva]**.
1. Termina la configurazione dell’attività.

## Considerazioni {#considerations}

* [!DNL Target] cerca attualmente [!UICONTROL Frammenti di contenuto] per importare ogni dieci minuti. Importazione [!UICONTROL Frammento di contenuto] devono essere disponibili in [!DNL Target] entro dieci minuti, ma questo intervallo di tempo dovrebbe accorciarsi andando avanti.
* La [!UICONTROL Frammento di contenuto] viene importato in [!DNL Target] come offerta JSON. La [!UICONTROL Frammento di contenuto] La versione &quot;principale&quot; rimane in [!DNL AEM]. Non è possibile modificare il [!UICONTROL Frammento di contenuto] in [!DNL Target].
* Non è possibile creare [!UICONTROL Frammenti di contenuto] utilizzo [!DNL Adobe I/O]. Crea [!UICONTROL Frammenti di contenuto] utilizzando AEM, come spiegato in precedenza.
* Se aggiorni il tuo [!UICONTROL Frammento di contenuto] in AEM [!UICONTROL Frammento di contenuto] devono essere pubblicati ed esportati in [!DNL Target] di nuovo [!DNL Target] può utilizzare le modifiche più recenti.