---
keywords: impostazioni attività;obiettivi e impostazioni A/B;impostazioni di reporting;metriche obiettivo;metriche di successo;metriche di successo dipendenti;impostazioni avanzate;obiettivo principale;metriche aggiuntive;obiettivo;priorità;durata;soluzione di reporting;obiettivo;pubblico per rapporti;Quale metrica di successo deve essere raggiunta prima di incrementare questa metrica;Cosa succede dopo che un utente ha individuato questa metrica obiettivo;note
description: Scopri come utilizzare la pagina [!UICONTROL Obiettivi e impostazioni] per specificare informazioni sugli obiettivi di un'attività A/B.
title: Come posso specificare obiettivi e impostazioni in un'attività A/B di  [!DNL Target] ?
feature: A/B Tests
exl-id: 6c970289-a897-46bc-a8d2-ba8c045abe12
source-git-commit: eb7e892a85fa3952ffc22172085d421756d0dfb5
workflow-type: tm+mt
source-wordcount: '1411'
ht-degree: 37%

---

# Obiettivi e impostazioni

Nella pagina [!UICONTROL Obiettivi e impostazioni] di [!DNL Adobe Target] è possibile specificare informazioni sugli obiettivi dell&#39;attività.

Le impostazioni disponibili dipendono dall&#39;utilizzo di Target o [Analytics](/help/main/c-integrating-target-with-mac/a4t/a4t.md) come origine per la generazione di rapporti.

## [!UICONTROL Impostazioni attività] {#section_DCBDC354261F420EBD4B43EA34947BAC}

La sezione [!UICONTROL Impostazioni attività] della pagina [!UICONTROL Obiettivi e impostazioni] consente di configurare le opzioni seguenti:

| Impostazioni | Descrizione |
|--- |--- |
| [!UICONTROL Obiettivo] | Specifica una finalità facoltativa. L’obiettivo può essere qualsiasi informazione che aiuti te e i membri del tuo team a identificare l’attività. |
| [!UICONTROL Priorità] | A seconda delle impostazioni, l&#39;interfaccia utente di [!DNL Target] e le opzioni per [!UICONTROL Priorità] variano. Puoi utilizzare le impostazioni legacy di [!UICONTROL Bassa], [!UICONTROL Medium] o [!UICONTROL Alta] oppure abilitare le priorità precise da 0 a 999.<P>La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.<P>Se questa opzione non è abilitata in [!UICONTROL Amministrazione] (impostazione predefinita), specificare una priorità: [!UICONTROL Bassa], [!UICONTROL Medium] o [!UICONTROL Alta].<P>Per abilitare [le priorità precise](/help/main/administrating-target/reporting.md), fai clic su [!UICONTROL Amministrazione] > [!UICONTROL Generazione rapporti], quindi attiva l&#39;opzione [!UICONTROL Abilita priorità precise]. <P>Se questa opzione è abilitata, specifica un valore compreso tra 0 e 999: 0 = [!UICONTROL Bassa] e 999 = [!UICONTROL Alta]. <P>Per le attività create con le versioni precedenti di [!DNL Target], la priorità [!UICONTROL Bassa] viene convertita in 0, [!UICONTROL Medium] in 5 e la priorità [!UICONTROL Alta] in 10. Se necessario, è possibile modificare questi valori.<P>Nota: prima di poter disabilitare questa opzione dopo aver utilizzato le priorità precise, tutte le priorità devono essere impostate su 0, 5 o 10. |
| Durata | L’attività può iniziare dopo l’approvazione, oppure è possibile impostare una data e un’ora specifiche. Analogamente, l’attività può terminare quando viene disattivata, oppure è possibile impostare una data e un’ora specifiche. Il selettore dell&#39;ora utilizza un orologio di 24 ore, dove 00:00 corrisponde a mezzanotte. Il fuso orario è impostato sul fuso configurato nel browser. Per utilizzare un fuso orario diverso, imposta il browser su un altro fuso orario e riavvia il browser. |

## [!UICONTROL Impostazioni reporting] {#section_13119392051044FBA6387D9B3B1C43CF}

La sezione [!UICONTROL Impostazioni reporting] della pagina [!UICONTROL Obiettivi e impostazioni] consente di configurare le opzioni seguenti:

