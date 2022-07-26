---
keywords: impostazioni;priorità
description: Adobe [!DNL Target] determina in modo diverso l’attività (o le attività) da consegnare a una pagina, a seconda di quale [!DNL Target] e quale funzione di creazione di attività utilizzi.
title: Come funziona [!DNL Target] Assegnare la priorità a diverse attività?
feature: Activities
exl-id: c32f1699-e564-40dd-8ff1-7c75a672c6ef
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 87%

---

# Priorità

Target determina in modo diverso l’attività (o le attività) da consegnare a una pagina, a seconda dell’interfaccia di Target e della funzione di creazione attività (Compositore esperienza visivo o Compositore basato su moduli) che stai utilizzando.

## Solo Compositore esperienza visivo di Target Standard/Premium o solo Compositore esperienza basato su moduli con globale [!DNL Target] Solo richiesta {#section_4A0A317DFED345649B58B0CB5B410C8B}

Se la tua società utilizza esclusivamente il Compositore esperienza visivo di Target Standard/Premium, per la stessa chiamata possono essere restituiti i contenuti da più attività. Le attività vengono consegnate in base al seguente flusso decisionale:

1. La chiamata al server di Target contiene le informazioni sull’URL.
1. Target richiama ogni attività in esecuzione su tale URL.
1. Target tenta di stabilire la corrispondenza tra il visitatore e le attività.

   Se il visitatore fa già parte di un test A/B o test multivariato, la corrispondenza con tale test permane fino alla conversione. Se era già in un’attività di targeting di esperienza, la sua corrispondenza con tale attività dovrà essere nuovamente stabilita. Se soddisfa le regole del pubblico, allora il visitatore rientra in tali attività e in esperienze specifiche.

1. Alla pagina vengono restituiti i contenuti per tutte le attività e le esperienze a cui corrisponde il visitatore.
1. Se i contenuti di ogni attività fanno riferimento a diversi [selettori CSS](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337), vengono visualizzati tutti i contenuti.

   In caso di sovrapposizione o di selettore CSS duplicato, viene visualizzato il contenuto dell’attività con la priorità più alta. I risultati di tutte le attività eseguite sulla pagina vengono conteggiati e si riflettono nei rapporti.

   >[!IMPORTANT]
   >
   >Target restituisce i contenuti per tutte le attività sulla pagina, a partire da quello con priorità più bassa, che viene poi sovrascritto da ogni attività, dalla priorità più bassa a quella più alta. Nella maggioranza dei casi, questo determina la visualizzazione del contenuto con la priorità più elevata. Tuttavia, se un’attività con priorità più bassa modifica la struttura del DOM per la pagina, è possibile che l’attività con priorità più elevata non riconosca la struttura della pagina, e in tal caso verrà visualizzato il contenuto con priorità inferiore. I risultati di tutte le attività eseguite sulla pagina vengono conteggiati e si riflettono nei rapporti.

1. Se più attività condividono lo stesso livello di priorità, esistono due fattori risolutivi:

   * Se il targeting per il pubblico è stato impostato per una sola attività, viene visualizzata tale attività.
   * Se il targeting per il pubblico è stato impostato per tutte le attività o per nessuna, viene visualizzata l’attività che è stata approvata per prima.

## Compositore esperienza basato su moduli di Target Standard/Premium e [!DNL Target] Compositore esperienza visivo di Standard/Premium {#section_4620253E1CE942DD830724C7822B175F}

>[!NOTE]
>
>Queste informazioni si applicano anche alle campagne in esecuzione che sono state create in [!DNL Target Classic].

Se la tua società utilizza il compositore basato su moduli di Target Standard/Premium e il Compositore esperienza visivo di Target Standard/Premium, può essere fornito il contenuto di più attività del Compositore esperienza visivo, ma solo un’attività dal flusso di lavoro basato su moduli. Le attività vengono consegnate in base al seguente flusso decisionale:

1. La chiamata al server di Target contiene informazioni su [!DNL Target] richiesta e URL.
1. Target Classic e Standard richiamano ogni attività in esecuzione in [!DNL Target] richiesta.
1. Target tenta di stabilire la corrispondenza tra il visitatore e le attività.

   Se il visitatore fa già parte di un test A/B o test multivariato, la corrispondenza con tale test permane fino alla conversione. Se era già in un’attività di targeting di esperienza, la sua corrispondenza con tale attività dovrà essere nuovamente stabilita. Se soddisfa le regole del pubblico, allora il visitatore rientra in tali attività e in esperienze specifiche.

