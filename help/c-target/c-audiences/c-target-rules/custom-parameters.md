---
keywords: parametri personalizzati;parametri personalizzati di target;targetpageparams;parametri mbox di targeting
description: I parametri personalizzati sono parametri mbox. Se li trasmetti alle mbox, o utilizzi la funzione targetPageParams, questi parametri vengono visualizzati qui e possono essere utilizzati nei tipi di pubblico.
title: Parametri personalizzati
feature: Audiences
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 90%

---


# Parametri personalizzati{#custom-parameters}

I parametri personalizzati sono parametri mbox. Se li trasmetti alle mbox, o utilizzi la funzione targetPageParams, questi parametri vengono visualizzati qui e possono essere utilizzati nei tipi di pubblico.

Per ulteriori informazioni, consultate [Trasmettere i parametri a una mbox globale](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md).

Durante la creazione di un pubblico personalizzato basato su un parametro mbox, `mboxParameter` non richiede più di specificare `mboxName`. Il nome dell’elemento mbox è ora facoltativo. Questa modifica consente di utilizzare parametri da più elementi mbox o di fare riferimento a un parametro che non è ancora stato registrato nella rete Edge.

1. Nell’interfaccia di [!DNL Target] fai clic su **[!UICONTROL Pubblico]** > **[!UICONTROL Crea pubblico]**.
1. Dai un nome al pubblico.
1. Fare clic su **[!UICONTROL Aggiungi regola]** > **[!UICONTROL Personalizzato]**.

   Per selezionare il parametro desiderato:

   * Mentre crei un nuovo pubblico, seleziona il nome di un parametro dall&#39;elenco, comincia a digitare i primi caratteri del parametro desiderato o il nome intero.
   * Se ricordi il nome mbox ma non il nome del parametro, usa la casella di controllo per filtrare una mbox nota trasmettendo il parametro desiderato.

   Con uno di questi metodi, non esiste alcun collegamento tra mbox e il parametro. Il pubblico funzionerà sulla base del parametro su tutte le mbox che trasmettono tale parametro.

   Se modifichi un pubblico esistente, i criteri di filtraggio vengono visualizzati con il nome mbox fornito durante la creazione.

1. Scegli un valutatore:

   * Contiene (senza distinzione maiuscole/minuscole)
   * Non contiene (senza distinzione maiuscole/minuscole)
   * È uguale a

   ![Parametro per pubblico Personalizzato](/help/c-target/c-audiences/c-target-rules/assets/custom.png)

1. Inserisci ciascun valore in una nuova riga.
1. (Facoltativo) Fai clic su **[!UICONTROL Aggiungi regola]** per impostare regole aggiuntive per il pubblico.
1. Fai clic su **[!UICONTROL Salva]**.

I [dettagli della definizione di una scheda a comparsa](/help/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) del pubblico visualizzano il nome del parametro nella sezione Regole. Non esiste un riferimento al mbox utilizzato per il filtraggio.

>[!NOTE]
>
>Per i tipi di pubblico personalizzati creati prima della versione 18.5.1 di Target (22 maggio 2018), i nomi mbox non verranno visualizzati nella scheda a comparsa di definizione del pubblico. È necessario salvare nuovamente il pubblico personalizzato per far sì che il nome mbox venga mostrato nella scheda.

## Considerazioni {#considerations}

* I tipi di pubblico e le attività vengono valutati per una mbox specifica. Ad esempio, se la mbox globale trasmette un determinato parametro, ma la mbox regionale non lo fa, il targeting per attività/pubblico non verrà qualificato per la mbox regionale.
* Il targeting non viene valutato sui parametri mbox interni, come mboxPC, mboxSession, mbox3rdPartyId, mboxMCSDID, mboxMCAVID, mboxMCGVID, mboxCount, mboxId e mboxVersion.

## Video di formazione: Creazione di audience ![Logo di esercitazione](/help/assets/tutorial.png)

Questo video contiene informazioni sull&#39;utilizzo delle categorie di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392)
