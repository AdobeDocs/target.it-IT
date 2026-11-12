---
keywords: personalizzazione automatizzata;ap
description: Scopri come creare un'attività [!UICONTROL Automated Personalization] (AP) utilizzando il [!UICONTROL Compositore esperienza visivo].
title: Come si crea un'attività [!UICONTROL Automated Personalization]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Automated Personalization
exl-id: eadc2bbc-310b-479f-b75b-253e8d7aa812
TQID: 'https://experienceleague.adobe.com/5eUFwob4BekIJP4SM2lrSDQam4h1AXIByJjM7-1RNL8'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: c86619f0c004279bf4d9b871c84bf2e37ba932b7
workflow-type: tm+mt
source-wordcount: '1963'
ht-degree: 17%
---
# Crea un&#39;attività [!UICONTROL Automated Personalization] {#create-ap-activity}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come creare un&#39;attività **[!UICONTROL Automated Personalization]** (AP) nel **[!UICONTROL Compositore esperienza visivo]** (VEC). Puoi creare le tue esperienze, impostare il targeting e un gruppo di controllo, quindi configurare obiettivi e impostazioni.

>[!ENDSHADEBOX]

Il flusso di lavoro dell&#39;attività **[!UICONTROL Automated Personalization]** in [!DNL Target] è diverso da quello degli altri tipi di attività. Segue il flusso di lavoro guidato in tre passaggi nel **[!UICONTROL Compositore esperienza visivo]**:

1. [Creare esperienze](#build-experiences)
1. [Imposta targeting](#set-targeting)
1. [Configurare obiettivi e impostazioni](#configure-goals-and-settings)

## Prima di iniziare {#before-you-begin}

Per prestazioni ottimali, mantieni le attività **[!UICONTROL Automated Personalization]** e **[!UICONTROL Targeting automatico]** entro i seguenti limiti:

* 4-6 posizioni, con 4-6 offerte per posizione.
* Meno di 5.000 esperienze totali per ottenere risultati ottimali. Il limite rigido è di 30.000 e lo stesso limite si applica quando l&#39;opzione **[!UICONTROL Non consentire duplicati]** è abilitata.

Il numero totale di esperienze cresce dalla combinazione cartesiana di posizioni e offerte. Configurazioni più grandi possono rallentare il caricamento o la modifica nel **[!UICONTROL Compositore esperienza visivo]**.

## Passaggio 1: creare esperienze {#build-experiences}

Definisci il pool di varianti di contenuto su cui **[!UICONTROL Automated Personalization]** può eseguire la personalizzazione. Più le tue esperienze e offerte sono ricche e distinte, migliore è la capacità dell’algoritmo di associare il contenuto giusto a ogni visitatore.

### Creare l’attività {#create-activity}

Avvia l&#39;attività e apri la pagina che desideri personalizzare nel **[!UICONTROL Compositore esperienza visivo]**.

1. Dall&#39;elenco [!DNL Target] **[!UICONTROL Attività]**, fare clic su **[!UICONTROL Crea attività]** > **[!UICONTROL Automated Personalization]**.

   ![](../assets/ap-activities-2.png)

1. Scegli il Compositore esperienza:

   * Per utilizzare il **[!UICONTROL Compositore esperienza visivo]** (VEC), fare clic su **[!UICONTROL Visivo]**.

   * Per utilizzare il **[!UICONTROL Compositore esperienza basato su moduli]**, seleziona **[!UICONTROL Modulo]**. Per ulteriori informazioni, consulta [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

     >[!NOTE]
     >
     >Oltre al Compositore esperienza visivo e al Compositore esperienza basato su moduli **[!UICONTROL 1}, [!DNL Target] offre il**[!UICONTROL  Compositore esperienza visivo per applicazione a pagina singola ]**.]** Per ulteriori informazioni sui vari moduli di composizione, consulta [Esperienze e offerte](/help/main/c-experiences/experiences.md). Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, vedere [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

     ![](../assets/ap-activities-3.png)

1. (Condizionale) [Scegliere un&#39;area di lavoro](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Nella casella **[!UICONTROL Immetti URL attività]**, specifica l&#39;[URL attività](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md). Se l’account è [configurato con un URL predefinito](/help/main/administrating-target/visual-experience-composer-set-up.md), questo verrà visualizzato come impostazione predefinita. Se necessario, puoi passare dall’URL predefinito a un altro.

   [!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `http://www.adobe.com`] e [!DNL `https://www.adobe.com`] corrispondono entrambi.

1. Quindi fare clic su **[!UICONTROL Crea]**. La pagina con l’URL specificato viene aperta nel Compositore esperienza visivo.

1. Per assegnare un nome all&#39;attività, fare clic sull&#39;icona **[!UICONTROL Modifica]** ( ![Modifica icona](/help/main/assets/icons/Edit.svg) ) e specificare un nome descrittivo per l&#39;attività, quindi fare clic su **[!UICONTROL Salva]**.

   {{activity-name-rules}}

   ![](../assets/ap-activities-1.png)

### Progettare il contenuto {#design-content}

Configura il contenuto che l’algoritmo può combinare ed escludi le esperienze che non desideri.

1. Modificare gli elementi della pagina come descritto in [Opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   * Per visualizzare rapidamente l’anteprima di più immagini, seleziona più immagini contemporaneamente da Gestione risorse. Puoi quindi visualizzare la pagina con ciascuna delle immagini configurate per l’attività.
   * Per modificare il testo nelle offerte, modifica l’elemento di testo direttamente nella pagina.

   Quando si modifica un elemento, vengono visualizzate barre su tale elemento per indicare che è stato modificato.

1. Fai clic sull&#39;icona **[!UICONTROL Gestisci contenuto]** ( ![icona Gestisci contenuto](/help/main/assets/icons/Experience.svg) ) per configurare le combinazioni disponibili.

   Viene visualizzata la finestra di dialogo **[!UICONTROL Gestisci contenuto]** con due schede: **[!UICONTROL Esperienze]** e **[!UICONTROL Offerte]**.

   ![](../assets/ap-activities-4.png)

1. Nella scheda **[!UICONTROL Esperienze]**, controlla l&#39;elenco delle parti di contenuto e la posizione a cui ciascuna di esse è assegnata.

1. (Facoltativo) Per escludere delle esperienze dall&#39;attività, seleziona la casella di controllo per ogni esperienza da escludere, quindi fai clic sull&#39;icona **[!UICONTROL Escludi]**.

   Per ulteriori opzioni, vedi [Gestione delle esclusioni](/help/main/c-activities/t-automated-personalization/managing-exclusions.md).

   ![](../assets/ap-activities-5.png)

1. (Condizionale) Fai clic sulla scheda **[!UICONTROL Offerte]** per gestire le offerte nell&#39;attività.

   * Per organizzare le offerte per il reporting, seleziona parti di contenuto e assegnale a gruppi di reporting. Per ulteriori informazioni, consulta [Gruppi di reporting di offerte in Automated Personalization](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md).
   * Per limitare il numero di utenti che visualizzano un’offerta, utilizza il targeting per consentire solo a determinati visitatori di visualizzare tale offerta.

<!--
1. (Conditional) Click **[!UICONTROL Exclusion Groups]** to choose any combination of elements that you want to exclude from the activity.

   ![Exclusion Groups tab of Manage Content dialog box](/help/main/c-activities/t-automated-personalization/assets/exclusion_groups-new.png)

   Although you can create up to 30,000 experiences in an AP test, the algorithm performs its best when fewer than 10,000 distinct experiences are used. This same limit is applied even when the activity has enabled the **[!UICONTROL Disallow Duplicates]** option.

   If you do not currently have any exclusion groups included in your activity, click **Create Exclusion Group**. You can filter to create a list that shows only the combinations you want to exclude. Name your exclusion group, then click **Save**.

   To edit an existing exclusion group, hover over the group you want to edit, then click the pencil icon.
-->

1. Fai clic su **[!UICONTROL Fine]** una volta completata la configurazione del contenuto dell&#39;attività.

## Passaggio 2: impostare il targeting {#set-targeting}

Decidi quali visitatori accedono all’attività e quanta parte del traffico è esposto. Associali a un gruppo di controllo in modo che [!DNL Target] possa misurare i risultati della personalizzazione dell&#39;incremento.

1. Fai clic su **[!UICONTROL Targeting]** nella parte superiore del **[!UICONTROL Compositore esperienza visivo]** per passare al passaggio successivo nel flusso di lavoro guidato in tre passaggi.

   ![Passaggio destinazione test AP](/help/main/c-activities/t-automated-personalization/assets/ap-traffic-flow.png)

1. (Facoltativo) Fai clic sul controllo **[!UICONTROL Tutti i visitatori]** per [selezionare un altro pubblico](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) per l&#39;attività e impostarne la percentuale di visitatori.

   Il pubblico **[!UICONTROL Tutti i visitatori]** è impostato come predefinito. Se selezioni un altro pubblico, il suo nome viene visualizzato nel controllo più a sinistra. Ad esempio, puoi limitare l’accesso al 50% di tutti i visitatori o 45% del pubblico “Californians”.

1. Fare clic sul controllo **[!UICONTROL Allocazione traffico]** e scegliere una delle opzioni seguenti:

   ![Opzioni obiettivo di allocazione traffico](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation-goal-ap-new.png)

   +++Opzioni obiettivo di allocazione traffico

   | Opzione | Quando utilizzarlo |
   |--- |--- |
   | **[!UICONTROL Valuta algoritmo Personalization (50/50)]** | Il tuo obiettivo è quello di testare l&#39;algoritmo. I visitatori sono suddivisi 50/50 tra il controllo e l’algoritmo di destinazione. Questa suddivisione fornisce la stima più accurata dell’incremento ed è il modo più veloce e accurato per verificare se le prestazioni dell’algoritmo sono migliori rispetto all’assenza di personalizzazione (ad esempio, un controllo fornito in modo casuale). Consigliato per l’utilizzo con &quot;esperienze casuali&quot; come controllo. |
   | **[!UICONTROL Massimizzazione del traffico Personalization (90/10)]** | L&#39;obiettivo è quello di creare un&#39;attività &quot;sempre attiva&quot;. Il 10% dei visitatori entra nel controllo, il che assicura che ci siano abbastanza dati per consentire agli algoritmi di continuare a imparare nel tempo. Questo è il modo più veloce e preciso per massimizzare la quantità di traffico personalizzato quando sei meno interessato all’incremento esatto. Il compromesso è che si ha meno precisione in cosa sia l&#39;incremento esatto. Indipendentemente dall’obiettivo, questa opzione è la suddivisione del traffico consigliata quando utilizzi come controllo un’esperienza specifica. |
   | **[!UICONTROL Personalizza allocazione]** | Si desidera dividere la percentuale manualmente. |

   +++

1. (Condizionale) Dall&#39;elenco a discesa **[!UICONTROL Controllo]**, [selezionare un&#39;esperienza specifica da utilizzare come controllo](/help/main/c-activities/t-automated-personalization/experience-as-control.md) oppure selezionare **[!UICONTROL Esperienza casuale]**.

   L&#39;esperienza di controllo fornisce un confronto per determinare l&#39;incremento fornito dal test automatizzato. **[!UICONTROL Automated Personalization]** misura sempre le prestazioni rispetto a un gruppo di controllo. La migliore prassi è quella di collocare almeno il 10% dei partecipanti nel gruppo di controllo.

   >[!NOTE]
   >
   >Nelle attività di **[!UICONTROL Automated Personalization]**, i criteri di ingresso (targeting URL, regole modello e destinazioni pubblico) vengono valutati per ogni richiesta. Nelle versioni precedenti, i criteri di ingresso venivano valutati una volta a sessione.

## Passaggio 3: configurare obiettivi e impostazioni {#configure-goals-and-settings}

Dire a [!DNL Target] come si presenta il successo. L’obiettivo di ottimizzazione scelto è la metrica su cui l’algoritmo di personalizzazione si allinea, quindi scegli il risultato più importante per questa attività.

1. Fai clic su **[!UICONTROL Avanti]** per visualizzare la pagina **[!UICONTROL Obiettivi e impostazioni]**.

1. Configura l&#39;attività con le impostazioni seguenti, quindi fai clic su **[!UICONTROL Salva e chiudi]**.

   | Impostazione | Descrizione |
   |--- |--- |
   | **[!UICONTROL Nome]** | Assegna un nome all’attività. Assegna all&#39;attività un nome sufficientemente descrittivo da consentire ai membri del team di riconoscerla nell&#39;elenco **[!UICONTROL Attività]**. Segui le regole del nome attività descritte in [Passaggio 1: Creare esperienze](#build-experiences). |
   | **[!UICONTROL Obiettivo]** | (Facoltativo) Inserire la finalità del test. La finalità aiuta a ricordare lo scopo dell&#39;attività. |
   | **[!UICONTROL Priorità]** | Decide quale attività viene visualizzata quando diverse attività condividono una posizione e un pubblico. Vedere [Impostare la priorità](#set-priority). |
   | **[!UICONTROL Durata]** | Imposta le date di inizio e di fine dell&#39;attività. Puoi selezionare **[!UICONTROL Quando è attivato]** oppure specificare una data e un&#39;ora specifiche. |
   | **[!UICONTROL Obiettivo di ottimizzazione]** | La metrica su cui si basa l’algoritmo di personalizzazione. Vedi [Imposta l&#39;obiettivo di ottimizzazione](#set-optimization-goal). |
   | **[!UICONTROL Metrica di conversione]** | Per impostazione predefinita, la metrica di conversione è la stessa della metrica dell’obiettivo di ottimizzazione. Tuttavia, puoi definire una metrica di conversione separata deselezionando l&#39;opzione **[!UICONTROL Uguale all&#39;obiettivo di ottimizzazione]**. |
   | **[!UICONTROL Altre metriche]** | Aggiungi eventuali metriche di reporting aggiuntive da utilizzare. Puoi aggiungere metriche di conversione o ricavi.<P>**Nota**: la metrica **[!UICONTROL Coinvolgimento]** non è supportata come metrica aggiuntiva. L&#39;interfaccia utente di [!DNL Target] potrebbe consentire di selezionare la metrica **[!UICONTROL Coinvolgimento]**, ma i dati non vengono visualizzati con precisione nei report. |
   | **[!UICONTROL Tipi di pubblico per reporting]** | Aggiungi tipi di pubblico per poter filtrare i rapporti in base al pubblico. Per impostazione predefinita, il rapporto mostra risultati per tutti i visitatori idonei. Aggiungi dei tipi di pubblico per filtrare i risultati per sottoinsiemi più specifici di visitatori.<P>**Nota**: a differenza di altri tipi di attività, **[!UICONTROL Automated Personalization]** non può utilizzare **[!UICONTROL Adobe Analytics]** come origine per la generazione di rapporti (A4T). |
   | **[!UICONTROL Note]** | Inserisci informazioni sull’attività, utili per te o per gli altri membri del gruppo. Il riquadro **[!UICONTROL Notes]** è ridimensionabile. |

   Quando denomini o rinomini una metrica, i seguenti caratteri non sono consentiti: `/`, `?`, `#`, `:`, `=`, `+`, `-` e `@`.

### Impostare la priorità {#set-priority}

La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.

A seconda delle impostazioni, l&#39;interfaccia utente di [!DNL Target] e le opzioni per **[!UICONTROL Priorità]** variano:

* **Priorità legacy (impostazione predefinita):** Se le priorità precise non sono abilitate, specifica una priorità di **[!UICONTROL Bassa]**, **[!UICONTROL Medium]** o **[!UICONTROL Alta]**.
* **Priorità precise:** Specificare un valore compreso tra 0 e 999, dove 0 = bassa e 999 = alta. Per abilitare questa opzione, fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Generazione rapporti]**, quindi attiva l&#39;opzione **[!UICONTROL Abilita priorità precise]**.

Per le attività create con le versioni precedenti di [!DNL Target Standard/Premium], la priorità **[!UICONTROL Bassa]** è convertita in 0, la priorità **[!UICONTROL Medium]** è convertita in 5 e la priorità **[!UICONTROL Alta]** in 10. Se necessario, è possibile modificare questi valori.

>[!NOTE]
>
>Prima di poter disabilitare le priorità dettagliate dopo averle utilizzate, tutte le priorità devono essere impostate su 0, 5 o 10.

### Impostare l’obiettivo di ottimizzazione {#set-optimization-goal}

L’obiettivo di ottimizzazione è costituito da due parametri:

* Ciò che desideri misurare con l&#39;attività
* Azione eseguita da un partecipante all&#39;attività che indica che l&#39;obiettivo è stato raggiunto

Puoi scegliere di denominare l&#39;obiettivo di ottimizzazione selezionando i tre punti a destra di **[!UICONTROL Obiettivo principale]**. Le attività di **[!UICONTROL Automated Personalization]** possono misurare **[!UICONTROL Conversion]** o **[!UICONTROL Revenue]**. La conversione può essere ottenuta visualizzando una pagina o una mbox. È possibile inoltre il tracciamento dei clic.

L’obiettivo principale diventa anche la metrica di modellazione utilizzata dal sistema di modellazione per calcolare il successo dell’esperienza.

I visitatori possono essere mantenuti nell&#39;attività per scopi di tracciamento, dopo aver raggiunto l&#39;obiettivo di modellazione. Ad esempio, spesso per migliorare i click-rate viene utilizzata un&#39;attività **[!UICONTROL Automated Personalization]** impostata come obiettivo di modellazione. Tuttavia, è importante vedere in che modo l’aumento dei tassi di clic porta alla conversione finale, pertanto è essenziale tenere traccia di tutta la conversione finale.

#### Rendere una metrica dipendente da un’altra {#add-dependency}

È possibile fornire la dipendenza su più metriche insieme alla flessibilità necessaria, per scegliere se la metrica debba essere raggiunta o meno per incrementare il conteggio. È necessario definire entrambe le metriche (o più metriche) di successo prima di renderle interdipendenti tra loro. L’opzione **[!UICONTROL Aggiungi dipendenza]** consente di incrementare la metrica di successo nel caso in cui un’altra metrica di successo venga raggiunta o meno.

Per aggiungere una dipendenza:

1. Dopo aver aggiunto ulteriori metriche, fai clic su **[!UICONTROL Impostazioni avanzate]** sotto il menu a tre punti a destra di **[!UICONTROL Obiettivo aggiuntivo]**.

1. Fai clic sull&#39;opzione **[!UICONTROL Aggiungi dipendenza]** nella parte inferiore della sezione **[!UICONTROL Impostazioni reporting]**.

1. Trascina e rilascia le metriche desiderate dal riquadro di sinistra a quello di destra, quindi fai clic su **[!UICONTROL Raggiunto]** per scegliere tra **[!UICONTROL Raggiunto]** e **[!UICONTROL Non raggiunto]**.

È possibile modificare o rimuovere le dipendenze dopo averle aggiunte.

## Visualizzare l’anteprima delle esperienze {#preview-experiences}

Controlla l’aspetto delle esperienze sul sito prima di avviare l’attività.

1. Dopo aver fatto clic su **[!UICONTROL Salva e chiudi]**, viene visualizzata la pagina **[!UICONTROL Panoramica]** dell&#39;attività. Fai clic su **Anteprima esperienze**.

1. Nel pop-up che appare, visualizza e condividi i collegamenti alle esperienze di Personalizzazione automatizzata sul tuo sito. Questi collegamenti forniscono una &quot;anteprima fedele&quot; delle esperienze al di fuori del **[!UICONTROL Target]** **[!UICONTROL Compositore esperienza visivo]**.

   >[!NOTE]
   >
   >Per condividere l’anteprima, è necessario condividere i collegamenti dal messaggio. Non è possibile fare clic su un collegamento e quindi copiare l’URL direttamente dal browser. Copiare il collegamento fa sì che l’URL contenga un parametro che visualizza correttamente la pagina solo quando si accede alla pagina dal collegamento nel messaggio.

Per informazioni sul reporting, consulta [Rapporti di Automated Personalization](/help/main/c-reports/personalization-reports/reports-ap.md).
