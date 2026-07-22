---
title: Generazione di rapporti
description: Scopri come visualizzare il reporting dei flag di funzione in Flag utilizzando Customer Journey Analytics.
badge: label="Beta" type="Informative"
hide: true
exl-id: edddca99-f263-461b-a16f-b46ee7c15f6c
source-git-commit: 8fffd619232b2cae2f5dd0aa1e0a55183c4be698
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 1%

---

# Generazione di rapporti {#reporting}

I flag consentono la generazione di rapporti tramite **Customer Journey Analytics (CJA)**. Una scheda **Report** è disponibile in ogni flag di funzionalità e pagina dei dettagli del gruppo di funzionalità. Ti consente di visualizzare un rapporto di CJA con ambito specifico per tale flag o gruppo, incorporato direttamente nella pagina.

>[!NOTE]
>
>Report aperti con un intervallo di reporting di **30 giorni** per impostazione predefinita. Puoi regolare l’intervallo dall’intestazione del pannello.

## Prerequisiti {#prerequisites}

Prima di poter visualizzare i rapporti, assicurati che:

1. Il reporting è configurato per l&#39;applicazione. Vedere [Configurazione di CJA per il reporting dei flag di funzionalità](set-up-cja-reporting.md).
1. Il flag di funzione o il gruppo di funzioni è attivo e contiene dati accumulati.

## Visualizzare un rapporto {#view-report}

### Aprire la scheda Report e scegliere una visualizzazione dati {#open-report-tab}

1. Apri un flag di funzionalità o un gruppo di funzionalità e seleziona la scheda **Report**.
1. Viene visualizzata una finestra di dialogo **Seleziona visualizzazione dati**, in cui sono elencate le visualizzazioni dati di CJA disponibili. Il primo è selezionato per impostazione predefinita.
1. Scegliere la visualizzazione dati desiderata e selezionare **Visualizza report**. Seleziona **Annulla** per chiudere la finestra di dialogo senza caricare un report.
1. Il report viene caricato all’interno della scheda, con ambito corrispondente all’ID entità del flag o del gruppo.

![Scheda Report nella pagina dei dettagli di un flag di funzionalità](assets/report-tab.png)

>[!NOTE]
>
>La finestra di dialogo elenca solo le visualizzazioni dati a cui hai accesso nella sandbox corrente. Se non ne è disponibile alcuna, nella finestra di dialogo viene visualizzato un messaggio e **Visualizza report** rimane disabilitato. Verificare le autorizzazioni di visualizzazione dati o cambiare sandbox.

![Finestra di dialogo Seleziona visualizzazione dati](assets/select-dataview.png)

### Visualizzare il rapporto sulle prestazioni {#view-performance-report}

Il dashboard **Flags Overview** incorporato visualizza:

* **Persone totali**, **Partecipazione persone per giorno** e **Partecipazione persone per variante** (ID gruppo di controllo vs. ID variante)
* Una tabella **Panoramica** che elenca ogni variante con il relativo numero di persone e la percentuale di partecipazione

Regola l’intervallo di date dall’intestazione del pannello per tracciare nuovamente per una finestra diversa (30 giorni predefiniti).

![Rapporto prestazioni panoramica contrassegni](assets/performance-report.png)

### Esplora i risultati della sperimentazione {#explore-experimentation-results}

1. Nel pannello **Sperimentazione**, sono preselezionati **Esperimento** (ID entità flag o gruppo) e **Variante controllo**.
1. Aggiungi una **metrica di successo** utilizzando **Aggiungi metrica** e scegli una **metrica di normalizzazione** (**Persone**) predefinita in base al grafico da tracciare.
1. Facoltativamente, abilita **Includi limiti superiori/inferiori dell&#39;affidabilità**.
1. Seleziona **Build** per calcolare **Lift**, **Confidence** e **Conversion rate** per variante per la metrica selezionata.

![Pannello Sperimentazione con selettori esperimento, variante controllo e metrica](assets/experimentation-selection.png)

Per ulteriori dettagli sul calcolo di queste metriche, consulta la [documentazione del pannello Sperimentazione](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-workspace/panels/experimentation).

![Risultati della sperimentazione che mostrano l&#39;incremento, l&#39;affidabilità e il tasso di conversione per variante](assets/experimentation.png)

## Vedi anche {#see-also}

* [Configurare CJA per la generazione di rapporti sui flag di funzione](set-up-cja-reporting.md)
* [Creare il primo flag di funzione](create-your-first-feature-flag.md)
* [Test A/B con flag di funzione](a-b-testing.md)
* [Creare un gruppo di funzioni](create-a-feature-group.md)

<!-- -->
