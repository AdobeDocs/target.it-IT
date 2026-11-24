---
keywords: creazione di criteri personalizzati;algoritmi;criteri;criteri consigli;csv;ftp;caricare csv
description: Scopri come caricare un file CSV per personalizzare i consigli in Adobe [!DNL Target] Recommendations.
title: Caricare criteri personalizzati
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 33434121-e0ae-4b82-b1dd-78b9738026cb
TQID: 'https://experienceleague.adobe.com/8gSKOQxHGB5TPe6vdhjgy5sAFxN8O7dodITo7wgrR50'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 14%
---
# Caricare criteri personalizzati {#upload-custom-criteria}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come caricare un file CSV di consigli per creare criteri personalizzati in [!DNL Adobe Target Recommendations].

>[!ENDSHADEBOX]

I criteri personalizzati utilizzano un file CSV di consigli caricato in [!DNL Target]. In questo modo i consigli calcolati al di fuori di [!DNL Target] possono essere consegnati in [!DNL Recommendations] attività. Per ulteriori informazioni sul funzionamento dei criteri personalizzati, vedere [La scienza alla base degli algoritmi di Recommendations di Target](/help/main/c-recommendations/c-algorithms/recommendations-algorithms.md).

I criteri personalizzati vengono creati dalla schermata **[!UICONTROL Crea nuovo criterio]**. Per informazioni su come raggiungere questa schermata, vedere [Accedere alla schermata Crea nuovo criterio](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#access-create-criteria). I passaggi seguenti iniziano dalla schermata della libreria **[!UICONTROL Consigli]** > **[!UICONTROL Criteri]**.

1. Fai clic su **[!UICONTROL Consigli]** > **[!UICONTROL Criteri]**.

1. Fai clic su **[!UICONTROL Crea criterio]** > **[!UICONTROL Crea criterio]**.

   ![Pagina Criteri con il menu Crea criteri aperto, che mostra Crea criteri e Crea sequenza criteri](../assets/criteria_create_1.png)

1. Immettere le informazioni nella sezione [Informazioni di base](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info).

1. Dall&#39;elenco a discesa **[!UICONTROL Seleziona tipo di algoritmo]**, selezionare **[!UICONTROL Criteri personalizzati]**. Dall&#39;elenco a discesa **[!UICONTROL Algoritmo]**, selezionare **[!UICONTROL Algoritmo personalizzato]**.

   ![Sezione Algoritmo Consigli con Criteri personalizzati come Tipo di algoritmo e Algoritmo personalizzato come Algoritmo](../assets/criteria_create_9.png)

1. (Condizionale) Inserisci le informazioni nelle sezioni [Contenuto di backup](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content) e [Regole di inclusione](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion).

1. Nella sezione **[!UICONTROL Carica CSV]**, seleziona il **[!UICONTROL Percorso]** del file CSV.

   Il file CSV deve essere formattato correttamente per essere caricato con successo. Per ottenere un file CSV formattato correttamente, fare clic su **[!UICONTROL Scarica il modello CSV]**.

   Sono disponibili le seguenti opzioni di posizione:

   * **FTP**: per caricare il file CSV da un server FTP, selezionare **[!UICONTROL FTP]**, quindi immettere le informazioni richieste. È possibile utilizzare SSL, che utilizza il protocollo FTPS per trasferire il file CSV in modo sicuro.

   * **SFTP**: per caricare il file CSV da un server SFTP, seleziona **[!UICONTROL SFTP]**, quindi immetti il nome host o l&#39;indirizzo IP, la porta (impostazione predefinita: 22), il nome utente, una password e/o la chiave privata SSH, la directory e il nome file. Per informazioni dettagliate, consulta [Impostazioni del server SFTP supportate](/help/main/c-recommendations/c-products/feeds.md#steps).

     SFTP non modifica il formato CSV dei criteri personalizzati. Utilizza il formato `# Key,Recommendation_1,...`. Un file CSV nel formato di un tipo di feed diverso causa un errore di importazione.

   * **URL**: per caricare il file CSV da un URL, seleziona **[!UICONTROL URL]**, quindi immetti un URL di feed.

     ![Carica sezione CSV con le opzioni Posizione FTP, SFTP e URL evidenziate e SFTP selezionato](../assets/criteria_create_10.png)

1. Fai clic su **[!UICONTROL Crea]**.

## Considerazioni

* Le entità di criteri personalizzati (righe) possono contenere fino a 1.000 elementi consigliati (colonne).

* Gli aggiornamenti dei criteri personalizzati sono &quot;cumulativi&quot; per impostazione predefinita. Le nuove coppie chiave-valore nel file di caricamento CSV sovrascrivono le coppie chiave-valore esistenti. Le coppie chiave-valore esistenti le cui chiavi non sono nel caricamento CSV rimangono disponibili per la consegna e scadono 31 giorni dopo l’ultimo caricamento come parte del file CSV.

  Per eliminare i risultati esistenti non inclusi nel successivo caricamento CSV, contatta l’Assistenza clienti per abilitare l’impostazione corrispondente. Quando questa impostazione è abilitata, solo i tasti presenti nel file di feed CSV personalizzato sono disponibili per la consegna. Questa impostazione si applica a tutti i criteri personalizzati.

* I criteri personalizzati vengono aggiornati ogni 24 ore.

  Lo stato di caricamento e sincronizzazione di ogni caricamento di criteri personalizzati viene visualizzato nella pagina **[!UICONTROL Consigli]** > **[!UICONTROL Criteri]**. Lo stato viene visualizzato anche nella finestra di dialogo **[!UICONTROL Modifica]** quando vengono modificati i criteri personalizzati.

* Il flusso per un caricamento senza errori è **[!UICONTROL Pianificato]** > **[!UICONTROL Download del file di feed]** > **[!UICONTROL Importazione]** > **[!UICONTROL Completato]**.

* Se [!DNL Target] riscontra un problema con il caricamento, sono possibili i seguenti messaggi di errore:

  | Messaggio di errore | Dettagli |
  |--- |--- |
  | Errore sconosciuto | Indica un errore tecnico interno. |
  | Errore di analisi | Probabilmente si è verificato un problema con il formato di file feed. Correggere il formato del file e salvare nuovamente l&#39;algoritmo, che riavvia il processo di download. |
  | Server non trovato | Specifica un nome IP o host visibile su Internet. |
  | Errore di credenziali | Fornisci un nome utente e una password validi per un account attivo sul server. |
  | Directory non trovata | Fornisci una directory esistente sul server. |
  | File non trovato | Specificare il nome di un file esistente sul server nella directory specificata. |
