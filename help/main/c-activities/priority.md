---
keywords: impostazioni;priorità
description: Scopri come [!DNL Adobe Target] determina in modo diverso l'attività (o le attività) da consegnare a una pagina, a seconda dell'interfaccia [!DNL Target] e della funzione di creazione attività in uso.
title: In che modo [!DNL Target] assegna la priorità ad attività diverse?
feature: Activities
exl-id: c32f1699-e564-40dd-8ff1-7c75a672c6ef
TQID: 'https://experienceleague.adobe.com/KSkJ1CDkd4hgwnLQ1RKn8l8r2MDIO-6flcHcdN0c0oQ'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: 6efa6b7a-8062-5c41-aef4-b4853cc306ae
    internal-label: Activities
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 7eede3484d524e87127de9147aa786484fc87c7d
workflow-type: tm+mt
source-wordcount: '1043'
ht-degree: 19%
---
# Priorità {#priority}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come [!DNL Adobe Target] decide quali attività distribuire a una pagina, a seconda del compositore esperienza e del tipo di richiesta [!DNL Target] in uso.

>[!ENDSHADEBOX]

[!DNL Adobe Target] determina in modo diverso l&#39;attività (o le attività) da consegnare a una pagina a seconda dell&#39;interfaccia [!DNL Target] e della funzione di creazione attività ([**[!UICONTROL Compositore esperienza visivo]**](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) o [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md)) in uso. La tabella che segue riassume i tre casi, descritti nelle sezioni che seguono.

| Scenario | Attività che possono fornire | Contenuto restituito |
|---|---|---|
| **[!UICONTROL Solo Compositore esperienza visivo]** o **[!UICONTROL Solo Compositore esperienza basato su moduli]** con una richiesta [!DNL Target] globale | Vari prodotti | Contenuto di tutte le attività corrispondenti. Se i selettori si sovrappongono, viene visualizzato il contenuto dell’attività con priorità più alta. |
| **[!UICONTROL Compositore esperienza basato su moduli]** e **[!UICONTROL Compositore esperienza visivo]** | Vari prodotti | Se un’attività basata su moduli ha la priorità più elevata, il suo contenuto e il contenuto di tutte le attività del Compositore esperienza visivo corrispondenti. Se un’attività del Compositore esperienza visivo ha la priorità più alta, indica solo il contenuto di tutte le attività del Compositore esperienza visivo corrispondenti. |
| **[!UICONTROL Compositore esperienza basato su moduli]** con [!DNL Target] richieste non globali | Uno per chiamata | Contenuto dell’attività di corrispondenza a priorità più alta. |

## VEC o [!UICONTROL Compositore esperienza basato su moduli] con una richiesta globale {#section_4A0A317DFED345649B58B0CB5B410C8B}

Se l’azienda utilizza esclusivamente il Compositore esperienza visivo, è possibile restituire il contenuto di più attività per la stessa chiamata. Le attività vengono consegnate in base al seguente flusso decisionale:

1. La chiamata al server [!DNL Target] raggiunge [!DNL Target]. La chiamata contiene informazioni sull’URL della pagina richiesta.
1. [!DNL Target] richiama tutte le attività in esecuzione sull&#39;URL. Queste attività sono le candidate per la consegna.
1. [!DNL Target] tenta di associare il visitatore alle attività candidate.

   {{visitor-matching}}

1. Il contenuto di tutte le attività ed esperienze a cui corrisponde il visitatore viene restituito alla pagina, quindi il contenuto di più attività può essere consegnato per la stessa chiamata.
1. [!DNL Target] confronta i [selettori CSS](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md) a cui fa riferimento il contenuto di ogni attività. Se le attività fanno riferimento a selettori diversi, viene visualizzato tutto il contenuto.
1. Se un selettore si sovrappone o è duplicato, viene visualizzato il contenuto dell’attività con priorità più elevata.

   >[!IMPORTANT]
   >
   >[!DNL Target] restituisce il contenuto per tutte le attività sulla pagina, a partire dal contenuto con priorità più bassa, che viene quindi sovrascritto da ogni attività, dalla priorità più bassa a quella più alta. Di solito, questo determina la visualizzazione del contenuto con la priorità più elevata. Tuttavia, se un’attività con priorità inferiore modifica la struttura del DOM per la pagina, l’attività con priorità superiore potrebbe non riconoscere la struttura della pagina, pertanto viene visualizzato il contenuto con priorità inferiore.

