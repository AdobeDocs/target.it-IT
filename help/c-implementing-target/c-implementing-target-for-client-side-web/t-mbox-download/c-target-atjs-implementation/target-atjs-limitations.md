---
keywords: visual experience composer limitations;browser support;integrations;plugins;asynchronous considerations
description: Esistono alcune differenze tra at.js e mbox.js. In questa sezione vengono elencate alcune delle differenze e limitazioni, per aiutarti a utilizzare at.js con successo.
title: Limitazioni di at.js
feature: null
uuid: 6c2dfd85-4c4d-4204-a9e9-e358f0b70ded
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 100%

---


# Limitazioni di at.js{#at-js-limitations}

Esistono alcune differenze tra at.js e mbox.js. In questa sezione vengono elencate alcune delle differenze e limitazioni, per aiutarti a utilizzare at.js con successo.

## Limitazioni note del Compositore esperienza visivo {#section_4B63C97169DE4C93B22944E880FD3DF1}

* Con le applicazioni a pagina singola si dovrebbero evitare le opzioni Inserisci elemento e Ridisponi nel Compositore esperienza visivo.

   Poiché il DOM non è cancellato per gli eventi di caricamento pagina nelle applicazioni a pagina singola come succede nei siti web tradizionali, le manipolazioni Inserisci elemento e Ridisponi potrebbero essere applicate più volte a seconda del modo in cui il visitatore naviga nell’applicazione.

## Integrazioni e plug-in {#section_D92E31170176406AAC7B5005F03D3425}

Alcune funzioni di [!DNL mbox.js] non sono disponibili in [!DNL at.js]. Gli [oggetti e i metodi interni di mbox.js](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md#section_8C78059D15D9452F95636A5640188537) (come `mbox`, `mboxCurrent`, `mboxFactoryDefault`, `mboxFactories` e altri) non sono più supportati da [!DNL at.js] (ad esempio: `mboxFactoryDefault`). È una scelta progettuale, pensata per scoraggiare gli utenti da eseguire “hacking” su [!DNL at.js] per sviluppare funzionalità non supportate che a lungo termine possono paralizzare un&#39;implementazione e renderne impossibile l&#39;aggiornamento. Gli unici metodi esposti sono descritti nelle pagine API di questa documentazione. Per questo motivo:

* Le [integrazioni](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39) legacy basate su pagina con altre soluzioni Adobe potrebbero non funzionare e devono essere aggiornate alle più recenti integrazioni lato server.
* [I plug-in personalizzati sviluppati per mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-plugins.md#concept_F5D4C0A4DACF41409CC42FDD93B13FAF) potrebbero non funzionare se non aggiornati per [!DNL at.js].

   Assicurati di includere eventuali [plug-in](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-plugins.md#concept_F5D4C0A4DACF41409CC42FDD93B13FAF) come parte del test.

## Considerazioni asincrone {#section_B586360A3DD34E2995AE25A18E3FB953}

Poiché tutte le mbox sono ora asincrone, non bloccano il rendering della pagina né tornano nell&#39;ordine in cui sono state attivate.

* Se utilizzi una mbox globale nel [Compositore esperienza basato su moduli](/help/c-experiences/experiences.md#section_3643394BD424463C8768F2907DEBCC22), tieni presente che le offerte HTML supportano solo i tag `<script>`, `<style>` e `<link>`.

   Durante la distribuzione, quando vengono applicate le offerte mbox globali, [!DNL at.js] filtra tutti gli altri tag HTML. Le mbox globali sono valide per l&#39;elemento HTML HEAD, che non consente l&#39;uso di DIV, SPAN e così via. Ad esempio, `<div>test</div>` non può essere applicato perché il tag `<div>` può essere utilizzato solo all’interno dell’elemento HTML BODY.

* L&#39;integrazione legacy di [!DNL Target] con [!DNL Analytics] basata sulla pagina non funziona.

   Questa integrazione richiede che la chiamata di [!DNL Target] sia effettuata prima della chiamata di [!DNL Analytics].

* Attenzione alle dipendenze JavaScript tra l&#39;offerta e la pagina.

   Non supporre che il JavaScript nella tua offerta si esegua prima del JavaScript hardcoded sotto la mbox.

* Attenzione alle dipendenze JavaScript tra più offerte sulla pagina.

   Non puoi più supporre che l&#39;offerta consegnata dalla prima mbox venga eseguita prima dell&#39;offerta consegnata dalla seconda mbox.

* La manipolazione DOM e le offerte di Reindirizzamento devono essere consegnate attraverso la mbox globale creata automaticamente in [!DNL at.js] nella sezione `<head>`.

   Una funzione `mboxCreate()` nella parte superiore della sezione `<body>` probabilmente provocherà una visualizzazione momentanea del contenuto predefinito.

