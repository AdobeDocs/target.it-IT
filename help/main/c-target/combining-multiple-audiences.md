---
keywords: pubblico;regole del pubblico;combinare il pubblico;esclusione;aggiungere esclusione;escludere;combinazione di tipi di pubblico;pubblico adhoc;pubblico ad hoc
description: Scopri come combinare più tipi di pubblico (tra cui quelli di Adobe Experience Cloud e [!DNL Target] audience) al volo per creare un pubblico ad hoc.
title: È possibile combinare più tipi di pubblico per creare un nuovo pubblico?
feature: Audiences
exl-id: 1d9bff9c-f63b-4e15-9809-71b046158b71
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 56%

---

# Combinare più tipi di pubblico

Combinare più tipi di pubblico (incluso [!DNL Adobe Experience Cloud], [!DNL Adobe Experience Platform], e [!DNL Target] audience) al volo per creare un pubblico ad hoc. Puoi anche creare regole di esclusione ed escludere un determinato pubblico da una regola.

>[!NOTE]
>
>Il [!DNL Adobe Experience Platform] l&#39;origine è disponibile per tutti [!DNL Target] clienti che utilizzano [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=en){target=_blank}. Tipi di pubblico disponibili da [!DNL Adobe Experience Platform] può essere utilizzato così come è o combinato con i tipi di pubblico esistenti, come spiegato in questo argomento.
>
>Per ulteriori informazioni, consulta [Utilizzare i tipi di pubblico da Adobe Experience Platform](/help/main/c-target/c-audiences/audiences.md#aep).

Supponi di avere un pubblico “Nuovi visitatori” e un pubblico “Utenti Chrome”. Per un&#39;attività specifica, è possibile combinare questi gruppi di pubblico esistenti per indirizzare nuovi visitatori che utilizzano browser Chrome. Anziché creare un terzo pubblico e archiviarlo nella libreria [!UICONTROL Pubblico], è possibile combinare questi due gruppi di pubblico durante la creazione dell&#39;attività o durante la modifica di un&#39;attività esistente.

Un altro esempio è la possibilità di eseguire il targeting per tutti i clienti fidelizzati. Ad esempio, puoi includere uno specifico [!DNL Audience Manager] per lo stato di fedeltà e combinarlo con un [!DNL Target] pubblico composto da persone iscritte al tuo programma fedeltà nella sessione corrente. Combinare questi due tipi di pubblico è più facile che creare un terzo pubblico permanente.

Puoi combinare fino a 20 tipi di pubblico utilizzando gli operatori AND e OR.

È possibile creare e utilizzare il pubblico combinato in varie posizioni in tutta l’interfaccia utente di [!DNL Target].

## Creare un pubblico combinato durante la creazione di un’attività {#section_2F1CE9434CC04174B4BA2BFC89B85D77}

Puoi creare un pubblico combinato specifico nella pagina di [!UICONTROL Target] dell’attività durante il flusso di lavoro guidato in tre passaggi.

1. Durante la creazione di un’ [attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), sulla **[!UICONTROL Targeting]** , fare clic sui tre puntini di sospensione verticali e quindi su **[!UICONTROL Sostituisci pubblico]**.

   ![Risultato passaggio](assets/edit_audience.png)

1. Nella pagina **[!UICONTROL Scegli pubblico]** seleziona le caselle di controllo accanto ai gruppi di pubblico desiderati che desideri utilizzare come blocchi predefiniti per il pubblico combinato.

   Utilizza il [!UICONTROL Cerca tipi di pubblico] per limitare la ricerca del pubblico desiderato.

   ![Risultato passaggio](assets/combine_multiple_audiences1.png)

1. Clic **[!UICONTROL Combinare più tipi di pubblico]** in alto a destra.

   ![Risultato passaggio](assets/combine_multiple_audiences2.png)

1. (Condizionale) Modifica il nuovo pubblico combinato come desiderato.

   Il [!UICONTROL Modifica pubblico] consente di trascinare e rilasciare blocchi predefiniti di pubblico aggiuntivi dal lato sinistro al nuovo pubblico combinato. Puoi anche aggiungere regole di esclusione ed escludere tipi di pubblico.

   1. Utilizza la funzionalità di trascinamento della selezione per aggiungere tipi di pubblico all’interno di una sezione esistente come blocco predefinito di livello 2.

      Ad esempio, riprendendo l’esempio precedente, supponiamo che ora desideri includere nel pubblico combinato anche gli utenti di Safari. Cerca e trascina il pubblico “Browser Safari” nella casella “Browser Firefox” a destra, come nell’esempio seguente:

      ![immagine combinate_multiple_audiences3](assets/combine_multiple_audiences3.png)

      Osserva che l’operatore tra i due tipi di pubblico definiti dal browser è “AND” (E). Seleziona la [!UICONTROL E] e cambiarlo in &quot;OR&quot; (O) per creare un nuovo pubblico combinato per i nuovi visitatori che utilizzano Firefox o Safari. Fai attenzione a evitare la creazione di regole che escludano tutti i potenziali membri del pubblico. Ad esempio, non è possibile che qualcuno visiti una pagina utilizzando contemporaneamente i browser Firefox e Safari.

      >[!NOTE]
      >
      >L’operatore (AND oppure OR) deve rimanere lo stesso quando combini gruppi di pubblico. Non puoi combinare e abbinare gli operatori.

   1. Per aggiungere un’esclusione a una regola, fai clic su **[!UICONTROL Escludi]**.

      ![combina_più_tipi di pubblico3a immagine](assets/combine_multiple_audiences3a.png)

      Trascina e rilascia un pubblico.

      Ad esempio, per escludere i visitatori dagli Stati Uniti dai nuovi visitatori, puoi trascinare nella casella il pubblico Mercato: Stati Uniti.

      Questo pubblico combinato include tutti i nuovi visitatori del tuo sito (esclusi quelli di San Francisco) che utilizzano Safari o Firefox.

   1. Per escludere un pubblico da una regola, fai clic su **[!UICONTROL Esclusione]** > **[!UICONTROL Escludi questo pubblico]**.

      Ad esempio, puoi creare un pubblico combinato che includa tutti i nuovi visitatori del sito, esclusi quelli che utilizzano Firefox. Escludere i visitatori con Firefox è più facile e veloce che creare un pubblico combinato che includa in modo esplicito più browser (Safari, Chrome e Internet Explorer), ma non includa Firefox.

1. Fornisci un nome descrittivo per il pubblico combinato, quindi fai clic su **[!UICONTROL Fine]**.

## Creare un pubblico combinato da utilizzare nel targeting metrico {#section_A42E795AFCBD4575809C5942039910F0}

Puoi creare un pubblico combinato specifico nella pagina [!UICONTROL Obiettivi e impostazioni] dell&#39;attività da utilizzare nel targeting metrico. Ad esempio, per creare un targeting basato sulla conversione utilizzando un pubblico combinato:

1. Durante la modifica o la creazione di un’ [attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), sulla **[!UICONTROL Obiettivi e impostazioni]** pagina, seleziona **[!UICONTROL Conversione]** per la metrica di successo, quindi seleziona **[!UICONTROL Visualizzazione di una Mbox]** come azione.
1. Seleziona la mbox desiderata nel campo **[!UICONTROL Ricerca mbox]**.

   ![immagine combinate_multiple_audiences4](assets/combine_multiple_audiences4.png)

1. Fai clic sull&#39;icona, quindi fai clic su **[!UICONTROL Aggiungi targeting pubblico]**.
1. Fai clic sul collegamento **[!UICONTROL Aggiungi condizione di pubblico/targeting]** per visualizzare la finestra di dialogo [!UICONTROL Scegli pubblico].

   ![immagine combinate_multiple_audiences5](assets/combine_multiple_audiences5.png)

1. Procedi con il [Passaggio 2](/help/main/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) in “Creare un pubblico combinato durante la creazione di un’attività” per creare il pubblico combinato.

## Creare un pubblico combinato da utilizzare nel reporting {#section_4682D342EFBB43C38E54B99B3A1E14CD}

Puoi creare un pubblico combinato specifico nella pagina dell&#39;attività [!UICONTROL Obiettivi e impostazioni] da utilizzare nel rapporto.

1. Durante la modifica o la creazione di un’ [attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), sulla **[!UICONTROL Obiettivi e impostazioni]** , fare clic su **[!UICONTROL Aggiungi pubblico]** icona sotto [!UICONTROL Tipi di pubblico per i rapporti] per visualizzare [!UICONTROL Scegli pubblico] pagina.

   ![immagine combinate_multiple_audiences6](assets/combine_multiple_audiences6.png)

1. Procedi con il [Passaggio 2](/help/main/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) in “Creare un pubblico combinato durante la creazione di un’attività” per creare il pubblico combinato.

## Creare un pubblico combinato durante la modifica di un’attività {#section_364A12CE96E04B61B7C18113AA586C2C}

Puoi creare un pubblico combinato specifico durante la modifica di un&#39;attività esistente.

1. Dalla pagina [!UICONTROL Attività], passa il mouse sull&#39;attività desiderata, quindi fai clic sull&#39;icona **[!UICONTROL Modifica]**.

   Oppure

   Fai clic sull&#39;attività desiderata per aprirla, quindi fai clic su **[!UICONTROL Modifica attività]**.

1. Fai clic su **[!UICONTROL Configura]** > **[!UICONTROL Tipi di pubblico]** > **[!UICONTROL Più tipi di pubblico]**.

   ![Configura > Tipi di pubblico > Più tipi di pubblico](assets/combine_multiple_audiences7.png)

1. Fai clic sull&#39;icona altre opzioni (tre puntini di sospensione verticali) accanto al pubblico corrente dell&#39;attività, quindi fai clic su **[!UICONTROL Sostituisci pubblico]**.

   ![Cambia pubblico](assets/combine_multiple_audiences8.png)

1. Procedi con il [Passaggio 2](/help/main/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) in “Creare un pubblico combinato durante la creazione di un’attività” per creare il pubblico combinato.