| Impostazioni | Descrizione |
|--- |--- |
| [!UICONTROL Reporting di Source] | Specifica da quali dati della soluzione vengono raccolti:<ul><li>[!DNL Adobe Target]</li><li>[!DNL Adobe Analytics]</li><li>[!DNL Adobe Customer Journey Analytics]</li></ul>Se un&#39;origine per la generazione di rapporti è specificata nelle [impostazioni account](/help/main/administrating-target/reporting.md), viene utilizzata l&#39;origine specificata e questa impostazione non è visibile.<P>Al fine di mantenere coerenza dei rapporti, non è possibile modificare l’origine per i rapporti una volta che l’attività è diventata attiva.<P>**Adobe Analytics**: consulta [Adobe Analytics as the Reporting Source for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) per informazioni sulle differenze tra le soluzioni di reporting e i vantaggi di ciascuna. Quando selezioni [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target], selezioni una suite di rapporti [!DNL Analytics] per ricevere i dati dell&#39;attività [!DNL Target].<P>Per specificare un&#39;origine per la generazione di rapporti, scegliere innanzitutto una delle [!DNL Analytics] società associate al proprio account, quindi selezionare la suite di rapporti appropriata per l&#39;attività. È possibile selezionare solo le suite di rapporti predisposte per la connessione a [!DNL Adobe Target]. Se le suite di rapporti previste non sono visualizzate, disconnettersi e accedere di nuovo a [!DNL Adobe Experience Cloud] per riprovare. Se la suite di rapporti non è ancora presente nell’elenco, contatta l’Assistenza clienti.<P><P>**Adobe Customer Journey Analytics**: per ulteriori informazioni sull&#39;integrazione tra [!DNL Adobe Customer Journey Analytics] e [!DNL Target], vedere [[!DNL Target] creazione di rapporti in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md).<P>Il reporting di [!DNL Target] in [!DNL Customer Journey Analytics] è supportato nelle attività A/B con suddivisione manuale del traffico. [!UICONTROL Le attività A/B di Targeting automatico] e [!UICONTROL Allocazione automatica] non possono utilizzare il reporting [!DNL Target] in [!DNL Customer Journey Analytics]. |
| [!UICONTROL Metrica per obiettivo] | Seleziona l’azione che deve essere eseguita da un visitatore per raggiungere l’obiettivo. Ad esempio, scegli una metrica [!UICONTROL Conversione], quindi imposta i parametri che determinano quando viene raggiunto il successo. Per ulteriori informazioni sull’impostazione delle metriche, consulta [Impostare le metriche](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md).<P>Nota: se la soluzione di reporting è impostata su [!DNL Analytics], l&#39;unica metrica di obiettivo disponibile è [!UICONTROL Conversione]. Impossibile selezionare [!DNL Analytics] metriche come obiettivo. Quando si seleziona la metrica di successo, viene visualizzato un selettore. Utilizza questo selettore per scegliere le specifiche per la metrica di successo.<P>Se attivato, il campo [!UICONTROL Valore stimato della conversione] (non disponibile per le metriche [!UICONTROL Punteggio di pagina]) fornisce un valore per l&#39;obiettivo, ma non per altre metriche. Questo valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. Per tutte le metriche relative ai ricavi ([!UICONTROL Ricavi per visitatore], [!UICONTROL Valore medio ordine], [!UICONTROL Vendite totali] e [!UICONTROL Ordini]), la stima utilizza [!UICONTROL Ricavi per visitatore]. Il tipo di dati è valuta.<P>Dopo aver raggiunto l’obiettivo dell’attività, un visitatore continua a vedere il contenuto dell’attività, a meno che il visitatore non sia idoneo per un’attività di priorità più elevata. Se il visitatore raggiunge nuovamente l’obiettivo, viene conteggiato come un’altra conversione. Si tratta di un comportamento diverso da quello predefinito in [!DNL Target Classic], che conta i visitatori come nuovi se visualizzano nuovamente l&#39;attività. |
| [!UICONTROL Altre metriche] | Consente di creare metriche di successo aggiuntive. Questa impostazione non è disponibile se la soluzione di reporting è impostata su [!DNL Analytics]. In questo caso, vengono applicate le metriche definite per la suite di rapporti [!DNL Analytics]. |
| [!UICONTROL Tipi di pubblico per reporting] | Per impostazione predefinita, nei rapporti sono mostrati i risultati per tutti i visitatori idonei. È possibile aggiungere tipi di pubblico per i rapporti per mostrare informazioni solo su tipi di pubblico specifici. Questa impostazione non è disponibile se si sceglie [!DNL Analytics] come soluzione di reporting. Il pubblico definito per la suite di rapporti [!DNL Analytics] è applicato. |

## Impostazioni avanzate {#section_E2FE441AFB324E498793ABB025ED9974}

La sezione [!UICONTROL Impostazioni avanzate] della pagina [!UICONTROL Obiettivi e impostazioni] consente di configurare le opzioni seguenti:

