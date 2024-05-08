---
keywords: Consigli;Impostazioni;nome;finalità;priorità;durata;impostazioni di generazione rapporti;altri metadati
description: Scopri come configurare le impostazioni utilizzate per descrivere e controllare un’attività Recommendations in Adobe Target.
title: Come si configurano le impostazioni delle attività di Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 77bb14fc-342d-41cd-8084-e21067f277af
source-git-commit: af8291a27e62a588046f66f20f8d3a47c8af0a18
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 48%

---

# Impostazioni delle attività di Consigli

Informazioni sulle impostazioni utilizzabili per descrivere e controllare un [!UICONTROL Recommendations] attività in [!DNL Adobe Target].

![Pagina Obiettivi e impostazioni della funzione Consigli](/help/main/c-recommendations/t-create-recs-activity/assets/recs-settings.png)

Le sezioni seguenti descrivono le impostazioni disponibili per un [!UICONTROL Recommendations] attività.

## Nome

Specifica un nome descrittivo che aiuterà te e il tuo team a identificare l’attività.

I seguenti caratteri non sono consentiti nel nome di un’attività:

`/`
`?`
`#`
`:`
`=`
`+`
`-`
`@`

Se si specifica un [!UICONTROL Recommendations] nome di attività già esistente per un’altra attività in [!UICONTROL Recommendations Classic], la nuova attività viene risincronizzata con un nuovo nome. Il nuovo nome è composto dal nome originale più una marca temporale per renderlo univoco. Questo nuovo nome viene visualizzato in entrambi [!DNL Target Standard/Premium] e [!UICONTROL Recommendations Classic].

## Finalità

(Facoltativo) Descrivi l’obiettivo dell’attività.

## Priorità

Sposta il cursore per determinare il livello di priorità.

La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.

## Durata

Imposta la durata dell’attività.

L’attività può iniziare dopo l’attivazione, oppure è possibile impostare una data e un’ora specifiche. Analogamente, l’attività può terminare quando viene disattivata, oppure è possibile impostare una data e un’ora specifiche. Il selettore dell’ora è nel formato 24 ore e la mezzanotte è indicata come 00:00. Il fuso orario è impostato sul fuso configurato nel browser. Per utilizzare un fuso orario diverso, imposta il browser su un altro fuso orario e riavvia il browser.

## Impostazioni reporting

* **Origine per la generazione di rapporti:** Specifica da quali dati della soluzione vengono raccolti:

   * [!DNL Adobe Target]
   * [!DNL Adobe Analytics]
   * [!DNL Adobe Customer Journey Analytics]

  Se una soluzione di reporting è specificata nel [impostazioni account](/help/main/administrating-target/reporting.md), viene utilizzata la soluzione specificata e questa impostazione non è visibile.

  Al fine di mantenere coerenza dei rapporti, non è possibile modificare l’origine per i rapporti una volta che l’attività è diventata attiva.

  **[!DNL Adobe Analytics]**: vedi [[!DNL Adobe Analytics] come origine di reporting per [!DNL Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) per scoprire le differenze tra le soluzioni di reporting e i vantaggi di ciascuna.

  Durante la selezione [!DNL Analytics] come origine di reporting per [!DNL Target] (A4T), seleziona un’ [!DNL Analytics] suite di rapporti da ricevere [!DNL Target] dati attività. A questo scopo, scegli innanzitutto una delle seguenti opzioni [!DNL Analytics] aziende a cui è associato il tuo account, quindi seleziona la suite di rapporti appropriata per l’attività. Solo le suite di rapporti per le quali è stato eseguito il provisioning [!DNL Target] sono disponibili per la selezione. Se non trovi la suite di rapporti desiderata, disconnettiti e accedi di nuovo al [!DNL Adobe Experience Cloud] per riprovare. Se la suite di rapporti non è ancora presente nell’elenco, contatta [Assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

  [!DNL Analytics for Target] (A4T) richiede un server di tracciamento per riportare correttamente i risultati. Un server di tracciamento predefinito viene visualizzato in [!UICONTROL Tracking Server] campo. Se utilizzi più server di tracciamento, assicurati di includere in questo campo il server di tracciamento corretto. Consulta [Utilizzo di un server di tracciamento di Analytics](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) per ulteriori informazioni.

  **[!DNL Adobe Customer Journey Analytics]**: vedi [[!DNL Target] creazione di rapporti in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) per ulteriori informazioni sull’integrazione tra [!DNL Adobe Customer Journey Analytics] e [!DNL Target].

* **Metrica per obiettivo**: seleziona la metrica di successo che determina il successo dell’attività.
* **Altre metriche:** Configura ulteriori metriche di successo da utilizzare nei rapporti.
* **Tipi di pubblico per i rapporti:** Definisci i tipi di pubblico che possono essere utilizzati per filtrare i rapporti.

## Altri metadati

Inserisci delle note sull’attività.

## Video di formazione: Impostazioni attività (3:02) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video include informazioni sulle impostazioni delle attività.

* Inserire una finalità per l’attività
* Impostare il livello di priorità delle attività
* Orari di inizio e fine dell’attività
* Aggiungere tipi di pubblico da usare come filtri nella generazione di rapporti
* Inserire delle note per le attività

>[!VIDEO](https://video.tv.adobe.com/v/17381)
