---
keywords: Real-time Customer Data Platform;rtcdp;personalizzazione;pubblico aep;pubblico adobe experience platform;attributi di profilo
description: Scopri come utilizzare l’integrazione  [!DNL Target]/[!DNL Real-time Customer Data Platform]  (RTCDP) per fornire dati più ricchi sui clienti e una personalizzazione di maggior impatto.
title: Come posso integrare  [!DNL Target]  con  [!DNL Real-time Customer Data Platform]?
feature: Integrations
exl-id: 1c066b62-91a2-4b8c-807a-3cc56fca7778
source-git-commit: 22dc0d43f64d927028b2d7a44f1bd983e2f669d3
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 17%

---

# Integra con [!DNL Real-time Customer Data Platform]

Costruita su [!DNL Adobe Experience Platform], [!DNL Real-time Customer Data Platform] (RTCDP) aiuta le aziende a riunire dati noti e non noti provenienti da più fonti aziendali per creare profili di clienti che possono essere utilizzati per fornire esperienze personalizzate ai clienti su tutti i canali e i dispositivi in tempo reale.

Per ulteriori informazioni su RTCDP, consulta [Panoramica di Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=it){target=_blank}.

## Utilizzare i tipi di pubblico da [!DNL Adobe Experience Platform] {#aep}

Utilizzo [pubblico](/help/main/c-target/c-audiences/audiences.md) creato in [!DNL Adobe Experience Platform] forniscono dati più ricchi sui clienti che consentono una personalizzazione più incisiva. La [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=it){target=_blank} (RTCDP), basato su [!DNL Adobe Experience Platform], consente alle aziende di unire dati noti e anonimi provenienti da più origini aziendali. Questo processo ti consente di creare profili cliente da utilizzare in tempo reale per fornire esperienze cliente personalizzate su tutti i canali e dispositivi.

Tramite la connessione di [!DNL Target] al [!DNL Real-time Customer Data Platform], i clienti possono arricchire la personalizzazione Web sbloccando nuovi segmenti che in precedenza potevano essere inaccessibili a [!DNL Target] per abilitare la personalizzazione in tempo reale di millisecondi nella prima pagina della visita Web di un cliente. Utilizzo di tipi di pubblico e attributi di profilo creati in [!DNL Adobe Experience Platform] ti consente di espandere i punti dati disponibili per una personalizzazione più ricca.

Questa integrazione sblocca i casi d’uso chiave con Real-time CDP:

* Personalizzazione a pagina singola/hit successivo
* Personalizzazione di utenti sconosciuti/nuovi

### Funzioni principali

Le caratteristiche principali includono:

* Diretta [!DNL Target] integrazione con Real-time CDP/[!DNL Adobe Experience Platform] sul bordo (rimozione della dipendenza da [!DNL Audience Core services] - AAM)
* [!UICONTROL Scheda Destinazioni Edge di Target] con governance e applicazione delle politiche
* Segmenti CDP in tempo reale e attributi di profilo condivisi

### Casi di utilizzo della personalizzazione

La tabella seguente mostra quale tipo di caso d’uso per la personalizzazione (sessione successiva o pagina stessa) è disponibile quando si utilizza il [!DNL Adobe Experience Platform Web SDK] rispetto all’utilizzo di at.js:

| Implementazione | Soluzioni/Caso d’uso abilitato |
| --- | --- |
| at.js | **Soluzioni**:<ul><li>[!DNL Adobe Audience Manager] (AAM) e [!DNL Target]</li><li>[!DNL RTCDP] (Premium o Ultimate) e [!DNL Target]</li><li>[!DNL RTCDP] (qualsiasi SKU), [!DNL AAM]e [!DNL Target]</li></ul>**Caso d’uso**:<ul><li>Personalizzazione di sessioni successive</li></ul> |
| [!DNL Platform Web SDK] o [!DNL AEP Server-Side API] | **Soluzioni**:<ul><li>[!DNL RTCDP] (qualsiasi SKU) e [!DNL Target]</li></ul>**Caso d’uso**:<ul><li>Personalizzazione di sessioni successive</li><li>Personalizzazione tramite pagina singola tramite Edge</li><li>Governance applicata durante la condivisione dei segmenti</li></ul>**Soluzioni**:<ul><li>[!DNL RTCDP] (qualsiasi SKU), [!DNL AAM]e [!DNL Target]</li></ul>**Caso d’uso**:<ul><li>Personalizzazione di sessioni successive</li><ul><li>[!DNL AAM] segmenti</li><li>Segmenti di terze parti tramite [!DNL AAM]</li></ul><li>Personalizzazione tramite pagina singola tramite Edge</li><ul><li>[!DNL RTCDP] segmenti</li><li>Governance applicata durante la condivisione dei segmenti</li></ul> |
| Miscela di [!UICONTROL at.js] e [!DNL Platform Web SDK] | **Soluzioni**:<ul><li>[!DNL RTCDP] (qualsiasi SKU) e [!DNL Target]</li></ul>**Caso d’uso**:<ul><li>Personalizzazione di sessioni successive</li><ul><li>Per tutte le pagine con [!UICONTROL at.js]</li></ul><li>Personalizzazione a pagina singola</li><ul><li>Per tutte le pagine con [!DNL Platform Web SDK]</li></ul></ul>**Soluzioni**:<ul><li>[!DNL RTCDP] (qualsiasi SKU), [!DNL AAM]e [!DNL Target]</li></ul>**Caso d’uso**:<ul><li>Personalizzazione di sessioni successive</li><ul><li>Per tutte le pagine con [!UICONTROL at.js]</li><li>[!DNL AAM] segmenti</li><li>Segmenti di terze parti tramite [!DNL AAM]</li></ul> |

