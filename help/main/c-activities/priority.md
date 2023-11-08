---
keywords: impostazioni;priorità
description: Scopri come [!DNL Adobe Target] determina in modo diverso l’attività o le attività da consegnare a una pagina, a seconda di quale [!DNL Target] e quale funzione di creazione di attività stai utilizzando.
title: In che modo [!DNL Target] Assegnare priorità ad attività diverse?
feature: Activities
exl-id: c32f1699-e564-40dd-8ff1-7c75a672c6ef
source-git-commit: 18765a82b5dca94654a412e2012a3f6c1a7b5128
workflow-type: tm+mt
source-wordcount: '1105'
ht-degree: 40%

---

# Priorità

[!DNL Adobe Target] determina in modo diverso l’attività o le attività da consegnare a una pagina, a seconda di quale [!DNL Target] e quale funzione di creazione attività ([[!UICONTROL Compositore esperienza visivo]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) o [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md)) in uso.

## [!DNL Target Standard/Premium] [!UICONTROL Compositore esperienza visivo] solo o [!UICONTROL Compositore esperienza basato su moduli] utilizzo di un [!DNL Target] solo richiesta {#section_4A0A317DFED345649B58B0CB5B410C8B}

Se l’azienda utilizza [!DNL Target Standard/Premium] e [!UICONTROL Compositore esperienza visivo] in via esclusiva, il contenuto da più attività può essere restituito per la stessa chiamata. Le attività vengono consegnate in base al seguente flusso decisionale:

1. Il [!DNL Target] la chiamata al server arriva a [!DNL Target] con informazioni sull’URL.
1. [!DNL Target] richiama ogni attività in esecuzione su tale URL.
1. [!DNL Target] tenta di stabilire la corrispondenza tra il visitatore e le attività.

   Se il visitatore si trova già in un [!UICONTROL Test A/B] o [!UICONTROL Test multivariato] attività, corrispondono a tale attività fino a quando non vengono convertiti. Se si trovavano precedentemente in un [!UICONTROL Targeting esperienza] attività, devono corrispondere di nuovo in esso. Se soddisfa le regole del pubblico, allora il visitatore rientra in tali attività e in esperienze specifiche.

1. Alla pagina vengono restituiti i contenuti per tutte le attività e le esperienze a cui corrisponde il visitatore.
1. Se i contenuti di ogni attività fanno riferimento a diversi [selettori CSS](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337), vengono visualizzati tutti i contenuti.

   In caso di sovrapposizione o di selettore CSS duplicato, viene visualizzato il contenuto dell’attività con la priorità più alta. I risultati di tutte le attività eseguite sulla pagina vengono conteggiati e si riflettono nei rapporti.

   >[!IMPORTANT]
   >
   >[!DNL Target] restituisce i contenuti per tutte le attività sulla pagina, a partire da quello con priorità più bassa, che viene poi sovrascritto da ogni attività, dalla priorità più bassa a quella più alta. Di solito, questo determina la visualizzazione del contenuto con la priorità più elevata. Tuttavia, se un’attività con priorità inferiore modifica la struttura del DOM per la pagina, è possibile che l’attività con priorità più alta non riconosca la struttura della pagina, per cui viene visualizzato il contenuto con priorità inferiore. I risultati di tutte le attività eseguite sulla pagina vengono conteggiati e si riflettono nei rapporti.

1. Se più attività condividono il livello di priorità, esistono due livelli di priorità:

   * Se il targeting per il pubblico è stato impostato per una sola attività, viene visualizzata tale attività.
   * Se tutti o nessuno ha un targeting, viene visualizzata l’attività approvata per prima.

## [!DNL Target Standard/Premium] [!UICONTROL Compositore esperienza basato su moduli] e [!DNL Target Standard/Premium] [!UICONTROL Compositore esperienza visivo] {#section_4620253E1CE942DD830724C7822B175F}

>[!NOTE]
>
>Queste informazioni si applicano anche alle campagne in esecuzione che sono state create in [!DNL Target Classic].

Se la tua azienda utilizza [!UICONTROL Compositore esperienza basato su moduli] in [!DNL Target Standard/Premium] e [!DNL Target Standard/Premium] [!UICONTROL Compositore esperienza visivo], quindi contenuto da più [!UICONTROL Compositore esperienza visivo] Le attività possono essere consegnate, ma solo una dal flusso di lavoro basato su moduli. Le attività vengono consegnate in base al seguente flusso decisionale:

1. [!DNL Target] la chiamata al server arriva a [!DNL Target] con informazioni su [!DNL Target] richiesta e URL.
1. [!DNL Target Classic] e [!DNL Target Standard/Premium] richiamare ogni attività in esecuzione in tale [!DNL Target] richiesta.
1. [!DNL Target] tenta di stabilire la corrispondenza tra il visitatore e le attività.

   Se il visitatore si trova già in un [!UICONTROL Test A/B] o [!UICONTROL Test multivariato] attività, corrispondono a quel test fino a quando non vengono convertiti. Se si trovavano precedentemente in un [!UICONTROL Targeting esperienza] attività, devono corrispondere di nuovo in esso. Se soddisfa le regole del pubblico, allora il visitatore rientra in tali attività e in esperienze specifiche.

1. Se un’attività basata su moduli ha la priorità più alta, il contenuto dell’attività viene restituito insieme a tutto il contenuto dell’attività corrispondente da [!UICONTROL Compositore esperienza visivo] attività.
1. Se un [!UICONTROL Compositore esperienza visivo] attività è la priorità più alta, quindi il contenuto da tutte le corrispondenze [!UICONTROL Compositore esperienza visivo] vengono restituite attività, ma non [!DNL Target Classic] o viene restituito il contenuto dell’attività basata su moduli.

   I risultati di tutte le attività eseguite sulla pagina vengono conteggiati e si riflettono nei rapporti.

