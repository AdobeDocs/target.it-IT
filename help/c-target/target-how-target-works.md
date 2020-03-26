---
keywords: targeting;cookie;first-party cookie;1st-party cookie
description: Adobe Target si integra con le tue pagine web tramite la libreria JavaScript at.js o mbox.js.
title: Come funziona il targeting
uuid: 8b5a36c0-555d-42c5-8b24-c08d07440a53
translation-type: tm+mt
source-git-commit: ba4c776d93f911c122f36113a99ce4349b3c5524

---


# Come funziona il targeting{#how-targeting-works}

Adobe Target si integra con le tue pagine web tramite la libreria JavaScript at.js o mbox.js. Una libreria JavaScript a cui si fa riferimento in ogni pagina è tutto ciò che serve per eseguire le attività di ottimizzazione.

Ogni volta che un visitatore richiede una pagina su cui è abilitato [!DNL Target], questo utilizza il processo seguente per distribuire le offerte:

1. Un cliente richiede una pagina dal server e la visualizza nel browser.
1. Nel browser del cliente viene impostato un cookie di prime parti impostare un ID visitatore univoco.

   Viene impostato anche un [!DNL Experience Cloud visitor ID] se utilizzi il profilo marketing principale.

1. La pagina effettua una chiamata a [!DNL Target] tramite il file [!DNL target.js] o una mbox sulla tua pagina.
1. In [!DNL Target] viene fatto riferimento al profilo associato al visitatore.
1. In [!DNL Target] vengono eseguiti gli eventuali script di profilo associati al profilo.
1. [!DNL Target] calcola la risposta.
1. Il contenuto viene visualizzato in base alle regole dell&#39;attività o della campagna.

L&#39;offerta che viene visualizzata in un test A/B di base viene scelta in modo casuale. Come risultato di questa suddivisione casuale del traffico, è possibile che sia richiesta una quantità notevole di traffico iniziale prima che le percentuali si livellino. Ad esempio, se disponi di un&#39;attività con due esperienze, l&#39;esperienza iniziale viene scelta in modo casuale. Se il traffico è limitato, è possibile che la percentuale di visitatori tenda in modo più netto verso una delle due esperienze. Con l’aumento del traffico, le percentuali tendono a equilibrarsi.
