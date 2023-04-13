---
keywords: Real-time Customer Data Platform;rtcdp;personalizzazione;pubblico aep;pubblico adobe experience platform;attributi di profilo
description: Scopri come utilizzare l’integrazione  [!DNL Target]/[!DNL Real-Time Customer Data Platform]  (RTCDP) per fornire dati più ricchi sui clienti e una personalizzazione di maggior impatto.
title: Come posso integrare  [!DNL Target]  con  [!DNL Real-Time Customer Data Platform]?
feature: Integrations
exl-id: 1c066b62-91a2-4b8c-807a-3cc56fca7778
source-git-commit: 08422323607f7238a7cf9bac5b863032ce734662
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 8%

---

# Integra con [!DNL Real-Time Customer Data Platform]

Incorporato [!DNL Adobe Experience Platform], [!DNL Real-Time Customer Data Platform] (RTCDP) consente alle aziende di riunire dati noti e anonimi provenienti da più origini aziendali. RTCDP consente di creare profili cliente da utilizzare in tempo reale per fornire esperienze cliente personalizzate per tutti i canali e i dispositivi.

Per ulteriori informazioni su RTCDP, consulta [Panoramica di Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=it){target=_blank}.

## Funzioni principali

Le caratteristiche principali includono:

* Diretta [!DNL Target] integrazione con Real-Time CDP/[!DNL Adobe Experience Platform] sul bordo (rimozione della dipendenza da [!DNL Audience Core services] - AAM)
* [!UICONTROL Scheda Destinazioni Edge di Target] con governance e applicazione delle politiche
* Segmenti CDP in tempo reale e attributi di profilo condivisi

## Scenari di implementazione

Le sezioni seguenti mostrano quale tipo di caso d’uso per la personalizzazione (sessione successiva o pagina stessa) è disponibile quando si utilizzano metodi di implementazione diversi:

### Implementazione di at.js

| Soluzioni | Caso d’uso abilitato |
| --- | --- |
| <ul><li>[!DNL Adobe Audience Manager] (AAM) e [!DNL Target]</li><li>[!DNL RTCDP] (Premium o Ultimate) e [!DNL Target]</li><li>[!DNL RTCDP] (qualsiasi SKU), [!DNL AAM]e [!DNL Target]</li></ul> | Personalizzazione di sessioni successive |

### [!DNL Adobe Experience Platform Web SDK] o [!DNL Experience Platform Server-Side API] implementazione

| Soluzioni | Caso d’uso abilitato |
| --- | --- |
| <ul><li>[!DNL RTCDP] (qualsiasi SKU) e [!DNL Target]</li></ul> | <ul><li>Personalizzazione di sessioni successive</li><li>Personalizzazione tramite pagina singola tramite Edge</li><li>Governance applicata durante la condivisione dei segmenti</li></ul> |
| <ul><li>[!DNL RTCDP] (qualsiasi SKU), [!DNL AAM]e [!DNL Target]</li></ul> | <ul><li>Personalizzazione di sessioni successive</li><ul><li>[!DNL AAM] segmenti</li><li>Segmenti di terze parti tramite [!DNL AAM]</li></ul><li>Personalizzazione tramite pagina singola tramite Edge</li><ul><li>[!DNL RTCDP] segmenti</li><li>Governance applicata durante la condivisione dei segmenti</li></ul> |

### Miscela di [!UICONTROL at.js] e [!DNL Platform Web SDK] implementazione

| Soluzioni | Caso d’uso abilitato |
| --- | --- |
| <ul><li>[!DNL RTCDP] (qualsiasi SKU) e [!DNL Target]</li></ul> | <ul><li>Personalizzazione di sessioni successive</li><ul><li>Per tutte le pagine con [!UICONTROL at.js]</li></ul><li>Personalizzazione a pagina singola</li><ul><li>Per tutte le pagine con [!DNL Platform Web SDK]</li></ul> |
| <ul><li>[!DNL RTCDP] (qualsiasi SKU), [!DNL AAM]e [!DNL Target]</li></ul> | <ul><li>Personalizzazione di sessioni successive</li><ul><li>Per tutte le pagine con [!UICONTROL at.js]</li><li>[!DNL AAM] segmenti</li><li>Segmenti di terze parti tramite [!DNL AAM]</li></ul> |