**Esempio**

In presenza di due attività, una con targeting per la parola chiave di ricerca del brand &quot;Nike&quot; e la seconda con targeting per la parola chiave non del brand &quot;sneakers&quot;, vengono controllate le priorità di entrambe le attività. Se l’attività Nike ha una priorità più alta, viene visualizzato tale contenuto. Se l’attività sneaker ha la priorità più alta, viene visualizzato il suo contenuto.

Se entrambe le attività di targeting hanno la stessa priorità, viene visualizzata l’attività che è stata vista più di recente. Se si tratta di un visitatore sulla pagina in questione, viene visualizzata l’attività attivata più di recente.

## [!DNL Target Standard/Premium] [!UICONTROL Compositore esperienza basato su moduli] con non globale [!DNL Target] richieste {#section_C3F5F09B0B2D4EF795C5929D5C426A8C}

>[!NOTE]
>
>Queste informazioni si applicano anche alle attività in esecuzione create in [!DNL Target Classic].

Se l’azienda utilizza [!DNL Target] richieste diverse da quelle globali [!DNL Target] nel compositore basato su modulo, è possibile restituire il contenuto di una sola attività per chiamata. Le attività vengono consegnate in base al seguente flusso decisionale:

1. Il [!DNL Target] la chiamata al server arriva a [!DNL Target] con informazioni su [!DNL Target] richiesta e URL.
1. [!DNL Target] richiama ogni attività in esecuzione in che [!DNL Target] richiesta.
1. [!DNL Target] tenta di associare il visitatore all’attività con priorità più elevata.

   Se il visitatore si trova già in un [!UICONTROL Test A/B] o [!UICONTROL Test multivariato] attività, corrispondono a tale attività fino a quando non vengono convertiti. Se si trovavano precedentemente in un [!UICONTROL Targeting esperienza] attività, devono corrispondere di nuovo in esso. Se soddisfa le regole del pubblico, allora il visitatore rientra in tali attività e in esperienze specifiche.

1. Se più attività condividono il livello di priorità, esistono due livelli di priorità:

   * Se il targeting per il pubblico è stato impostato per una sola attività, viene visualizzata tale attività.
   * Se tutti o nessuno ha un targeting, viene visualizzata l’attività approvata per prima.

## Esempi {#section_F6A788AAC3884A2FA03E47F0557A1213}

>[!NOTE]
>
>I valori di priorità variano a seconda delle impostazioni. Puoi utilizzare le impostazioni legacy di [!UICONTROL Basso], [!UICONTROL Medio], o [!UICONTROL Alta], oppure puoi abilitare le priorità dettagliate da 0 a 999. Per ulteriori informazioni, consulta [Impostazioni delle attività](/help/main/c-activities/activity-settings.md#task_C6B2FF8374724933BE79A83549B9CD02).

**Due [!DNL Target Classic] le attività utilizzano dati non globali [!DNL Target] richieste**

* Attività 1: homePageHero, offer1, priorità alta
* Attività 2: homePageHero, offer2, priorità bassa

Risposta: offer1

**Due attività utilizzano solo offerte create nel Compositore esperienza visivo per diversi selettori**

* Attività 1: target-global-mbox, selector1, visualExpCompOffer1, priorità bassa
* Attività 2: target-global-mbox, selector2, visualExpCompOffer2, priorità alta

Risposta: visualExpCompOffer1, visualExpCompOffer2

**Due attività utilizzano solo offerte create nel Compositore esperienza visivo per lo stesso selettore**

* Attività 1: target-global-mbox, selector1, visualExpCompOffer1, priorità bassa
* Attività 2: target-global-mbox, selector1, visualExpCompOffer2, priorità alta

Risposta: visualExpCompOffer1, visualExpCompOffer2

>[!NOTE]
>
>Questa è la stessa risposta del secondo caso d’uso precedente perché [!DNL Target Classic] non ha gestito le collisioni del selettore. [!DNL Target Standard/Premium] rileva tale comportamento e altri casi d’uso quando i selettori potrebbero entrare in conflitto sia nel DOM che visivamente (in genere eseguito a livello di editor di esperienze o in modalità di simulazione attività).

**Due attività utilizzano le offerte create in [!UICONTROL Compositore esperienza visivo] e due [!DNL Target Classic] attività**

* Attività 1: target-global-mbox, selector1, visualExpCompOffer1, media alta
* Attività 2: target-global-mbox, selector2, visualExpCompOffer2, priorità bassa
* Attività 1: target-global-mbox, offerta1, priorità alta
* Attività 2: target-global-mbox, offer2, priorità bassa

Risposta: offer1, visualExpCompOffer2, visualExpCompOffer1

>[!NOTE]
>
>L&#39;ordine delle risposte combinate è quello [!DNL Target Classic] il contenuto viene prima di tutto. Solo uno [!DNL Target Classic] la risposta viene elaborata come nel caso d’uso 1, quindi [!UICONTROL Compositore esperienza visivo] risposte alle offerte ordinate per priorità invertita.

## Video di formazione: Impostazioni attività (03:02)

Questo video include informazioni sulle impostazioni delle attività.

* Inserire una finalità per l’attività
* Impostare il livello di priorità delle attività
* Orari di inizio e fine dell’attività
* Aggiungere tipi di pubblico da usare come filtri nella generazione di rapporti
* Inserire delle note per le attività

>[!VIDEO](https://video.tv.adobe.com/v/17381)
