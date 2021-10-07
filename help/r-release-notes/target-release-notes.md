---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni saranno incluse nella prossima versione?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: bd7032b915bf1b333fa5cc3cb4825eaa7e4f83fb
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 43%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 6 ottobre 2021**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

>[!IMPORTANT]
>
>**Termine del ciclo di vita di mbox.js**: a partire dal 31 marzo 2021, [!DNL Adobe Target] non supporta più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto sulle pagine che hanno attività [!DNL Target] in esecuzione, che presenteranno il contenuto predefinito.
>
>Per evitare potenziali problemi con i siti, effettua la migrazione alla versione più recente del nuovo [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Target Standard/Premium] 21.10.1 (6 ottobre 2021)

Questa versione include le seguenti nuove funzionalità:

| Funzione | Dettagli |
| --- | --- |
|  Aggiornamento di Audiences UI | Come parte del continuo sforzo del team [!DNL Adobe Target] per migliorare l&#39;esperienza utente per gli utenti [!DNL Target], questa versione aggiorna le pagine [!UICONTROL Audiences] e [!UICONTROL Script di profilo] nell&#39;interfaccia utente [!DNL Target] . Questo aggiornamento unisce e standardizza i pattern di progettazione precedentemente incoerenti, aggiungendo nuovi miglioramenti, ad esempio:<ul><li>Possibilità di selezionare ed eliminare più tipi di pubblico contemporaneamente</li><li>Un [progetto di audience builder aggiornato](/help/c-target/c-audiences/create-audience.md)</li><li>Supporto delle regole di esclusione nel generatore di regole di libreria [!UICONTROL Audience]</li><li>Un nuovo filtro &quot;Audience Source&quot; per consentire un rilevamento più rapido del pubblico</li><li>Opzioni di ricerca e filtro persistenti della sessione</li></ul>Per ulteriori informazioni, consulta [Tipi di pubblico](/help/c-target/target.md).<br>**Nota**: La nuova interfaccia utente   Audiences e  [!UICONTROL Script ] di profilo verrà implementata in tutte le aree geografiche la prossima settimana. |
| [!UICONTROL Aggiornamento ] dell&#39;interfaccia utente Script di profilo | Anche la libreria [!UICONTROL Script di profilo] è stata aggiornata e include un&#39;interfaccia aggiornata insieme a diversi aggiornamenti di produttività:<ul><li>Possibilità di selezionare ed eliminare contemporaneamente più script di profilo</li><li>Un nuovo editor di codice per gli script di profilo</li><li>Evidenziazione della sintassi e controllo degli errori all&#39;interno dell&#39;editor di codice</li><li>Parametri dei token (mbox o profilo) completi automaticamente tramite scelte rapide da tastiera</li></ul>Per ulteriori informazioni, consulta [Profili dei visitatori](/help/c-target/c-visitor-profile/visitor-profile.md).<br>**Nota**: La nuova interfaccia utente   Audiences e  [!UICONTROL Script ] di profilo verrà implementata in tutte le aree geografiche la prossima settimana. |
| ![Badge ](/help/assets/premium.png) PremiumCriteri di Recommendations creazione e modifica | Il flusso di lavoro [!UICONTROL Recommendations Criteria] per la creazione e la modifica dei criteri è stato semplificato per semplificare la scelta dell&#39;algoritmo e delle impostazioni consigliate per raggiungere gli obiettivi.<br>Per ulteriori informazioni, consulta  [Creare criteri](/help/c-recommendations/c-algorithms/create-new-algorithm.md). |
| ![Miglioramenti ](/help/assets/premium.png) della frequenza di aggiornamento degli algoritmi e dell&#39;intervallo di lookback di Premium | È ora possibile eseguire gli algoritmi &quot;Più visualizzato&quot; e &quot;Più venduti&quot; con un intervallo di lookback di sei ore per acquisire il contenuto con tendenze più recenti. Quando l’intervallo di lookback di sei ore è selezionato, i risultati delle raccomandazioni vengono aggiornati ogni 3-6 ore nel corso della giornata.<br>Per ulteriori informazioni, consulta  [Origine dati ](/help/c-recommendations/c-algorithms/create-new-algorithm.md#data-source) in  *Creare criteri*. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
