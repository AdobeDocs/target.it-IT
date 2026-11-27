---
keywords: Consigli;Impostazioni;nome;finalità;priorità;durata;impostazioni di generazione rapporti;altri metadati
description: Scopri come configurare le impostazioni utilizzate per descrivere e controllare un’attività Consigli in Adobe Target.
title: Come Si Configurano Le Impostazioni Delle Attività Consigli?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 77bb14fc-342d-41cd-8084-e21067f277af
TQID: 'https://experienceleague.adobe.com/pfMAvl6MmLCtH3PZfOR4Ve-WFIc3e2iN2Bh-cIzjeC0'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 13%
---
# Impostazioni delle attività Consigli {#recs-activity-settings}

>[!BEGINSHADEBOX]

**In questa pagina:** Informazioni sulle impostazioni che descrivono e controllano un&#39;attività [!DNL Recommendations] in [!DNL Adobe Target].

>[!ENDSHADEBOX]

Le impostazioni delle attività identificano un&#39;attività [!DNL Recommendations], controllano quando e dove viene visualizzata e definiscono come vengono riportati i risultati.

## Nome

Fai clic sull&#39;icona Altre azioni ( ![Icona Altre azioni](/help/main/assets/icons/MoreSmallListVert.svg) ), quindi fai clic su **[!UICONTROL Rinomina]** per assegnare all&#39;attività un nome descrittivo che ne faciliti l&#39;identificazione.

I seguenti caratteri non sono consentiti nel nome di un&#39;attività: `/`, `?`, `#`, `:`, `=`, `+`, `-` e `@`.

Se il nome di un&#39;attività [!DNL Recommendations] esiste già per un&#39;altra attività in [!UICONTROL Recommendations Classic], la nuova attività verrà risincronizzata con un nuovo nome. Il nuovo nome è il nome originale con una marca temporale aggiunta, per renderlo univoco. Viene visualizzato in [!DNL Target Standard/Premium] e [!UICONTROL Recommendations Classic].

## Finalità

(Facoltativo) Descrivi l’obiettivo dell’attività.

## Priorità

Regolare il cursore per impostare il livello di priorità.

La priorità viene utilizzata quando più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.

## Durata

Imposta la durata dell’attività.

L’attività può iniziare quando è attivata o in una data e un’ora specifiche. Allo stesso modo, può terminare quando viene disattivato, o in una data e un’ora specifiche.

Il selettore dell’ora è nel formato 24 ore e la mezzanotte è indicata come 00:00. Il fuso orario è quello configurato nel browser. Per utilizzare un fuso orario diverso, impostare il browser su tale fuso orario e riavviare il browser.

## Impostazioni reporting

Le impostazioni seguenti definiscono il modo in cui vengono segnalati i risultati dell’attività.

* **[!UICONTROL Reporting di Source]:** Specifica la soluzione da cui vengono raccolti i dati: [!DNL Adobe Target], [!DNL Adobe Analytics] o [!DNL Adobe Customer Journey Analytics].

  Se una soluzione di reporting è specificata nelle [impostazioni account](/help/main/administrating-target/reporting.md), viene utilizzata tale soluzione e questa impostazione non è visibile. Al fine di mantenere coerenza dei rapporti, non è possibile modificare l’origine per i rapporti dopo che l’attività è diventata attiva.

  **[!DNL Adobe Analytics]**: vedi [[!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) per le differenze tra le soluzioni di generazione di rapporti e i vantaggi di ciascuna. Per la selezione della suite di rapporti [!DNL Analytics] e del server di tracciamento, vedere [Reporting Source](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reporting-source).

  **[!DNL Adobe Customer Journey Analytics]**: vedere [[!DNL Target] creazione di rapporti in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) per ulteriori informazioni sull&#39;integrazione tra [!DNL Adobe Customer Journey Analytics] e [!DNL Target].

* **[!UICONTROL Metrica per obiettivo]:** Seleziona la metrica di successo che determina se l&#39;attività ha esito positivo.
* **[!UICONTROL Altre metriche]:** Configura ulteriori metriche di successo per i report.
* **[!UICONTROL Tipi di pubblico per i rapporti]:** Definisce i tipi di pubblico che possono essere utilizzati per filtrare i rapporti.

## Altri metadati

Inserisci le note sull’attività.

## Video di formazione: Impostazioni attività (3:02) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video illustra le seguenti impostazioni per le attività:

* Immettere un obiettivo per l&#39;attività.
* Imposta il livello di priorità dell’attività.
* Pianifica gli orari di inizio e fine.
* Aggiungi dei tipi di pubblico per i rapporti per creare filtri per i rapporti.
* Immetti le note per l&#39;attività.

>[!VIDEO](https://video.tv.adobe.com/v/17381)