Per specificare le impostazioni avanzate, fai clic sull&#39;icona **[!UICONTROL Altro]** (puntini di sospensione verticali), quindi fai clic su **[!UICONTROL Impostazioni avanzate]**, come illustrato nella figura seguente.

![Menu Impostazioni avanzate](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/menu-advanced-settings-new.png)

>[!NOTE]
>
>Se utilizzi [!DNL Adobe Analytics] come origine per la generazione dei rapporti, le impostazioni vengono gestite dal server [!DNL Analytics]. L&#39;opzione Impostazioni avanzate non è disponibile.

![Impostazioni avanzate](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/advanced-settings.png)

| Impostazione | Descrizione |
|--- |--- |
| [!UICONTROL Quale metrica di successo deve essere raggiunta prima di incrementare questa metrica?] | Utilizza questa opzione per contare solo chi raggiunge la metrica di successo se in precedenza aveva raggiunto una metrica di successo diversa. Ad esempio, una conversione di attività potrebbe essere valida solo se il visitatore fa clic sull’offerta o raggiunge una pagina particolare prima della conversione. È possibile fornire la dipendenza su più metriche insieme alla flessibilità necessaria, per scegliere se la metrica debba essere raggiunta o meno per incrementare il conteggio. Definisci entrambe le metriche (o più metriche) di successo prima di renderle interdipendenti tra loro. L’opzione [!UICONTROL Aggiungi dipendenza] consente di incrementare la metrica di successo nel caso in cui un’altra metrica di successo venga raggiunta o meno. Per aggiungere una dipendenza:<ul><li>Dopo aver aggiunto le metriche aggiuntive, fai clic su [!UICONTROL Impostazioni avanzate].</li><li>Fai clic sull’opzione [!UICONTROL Aggiungi dipendenza]:</li><li>Trascina e rilascia le metriche desiderate dal riquadro di sinistra a quello di destra, quindi fai clic su [!UICONTROL Raggiunto] per scegliere tra [!UICONTROL Raggiunto] e[!UICONTROL &#x200B; Non raggiunto].</li><li>È possibile modificare o rimuovere le dipendenze dopo averle aggiunte.</li></ul> |
| [!UICONTROL Cosa succede quando un utente incontra questa metrica per obiettivo?] | Dopo che un visitatore raggiunge la metrica obiettivo, sono disponibili tre opzioni:<ul><li>Seleziona [!UICONTROL Incrementa il conteggio e mantieni utente attivo] per specificare la modalità di incremento del conteggio.</li><li>Seleziona [!UICONTROL Incrementa il conteggio, rilascia l’utente e consenti nuovo accesso] per specificare l’esperienza che l’utente vedrà se accede di nuovo all’attività.</li><li>Seleziona [!UICONTROL Incrementa il conteggio, rilascia l&#39;utente e impedisci nuovo accesso] per specificare cosa vedrà l&#39;utente al posto del contenuto dell&#39;attività.</li></ul> |
| [!UICONTROL Come verrà incrementato il conteggio?] | Sono disponibili tre opzioni per l’incremento del conteggio:<ul><li>[!UICONTROL Una volta per partecipante]</li><li>[!UICONTROL Su ogni impression (esclusi aggiornamenti pagina)]</li><li>[!UICONTROL Su ogni impression]</li></ul> |

Consulta [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) per ulteriori informazioni sulle impostazioni avanzate.

## Altri metadati {#section_2E8917BEFB954480A4206B9E9E917F80}

La sezione [!UICONTROL Altri metadati] della pagina [!UICONTROL Obiettivi e impostazioni] consente di specificare qualsiasi informazione sull&#39;attività utile da tenere a portata di mano per se stessi o per altri membri del team. Il riquadro Note è ridimensionabile.|

## Video di formazione

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Impostazioni attività (3:02) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video include informazioni sulle impostazioni delle attività.

* Inserire una finalità per l’attività
* Impostare il livello di priorità delle attività
* Orari di inizio e fine dell’attività
* Aggiungere tipi di pubblico da usare come filtri nella generazione di rapporti
* Inserire delle note per le attività

(https://video.tv.adobe.com/v/17381?captions=ita)

### Creazione di test A/B (8:36) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video mostra le impostazioni di attività nel flusso di lavoro guidato in tre passaggi durante la creazione di un’attività. Obiettivi e impostazioni sono discussi a partire dal 5:30.

* Creare un’attività A/B in Adobe Target
* Allocare il traffico con suddivisione manuale o automatica del traffico

>[!VIDEO](https://video.tv.adobe.com/v/17391)
