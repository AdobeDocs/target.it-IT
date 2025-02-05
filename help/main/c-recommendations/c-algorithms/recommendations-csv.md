---
keywords: creazione di criteri personalizzati;algoritmi;criteri;criteri di consigli;csv;ftp;caricamento csv
description: Scopri come caricare un file CSV per personalizzare i consigli in Adobe [!DNL Target] Recommendations.
title: Come posso caricare criteri personalizzati in  [!DNL Recommendations]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 33434121-e0ae-4b82-b1dd-78b9738026cb
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 33%

---

# Caricare criteri personalizzati

Carica un file CSV per personalizzare i consigli in [!DNL Adobe Target].

Sono disponibili diversi modi per raggiungere la schermata [!UICONTROL Create New Criteria]. Alcune opzioni dipendono dal modo in cui si raggiunge la schermata.

* Nella schermata della libreria **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**, fare clic su **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**. I criteri creati vengono automaticamente resi disponibili per tutte le attività di [!DNL Recommendations].
* Quando crei un&#39;attività [!DNL Recommendations] utilizzando [!UICONTROL Visual Experience Composer] (VEC), vieni immediatamente reindirizzato alla schermata [!UICONTROL Select Criteria] dopo aver selezionato un elemento nella pagina e aver fatto clic su [!UICONTROL Replace w/ Recommendations], [!UICONTROL Insert Recommendations Before] o [!UICONTROL Insert Recommendations After]. È quindi possibile selezionare un criterio disponibile oppure fare clic su **[!UICONTROL Create Criteria]**. Se si crea un nuovo criterio, è possibile salvarlo per utilizzarlo con altre attività di [!DNL Recommendations]. Per ulteriori informazioni, vedere [Creare un&#39;attività Recommendations](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* Quando modifichi un&#39;attività di [!DNL Recommendations], fai clic su una casella di [!UICONTROL Recommendations Location] nella pagina e seleziona **[!UICONTROL Change Criteria]**. Nella schermata [!UICONTROL Select Criteria], fare clic su **[!UICONTROL Create Criteria]**. È possibile salvare i nuovi criteri da utilizzare con altre attività di [!DNL Recommendations].

Nei passaggi seguenti si presuppone che si acceda alla schermata [!UICONTROL Create New Criteria] utilizzando il primo metodo: la schermata della libreria **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Fare clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Fare clic su **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**.

1. Immettere le informazioni nella sezione [Informazioni di base](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info).

1. Dall&#39;elenco a discesa **[!UICONTROL Select Algorithm Type]**, selezionare **[!UICONTROL Custom Criteria]**.

1. Dall&#39;elenco a discesa **[!UICONTROL Algorithm]**, selezionare **[!UICONTROL Custom Algorithm]**.

   >[!NOTE]
   >
   >I passaggi precedenti causano la visualizzazione della sezione [!UICONTROL Upload CSV] nella parte inferiore della finestra di dialogo [!UICONTROL Create Criteria].

1. (Condizionale) Inserisci le informazioni nella sezione [Contenuto di backup](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content).

1. (Condizionale) Inserisci le informazioni nella sezione [Regole di inclusione](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion).

1. Nella sezione **[!UICONTROL Upload CSV]**, seleziona **[!UICONTROL Location]** del file CSV.

Il file CSV deve essere formattato correttamente per essere caricato con successo. Fare clic su **[!UICONTROL Download the CSV template]** per ottenere un file CSV formattato correttamente.

Puoi scegliere tra due opzioni di posizione:

    * **FTP:** Per caricare il file CSV da un server FTP, selezionare **[!UICONTROL FTP]**, quindi immettere le informazioni richieste. Puoi utilizzare SSL, che utilizza il protocollo FTPS per trasferire il file CSV in modo sicuro.
    
    * **URL:** Per caricare il file CSV da un URL, selezionare **[!UICONTROL URL]**, quindi immettere un URL di feed.

1. Fare clic su **[!UICONTROL Create]**.

## Considerazioni

* Le entità di criteri personalizzati (righe) possono contenere fino a 1.000 elementi consigliati (colonne).

* Gli aggiornamenti dei criteri personalizzati sono per impostazione predefinita “cumulativi”. Le nuove coppie chiave-valore specificate nel file di caricamento CSV sovrascrivono le coppie chiave-valore esistenti. Le coppie chiave-valore esistenti prive di chiavi specificate nel file CSV caricato sono ancora disponibili per la consegna e scadono dopo 31 giorni dal momento in cui sono state caricate per l’ultima volta come parte del file CSV.

  Contatta l&#39;assistenza clienti per consentire l&#39;eliminazione dei risultati esistenti non inclusi nel successivo caricamento CSV. Se questa impostazione è abilitata, solo i tasti presenti nel file di feed CSV personalizzato sono disponibili per la consegna. Questa impostazione si applica a tutti i criteri personalizzati.

* I criteri personalizzati vengono aggiornati ogni 24 ore.

  Puoi visualizzare lo stato di caricamento e sincronizzazione dei criteri personalizzati caricati per ciascun criterio nella pagina [!UICONTROL Recommendations] > [!UICONTROL Criteria]. È inoltre possibile visualizzare lo stato nella finestra di dialogo [!UICONTROL Edit] quando si modificano i criteri personalizzati.

* Il flusso per un caricamento senza errori deve essere [!UICONTROL Scheduled] > [!UICONTROL Downloading Feed File] > [!UICONTROL Importing] > [!UICONTROL Successful].

* Di seguito sono riportati i possibili messaggi di errore che potresti ricevere se [!DNL Target] riscontra un problema con il caricamento:

  | Messaggio di errore | Dettagli |
  |--- |--- |
  | Errore sconosciuto | Indica un errore tecnico interno. |
  | Errore di analisi | Probabilmente si è verificato un problema con il formato di file feed. Correggere il formato del file e salvare nuovamente l&#39;algoritmo, che riavvia il processo di download. |
  | Server non trovato | Fornisci un IP o un nome host visibile su Internet. |
  | Errore di credenziali | Fornisci un nome utente e una password validi per un account attivo sul server. |
  | Directory non trovata | Fornisci una directory esistente sul server. |
  | File non trovato | Fornisci il nome di un file sul server nella directory indicata. |
