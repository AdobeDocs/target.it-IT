---
description: L’URL attività determina la pagina utilizzata nel test e che viene visualizzata quando il test è generato.
keywords: Panoramica e riferimento
seo-description: L’URL attività determina la pagina utilizzata nel test e che viene visualizzata quando il test è generato.
seo-title: URL attività
solution: Target
title: URL attività
topic: Standard
uuid: 65489969-d548-4286-858f-8420120317c0
translation-type: tm+mt
source-git-commit: 9137bbae24c6deef70a5b82fbe7bbd0a2dee9745

---


# URL attività{#activity-url}

L’URL attività determina la pagina utilizzata nel test e che viene visualizzata quando il test è generato.

Quando viene richiesto durante la creazione dell’attività, specifica l’URL attività. Digita l’URL completo (comprensivo di `https://`), quindi fai clic su **[!UICONTROL Crea]**.

>[!NOTE]
>
>[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `http://www.adobe.com`] e [!DNL `https://www.adobe.com`] sono entrambi validi.

## Specificate un URL diverso

Per impostazione predefinita [!UICONTROL , in Visual Experience Composer] (Compositore esperienza visivo) viene aperta la pagina specificata nelle Preferenze account [di Target](/help/administrating-target/r-target-account-preferences/target-account-preferences.md). È possibile specificare una pagina diversa durante la creazione dell’attività.

Per visualizzare una pagina diversa dopo l’apertura del [!UICONTROL Compositore esperienza visivo], fai clic sull’icona a forma di ingranaggio **[!UICONTROL Configura]**, quindi seleziona **[!UICONTROL Consegna pagine]**. Immetti l’URL nel campo URL attività.

![Consegna pagina, finestra di dialogo](/help/c-activities/t-test-ab/t-test-create-ab/assets/url-config-new.png)

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
