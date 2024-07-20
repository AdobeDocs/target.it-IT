---
keywords: Target;report;impostazioni dei report;preimpostazione;predefinito;preimpostazione target;predefinito target;metrica;destinatari;intervallo di date;impostazioni;download;visualizzazione tabella;visualizzazione grafico;incremento medio;incremento;contributo posizione;media corrente;metodologia di conteggio
description: Scopri come configurare le impostazioni dei rapporti in Adobe Target, compresi metriche, tipi di pubblico, intervalli di date e altro ancora.
title: Come si configurano le impostazioni dei rapporti?
feature: Reports
exl-id: 337579d1-c678-43b6-9e80-b5abe159c2d3
source-git-commit: 7de7bb1b3bc70a559d41edece8cae2d388cb0dda
workflow-type: tm+mt
source-wordcount: '1892'
ht-degree: 54%

---

# Impostazioni dei rapporti

Informazioni utili per impostare gli elementi da visualizzare nel report in [!DNL Adobe Target]. Le impostazioni dei rapporti possono essere salvate per un utilizzo successivo.

Per visualizzare un rapporto:

1. Fai clic su **[!UICONTROL Activities]**, quindi sull’attività desiderata tra quelle elencate.
1. Fare clic sulla scheda **[!UICONTROL Reports]**.

   ![Interfaccia utente per i rapporti](/help/main/c-reports/c-report-settings/assets/report_ui-new.png)

## Preimpostazione Target {#section_51F67341465045BEB4F1A2FB638A8EB1}

Puoi salvare fino a dieci diversi predefiniti del rapporto di una singola attività dopo averlo configurato come desiderato (metriche, destinatari, impostazioni avanzate e così via). Tutti gli utenti di [!DNL Target] possono visualizzare, modificare ed eliminare i vari predefiniti, indipendentemente da chi li ha creati.

Puoi anche configurare il rapporto di una singola attività come desiderato e salvare la configurazione come predefinito di default/preferito. Questa è la vista che compare quando vedi che il rapporto dell&#39;attività sta avanzando.

### Creare un predefinito o un predefinito predefinito predefinito

1. Configura il rapporto dell&#39;attività come desideri.

   Di seguito sono illustrate le impostazioni disponibili, tra cui metriche, intervalli di date, tipi di pubblico, impostazioni avanzate e così via.

1. Accanto a **[!UICONTROL Target Preset]**, fare clic sull&#39;icona dei tre puntini di sospensione verticali > **[!UICONTROL Save as New]**.

   ![Predefinito per rapporto](/help/main/c-reports/c-report-settings/assets/report_preset-new.png)

   Viene visualizzata la finestra di dialogo Nuovo predefinito:

   ![Finestra di dialogo Nuovo predefinito](/help/main/c-reports/c-report-settings/assets/report_preset_dialog-new.png)

1. Esaminare le informazioni nelle sezioni **[!UICONTROL Filters]** e **[!UICONTROL Settings]** per verificare che il report sia configurato come desiderato, quindi specificare **[!UICONTROL Preset Name]** (fino a 50 caratteri).
1. (Facoltativo) Se desideri che questa sia la tua visualizzazione predefinita/preferita del rapporto, imposta il pulsante **[!UICONTROL Set as default preset]** su Attivato.
1. Fare clic su **[!UICONTROL Save]**.

### Seleziona un predefinito diverso

Selezionare il predefinito desiderato dall&#39;elenco a discesa **[!UICONTROL Target Preset]**.

![Elenco a discesa Predefinito](/help/main/c-reports/c-report-settings/assets/report_preset_drop-down-new.png)

### Modificare un predefinito