1. Se un’attività basata su moduli ha la priorità più elevata, il contenuto dell’attività viene restituito insieme a tutti i contenuti di attività corrispondenti dalle attività del Compositore esperienza visivo.
1. Se un’attività del Compositore esperienza basato su moduli ha la priorità più elevata, viene restituito il contenuto di tutte le attività del compositore esperienza visivo, ma non vengono restituiti contenuti di attività basate su moduli o di Target Classic.

   I risultati di tutte le attività eseguite sulla pagina vengono conteggiati e si riflettono nei rapporti.

**Esempio**

In presenza di due attività, una con targeting impostato sulla parola chiave di ricerca del brand “Nike” e la seconda con targeting impostato sulla parola chiave generica “sneaker”, sono verificate le priorità di entrambe le attività. Se l’attività Nike ha una priorità più alta, viene visualizzato tale contenuto. Se l’attività sneaker ha la priorità più alta, viene visualizzato il suo contenuto.

Se entrambe le attività di targeting hanno la stessa priorità, viene visualizzata l’attività che è stata vista più di recente. Se si tratta di un visitatore sulla pagina in questione, viene visualizzata l’attività attivata più di recente.

## Compositore esperienza basato su moduli di Target Standard/Premium con non globale [!DNL Target] Richieste {#section_C3F5F09B0B2D4EF795C5929D5C426A8C}

>[!NOTE]
>
>Queste informazioni si applicano anche alle campagne in esecuzione che sono state create in Target Classic.

Se l&#39;azienda utilizza [!DNL Target] richieste diverse dal globale [!DNL Target] nel compositore basato su moduli, è possibile restituire il contenuto di una sola attività per chiamata. Le attività vengono consegnate in base al seguente flusso decisionale:

1. La [!DNL Target] la chiamata al server arriva a [!DNL Target] con informazioni sulle [!DNL Target] richiesta e URL.
1. [!DNL Target] richiama ogni attività in esecuzione in [!DNL Target] richiesta.
1. [!DNL Target] tenta di stabilire la corrispondenza tra il visitatore e l’attività con priorità più elevata.

   Se il visitatore fa già parte di un test A/B o test multivariato, la corrispondenza con tale test permane fino alla conversione. Se era già in un’attività di targeting di esperienza, la sua corrispondenza con tale attività dovrà essere nuovamente stabilita. Se soddisfa le regole del pubblico, allora il visitatore rientra in tali attività e in esperienze specifiche.

1. Se più attività condividono lo stesso livello di priorità, esistono due fattori risolutivi:

   * Se il targeting per il pubblico è stato impostato per una sola attività, viene visualizzata tale attività.
   * Se il targeting per il pubblico è stato impostato per tutte le attività o per nessuna, viene visualizzata l’attività che è stata approvata per prima.

## Esempi  {#section_F6A788AAC3884A2FA03E47F0557A1213}

>[!NOTE]
>
>I valori di priorità variano a seconda delle impostazioni. È possibile utilizzare le impostazioni legacy Bassa, Media o Alta, oppure attivare la priorità precisa da 0 a 999. Per ulteriori informazioni, consulta [Impostazioni attività](/help/main/c-activities/activity-settings.md#task_C6B2FF8374724933BE79A83549B9CD02).

**Due campagne di Target Classic utilizzano richieste Target non globali**

* Campagna 1: homePageHero, offer1, priorità alta
* Campagna 2: homePageHero, offer2, priorità bassa

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
>Questa è la stessa risposta del secondo caso di utilizzo precedente perché Target Classic non gestisce i conflitti di selettori. Target Standard rileva tale comportamento e altri casi di utilizzo in cui i selettori potrebbero essere in conflitto sia visivamente che in DOM (di solito succede a livello di editor di esperienza o in modalità di simulazione campagna).

**Due attività utilizzano offerte create nel Compositore esperienza visivo e due campagne di Target Classic**

* Attività 1: target-global-mbox, selector1, visualExpCompOffer1, media alta
* Attività 2: target-global-mbox, selector2, visualExpCompOffer2, priorità bassa
* Campagna 1: target-global-mbox, offer1, priorità alta
* Campagna 2: target-global-mbox, offer2, priorità bassa

Risposta: offer1, visualExpCompOffer2, visualExpCompOffer1

>[!NOTE]
>
>L’ordine delle risposte combinate prevede che il contenuto Classic venga prima (nel caso di utilizzo 1 sarà servita solo una risposta Classic), seguito dalle risposte all’offerta del Compositore esperienza visivo, ordinate per priorità inversa.

## Video di formazione: Impostazioni attività (03:02)

Questo video include informazioni sulle impostazioni delle attività.

* Inserire una finalità per l’attività
* Impostare il livello di priorità delle attività
* Orari di inizio e fine dell’attività
* Aggiungere tipi di pubblico da usare come filtri nella generazione di rapporti
* Inserire delle note per le attività

>[!VIDEO](https://video.tv.adobe.com/v/17381)
