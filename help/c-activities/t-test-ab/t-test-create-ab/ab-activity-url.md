---
keywords: url attività;url;url diverso
description: Scoprite come specificare l'URL attività che determina la pagina utilizzata nel test e che si apre quando il test viene progettato utilizzando  Adobe Target.
title: Cos'è l'URL attività in un'attività A/B?
feature: A/B Tests
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 73%

---


# URL attività

L&#39;URL attività determina la pagina utilizzata nel test e che si apre quando il test viene progettato utilizzando  Adobe Target.

Quando viene richiesto durante la creazione dell’attività, specifica l’URL attività. Digita l’URL completo (comprensivo di `https://`), quindi fai clic su **[!UICONTROL Crea]**.

>[!NOTE]
>
>[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `http://www.adobe.com`] e [!DNL `https://www.adobe.com`] sono entrambi validi.

## Specificare un URL diverso

Per impostazione predefinita, in [!UICONTROL Visual Experience Composer (Compositore esperienza visivo)] viene aperta la pagina specificata nelle impostazioni di [Visual Experience Composer (Compositore esperienza visivo)](/help/administrating-target/visual-experience-composer-set-up.md)
. È possibile specificare una pagina diversa durante la creazione dell’attività.

Per visualizzare una pagina diversa dopo l’apertura del [!UICONTROL Compositore esperienza visivo], fai clic sull’icona a forma di ingranaggio **[!UICONTROL Configura]**, quindi seleziona **[!UICONTROL Consegna pagine]**. Immetti l’URL nel campo URL attività.

![Finestra di dialogo Consegna pagine](/help/c-activities/t-test-ab/t-test-create-ab/assets/url-config-new.png)

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
>Se hai inserito un URL per un sito che non include il codice JavaScript di [!DNL Target] Standard, non puoi selezionare elementi di pagina.

Per impostazione predefinita, il [!UICONTROL Compositore esperienza visivo] non consente di modificare gli elementi contenenti JavaScript, ad esempio i banner rotanti. Puoi disattivare **[!UICONTROL Esegui rendering con JavaScript]** se desideri modificare tali elementi utilizzando il [!UICONTROL Compositore esperienza visivo].

>[!NOTE]
>
>Se modifichi l’URL dopo aver apportato modifiche a una pagina per una o più esperienze, l’esperienza viene reimpostata utilizzando la nuova pagina e le modifiche apportate andranno perse.
