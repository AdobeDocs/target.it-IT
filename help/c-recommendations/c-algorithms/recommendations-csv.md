---
keywords: creating custom criteria;algorithms;criteria;recommendations criteria;csv;ftp;upload csv
description: Carica un file CSV per personalizzare i consigli.
title: Caricare criteri personalizzati
feature: criteria
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 63%

---


# ![PREMIUM](/help/assets/premium.png) Caricare criteri personalizzati{#upload-custom-criteria}

Carica un file CSV per personalizzare i consigli.

Esistono diversi modi per raggiungere la schermata [!UICONTROL Crea nuovo criterio]. Alcune opzioni dipendono dal modo in cui si raggiunge la schermata.

* Nella schermata della libreria **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**, fate clic su **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]** (Crea criteri). I criteri creati vengono automaticamente resi disponibili per tutte le attività di [!DNL Recommendations].
* Quando create un&#39;attività [!DNL Recommendations] utilizzando [!UICONTROL Visual Experience Composer (Compositore esperienza visivo)] (VEC), viene immediatamente visualizzata la schermata [!UICONTROL Select Criteria] (Seleziona criteri) dopo aver selezionato un elemento nella pagina e dopo aver fatto clic su [!UICONTROL Replace w/ Recommendations], [!UICONTROL Insert Recommendations Before] oppure [!UICONTROL Insert Recommendations]. Potete quindi selezionare un criterio disponibile oppure fare clic su **[!UICONTROL Crea criteri]**. Se create un nuovo criterio, potete salvare i criteri da usare con altre attività [!DNL Recommendations]. Per ulteriori informazioni, vedere [Creare un&#39;attività Recommendations](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* Quando modifichi un’attività di [!DNL Recommendations], fai clic su una casella di [!UICONTROL Posizione Consigli] nella pagina e seleziona **[!UICONTROL Cambia criteri]**. Nella schermata [!UICONTROL Seleziona criteri], fare clic su **[!UICONTROL Crea criteri]**. Sarà possibile salvare i nuovi criteri da utilizzare per altre attività di [!DNL Recommendations].

Nella procedura seguente si presuppone che si possa accedere alla schermata [!UICONTROL Crea nuovi criteri] utilizzando il primo metodo: la schermata della libreria **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Fare clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Fare clic su **[!UICONTROL Crea criteri]** > **[!UICONTROL Carica criteri personalizzati]**.

1. Compila le informazioni nella sezione [Informazioni di base](/help/c-recommendations/c-algorithms/create-new-algorithm.md#info).

1. Compila le informazioni nella sezione [Origine dati](/help/c-recommendations/c-algorithms/create-new-algorithm.md#data-source).

1. Compila le informazioni nella sezione [Contenuto](/help/c-recommendations/c-algorithms/create-new-algorithm.md#content).

1. (Condizionale) Compila le informazioni nella sezione [Somiglianza di contenuto](/help/c-recommendations/c-algorithms/create-new-algorithm.md#similarity).

1. (Condizionale) Compila le informazioni nella sezione [Regole di inclusione](/help/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion).

1. (Condizionale) Compila le informazioni nella sezione [Attributo Weighting](/help/c-recommendations/c-algorithms/create-new-algorithm.md#weighting).

1. Nella sezione **[!UICONTROL Carica CSV]**, selezionate la **[!UICONTROL Posizione]** del file CSV.

   ![Carica sezione CSV](/help/c-recommendations/c-algorithms/assets/upload-csv.png)

   Il file CSV deve essere formattato correttamente per essere caricato con successo. Fai clic su **[!UICONTROL Scarica il modello CSV]** per ottenere un file CSV formattato correttamente.

   Puoi scegliere tra due opzioni di posizione:

   * **FTP:** per caricare il file CSV da un server FTP, seleziona **[!UICONTROL FTP]**, quindi inserisci le informazioni richieste. Hai la possibilità di scegliere SSL, che utilizza il protocollo FTPS per trasferire il file CSV in modo sicuro.
   * **URL:** per caricare il file CSV da un URL, selezionate  **[!UICONTROL URL]**, quindi immettete un URL per il feed.

1. Fai clic su **[!UICONTROL Salva]**.

   >[!NOTE]
   >
   >Le entità di criteri personalizzati (righe) possono contenere fino a 1.000 elementi consigliati (colonne).

Gli aggiornamenti dei criteri personalizzati sono per impostazione predefinita “cumulativi”. Le nuove coppie chiave-valore specificate nel file di caricamento CSV sovrascrivono le coppie chiave-valore esistenti. Le coppie chiave-valore esistenti prive di chiavi specificate nel file CSV caricato continueranno a essere disponibili per la consegna e scadranno dopo 31 giorni, a partire dal momento in cui sono state caricate con il file CSV.

Contatta l&#39;assistenza clienti per consentire l&#39;eliminazione dei risultati esistenti non inclusi nel successivo caricamento CSV. Se questa impostazione è attivata, solo i tasti presenti nel file di feed CSV personalizzato saranno disponibili per la distribuzione. Questa impostazione si applica a tutti i criteri personalizzati.

I criteri personalizzati vengono aggiornati ogni 24 ore.

Puoi visualizzare lo stato di caricamento e sincronizzazione dei criteri personalizzati caricati nella parte inferiore di ogni scheda criteri nella pagina Consigli > Criteri. Puoi inoltre visualizzare lo stato nella finestra di dialogo Modifica durante la modifica dei criteri personalizzati.

Il flusso in caso di caricamento senza errori dovrebbe essere Programmato > Scarica file feed > Importazione > Corretto.

Di seguito sono riportati alcuni possibili messaggi di errore che potrebbero essere visualizzati se [!DNL Target] ha un problema con il caricamento:

| Messaggio di errore | Dettagli |
|--- |--- |
| Errore sconosciuto | Indica un errore tecnico interno. |
| Errore di analisi | Probabilmente si è verificato un problema con il formato di file feed. Correggere il formato di file e salvare nuovamente l&#39;algoritmo, che riavvierà il processo di download dei file. |
| Server non trovato | Fornisci un IP o un nome host visibile su Internet. |
| Errore di credenziali | Fornisci un nome utente e una password validi per un account attivo sul server. |
| Directory non trovata | Fornisci una directory esistente sul server. |
| File non trovato | Fornisci il nome di un file sul server nella directory indicata. |

## Video di formazione: Creare i criteri in Recommendations (12:33)  ![Badge di esercitazione](/help/assets/tutorial.png)

Questo video contiene le seguenti informazioni (i dettagli sul caricamento dei criteri personalizzati iniziano alle 11:43):

* Creare criteri
* Creare sequenze di criteri
* Caricare criteri personalizzati

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)