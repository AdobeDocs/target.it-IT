---
keywords: Consigli;Impostazioni;nome;finalità;priorità;durata;impostazioni di generazione rapporti;altri metadati
description: Scopri come configurare le impostazioni utilizzate per descrivere e controllare un’attività Consigli in Adobe Target.
title: Come Si Configurano Le Impostazioni Delle Attività Consigli?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 77bb14fc-342d-41cd-8084-e21067f277af
source-git-commit: b7c7e8d85f7f39024ed5e57177e5c9f628460e9c
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 43%

---

# Impostazioni delle attività di Consigli

Informazioni sulle impostazioni utilizzabili per descrivere e controllare un&#39;attività [!UICONTROL Recommendations] in [!DNL Adobe Target].

Nelle sezioni seguenti vengono descritte le impostazioni disponibili per un&#39;attività [!UICONTROL Recommendations].

## Nome

Fai clic sull&#39;icona Altre azioni ( ![Icona Altre azioni](/help/main/assets/icons/MoreSmallListVert.svg) ), quindi fai clic su **[!UICONTROL Rename]** per fornire un nome descrittivo che possa aiutare te e il tuo team a identificare l&#39;attività.

I seguenti caratteri non sono consentiti nel nome di un’attività:

`/`
`?`
`#`
`:`
`=`
`+`
`-`
`@`

Se si specifica un nome di attività [!UICONTROL Recommendations] già esistente per un&#39;altra attività in [!UICONTROL Recommendations Classic], la nuova attività verrà risincronizzata con un nuovo nome. Il nuovo nome è composto dal nome originale più una marca temporale per renderlo univoco. Questo nuovo nome viene visualizzato in entrambi [!DNL Target Standard/Premium] e [!UICONTROL Recommendations Classic].

## Finalità

(Facoltativo) Descrivi l’obiettivo dell’attività.

## Priorità

Sposta il cursore per determinare il livello di priorità.

La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.

## Durata

Imposta la durata dell’attività.

L’attività può iniziare dopo l’attivazione, oppure è possibile impostare una data e un’ora specifiche. Analogamente, l’attività può terminare quando viene disattivata, oppure è possibile impostare una data e un’ora specifiche. Il selettore dell&#39;ora utilizza un orologio di 24 ore, dove 00:00 corrisponde a mezzanotte. Il fuso orario è impostato sul fuso configurato nel browser. Per utilizzare un fuso orario diverso, imposta il browser su un altro fuso orario e riavvia il browser.

## Impostazioni reporting

* **Source di reporting:** Specificare i dati della soluzione da cui vengono raccolti:

   * [!DNL Adobe Target]
   * [!DNL Adobe Analytics]
   * [!DNL Adobe Customer Journey Analytics]

  Se una soluzione di reporting è specificata nelle [impostazioni account](/help/main/administrating-target/reporting.md), viene utilizzata la soluzione specificata e questa impostazione non è visibile.

  Al fine di mantenere coerenza dei rapporti, non è possibile modificare l’origine per i rapporti una volta che l’attività è diventata attiva.

  **[!DNL Adobe Analytics]**: consulta [[!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) per informazioni sulle differenze tra le soluzioni per la generazione di rapporti e i vantaggi di ciascuna.

  Quando selezioni [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target] (A4T), selezioni una suite di rapporti [!DNL Analytics] per ricevere i dati dell&#39;attività [!DNL Target]. Scegli innanzitutto una delle [!DNL Analytics] società a cui è associato il tuo account, quindi seleziona la suite di rapporti appropriata per l&#39;attività. È possibile selezionare solo le suite di rapporti predisposte per la connessione a [!DNL Target]. Se la suite di rapporti prevista non è visibile, disconnettersi e accedere nuovamente a [!DNL Adobe Experience Cloud] per riprovare. Se la suite di rapporti non è ancora presente nell&#39;elenco, contatta l&#39;[Assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

  [!DNL Analytics for Target] (A4T) richiede un server di tracciamento per riportare correttamente i risultati. Nel campo [!UICONTROL Tracking Server] viene visualizzato un server di tracciamento predefinito. Se utilizzi più server di tracciamento, assicurati di includere in questo campo il server di tracciamento corretto. Per ulteriori informazioni, vedere [Utilizzo di un server di tracciamento di Analytics](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

  **[!DNL Adobe Customer Journey Analytics]**: vedere [[!DNL Target] creazione di rapporti in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) per ulteriori informazioni sull&#39;integrazione tra [!DNL Adobe Customer Journey Analytics] e [!DNL Target].

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
