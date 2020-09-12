---
keywords: creating custom criteria;algorithms;criteria;recommendations criteria;csv;ftp;upload csv
description: Carica un file CSV per personalizzare i consigli.
title: Caricare criteri personalizzati
feature: criteria
uuid: e0b4d320-db00-43ad-b49e-ce36c8532320
translation-type: tm+mt
source-git-commit: 108bbe65732b7df20caf9df6b3e5b77e3c31c457
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 63%

---


# ![PREMIUM](/help/assets/premium.png) Caricare criteri personalizzati{#upload-custom-criteria}

Carica un file CSV per personalizzare i consigli.

Esistono diversi modi per raggiungere la schermata [!UICONTROL Crea nuovo criterio]. Alcune opzioni dipendono dal modo in cui si raggiunge la schermata.

* On the **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** library screen, click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**. I criteri creati vengono automaticamente resi disponibili per tutte le attività di [!DNL Recommendations].
* Quando create un&#39; [!DNL Recommendations] attività utilizzando Visual Experience Composer (VEC) (Compositore esperienza [!UICONTROL visivo] ), viene visualizzata immediatamente la schermata [!UICONTROL Select Criteria (Seleziona criteri] ) dopo che avete selezionato un elemento nella pagina e fate clic su [!UICONTROL Replace w/ Recommendations], [!UICONTROL Insert Recommendations Before](Inserisci prima [!UICONTROL ) o]Insert Recommendations After. Potete quindi selezionare un criterio disponibile oppure fare clic su **[!UICONTROL Crea criteri]**. Se create un nuovo criterio, potete salvare i criteri da usare con altre [!DNL Recommendations] attività. For more information, see [Create a Recommendations activity](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* Quando modifichi un’attività di [!DNL Recommendations], fai clic su una casella di [!UICONTROL Posizione Consigli] nella pagina e seleziona **[!UICONTROL Cambia criteri]**. On the [!UICONTROL Select Criteria] screen, click **[!UICONTROL Create Criteria]**. Sarà possibile salvare i nuovi criteri da utilizzare per altre attività di [!DNL Recommendations].

Nella procedura seguente si presuppone che sia possibile accedere alla schermata [!UICONTROL Crea nuovo criterio] utilizzando il primo metodo: nella schermata Libreria **[!UICONTROL Recommendations]** > **[!UICONTROL Criteri]** .

1. Fate clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Criteri]**.

1. Fate clic su **[!UICONTROL Crea criteri]** > **[!UICONTROL Carica criteri]** personalizzati.

1. Fill in the information in the [Basic Information](/help/c-recommendations/c-algorithms/create-new-algorithm.md#info) section.

1. Compila le informazioni nella sezione Origine [](/help/c-recommendations/c-algorithms/create-new-algorithm.md#data-source) dati.

1. Fill in the information in the [Content](/help/c-recommendations/c-algorithms/create-new-algorithm.md#content) section.

1. (Condizionale) Compila le informazioni nella sezione [Somiglianza](/help/c-recommendations/c-algorithms/create-new-algorithm.md#similarity) contenuto.

1. (Condizionale) Compila le informazioni nella sezione [Regole](/help/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion) di inclusione.

1. (Riempimento condizionale nelle informazioni nella sezione Ponderazione [](/help/c-recommendations/c-algorithms/create-new-algorithm.md#weighting) attributo.

1. Nella sezione **[!UICONTROL Carica CSV]** , selezionate la **[!UICONTROL posizione]** del file CSV.

   ![Carica sezione CSV](/help/c-recommendations/c-algorithms/assets/upload-csv.png)

   Il file CSV deve essere formattato correttamente per essere caricato con successo. Fai clic su **[!UICONTROL Scarica il modello CSV]** per ottenere un file CSV formattato correttamente.

   Puoi scegliere tra due opzioni di posizione:

   * **FTP:** per caricare il file CSV da un server FTP, seleziona **[!UICONTROL FTP]**, quindi inserisci le informazioni richieste. Hai la possibilità di scegliere SSL, che utilizza il protocollo FTPS per trasferire il file CSV in modo sicuro.
   * **URL:** Per caricare il file CSV da un URL, selezionate **[!UICONTROL URL]**, quindi immettete un URL per feed.

1. Fai clic su **[!UICONTROL Salva]**.

   >[!NOTE]
   >
   >Le entità di criteri personalizzati (righe) possono contenere fino a 1.000 elementi consigliati (colonne).

Gli aggiornamenti dei criteri personalizzati sono per impostazione predefinita “cumulativi”. Le nuove coppie chiave-valore specificate nel file di caricamento CSV sovrascrivono le coppie chiave-valore esistenti. Le coppie chiave-valore esistenti prive di chiavi specificate nel file CSV caricato continueranno a essere disponibili per la consegna e scadranno dopo 31 giorni, a partire dal momento in cui sono state caricate con il file CSV.

Contatta l&#39;assistenza clienti per consentire l&#39;eliminazione dei risultati esistenti non inclusi nel successivo caricamento CSV. Se questa impostazione è attivata, solo i tasti presenti nel file di feed CSV personalizzato saranno disponibili per la distribuzione. Questa impostazione si applica a tutti i criteri personalizzati.

I criteri personalizzati vengono aggiornati ogni 24 ore.

Puoi visualizzare lo stato di caricamento e sincronizzazione dei criteri personalizzati caricati nella parte inferiore di ogni scheda criteri nella pagina Consigli > Criteri. Puoi inoltre visualizzare lo stato nella finestra di dialogo Modifica durante la modifica dei criteri personalizzati.

Il flusso in caso di caricamento senza errori dovrebbe essere Programmato > Scarica file feed > Importazione > Corretto.

The following are possible error messages you might receive if [!DNL Target] encounters a problem with the upload:

| Messaggio di errore | Dettagli |
|--- |--- |
| Errore sconosciuto | Indica un errore tecnico interno. |
| Errore di analisi | Probabilmente si è verificato un problema con il formato di file feed. Correggere il formato di file e salvare nuovamente l&#39;algoritmo, che riavvierà il processo di download dei file. |
| Server non trovato | Fornisci un IP o un nome host visibile su Internet. |
| Errore di credenziali | Fornisci un nome utente e una password validi per un account attivo sul server. |
| Directory non trovata | Fornisci una directory esistente sul server. |
| File non trovato | Fornisci il nome di un file sul server nella directory indicata. |

## Video di formazione: Creare i criteri in Recommendations (12:33) ![Badge di esercitazione](/help/assets/tutorial.png)

Questo video contiene le seguenti informazioni (i dettagli sul caricamento dei criteri personalizzati iniziano alle 11:43):

* Creare criteri
* Creare sequenze di criteri
* Caricare criteri personalizzati

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)