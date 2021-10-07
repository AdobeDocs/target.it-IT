---
keywords: creazione di criteri personalizzati;algoritmi;criteri;criteri di consigli;csv;ftp;caricamento csv
description: Scopri come caricare un file CSV per personalizzare i consigli in Adobe [!DNL Target] Recommendations.
title: Come si caricano i criteri personalizzati in Recommendations?
feature: Recommendations
exl-id: 33434121-e0ae-4b82-b1dd-78b9738026cb
source-git-commit: 7a52f7c046fb00672ef1b13704308be39f89c7ad
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 39%

---

# ![PREMIUM](/help/assets/premium.png) Caricare criteri personalizzati

Carica un file CSV per personalizzare i consigli in [!DNL Adobe Target].

Esistono diversi modi per raggiungere la schermata [!UICONTROL Crea nuovo criterio]. Alcune opzioni dipendono dal modo in cui si raggiunge la schermata.

* Nella schermata della libreria **[!UICONTROL Recommendations]** > **[!UICONTROL Criteri]**, fai clic su **[!UICONTROL Crea criteri]** > **[!UICONTROL Crea criteri]**. I criteri creati vengono automaticamente resi disponibili per tutte le attività di [!DNL Recommendations].
* Quando crei un&#39;attività [!DNL Recommendations] utilizzando il [!UICONTROL Compositore esperienza visivo] (VEC), vieni immediatamente portato alla schermata [!UICONTROL Seleziona criteri] dopo aver selezionato un elemento nella pagina e dopo aver fatto clic su [!UICONTROL Sostituisci con Recommendations], [!UICONTROL Inserisci Recommendations prima], o [!UICONTROL Recommendations Inserisci]. Puoi quindi selezionare un criterio disponibile oppure fare clic su **[!UICONTROL Crea criterio]**. Se crei un nuovo criterio, puoi salvarne l’utilizzo con altre attività [!DNL Recommendations]. Per ulteriori informazioni, consulta [Creare un’attività Recommendations](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* Quando modifichi un’attività di [!DNL Recommendations], fai clic su una casella di [!UICONTROL Posizione Consigli] nella pagina e seleziona **[!UICONTROL Cambia criteri]**. Nella schermata [!UICONTROL Seleziona criteri], fai clic su **[!UICONTROL Crea criteri]**. Puoi salvare i nuovi criteri da utilizzare per altre attività [!DNL Recommendations] .

I passaggi seguenti presuppongono l&#39;accesso alla schermata [!UICONTROL Crea nuovo criterio] utilizzando il primo metodo: la schermata della libreria **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** .

1. Fai clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Criteri]**.

1. Fai clic su **[!UICONTROL Crea criterio]**.

1. Compila le informazioni nella sezione [Informazioni di base](/help/c-recommendations/c-algorithms/create-new-algorithm.md#info) .

   1. Dall’elenco a discesa **[!UICONTROL Seleziona algoritmo]** Tipo , seleziona **[!UICONTROL Criteri personalizzati]**.

   1. Dall’elenco a discesa **[!UICONTROL Algorithm]** , seleziona **[!UICONTROL Custom Algorithm]** (Algoritmo personalizzato).

      >[!NOTE]
      >
      >I passaggi precedenti fanno sì che la sezione [!UICONTROL Carica CSV] venga visualizzata nella parte inferiore della finestra di dialogo [!UICONTROL Crea nuovo criterio].

1. (Condizionale) Compila le informazioni nella sezione [Contenuto backup](/help/c-recommendations/c-algorithms/create-new-algorithm.md#content) .

1. (Condizionale) Compila le informazioni nella sezione [Regole di inclusione](/help/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion) .

1. Nella sezione **[!UICONTROL Carica CSV]** , seleziona la **[!UICONTROL Posizione]** del file CSV.

   ![Sezione Carica CSV](assets/upload-csv.png)

   Il file CSV deve essere formattato correttamente per essere caricato con successo. Fai clic su **[!UICONTROL Scarica il modello CSV]** per ottenere un file CSV formattato correttamente.

   Puoi scegliere tra due opzioni di posizione:

   * **FTP:** per caricare il file CSV da un server FTP, seleziona **[!UICONTROL FTP]**, quindi inserisci le informazioni richieste. Puoi utilizzare SSL, che utilizza il protocollo FTPS per trasferire il file CSV in modo sicuro.
   * **URL:** per caricare il file CSV da un URL, seleziona  **[!UICONTROL URL]**, quindi immetti un URL di feed.

1. Fai clic su **[!UICONTROL Salva]**.

## Considerazioni

* Le entità di criteri personalizzati (righe) possono contenere fino a 1.000 elementi consigliati (colonne).

* Gli aggiornamenti dei criteri personalizzati sono per impostazione predefinita “cumulativi”. Le nuove coppie chiave-valore specificate nel file di caricamento CSV sovrascrivono le coppie chiave-valore esistenti. Le coppie chiave-valore esistenti prive di chiavi specificate nel caricamento CSV sono ancora disponibili per la consegna e scadono dopo 31 giorni dal loro ultimo caricamento come parte del file CSV.

   Contatta l&#39;assistenza clienti per consentire l&#39;eliminazione dei risultati esistenti non inclusi nel successivo caricamento CSV. Se questa impostazione è abilitata, solo i tasti presenti nel file di feed CSV personalizzato sono disponibili per la consegna. Questa impostazione si applica a tutti i criteri personalizzati.

* I criteri personalizzati vengono aggiornati ogni 24 ore.

   Puoi visualizzare lo stato di caricamento e sincronizzazione dei criteri personalizzati caricati nella parte inferiore di ogni scheda criteri nella pagina [!UICONTROL Recommendations] > [!UICONTROL Criteria] . Lo stato viene visualizzato anche nella finestra di dialogo [!UICONTROL Modifica] durante la modifica dei criteri personalizzati.

* Il flusso per un caricamento senza errori deve essere [!UICONTROL Pianificato] > [!UICONTROL Download del file di feed] > [!UICONTROL Importazione] > [!UICONTROL Riuscito].

* Di seguito sono riportati i possibili messaggi di errore che potresti ricevere se [!DNL Target] riscontra un problema con il caricamento:

   | Messaggio di errore | Dettagli |
   |--- |--- |
   | Errore sconosciuto | Indica un errore tecnico interno. |
   | Errore di analisi | Probabilmente si è verificato un problema con il formato di file feed. Correggere il formato del file e salvare nuovamente l&#39;algoritmo, che riavvia il processo di download del file. |
   | Server non trovato | Fornisci un IP o un nome host visibile su Internet. |
   | Errore di credenziali | Fornisci un nome utente e una password validi per un account attivo sul server. |
   | Directory non trovata | Fornisci una directory esistente sul server. |
   | File non trovato | Fornisci il nome di un file sul server nella directory indicata. |

## Video di formazione: Creare i criteri in Recommendations (12:33) ![Icona Tutorial](/help/assets/tutorial.png)

Questo video contiene le seguenti informazioni (i dettagli sul caricamento di criteri personalizzati iniziano alle 11:43):

* Creare criteri
* Creare sequenze di criteri
* Caricare criteri personalizzati

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
