---
title: Reporting
description: Scopri come visualizzare il reporting dei flag di funzione in Flag utilizzando Customer Journey Analytics.
hide: true
exl-id: edddca99-f263-461b-a16f-b46ee7c15f6c
source-git-commit: 35fa45d2a5374dcc47a02bb737f28f24847d7fc6
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 1%

---

# Generazione di rapporti {#reporting}

I flag consentono la generazione di rapporti tramite **Customer Journey Analytics (CJA)**. Non è presente alcuna scheda Risultati o Report nella console. Un pulsante **Report** su ogni flag di funzionalità o gruppo di funzionalità apre un dashboard CJA con ambito per l&#39;elemento.

## Prerequisiti {#prerequisites}

Prima di poter visualizzare i rapporti, assicurati che:

1. La creazione di report è impostata per l&#39;applicazione. Vedere [Configurare la creazione di report con Customer Journey Analytics](#setup).
1. Il flag di funzione o il gruppo di funzioni è attivo e contiene dati accumulati.

## Visualizzare un rapporto {#view-report}

Per aprire un report per un flag di funzione o un gruppo di funzioni:

1. Passa al flag di funzione o al gruppo di funzioni nella console.
1. Seleziona **Report**.

Viene visualizzato un dashboard di Customer Journey Analytics con ambito, in cui vengono visualizzati i dati per tale flag o gruppo di funzioni. Il dashboard include:

* **Partecipanti** — Numero totale di utenti qualificati per la funzionalità (combinazione variante + gruppo di controllo)
* **Gruppo di controllo** — Numero di utenti assegnati al gruppo di controllo (utenti che hanno ricevuto l&#39;esperienza predefinita)
* **Suddivisione variante** — Numero cumulativo di utenti iscritti a ogni variante e al gruppo di controllo
* **Iscrizione giornaliera**: grafici a livello di giorno che mostrano l&#39;iscrizione in ogni variante e nel tempo nel gruppo di controllo

## Configurare la generazione di rapporti con Customer Journey Analytics {#setup}

Il reporting richiede un set di dati Customer Journey Analytics connesso all’applicazione Flags. Per abilitare il reporting per la tua applicazione, contatta il supporto dei flag o il tuo rappresentante Adobe.

>[!NOTE]
>
>L’identità passata nella richiesta di funzione non deve essere collegata a un profilo. La valutazione viene eseguita in fase di runtime e l’evento viene inviato a Customer Journey Analytics.

## Vedi anche {#see-also}

* [Creare il primo flag di funzione](create-your-first-feature-flag.md)
* [Test A/B con flag di funzione](a-b-testing.md)
* [Creare un gruppo di funzioni](create-a-feature-group.md)

<!-- -->
