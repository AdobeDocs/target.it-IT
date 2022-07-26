---
keywords: parametri personalizzati;parametri personalizzati di target;targetpageparams;parametri mbox di targeting
description: Scopri come trasmettere parametri personalizzati a [!DNL Adobe Target] da utilizzare nei tipi di pubblico.
title: Posso indirizzare i visitatori in base a parametri personalizzati?
feature: Audiences
exl-id: f0669888-6b9e-4738-9ed4-0418ea56fffa
source-git-commit: 8890d29a71506095a166321e324a000b5ad862a6
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 40%

---

# Parametri personalizzati

I parametri personalizzati sono parametri mbox in [!DNL Adobe Target]. Se trasmetti parametri mbox a mbox o utilizza la `targetPageParams` tali parametri vengono visualizzati qui per l&#39;utilizzo in audience.

Per ulteriori informazioni, consulta [Trasmettere parametri a una mbox globale](https://developer.adobe.com/target/implement/client-side/atjs/global-mbox/pass-parameters-to-global-mbox/){target=_blank}.

Durante la creazione di un pubblico personalizzato basato su un parametro mbox, `mboxParameter` non richiede più di specificare `mboxName`. Il nome dell’elemento mbox è ora facoltativo. Questa modifica consente di utilizzare parametri da più elementi mbox o di fare riferimento a un parametro che non è ancora stato registrato nella rete Edge.

1. Nell’interfaccia di [!DNL Target] fai clic su **[!UICONTROL Pubblico]** > **[!UICONTROL Crea pubblico]**.
1. Assegna un nome al pubblico e aggiungi una descrizione facoltativa.
1. Trascinamento della selezione **[!UICONTROL Personalizzato]** in Audience Builder.

   Per selezionare il parametro desiderato:

   * Durante la creazione di un pubblico, seleziona un nome di parametro dall’elenco, inizia a digitare i primi caratteri del nome di parametro desiderato o il nome completo del parametro desiderato.
   * Se ricordi il nome mbox ma non il nome del parametro, utilizza la variabile [!UICONTROL Filtra per] elenco a discesa per filtrare su una mbox nota trasmettendo il parametro desiderato.

   Con uno di questi metodi, non esiste alcun collegamento tra mbox e il parametro. Il pubblico funziona in base al parametro per tutte le mbox che trasmettono quel parametro.

   >[!NOTE]
   >
   >La mbox selezionata dalla [!UICONTROL Filtra per] l’elenco a discesa non viene salvato durante la creazione dell’attività. Questa opzione consente di filtrare i parametri in base alla mbox selezionata.

   Se modifichi un pubblico esistente, i criteri di filtraggio vengono visualizzati con il nome mbox fornito durante la creazione.

1. Scegli un valutatore:

   * Contiene (senza distinzione maiuscole/minuscole)
   * Non contiene (senza distinzione maiuscole/minuscole)
   * È uguale a
   * È diverso da
   * È maggiore di
   * È maggiore o uguale a
   * È minore di
   * È minore o uguale a
   * Parametro presente
   * Parametro non presente
   * Valore parametro presente
   * Il valore del parametro non è presente
   * Parametro o valore non presente
   * Inizia con
   * Termina con

   ![Parametro per pubblico Personalizzato](assets/custom.png)

1. Inserisci ciascun valore in una nuova riga.
1. (Facoltativo) Imposta regole aggiuntive per il pubblico.
1. Fai clic su **[!UICONTROL Fine]**.

I [dettagli della definizione di una scheda a comparsa](/help/main/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) del pubblico visualizzano il nome del parametro nella sezione Regole. **** Non esiste un riferimento al mbox utilizzato per il filtraggio.

>[!NOTE]
>
>Per tipi di pubblico personalizzati creati prima della [!DNL Target] Nella versione 18.5.1 (22 maggio 2018), i nomi mbox non vengono visualizzati nella scheda a comparsa di definizione del pubblico. Salva nuovamente il pubblico personalizzato per ottenere il nome mbox da visualizzare nella scheda .

## Considerazioni {#considerations}

* I tipi di pubblico e le attività vengono valutati per una mbox specifica. Ad esempio, se la mbox globale trasmette un determinato parametro, ma la mbox regionale no, il targeting di attività/pubblico per tale parametro non è qualificato per la mbox regionale.
* Il targeting non viene valutato su parametri mbox interni, come mboxPC, mboxSession, mbox3rdPartyId, mboxMCSDID, mboxMCAVID, mboxMCGVID, mboxCount, mboxId e mboxVersion.

## Video di formazione: Creazione di tipi di pubblico ![Badge tutorial](/help/main/assets/tutorial.png)

Questo video contiene informazioni sull&#39;utilizzo delle categorie di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392)
