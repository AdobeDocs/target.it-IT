---
keywords: creazione di criteri personalizzati;algoritmi;criteri;criteri di consigli;csv;ftp;caricamento csv
description: Scopri come caricare un file CSV per personalizzare i consigli in Adobe [!DNL Target] Recommendations.
title: Come si caricano i criteri personalizzati in Recommendations?
feature: Recommendations
exl-id: 33434121-e0ae-4b82-b1dd-78b9738026cb
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 39%

---

# ![PREMIUM](/help/main/assets/premium.png) Caricare criteri personalizzati

Carica un file CSV per personalizzare i consigli in [!DNL Adobe Target].

Esistono diversi modi per raggiungere la schermata [!UICONTROL Crea nuovo criterio]. Alcune opzioni dipendono dal modo in cui si raggiunge la schermata.

* Sulla **[!UICONTROL Recommendations]** > **[!UICONTROL Criteri]** libreria, fai clic su **[!UICONTROL Creare criteri]** > **[!UICONTROL Creare criteri]**. I criteri creati vengono automaticamente resi disponibili per tutte le attività di [!DNL Recommendations].
* Quando crei un [!DNL Recommendations] utilizzando [!UICONTROL Compositore esperienza visivo] (Compositore esperienza visivo), vieni immediatamente portato al [!UICONTROL Seleziona criteri] dopo aver selezionato un elemento nella pagina e aver fatto clic su [!UICONTROL Sostituisci con Recommendations], [!UICONTROL Inserisci Recommendations prima]oppure [!UICONTROL Inserisci Recommendations dopo]. Puoi quindi selezionare un criterio disponibile oppure fare clic su **[!UICONTROL Creare criteri]**. Se crei un nuovo criterio, puoi salvarne l’utilizzo con altri [!DNL Recommendations] attività. Per ulteriori informazioni, consulta [Creare un’attività Recommendations](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* Quando modifichi un’attività di [!DNL Recommendations], fai clic su una casella di [!UICONTROL Posizione Consigli] nella pagina e seleziona **[!UICONTROL Cambia criteri]**. Sulla [!UICONTROL Seleziona criteri] schermata, fai clic su **[!UICONTROL Creare criteri]**. Puoi salvare i nuovi criteri da utilizzare con altri [!DNL Recommendations] attività.

I passaggi seguenti presuppongono l’accesso al [!UICONTROL Creare nuovi criteri] utilizzando il primo metodo: la **[!UICONTROL Recommendations]** > **[!UICONTROL Criteri]** libreria.

1. Fai clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Criteri]**.

1. Fai clic su **[!UICONTROL Crea criterio]**.

1. Compila le informazioni nel [Informazioni di base](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) sezione .

   1. Da **[!UICONTROL Seleziona algoritmo]** Elenco a discesa Tipo , seleziona **[!UICONTROL Criteri personalizzati]**.

   1. Da **[!UICONTROL Algoritmo]** elenco a discesa, seleziona **[!UICONTROL Algoritmo personalizzato]**.

      >[!NOTE]
      >
      >Le fasi precedenti causano la [!UICONTROL Carica CSV] da visualizzare nella parte inferiore della sezione [!UICONTROL Creare nuovi criteri] finestra di dialogo.

1. (Condizionale) Compila le informazioni nel [Contenuto backup](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content) sezione .

1. (Condizionale) Compila le informazioni nel [Regole di inclusione](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion) sezione .

1. In **[!UICONTROL Carica CSV]** seleziona la sezione **[!UICONTROL Posizione]** del file CSV.

   ![Sezione Carica CSV](assets/upload-csv.png)

   Il file CSV deve essere formattato correttamente per essere caricato con successo. Fai clic su **[!UICONTROL Scarica il modello CSV]** per ottenere un file CSV formattato correttamente.

   Puoi scegliere tra due opzioni di posizione:

   * **FTP:** per caricare il file CSV da un server FTP, seleziona **[!UICONTROL FTP]**, quindi inserisci le informazioni richieste. Puoi utilizzare SSL, che utilizza il protocollo FTPS per trasferire il file CSV in modo sicuro.
   * **URL:** Per caricare il file CSV da un URL, seleziona **[!UICONTROL URL]**, quindi immetti un URL di feed.

1. Fai clic su **[!UICONTROL Salva]**.

## Considerazioni

* Le entità di criteri personalizzati (righe) possono contenere fino a 1.000 elementi consigliati (colonne).

* Gli aggiornamenti dei criteri personalizzati sono per impostazione predefinita “cumulativi”. Le nuove coppie chiave-valore specificate nel file di caricamento CSV sovrascrivono le coppie chiave-valore esistenti. Le coppie chiave-valore esistenti prive di chiavi specificate nel caricamento CSV sono ancora disponibili per la consegna e scadono dopo 31 giorni dal loro ultimo caricamento come parte del file CSV.

   Contatta l&#39;assistenza clienti per consentire l&#39;eliminazione dei risultati esistenti non inclusi nel successivo caricamento CSV. Se questa impostazione è abilitata, solo i tasti presenti nel file di feed CSV personalizzato sono disponibili per la consegna. Questa impostazione si applica a tutti i criteri personalizzati.

* I criteri personalizzati vengono aggiornati ogni 24 ore.

   Puoi visualizzare lo stato di caricamento e sincronizzazione dei criteri personalizzati caricati nella parte inferiore di ogni scheda criteri nel [!UICONTROL Recommendations] > [!UICONTROL Criteri] pagina. Puoi anche visualizzare lo stato nel [!UICONTROL Modifica] finestra di dialogo per la modifica dei criteri personalizzati.

* Il flusso per un caricamento senza errori deve essere [!UICONTROL Pianificato] > [!UICONTROL Download del file di feed] > [!UICONTROL Importazione] > [!UICONTROL Operazione riuscita].

* Di seguito sono riportati i possibili messaggi di errore che potresti ricevere se [!DNL Target] rileva un problema con il caricamento:

   | Messaggio di errore | Dettagli |
   |--- |--- |
   | Errore sconosciuto | Indica un errore tecnico interno. |
   | Errore di analisi | Probabilmente si è verificato un problema con il formato di file feed. Correggere il formato del file e salvare nuovamente l&#39;algoritmo, che riavvia il processo di download del file. |
   | Server non trovato | Fornisci un IP o un nome host visibile su Internet. |
   | Errore di credenziali | Fornisci un nome utente e una password validi per un account attivo sul server. |
   | Directory non trovata | Fornisci una directory esistente sul server. |
   | File non trovato | Fornisci il nome di un file sul server nella directory indicata. |

## Video di formazione: Creare i criteri in Recommendations (12:33) ![Icona Tutorial](/help/main/assets/tutorial.png)

Questo video contiene le seguenti informazioni (i dettagli sul caricamento di criteri personalizzati iniziano alle 11:43):

* Creare criteri
* Creare sequenze di criteri
* Caricare criteri personalizzati

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