### Tempo di valutazione del segmento

La tabella seguente mostra il tempo di valutazione dei segmenti per gli eventi provenienti da diversi scenari di implementazione:

| Scenario | Segmento perimetrale (valutazione in millisecondi) | Segmento in streaming (valutazione dei minuti) | Valutazione dei segmenti in batch |
| --- | --- | --- | --- |
| Eventi/dati da [!DNL Adobe Experience Platform] SDK | Sì | Sì | N/D |
| Eventi da [!UICONTROL at.js] | No | Sì | N/D |
| Eventi da [!DNL Target Mobile] SDK | No | Sì | N/D |
| Eventi da caricamento batch | No | No | Sì |
| Eventi da dati offline (streaming) | No | Sì | Sì |

### Collegamenti per ulteriori informazioni

Per maggiori informazioni, vedi i seguenti argomenti:

* [Note sulla versione delle destinazioni](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=en#destinations){target=_blank} in *Note sulla versione di Adobe Experience Platform*
* [Configurare le destinazioni di personalizzazione per la personalizzazione della stessa pagina e della pagina successiva](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html){target=_blank} in *Panoramica sulle destinazioni* guida.
* [Connessione di personalizzazione personalizzata](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html){target=_blank} in *Panoramica sulle destinazioni* guida
* [Connessione Adobe Target](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection.html){target=_blank} in *Panoramica sulle destinazioni* guida
* [Configurare le destinazioni di personalizzazione per la stessa pagina e i casi d’uso di personalizzazione della pagina successivi](https://www.adobe.com/go/destinations-edge-personalization-en){target=_blank} in *Panoramica sulle destinazioni* guida

## Condividere gli attributi del profilo CDP in tempo reale con [!DNL Target] {#rtcdp-profile-attributes}

Gli attributi del profilo CDP in tempo reale possono essere condivisi con [!DNL Target] da utilizzare nelle offerte HTML e [Offerte JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md).

### Limitazioni e considerazioni sulle funzioni degli attributi di profilo CDP in tempo reale

>[!NOTE]
>
>La funzione Attributi del profilo CDP in tempo reale è attualmente disponibile in versione beta per le offerte HTML e [Offerte JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md).

Considera i seguenti aspetti:

* Gli attributi all’interno di una determinata offerta devono provenire dalla stessa Sandbox AEP. In altre parole, un’offerta non può contenere attributi di diverse Sandbox AEP.
* Gli attributi all&#39;interno di una data offerta possono provenire da fonti diverse; vale a dire [!DNL Target] profilo e profilo AEP. (In altre parole, è possibile combinare gli attributi indipendentemente dal fatto che provengano da [!DNL Target] o dal profilo AEP.)
* Quando definisci un’offerta, puoi assegnare valori predefiniti per gli attributi del profilo CDP in tempo reale, nel caso in cui l’attributo non abbia un valore esplicito. Ad esempio, se un criterio di consenso o governance blocca l’attributo utilizzato nel servizio di personalizzazione, è possibile utilizzare il valore predefinito.
* Quando vengono condivisi, gli attributi del profilo CDP in tempo reale vengono utilizzati nei modelli di personalizzazione intelligenza artificiale/apprendimento automatico per [!UICONTROL Targeting automatico] e [!UICONTROL Automated Personalization] attività.

### Caso di utilizzo di esempio

In qualità di esperto di marketing online, desideri che AEP/Unified Profile condivida i valori degli attributi con [!DNL Target] per fornire personalizzazione in tempo reale. Utilizzando gli attributi del profilo CDP in tempo reale, puoi visualizzare il valore dell’attributo AEP in un [!DNL Target] offerta con sostituzione token. Ad esempio, puoi personalizzare in base al colore preferito di un cliente utilizzando `${aep.profile.favoriteColor}`, o il livello fedeltà e il valore del punto fedeltà utilizzando i token `${aep.loyalty.tier}` e `${aep.loyalty.points}`.

![immagine offer-json-aep-shared-attribute](/help/main/c-experiences/c-manage-content/assets/offer-json-aep-shared-attribute.png)

L’assegnazione di valori predefiniti è facoltativa.

## Video e post di blog

I video e i post di blog seguenti forniscono ulteriori informazioni sulla personalizzazione avanzata con Target e RTCDP:

### Video: Personalizzazione con hit successivo con Real-time CDP e [!DNL Adobe Target]{#RTCDP}

Scopri come personalizzare l’hit successivo con [!DNL Real-time Customer Data Platform] e [!DNL Adobe Target]. La [!DNL Adobe Target] destinazione [!DNL Real-time CDP] consente di utilizzare [!DNL Experience Platform] segmenti in [!DNL Adobe Target] per la stessa personalizzazione della pagina e la personalizzazione della pagina successiva con governance e supporto per la privacy.

Per ulteriori informazioni, consulta [Personalizzazione con hit successivo con Real-time CDP e Adobe Target](https://experienceleague.adobe.com/docs/platform-learn/tutorials/experience-cloud/next-hit-personalization.html){target=_blank} in *Tutorials piattaforma* guida.

>[!VIDEO](https://video.tv.adobe.com/v/340091?quality=12&learn=on)

### Blog e video di Adobe Target:

[[!DNL Adobe] announces Same Page Enhanced Personalization with [!DNL Adobe Target] e [!DNL Real-time Customer Data Platform]](https://blog.adobe.com/en/publish/2021/10/05/adobe-announces-same-page-enhanced-personalization-with-adobe-target-real-time-customer-data-platform){target=_blank}
