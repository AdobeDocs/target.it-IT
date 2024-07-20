---
keywords: profilo visitatore;targeting profilo visitatore
description: Scopri come creare tipi di pubblico in [!DNL Adobe Target] per eseguire il targeting dei visitatori che soddisfano parametri di profilo specifici, come visitatori nuovi o di ritorno, affinità tra categorie e altro ancora.
title: Posso Eseguire Il Targeting Di Visitatori Che Soddisfano Parametri Di Profilo Specifici?
feature: Audiences
exl-id: aca45b80-660d-4b8e-a0d7-84627b8fd77b
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 34%

---

# Profilo visitatore

Crea tipi di pubblico in [!DNL Adobe Target] per eseguire il targeting dei visitatori che soddisfano parametri di profilo specifici.

1. Nell&#39;interfaccia [!DNL Target], fare clic su **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Assegna un nome al pubblico e aggiungi una descrizione facoltativa.
1. Trascina **[!UICONTROL Visitor Profile]** nel riquadro Generatore di pubblico.

1. Fare clic su **[!UICONTROL Select]**, quindi selezionare una delle opzioni seguenti:

   ![immagine target_visitor_profile](assets/target_visitor_profile.png)

   I parametri del profilo del visitatore vengono trasmessi tramite mbox (profilo). Puoi eseguire il targeting dei visitatori nuovi o di ritorno, o includere tutti gli utenti.

   * [!UICONTROL New Visitor]
   * [!UICONTROL Returning Visitor]
   * [!UICONTROL In Other Tests]
   * [!UICONTROL Not In Other Tests]
   * [!UICONTROL First Page of Session]
   * [!UICONTROL Not First Page of Session]
   * [!UICONTROL Category Affinity]

   Un profilo visitatore viene creato nella memoria Edge locale per ogni chiamata mbox con nuovo `mboxPC`. Dopo 30 minuti di inattività, il profilo viene salvato nel database [!DNL Target] ed è accessibile da altri server Edge.

   Quando un visitatore del sito accede a metà sessione e ottiene un `3rdpartyId`, tutti gli attributi di profilo precedentemente caricati associati a `3rdPartyId` sono immediatamente disponibili.

   Puoi eseguire il targeting di parametri di profilo personalizzati e parametri `user.`. Scegli il parametro che desideri utilizzare per eseguire il targeting dell’attività. Se il parametro desiderato non viene visualizzato, significa che non è stato attivato da una mbox.

1. (Facoltativo) Imposta regole aggiuntive per il pubblico.
1. Fare clic su **[!UICONTROL Done]**.

## Video di formazione: Creazione di tipi di pubblico ![Icona panoramica](/help/main/assets/overview.png)

Questo video contiene informazioni sull&#39;utilizzo delle categorie di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392)