1. Seleziona il predefinito da modificare.
1. Modifica la configurazione del rapporto come preferisci (metriche, intervalli di date, destinatari, impostazioni avanzate e così via).

   Dopo aver fatto clic su [!UICONTROL Save] dopo aver modificato la configurazione del report, viene visualizzato un asterisco ( &#42; ) dopo il nome del predefinito per indicare che è stato modificato, come illustrato di seguito:

   ![Predefinito per rapporto con asterisco](/help/main/c-reports/c-report-settings/assets/report_preset_asterisk-new.png)

1. Fai clic sull&#39;icona dei tre puntini di sospensione verticali > **[!UICONTROL Save as New]** per creare un nuovo predefinito.

   Oppure

   Fai clic sull&#39;icona dei tre puntini di sospensione verticali > **[!UICONTROL Update]** per aggiornare il predefinito corrente.

   ![Aggiorna predefinito del rapporto](/help/main/c-reports/c-report-settings/assets/report_preset_update-new.png)

### Eliminare un predefinito

1. Seleziona il predefinito da eliminare.
1. Fai clic sull&#39;icona dei tre puntini di sospensione verticali > **[!UICONTROL Delete]**.

   ![Elimina predefinito del rapporto](/help/main/c-reports/c-report-settings/assets/report_preset_delete-new.png)

1. Fai di nuovo clic su **[!UICONTROL Delete]** per confermare l&#39;eliminazione (i predefiniti eliminati non possono essere recuperati).

### Gestione degli errori nei predefiniti

Gli avvisi e i messaggi all&#39;interno dei rapporti ti consentono di sapere se un predefinito non è più valido. L&#39;avviso o il messaggio indica di scegliere dei destinatari, una metrica, un gruppo di host o un&#39;esperienza differenti per rendere valido il predefinito.

Nell&#39;elenco seguente sono descritte alcune delle situazioni che potrebbero provocare la mancata validità di un predefinito:

* Un gruppo di destinatari di reporting è stato rimosso dall&#39;attività ma è riportato nella definizione del predefinito.
* Una metrica (o più) è stata eliminata ma è riportata nella definizione del predefinito. Ad esempio, potresti eliminare una o più metriche dall&#39;attività e aggiungerne di nuove.
* Un gruppo di host (o più) non esiste ma è riportato nella definizione del predefinito.
* Un&#39;esperienza (o più) è stata eliminata dopo la creazione del predefinito, ma è riportata nella definizione del predefinito.
* Un predefinito non è valido perché le entità riportate esistono ancora ma sono state aggiornate in modo tale da modificare semanticamente la definizione del predefinito. Ad esempio, immagina di creare inizialmente un predefinito denominato “Ricavi da Chrome”. In seguito aggiorni l&#39;attività per misurare la metrica di Conversione anziché Ricavi. Questo aggiornamento alla definizione dell’attività invalida semanticamente la definizione del predefinito.

## Metrica rapporto {#section_894ABD7148244806B7CE556EBBA2AD62}

Fai clic sull&#39;elenco a discesa **[!UICONTROL Report Metric]** per selezionare una [metrica di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) diversa o più metriche da visualizzare nel grafico.

Per impostazione predefinita, la metrica principale è determinata nella configurazione delle metriche di successo quando crei l’attività. Se modifichi la configurazione e salvi di nuovo l’attività, la metrica principale per la generazione dei rapporti si aggiorna.

Per ulteriori informazioni sulla selezione di più metriche da visualizzare nei report, vedere [Visualizzare più metriche in un report](/help/main/c-reports/c-report-settings/view-multiple-metrics.md#concept_9E3C3F6F3EC1412FAF252975AC0720B7).

## Destinatari {#section_70926EB4618945D9AFF2B0564FF3717B}

Fare clic sull&#39;elenco a discesa [!UICONTROL Audience] per modificare il pubblico visualizzato per il report.

Per ulteriori informazioni, consulta [Tipi di pubblico](/help/main/c-target/target.md#concept_A782F8481A5041EBA75103CB26376522).

## Intervallo date {#section_A410A768403C4E01891F95CB357E63ED}

Nella casella Intervallo date viene visualizzato l&#39;intervallo di date corrente del rapporto. Fai clic sull&#39;icona a discesa per visualizzare un calendario che consente di modificare l&#39;intervallo di date del rapporto.

![Calendario](/help/main/c-reports/c-report-settings/assets/date_range-new.png)

Selezionare le nuove date **[!UICONTROL Start]** e **[!UICONTROL End]** per il report. È inoltre possibile utilizzare le caselle di controllo **[!UICONTROL From start of Activity]** e **[!UICONTROL Till end of Activity]**.

Fare clic su **[!UICONTROL Custom Dates]** per selezionare intervalli di date predefiniti: Ultimi 7 giorni, Ultimi 15 giorni o Ultimi 30 giorni. Questi intervalli di date predefiniti sono incrementali. Se la data di inizio è inferiore al numero di giorni scelti, il calendario mostrerà l’intervallo dalla data di inizio, ma il roll on una volta che la data di inizio è più vecchia del numero di giorni scelti con l’aumento della durata dell’attività.

Per i rapporti sono previste le seguenti limitazioni di data:

* La data di inizio del rapporto deve risalire agli ultimi due anni.
* I rapporti sui gruppi di offerte sono limitati a 99 giorni da oggi.
* I rapporti orari sono limitati a 15 giorni.

## Impostazioni  {#section_D99CE462107D45CABE0960F820E1E972}

Per configurare le impostazioni dei rapporti:

1. Fai clic sull’icona a forma di ingranaggio, quindi apporta le modifiche desiderate (come spiegato di seguito).
1. Al termine, fai clic su **[!UICONTROL Save]**.

Nell’illustrazione seguente viene mostrata la finestra di dialogo Impostazioni per un’attività A/B:

![Finestra di dialogo Impostazioni](/help/main/c-reports/c-report-settings/assets/ab_settings_dialog-new.png)

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
>Se l&#39;organizzazione utilizza [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target=_blank} (AEP) per inviare i dati delle metriche a [!DNL Target], l&#39;ambiente nello stream di dati di AEP deve corrispondere all&#39;ambiente nelle impostazioni del report [!DNL Target].


### Ripristina dati rapporto

Reimposta i dati di reporting per rimuovere i dati obsoleti. I visitatori attuali rimangono nell’attività.  Questa opzione è disponibile solo per coloro che dispongono di autorizzazioni [!UICONTROL Approver].

>[!IMPORTANT]
>
>Questa è un’azione permanente e non può essere annullata.

### Escludere i valori estremi

L&#39;opzione [!UICONTROL Exclude Extreme Values] è applicabile solo alle attività con tipi di metrica di ricavi e coinvolgimento. Per ulteriori informazioni, consulta [Esclusione di ordini estremi](/help/main/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA).

## Scarica {#section_77E65C50BAAF4AB79242DB3A8778ADEF}

Fare clic sull&#39;icona **[!UICONTROL Download]** per scaricare i dati del report in formato [!DNL .csv] per l&#39;importazione rapida in Excel, Access o altri programmi di analisi dei dati.

![Icona download](/help/main/c-reports/c-report-settings/assets/download-icon.png)

Per ulteriori informazioni, consulta [Download di dati in un file CSV](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md).

## Aggiorna {#section_E203729F2F314DF3856D2EE67C60B370}

Fare clic sull&#39;icona **[!UICONTROL Refresh]** per aggiornare la tabella e il grafico di un report senza aggiornare l&#39;intera pagina, la configurazione o l&#39;intervallo di date.

## Altre opzioni {#section_AB1B5C695D7045A0A0AC0E2698D2E7DE}

Fare clic sull&#39;icona Altre opzioni (tre puntini di sospensione verticali) per accedere alle opzioni [!UICONTROL Edit Activity] e [!UICONTROL View Experience URLs].

## Opzioni di visualizzazione

Puoi visualizzare il rapporto in vari formati, a seconda del tipo di attività. Seleziona l’opzione desiderata.

![Visualizza icone opzioni](/help/main/c-reports/c-report-settings/assets/view-options.png)

* **Vista tabella**: fare clic sull&#39;icona **[!UICONTROL Table View]** per visualizzare il report come tabella.
* **Visualizzazione grafico**: fare clic sull&#39;icona **[!UICONTROL Graph View]** per visualizzare il report sotto forma di grafico.
* **Segmenti automatizzati**:(disponibile solo per le attività di Automated Personalization (AP) e Targeting automatico (AT).) Fai clic sull&#39;icona **[!UICONTROL Automated Segments] per visualizzare il rapporto [Segmenti automatizzati](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md).
* **Attributi importanti**: (disponibile solo per le attività di Automated Personalization (AP) e Targeting automatico (AT).) Fai clic sull&#39;icona **[!UICONTROL Important Attributes] per visualizzare il [report Attributi importanti](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md).

## Incremento medio, limiti di incremento e intervallo di affidabilità {#section_0D87615B1D3344B3858BA494EEBC16FB}

I rapporti includono diversi punti di dati e rappresentazioni di visualizzazione che consentono di comprendere i limiti di incremento e il livello di affidabilità associati all’attività. Ciò consente di determinare più accuratamente un vincitore.

Per ulteriori informazioni, vedere [Calcoli statistici nei test A/Bn](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

Considera i seguenti aspetti:

* Disponibile solo quando i rapporti vengono visualizzati nella vista Tabella.
* Questa funzionalità non è disponibile per le attività che utilizzano [Analytics come origine per la generazione di rapporti (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

## Contributo posizione {#section_5832F126AC114AE1ABFFF4D9B904393B}

Fai clic sull&#39;icona **[!UICONTROL Location Contribution]** per far sì che il rapporto mostri il contributo in base alla posizione.

## Esperienze {#section_3A450DE1FA7E43F0AAB73165EC3D1C34}

(Disponibile solo quando i rapporti vengono visualizzati nella vista Grafico)

Seleziona o deseleziona le esperienze sul lato sinistro del grafico per visualizzare o nascondere dal grafico le esperienze corrispondenti.

Nell’illustrazione seguente, il rapporto contiene solo le esperienze Default, Mid-East e Total (Predefinito, Medio Oriente, Totale). L’esperienza Asia è nascosta nel grafico.

![Esperienze](/help/main/c-reports/c-report-settings/assets/report_experiences-new.png)

## Media corrente {#section_59066693158C4433B87D07402C2BC6CD}

(Disponibile solo quando i rapporti vengono visualizzati nella vista Grafico)

La &quot;Media corrente&quot; riflette le conversioni cumulative (dall’inizio dell’intervallo di reporting alla data rappresentata sul grafico) divise per i visitatori cumulativi.

Seleziona la vista grafico desiderata:

* Media corrente
* Media corrente - Incremento
* Giornaliero
* Incremento giornaliero

![Rapporto Media corrente](/help/main/c-reports/c-report-settings/assets/report_running_average-new.png)

Il nome dell’elenco a discesa varia a seconda della vista selezionata, ma sarà una delle viste elencate in precedenza.

## Metodologia di conteggio {#section_01B0ED5665C74AE1AE97259800190C3E}

(Disponibile solo quando i rapporti vengono visualizzati nella vista Grafico)

È possibile scegliere la metodologia di conteggio per i grafici del rapporto. Si noti che questo non è supportato per le attività [!UICONTROL Automated Personalization] (AP).

Per accedere all&#39;opzione [!UICONTROL Counting Methodology], durante la visualizzazione di un report in modalità grafico fare clic sull&#39;elenco a discesa **[!UICONTROL My Primary Goal]**, quindi selezionare la metodologia di conteggio.

La metodologia di conteggio sarà la stessa di quella selezionata nella finestra di dialogo [!UICONTROL Settings], sopra descritta.

![Metodologia di conteggio](/help/main/c-reports/c-report-settings/assets/counting_methodology_2-new.png)

Per impostazione predefinita, il grafico viene tracciato in modalità [!UICONTROL Daily].

È possibile modificare la modalità facendo clic sull&#39;elenco a discesa [!UICONTROL Daily] e selezionando un&#39;opzione cumulativa.

![Cumulativo](/help/main/c-reports/c-report-settings/assets/counting_methodology-new.png)

>[!NOTE]
>
>Il nome dell’elenco a discesa varia a seconda della modalità selezionata.

Sono disponibili quattro modalità per le attività di targeting automatico: controllo giornaliero, targeting giornaliero, controllo cumulativo e targeting cumulativo.

L’ordine predefinito in cui viene tracciato il grafico è il seguente:

* **Test A/B (tra cui Allocazione automatica e Automated Personalization)**: ordine di creazione dell&#39;esperienza, in ordine decrescente.
* **Targeting esperienza (XT)**: ordine delle esperienze nell&#39;attività.
* **Test multivariato (MVT)**: alfabetico per nome esperienza.
* **Recommendations**: ordine di creazione dell&#39;esperienza, in ordine decrescente.

Quando lavori con le opzioni di metodologia di conteggio, considera le seguenti avvertenze:

* Per [attività Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md), non è possibile selezionare &quot;Visitatori&quot; come metodologia di conteggio. Il targeting automatico è l’unico tipo di attività i cui dati non possono essere visualizzati per visitatori.
* Per le attività che utilizzano [Analytics come origine per la generazione di rapporti (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md), non è possibile tracciare cumulativamente Visitatore, Visita o Impression.

## Utilizzo di grafici con più di 16 esperienze nell’attività

Se le esperienze di un’attività sono meno di 16, ogni esperienza è rappresentata da un colore diverso nel grafico.

Se le esperienze sono più di 16, nel grafico vengono tracciate le linee colorate delle prime 16. Le restanti esperienze appaiono in grigio nel riquadro Esperienze a sinistra e le linee corrispondenti non sono incluse nel grafico. In un dato momento è possibile visualizzare le linee corrispondenti a 16 esperienze.

Se passi il cursore del mouse sopra una delle esperienze in grigio, sul grafico viene visualizzata temporaneamente la corrispondente linea grigia. Per visualizzare con un colore la linea di un’esperienza grigia, fai clic sul nome di un’esperienza visualizzata a colori per deselezionarla, quindi fai clic sul nome dell’esperienza grigia desiderata per selezionarla.

Ad esempio, la figura seguente mostra il grafico di un’attività con 26 esperienze:

![immagine graph_1](assets/graph_1.png)

Il grafico mostra le linee delle prime 16 esperienze (alcune si sovrappongono, quindi sembra che siano meno di 16). Il punto colorato nel riquadro Esperienze a sinistra indica il colore associato all’esperienza corrispondente.

Se scorri verso il basso nel riquadro Esperienze, puoi notare che i nomi delle esperienze dalla 17 alla 26 sono in grigio, come illustrato nella figura seguente:

![immagine graph_2](assets/graph_2.png)

Se passi il cursore del mouse sopra una delle esperienze in grigio, sul grafico viene visualizzata temporaneamente la corrispondente linea grigia.

Supponiamo che desideri visualizzare la linea dell’esperienza R e nascondere quella linea dell’esperienza P. Fai clic sul nome dell’esperienza P per deselezionarla, quindi fai clic sul nome dell’esperienza R per selezionarla, come illustrato di seguito:

![immagine graph_3](assets/graph_3.png)
