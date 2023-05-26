---
keywords: url attività;url;url diverso
description: Scopri come specificare l’URL attività che determina la pagina utilizzata nel test e che viene visualizzata quando il test viene progettato utilizzando Adobe Target.
title: Qual è l’URL attività in un’attività A/B?
feature: A/B Tests
exl-id: 7482ae10-fb7e-42ba-9ea0-97b82ed85bff
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 73%

---

# URL attività

L’URL attività determina la pagina utilizzata nel test e che viene visualizzata quando il test viene progettato utilizzando Adobe Target.

Quando viene richiesto durante la creazione dell’attività, specifica l’URL attività. Digita l’URL completo (comprensivo di `https://`), quindi fai clic su **[!UICONTROL Crea]**.

>[!NOTE]
>
>[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `http://www.adobe.com`] e [!DNL `https://www.adobe.com`] sono entrambi validi.

## Specificare un URL diverso

Per impostazione predefinita, il [!UICONTROL Compositore esperienza visivo] apre la pagina specificata nel [Impostazioni del Compositore esperienza visivo](/help/main/administrating-target/visual-experience-composer-set-up.md)
. È possibile specificare una pagina diversa durante la creazione dell’attività.

Per visualizzare una pagina diversa dopo l’apertura del [!UICONTROL Compositore esperienza visivo], fai clic sull’icona a forma di ingranaggio **[!UICONTROL Configura]**, quindi seleziona **[!UICONTROL Consegna pagine]**. Immetti l’URL nel campo URL attività.

![Finestra di dialogo Consegna pagine](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/url-config-new.png)

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