1. Se più attività condividono un livello di priorità, viene applicato un tiebreaker. Se solo una delle attività dispone di un targeting di pubblico, viene visualizzata tale attività. Se tutte o nessuna delle attività ha un targeting, viene visualizzata l’attività approvata per prima.
1. I risultati di tutte le attività eseguite sulla pagina vengono conteggiati e si riflettono nei rapporti.

## [!UICONTROL Compositore esperienza basato su moduli] e Compositore esperienza visivo {#section_4620253E1CE942DD830724C7822B175F}

Se l&#39;azienda utilizza il [!UICONTROL Compositore esperienza basato su moduli] *e* il Compositore esperienza visivo, è possibile distribuire il contenuto di più [!UICONTROL attività del Compositore esperienza basato su moduli] e del Compositore esperienza visivo. In precedenza, era possibile eseguire una sola attività dal flusso di lavoro basato su moduli. Non esiste più un limite al numero di attività basate su moduli che possono essere consegnate.

Le attività vengono consegnate in base al seguente flusso decisionale:

1. La chiamata al server [!DNL Target] raggiunge [!DNL Target]. La chiamata contiene informazioni sulla richiesta [!DNL Target] e sull&#39;URL.
1. [!DNL Target] richiama tutte le attività in esecuzione nella richiesta [!DNL Target]. Queste attività sono le candidate per la consegna.
1. [!DNL Target] tenta di associare il visitatore alle attività candidate.

   {{visitor-matching}}

1. [!DNL Target] controlla quali delle attività corrispondenti hanno la priorità più alta e se tale attività è stata creata nel [!UICONTROL Compositore esperienza basato su moduli] o nel Compositore esperienza visivo.
1. Se un’attività basata su modulo ha la priorità più elevata, il suo contenuto viene restituito insieme a quello di tutte le attività del Compositore esperienza visivo corrispondenti.
1. Se un’attività del Compositore esperienza visivo ha la priorità più alta, viene restituito il contenuto di tutte le attività del Compositore esperienza visivo corrispondenti, ma non viene restituito alcun contenuto di attività basato su moduli.
1. I risultati di tutte le attività eseguite sulla pagina vengono conteggiati e si riflettono nei rapporti.

**Esempio**

Esistono due attività: una è indirizzata alla parola chiave di ricerca &quot;Nike&quot; e l’altra alla parola chiave non di marca &quot;sneakers&quot;. Vengono verificate le priorità di entrambe le attività. Se l’attività Nike ha una priorità più alta, viene visualizzato il relativo contenuto. Se l’attività sneaker ha la priorità più alta, viene visualizzato il suo contenuto.

Se entrambe le attività di targeting hanno la stessa priorità, viene visualizzata l’attività che è stata vista più di recente. Se si tratta di un visitatore sulla pagina in questione, viene visualizzata l’attività attivata più di recente.

## [!UICONTROL Compositore esperienza basato su moduli] con richieste non globali {#section_C3F5F09B0B2D4EF795C5929D5C426A8C}

Se la società utilizza [!DNL Target] richieste diverse dalla richiesta globale di [!DNL Target] nel compositore basato su moduli, è possibile restituire il contenuto di una sola attività per chiamata. Le attività vengono consegnate in base al seguente flusso decisionale:

1. La chiamata al server [!DNL Target] raggiunge [!DNL Target]. La chiamata contiene informazioni sulla richiesta [!DNL Target] e sull&#39;URL.
1. [!DNL Target] richiama tutte le attività in esecuzione nella richiesta [!DNL Target]. Queste attività sono le candidate per la consegna.
1. [!DNL Target] tenta di associare il visitatore all&#39;attività candidato con la priorità più elevata.

   {{visitor-matching}}

1. Se più attività condividono un livello di priorità, viene applicato un tiebreaker. Se solo una delle attività dispone di un targeting di pubblico, viene visualizzata tale attività. Se tutte o nessuna delle attività ha un targeting, viene visualizzata l’attività approvata per prima.
1. Il contenuto di quella singola attività viene restituito alla pagina.

## Esempi {#section_F6A788AAC3884A2FA03E47F0557A1213}

>[!NOTE]
>
>I valori di priorità variano a seconda delle impostazioni. Puoi utilizzare le impostazioni legacy di **[!UICONTROL Bassa]**, **[!UICONTROL Medium]** o **[!UICONTROL Alta]** oppure abilitare le priorità precise da 0 a 999. Per ulteriori informazioni, vedere [Impostazioni attività](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#section_DCBDC354261F420EBD4B43EA34947BAC).

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
