---
keywords: Target Standard;at.js;implementazione
description: Scopri come migrare a at.js, la nuova libreria di implementazione per Adobe [!DNL Target] progettata sia per le tipiche implementazioni web che per le applicazioni a pagina singola (SPA).
title: Come si effettua la migrazione da mbox.js a at.js?
feature: at.js
role: Developer
exl-id: 1d95faeb-7caa-44d6-b637-a06db393e50e
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 91%

---

# Migrare da mbox.js a at.js

La libreria at.js è una nuova libreria di implementazione per [!DNL Adobe Target] progettata sia per le implementazioni web tipiche che per le applicazioni a pagina singola.

Ad esempio, [!DNL at.js] migliora i tempi di caricamento delle pagine per le implementazioni web e fornisce migliori opzioni di implementazione per le applicazioni a pagina singola.

[!DNL at.js] sostituisce [!DNL mbox.js] per le implementazioni di [!DNL Target]. La libreria [!DNL at.js] include anche i componenti inclusi in [!DNL target.js], quindi cessano le chiamate a [!DNL target.js].

>[!NOTE]
>
>Adobe Experience Manager (AEM) 6.2 con FP-11577 (o versioni successive) supporta le implementazioni di at.js con l’integrazione di Adobe Target Cloud Services. Per ulteriori informazioni, consulta [Pacchetti di funzionalità](https://experienceleague.adobe.com/docs/?lang=it#experience-cloud) e [Integrazione con Adobe Target](https://docs.adobe.com/docs/en/aem/6-2/administer/integration/marketing-cloud/target.html) nella documentazione di *Adobe Experience Manager 6.2*.

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

## Video di formazione: at. js - Vantaggi e best practice per l’implementazione ![Icona Panoramica](/help/assets/overview.png)

Questo video è una registrazione di “ [Office Hours](/help/cmp-resources-and-contact-information.md)”, un’iniziativa condotta dal team di assistenza clienti Adobe.

* Funzionamento della libreria at.js
* Vantaggi di at.js rispetto mbox.js
* Gestione at.js della visualizzazione momentanea di altri contenuti
* Gestione degli errori in at.js
* Metodi di debug
* Problemi noti e percorsi futuri

>[!VIDEO](https://video.tv.adobe.com/v/22223/)
