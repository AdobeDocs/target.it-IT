---
keywords: pubblico;regole del pubblico;combinare il pubblico;esclusione;aggiungere esclusione;escludere;combinazione di tipi di pubblico;pubblico adhoc;pubblico ad hoc
description: Scopri come combinare più tipi di pubblico (tra cui i tipi di pubblico di Adobe Experience Cloud e [!DNL Target] audience) per creare al volo tipi di pubblico ad hoc.
title: Posso combinare più tipi di pubblico per creare un nuovo pubblico?
feature: Audiences
exl-id: 1d9bff9c-f63b-4e15-9809-71b046158b71
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '960'
ht-degree: 64%

---

# Combinare più tipi di pubblico

Combinare più tipi di pubblico (tra cui [!DNL Adobe Experience Cloud], [!DNL Adobe Experience Platform]e [!DNL Target] audience) per creare al volo tipi di pubblico ad hoc. Puoi anche creare regole di esclusione ed escludere un determinato pubblico da una regola.

>[!NOTE]
>
>La [!DNL Adobe Experience Platform] l&#39;origine è disponibile per tutti [!DNL Target] i clienti che utilizzano [Adobe Experience Platform Web SDK](https://developer.adobe.com/target/implement/client-side/aep-web-sdk/){target=_blank}. Tipi di pubblico disponibili dal [!DNL Adobe Experience Platform] può essere utilizzato così come è o combinato con tipi di pubblico esistenti, come spiegato in questo argomento.
>
>Per ulteriori informazioni consulta [Utilizzare i tipi di pubblico da Adobe Experience Platform](/help/main/c-target/c-audiences/audiences.md#aep).

Supponi di avere un pubblico “Nuovi visitatori” e un pubblico “Utenti Chrome”. Per un&#39;attività specifica, è possibile combinare questi gruppi di pubblico esistenti per indirizzare nuovi visitatori che utilizzano browser Chrome. Anziché creare un terzo pubblico e archiviarlo nella libreria [!UICONTROL Pubblico], è possibile combinare questi due gruppi di pubblico durante la creazione dell&#39;attività o durante la modifica di un&#39;attività esistente.

Ad esempio, puoi rivolgerti a tutti i clienti fidelizzati. Ad esempio, puoi includere un [!DNL Audience Manager] pubblico per lo stato fedeltà e combinarlo con un [!DNL Target] pubblico composto da persone che hanno firmato per il tuo programma fedeltà durante la sessione corrente. Combinare questi due tipi di pubblico è più semplice che creare un terzo pubblico permanente.

È possibile combinare fino a 20 tipi di pubblico utilizzando gli operatori AND e OR.

È possibile creare e utilizzare il pubblico combinato in varie posizioni in tutta l’interfaccia utente di [!DNL Target].

## Creare un pubblico combinato durante la creazione di un’attività {#section_2F1CE9434CC04174B4BA2BFC89B85D77}

Puoi creare un pubblico combinato specifico nella pagina di [!UICONTROL Target] dell’attività durante il flusso di lavoro guidato in tre passaggi.

1. Durante la creazione di un’ [attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), sul **[!UICONTROL Targeting]** fare clic sui tre puntini di sospensione verticali, quindi fare clic su **[!UICONTROL Sostituisci pubblico]**.

   ![Risultato passaggio](assets/edit_audience.png)

1. Nella pagina **[!UICONTROL Scegli pubblico]** seleziona le caselle di controllo accanto ai gruppi di pubblico desiderati che desideri utilizzare come blocchi predefiniti per il pubblico combinato.

   Utilizza la [!UICONTROL Cerca tipi di pubblico] per limitare la ricerca del pubblico desiderato.

   ![Risultato passaggio](assets/combine_multiple_audiences1.png)

1. Fai clic su **[!UICONTROL Combinare più tipi di pubblico]** nell&#39;angolo in alto a destra.

   ![Risultato passaggio](assets/combine_multiple_audiences2.png)

1. (Condizionale) Modifica il nuovo pubblico combinato come desiderato.

   La [!UICONTROL Modifica pubblico] consente di trascinare e rilasciare ulteriori blocchi predefiniti per il pubblico dal lato sinistro al nuovo pubblico combinato. Puoi anche aggiungere regole di esclusione per escludere i tipi di pubblico.

   1. Utilizza la funzionalità di trascinamento della selezione per aggiungere tipi di pubblico all’interno di una sezione esistente come modulo di livello 2.

      Ad esempio, riprendendo l’esempio precedente, supponiamo che ora desideri includere nel pubblico combinato anche gli utenti di Safari. Cerca e trascina il pubblico “Browser Safari” nella casella “Browser Firefox” a destra, come nell’esempio seguente:

      ![immagine combinare_multiple_audiences3](assets/combine_multiple_audiences3.png)

      Osserva che l’operatore tra i due tipi di pubblico definiti dal browser è “AND” (E). Seleziona la [!UICONTROL E] elenco a discesa e modificalo in &quot;OR&quot; (O) per creare un nuovo pubblico combinato per i nuovi visitatori che utilizzano Firefox o Safari. Fai attenzione a evitare la creazione di regole che escludano tutti i potenziali membri del pubblico. Ad esempio, non è possibile che qualcuno visiti una pagina utilizzando contemporaneamente i browser Firefox e Safari.

      >[!NOTE]
      >
      >L’operatore (AND oppure OR) deve rimanere lo stesso quando combini gruppi di pubblico. Non puoi combinare e abbinare gli operatori.

   1. Per aggiungere un’esclusione a una regola, fai clic su **[!UICONTROL Escludi]**.

      ![combinare_multiple_audiences3a immagine](assets/combine_multiple_audiences3a.png)

      Trascina e rilascia un pubblico.

      Ad esempio, per escludere i visitatori dagli Stati Uniti dai nuovi visitatori, puoi trascinare Market: Pubblico americano nella scatola.

      Questo pubblico combinato include tutti i nuovi visitatori del tuo sito (esclusi quelli di San Francisco) che utilizzano Safari o Firefox.

   1. Per escludere un pubblico da una regola, fai clic su **[!UICONTROL Esclusione]** > **[!UICONTROL Escludi questo pubblico]**.

      Ad esempio, puoi creare un pubblico combinato che includa tutti i nuovi visitatori del sito, esclusi quelli che utilizzano Firefox. Escludere i visitatori con Firefox è più facile e veloce che creare un pubblico combinato che includa in modo esplicito più browser (Safari, Chrome e Internet Explorer), ma non includa Firefox.

1. Fornisci un nome descrittivo per il pubblico combinato, quindi fai clic su **[!UICONTROL Fine]**.

## Creare un pubblico combinato da utilizzare nel targeting metrico {#section_A42E795AFCBD4575809C5942039910F0}

Puoi creare un pubblico combinato specifico nella pagina [!UICONTROL Obiettivi e impostazioni] dell&#39;attività da utilizzare nel targeting metrico. Ad esempio, per creare un targeting basato sulla conversione utilizzando un pubblico combinato:

1. Durante la modifica o la creazione di un&#39; [attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), nella pagina **[!UICONTROL Obiettivi e impostazioni]**, seleziona **[!UICONTROL Conversione]** per la metrica di successo, quindi seleziona **[!UICONTROL Visualizza una mbox]** come azione.
1. Seleziona la mbox desiderata nel campo **[!UICONTROL Ricerca mbox]**.

   ![immagine combinare_multiple_audiences4](assets/combine_multiple_audiences4.png)

1. Fai clic sull&#39;icona, quindi fai clic su **[!UICONTROL Aggiungi targeting pubblico]**.
1. Fai clic sul collegamento **[!UICONTROL Aggiungi condizione di pubblico/targeting]** per visualizzare la finestra di dialogo [!UICONTROL Scegli pubblico].

   ![combinare_multiple_audiences5 immagine](assets/combine_multiple_audiences5.png)

1. Procedi con il [Passaggio 2](/help/main/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) in “Creare un pubblico combinato durante la creazione di un’attività” per creare il pubblico combinato.

## Creare un pubblico combinato da utilizzare nel reporting {#section_4682D342EFBB43C38E54B99B3A1E14CD}

Puoi creare un pubblico combinato specifico nella pagina dell&#39;attività [!UICONTROL Obiettivi e impostazioni] da utilizzare nel rapporto.

1. Durante la modifica o la creazione di un’ [attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), nella pagina **[!UICONTROL Obiettivi e impostazioni]** fai clic sull&#39;icona **[!UICONTROL Aggiungi pubblico]** in [!UICONTROL Pubblico per la creazione di rapporti] per visualizzare la pagina [!UICONTROL Scegli pubblico].

   ![immagine combinare_multiple_audiences6](assets/combine_multiple_audiences6.png)

1. Procedi con il [Passaggio 2](/help/main/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) in “Creare un pubblico combinato durante la creazione di un’attività” per creare il pubblico combinato.

## Creare un pubblico combinato durante la modifica di un’attività {#section_364A12CE96E04B61B7C18113AA586C2C}

Puoi creare un pubblico combinato specifico durante la modifica di un&#39;attività esistente.

1. Dalla pagina [!UICONTROL Attività], passa il mouse sull&#39;attività desiderata, quindi fai clic sull&#39;icona **[!UICONTROL Modifica]**.

   Oppure

   Fai clic sull&#39;attività desiderata per aprirla, quindi fai clic su **[!UICONTROL Modifica attività]**.

1. Fai clic sul pulsante **[!UICONTROL Configura]** > **[!UICONTROL Tipi di pubblico]** > **[!UICONTROL Più tipi di pubblico]**.

   ![Configura > Tipi di pubblico > Più tipi di pubblico](assets/combine_multiple_audiences7.png)

1. Fai clic sull’icona altre opzioni (tre puntini di sospensione verticali) accanto al pubblico corrente dell’attività, quindi fai clic su **[!UICONTROL Cambia pubblico]**.

   ![Cambia pubblico](assets/combine_multiple_audiences8.png)

1. Procedi con il [Passaggio 2](/help/main/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) in “Creare un pubblico combinato durante la creazione di un’attività” per creare il pubblico combinato.
