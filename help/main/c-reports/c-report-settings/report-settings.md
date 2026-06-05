---
keywords: Target;report;impostazioni dei report;preimpostazione;predefinito;preimpostazione target;predefinito target;metrica;pubblico;intervallo di date;impostazioni;download;visualizzazione tabella;visualizzazione grafico;incremento medio;incremento;contributo posizione;media corrente;metodologia di conteggio
description: Scopri come configurare le impostazioni dei rapporti in Adobe Target, compresi metriche, tipi di pubblico, intervalli di date e altro ancora.
title: Come si configurano le impostazioni dei rapporti?
feature: Reports
exl-id: 337579d1-c678-43b6-9e80-b5abe159c2d3
TQID: https://experienceleague.adobe.com/Nz7EFST7BeVE2FqfFkbWnp-hRJug7HPlOodak73H-Uo
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1932
ht-degree: 47%

---

# Impostazioni dei rapporti

Informazioni utili per impostare gli elementi da visualizzare nel report in [!DNL Adobe Target]. Le impostazioni dei rapporti possono essere salvate per un utilizzo successivo.

Per visualizzare un rapporto:

1. Fai clic su **[!UICONTROL Attività]**, quindi sull’attività desiderata tra quelle elencate.
1. Fai clic sulla scheda **[!UICONTROL Rapporti]**.

   ![Interfaccia utente per i rapporti](/help/main/c-reports/c-report-settings/assets/report-ui-refresh.png)

## Preimpostazione Target {#section_51F67341465045BEB4F1A2FB638A8EB1}

Puoi salvare fino a dieci diversi predefiniti del rapporto di una singola attività dopo averlo configurato come desiderato (metriche, pubblico, impostazioni avanzate e così via). Tutti gli utenti di [!DNL Target] possono visualizzare, modificare ed eliminare i vari predefiniti, indipendentemente da chi li ha creati.

Puoi anche configurare il rapporto di una singola attività come desiderato e salvare la configurazione come predefinito di default/preferito. Questa è la vista che viene visualizzata quando vedi che il rapporto dell&#39;attività sta avanzando.

### Creare un predefinito o un predefinito predefinito predefinito

1. Configura il rapporto dell&#39;attività come desideri.

   Di seguito sono illustrate le impostazioni disponibili, tra cui metriche, intervalli di date, tipi di pubblico, impostazioni avanzate e così via.

1. Accanto a **[!UICONTROL Predefinito target]**, fai clic sull&#39;icona **[!UICONTROL Altre opzioni]** ( ![Icona altre opzioni](/help/main/assets/icons/MoreSmallListVert.svg) ) > **[!UICONTROL Salva come nuovo]**.

   Viene visualizzata la finestra di dialogo [!UICONTROL Crea predefinito].

   ![Finestra di dialogo Nuovo predefinito](/help/main/c-reports/c-report-settings/assets/report_preset_dialog-new.png)

1. Rivedi le informazioni nelle sezioni **[!UICONTROL Filtri]** per verificare che il rapporto sia configurato come desiderato, quindi specifica il **[!UICONTROL Nome predefinito]** (fino a 50 caratteri).
1. (Condizionale) Se desideri che questa sia la tua visualizzazione predefinita/preferita del rapporto, imposta il **[!UICONTROL predefinito predefinito predefinito]** su Attivato.
1. Fai clic su **[!UICONTROL Crea]**.

### Seleziona un predefinito diverso

Seleziona la preimpostazione desiderata dall&#39;elenco a discesa **[!UICONTROL Preimpostazioni Target]**.

### Modificare un predefinito

