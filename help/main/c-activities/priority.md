---
keywords: impostazioni;priorità
description: Scopri come [!DNL Adobe Target] determina in modo diverso l'attività (o le attività) da consegnare a una pagina, a seconda dell'interfaccia [!DNL Target] e della funzione di creazione attività in uso.
title: In che modo  [!DNL Target]  assegna la priorità ad attività diverse?
feature: Activities
exl-id: c32f1699-e564-40dd-8ff1-7c75a672c6ef
TQID: https://experienceleague.adobe.com/KSkJ1CDkd4hgwnLQ1RKn8l8r2MDIO-6flcHcdN0c0oQ
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 987
ht-degree: 34%

---

# Priorità

[!DNL Adobe Target] determina in modo diverso l&#39;attività (o le attività) da consegnare a una pagina a seconda dell&#39;interfaccia [!DNL Target] e della funzione di creazione attività ([[!UICONTROL Compositore esperienza visivo]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) o [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md)) in uso.

## [!UICONTROL Solo Compositore esperienza visivo] o [!UICONTROL Solo Compositore esperienza basato su moduli] utilizzando una richiesta [!DNL Target] globale {#section_4A0A317DFED345649B58B0CB5B410C8B}

Se l’azienda utilizza esclusivamente il Compositore esperienza visivo, è possibile restituire il contenuto di più attività per la stessa chiamata. Le attività vengono consegnate in base al seguente flusso decisionale:

1. La chiamata al server [!DNL Target] arriva a [!DNL Target] con informazioni sull&#39;URL.
1. [!DNL Target] richiama ogni attività in esecuzione su tale URL.
1. [!DNL Target] tenta di associare il visitatore alle attività.

   Se il visitatore si trova già in un&#39;attività [!UICONTROL Test A/B] o [!UICONTROL Test multivariato], la corrispondenza con tale attività verrà mantenuta fino alla conversione. Se si trovavano in precedenza in un&#39;attività [!UICONTROL Targeting esperienza], devono corrispondere nuovamente in essa. Se soddisfa le regole del pubblico, allora il visitatore rientra in tali attività e in esperienze specifiche.

1. Alla pagina vengono restituiti i contenuti per tutte le attività e le esperienze a cui corrisponde il visitatore.
1. Se il contenuto di ogni attività fa riferimento a [selettori CSS](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337) diversi, viene visualizzato tutto il contenuto.

   In caso di sovrapposizione o di selettore CSS duplicato, viene visualizzato il contenuto dell’attività con la priorità più alta. I risultati di tutte le attività eseguite sulla pagina vengono conteggiati e si riflettono nei rapporti.

   >[!IMPORTANT]
   >
   >[!DNL Target] restituisce il contenuto per tutte le attività sulla pagina, a partire dal contenuto con priorità più bassa, che viene quindi sovrascritto da ogni attività, dalla priorità più bassa a quella più alta. Di solito, questo determina la visualizzazione del contenuto con la priorità più elevata. Tuttavia, se un’attività con priorità inferiore modifica la struttura del DOM per la pagina, è possibile che l’attività con priorità più alta non riconosca la struttura della pagina, per cui viene visualizzato il contenuto con priorità inferiore. I risultati di tutte le attività eseguite sulla pagina vengono conteggiati e si riflettono nei rapporti.

1. Se più attività condividono il livello di priorità, esistono due livelli di priorità:

   * Se il targeting per il pubblico è stato impostato per una sola attività, viene visualizzata tale attività.
   * Se tutti o nessuno ha un targeting, viene visualizzata l’attività approvata per prima.

## [!UICONTROL Compositore esperienza basato su moduli] e [!UICONTROL Compositore esperienza visivo] {#section_4620253E1CE942DD830724C7822B175F}

Se l&#39;azienda utilizza il [!UICONTROL Compositore esperienza basato su moduli] *e* il Compositore esperienza visivo, è possibile distribuire il contenuto di più [!UICONTROL Compositore esperienza basato su moduli] e attività del Compositore esperienza visivo. In precedenza, era possibile eseguire una sola attività dal flusso di lavoro basato su moduli. Non esiste più un limite al numero di attività basate su moduli che possono essere consegnate.

Le attività vengono consegnate in base al seguente flusso decisionale:

1. Chiamata al server [!DNL Target] inviata a [!DNL Target] con informazioni sulla richiesta e sull&#39;URL di [!DNL Target].
1. [!DNL Target] richiama ogni attività in esecuzione nella richiesta [!DNL Target].
1. [!DNL Target] tenta di associare il visitatore alle attività.

   Se il visitatore si trova già in un&#39;attività [!UICONTROL Test A/B] o [!UICONTROL Test multivariato], la corrispondenza con tale test viene mantenuta fino alla conversione. Se si trovavano in precedenza in un&#39;attività [!UICONTROL Targeting esperienza], devono corrispondere nuovamente in essa. Se soddisfa le regole del pubblico, allora il visitatore rientra in tali attività e in esperienze specifiche.

1. Se un’attività basata su moduli ha la priorità più alta, il contenuto dell’attività viene restituito insieme a tutto il contenuto dell’attività corrispondente dalle attività del Compositore esperienza visivo.
1. Se un’attività del Compositore esperienza visivo ha la priorità più alta, viene restituito il contenuto di tutte le attività del Compositore esperienza visivo corrispondenti, ma non viene restituito alcun contenuto di attività basato su modulo.

   I risultati di tutte le attività eseguite sulla pagina vengono conteggiati e si riflettono nei rapporti.

**Esempio**

In presenza di due attività, una con targeting per la parola chiave di ricerca del brand &quot;Nike&quot; e la seconda con targeting per la parola chiave non del brand &quot;sneakers&quot;, vengono controllate le priorità di entrambe le attività. Se l’attività Nike ha una priorità più alta, viene visualizzato tale contenuto. Se l’attività sneaker ha la priorità più alta, viene visualizzato il suo contenuto.

Se entrambe le attività di targeting hanno la stessa priorità, viene visualizzata l’attività che è stata vista più di recente. Se si tratta di un visitatore sulla pagina in questione, viene visualizzata l’attività attivata più di recente.

## [!UICONTROL Compositore esperienza basato su moduli] con [!DNL Target] richieste non globali {#section_C3F5F09B0B2D4EF795C5929D5C426A8C}

Se la società utilizza [!DNL Target] richieste diverse dalla richiesta globale di [!DNL Target] nel compositore basato su moduli, è possibile restituire il contenuto di una sola attività per chiamata. Le attività vengono consegnate in base al seguente flusso decisionale:

1. La chiamata al server [!DNL Target] arriva a [!DNL Target] con informazioni sulla richiesta e sull&#39;URL di [!DNL Target].
1. [!DNL Target] richiama ogni attività in esecuzione nella richiesta [!DNL Target].
1. [!DNL Target] tenta di associare il visitatore all&#39;attività con la priorità più alta.

   Se il visitatore si trova già in un&#39;attività [!UICONTROL Test A/B] o [!UICONTROL Test multivariato], la corrispondenza con tale attività verrà mantenuta fino alla conversione. Se si trovavano in precedenza in un&#39;attività [!UICONTROL Targeting esperienza], devono corrispondere nuovamente in essa. Se soddisfa le regole del pubblico, allora il visitatore rientra in tali attività e in esperienze specifiche.

1. Se più attività condividono il livello di priorità, esistono due livelli di priorità:

   * Se il targeting per il pubblico è stato impostato per una sola attività, viene visualizzata tale attività.
   * Se tutti o nessuno ha un targeting, viene visualizzata l’attività approvata per prima.

## Esempi {#section_F6A788AAC3884A2FA03E47F0557A1213}

>[!NOTE]
>
>I valori di priorità variano a seconda delle impostazioni. Puoi utilizzare le impostazioni legacy di [!UICONTROL Bassa], [!UICONTROL Medium] o [!UICONTROL Alta] oppure abilitare le priorità precise da 0 a 999. Per ulteriori informazioni, vedere [Impostazioni attività](/help/main/c-activities/activity-settings.md#task_C6B2FF8374724933BE79A83549B9CD02).

Risposta: offer1

**Due attività utilizzano solo le offerte create nel [!UICONTROL Compositore esperienza visivo] per selettori diversi**

* Attività 1: target-global-mbox, selector1, visualExpCompOffer1, priorità bassa
* Attività 2: target-global-mbox, selector2, visualExpCompOffer2, priorità alta

Risposta: visualExpCompOffer1, visualExpCompOffer2

**Due attività utilizzano solo le offerte create nel [!UICONTROL Compositore esperienza visivo] per lo stesso selettore**

* Attività 1: target-global-mbox, selector1, visualExpCompOffer1, priorità bassa
* Attività 2: target-global-mbox, selector1, visualExpCompOffer2, priorità alta

Risposta: visualExpCompOffer1, visualExpCompOffer2

## Video di formazione: Impostazioni attività (3:02)

Questo video include informazioni sulle impostazioni delle attività.

* Inserire una finalità per l’attività
* Impostare il livello di priorità delle attività
* Orari di inizio e fine dell’attività
* Aggiungere tipi di pubblico da usare come filtri nella generazione di rapporti
* Inserire delle note per le attività

>[!VIDEO](https://video.tv.adobe.com/v/17381)
