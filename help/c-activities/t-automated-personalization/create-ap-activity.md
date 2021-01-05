---
keywords: automated personalization;ap;audiences;ensemble;random forest;residual variance;error variance;lifetime value
description: Il flusso di lavoro  attività Automated Personalization in  Adobe Target varia dal flusso di lavoro degli altri tipi di attività.
title: Creare un'attività di personalizzazione automatizzata
feature: Automated Personalization
translation-type: tm+mt
source-git-commit: 4adade56529fb95e4400e06d04d3c6c69e120edc
workflow-type: tm+mt
source-wordcount: '2040'
ht-degree: 92%

---


# ![PREMIUM](/help/assets/premium.png) Creare un’attività di personalizzazione automatizzata

Il flusso di lavoro dell&#39;attività [!UICONTROL  Automated Personalization] (AP) in [!DNL Adobe Target] varia a seconda del flusso di lavoro degli altri tipi di attività.

1. Nell&#39;elenco [!DNL Target] [!UICONTROL Attività], fare clic su **[!UICONTROL Crea attività]** > **[!UICONTROL Automated Personalization]**.

   ![Crea attività: Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/assets/ap_create-new.png)

1. Per utilizzare [!UICONTROL Visual Experience Composer (Compositore esperienza visivo)] (VEC), fate clic su **[!UICONTROL Visual (Predefinito)]**.

   ![Finestra di dialogo Crea attività di personalizzazione automatizzata](/help/c-activities/t-automated-personalization/assets/ap_url-new.png)

   Se preferite utilizzare [!UICONTROL Form-Based Experience Composer], selezionate [!UICONTROL Form]. Per ulteriori informazioni, consulta [Compositore esperienza basato su moduli](/help/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Oltre a VEC e [!UICONTROL Form-Based Experience Composer], [!DNL Target] offre la [!UICONTROL Single Page Application VEC] e la VEC for Mobile Apps. Per ulteriori informazioni sui vari moduli di composizione, consulta [Esperienze e offerte](/help/c-experiences/experiences.md).
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, consulta [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >L’opzione [!UICONTROL Choose Workplace] (Scegli luogo di lavoro) nell’illustrazione precedente è una funzione di [Target Premium](/help/c-intro/intro.md). Se la tua organizzazione dispone di una licenza di Target Standard, questa opzione non è disponibile.

1. (Condizionale) Se siete un cliente [!DNL Target] Premium, [scegliete un&#39;area di lavoro](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. Verifica o inserisci l’URL di attività, quindi fai clic su **[!UICONTROL Avanti]**.

   >[!NOTE]
   >
   >[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `http://www.adobe.com`] e [!DNL `https://wwww.adobe.com`] sono entrambi validi.

   La pagina con l’URL specificato viene visualizzata nel Compositore esperienza visivo.

1. Per assegnare un nome all&#39;attività, fate clic sul campo **[!UICONTROL Name]** e digitate il nome dell&#39;attività.

   ![Campo Nome](/help/c-activities/t-automated-personalization/assets/ab_newname-new.png)

   I seguenti caratteri non sono consentiti nel nome di un’attività:

   | Carattere | Descrizione |
   |--- |--- |
   | / | Barra |
   | ? | Punto interrogativo |
   | # | Cancelletto |
   | : | Due punti |
   | = | Uguale |
   | + | Più |
   | - | Meno |
   | @ | Chiocciola |

1. Modifica gli elementi della pagina come descritto in [Opzioni del Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/viztarget-options.md).

   È possibile selezionare più immagini contemporaneamente dal gestore delle risorse. In questo modo è possibile visualizzare rapidamente la pagina con ciascuna delle immagini configurate per l&#39;attività. Inoltre è possibile modificare facilmente gli elementi di testo nelle offerte. Quando si modifica un elemento, su tale elemento vengono visualizzate delle barre per indicare che è stato modificato.

1. Fai clic su **[!UICONTROL Gestisci contenuto]** per configurare le combinazioni disponibili.

   ![Opzione Gestione contenuto](/help/c-activities/t-automated-personalization/assets/manage-content.png)

   Viene visualizzata una finestra di dialogo con tre opzioni nella parte superiore dello schermo: Esperienze, Offerte e Gruppi di esclusione.

   ![Finestra di dialogo Gestione contenuto](/help/c-activities/t-automated-personalization/assets/ap_content-new.png)

   >[!NOTE]
   >
   >Anche se è possibile creare fino a 30.000 esperienze in un’attività Personalizzazione automatizzata, l’attività fornisce migliori prestazioni quando si utilizzano meno di 5.000 esperienze.

   L’elenco [!UICONTROL Esperienze] mostra ogni elemento di contenuto selezionato per l’attività e la posizione a cui è assegnato.

   Per escludere esperienze specifiche, passa il cursore sopra l’esperienza desiderata e fai clic sull’icona Escludi.

   ![Icona Escludi per una singola esperienza](/help/c-activities/t-automated-personalization/assets/icon-exclude.png)

   Oppure, per escludere o includere più esperienze in blocco, seleziona la casella di controllo delle esperienze rilevanti e fai clic su Escludi in alto a destra nella finestra di dialogo.

   ![Opzioni di esclusione per più esperienze](/help/c-activities/t-automated-personalization/assets/batch-exclude.png)

   Per filtrare l’elenco in modo da visualizzare solo le attività escluse o incluse, fai clic sull’elenco a discesa **Stato**.

1. (Facoltativo) Fai clic su **[!UICONTROL Offerte]** per selezionare parti di contenuto e assegnarle a gruppi di reporting o per consentire solamente a determinati visitatori di visualizzare alcune offerte con targeting.

   Per ulteriori informazioni, consulta [Gruppi di reporting delle offerte in Personalizzazione automatizzata](/help/c-reports/offer-reporting-groups-in-automated-personalization.md#concept_194128C0B56B4B26AAB57DB49892960C).

   Utilizza l&#39;elenco [!UICONTROL Posizione] per filtrare le offerte in base alla posizione. Utilizza l&#39;elenco [!UICONTROL Gruppo di rapporti] per filtrare le offerte in base ai gruppi di rapporti. È inoltre possibile utilizzare l&#39;elenco [!UICONTROL Gruppo di rapporti] per filtrare le [!UICONTROL Offerte non assegnate] così da poter assegnare un gruppo di rapporti a un&#39;offerta attualmente non assegnata ad alcun gruppo di rapporti.

   Per aggiungere esperienze specifiche a un gruppo di reporting, passa il cursore sull’offerta desiderata e fai clic sull’icona della cartella.

   ![Icona della cartella](/help/c-activities/t-automated-personalization/assets/icon-folder.png)

   Per raccogliere più esperienze in un gruppo di reporting, seleziona la casella di controllo delle esperienze desiderate e fai clic sull’icona della cartella Gruppo di reporting in alto a destra nella finestra di dialogo.

   ![Opzioni Gruppo di reporting](/help/c-activities/t-automated-personalization/assets/report-group-options.png)

   È importante comprendere che i gruppi di rapporti incidono sul modo in cui Target genera i propri modelli. Di conseguenza, è consigliabile utilizzare i gruppi di rapporti solo se si prevede di sostituire o aggiungere nuove offerte mentre l&#39;attività è in corso. Se una nuova offerta viene introdotta in un&#39;attività in corso, inserire la nuova offerta in un gruppo con offerte analoghe esistenti permette alla macchina di utilizzare i dati già raccolti per le altre offerte del suo gruppo così da conoscere la nuova offerta. È sconsigliabile mettere tutte le offerte in un unico gruppo di rapporti.

   Per informazioni su come indirizzare un’offerta a tipi di pubblico specifici, consulta [Offerte Personalizzazione automatizzata di Target](/help/c-activities/t-automated-personalization/ap-target-offers.md#task_F207ED7A41B84FD39BB6FCBFABF4B23E).

1. (Condizionale) Fai clic su **[!UICONTROL Gruppi di esclusione]** per scegliere le combinazioni di elementi da escludere dall’attività.

   ![Scheda Gruppi di esclusione della finestra di dialogo Gestione contenuto](/help/c-activities/t-automated-personalization/assets/exclusion_groups-new.png)

   Anche se è possibile creare fino a 30.000 esperienze in un test di Personalizzazione automatizzata, l&#39;algoritmo fornisce prestazioni migliori quando si utilizzano meno di 10.000 esperienze.

   Se nell&#39;attività non sono presenti gruppi di esclusione, fai clic su **Crea gruppo di esclusione**. È possibile filtrare l&#39;attività per creare un elenco che mostra solo le combinazioni che desideri escludere. Denomina il gruppo di esclusione e fai clic su **Salva**.

   Per modificare un gruppo di esclusione esistente, posiziona il puntatore del mouse sul gruppo che desideri modificare, quindi fai clic sull&#39;icona a forma di matita.

1. Una volta completata l’impostazione del contenuto dell’attività, fai clic su **[!UICONTROL Fine]**.

1. Se hai già utilizzato altri tipi di attività di Target, la fase di **Targeting** ti risulterà familiare. Qui puoi selezionare un pubblico e specificare la percentuale di visitatori che vedranno l&#39;esperienza di controllo facendo clic sull&#39;elenco a discesa **[!UICONTROL Personalizza allocazione]**, quindi fai clic su **Successivo**.

   L’elenco a discesa [!UICONTROL Personalizza allocazione] consente di scegliere tra le seguenti opzioni:

   ![Elenco a discesa Obiettivo di allocazione traffico](/help/c-activities/t-automated-personalization/assets/traffic-allocation-goal-ap.png)

   * **Valuta algoritmo di personalizzazione (50/50):** se l’obiettivo è quello di testare l’algoritmo, assegna il 50% dei visitatori all’algoritmo di controllo e l’altro 50% a quello di destinazione. Questa suddivisione fornisce la stima più accurata dell’incremento. È consigliata quando il controllo è impostato su “Esperienze casuali”.
   * **Massimizza traffico personalizzazione (90/10):** se il tuo obiettivo è invece quello di creare un’attività “sempre attiva”, inserisci il 10% dei visitatori nel controllo affinché ci siano abbastanza dati per consentire agli algoritmi di continuare a imparare nel tempo. In questo caso, considera che la personalizzazione di una proporzione maggiore del traffico va a scapito della precisione nell’incremento rilevato. Indipendentemente dall’obiettivo, questa è la suddivisione del traffico consigliata quando si utilizza come controllo un’esperienza specifica.
   * **Personalizza allocazione**: specifica manualmente la percentuale di suddivisione, in base alle tue esigenze.

1. (Condizionale) Dall’elenco a discesa [!UICONTROL Controllo], [seleziona un’esperienza specifica da usare come controllo](/help/c-activities/t-automated-personalization/experience-as-control.md) oppure seleziona [!UICONTROL Esperienza casuale.]

   L&#39;esperienza di controllo fornisce un confronto per determinare l&#39;incremento fornito dal test automatizzato.

   Nella personalizzazione automatizzata le prestazioni vengono sempre misurate in base al confronto con un gruppo di controllo. La migliore prassi è quella di collocare almeno il 10% dei partecipanti nel gruppo di controllo. Se l&#39;obiettivo è quello di verificare se l&#39;algoritmo di personalizzazione sui dati stia fornendo migliori prestazioni rispetto all&#39;assenza di personalizzazione (vale a dire, il controllo eseguito in modo casuale), allora il modo più veloce e preciso per raggiungere questo obiettivo è la suddivisione di un 50% e l&#39;altro 50% del traffico tra il controllo e l&#39;algoritmo di personalizzazione. Se desideri massimizzare la quantità di traffico personalizzato e sei meno interessato a conoscere l&#39;incremento esatto generato dall&#39;attività, allora il modo più veloce e preciso per raggiungere questo obiettivo è la suddivisione del 10% e del 90% del traffico tra il controllo e l&#39;algoritmo di personalizzazione.

   >[!NOTE]
   >
   >Nelle attività di personalizzazione automatizzata, i criteri di ingresso (destinazione URL, regole modello e destinazione pubblico) vengono valutati per ogni richiesta. Nelle versioni precedenti, i criteri di ingresso venivano valutati una volta a sessione.

1. Fai clic su **[!UICONTROL Successivo]** per visualizzare la pagina **[!UICONTROL Obiettivi e impostazioni]**.
1. Configura l’attività con le impostazioni seguenti, quindi fai clic su **[!UICONTROL Salva e chiudi]**.

   | Impostazione | Descrizione |
   |--- |--- |
   | Nome | Assegna un nome all’attività. Attribuisci all&#39;attività un nome sufficientemente descrittivo da consentire ai membri del gruppo di riconoscerla nell&#39;elenco delle attività.  Consultate la tabella qui sopra per vedere quali caratteri non sono consentiti nel nome di un’attività. |
   | Finalità | (Facoltativo) Inserire la finalità del test. La finalità aiuta a ricordare lo scopo dell&#39;attività. |
   | Priorità | L’interfaccia utente e le opzioni per Priorità variano a seconda delle impostazioni. È possibile utilizzare le impostazioni legacy Bassa, Media o Alta, oppure attivare la priorità precisa da 0 a 999.<br>La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.<br>Se questa opzione non è abilitata in  [!UICONTROL Amministrazione] >   Reporting (impostazione predefinita), specificate una priorità: Bassa, Media o Alta.<br>Per abilitare le priorità con granulometria fine, fai clic su  [!UICONTROL Amministrazione] >  [!UICONTROL Rapporti], quindi seleziona l’opzione  [!UICONTROL Abilita ] priorità con granulosità fine per la posizione &quot;Attiva&quot;.<br>Se questa opzione è abilitata, specifica un valore compreso tra 0 e 999:<ul><li>0 = Bassa</li><li>999 = Alta</li></ul>Per le attività create con le versioni precedenti di Target Standard/Premium, la priorità Bassa viene convertita in 0, la priorità Media in 5 e la priorità Alta in 10. Se necessario, è possibile modificare questi valori.<br>**Nota**: prima di poter disabilitare questa opzione dopo aver utilizzato le priorità precise, tutte le priorità devono essere impostate su 0, 5 o 10. |
   | Durata | Imposta le date di inizio e di fine dell&#39;attività. |
   | Obiettivo di ottimizzazione | Specifica l&#39;obiettivo di ottimizzazione, costituito da due parametri:<ul><li>Ciò che desideri misurare con l&#39;attività</li><li>L&#39;azione intrapresa da un partecipante a un&#39;attività che dimostra che l&#39;obiettivo è stato raggiunto.</li></ul>È possibile scegliere di assegnare un nome all&#39;obiettivo di ottimizzazione, selezionando i tre punti a destra di “Il mio obiettivo principale”. Le attività personalizzazione automatizzata sono in grado di misurare conversione, RPV e AOV. La conversione può essere ottenuta mediante la visualizzazione di una pagina o di una mbox. È possibile inoltre il tracciamento dei clic.<br>L’obiettivo principale diventa anche la metrica di modellazione, utilizzata dal sistema di modellazione per calcolare il successo dell’esperienza.<br>I visitatori possono essere mantenuti nell&#39;attività per scopi di tracciamento, dopo aver raggiunto l&#39;obiettivo di modellazione. Ad esempio, spesso per aumentare il numero di clic si ricorre a un’attività di Personalizzazione automatizzata che viene impostata come obiettivo di modellazione. Tuttavia è importante capire in che modo un maggior numero di clic porti alla conversione finale, perciò è essenziale effettuare il tracciamento fino alla conversione finale.<br>È possibile fornire la dipendenza su più metriche insieme alla flessibilità necessaria, per scegliere se la metrica debba essere raggiunta o meno per incrementare il conteggio.<br>È necessario definire entrambe le metriche (o più metriche) di successo prima di renderle interdipendenti tra loro.<br>L’opzione Aggiungi dipendenza consente di incrementare la metrica di successo nel caso in cui un’altra metrica di successo venga raggiunta o meno.<br>Per aggiungere una dipendenza:<ol><li>Dopo aver aggiunto ulteriori metriche, fai clic su [!UICONTROL Impostazioni avanzate] sotto il menu a tre punti a destra di Obiettivo aggiuntivo.</li><li>Fai clic sull’opzione [!UICONTROL Aggiungi dipendenza] nella parte inferiore della sezione [!UICONTROL Impostazioni reporting].</li><li>Trascina e rilascia le metriche desiderate dal riquadro di sinistra a quello di destra, quindi fai clic su [!UICONTROL Raggiunto] per scegliere tra [!UICONTROL Raggiunto] e [!UICONTROL Non raggiunto]</li></ol>È possibile modificare o rimuovere le dipendenze dopo averle aggiunte. |
   | Metrica di conversione | Per impostazione predefinita, la metrica di conversione è identica alla metrica di obiettivo ottimizzata. Tuttavia, puoi definire una metrica di conversione separata deselezionando l’opzione [!UICONTROL Uguale all’obiettivo di ottimizzazione]. |
   | Altre metriche | Indica eventuali metriche di reporting aggiuntive da utilizzare. Puoi aggiungere metriche di conversione o ricavi.<br>**Nota**: la metrica di coinvolgimento non è supportata anche come metrica aggiuntiva. L&#39;interfaccia utente potrebbe consentire di selezionare la metrica di coinvolgimento, ma i dati non verranno visualizzati in modo accurato nei rapporti. |
   | Tipi di pubblico per i rapporti | Aggiungi tipi di pubblico per poter filtrare i rapporti in base al pubblico. Per impostazione predefinita, il rapporto mostra risultati per tutti i visitatori idonei. Aggiungi dei tipi di pubblico per filtrare i risultati per sottoinsiemi più specifici di visitatori.<br>**Nota**: a differenza di altri tipi di attività, la personalizzazione automatizzata non può utilizzare Adobe Analytics come origine per la generazione di rapporti. |
   | Note | Inserisci informazioni sull’attività, utili per te o per gli altri membri del gruppo. Il riquadro delle note è ridimensionabile. |

   Nota che quando denomini o rinomini una metrica, i seguenti caratteri non sono consentiti:

   | Carattere | Descrizione |
   |--- |--- |
   | / | Barra |
   | ? | Punto interrogativo |
   | # | Cancelletto |
   | : | Due punti |
   | = | Uguale |
   | + | Più |
   | - | Meno |
   | @ | Chiocciola |

Dopo aver fatto clic su **[!UICONTROL Crea]** verrà visualizzato il riepilogo attività. Fai clic su **Anteprima esperienze** per poter vedere in anteprima l&#39;aspetto che avranno le tue esperienze quando saranno distribuite. Appare un riquadro a comparsa che puoi utilizzare per visualizzare e condividere i collegamenti alle esperienze di Personalizzazione automatizzata sul tuo sito per ottenere una “anteprima fedele” al di fuori del Compositore esperienza visivo di Target. Per condividere l’anteprima, è necessario condividere i collegamenti dal messaggio. Non è possibile fare clic su un collegamento e poi copiare l&#39;URL direttamente dalla pagina, perché l&#39;URL contiene un parametro che visualizza la pagina correttamente solo quando si accede alla pagina dal collegamento nel messaggio.

Per informazioni sull’attività di reporting, consulta [Rapporti per Personalizzazione automatizzata](/help/c-reports/reports-ap.md#concept_C02BAFC922114A44846998FD956E345A).
