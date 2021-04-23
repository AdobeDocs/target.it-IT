---
keywords: document.write;target;implementare;implementare target;dtm;gestione tag dinamica;at.js;mbox.js;target.js;mbox;adobe experience platform web skd;aep web sdk;web sdk
description: Implementa le librerie Adobe [!DNL Target] by referencing the [!DNL Target] (at.js o mbox.js) nelle tue pagine web.
title: 'Comprendere le librerie JavaScript di  [!DNL Target] '
feature: Implementazione
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 23%

---


# Comprendere le librerie JavaScript di [!DNL Target]

Implementa [!DNL Adobe Target] facendo riferimento alle librerie [!DNL Adobe Target] (Adobe Experience Platform Web SDK o at.js) nelle tue pagine web.

>[!NOTE]
>
>La libreria mbox.js non verrà più sviluppata. Tutti i clienti devono migrare da mbox.js a at.js o a [!UICONTROL Adobe Experience Platform Web SDK] prima del 31 marzo 2021. Per ulteriori informazioni, consulta [Migrare a at.js da mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA) o [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md).

## Differenze tra le [!DNL Target] librerie JavaScript {#section_40117C78C2F84FECAC4F1BA40CC4F171}

La tabella seguente spiega le differenze tra le librerie JavaScript [!DNL Target]:

| Riferimento alla libreria | Descrizione |
|--- |--- |
| Adobe Experience Platform Web SDK | Il [!UICONTROL Adobe Experience Platform Web SDK] consente di interagire con i vari servizi presenti in [!DNL Experience Cloud] (incluso [!DNL Target]) tramite Adobe Experience Edge Network. Se scegli di eseguire la migrazione a [!DNL Adobe Experience Platform Web SDK], consulta [Cos’è Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) nella *Guida all’SDK per web*. |
| at.js | at.js sostituisce mbox.js per le implementazioni di [!DNL [!DNL Target]] .<br>Tra gli altri vantaggi, at.js migliora i tempi di caricamento delle pagine per le implementazioni web, migliora la sicurezza, evita gli avvisi document.write in Google Chrome e fornisce migliori opzioni di implementazione per le applicazioni a pagina singola.<br>Per ulteriori informazioni, consulta [Implementazione di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md). |

## Impatto di at.js sul tempo di caricamento della pagina {#section_16630CD0FF0A498EB596A51381366A5A}

Molti clienti e consulenti vogliono conoscere l&#39;impatto di [!DNL at.js] sul tempo di caricamento delle pagine, soprattutto nel contesto di utenti nuovi rispetto a utenti di ritorno. Sfortunatamente, è difficile misurare e fornire numeri concreti per quanto riguarda il modo in cui [!DNL at.js] influisce sul tempo di caricamento delle pagine a causa dell&#39;implementazione di ciascun cliente.

Tuttavia, se nella pagina è presente l’API visitatore, [!DNL Target] può comprendere meglio in che modo [!DNL at.js] influisce sul tempo di caricamento delle pagine.

>[!NOTE]
>
>Le API dei visitatori e [!DNL at.js] hanno un impatto sul tempo di caricamento della pagina solo quando utilizzi la mbox globale (a causa della tecnica di celamento del corpo). Le mbox regionali non sono influenzate dall&#39;integrazione delle API dei visitatori.

Le sezioni seguenti illustrano la sequenza di azioni per i visitatori nuovi e per i visitatori di ritorno:

### Visitatori nuovi

1. L&#39;API dei visitatori viene caricata, analizzata ed eseguita.
1. at.js viene caricato, analizzato ed eseguito.
1. Se la creazione automatica mbox globale è abilitata, la libreria JavaScript [!DNL Target]:

   * Crea un&#39;istanza dell&#39;oggetto Visitatore.
   * La libreria [!DNL Target] cerca di recuperare i dati [!UICONTROL ID visitatore Experience Cloud].
   * Per un nuovo visitatore, l’API visitatore genera una richiesta cross-domain a `demdex.net`.
   * Dopo aver recuperato i dati [!UICONTROL ID visitatore di Experience Cloud], viene avviata una richiesta a Target.

### Visitatori di ritorno

1. L&#39;API dei visitatori viene caricata, analizzata ed eseguita.
1. at.js viene caricato, analizzato ed eseguito.
1. Se la creazione automatica mbox globale è abilitata, la libreria JavaScript [!DNL Target]:

   * Crea un&#39;istanza dell&#39;oggetto Visitatore.
   * La libreria [!DNL Target] cerca di recuperare i dati [!UICONTROL ID visitatore Experience Cloud].
   * L&#39;API dei visitatori recupera i dati dai cookie.
   * Dopo il recupero dei dati di [!UICONTROL ID visitatore di Experience Cloud], viene avviata una richiesta a [!DNL Target].

>[!NOTE]
>
>Per i nuovi visitatori, quando è presente l&#39;API visitatore, [!DNL Target] si connette più volte per assicurarsi che le richieste [!DNL Target] contengano i dati [!UICONTROL ID visitatore Experience Cloud]. Per i visitatori di ritorno, [!DNL Target] passa il cursore solo su [!DNL Target] per recuperare il contenuto personalizzato.
