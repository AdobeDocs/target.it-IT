---
description: LʼURL attività determina la pagina utilizzata nel test, visualizzata quando il test viene progettato.
keywords: Targeting
seo-description: LʼURL attività determina la pagina utilizzata nel test, visualizzata quando il test viene progettato.
seo-title: URL attività
solution: Target
title: URL attività
uuid: 970de8ba-ab60-4339-866b-27889bec67f9
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# URL attività{#activity-url}

LʼURL attività determina la pagina utilizzata nel test, visualizzata quando il test viene progettato.

Quando viene richiesto durante la creazione dell’attività, specifica l’URL attività. Digita l’URL completo (comprensivo di `https://`), quindi fai clic su **[!UICONTROL Crea attività]**.

>[!NOTE]
>
>[!DNL Target] non distingue tra protocolli URL ( [!DNL https] e [!DNL http]). Di conseguenza, [!DNL `https://www.adobe.com`] e [!DNL `http://www.adobe.com`] sono entrambi validi.

Per impostazione predefinita, il Compositore esperienza visivo apre la pagina specificata nelle preferenze dell’account. È possibile specificare una pagina diversa durante la creazione dell’attività.

Per visualizzare una pagina diversa dopo lʼapertura del Compositore esperienza visivo, fai clic su **[!UICONTROL Configura]** e seleziona **[!UICONTROL URL]**, quindi immetti lʼURL nella casella URL attività.

![](assets/url-config.png)

Fai clic su **[!UICONTROL Aggiungi regola modello]** per aggiungere più pagine o sezioni all’attività.

Le regole aggiuntive possono essere basate su uno dei seguenti elementi:

* URL
* Dominio
* Percorso
* Frammento hash (#)
* Query
* Parametro mbox

È possibile aggiungere altre regole all’URL attività mediante l’operatore E oppure O. Tutte le regole aggiunte vengono valutate tra loro con E.

Al termine, fai clic su **[!UICONTROL Salva]**.

>[!NOTE]
>
>Se hai inserito un URL per un sito che non include il codice JavaScript di Target Standard, non puoi selezionare elementi di pagina.

Per impostazione predefinita, il [!UICONTROL Compositore esperienza visivo] non consente di modificare gli elementi contenenti JavaScript, ad esempio i banner rotanti. Puoi disattivare **[!UICONTROL Esegui rendering con JavaScript]** se desideri modificare tali elementi utilizzando il [!UICONTROL Compositore esperienza visivo].

>[!NOTE]
>
>Se modifichi l’URL dopo aver apportato modifiche a una pagina per una o più esperienze, l’esperienza viene reimpostata utilizzando la nuova pagina e le modifiche apportate andranno perse.