## Tempo di valutazione del segmento

La tabella seguente mostra il tempo di valutazione dei segmenti per gli eventi provenienti da diversi scenari di implementazione:

| Scenario | Segmento perimetrale (valutazione in millisecondi) | Segmento in streaming (valutazione dei minuti) | Valutazione dei segmenti in batch |
| --- | --- | --- | --- |
| Eventi/dati da [!DNL Adobe Experience Platform] SDK | Sì | Sì | N/D |
| Eventi da [!UICONTROL at.js] | No | Sì | N/D |
| Eventi da [!DNL Target Mobile] SDK | No | Sì | N/D |
| Eventi da caricamento batch | No | No | Sì |
| Eventi da dati offline (streaming) | No | Sì | Sì |

## Utilizzare i tipi di pubblico da [!DNL Adobe Experience Platform] {#aep}

Utilizzo [pubblico](/help/main/c-target/c-audiences/audiences.md) creato in [!DNL Adobe Experience Platform] forniscono dati più ricchi sui clienti che consentono una personalizzazione più incisiva. La [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=it){target=_blank} (RTCDP), basato su [!DNL Adobe Experience Platform], consente alle aziende di unire dati noti e anonimi provenienti da più origini aziendali. Questo processo ti consente di creare profili cliente da utilizzare in tempo reale per fornire esperienze cliente personalizzate su tutti i canali e dispositivi.

Collegamento [!DNL Target] al [!DNL Real-Time Customer Data Platform], i clienti possono arricchire la loro personalizzazione web. Questa integrazione consente di sbloccare nuovi segmenti che potrebbero essere stati precedentemente inaccessibili a [!DNL Target] per abilitare la personalizzazione in tempo reale di millisecondi nella prima pagina della visita web di un cliente. Utilizzo di tipi di pubblico e attributi di profilo creati in [!DNL Adobe Experience Platform] ti consente di espandere i punti dati disponibili per una personalizzazione più ricca.

Questa integrazione sblocca i casi d’uso chiave con Real-Time CDP:

* Personalizzazione a pagina singola/hit successivo
* Personalizzazione di utenti sconosciuti/nuovi

## Condividere gli attributi del profilo Real-Time CDP con [!DNL Target] {#rtcdp-profile-attributes}

Gli attributi del profilo Real-Time CDP possono essere condivisi con [!DNL Target] da utilizzare nelle offerte HTML e [Offerte JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md).

### Limitazioni e considerazioni delle funzioni Attributi del profilo di Real-Time CDP

>[!NOTE]
>
>La funzione Attributi del profilo Real-Time CDP è disponibile in versione beta per le offerte di HTML e [Offerte JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md).

Considera i seguenti aspetti:

