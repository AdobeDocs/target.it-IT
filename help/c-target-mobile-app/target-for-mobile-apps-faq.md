---
description: Frequently Asked Questions about Adobe Target for mobile apps.
keywords: mobile app;frequently asked questions;faq;target mobile app
seo-description: Frequently Asked Questions about Adobe Target for mobile apps.
seo-title: Domande frequenti su Adobe Target per app mobili
title: Domande frequenti su Adobe Target per app mobili
topic: Target
uuid: 3d6422ac-7cff-4e0d-9cea-64a64cd1a098
translation-type: tm+mt
source-git-commit: 43a00c7ade1f2e10a023ffdcb2e75cf2483e6907

---


# Target for mobile apps FAQ

Elenco di domande frequenti su [!DNL Target] per app mobili.

## Devo utilizzare [!DNL Adobe Experience Platform Launch] per distribuire l’SDK, oppure posso distribuire l’SDK senza utilizzare [!DNL Launch]?

L’SDK è disponibile sul git di [Adobe Marketing Cloud](https://github.com/Adobe-Marketing-Cloud/acp-sdks/). Se non usi [Launch](https://docs.adobe.com/content/help/en/launch/using/overview.html), devi gestire il file delle impostazioni e gestirlo nell'app.

## È possibile utilizzare Visual Experience Composer (VEC) per app mobili con il supporto nativo React per l'SDK v5 di Adobe Experience Platform?

Al momento, [VEC per le app](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md) mobili native non supporta l'app nativa React. È necessario utilizzare Experience Composer (Compositore esperienza basato su [moduli](/help/c-experiences/form-experience-composer.md)).

## L’integrazione con Mobile SDK consente l’implementazione di nuove funzionalità per dispositivi mobili? È possibile attivare e disattivare il flag di funzione senza nuove distribuzioni di codice?

Sì, puoi usare il nostro SDK per dispositivi mobili per distribuire gradualmente le funzionalità.

## Per una logica più complessa, devo sviluppare direttamente nell'app invece di utilizzare Mobile VEC? In caso affermativo, quale lingua di sviluppo dovrei usare?

Attualmente, il VEC supporta casi d’uso comuni come la modifica di immagine, testo, colore, ecc. Per casi di utilizzo più avanzati, ad esempio per personalizzare il layout dell'app, dovete inserire la [!DNL Target] richiesta/posizione (mbox) nel codice e utilizzare Experience Composer (Compositore esperienza basato su [modulo](/help/c-experiences/form-experience-composer.md) ) per progettare le esperienze e allocare il traffico. Il nostro SDK per dispositivi mobili supporta Java, Objective C e Swift. Dipende dalle preferenze e risorse del team per scegliere la lingua.

## Quali SDK sono disponibili oggi?

Gli SDK di Adobe Experience Platform Mobile al momento supportano iOS, Android e React. Per ulteriori informazioni, consulta la guida [agli SDK per dispositivi mobili](https://aep-sdks.gitbook.io/docs/)Adobe Experience Cloud Platform.

## Qual è la frequenza della funzione basata sulla posizione, in termini di verifica della latitudine e della longitudine?

See the [Adobe Places documentation](https://placesdocs.com/places-services-by-adobe-documentation/) for more information.

## Quali classi native sono supportate dalle visualizzazioni mobili? Supportano qualsiasi classe derivata da NSObject (o qualsiasi oggetto Android) o solo NSViewController e Activities?

For more information, visit the Android documentation for the manual way of declaring views.[](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md#views)

## È necessario at.js per il funzionamento degli SDK di Adobe Experience Platform Mobile?

No, you don’t need at.js to use the mobile SDKs. at.js è la libreria [!DNL Target] JavaScript per i siti Web. Gli SDK di Adobe Experience Platform Mobile sono per le app mobili.

## Target Mobile è una funzionalità solo dello SKU prodotto Adobe Target Premium?

Per i clienti di Adobe Target Standard, potete utilizzare i nostri SDK Mobile solo per attività Test e Targeting delle esperienze A/B (XT). Se desiderate utilizzare le funzionalità di Recommendations o basate sull'intelligenza artificiale nell'app mobile, avete bisogno di una licenza [Adobe Target Premium](/help/c-intro/intro.md#premium) .

## Can I leverage audiences from Adobe Audience Manager (AAM) in the VEC for Mobile Apps?

Yes, Adobe Experience Platform Mobile SDKs are built for Audience Manager, Analytics, Campaign, and Target. [](https://docs.adobe.com/content/help/en/audience-manager/user-guide/aam-home.html)[](https://docs.adobe.com/content/help/en/analytics/landing/home.html)[](https://docs.adobe.com/content/help/en/campaign-standard/using/campaign-standard-home.html) Your audiences in Audience Manager are shared with .[!DNL Target]

## Is there a mobile app integration between Adobe Experience Manager (AEM) and Target mobile activities?

E' nella nostra tabella di marcia, ma non c'è ancora una data. Currently, you can share JSON Experience Fragments from AEM to Target and there might be potential to then use them in a mobile app activity.[](/help/c-experiences/c-manage-content/aem-experience-fragments.md)

## È possibile aggiungere altre immagini utilizzando il VEC o solo modificare le immagini esistenti?

Al momento potete modificare solo le immagini esistenti.
