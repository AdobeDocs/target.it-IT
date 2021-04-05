---
description: Scopri l’implementazione legacy di mbox.js di Adobe Target. Esegui la migrazione a Adobe Experience Platform Web SDK (AEP Web SDK) o all’ultima versione di at.js.
title: Quali metodi di pagina utilizzano mbox.js?
feature: at.js
role: Sviluppatori
exl-id: a0f7b956-7855-4165-b34c-33d81a8fac55
translation-type: tm+mt
source-git-commit: 0a685427a047bfc0a2f5e81525b32df70af6d69f
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 88%

---

# Metodi Target per chiamate pagina per le diverse versioni della libreria mbox.js{#target-page-methods-by-mbox-js-library-version}

Il modo in cui Target effettua e risponde alle chiamate dalla pagina dipende dalla versione della libreria di Target che stai utilizzando, dall’eventuale implementazione del servizio ID visitatore di Experience Cloud e dall’esistenza dell’ID del visitatore.

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: A partire dal 31 marzo 2021,  [!DNL Adobe Target] non supporta più la libreria mbox.js . Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto positivo sulle pagine che hanno [!DNL Target] attività in esecuzione servendo il contenuto predefinito.
>
>È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js prima di tale data, per evitare potenziali problemi con i siti. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

>[!NOTE]
>
>Se utilizzi [!DNL at.js], tutte le chiamate vengono effettuate utilizzando JSON. Questa pagina fornisce dettagli sulle versioni della libreria [!DNL mbox.js]. I comportamenti descritti negli scenari riportati di seguito non sono applicabili a [!DNL at.js].

Questa sezione fornisce informazioni su come ogni versione della libreria di [!DNL Target] risponde alla chiamata di [!DNL Target] dalla pagina, in ognuno dei seguenti scenari.

Esistono diversi tipi o endpoint, a seconda dell’implementazione e della versione della libreria. Devi acquisire familiarità con ogni tipo per comprendere come [!DNL Target] risponde alle chiamate in ogni scenario.

| Tipo/Endpoint | Metodo di chiamata | Contenuto della risposta |
|--- |--- |--- |
| Creazione automatica mbox globale, sincrono | document.write per effettuare la chiamata | JavaScript senza document.write() |
| Creazione automatica mbox globale, asincrono | createElement() per aggiungere una chiamata al corpo | JavaScript senza document.write() |
| Standard | document.write per effettuare la chiamata | JavaScript con document.write() |
| AJAX | createElement() per aggiungere una chiamata al corpo | JavaScript senza document.write() |
| json | XMLHTTPrequest() per effettuare la chiamata | restituisce la risposta JSON |

>[!IMPORTANT]
>
>Per tutti i tipi eccetto standard, tutti i codici e le offerte personalizzati devono essere scritti in modo da supportare un ambiente AJAX. Ad esempio, se utilizzi un JavaScript che include `document.write()`, lo script non funzionerà come previsto.

## Nessuna implementazione del servizio ID visitatore {#section_C6F7213FDE4D48E8BBCB1A9A26310FEE}

Se utilizzi [!DNL Target Standard] o [!DNL Premium] con [!DNL mbox.js] e per il tuo account è stata abilitata l’opzione [!UICONTROL Crea mbox globale], viene effettuato il tipo di chiamata e risposta **Creazione automatica mbox globale, sincrono**, a prescindere dalla versione di [!DNL mbox.js].

Se scrivi codice personalizzato anziché utilizzare le azioni disponibili nel [!UICONTROL Compositore esperienza visivo], assicurati che il codice sia appropriato per un ambiente AJAX. Ad esempio, se utilizzi un JavaScript che include `document.write()`, lo script non funzionerà come previsto.

>[!NOTE]
>
>Se una stessa pagina contiene più chiamate mbox AJAX con lo stesso nome mbox ma diversi parametri, queste non funzioneranno correttamente. Viene effettuata solo la prima chiamata.

Se utilizzi “Creazione automatica mbox globale”, ma la pagina contiene anche delle chiamate `mboxCreate`, ad esempio, e implementi [!DNL Target Standard] o [!DNL Premium] su una pagina già utilizzata in un’implementazione precedente, le chiamate mbox globali vengono effettuate utilizzando l’endpoint **Creazione automatica mbox globale, standard** e le chiamate `mboxCreate` vengono effettuate utilizzando l’endpoint **standard**. L’endpoint **standard** utilizza `document.write()` per effettuare la chiamata e rispondere. Questo blocca il caricamento della pagina, incluso il contenuto consegnato nella risposta AJAX, fino a quando non saranno state scaricate tutte le informazioni.

