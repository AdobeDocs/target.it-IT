---
description: Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per i prossimi o imminenti [! DNL Adobe Target].
keywords: note sulla versione
seo-description: Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per i prossimi o imminenti [! DNL Adobe Target].
seo-title: Note di rilascio di Adobe Target (prerelease)
solution: Target
title: Note sulla versione di Target (prerelease)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 7cdff6e1beca45a4900090bc91a38be7e000f289

---


# Note sulla versione di Target (prerelease){#target-release-notes-prerelease}

Queste note sulla versione contengono informazioni su funzioni, miglioramenti e correzioni per le versioni più recenti o in arrivo di [!DNL Adobe Target].

**Ultimo aggiornamento: 11 luglio 2019**

>[!NOTE]
>
>Queste note sulla versione contengono delle informazioni in anteprima. Le date di rilascio, le funzioni e altre informazioni sono soggette a modifiche senza preavviso. Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali o possono essere diverse, a seconda della tempistica delle release.
>
>The issue numbers in parentheses are for internal [!DNL Adobe] use.

## Target Standard/Premium 19.7.1 (23 luglio 2019) {#tgt-19-7-1}

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Funzione / Miglioramento | Descrizione |
| --- | --- |
| Compositore esperienza visivo | When you click an image then click [!UICONTROL Replace With], two new options display:<ul><li>**HTML**: Potete sostituire un&#39;immagine con HTML per fornire un controllo completo dell&#39;elemento senza necessità di selezionare l&#39;elemento principale per accedere all&#39;opzione HTML.</li><li>**Frammento esperienza**: Puoi sostituire un&#39;immagine con un frammento [esperienza di Adobe Experience Manager (AEM)](/help/c-experiences/c-manage-content/aem-experience-fragments.md) per inserire rapidamente gli elementi creati in AEM in attività Target.</li></ul>(TGT-34097) |
| Compositore esperienza visivo per app mobile | Nella VEC App mobile viene visualizzato un nuovo pannello Modifiche che mostra gli elementi configurati per il tracciamento dei clic. (TGT-31741) |
| ![Premium badgerecommendations](/help/assets/premium.png)<br>in A/B Testing and Experience Targeting (XT) attività | Lo stato Offer Offer (algoritmo) di Recommendations viene visualizzato nella pagina Overview (Panoramica) per le attività A/B Test and XT che contengono Recommendations offerte. Gli stati includono: Risultati pronti, Risultati non pronti e Feed di feed. (TGT-33649) |
| Supporto di monitoraggio tra più domini per at. js 2.0 + tramite la libreria Experience Cloud ID (ECID) | In precedenza, il monitoraggio tra domini non era supportato in at. js 2.*x*. Con questa release, i clienti che usano at. js 2.0 o versioni successive possono ora utilizzare il tracciamento tra domini attraverso la libreria ECID. Affinché il tracciamento interdominio funzioni, la libreria ECID deve essere installata sulla pagina insieme a. js 2.0 o versione successiva. [È](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-release-notes.html) necessario utilizzare la libreria Experience Cloud ID 4.3.0 +. |
| Supporto di Target per ITP 2.1 e ITP 2.2 di Apple tramite la libreria Experience Cloud ID (ECID) 4.3 | Oggi, i clienti di Target possono attenuare ITP 2.1 e ITP 2.2 Apple sfruttando il programma di certificazione CNAME di Adobe. With this release, Target introduces a seamless integration with the ECID library 4.3, which leverages a server-side cookie to mitigate ITP 2.1 and ITP 2.2. It is highly recommended that Target customers deploy [ECID library 4.3+](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-release-notes.html) in conjunction with Target’s JavaScript library to mitigate any future ITP releases. La libreria ECID continuerà a presentare miglioramenti che offrono una soluzione solida ai criteri di cookie in continua evoluzione introdotti dai browser. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
