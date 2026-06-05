---
keywords: Test multivariati;URL attività
description: Scopri come specificare l'URL attività che determina la pagina utilizzata nel test e che viene visualizzata quando l'attività [!UICONTROL Test multivariato] è progettata utilizzando [!DNL Adobe Target].
title: Qual è l'URL attività in un'attività [!UICONTROL Test multivariato] (MVT)?
feature: Multivariate Tests
exl-id: 336169ae-7c8b-4fd5-9b1c-0bd3e9524425
source-git-commit: 8f9c0ea65197fd639d463628e54db79db993c2da
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 45%

---

# URL attività

L&#39;URL attività determina la pagina utilizzata nel [!UICONTROL test multivariato] (MVT) e che viene visualizzata quando il test è progettato in [!DNL Adobe Target].

Quando viene richiesto durante la [creazione dell’attività](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md), specifica l’URL attività. Digitare l&#39;URL completo (incluso `https://`), quindi fare clic su **[!UICONTROL Avanti]**.

>[!NOTE]
>
>[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `https://www.adobe.com`] e [!DNL `http://www.adobe.com`] corrispondono entrambi.

Per impostazione predefinita, il [!UICONTROL Compositore esperienza visivo] (VEC) apre la pagina specificata nelle [impostazioni del Compositore esperienza visivo](/help/main/administrating-target/visual-experience-composer-set-up.md). È possibile specificare una pagina diversa durante la creazione dell’attività.

Per visualizzare una pagina diversa dopo l&#39;apertura del Compositore esperienza visivo, fai clic sull&#39;icona **[!UICONTROL Configura]**, seleziona **[!UICONTROL Consegna pagine]**, quindi specifica l&#39;URL.

![Finestra di dialogo Consegna pagine](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/url-config.png)

Fai clic su **[!UICONTROL Aggiungi regola modello]** per aggiungere più pagine o sezioni all’attività.

Le regole aggiuntive possono essere basate su uno dei seguenti elementi:

* URL
* Dominio
* Percorso
* Frammento hash (#)
* Query
* Parametro

È possibile unire ulteriori regole all’URL attività con AND o OR. Tutte le regole aggiunte vengono valutate l&#39;una rispetto all&#39;altra mediante l&#39;operatore AND.

Al termine, fai clic su **[!UICONTROL Salva]**.

>[!NOTE]
>
>Se è stato immesso un URL per un sito che non include il codice JavaScript [!DNL Target], non è possibile selezionare elementi di pagina.

Per impostazione predefinita, il Compositore esperienza visivo non consente di modificare gli elementi contenenti JavaScript, ad esempio i banner rotanti. Puoi disattivare **[!UICONTROL Esegui rendering con JavaScript]** se desideri modificare tali elementi utilizzando il [!UICONTROL Compositore esperienza visivo].

>[!NOTE]
>
>Se modifichi l’URL dopo aver apportato modifiche a una pagina per una o più esperienze, l’esperienza viene reimpostata utilizzando la nuova pagina e le modifiche apportate andranno perse.