Se utilizzi solo mboxCreate, ad esempio nelle pagine create con [!DNL Target Classic], la pagina funziona come sempre.

| Metodo di creazione | mbox.js v57 | mbox.js v58 | mbox.js v59 | mbox.js v60 |
|---|---|---|---|---|
| Creazione automatica mbox globale | Creazione automatica mbox globale, sincrono | Creazione automatica mbox globale, sincrono | Creazione automatica mbox globale, sincrono | Creazione automatica mbox globale, sincrono |
| mboxCreate | Standard | Standard | Standard | Standard |

## Implementazione del servizio ID visitatore presente, ma nessun ID visitatore impostato {#section_29888A119C7A4753AD287FC845AA63F4}

Se non è stato impostato alcun ID visitatore, non è disponibile un cookie visitatore [!DNL Experience Cloud] per l’utente. La pagina chiama il servizio ID visitatore per ottenere l’ID del visitatore. attende la risposta dal servizio ID che effettua la chiamata a [!DNL Target]Target.

>[!NOTE]
>
>Si consiglia vivamente [!DNL Mbox.js] v58 per garantire che venga restituito l’ID visitatore prima che venga effettuata la chiamata di Target.

Se in questo scenario utilizzi la versione 57 di [!DNL mbox.js], tutto funziona come se non vi fosse alcuna implementazione del servizio ID visitatore, come descritto nello scenario precedente. A partire da [!DNL mbox.js] versione 58, il servizio [!DNL Experience Cloud Visitor ID] restituisce un ID visitatore prima delle chiamate [!DNL Target]. In tal modo, i dati del pubblico condivisi attraverso il servizio principale Profili e Tipi di pubblico sono disponibili per la prima chiamata [!DNL Target] nella sessione del visitatore. Per evitare che appaia momentaneamente il contenuto predefinito prima che venga restituito il contenuto del test, [!DNL Target] nasconde l’elemento `<BODY>` finché non viene restituita la risposta del servizio ID visitatore. Nella versione 58, `display:none` viene utilizzato per nascondere la pagina. Questo crea alcuni problemi con i siti dinamici; a partire dalla versione 59, viene quindi utilizzato `opacity:0` per nascondere il contenuto.

| Metodo di creazione | mbox.js v57 | mbox.js v58 | mbox.js v59 | mbox.js v60 |
|---|---|---|---|---|
| Creazione automatica mbox globale | Creazione automatica mbox globale, sincrono | Creazione automatica mbox globale, asincrono | Creazione automatica mbox globale, asincrono | Creazione automatica mbox globale, asincrono |
| mboxCreate | Standard | AJAX | AJAX | AJAX |

## Implementazione del servizio ID visitatore e presenza dell’ID visitatore  {#section_9CD4AE4C8186425D886398BC3CE6C46D}

Se è presente il cookie ID visitatore, non è necessario che [!DNL Target] effettui una chiamata al servizio ID visitatore. In questo caso, non occorre attendere la risposta dal servizio ID visitatore prima di visualizzare il contenuto. Per le versioni da 57 a 59, viene utilizzato il tipo **Creazione automatica mbox globale, sincrono** e la pagina attende quindi la restituzione della chiamata a [!DNL Target] prima di continuare il caricamento. In questo modo si evita la visualizzazione momentanea del contenuto predefinito. Per v60 viene utilizzato il tipo **mbox globale, asincrono** in modo che [!DNL Target] attenda la risposta del servizio di rinuncia di [!DNL Experience Cloud]. Il servizio di rinuncia fa parte del rilascio Data Co-op dell’autunno 2016. Poiché tutte le chiamate vengono restituite utilizzando AJAX, non utilizzare `document.write()` con la versione 60 di [!DNL mbox.js].

| Metodo di creazione | mbox.js v57 | mbox.js v58 | mbox.js v59 | mbox.js v60 |
|---|---|---|---|---|
| Creazione automatica mbox globale | Creazione automatica mbox globale, sincrono | Creazione automatica mbox globale, sincrono | Creazione automatica mbox globale, sincrono | Creazione automatica mbox globale, asincrono (per supportare lo sviluppo Data Co-op, con rilascio nel 2016) |
| mboxCreate | Standard | Standard | Standard | AJAX |
