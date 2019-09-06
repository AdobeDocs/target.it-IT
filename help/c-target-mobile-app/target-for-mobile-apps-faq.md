---
description: Domande frequenti su Adobe Target per le app mobili.
keywords: app per dispositivi mobili; domande frequenti; faq; app mobile di destinazione
seo-description: Domande frequenti su Adobe Target per le app mobili.
seo-title: Domande frequenti su Adobe Target per le app mobili
title: Domande frequenti su Adobe Target per app mobili
topic: Target
uuid: 3d6422ac-7cff-4e0d-9cea-64a64cd1a098
translation-type: tm+mt
source-git-commit: 43a00c7ade1f2e10a023ffdcb2e75cf2483e6907

---


# Target for mobile apps FAQ

Elenco delle domande frequenti sulle [!DNL Target] app mobili.

## Posso utilizzare [!DNL Adobe Experience Platform Launch] per distribuire l'SDK, o posso distribuire l'SDK senza utilizzare [!DNL Launch]?

L'SDK è disponibile sul git [di Adobe Marketing Cloud](https://github.com/Adobe-Marketing-Cloud/acp-sdks/). Se non usi [Launch](https://docs.adobe.com/content/help/en/launch/using/overview.html), devi gestire il tuo file di impostazioni e gestirlo nell'app.

## È possibile utilizzare Visual Experience Composer (Compositore esperienza visivo) per le app mobili con il supporto nativo per la piattaforma Adobe Experience Platform SDK v 5?

Il [VEC per app mobile native](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md) al momento non supporta l'app nativa Reagisci. È necessario utilizzare il composer di esperienze [basato su modulo](/help/c-experiences/form-experience-composer.md).

## L'integrazione dell'SDK di Mobile consente di uscire dalla nuova funzionalità mobile? Posso attivare e disattivare il flag della funzione senza nuove distribuzioni del codice?

Sì, puoi utilizzare il nostro SDK di Mobile per distribuire gradualmente le funzionalità.

## Per una logica più complessa, posso sviluppare direttamente nell'app invece di utilizzare la VEC Mobile? In tal caso, quale linguaggio di sviluppo devo usare?

Al momento, la VEC supporta casi d'uso comuni quali la modifica dell'immagine, del testo, del colore e così via. Per casi d'uso più avanzati, ad esempio personalizzare il layout dell'app, dovete inserire [!DNL Target] la richiesta/posizione (mbox) nel codice e utilizzare il [Composer esperienza basato su modulo](/help/c-experiences/form-experience-composer.md) per progettare le esperienze e allocare il traffico. Il nostro SDK di Mobile supporta Java, Objective C e Swift. Dipende dalle preferenze e dalle risorse del team per scegliere la lingua.

## Quali SDK sono disponibili oggi?

Gli SDK per dispositivi mobili Adobe Experience Platform attualmente supportano iOS, Android e Reagisci. Per ulteriori informazioni, consulta la guida SDK per dispositivi mobili di [Adobe Experience Cloud](https://aep-sdks.gitbook.io/docs/).

## Qual è la frequenza della funzione basata sulla posizione, in termini di verifica della latitudine e della longitudine?

See the [Adobe Places documentation](https://placesdocs.com/places-services-by-adobe-documentation/) for more information.

## Quali classi native eseguono il supporto per «visualizzazioni» mobile? Supportano qualsiasi classe derivata nsobject (o qualsiasi oggetto Android) o nsviewcontroller e attività?

Per ulteriori informazioni, visita la documentazione di Android per ottenere il modo [manuale di dichiarare le visualizzazioni](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md#views).

## Per lavorare, devo usare at. js per gli SDK mobile della piattaforma Adobe Experience Platform?

No, at use at. js to use the mobile SDK. at. js è la [!DNL Target] libreria javascript per i siti Web. Gli SDK per dispositivi mobili Adobe Experience Platform sono per app mobili.

## Target Mobile è una funzionalità solo per Adobe Target Premium Product SKU?

Per i clienti Adobe Target Standard, puoi utilizzare i nostri SDK Mobile per le attività di test A/B e Targeting delle esperienze (XT). Se desiderate utilizzare le funzionalità di Recommendations o AI nell'app mobile, dovete disporre di [una licenza Adobe Target Premium](/help/c-intro/intro.md#premium) .

## Posso sfruttare i tipi di pubblico di Adobe Audience Manager (AAM) nel VEC per app mobili?

Sì, gli SDK mobile della piattaforma Adobe Experience Platform sono creati per [Audience Manager](https://docs.adobe.com/content/help/en/audience-manager/user-guide/aam-home.html), [Analytics](https://docs.adobe.com/content/help/en/analytics/landing/home.html), [Campaign](https://docs.adobe.com/content/help/en/campaign-standard/using/campaign-standard-home.html)e Target. I tuoi tipi di pubblico in Audience Manager sono condivisi [!DNL Target].

## Esiste un'integrazione con app mobili tra le attività di Mobile Adobe Experience Manager (AEM) e Target?

È nella nostra roadmap, ma non c'è ancora una timeline. Al momento, puoi condividere i frammenti [esperienza JSON](/help/c-experiences/c-manage-content/aem-experience-fragments.md) da AEM a Target e quindi utilizzarli in un'attività app mobile.

## È possibile aggiungere altre immagini utilizzando l'aula virtuale o modificare solo le immagini esistenti?

Al momento potete modificare solo le immagini esistenti.
