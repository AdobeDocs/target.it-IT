---
keywords: profilo visitatore;targeting profilo visitatore
description: Scopri come creare tipi di pubblico in Adobe [!DNL Target] per rivolgerti ai visitatori che soddisfano parametri di profilo specifici come visitatori nuovi o di ritorno, affinità tra categorie e altro ancora.
title: Posso [!DNL Target] Visitatori che soddisfano parametri di profilo specifici?
feature: Tipi di pubblico
exl-id: aca45b80-660d-4b8e-a0d7-84627b8fd77b
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 83%

---

# Profilo visitatore

Crea tipi di pubblico per rivolgerti ai visitatori che soddisfano parametri di profilo specifici.

1. Nell’interfaccia di [!DNL Target] fai clic su **[!UICONTROL Pubblico]** > **[!UICONTROL Crea pubblico]**.
1. Dai un nome al pubblico.
1. Fai clic su **[!UICONTROL Aggiungi regola]** > **[!UICONTROL Profilo visitatore]**.

   ![](assets/target_visitor_profile.png)

1. Fai clic su **[!UICONTROL Seleziona]**, quindi scegli una delle seguenti opzioni:

   I parametri del profilo del visitatore vengono trasmessi tramite mbox (profilo). Puoi eseguire il targeting dei visitatori nuovi o di ritorno, o includere tutti gli utenti.

   * Nuovo visitatore
   * Visitatore di ritorno
   * In altri test
   * Non in altri test
   * Prima pagina della sessione
   * Non la prima pagina della sessione
   * Affinità tra categorie

   Un profilo visitatore viene creato nella memoria Edge locale per ogni chiamata mbox con nuovo `mboxPC`. Dopo 30 minuti di inattività, il profilo viene salvato nel database di Target ed è accessibile da altri Edge.

   Quando un visitatore del sito accede a metà sessione e ottiene un `3rdpartyId`, tutti gli attributi di profilo precedentemente caricati associati a tale `3rdPartyId` sono immediatamente disponibili.

   Puoi eseguire il targeting di parametri di profilo personalizzati e parametri `user.`. Scegli il parametro che desideri utilizzare per eseguire il targeting dell’attività. Se il parametro desiderato non viene visualizzato, significa che non è stato attivato da una mbox.

1. (Facoltativo) Fai clic su **[!UICONTROL Aggiungi regola]** per impostare regole aggiuntive per il pubblico.
1. Fai clic su **[!UICONTROL Salva]**.

## Video di formazione: Creazione di tipi di pubblico ![Badge panoramica](/help/assets/overview.png)

Questo video contiene informazioni sull&#39;utilizzo delle categorie di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392)