1. Seleziona il predefinito da modificare.
1. Modifica la configurazione del rapporto come preferisci (metriche, intervalli di date, pubblico, impostazioni avanzate e così via).

   Dopo aver fatto clic su [!UICONTROL Salva] dopo aver modificato la configurazione del report, viene visualizzato un asterisco ( &#42; ) dopo il nome del predefinito per indicare che è stato modificato.

1. Fai clic sull&#39;icona **[!UICONTROL Altre opzioni]** ( ![Altre opzioni](/help/main/assets/icons/MoreSmallListVert.svg) ) > **[!UICONTROL Salva come nuovo]** per creare un nuovo predefinito.

### Eliminare un predefinito

1. Seleziona il predefinito da eliminare.
1. Fai clic sull&#39;icona **[!UICONTROL Altre opzioni]** ( ![Altre opzioni](/help/main/assets/icons/MoreSmallListVert.svg) ) > **[!UICONTROL Elimina]**.

1. Fai di nuovo clic su **[!UICONTROL Elimina]** per confermare l&#39;eliminazione (i predefiniti eliminati non possono essere recuperati).

### Gestione degli errori nei predefiniti

Gli avvisi e i messaggi all&#39;interno dei rapporti ti consentono di sapere se un predefinito non è più valido. L’avviso o il messaggio indica di scegliere un pubblico, una metrica, un gruppo di host o un&#39;esperienza differenti per creare un predefinito valido.

Nell&#39;elenco seguente sono descritte alcune delle situazioni che potrebbero provocare la mancata validità di un predefinito:

* Un pubblico di reporting è stato rimosso dall’attività ma è riportato nella definizione del predefinito.
* Una metrica (o più) è stata eliminata ma è riportata nella definizione del predefinito. Ad esempio, potresti eliminare una o più metriche dall&#39;attività e aggiungerne di nuove.
* Un gruppo di host (o più) non esiste ma è riportato nella definizione del predefinito.
* Un&#39;esperienza (o più) è stata eliminata dopo la creazione del predefinito, ma è riportata nella definizione del predefinito.
* Un predefinito non è valido perché le entità riportate esistono ancora ma sono state aggiornate in modo tale da modificare semanticamente la definizione del predefinito. Ad esempio, immagina di creare inizialmente un predefinito denominato “Ricavi da Chrome”. In seguito aggiorni l&#39;attività per misurare la metrica di Conversione anziché Ricavi. Questo aggiornamento alla definizione dell’attività invalida semanticamente la definizione del predefinito.

## [!UICONTROL Metrica report] {#section_894ABD7148244806B7CE556EBBA2AD62}

Fai clic sull&#39;elenco a discesa **[!UICONTROL Metrica rapporto]** per selezionare una [metrica di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) diversa o più metriche da visualizzare nel grafico.

Per impostazione predefinita, la metrica principale è determinata nella configurazione delle metriche di successo quando crei l’attività. Se modifichi la configurazione e salvi di nuovo l’attività, la metrica principale per la generazione dei rapporti si aggiorna.

Per ulteriori informazioni sulla selezione di più metriche da visualizzare nei report, vedere [Visualizzare più metriche in un report](/help/main/c-reports/c-report-settings/view-multiple-metrics.md#concept_9E3C3F6F3EC1412FAF252975AC0720B7).

## [!UICONTROL Pubblico] {#section_70926EB4618945D9AFF2B0564FF3717B}

Fai clic sull&#39;elenco a discesa **[!UICONTROL Pubblico]** per modificare il pubblico visualizzato per il rapporto.

Per ulteriori informazioni, consulta [Tipi di pubblico](/help/main/c-target/target.md#concept_A782F8481A5041EBA75103CB26376522).

## [!UICONTROL Intervallo date predefinito]

Fai clic sull&#39;elenco a discesa **[!UICONTROL Intervallo date predefinito]** per scegliere tra intervalli di date predefiniti.

Seleziona la nuova data di **[!UICONTROL Inizio]** e **[!UICONTROL Fine]** del report. Puoi anche utilizzare gli intervalli **[!UICONTROL Inizio attività]** e **[!UICONTROL Inizio attività - Fine attività]**.

Gli intervalli di date predefiniti includono: Ultimi 7 giorni, Ultimi 15 giorni o Ultimi 30 giorni. Questi intervalli di date predefiniti sono incrementali. Se la data di inizio è inferiore al numero di giorni scelti, il calendario visualizza l’intervallo dalla data di inizio, ma riproduce il calendario una volta che la data di inizio è più vecchia del numero di giorni scelti con l’aumento della durata dell’attività.

Per i rapporti sono previste le seguenti limitazioni di data:

* La data di inizio del rapporto deve risalire agli ultimi due anni.
* I rapporti sui gruppi di offerte sono limitati a 99 giorni da oggi.
* I rapporti orari sono limitati a 15 giorni.

## Intervallo date {#section_A410A768403C4E01891F95CB357E63ED}

Nella casella [!UICONTROL Intervallo date] viene visualizzato l&#39;intervallo di date corrente del report. Fai clic sull&#39;icona **[!UICONTROL Calendario]** ( ![Icona Calendario](/help/main/assets/icons/Calendar.svg) ) per visualizzare un calendario che consente di modificare l&#39;intervallo di date del rapporto.

## Impostazioni {#section_D99CE462107D45CABE0960F820E1E972}

Per configurare le impostazioni dei rapporti:

1. Fai clic sull&#39;icona **[!UICONTROL Impostazioni report]** ( ![Icona Impostazioni report](/help/main/assets/icons/Setting.svg) ), apporta le modifiche desiderate (come spiegato di seguito).
1. Fai clic su **[!UICONTROL Salva]** una volta eseguito.

A seconda del tipo di attività selezionato, le opzioni variano:

### Metodologia di conteggio

Seleziona la metodologia desiderata:

* Visitatori
* Visite
* Impression attività

### Controllo

Seleziona l’esperienza di controllo da utilizzare per calcolare e confrontare l’incremento.

### Ambiente {#environment}

Seleziona l’ambiente (gruppo host) da utilizzare per il rapporto. Per ulteriori informazioni, consulta [Host](/help/main/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E).

>[!NOTE]
>
>Se l&#39;organizzazione utilizza [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=it){target=_blank} (AEP) per inviare i dati delle metriche a [!DNL Target], l&#39;ambiente nello stream di dati di AEP deve corrispondere all&#39;ambiente nelle impostazioni del report [!DNL Target].

### Ripristina dati rapporto

Fare clic su [!UICONTROL Reimposta dati report]. Reimposta i dati di reporting per rimuovere i dati obsoleti. I visitatori attuali rimangono nell&#39;attività.  Questa opzione è disponibile solo per coloro che dispongono di autorizzazioni [!UICONTROL Approvatore].

>[!IMPORTANT]
>
>Questa è un’azione permanente e non può essere annullata.

Escludere i valori estremi

L&#39;opzione [!UICONTROL Escludi valori estremi] è applicabile solo alle attività con tipi di metrica di ricavi e coinvolgimento. Per ulteriori informazioni, consulta [Esclusione di ordini estremi](/help/main/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA).

## Scarica {#section_77E65C50BAAF4AB79242DB3A8778ADEF}

Fai clic sull&#39;icona **[!UICONTROL Scarica]** ( ![Icona Scarica](/help/main/assets/icons/Download.svg) ) per scaricare i dati del rapporto in formato [!DNL .csv] per l&#39;importazione rapida in Excel, Access o altri programmi di analisi dei dati.

Per ulteriori informazioni, consulta [Download di dati in un file CSV](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md).

## Aggiorna {#section_E203729F2F314DF3856D2EE67C60B370}

Fai clic sull&#39;icona **[!UICONTROL Aggiorna]** ( ![Icona Aggiorna](/help/main/assets/icons/Refresh.svg) ) per aggiornare la tabella e il grafico di un report senza aggiornare l&#39;intera pagina, la configurazione o l&#39;intervallo di date.

## Altre opzioni {#section_AB1B5C695D7045A0A0AC0E2698D2E7DE}

Fai clic sull&#39;icona **[!UICONTROL Altre opzioni]** ( ![Altre opzioni](/help/main/assets/icons/MoreSmallListVert.svg) ) per accedere alle opzioni [!UICONTROL Salva come nuovo] e [!UICONTROL Elimina].

## Opzioni di visualizzazione

Puoi visualizzare il rapporto in vari formati, a seconda del tipo di attività. Seleziona l’opzione desiderata.

* **Vista tabella**: fare clic sull&#39;icona **[!UICONTROL Vista tabella]** (![Icona Vista tabella](/help/main/assets/icons/Table.svg) ) per visualizzare il report come tabella.
* **Vista grafico**: fai clic sull&#39;icona **[!UICONTROL Vista grafico]** (![Icona Vista grafico](/help/main/assets/icons/GraphTrend.svg) ) per visualizzare il rapporto sotto forma di grafico.
* **Segmenti automatizzati**:(disponibile solo per [!UICONTROL attività Automated Personalization] (AP) e [!UICONTROL Targeting automatico] (AT).) Fai clic sull&#39;icona **[!UICONTROL Segmenti automatizzati] (![icona Segmenti automatizzati](/help/main/assets/icons/AutomatedSegment.svg) ) per visualizzare il [rapporto Segmenti automatizzati](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md).
* **Attributi importanti**: (disponibile solo per le attività [!DNL Automated Personalization] (AP) e [!UICONTROL Targeting automatico] (AT).) Fai clic sull&#39;icona **[!UICONTROL Attributi importanti]** ( ![Icona Attributi importanti](/help/main/assets/icons/ViewList.svg) ) per visualizzare il [report Attributi importanti](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md).

## Incremento medio, limiti di incremento e intervallo di affidabilità {#section_0D87615B1D3344B3858BA494EEBC16FB}

I rapporti includono diversi punti di dati e rappresentazioni di visualizzazione che consentono di comprendere i limiti di incremento e il livello di affidabilità associati all’attività. Ciò consente di determinare più accuratamente un vincitore.

Per ulteriori informazioni, vedere [Calcoli statistici nei test A/Bn](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

Considera i seguenti aspetti:

* Disponibile solo quando si visualizzano i report in [!UICONTROL Vista tabella].
* Questa funzionalità non è disponibile per le attività che utilizzano [Analytics come origine per la generazione di rapporti (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

## Contributo posizione {#section_5832F126AC114AE1ABFFF4D9B904393B}

Fai clic sull&#39;icona [[!UICONTROL Contributo posizione]](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) ( ![Icona Contributo posizione](/help/main/assets/icons/LocationContribution.svg) ) per far sì che il rapporto mostri il contributo in base alla posizione per le attività Test multivariato (MVT).

## Esperienze {#section_3A450DE1FA7E43F0AAB73165EC3D1C34}

Disponibile solo quando si visualizza il report in [!UICONTROL Vista grafico].

Seleziona o deseleziona le esperienze sul lato sinistro del grafico per visualizzare o nascondere dal grafico le esperienze corrispondenti.

## Media corrente {#section_59066693158C4433B87D07402C2BC6CD}

Disponibile solo quando si visualizza il report in [!UICONTROL Vista grafico].

La &quot;Media corrente&quot; riflette le conversioni cumulative (dall’inizio dell’intervallo di reporting alla data rappresentata sul grafico) divise per i visitatori cumulativi.

Seleziona la vista grafico desiderata:

* Media corrente
* Media corrente - Incremento
* Giornaliero
* Incremento giornaliero

Il nome dell’elenco a discesa varia a seconda della vista selezionata, ma sarà una delle viste elencate in precedenza.

## Metodologia di conteggio {#section_01B0ED5665C74AE1AE97259800190C3E}

Disponibile solo quando si visualizza il report in [!UICONTROL Vista grafico].

È possibile scegliere la metodologia di conteggio per i grafici del rapporto. Nota che questo non è supportato per [!UICONTROL attività Automated Personalization] (AP).

Per accedere all&#39;opzione [!UICONTROL Metodologia di conteggio], durante la visualizzazione di un report in modalità grafico fare clic sull&#39;elenco a discesa **[!UICONTROL Obiettivo principale]**, quindi selezionare la metodologia di conteggio.

La metodologia di conteggio sarà la stessa di quella selezionata nella finestra di dialogo [!UICONTROL Impostazioni], sopra descritta.

Per impostazione predefinita, il grafico è tracciato in modalità [!UICONTROL Giornaliero].

Puoi modificare la modalità facendo clic sull&#39;elenco a discesa [!UICONTROL Giornaliero] e selezionando un&#39;opzione cumulativa.

>[!NOTE]
>
>Il nome dell’elenco a discesa varia a seconda della modalità selezionata.

Sono disponibili quattro modalità per le attività [!UICONTROL Targeting automatico]: [!UICONTROL Controllo giornaliero], [!UICONTROL Target giornaliero], [!UICONTROL Controllo cumulativo] e [!UICONTROL Target cumulativo].

L’ordine predefinito in cui viene tracciato il grafico è il seguente:

* **[!UICONTROL Test A/B] (inclusi [!UICONTROL Allocazione automatica] e [!UICONTROL Automated Personalization])**: ordine di creazione dell&#39;esperienza, in ordine decrescente.
* **[!UICONTROL Targeting esperienza] (XT)**: ordine delle esperienze nell&#39;attività.
* **[!UICONTROL Test multivariato] (MVT)**: alfabetico per nome esperienza.
* **[!UICONTROL Consigli]**: ordine di creazione dell&#39;esperienza, in ordine decrescente.

Mentre lavori con le opzioni [!UICONTROL Metodologia di conteggio], considera le seguenti avvertenze:

* Per le attività [[!UICONTROL Targeting automatico]](/help/main/c-activities/auto-target/auto-target-to-optimize.md), non è possibile selezionare &quot;Visitatori&quot; come metodologia di conteggio. [!UICONTROL Targeting automatico] è l&#39;unico tipo di attività che non è possibile tracciare dai visitatori.
* Per le attività che utilizzano [Analytics come origine per la generazione di rapporti (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md), non è possibile tracciare cumulativamente Visitatore, Visita o Impression.

## Utilizzo di grafici con più di 16 esperienze nell’attività

Se le esperienze di un’attività sono meno di 16, ogni esperienza è rappresentata da un colore diverso nel grafico.

Se le esperienze sono più di 16, nel grafico vengono tracciate le linee colorate delle prime 16. Le restanti esperienze sono visualizzate in grigio nel riquadro Esperienze a sinistra e le linee corrispondenti non sono incluse nel grafico. In un dato momento è possibile visualizzare le linee corrispondenti a 16 esperienze.

Se passi il puntatore su una delle esperienze in grigio, sul grafico viene visualizzata temporaneamente la corrispondente linea grigia. Per visualizzare con un colore la linea di un’esperienza grigia, fai clic sul nome di un’esperienza visualizzata a colori per deselezionarla, quindi fai clic sul nome dell’esperienza grigia desiderata per selezionarla.

Il grafico mostra le linee delle prime 16 esperienze (alcune si sovrappongono, quindi sembra che siano meno di 16). Il punto colorato nel riquadro Esperienze a sinistra indica il colore associato all’esperienza corrispondente.

Se scorri verso il basso nel riquadro Esperienze, puoi notare che i nomi delle esperienze dalla 17 alla 26 sono in grigio, come illustrato nella figura seguente:

Se passi il cursore del mouse sopra una delle esperienze in grigio, sul grafico viene visualizzata temporaneamente la corrispondente linea grigia.

Supponiamo che desideri visualizzare la linea dell’esperienza R e nascondere quella linea dell’esperienza P. Fai clic sul nome dell’esperienza P per deselezionarla, quindi fai clic sul nome dell’esperienza R per selezionarla, come illustrato di seguito:
