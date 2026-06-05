---
keywords: personalizzazione automatizzata;ap
description: Scopri come creare un'attività [!UICONTROL Automated Personalization] (AP) in [!DNL Adobe Target] utilizzando [!UICONTROL Visual Experience Composer].
title: Come si crea un'attività [!UICONTROL Automated Personalization]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Automated Personalization
exl-id: eadc2bbc-310b-479f-b75b-253e8d7aa812
source-git-commit: c467f629596b37c334276d6f095f19b639a8518d
workflow-type: tm+mt
source-wordcount: '1927'
ht-degree: 30%

---

# Crea un&#39;attività [!UICONTROL Automated Personalization]

Creare un&#39;attività [!UICONTROL Automated Personalization] (AP) in [!DNL Adobe Target] utilizzando il [!UICONTROL Compositore esperienza visivo].

Il flusso di lavoro dell&#39;attività [!UICONTROL Automated Personalization] (AP) in [!DNL Target] è diverso da quello degli altri tipi di attività.

1. Dall&#39;elenco [!DNL Target] [!UICONTROL Attività], fare clic su **[!UICONTROL Crea attività]** > **[!UICONTROL Automated Personalization]**.

   ![Crea attività: Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/assets/ap-create-new.png)

1. Per utilizzare il [!UICONTROL Compositore esperienza visivo] (VEC), fare clic su **[!UICONTROL Visivo]**.

   Per utilizzare il [!UICONTROL Compositore esperienza basato su moduli], selezionare [!UICONTROL Modulo]. Per ulteriori informazioni, consulta [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Oltre al Compositore esperienza visivo e al Compositore esperienza basato su moduli [!UICONTROL 1&rbrace;, [!DNL Target] offre il [!UICONTROL Compositore esperienza visivo per applicazione a pagina singola]. &#x200B;]Per ulteriori informazioni sui vari moduli di composizione, consulta [Esperienze e offerte](/help/main/c-experiences/experiences.md).
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, vedere [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Condizionale) [Scegliere un&#39;area di lavoro](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Verificare o immettere l&#39;URL attività, quindi fare clic su **[!UICONTROL Crea]**.

   >[!NOTE]
   >
   >[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `http://www.adobe.com`] e [!DNL `https://wwww.adobe.com`] corrispondono entrambi.

   La pagina con l’URL specificato viene aperta nel Compositore esperienza visivo.

1. Fai clic sul campo **[!UICONTROL Name]** e digita il nome dell&#39;attività.

   ![Campo Nome](/help/main/c-activities/t-automated-personalization/assets/ap-new-name.png)

   Il nome dell’attività non può iniziare con uno dei seguenti caratteri:

   | Carattere | Descrizione |
   |--- |--- |
   | `=` | Uguale |
   | `+` | Più |
   | `-` | Meno |
   | `@` | Chiocciola |

   Il nome dell’attività non può contenere nessuna delle seguenti sequenze di caratteri:

   | Sequenza di caratteri | Descrizione |
   |--- |--- |
   | ;= | Punto e virgola, uguale a |
   | ;+ | Punto e virgola, segno più |
   | ;- | Punto e virgola, meno |
   | ;@ | Punto e virgola, segno A |
   | ,= | Virgola, uguale a |
   | ,+ | Virgola più |
   | ,- | Virgola meno |
   | ,@ | Virgola, segno A |
   | `[`&quot; | Parentesi quadra aperta, virgolette doppie |
   | &quot;`]` | Virgolette doppie, parentesi quadra chiusa |

1. Modifica gli elementi della pagina come descritto in [Opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   È possibile selezionare più immagini contemporaneamente dal gestore delle risorse. Questo consente di visualizzare rapidamente la pagina con ciascuna delle immagini configurate per l’attività. Inoltre è possibile modificare facilmente gli elementi di testo nelle offerte. Quando si modifica un elemento, su tale elemento vengono visualizzate delle barre per indicare che è stato modificato.

1. Fai clic su **[!UICONTROL Gestisci contenuto]** per configurare le combinazioni disponibili.

   ![Opzione Gestione contenuto](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   Viene visualizzata una finestra di dialogo con tre opzioni nella parte superiore dello schermo: [!UICONTROL Esperienze], [!UICONTROL Offerte] e [!UICONTROL Gruppi di esclusione].

   ![Finestra di dialogo Gestione contenuto](/help/main/c-activities/t-automated-personalization/assets/ap_content-new.png)

   >[!NOTE]
   >
   >Anche se è possibile creare fino a 30.000 esperienze in un’attività Personalizzazione automatizzata, l’attività fornisce prestazioni migliori quando si utilizzano meno di 5.000 esperienze. Lo stesso limite viene applicato anche quando l&#39;attività ha abilitato l&#39;opzione [!UICONTROL Non consentire duplicati].

   L&#39;elenco [!UICONTROL Esperienze] mostra ogni elemento di contenuto selezionato per l&#39;attività e la posizione a cui è assegnato.

   Per escludere esperienze specifiche, passa il mouse sull&#39;esperienza desiderata e fai clic sull&#39;icona [!UICONTROL Escludi].

   ![Icona Escludi per una singola esperienza](/help/main/c-activities/t-automated-personalization/assets/icon-exclude.png)

   Puoi escludere o includere esperienze in blocco selezionando la casella di controllo per le esperienze rilevanti e quindi facendo clic sull&#39;icona [!UICONTROL Escludi] nell&#39;angolo in alto a destra della finestra di dialogo.

   ![Opzioni di esclusione per più esperienze](/help/main/c-activities/t-automated-personalization/assets/batch-exclude.png)

   Per filtrare questo elenco in modo da visualizzare solo le attività escluse o incluse, fai clic sull&#39;elenco a discesa [!UICONTROL Stato].

1. (Facoltativo) Fai clic su **[!UICONTROL Offerte]** per selezionare parti di contenuto e assegnarle a gruppi di reporting o per consentire solo a determinati visitatori di visualizzare alcune offerte con targeting.

   Per ulteriori informazioni sui gruppi di reporting, vedi [Gruppi di reporting di offerte in Automated Personalization](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md).

1. (Condizionale) Fai clic su **[!UICONTROL Gruppi di esclusione]** per scegliere una combinazione di elementi da escludere dall&#39;attività.

   ![Scheda Gruppi di esclusione della finestra di dialogo Gestione contenuto](/help/main/c-activities/t-automated-personalization/assets/exclusion_groups-new.png)

   Anche se è possibile creare fino a 30.000 esperienze in un test AP, l&#39;algoritmo fornisce prestazioni migliori quando si utilizzano meno di 10.000 esperienze. Lo stesso limite viene applicato anche quando l&#39;attività ha abilitato l&#39;opzione [!UICONTROL Non consentire duplicati].

   Se nell&#39;attività non sono presenti gruppi di esclusione, fai clic su **Crea gruppo di esclusione**. È possibile filtrare l&#39;attività per creare un elenco che mostra solo le combinazioni che desideri escludere. Assegna un nome al gruppo di esclusione, quindi fai clic su **Salva**.

   Per modificare un gruppo di esclusione esistente, posiziona il puntatore del mouse sul gruppo che desideri modificare, quindi fai clic sull&#39;icona a forma di matita.

1. Fai clic su **[!UICONTROL Fine]** una volta completata la configurazione del contenuto dell&#39;attività.

1. Il passaggio **Targeting** ha un aspetto familiare se sono stati utilizzati altri tipi di attività [!DNL Target]. Qui puoi selezionare un pubblico e specificare la percentuale di visitatori che visualizzano l&#39;esperienza di controllo facendo clic sull&#39;elenco a discesa **[!UICONTROL Personalizza allocazione]**, quindi fai clic su **Successivo**.

   L’elenco a discesa [!UICONTROL Personalizza allocazione] consente di scegliere tra le seguenti opzioni:

   ![Elenco a discesa Obiettivo di allocazione traffico](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation-goal-ap.png)

   * **[!UICONTROL Valuta algoritmo di Personalization (50/50)]:** Se l&#39;obiettivo è quello di testare l&#39;algoritmo, assegna il 50% dei visitatori all&#39;algoritmo di controllo e l&#39;altro 50% a quello di destinazione. Questa suddivisione fornisce la stima più accurata dell’incremento. Consigliato per l’utilizzo con &quot;esperienze casuali&quot; come controllo.
   * **[!UICONTROL Massimizzazione del traffico Personalization (90/10)]:** Se il tuo obiettivo è invece quello di creare un&#39;attività &quot;sempre attiva&quot;, inserisci il 10% dei visitatori nel controllo. Questa opzione assicura che siano presenti dati sufficienti per consentire agli algoritmi di continuare a imparare nel tempo. In questo caso, il compromesso è che, in cambio della personalizzazione di una proporzione maggiore del traffico, si ha meno precisione in cosa sia l’incremento esatto. Indipendentemente dall’obiettivo, questa opzione rappresenta la suddivisione del traffico consigliata quando si utilizza come controllo un’esperienza specifica.
   * **[!UICONTROL Personalizza allocazione]:** dividi manualmente la percentuale come desiderato.

1. (Condizionale) Dall&#39;elenco a discesa [!UICONTROL Controllo], [selezionare un&#39;esperienza specifica da utilizzare come controllo](/help/main/c-activities/t-automated-personalization/experience-as-control.md) oppure selezionare [!UICONTROL Esperienza casuale.]

   L&#39;esperienza di controllo fornisce un confronto per determinare l&#39;incremento fornito dal test automatizzato.

   [!UICONTROL Automated Personalization] misura sempre le prestazioni rispetto a un gruppo di controllo. La migliore prassi è quella di collocare almeno il 10% dei partecipanti nel gruppo di controllo. Se l’obiettivo è quello di verificare se l’algoritmo di personalizzazione sui dati che ti vengono forniti funziona meglio dell’assenza di personalizzazione (ad esempio, il controllo fornito in modo casuale), il modo più veloce e preciso per raggiungere questo obiettivo è quello di suddividere il traffico del 50% tra il controllo e l’algoritmo di personalizzazione. Se desideri massimizzare la quantità di traffico personalizzato e non sei interessato a comprendere l’incremento esatto che l’attività sta generando, il modo più veloce e preciso per raggiungere questo obiettivo è quello di suddividere il traffico del 10% e del 90% tra il controllo e l’algoritmo di personalizzazione.

   >[!NOTE]
   >
   >Nelle attività di [!UICONTROL Automated Personalization], i criteri di ingresso (targeting URL, regole modello e destinazioni pubblico) vengono valutati per ogni richiesta. Nelle versioni precedenti, i criteri di ingresso venivano valutati una volta a sessione.

1. Fai clic su **[!UICONTROL Avanti]** per visualizzare la pagina **[!UICONTROL Obiettivi e impostazioni]**.
1. Configura l&#39;attività con le impostazioni seguenti, quindi fai clic su **[!UICONTROL Salva e chiudi]**.

   | Impostazione | Descrizione |
   |--- |--- |
   | [!UICONTROL Nome] | Assegna un nome all’attività. Assegna all&#39;attività un nome sufficientemente descrittivo da consentire ai membri del team di riconoscerla nell&#39;elenco [!UICONTROL Attività]. Consultate la tabella qui sopra per vedere quali caratteri non sono consentiti nel nome di un’attività. |
   | [!UICONTROL Obiettivo] | (Facoltativo) Inserire la finalità del test. La finalità aiuta a ricordare lo scopo dell&#39;attività. |
   | [!UICONTROL Priorità] | A seconda delle impostazioni, l&#39;interfaccia utente di [!DNL Target] e le opzioni per [!UICONTROL Priorità] variano. Puoi utilizzare le impostazioni legacy di [!UICONTROL Bassa], [!UICONTROL Medium] o [!UICONTROL Alta] oppure abilitare le priorità precise da 0 a 999.<P>La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.<P>Se questa opzione non è abilitata in [!UICONTROL Amministrazione] > [!UICONTROL Generazione rapporti] (impostazione predefinita), specificare una priorità: [!UICONTROL Bassa], [!UICONTROL Medium] o [!UICONTROL Alta].<P>Per abilitare le priorità dettagliate, fai clic su [!UICONTROL Amministrazione] > [!UICONTROL Generazione rapporti], quindi attiva l&#39;opzione [!UICONTROL Abilita priorità precise].<P>Se questa opzione è abilitata, specifica un valore compreso tra 0 e 999:<ul><li>0 = Bassa</li><li>999 = Alta</li></ul>Per le attività create con le versioni precedenti di [!DNL Target Standard/Premium], la priorità [!UICONTROL Bassa] è convertita in 0, la priorità [!UICONTROL Medium] è convertita in 5 e la priorità [!UICONTROL Alta] in 10. Se necessario, è possibile modificare questi valori.<P>**Nota**: prima di poter disabilitare questa opzione dopo aver utilizzato le priorità precise, tutte le priorità devono essere impostate su 0, 5 o 10. |
   | [!UICONTROL Durata] | Imposta le date di inizio e di fine dell&#39;attività. Puoi selezionare [!UICONTROL Quando è attivato] oppure specificare una data e un&#39;ora specifiche. |
   | [!UICONTROL Obiettivo di ottimizzazione] | Specifica l&#39;obiettivo di ottimizzazione, costituito da due parametri:<ul><li>Ciò che desideri misurare con l&#39;attività</li><li>L&#39;azione intrapresa da un partecipante a un&#39;attività che dimostra che l&#39;obiettivo è stato raggiunto.</li></ul>Puoi scegliere di denominare l&#39;obiettivo di ottimizzazione selezionando i tre punti a destra di [!UICONTROL Obiettivo principale]. Le attività di [!UICONTROL Automated Personalization] possono misurare [!UICONTROL Conversion] o [!UICONTROL Revenue]. La conversione può essere ottenuta visualizzando una pagina o una mbox. È possibile inoltre il tracciamento dei clic.<P>L’obiettivo principale diventa anche la metrica di modellazione utilizzata dal sistema di modellazione per calcolare il successo dell’esperienza.<P>I visitatori possono essere mantenuti nell&#39;attività per scopi di tracciamento, dopo aver raggiunto l&#39;obiettivo di modellazione. Ad esempio, spesso per migliorare i click-rate viene utilizzata un&#39;attività [!UICONTROL Automated Personalization] impostata come obiettivo di modellazione. Tuttavia è importante capire in che modo un maggior numero di clic porti alla conversione finale, perciò è essenziale effettuare il tracciamento fino alla conversione finale.<P>È possibile fornire la dipendenza su più metriche insieme alla flessibilità necessaria, per scegliere se la metrica debba essere raggiunta o meno per incrementare il conteggio.<P>È necessario definire entrambe le metriche (o più metriche) di successo prima di renderle interdipendenti tra loro.<P>L’opzione [!UICONTROL Aggiungi dipendenza] consente di incrementare la metrica di successo nel caso in cui un’altra metrica di successo venga raggiunta o meno.<P>Per aggiungere una dipendenza:<ol><li>Dopo aver aggiunto ulteriori metriche, fai clic su **[!UICONTROL Impostazioni avanzate]** sotto il menu a tre punti a destra di [!UICONTROL Obiettivo aggiuntivo].</li><li>Fai clic sull&#39;opzione **[!UICONTROL Aggiungi dipendenza]** nella parte inferiore della sezione [!UICONTROL Impostazioni reporting].</li><li>Trascina e rilascia le metriche desiderate dal riquadro di sinistra a quello di destra, quindi fai clic su [!UICONTROL Raggiunto] per scegliere tra [!UICONTROL Raggiunto] e [!UICONTROL Non raggiunto].</li></ol>È possibile modificare o rimuovere le dipendenze dopo averle aggiunte. |
   | [!UICONTROL Metrica di conversione] | Per impostazione predefinita, la metrica di conversione è la stessa della metrica dell’obiettivo di ottimizzazione. Tuttavia, puoi definire una metrica di conversione separata deselezionando l&#39;opzione [!UICONTROL Uguale all&#39;obiettivo di ottimizzazione]. |
   | [!UICONTROL Altre metriche] | Aggiungi eventuali metriche di reporting aggiuntive da utilizzare. Puoi aggiungere metriche di conversione o ricavi.<P>**Nota**: la metrica [!UICONTROL Coinvolgimento] non è supportata come metrica aggiuntiva. L&#39;interfaccia utente di [!DNL Target] potrebbe consentire di selezionare la metrica [!UICONTROL Coinvolgimento], ma i dati non vengono visualizzati con precisione nei report. |
   | [!UICONTROL Tipi di pubblico per reporting] | Aggiungi tipi di pubblico per poter filtrare i rapporti in base al pubblico. Per impostazione predefinita, il rapporto mostra risultati per tutti i visitatori idonei. Aggiungi dei tipi di pubblico per filtrare i risultati per sottoinsiemi più specifici di visitatori.<P>**Nota**: a differenza di altri tipi di attività, [!UICONTROL Automated Personalization] non può utilizzare [!UICONTROL Adobe Analytics] come origine per la generazione di rapporti (A4T). |
   | [!UICONTROL Note] | Inserisci informazioni sull’attività, utili per te o per gli altri membri del gruppo. Il riquadro [!UICONTROL Notes] è ridimensionabile. |

   Quando denomini o rinomini una metrica, i seguenti caratteri non sono consentiti:

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

Dopo aver fatto clic su **[!UICONTROL Salva e chiudi]**, viene visualizzata la pagina [!UICONTROL Panoramica] dell&#39;attività. Fai clic su **Anteprima esperienze** per visualizzare in anteprima l&#39;aspetto delle esperienze consegnate. Viene visualizzato un pop-up che puoi utilizzare per visualizzare e condividere i collegamenti alle esperienze di Personalizzazione automatizzata sul tuo sito per ottenere una &quot;anteprima fedele&quot; al di fuori del [!UICONTROL Target] [!UICONTROL Compositore esperienza visivo]. Per condividere l’anteprima, è necessario condividere i collegamenti dal messaggio. Non è possibile fare clic su un collegamento e quindi copiare l’URL direttamente dal browser. Copiare il collegamento fa sì che l’URL contenga un parametro che visualizza correttamente la pagina solo quando si accede alla pagina dal collegamento nel messaggio.

Per informazioni sul reporting, consulta [Rapporti di Automated Personalization](/help/main/c-reports/personalization-reports/reports-ap.md).
