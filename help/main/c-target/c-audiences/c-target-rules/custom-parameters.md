---
keywords: parametri personalizzati;parametri personalizzati di target;targetpageparams;parametri mbox di targeting
description: Scopri come trasmettere parametri personalizzati a  [!DNL Adobe Target]  per l'utilizzo in tipi di pubblico.
title: Posso indirizzare i visitatori in base a parametri personalizzati?
feature: Audiences
exl-id: f0669888-6b9e-4738-9ed4-0418ea56fffa
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 37%

---

# Parametri personalizzati

I parametri personalizzati sono parametri mbox in [!DNL Adobe Target]. Se trasmetti parametri mbox alle mbox o utilizzi la funzione `targetPageParams`, tali parametri vengono visualizzati qui per essere utilizzati nei tipi di pubblico.

Per ulteriori informazioni, consulta [Trasmettere i parametri a una mbox globale](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/global-mbox/pass-parameters-to-global-mbox.html?lang=it){target=_blank}.

Durante la creazione di un pubblico personalizzato basato su un parametro mbox, `mboxParameter` non richiede più di specificare `mboxName`. Il nome dell’elemento mbox è ora facoltativo. Questa modifica consente di utilizzare parametri da più elementi mbox o di fare riferimento a un parametro che non è ancora stato registrato nella rete Edge.

1. Nell&#39;interfaccia [!DNL Target], fare clic su **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Assegna un nome al pubblico e aggiungi una descrizione facoltativa.
1. Trascina **[!UICONTROL Custom]** nel generatore di pubblico.

   Per selezionare il parametro desiderato:

   * Durante la creazione di un pubblico, seleziona un nome di parametro dall’elenco, inizia a digitare i primi caratteri del nome di parametro desiderato o digita il nome completo del nome di parametro desiderato.
   * Se ricordi il nome mbox ma non il nome del parametro, utilizza l&#39;elenco a discesa [!UICONTROL Filter by] per filtrare in base a una mbox nota che trasmette il parametro desiderato.

   Con uno di questi metodi, non esiste alcun collegamento tra mbox e il parametro. Il pubblico funziona in base al parametro su tutte le mbox che trasmettono tale parametro.

   >[!NOTE]
   >
   >La mbox selezionata dall&#39;elenco a discesa [!UICONTROL Filter By] non viene salvata durante la creazione dell&#39;attività. Questa opzione consente di filtrare i parametri in base alla mbox selezionata.

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
   * Il parametro è presente
   * Il parametro non è presente
   * Il valore del parametro è presente
   * Il valore del parametro non è presente
   * Parametro o valore non presente
   * Inizia con
   * Termina con

   ![Parametro per pubblico Personalizzato](assets/custom.png)

1. Inserisci ciascun valore in una nuova riga.
1. (Facoltativo) Imposta regole aggiuntive per il pubblico.
1. Fare clic su **[!UICONTROL Done]**.

La scheda a comparsa [dettagli definizione del pubblico](/help/main/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) mostra il nome del parametro nella sezione **[!UICONTROL Rules]**. Non esiste un riferimento al mbox utilizzato per il filtraggio.

>[!NOTE]
>
>Per i tipi di pubblico personalizzati creati prima della versione 18.5.1 di [!DNL Target] (22 maggio 2018), i nomi mbox non vengono visualizzati nella scheda a comparsa di definizione del pubblico. Salva nuovamente il pubblico personalizzato per far sì che il nome mbox venga mostrato nella scheda.

## Considerazioni {#considerations}

* I tipi di pubblico e le attività vengono valutati per una mbox specifica. Ad esempio, se la mbox globale trasmette un determinato parametro, ma la mbox regionale non lo fa, il targeting per attività/pubblico non è qualificato per la mbox regionale.
* Il targeting non viene valutato sui parametri mbox interni, come mboxPC, mboxSession, mbox3rdPartyId, mboxMCSDID, mboxMCAVID, mboxMCGVID, mboxCount, mboxId e mboxVersion.

## Video di formazione: Creazione di tipi di pubblico ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video contiene informazioni sull&#39;utilizzo delle categorie di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392)
