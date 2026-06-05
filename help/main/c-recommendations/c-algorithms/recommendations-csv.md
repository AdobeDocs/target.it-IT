---
keywords: creazione di criteri personalizzati;algoritmi;criteri;criteri di consigli;csv;ftp;caricamento csv
description: Scopri come caricare un file CSV per personalizzare i consigli in Adobe [!DNL Target] Recommendations.
title: Come posso caricare criteri personalizzati in  [!DNL Recommendations]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 33434121-e0ae-4b82-b1dd-78b9738026cb
TQID: https://experienceleague.adobe.com/8gSKOQxHGB5TPe6vdhjgy5sAFxN8O7dodITo7wgrR50
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 16fb7a1902ea76cab56a93fa141a32a3c6bc4467
workflow-type: tm+mt
source-wordcount: 696
ht-degree: 32%

---

# Caricare criteri personalizzati

Carica un file CSV per personalizzare i consigli in [!DNL Adobe Target].

Esistono diversi modi per raggiungere la schermata [!UICONTROL Crea nuovo criterio]. Alcune opzioni dipendono dal modo in cui si raggiunge la schermata.

* Nella schermata della libreria **[!UICONTROL Recommendations]** > **[!UICONTROL Criteri]**, fai clic su **[!UICONTROL Crea criterio]** > **[!UICONTROL Crea criterio]**. I criteri creati vengono automaticamente resi disponibili per tutte le attività di [!DNL Recommendations].
* Quando crei un&#39;attività [!DNL Recommendations] utilizzando il [!UICONTROL Compositore esperienza visivo], viene visualizzata immediatamente la schermata [!UICONTROL Seleziona criteri] dopo aver selezionato un elemento nella pagina e aver fatto clic su [!UICONTROL Sostituisci con consigli], [!UICONTROL Inserisci consigli prima] o [!UICONTROL Inserisci consigli dopo]. È quindi possibile selezionare un criterio disponibile oppure fare clic su **[!UICONTROL Crea criterio]**. Se si crea un nuovo criterio, è possibile salvarlo per utilizzarlo con altre attività di [!DNL Recommendations]. Per ulteriori informazioni, vedere [Creare un&#39;attività Consigli](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* Quando modifichi un&#39;attività [!DNL Recommendations], fai clic su una casella di [!UICONTROL Posizione consigli] nella pagina e seleziona **[!UICONTROL Cambia criteri]**. Nella schermata [!UICONTROL Seleziona criteri], fai clic su **[!UICONTROL Crea criteri]**. È possibile salvare i nuovi criteri da utilizzare con altre attività di [!DNL Recommendations].

La procedura seguente presuppone che tu acceda alla schermata [!UICONTROL Crea nuovo criterio] utilizzando il primo metodo: la schermata della libreria **[!UICONTROL Consigli]** > **[!UICONTROL Criteri]**.

1. Fai clic su **[!UICONTROL Consigli]** > **[!UICONTROL Criteri]**.

1. Fai clic su **[!UICONTROL Crea criterio]** > **[!UICONTROL Crea criterio]**.

1. Immettere le informazioni nella sezione [Informazioni di base](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info).

1. Dall&#39;elenco a discesa **[!UICONTROL Seleziona tipo di algoritmo]**, selezionare **[!UICONTROL Criteri personalizzati]**.

1. Dall&#39;elenco a discesa **[!UICONTROL Algoritmo]**, selezionare **[!UICONTROL Algoritmo personalizzato]**.

   >[!NOTE]
   >
   >I passaggi precedenti causano la visualizzazione della sezione [!UICONTROL Carica CSV] nella parte inferiore della finestra di dialogo [!UICONTROL Crea criterio].

1. (Condizionale) Inserisci le informazioni nella sezione [Contenuto di backup](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content).

1. (Condizionale) Inserisci le informazioni nella sezione [Regole di inclusione](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion).

1. Nella sezione **[!UICONTROL Carica CSV]**, seleziona il **[!UICONTROL Percorso]** del file CSV.

   Il file CSV deve essere formattato correttamente per essere caricato con successo. Fai clic su **[!UICONTROL Scarica il modello CSV]** per ottenere un file CSV formattato correttamente.

   Puoi scegliere tra due opzioni di posizione:

   * **FTP:** Per caricare il file CSV da un server FTP, selezionare **[!UICONTROL FTP]**, quindi immettere le informazioni richieste. Puoi utilizzare SSL, che utilizza il protocollo FTPS per trasferire il file CSV in modo sicuro.

   * **URL:** Per caricare il file CSV da un URL, seleziona **[!UICONTROL URL]**, quindi immetti un URL di feed.

1. Fai clic su **[!UICONTROL Crea]**.

## Considerazioni

* Le entità di criteri personalizzati (righe) possono contenere fino a 1.000 elementi consigliati (colonne).

* Gli aggiornamenti dei criteri personalizzati sono per impostazione predefinita “cumulativi”. Le nuove coppie chiave-valore specificate nel file di caricamento CSV sovrascrivono le coppie chiave-valore esistenti. Le coppie chiave-valore esistenti prive di chiavi specificate nel file CSV caricato sono ancora disponibili per la consegna e scadono dopo 31 giorni dal momento in cui sono state caricate per l’ultima volta come parte del file CSV.

  Contatta l&#39;assistenza clienti per consentire l&#39;eliminazione dei risultati esistenti non inclusi nel successivo caricamento CSV. Se questa impostazione è abilitata, solo i tasti presenti nel file di feed CSV personalizzato sono disponibili per la consegna. Questa impostazione si applica a tutti i criteri personalizzati.

* I criteri personalizzati vengono aggiornati ogni 24 ore.

  Puoi visualizzare lo stato di caricamento e sincronizzazione dei criteri personalizzati caricati per ogni criterio nella pagina [!UICONTROL Consigli] > [!UICONTROL Criteri]. È inoltre possibile visualizzare lo stato nella finestra di dialogo [!UICONTROL Modifica] durante la modifica dei criteri personalizzati.

* Il flusso per un caricamento senza errori deve essere [!UICONTROL Pianificato] > [!UICONTROL Download del file di feed] > [!UICONTROL Importazione] > [!UICONTROL Completato].

* Di seguito sono riportati i possibili messaggi di errore che potresti ricevere se [!DNL Target] riscontra un problema con il caricamento:

  | Messaggio di errore | Dettagli |
  |--- |--- |
  | Errore sconosciuto | Indica un errore tecnico interno. |
  | Errore di analisi | Probabilmente si è verificato un problema con il formato di file feed. Correggere il formato del file e salvare nuovamente l&#39;algoritmo, che riavvia il processo di download. |
  | Server non trovato | Fornisci un IP o un nome host visibile su Internet. |
  | Errore di credenziali | Fornisci un nome utente e una password validi per un account attivo sul server. |
  | Directory non trovata | Fornisci una directory esistente sul server. |
  | File non trovato | Fornisci il nome di un file sul server nella directory indicata. |
