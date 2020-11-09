---
keywords: Target Standard;at.js;implementation
description: La libreria at.js è una nuova libreria di implementazione per Adobe Target progettata sia per le implementazioni web tipiche che per le applicazioni a pagina singola.
title: Migrare da mbox.js a at.js
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 96%

---


# Migrare da mbox.js a at.js{#migrate-from-mbox-js-to-at-js}

La libreria at.js è una nuova libreria di implementazione per [!DNL Adobe Target] progettata sia per le implementazioni web tipiche che per le applicazioni a pagina singola.

Ad esempio, [!DNL at.js] migliora i tempi di caricamento delle pagine per le implementazioni web e fornisce migliori opzioni di implementazione per le applicazioni a pagina singola.

[!DNL at.js] sostituisce [!DNL mbox.js] per le implementazioni di [!DNL Target]. La libreria [!DNL at.js] include anche i componenti inclusi in [!DNL target.js], quindi cessano le chiamate a [!DNL target.js].

>[!NOTE]
>
>Adobe Experience Manager (AEM) 6.2 con FP-11577 (o versioni successive) supporta le implementazioni di at.js con l’integrazione di Adobe Target Cloud Services. Per ulteriori informazioni, consulta [Pacchetti di funzionalità](https://docs.adobe.com/docs/en/aem/6-2/release-notes/feature-packs.html) e [Integrazione con Adobe Target](https://docs.adobe.com/docs/en/aem/6-2/administer/integration/marketing-cloud/target.html) nella documentazione di *Adobe Experience Manager 6.2*.

## Vantaggi di at.js {#benefits}

Nella tabella seguente vengono illustrate le differenze tra le due librerie:

| Riferimento alla libreria | Descrizione |
|--- |--- |
| at.js | at.js sostituisce mbox.js per le implementazioni di [!DNL Target].<br>Tra gli altri vantaggi, at.js migliora i tempi di caricamento delle pagine per le implementazioni web, migliora la sicurezza, evita gli avvisi document.write in Google Chrome e fornisce migliori opzioni di implementazione per le applicazioni a pagina singola.<br>Per ulteriori informazioni, consulta [Implementazione di at.js](#implement). |
| mbox.js | Prima di [!DNL Target] 16.3.1 (marzo 2016), [!DNL Target] richiedeva una chiamata a mbox.js per creare la mbox globale necessaria ad [!DNL Target] per fornire attività e tracciare i clic e la maggior parte delle metriche di successo. Questo file contiene le librerie necessarie per tutte le attività. Non è necessario mantenere diverse versioni del file specifiche per le singole attività.<br>Se sulla tua pagina sono già presenti wrapping mbox derivanti da un’implementazione precedente di [!DNL Target], puoi riutilizzarle nella nuova interfaccia. Il file mbox.js aggiornato rimane necessario, ma queste mbox possono essere selezionate per le attività e modificate utilizzando il Compositore esperienza visivo.<br>[!DNL Target] Standard e Premium aggiornano e integrano mbox.js con un riferimento a un file target.js. Il file target.js è in hosting presso Adobe. Il file Target.js consente di modificare il contenuto in qualsiasi pagina utilizzando il Compositore esperienza visivo, anche se la pagina non contiene mbox predefinite. Devi fare riferimento a questo file su ogni pagina del sito.<br>Per ulteriori informazioni, consulta [Implementazione di mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md).<br>**Importante**: la libreria mbox.js è ancora supportata, ma non ci saranno aggiornamenti di funzionalità. Tutti i clienti devono migrare a at.js. Per ulteriori informazioni, consulta [Migrazione a at.js da mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md) |

## Implementare at.js {#implement}

Per utilizzare [!DNL at.js], sostituisci il riferimento [!DNL mbox.js] nelle pagine in cui desideri implementarlo. Non puoi utilizzare [!DNL mbox.js] e [!DNL at.js] in un’unica pagina. Tuttavia, puoi utilizzarli su pagine diverse del sito.

La libreria [!DNL at.js] funziona per le implementazioni esistenti utilizzando le funzioni `mboxCreate()`, `mboxDefine()` e `mboxUpdate()` e supporta nuove funzionalità incentrate sulle implementazioni basate su applicazioni a pagina singola.

Puoi utilizzare [!DNL at.js] ovunque ora utilizzi [!DNL mbox.js].

La libreria [!DNL at.js] offre diversi miglioramenti rispetto alla libreria [!DNL mbox.js], tra cui:

* Comunicazione completamente asincrona tramite Ajax cross domain

   >[!IMPORTANT]
   >
   >Sebbene [!DNL at.js] comunichi in modo asincrono con i server di [!DNL Target], il file [!DNL at.js] deve essere caricato in maniera sincrona nella sezione `<head>` della tua pagina. Possibilmente deve essere uno dei primi script a essere caricati. Una volta caricato, [!DNL at.js] esegue le chiamate mbox in modo asincrono tramite `XMLHttpRequest` e lascia continuare il rendering della pagina.

* Non si verificano più blocchi dovuti a chiamate
* Non utilizza `document.write()`
* I codici JavaScript non vengono eseguiti immediatamente nelle risposte di [!DNL Target]
* Gestione migliore del timeout e degli errori

   * Personalizzazione del [timeout](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) per chiamata
   * Nessun ricaricamento in caso di timeout

* Funzioni progettate specificamente per applicazioni a pagina singola/framework MVC

## Video di formazione: at. js - Vantaggi e best practice per l’implementazione ![badge Panoramica](/help/assets/overview.png)

Questo video è una registrazione di “ [Office Hours](/help/cmp-resources-and-contact-information.md)”, un’iniziativa condotta dal team di assistenza clienti Adobe.

* Funzionamento della libreria at.js
* Vantaggi di at.js rispetto mbox.js
* Gestione at.js della visualizzazione momentanea di altri contenuti
* Gestione degli errori in at.js
* Metodi di debug
* Problemi noti e percorsi futuri

>[!VIDEO](https://video.tv.adobe.com/v/22223/)
