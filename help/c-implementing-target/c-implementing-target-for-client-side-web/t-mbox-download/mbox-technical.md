---
keywords: implementazione;mbox.js;libreria di manipolazione dom;target.js;compositore di esperienza visivo;iframe;siti angular;applicazioni a pagina singola;app a singola pagina;SPA
description: Scopri l’implementazione legacy di mbox.js di Adobe Target. Esegui la migrazione a Adobe Experience Platform Web SDK (AEP Web SDK) o all’ultima versione di at.js.
title: Come funziona la libreria [!DNL Target] mbox.js?
feature: at.js
role: Developer
exl-id: 62f0cbd2-17f0-43f4-98d3-ea39f314525e
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 78%

---

# Funzionamento di mbox.js

Informazioni utili per il personale tecnico, per comprendere l’implementazione di mbox.js e come potrebbe influenzare il sito.

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: a partire dal 31 marzo 2021, [!DNL Adobe Target] non supporta più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e le pagine che hanno attività [!DNL Target] in esecuzione, si troveranno a utilizzare il contenuto predefinito.
>
>È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js prima di tale data, per evitare potenziali problemi con i siti. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## Manipolazione di DOM {#section_169F8D4C077948DCB4F891ABBB03FF63}

[!DNL Target.js] controlla la libreria di manipolazione DOM utilizzata da Standard. Per visualizzare il contenuto di un sito web, [!DNL target.js] fa riferimento a [!DNL sizzle.js] (versione 1.10.8-pre). [!DNL Sizzle.js] abilita i selettori degli elementi HTML. A parte [!DNL sizzle.js], viene utilizzato solo JavaScript nativo. Non sono richieste jquery.

Inoltre, il frammento seguente viene utilizzato per il polling del DOM:
`https://github.com/dperini/ContentLoaded`

## Target.js e il Compositore esperienza visivo {#section_2B3FF6AC5B8D431C83D9EDCF53CB1472}

Quando si utilizza il [!UICONTROL Compositore esperienza visivo] per impostare l’esperienza per un’attività, la pagina web viene aperta in un iFrame. Una volta caricato l’iFrame, Standard invia una chiamata API `postMessage` HTML5. [!DNL Target.js] rileva eventuali chiamate `postMessage` e include le seguenti librerie JavaScript sul sito web:

* Per la generazione delle miniature: [!DNL https://html2canvas.hertzen.com/]
* Per query interdominio: [!DNL Admin.js], [!DNL CDQ.base.js], [!DNL CDQ.host.js], [!DNL admin.css], utilizzati per inviare messaggi tra iFrame. Questi script consentono ad Adobe l’invio di dati tra pagine.

## Considerazioni per siti Angular e applicazioni a pagina singola {#section_16D76F16077A434FAE8CEC6FD43BE6D7}

Se si implementa Target in un sito Angular o in applicazioni a pagina singola, è necessario utilizzare la libreria at.js invece di mbox.js.
