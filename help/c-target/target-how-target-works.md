---
description: Adobe Target si integra con le tue pagine web tramite la libreria JavaScript at.js o mbox.js.
keywords: targeting;cookie;cookie di prima parte;cookie di 1ª parte
seo-description: Adobe Target si integra con le tue pagine web tramite la libreria JavaScript at.js o mbox.js.
seo-title: Come funziona il targeting
solution: Target
title: Come funziona il targeting
uuid: 8b5a36c0-555d-42c5-8b24-c08d07440a53
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Come funziona il targeting{#how-targeting-works}

Adobe Target si integra con le tue pagine web tramite la libreria JavaScript at.js o mbox.js.

In [!DNL Target Classic] sono utilizzate mbox intorno a ogni area nella pagina in cui visualizzare contenuto con targeting o raccogliere dati. Queste mbox non sono necessarie in [!DNL Target Standard]. Una libreria JavaScript a cui fare riferimento in ogni pagina è tutto ciò che serve per eseguire le attività di ottimizzazione.

Ogni volta che un visitatore richiede una pagina su cui è abilitato [!DNL Target], questo utilizza il processo seguente per distribuire le offerte:

1. Un cliente richiede una pagina dal server e la visualizza nel browser.
1. Nel browser del cliente viene impostato un cookie di prime parti impostare un ID visitatore univoco.

   Viene impostato anche un [!DNL Experience Cloud visitor ID] se utilizzi il profilo marketing principale.

1. La pagina effettua una chiamata a [!DNL Target] tramite il file [!DNL target.js] o una mbox sulla tua pagina.
1. In [!DNL Target] viene fatto riferimento al profilo associato al visitatore.
1. In [!DNL Target] vengono eseguiti gli eventuali script di profilo associati al profilo.
1. [!DNL Target] calcola la risposta.
1. Il contenuto viene visualizzato in base alle regole dell'attività o della campagna.

L'offerta che viene visualizzata in un test A/B di base viene scelta in modo casuale. Come risultato di questa suddivisione casuale del traffico, è possibile che sia richiesta una quantità notevole di traffico iniziale prima che le percentuali si livellino. Ad esempio, se disponi di un'attività con due esperienze, l'esperienza iniziale viene scelta in modo casuale. Se il traffico è limitato, è possibile che la percentuale di visitatori tenda in modo più netto verso una delle due esperienze. Con l’aumento del traffico, le percentuali tendono a equilibrarsi.
