---
keywords: profilo visitatore;targeting profilo visitatore
description: Scopri come creare tipi di pubblico in [!DNL Adobe Target] per indirizzare l’attività ai visitatori che soddisfano parametri di profilo specifici, ad esempio visitatori nuovi o di ritorno, affinità tra categorie e altro ancora.
title: Posso Indirizzare I Visitatori Che Soddisfano Parametri Di Profilo Specifici?
feature: Audiences
exl-id: aca45b80-660d-4b8e-a0d7-84627b8fd77b
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 47%

---

# Profilo visitatore

Crea un pubblico in [!DNL Adobe Target] per indirizzare l’attività ai visitatori che soddisfano parametri di profilo specifici.

1. Nell’interfaccia di [!DNL Target] fai clic su **[!UICONTROL Pubblico]** > **[!UICONTROL Crea pubblico]**.
1. Assegna un nome al pubblico e aggiungi una descrizione facoltativa.
1. Trascinamento della selezione **[!UICONTROL Profilo visitatore]** nel riquadro audience builder (generatore di pubblico).

1. Fai clic su **[!UICONTROL Seleziona]**, quindi scegli una delle seguenti opzioni:

   ![](assets/target_visitor_profile.png)

   I parametri del profilo del visitatore vengono trasmessi tramite mbox (profilo). Puoi eseguire il targeting dei visitatori nuovi o di ritorno, o includere tutti gli utenti.

   * [!UICONTROL Nuovo visitatore]
   * [!UICONTROL Visitatore di ritorno]
   * [!UICONTROL In altri test]
   * [!UICONTROL Non in altri test]
   * [!UICONTROL Prima pagina della sessione]
   * [!UICONTROL Non la prima pagina della sessione]
   * [!UICONTROL Affinità tra categorie]

   Un profilo visitatore viene creato nella memoria Edge locale per ogni chiamata mbox con nuovo `mboxPC`. Dopo 30 minuti di inattività, il profilo viene salvato nel [!DNL Target] database ed è accessibile da altri Edge.

   Quando un visitatore del sito accede a metà sessione e ottiene un `3rdpartyId`, tutti gli attributi di profilo precedentemente caricati associati a `3rdPartyId` sono immediatamente disponibili.

   Puoi eseguire il targeting di parametri di profilo personalizzati e parametri `user.`. Scegli il parametro che desideri utilizzare per eseguire il targeting dell’attività. Se il parametro desiderato non viene visualizzato, non è stato attivato da una mbox.

1. (Facoltativo) Imposta regole aggiuntive per il pubblico.
1. Fai clic su **[!UICONTROL Fine]**.

## Video di formazione: Creazione di tipi di pubblico ![Badge panoramica](/help/main/assets/overview.png)

Questo video contiene informazioni sull&#39;utilizzo delle categorie di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392)
