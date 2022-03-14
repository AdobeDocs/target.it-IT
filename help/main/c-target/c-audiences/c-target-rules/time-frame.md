---
keywords: intervallo temporale;data di inizio;data di fine;date di inizio/fine;pianificazione di target;ripartizione settimanale;ripartizione giornaliera;ripartizione
description: Scopri come utilizzare le date e gli orari di inizio e fine per eseguire il targeting degli utenti che visitano il tuo sito durante un intervallo di tempo specifico.
title: Posso Eseguire il targeting dei visitatori che visitano il mio sito a orari specifici?
feature: Audiences
exl-id: 814d545d-baee-4f8b-a2ed-ed68fceaeb7f
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 45%

---

# Intervallo temporale

Puoi aggiungere date e ore di inizio e fine in [!DNL Adobe Target] per eseguire il targeting degli utenti che visitano il sito durante un intervallo di tempo specifico. Puoi anche impostare le opzioni Ripartizione settimanale e giornaliera per creare pattern ricorrenti per il targeting del pubblico.

Ad esempio, utilizzando [funzionalità di pubblico combinato e ad hoc](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5), è possibile indirizzare gli utenti che spendono meno su contenuti specifici nei tre giorni che precedono il Black Friday e su altri contenuti dopo il Black Friday.

1. Nell’interfaccia di [!DNL Target] fai clic su **[!UICONTROL Pubblico]** > **[!UICONTROL Crea pubblico]**.
1. Assegna un nome al pubblico e aggiungi una descrizione facoltativa.
1. Trascinamento della selezione **[!UICONTROL Intervallo temporale]** nel riquadro audience builder (generatore di pubblico).

   ![](assets/target_timeframe_dialog.png)

1. Specifica la [!UICONTROL Inizio] e [!UICONTROL Fine] date e ore del pubblico.

   Lascia la data di inizio vuota per avviare il targeting in base alla pianificazione dellʼattività. Lascia la data di fine vuota per continuare il targeting fino alla data e allʼora di fine dellʼattività.

   Puoi anche lasciare vuote entrambe le date di inizio o di fine. Questa funzionalità ti consente di utilizzare lo stesso pubblico in più attività (senza creare una copia del pubblico) controllando le date di inizio e di fine a livello di attività.

   >[!NOTE]
   >
   >Il fuso orario per le date di inizio/fine viene visualizzato come GMT +/- NN:NN, dove NN:NN è lo scostamento da GMT e corrisponde al fuso orario dell’account, non a quello del visitatore. Ad esempio, il fuso orario della California verrebbe visualizzato come GMT -08:00.

1. (Condizionale) Fai clic su **[!UICONTROL Imposta frequenza]** per impostare pattern ricorrenti, inclusi giorni della settimana e ore.

   ![Ripartizione settimanale e giornaliera](assets/week_and_day_parting.png)

   Si potrebbe utilizzare [!UICONTROL Frequenza] ad esempio, per visualizzare un’opzione &quot;Chat Now&quot; ai visitatori solo durante i giorni e le ore in cui il call center è attivo.

   Seleziona uno o più giorni della settimana, quindi imposta gli orari di inizio e fine. Fai clic su **[!UICONTROL Aggiungi frequenza]** per specificare pattern aggiuntivi, come desiderato.

   >[!NOTE]
   >
   >Il fuso orario per [!UICONTROL Ripartizione settimanale e giornaliera] viene visualizzato come GMT +/- NN:NN, dove NN:NN è lo scostamento da GMT e corrisponde al fuso orario dellʼaccount, non a quello del visitatore. Ad esempio, il fuso orario della California per l’ora legale Pacifico veniva visualizzato come GMT -07:00.

1. (Facoltativo) Imposta regole aggiuntive per il pubblico.

   Puoi ripetere il passaggio 5 per ogni regola, se necessario.

1. Fai clic su **[!UICONTROL Fine]**.

## Video di formazione: Creazione di tipi di pubblico ![Badge panoramica](/help/main/assets/overview.png)

Questo video contiene informazioni sull&#39;utilizzo delle categorie di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392)
