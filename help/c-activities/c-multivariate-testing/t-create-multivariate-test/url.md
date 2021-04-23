---
keywords: Test multivariati;URL attività
description: Scopri come specificare l’URL attività che determina la pagina utilizzata nel test e che viene visualizzata quando l’attività Test multivariato è progettata utilizzando Adobe Target.
title: Cos’è l’URL attività in un’attività multivariato (MVT)?
feature: Test multivariati
exl-id: 336169ae-7c8b-4fd5-9b1c-0bd3e9524425
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 78%

---

# URL attività

L’URL attività determina la pagina utilizzata nel [!UICONTROL test multivariato] (MVT) e che viene visualizzata quando il test è progettato in [!DNL Adobe Target].

Quando viene richiesto durante la [creazione dell’attività](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md), specifica l’URL attività. Digita l’URL completo (comprensivo di `https://`), quindi fai clic su **[!UICONTROL Successivo]**.

>[!NOTE]
>
>[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `https://www.adobe.com`] e [!DNL `http://www.adobe.com`] sono entrambi validi.

Per impostazione predefinita, il [!UICONTROL Compositore esperienza visivo] (VEC) apre la pagina specificata nelle [impostazioni del Compositore esperienza visivo](/help/administrating-target/visual-experience-composer-set-up.md). È possibile specificare una pagina diversa durante la creazione dell’attività.

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
