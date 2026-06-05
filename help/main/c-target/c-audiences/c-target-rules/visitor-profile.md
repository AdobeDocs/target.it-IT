---
keywords: profilo visitatore;targeting profilo visitatore
description: Scopri come creare tipi di pubblico in [!DNL Adobe Target] per eseguire il targeting dei visitatori che soddisfano parametri di profilo specifici, come visitatori nuovi o di ritorno, affinità tra categorie e altro ancora.
title: Posso Eseguire Il Targeting Di Visitatori Che Soddisfano Parametri Di Profilo Specifici?
feature: Audiences
exl-id: aca45b80-660d-4b8e-a0d7-84627b8fd77b
TQID: https://experienceleague.adobe.com/lGNJLzHHa7aBUY3ZzJUU-9I8aPNsZgye1zmnN2mGHc4
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 250
ht-degree: 36%

---

# Profilo visitatore

Crea tipi di pubblico in [!DNL Adobe Target] per eseguire il targeting dei visitatori che soddisfano parametri di profilo specifici.

1. Nell&#39;interfaccia [!DNL Target], fare clic su **[!UICONTROL Tipi di pubblico]** > **[!UICONTROL Crea pubblico]**.
1. Assegna un nome al pubblico e aggiungi una descrizione facoltativa.
1. Trascina e rilascia **[!UICONTROL Profilo visitatore]** nel riquadro generatore di pubblico.

1. Fai clic su **[!UICONTROL Seleziona]**, quindi scegli una delle seguenti opzioni:

   ![immagine target_visitor_profile](assets/target_visitor_profile.png)

   I parametri del profilo del visitatore vengono trasmessi tramite mbox (profilo). Puoi eseguire il targeting dei visitatori nuovi o di ritorno, o includere tutti gli utenti.

   * [!UICONTROL Nuovo visitatore]
   * [!UICONTROL Visitatore di ritorno]
   * [!UICONTROL In Altri Test]
   * [!UICONTROL Non In Altri Test]
   * [!UICONTROL Prima pagina della sessione]
   * [!UICONTROL Non prima pagina della sessione]
   * [!UICONTROL Affinità tra categorie]

   Un profilo visitatore viene creato nella memoria Edge locale per ogni chiamata mbox con nuovo `mboxPC`. Dopo 30 minuti di inattività, il profilo viene salvato nel database [!DNL Target] ed è accessibile da altri server Edge.

   Quando un visitatore del sito accede a metà sessione e ottiene un `3rdpartyId`, tutti gli attributi di profilo precedentemente caricati associati a `3rdPartyId` sono immediatamente disponibili.

   Puoi eseguire il targeting di parametri di profilo personalizzati e parametri `user.`. Scegli il parametro che desideri utilizzare per eseguire il targeting dell’attività. Se il parametro desiderato non viene visualizzato, significa che non è stato attivato da una mbox.

1. (Facoltativo) Imposta regole aggiuntive per il pubblico.
1. Fai clic su **[!UICONTROL Fine]**.

## Video di formazione: Creazione di tipi di pubblico ![Icona panoramica](/help/main/assets/overview.png)

Questo video contiene informazioni sull&#39;utilizzo delle categorie di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392)
