---
description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per le versioni più recenti o imminenti di Adobe Target.
keywords: note sulla versione;rilasci;aggiornamenti;release futura;miglioramenti;nuove funzioni;correzioni
seo-description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per le versioni DNL Adobe Target più recenti o imminenti.
seo-title: Note sulla versione prerelease di Adobe Target
solution: Target
title: Note sulla versione di Target (prerelease)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 0d7d4666b5fc0d27ccdde812ef8f1182400dd3e8

---


# Note sulla versione di Target (prerelease){#target-release-notes-prerelease}

Queste note sulla versione contengono informazioni su funzioni, miglioramenti e correzioni per le versioni più recenti o in arrivo di [!DNL Adobe Target].

**Ultimo aggiornamento: 17 ottobre 2019**

>[!NOTE]
>
>Queste note sulla versione contengono delle informazioni sulla versione prerelease. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso. Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali o possono essere diverse, a seconda della tempistica delle release.
>
>I codici tra parentesi sono per uso interno di [!DNL Adobe].

## Target Standard/Premium 19.10.1 (22 ottobre 2019)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| ![Premium badge](/help/assets/premium.png) - Raccomandazioni<br>basate sull'utente (24 ottobre 2019) | Raccomanda gli elementi in base alla cronologia di navigazione, visualizzazione e acquisto di ogni visitatore. Tali elementi sono generalmente denominati "Consigliati per l'utente."<br>Questo criterio consente di fornire contenuti ed esperienze personalizzati sia ai visitatori nuovi che di ritorno. L'elenco delle raccomandazioni è ponderato per l'attività più recente del visitatore, viene aggiornato in sessione e diventa più personalizzato man mano che il visitatore naviga nel sito.<br>Per ulteriori informazioni, vedere "Raccomandazioni basate sull'utente" in [Criteri/algoritmi](/help/c-recommendations/c-algorithms/algorithms.md#criteria-algorithms). |

### Miglioramenti, correzioni e modifiche

* Quando effettuate l’accesso al [!DNL Adobe Experience Cloud]pannello, viene visualizzata la nuova navigazione dell’intestazione. La navigazione precedente è molto simile a quella con la barra nera nella parte superiore, ma offre i seguenti miglioramenti:

   * Passaggio più semplice tra organizzazioni [!DNL Identity Management System] (IMS) o a una soluzione diversa.
   * Aiuto utente migliorato: I risultati della ricerca includono i risultati della documentazione del [!DNL Target] prodotto, forum della community e altri contenuti video, che consentono di accedere più facilmente a più contenuti per trarre il massimo vantaggio [!DNL Target]. È stato inoltre aggiunto un meccanismo di feedback nel menu [!UICONTROL Aiuto] , che semplifica la segnalazione dei problemi o la condivisione delle idee.

   * Miglioramento della funzionalità NPS (Net Promoter Score) per il feedback, in modo che il modale del sondaggio non disturbi il flusso di lavoro.
   * Flusso di accesso migliorato. Precedentemente, tutti [!DNL Target] i clienti accedevano alla pagina di destinazione di Target dopo aver fatto clic sull’ [!DNL Target] icona nell’intestazione. Questa pagina ha quindi permesso ai clienti di procedere con [!DNL Target Standard/Premium], [!DNL Search&Promote], o [!DNL Recommendations Classic], come mostrato di seguito:

      ![Pagina di destinazione](/help/r-release-notes/assets/landing.png)

      Abbiamo eliminato questa pagina di destinazione per tutti i nostri clienti. Ora è sempre possibile accedere direttamente alla pagina Elenco  attività facendo clic sull’ [!DNL Target] icona nella nuova barra di navigazione dell’intestazione.

      Se utilizzate [!DNL Recommendations Classic], potete passare direttamente alla soluzione oppure dal collegamento breve creato nella scheda [!UICONTROL Recommendations] , come illustrato di seguito:

      ![Collegamento profondo Recs Classic](/help/r-release-notes/assets/recs-classic.png)

      Se utilizzate [!DNL Search&Promote], dovete accedere direttamente all’URL [](https://center.atomz.com/center/?ims=1) Search&amp;Promote (https://center.atomz.com/center/?ims=1). Il percorso per raggiungere [!DNL Search&Promote] dall'interno di [!DNL Adobe Target] è stato rimosso completamente.

   * Le notifiche per non [!DNL Target] sono attualmente disponibili nel menu a discesa [!UICONTROL Notifiche] dell'intestazione.
   >[!NOTE]
   >
   >Queste funzioni non verranno implementate simultaneamente, né verranno distribuite insieme a tutti i clienti. Nel corso dei prossimi giorni verranno introdotte queste funzionalità a partire dalla release [!DNL Target Standard/Premium] 19.10.1 (22 ottobre 2019).
   >
   >Durante il rollout della nuova barra di navigazione, noterete anche alcune modifiche agli URL. Tutti i precedenti collegamenti con segnalibro continuano a funzionare, ma vi invitiamo a contrassegnare nuovi collegamenti per un'apertura più rapida.

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
