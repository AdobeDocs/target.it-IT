---
keywords: personalizzazione automatizzata;ap;pubblico;insieme;foresta casuale;varianza residua;varianza errore;valore vita
description: Scopri come creare un [!UICONTROL Automated Personalization] Attività di (AP) in [!DNL Adobe Target] utilizzando [!UICONTROL Compositore esperienza visivo].
title: Come si crea un [!UICONTROL Automated Personalization] Attività?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
exl-id: eadc2bbc-310b-479f-b75b-253e8d7aa812
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '1853'
ht-degree: 62%

---

# Creare un’attività di [!UICONTROL Automated Personalization]

Creare un [!UICONTROL Automated Personalization] Attività di (AP) in [!DNL Adobe Target] utilizzando [!UICONTROL Compositore esperienza visivo] (VEC).

Il [!UICONTROL Automated Personalization] Flusso di lavoro di attività (AP) in [!DNL Adobe Target] varia dal flusso di lavoro degli altri tipi di attività.

1. Dalla sezione [!DNL Target] [!UICONTROL Attività] , fare clic su **[!UICONTROL Crea attività]** > **[!UICONTROL Automated Personalization]**.

   ![Crea attività: Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/assets/ap-create-new.png)

1. Per utilizzare il Compositore esperienza visivo, fai clic su **[!UICONTROL Visivo (predefinito)]**.

   ![Finestra di dialogo Crea attività di personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/assets/ap_url-new.png){width="300"}

   Per utilizzare [!UICONTROL Compositore esperienza basato su moduli], seleziona [!UICONTROL Modulo]. Per ulteriori informazioni, consulta [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Oltre al Compositore esperienza visivo e [!UICONTROL Compositore esperienza basato su moduli], [!DNL Target] offre [!UICONTROL Compositore esperienza visivo per applicazione a pagina singola]. Per ulteriori informazioni sui vari moduli di composizione, consulta [Esperienze e offerte](/help/main/c-experiences/experiences.md).
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, consulta [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Condizionale) [Scegli un’area di lavoro](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Verifica o inserisci l’URL di attività, quindi fai clic su **[!UICONTROL Avanti]**.

   >[!NOTE]
   >
   >[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `http://www.adobe.com`] e [!DNL `https://wwww.adobe.com`] sono entrambi validi.

   La pagina con l’URL specificato viene aperta nel Compositore esperienza visivo.

1. Per assegnare un nome all’attività, fai clic su **[!UICONTROL Nome]** e digita il nome dell’attività.

   ![Campo Nome](/help/main/c-activities/t-automated-personalization/assets/ap-new-name.png)

   Il nome dell’attività non può iniziare con uno dei seguenti caratteri:

   | Carattere | Descrizione |
   |--- |--- |
   | `=` | Uguale |
   | `+` | Più |
   | `-` | Meno |
   | `@` | Chiocciola |

   Inoltre, il nome dell’attività non può contenere nessuna delle seguenti sequenze di caratteri: &quot;;=&quot;, &quot;;+&quot;, &quot;;-&quot;, &quot;;@&quot;, &quot;,=&quot;, &quot;,+&quot;, &quot;,-&quot;, &quot;,@&quot;, &quot;[&quot;&#39;, &#39;&quot;]&#39;, &#39;[&quot;, &quot;]&quot;.

1. Modifica gli elementi della pagina come descritto in [Opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   È possibile selezionare più immagini contemporaneamente dal gestore delle risorse. In questo modo è possibile visualizzare rapidamente la pagina con ciascuna delle immagini configurate per l&#39;attività. Inoltre è possibile modificare facilmente gli elementi di testo nelle offerte. Quando si modifica un elemento, su tale elemento vengono visualizzate delle barre per indicare che è stato modificato.

1. Fai clic su **[!UICONTROL Gestisci contenuto]** per configurare le combinazioni disponibili.

   ![Opzione Gestione contenuto](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   Viene visualizzata una finestra di dialogo con tre opzioni nella parte superiore dello schermo: [!UICONTROL Esperienze], [!UICONTROL Offerte], e [!UICONTROL Gruppi di esclusione].

   ![Finestra di dialogo Gestione contenuto](/help/main/c-activities/t-automated-personalization/assets/ap_content-new.png)

   >[!NOTE]
   >
   >Anche se è possibile creare fino a 30.000 esperienze in un’attività Personalizzazione automatizzata, l’attività fornisce migliori prestazioni quando si utilizzano meno di 5.000 esperienze. Lo stesso limite viene applicato anche quando l’attività ha abilitato l’opzione [!UICONTROL Disabilita duplicati].

   Il [!UICONTROL Esperienze] mostra ogni elemento di contenuto selezionato per l’attività e la posizione a cui è assegnato.

   Per escludere esperienze specifiche, passa il cursore sopra l’esperienza desiderata e fai clic su [!UICONTROL Escludi] icona.

   ![Icona Escludi per una singola esperienza](/help/main/c-activities/t-automated-personalization/assets/icon-exclude.png)

   Per escludere e includere esperienze in blocco, seleziona la casella di spunta per le esperienze rilevanti e fai clic su [!UICONTROL Escludi] nell&#39;angolo superiore destro della finestra di dialogo.

   ![Opzioni di esclusione per più esperienze](/help/main/c-activities/t-automated-personalization/assets/batch-exclude.png)

   Per filtrare l’elenco in modo da visualizzare solo le attività escluse o incluse, fai clic sull’elenco a discesa [!UICONTROL Stato].

1. (Facoltativo) Fai clic su **[!UICONTROL Offerte]** per selezionare parti di contenuto e assegnarle a gruppi di reporting o per consentire solamente a determinati visitatori di visualizzare alcune offerte con targeting.

   Per ulteriori informazioni sui gruppi di reporting, consulta [Gruppi di reporting di offerte in Automated Personalization](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md).

1. (Condizionale) Fai clic su **[!UICONTROL Gruppi di esclusione]** per scegliere le combinazioni di elementi da escludere dall’attività.

   ![Scheda Gruppi di esclusione della finestra di dialogo Gestione contenuto](/help/main/c-activities/t-automated-personalization/assets/exclusion_groups-new.png)

   Anche se è possibile creare fino a 30.000 esperienze in un test di Personalizzazione automatizzata, l&#39;algoritmo fornisce prestazioni migliori quando si utilizzano meno di 10.000 esperienze. Lo stesso limite viene applicato anche quando l’attività ha abilitato l’opzione [!UICONTROL Disabilita duplicati].

   Se nell&#39;attività non sono presenti gruppi di esclusione, fai clic su **Crea gruppo di esclusione**. È possibile filtrare l&#39;attività per creare un elenco che mostra solo le combinazioni che desideri escludere. Denomina il gruppo di esclusione e fai clic su **Salva**.

   Per modificare un gruppo di esclusione esistente, posiziona il puntatore del mouse sul gruppo che desideri modificare, quindi fai clic sull&#39;icona a forma di matita.

1. Una volta completata l’impostazione del contenuto dell’attività, fai clic su **[!UICONTROL Fine]**.

1. Il **Targeting** se hai usato altri [!DNL Target] tipi di attività. Qui puoi selezionare un pubblico e specificare la percentuale di visitatori che visualizzano l’esperienza di controllo facendo clic sul pulsante **[!UICONTROL Personalizza allocazione]** , quindi fai clic su **Successivo**.

   L’elenco a discesa [!UICONTROL Personalizza allocazione] consente di scegliere tra le seguenti opzioni:

   ![Elenco a discesa Obiettivo di allocazione traffico](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation-goal-ap.png)

   * **[!UICONTROL Valuta algoritmo di personalizzazione (50/50)]:** Se l&#39;obiettivo è quello di testare l&#39;algoritmo, assegna il 50% dei visitatori all&#39;algoritmo di controllo e l&#39;altro 50% a quello di destinazione. Questa suddivisione fornisce la stima più accurata dell’incremento. Consigliato per l’utilizzo con &quot;esperienze casuali&quot; come controllo.
   * **[!UICONTROL Massimizzare il traffico di personalizzazione (90/10)]:** Se il tuo obiettivo è invece quello di creare un’attività &quot;sempre attiva&quot;, inserisci il 10% dei visitatori nel controllo. Questa opzione assicura che siano presenti dati sufficienti per consentire agli algoritmi di continuare a imparare nel tempo. Tieni presente che il compromesso qui è che in cambio della personalizzazione di una proporzione maggiore del traffico, hai meno precisione in cosa sia l’incremento esatto. Indipendentemente dall’obiettivo, questa è la suddivisione del traffico consigliata quando si utilizza come controllo un’esperienza specifica.
   * **[!UICONTROL Personalizza allocazione]:** Dividi manualmente la percentuale come desiderato.

1. (Condizionale) Dall’elenco a discesa [!UICONTROL Controllo], [seleziona un’esperienza specifica da usare come controllo](/help/main/c-activities/t-automated-personalization/experience-as-control.md) oppure seleziona [!UICONTROL Esperienza casuale.]

   L&#39;esperienza di controllo fornisce un confronto per determinare l&#39;incremento fornito dal test automatizzato.

   [!UICONTROL Nella personalizzazione automatizzata le prestazioni vengono sempre misurate in base al confronto con un gruppo di controllo. ] La migliore prassi è quella di collocare almeno il 10% dei partecipanti nel gruppo di controllo. Se l&#39;obiettivo è quello di verificare se l&#39;algoritmo di personalizzazione sui dati stia fornendo migliori prestazioni rispetto all&#39;assenza di personalizzazione (vale a dire, il controllo eseguito in modo casuale), allora il modo più veloce e preciso per raggiungere questo obiettivo è la suddivisione di un 50% e l&#39;altro 50% del traffico tra il controllo e l&#39;algoritmo di personalizzazione. Se desideri massimizzare la quantità di traffico personalizzato e sei meno interessato a conoscere l&#39;incremento esatto generato dall&#39;attività, allora il modo più veloce e preciso per raggiungere questo obiettivo è la suddivisione del 10% e del 90% del traffico tra il controllo e l&#39;algoritmo di personalizzazione.

   >[!NOTE]
   >
   >In entrata [!UICONTROL Automated Personalization] Le attività, i criteri di immissione (targeting URL, regole modello e target di pubblico) vengono valutati per ogni richiesta. Nelle versioni precedenti, i criteri di ingresso venivano valutati una volta a sessione.

1. Fai clic su **[!UICONTROL Successivo]** per visualizzare la pagina **[!UICONTROL Obiettivi e impostazioni]**.
1. Configura l’attività con le impostazioni seguenti, quindi fai clic su **[!UICONTROL Salva e chiudi]**.

   | Impostazione | Descrizione |
   |--- |--- |
   | [!UICONTROL Nome] | Assegna un nome all’attività. Assegna all’attività un nome sufficientemente descrittivo da consentire ai membri del gruppo di riconoscerla nel [!UICONTROL Attività] elenco. Consultate la tabella qui sopra per vedere quali caratteri non sono consentiti nel nome di un’attività. |
   | [!UICONTROL Finalità] | (Facoltativo) Inserire la finalità del test. La finalità aiuta a ricordare lo scopo dell&#39;attività. |
   | [!UICONTROL Priorità] | L’interfaccia utente e le opzioni per [!UICONTROL Priorità] variano a seconda delle impostazioni. È possibile utilizzare le impostazioni legacy Bassa, Media o Alta, oppure attivare la priorità precisa da 0 a 999.<br>La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.<br>Se questa opzione non è abilitata in [!UICONTROL Amministrazione] > [!UICONTROL Generazione rapporti] (impostazione predefinita), specifica una priorità: Bassa, Media o Alta.<br>Per abilitare le priorità dettagliate, fai clic su [!UICONTROL Amministrazione] > [!UICONTROL Generazione rapporti], quindi attiva/disattiva [!UICONTROL Abilita priorità precise] nella posizione &quot;On&quot;.<br>Se questa opzione è abilitata, specifica un valore compreso tra 0 e 999:<ul><li>0 = Bassa</li><li>999 = Alta</li></ul>Per le attività create con le versioni precedenti di [!DNL Target Standard/Premium], la priorità Bassa viene convertita in 0, la priorità Media in 5 e la priorità Alta in 10. Se necessario, è possibile modificare questi valori.<br>**Nota**: prima di poter disabilitare questa opzione dopo aver utilizzato le priorità precise, tutte le priorità devono essere impostate su 0, 5 o 10. |
   | [!UICONTROL Durata] | Imposta le date di inizio e di fine dell&#39;attività. Puoi selezionare [!UICONTROL Quando è attivato] oppure puoi specificare una data e un’ora specifiche. |
   | [!UICONTROL Obiettivo di ottimizzazione] | Specifica l&#39;obiettivo di ottimizzazione, costituito da due parametri:<ul><li>Ciò che desideri misurare con l&#39;attività</li><li>L&#39;azione intrapresa da un partecipante a un&#39;attività che dimostra che l&#39;obiettivo è stato raggiunto.</li></ul>Puoi scegliere di denominare l’obiettivo di ottimizzazione selezionando i tre punti a destra di [!UICONTROL Il mio obiettivo principale]. [!UICONTROL Automated Personalization] le attività possono misurare [!UICONTROL Conversione] o [!UICONTROL Ricavi]. La conversione può essere ottenuta mediante la visualizzazione di una pagina o di una mbox. È possibile inoltre il tracciamento dei clic.<br>L&#39;obiettivo principale diventa anche la metrica di modellazione, utilizzata dal sistema di modellazione per calcolare il successo dell&#39;esperienza.<br>I visitatori possono essere mantenuti nell&#39;attività per scopi di tracciamento, dopo aver raggiunto l&#39;obiettivo di modellazione. Ad esempio, spesso un’ [!UICONTROL Automated Personalization] L’attività viene utilizzata per migliorare i tassi di clic e viene impostata come obiettivo di modellazione. Tuttavia è importante capire in che modo un maggior numero di clic porti alla conversione finale, perciò è essenziale effettuare il tracciamento fino alla conversione finale.<br>È possibile fornire la dipendenza su più metriche insieme alla flessibilità necessaria, per scegliere se la metrica debba essere raggiunta o meno per incrementare il conteggio.<br>È necessario definire entrambe le metriche (o più metriche) di successo prima di renderle interdipendenti tra loro.<br>L’opzione Aggiungi dipendenza consente di incrementare la metrica di successo nel caso in cui un’altra metrica di successo venga raggiunta o meno.<br>Per aggiungere una dipendenza:<ol><li>Dopo aver aggiunto ulteriori metriche, fai clic su **[!UICONTROL Impostazioni avanzate]**[!UICONTROL  sotto il menu a tre punti a destra di Obiettivo aggiuntivo].</li><li>Fai clic sull’opzione **[!UICONTROL Aggiungi dipendenza]** nella parte inferiore della sezione [!UICONTROL Impostazioni reporting].</li><li>Trascina e rilascia le metriche desiderate dal riquadro di sinistra a quello di destra, quindi fai clic su [!UICONTROL Raggiunto] per scegliere tra [!UICONTROL Raggiunto] e [!UICONTROL Non raggiunto]</li></ol>È possibile modificare o rimuovere le dipendenze dopo averle aggiunte. |
   | [!UICONTROL Metrica di conversione] | Per impostazione predefinita, la metrica di conversione è identica alla metrica di obiettivo ottimizzata. Tuttavia, puoi definire una metrica di conversione separata deselezionando l’opzione [!UICONTROL Uguale all’obiettivo di ottimizzazione]. |
   | [!UICONTROL Altre metriche] | Aggiungi eventuali metriche di reporting aggiuntive da utilizzare. Puoi aggiungere metriche di conversione o ricavi.<br>**Nota**: la metrica di coinvolgimento non è supportata anche come metrica aggiuntiva. L’interfaccia utente potrebbe consentire di selezionare [!UICONTROL Coinvolgimento] metrica, ma i dati non vengono visualizzati con precisione nei rapporti. |
   | [!UICONTROL Tipi di pubblico per i rapporti] | Aggiungi tipi di pubblico per poter filtrare i rapporti in base al pubblico. Per impostazione predefinita, il rapporto mostra risultati per tutti i visitatori idonei. Aggiungi dei tipi di pubblico per filtrare i risultati per sottoinsiemi più specifici di visitatori.<br>**Nota**: a differenza di altri tipi di attività, [!UICONTROL Automated Personalization] non può utilizzare [!UICONTROL Adobe Analytics] come fonte di reporting (A4T). |
   | [!UICONTROL Note] | Inserisci informazioni sull’attività, utili per te o per gli altri membri del gruppo. Il [!UICONTROL Note] è ridimensionabile. |

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

Dopo aver fatto clic su **[!UICONTROL Salva e chiudi]**, dell&#39;attività [!UICONTROL Panoramica] viene visualizzata la pagina. Clic **Anteprima esperienze** per visualizzare in anteprima come si presentano le esperienze consegnate. Viene visualizzato un pop-up che puoi utilizzare per visualizzare e condividere i collegamenti alle esperienze di Personalizzazione automatizzata sul tuo sito per ottenere una &quot;anteprima fedele&quot; al di fuori di [!UICONTROL Target]Compositore esperienza visivo di. Per condividere l’anteprima, è necessario condividere i collegamenti dal messaggio. Non è possibile fare clic su un collegamento e quindi copiare l’URL direttamente dal browser. Copiare il collegamento fa sì che l’URL contenga un parametro che visualizza correttamente la pagina solo quando si accede alla pagina dal collegamento nel messaggio.

Per informazioni sull’attività di reporting, consulta [Rapporti per Personalizzazione automatizzata](/help/main/c-reports/personalization-reports/reports-ap.md).
