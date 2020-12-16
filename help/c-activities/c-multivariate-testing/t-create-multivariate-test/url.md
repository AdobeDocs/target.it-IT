---
keywords: Targeting
description: L'URL attività determina la pagina utilizzata in un test multivariato  Adobe Target (MVT), che si apre quando il test è progettato in  Adobe Target.
title: URL attività
feature: mvt
translation-type: tm+mt
source-git-commit: c2769c0fcf7a05c10405ec855468c829aca785c0
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 84%

---


# URL attività{#activity-url}

L’URL attività determina la pagina utilizzata nel [!UICONTROL test multivariato] (MVT) e che viene visualizzata quando il test è progettato in [!DNL Adobe Target].

Quando viene richiesto durante la [creazione dell’attività](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md), specifica l’URL attività. Digita l’URL completo (comprensivo di `https://`), quindi fai clic su **[!UICONTROL Successivo]**.

>[!NOTE]
>
>[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `https://www.adobe.com`] e [!DNL `http://www.adobe.com`] sono entrambi validi.

Per impostazione predefinita, in [!UICONTROL Visual Experience Composer (Compositore esperienza visivo)] (VEC) viene aperta la pagina specificata nelle impostazioni di [Visual Experience Composer (Compositore esperienza visivo)](/help/administrating-target/visual-experience-composer-set-up.md). È possibile specificare una pagina diversa durante la creazione dell’attività.

Per visualizzare una pagina diversa dopo l’apertura del Compositore esperienza visivo, fai clic sull’icona **[!UICONTROL Configura]**, seleziona **[!UICONTROL Consegna pagine]** e specifica l’URL.

![Finestra di dialogo Consegna pagine](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/url-config.png)

Fai clic su **[!UICONTROL Aggiungi regola modello]** per aggiungere più pagine o sezioni all’attività.

Le regole aggiuntive possono essere basate su uno dei seguenti elementi:

* URL
* Dominio
* Percorso
* Frammento hash (#)
* Query
* Parametro

È possibile aggiungere altre regole all’URL attività mediante l’operatore E oppure O. Tutte le regole aggiunte vengono valutate tra loro con E.

Al termine, fai clic su **[!UICONTROL Salva]**.

>[!NOTE]
>
>Se hai inserito un URL per un sito che non include il codice JavaScript di Target Standard, non puoi selezionare elementi di pagina.

Per impostazione predefinita, il Compositore esperienza visivo non consente di modificare gli elementi contenenti JavaScript, ad esempio i banner rotanti. Puoi disattivare **[!UICONTROL Esegui rendering con JavaScript]** se desideri modificare tali elementi utilizzando il [!UICONTROL Compositore esperienza visivo].

>[!NOTE]
>
>Se modifichi l’URL dopo aver apportato modifiche a una pagina per una o più esperienze, l’esperienza viene reimpostata utilizzando la nuova pagina e le modifiche apportate andranno perse.