---
keywords: arco temporale;data di inizio;data di fine;date di inizio/fine;pianificazione di target;ripartizione settimanale;ripartizione giornaliera;ripartizione
description: Scopri come utilizzare le date e le ore di inizio e fine per eseguire il targeting degli utenti che visitano il sito durante un intervallo di tempo specifico.
title: Posso indirizzare l’attività a visitatori che visitano il mio sito in momenti specifici?
feature: Audiences
exl-id: 814d545d-baee-4f8b-a2ed-ed68fceaeb7f
source-git-commit: 0e4698935b90cc0236abe6a47a6183c7fd2a7b20
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 34%

---

# [!UICONTROL Time Frame]

È possibile aggiungere date e ore di inizio e fine in [!DNL Adobe Target] per eseguire il targeting degli utenti che visitano il sito durante un intervallo di tempo specifico. Puoi anche impostare le opzioni Ripartizione settimanale e giornaliera per creare pattern ricorrenti per il targeting del pubblico.

Ad esempio, utilizzando [funzione tipi di pubblico combinati ad hoc](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5), puoi indirizzare gli utenti che spendono meno su contenuti specifici nei tre giorni prima del Black Friday e su altri contenuti dopo il Black Friday.

1. In [!DNL Target] , fare clic su **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Assegna un nome al pubblico e aggiungi una descrizione facoltativa.
1. Trascina **[!UICONTROL Time Frame]** nel riquadro audience builder.

   ![immagine target_timeframe_dialog](assets/target_timeframe_dialog.png)

1. Specifica la [!UICONTROL Start] e [!UICONTROL End] date e ore per il pubblico.

   Lascia la data di inizio vuota per avviare il targeting in base alla pianificazione dellʼattività. Lascia la data di fine vuota per continuare il targeting fino alla data e allʼora di fine dellʼattività.

   Puoi anche lasciare vuote entrambe le date di inizio o di fine. Questa funzionalità consente di utilizzare lo stesso pubblico in più attività (senza creare una copia del pubblico) controllando le date di inizio e di fine a livello di attività.

   >[!NOTE]
   >
   >Considera i seguenti aspetti:
   >
   >* Il fuso orario per le date di inizio/fine viene visualizzato come GMT +/- NN:NN, dove NN:NN è lo scostamento da GMT e corrisponde al fuso orario dell’account, non a quello del visitatore. Ad esempio, il fuso orario della California verrebbe visualizzato come GMT -08:00.
   >
   >* [!DNL Target] I tipi di pubblico dell’ora legale non tengono conto delle modifiche dell’ora legale (DST). È necessario salvare nuovamente manualmente i tipi di pubblico per tenere conto delle modifiche dell’ora legale.

1. (Condizionale) Fai clic su **[!UICONTROL Set frequency]** per impostare pattern ricorrenti, inclusi giorni della settimana e ore.

   ![Ripartizione settimanale e giornaliera](assets/week_and_day_parting.png)

   È possibile utilizzare [!UICONTROL Frequency] opzioni, ad esempio, per mostrare l’opzione &quot;Chat ora&quot; ai visitatori solo nei giorni e nelle ore in cui il call center dispone di personale.

   Seleziona uno o più giorni della settimana, quindi imposta gli orari di inizio e fine. Clic **[!UICONTROL Add frequency]** per specificare altri pattern, come desiderato.

   >[!NOTE]
   >
   >Il fuso orario per [!UICONTROL Week and Day Parting] viene visualizzato come GMT +/- NN:NN, dove NN:NN è lo scostamento da GMT e riflette il fuso orario a livello di account anziché quello del visitatore. Ad esempio, il fuso orario della California per ora legale del Pacifico verrà visualizzato come GMT -07:00.

1. (Facoltativo) Imposta regole aggiuntive per il pubblico.

   Se necessario, puoi ripetere il passaggio 5 per ogni regola.

1. Clic **[!UICONTROL Done]**.

## Video di formazione: Creazione di tipi di pubblico ![Badge panoramica](/help/main/assets/overview.png)

Questo video contiene informazioni sull&#39;utilizzo delle categorie di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392)