* Gli attributi all’interno di una determinata offerta devono provenire dalla stessa [!UICONTROL Experience Platform] sandbox. (In altre parole, un&#39;offerta non può contenere attributi di diversi [!UICONTROL Experience Platform] sandbox.)
* Gli attributi all’interno di una data offerta possono provenire da fonti diverse; vale a dire [!DNL Target] il profilo e [!UICONTROL Experience Platform] profilo. (In altre parole, è possibile combinare gli attributi indipendentemente dal fatto che provengano da [!DNL Target] o dal [!UICONTROL Experience Platform] profilo).
* Quando definisci un’offerta, puoi assegnare valori predefiniti per [!UICONTROL Attributi del profilo di Real-Time CDP], nel caso in cui l&#39;attributo non abbia un valore esplicito. Ad esempio, se un criterio di consenso o governance blocca l’attributo utilizzato nel servizio di personalizzazione, è possibile utilizzare il valore predefinito.

### Caso di utilizzo di esempio JSON

In qualità di esperto di marketing online, desideri che AEP/Unified Profile condivida i valori degli attributi con [!DNL Target] per fornire personalizzazione in tempo reale. Utilizzando [!UICONTROL Attributi del profilo di Real-Time CDP], puoi visualizzare il valore della [!UICONTROL Experience Platform] in un [!DNL Target] offerta con sostituzione token. Ad esempio, puoi personalizzare in base al colore preferito di un cliente utilizzando `${aep.profile.favoriteColor}`, o il livello fedeltà e il valore del punto fedeltà utilizzando i token `${aep.loyalty.tier}` e `${aep.loyalty.points}`.

Per creare un’offerta JSON per condividere gli attributi del profilo AEP/Unified con [!DNL Target]:

1. Quando [creazione di un’offerta JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md), dal **[!UICONTROL Selezionare un&#39;origine]** elenco, selezionare **[!UICONTROL Adobe Experience Platform]**.
1. Da **[!UICONTROL Selezionare un nome di sandbox di profilo]** seleziona la sandbox desiderata.
1. Da **[!UICONTROL Selezionare un attributo di profilo]** seleziona gli attributi desiderati.
1. (Facoltativo) Dal **[!UICONTROL Inserisci un valore predefinito]** seleziona i valori desiderati.
1. Fai clic su **[!UICONTROL Aggiungi]**.

L’illustrazione seguente mostra due attributi di profilo: `loyalty.tier` e `loyalty.points` sono stati aggiunti all’offerta JSON.

![immagine offer-json-aep-shared-attribute](/help/main/c-experiences/c-manage-content/assets/offer-json-aep-shared-attribute.png)

## Collegamenti per ulteriori informazioni

Per maggiori informazioni, vedi i seguenti argomenti:

* [Note sulla versione delle destinazioni](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=en#destinations){target=_blank} in *Note sulla versione di Adobe Experience Platform*
* [Configurare le destinazioni di personalizzazione per la personalizzazione della stessa pagina e della pagina successiva](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html){target=_blank} in *Panoramica sulle destinazioni* guida.
* [Connessione Adobe Target](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection.html){target=_blank} in *Panoramica sulle destinazioni* guida
* [Attributi mappa](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-profile-request-destinations.html?lang=en#map-attributes){target=_blank} in *Panoramica sulle destinazioni* guida.

## Video e post di blog

I video e i post di blog seguenti forniscono ulteriori informazioni sulla personalizzazione avanzata con Target e RTCDP:

### Video: Personalizzazione con hit successivo con Real-Time CDP e [!DNL Adobe Target]{#RTCDP}

Scopri come personalizzare l’hit successivo con [!DNL Real-Time Customer Data Platform] e [!DNL Adobe Target]. La [!DNL Adobe Target] destinazione [!DNL Real-Time CDP] consente di utilizzare [!DNL Experience Platform] segmenti in [!DNL Adobe Target] per la stessa personalizzazione della pagina e la personalizzazione della pagina successiva con governance e supporto per la privacy.

Per ulteriori informazioni, consulta [Personalizzazione con hit successivo con Real-Time CDP e Adobe Target](https://experienceleague.adobe.com/docs/platform-learn/tutorials/experience-cloud/next-hit-personalization.html){target=_blank} in *Tutorials piattaforma* guida.

>[!VIDEO](https://video.tv.adobe.com/v/340091?quality=12&learn=on)

### [!DNL Adobe Target] blog e video: Personalizzazione avanzata a pagina singola

[[!DNL Adobe] announces Same-Page Enhanced Personalization with [!DNL Adobe Target] e [!DNL Real-time Customer Data Platform]](https://blog.adobe.com/en/publish/2021/10/05/adobe-announces-same-page-enhanced-personalization-with-adobe-target-real-time-customer-data-platform){target=_blank}
