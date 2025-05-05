---
keywords: Real-time Customer Data Platform;rtcdp;personalizzazione;tipi di pubblico aep;tipi di pubblico di adobe experience platform;attributi del profilo
description: Scopri come utilizzare l’integrazione  [!DNL Target]/[!DNL Real-Time Customer Data Platform]  (RTCDP) per fornire dati più ricchi sui clienti e una personalizzazione di maggior impatto.
title: Come posso integrare  [!DNL Target]  con  [!DNL Real-Time Customer Data Platform]?
feature: Integrations
exl-id: 1c066b62-91a2-4b8c-807a-3cc56fca7778
source-git-commit: 4104b6cb67347205c0143c9dea46dd483a8266ce
workflow-type: tm+mt
source-wordcount: '975'
ht-degree: 71%

---

# Integrare con [!DNL Real-Time Customer Data Platform]

Basato su [!DNL Adobe Experience Platform], [!DNL Real-Time Customer Data Platform] (RTCDP) consente alle aziende di riunire dati noti e anonimi provenienti da più origini aziendali. RTCDP consente di creare profili cliente da utilizzare per fornire ai clienti esperienze personalizzate in tempo reale su tutti i canali e i dispositivi.

Per ulteriori informazioni su RTCDP, vedere [Panoramica di Real-Time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=it){target=_blank}.

## Funzioni chiave

Le funzioni chiave includono:

* Integrazione diretta con [!DNL Target] tramite Real-Time CDP/[!DNL Adobe Experience Platform] in Edge (rimuovendo la dipendenza da [!DNL Audience Core services] - AAM)
* [!UICONTROL Target Edge Destinations Card] con governance e applicazione dei criteri
* Segmenti Real-Time CDP e attributi di profilo condivisi

## Scenari di implementazione

Le sezioni seguenti illustrano quale tipo di caso d’uso di personalizzazione (sessione successiva o stessa pagina) è disponibile quando si utilizzano metodi di implementazione diversi:

### Implementazione di at.js

| Soluzioni | Caso d’uso abilitato |
| --- | --- |
| <ul><li>[!DNL Adobe Audience Manager] (AAM) e [!DNL Target]</li><li>[!DNL RTCDP] (Premium o Ultimate) e [!DNL Target]</li><li>[!DNL RTCDP] (qualsiasi SKU), [!DNL AAM] e [!DNL Target]</li></ul> | Personalizzazione sessione successiva |

### Implementazione di [!DNL Adobe Experience Platform Web SDK] o di [!DNL Experience Platform Server-Side API]

| Soluzioni | Caso d’uso abilitato |
| --- | --- |
| <ul><li>[!DNL RTCDP] (qualsiasi SKU) e [!DNL Target]</li></ul> | <ul><li>Personalizzazione sessione successiva</li><li>Personalizzazione stessa pagina tramite Edge</li><li>Governance applicata durante la condivisione dei segmenti</li></ul> |
| <ul><li>[!DNL RTCDP] (qualsiasi SKU), [!DNL AAM] e [!DNL Target]</li></ul> | <ul><li>Personalizzazione sessione successiva</li><ul><li>Segmenti [!DNL AAM]</li><li>Segmenti di terze parti tramite [!DNL AAM]</li></ul><li>Personalizzazione stessa pagina tramite Edge</li><ul><li>Segmenti [!DNL RTCDP]</li><li>Governance applicata durante la condivisione dei segmenti</li></ul> |

### Combinazione di implementazione [!UICONTROL at.js] e [!DNL Platform Web SDK]

| Soluzioni | Caso d’uso abilitato |
| --- | --- |
| <ul><li>[!DNL RTCDP] (qualsiasi SKU) e [!DNL Target]</li></ul> | <ul><li>Personalizzazione sessione successiva</li><ul><li>Per tutte le pagine con [!UICONTROL at.js]</li></ul><li>Personalizzazione stessa pagina</li><ul><li>Per tutte le pagine con [!DNL Platform Web SDK]</li></ul> |
| <ul><li>[!DNL RTCDP] (qualsiasi SKU), [!DNL AAM] e [!DNL Target]</li></ul> | <ul><li>Personalizzazione sessione successiva</li><ul><li>Per tutte le pagine con [!UICONTROL at.js]</li><li>Segmenti [!DNL AAM]</li><li>Segmenti di terze parti tramite [!DNL AAM]</li></ul> |

## Tempo di valutazione del segmento

La tabella seguente mostra il tempo di valutazione dei segmenti per gli eventi provenienti da diversi scenari di implementazione:

| Scenario | Segmento Edge (valutazione in millisecondi) | Segmento in streaming (valutazione in minuti) | Valutazione dei segmenti in batch |
| --- | --- | --- | --- |
| Eventi/dati da SDK di [!DNL Adobe Experience Platform] | Sì | Sì | N/D |
| Eventi da [!UICONTROL at.js] | No | Sì | N/D |
| Eventi da SDK di [!DNL Target Mobile] | No | Sì | N/D |
| Eventi da caricamento in batch | No | No | Sì |
| Eventi da dati offline (flusso) | No | Sì | Sì |

## Utilizzo dei tipi di pubblico da [!DNL Adobe Experience Platform] {#aep}

L’utilizzo dei [tipi di pubblico](/help/main/c-target/c-audiences/audiences.md) creati in [!DNL Adobe Experience Platform] fornisce dati più completi sui clienti, per una personalizzazione più incisiva. [Real-Time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=it){target=_blank} (RTCDP), basato su [!DNL Adobe Experience Platform], consente alle aziende di unire dati noti e anonimi provenienti da più origini aziendali. Questo processo consente di creare profili cliente da utilizzare per fornire ai clienti esperienze personalizzate in tempo reale su tutti i canali e i dispositivi.

Collegando [!DNL Target] a [!DNL Real-Time Customer Data Platform], i clienti possono arricchire la loro personalizzazione web. Questa integrazione consente di sbloccare nuovi segmenti che potrebbero essere stati precedentemente inaccessibili a [!DNL Target] per abilitare la personalizzazione dei millisecondi in tempo reale nella prima pagina della visita web di un cliente. L’utilizzo dei tipi di pubblico e degli attributi di profilo creati in [!DNL Adobe Experience Platform] consente di espandere i punti dati disponibili per una personalizzazione più completa.

Questa integrazione sblocca i casi d’uso chiave con Real-Time CDP:

* Personalizzazione stessa pagina/hit successivo
* Personalizzazione utenti nuovi/sconosciuti

## Condividere gli attributi di profilo Real-Time CDP con [!DNL Target] {#rtcdp-profile-attributes}

Gli attributi di profilo Real-Time CDP possono essere condivisi con [!DNL Target] per l’utilizzo nelle offerte HTML e [JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md).

### Limitazioni e considerazioni sulle funzioni degli attributi di profilo di Real-Time CDP {#limitations}

Considera i seguenti aspetti:

* Gli attributi all&#39;interno di una determinata offerta devono appartenere alla stessa sandbox [!UICONTROL Experience Platform]. In altre parole, un&#39;offerta non può contenere attributi di sandbox [!UICONTROL Experience Platform] diverse.
* Gli attributi all&#39;interno di una determinata offerta possono provenire da origini diverse, ovvero il profilo [!DNL Target] e il profilo [!UICONTROL Experience Platform]. In altre parole, è possibile combinare gli attributi provenienti da [!DNL Target] o dal profilo [!UICONTROL Experience Platform].
* Quando definisci un&#39;offerta, puoi assegnare valori predefiniti per [!UICONTROL Real-Time CDP Profile Attributes], nel caso in cui l&#39;attributo non abbia un valore esplicito. Ad esempio, se un criterio di consenso o governance blocca l’attributo utilizzato nel servizio di personalizzazione, è possibile utilizzare il valore predefinito.
* [!DNL Target] supporta solo il tipo di dati &quot;stringa&quot; per gli attributi di profilo [!DNL Adobe Experience Platform] da utilizzare nelle offerte. Gli attributi di tipo &quot;Map&quot; e &quot;Array&quot; non sono ancora supportati.

### Caso d’uso di esempio JSON

In qualità di addetto marketing online, desideri che AEP/Profilo unificato condivida i valori degli attributi con [!DNL Target] per fornire personalizzazione in tempo reale. Utilizzando [!UICONTROL Real-Time CDP Profile Attributes], è possibile visualizzare il valore dell&#39;attributo [!UICONTROL Experience Platform] in un&#39;offerta [!DNL Target] utilizzando la sostituzione del token. Ad esempio, puoi effettuare una personalizzazione in base al colore preferito di un cliente utilizzando `${aep.profile.favoriteColor}`, o il livello di fidelizzazione e il valore del punto fedeltà utilizzando i token `${aep.loyalty.tier}` e `${aep.loyalty.points}`.

Per creare un’offerta JSON per condividere gli attributi AEP/Profilo unificato con [!DNL Target]:

1. Durante la [creazione di un&#39;offerta JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md), dall&#39;elenco **[!UICONTROL Select a source]**, selezionare **[!UICONTROL Adobe Experience Platform]**.
1. Dall&#39;elenco **[!UICONTROL Select a profile sandbox name]**, selezionare la sandbox desiderata.
1. Dall&#39;elenco **[!UICONTROL Select a profile attribute]**, selezionare gli attributi desiderati.
1. (Facoltativo) Dall&#39;elenco **[!UICONTROL Insert a default value]**, selezionare i valori desiderati.
1. Fare clic su **[!UICONTROL Add]**.

L’illustrazione seguente mostra che due attributi di profilo, `loyalty.tier` e `loyalty.points`, sono stati aggiunti all’offerta JSON.

![immagine offer-json-aep-shared-attribute](/help/main/c-experiences/c-manage-content/assets/offer-json-aep-shared-attribute.png)

## Collegamenti per ulteriori informazioni

Per ulteriori informazioni, consulta i seguenti argomenti:

* [Note sulla versione delle destinazioni](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it#destinations){target=_blank} nelle *Note sulla versione di Adobe Experience Platform*
* [Configurare le destinazioni di personalizzazione per la personalizzazione della stessa pagina e della pagina successiva](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html?lang=it){target=_blank} nella *Panoramica sulle destinazioni*.
* [Connessione Adobe Target](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection.html?lang=it){target=_blank} nella guida *Panoramica sulle destinazioni*
* [Mappa gli attributi](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-profile-request-destinations.html?lang=it#map-attributes){target=_blank} nella guida *Panoramica sulle destinazioni*.
* [Attiva i tipi di pubblico nelle destinazioni di personalizzazione Edge](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html?lang=it){target=_blank} nella guida *Panoramica sulle destinazioni*.
* [Personalizzazione della stessa pagina e della pagina successiva tramite le destinazioni di Personalization [!DNL Adobe Target] e personalizzate](https://experienceleague.adobe.com/docs/experience-platform/destinations/destinations-faq.html?lang=it#same-next-page-personalization){target=_blank} nella sezione &quot;Domande frequenti&quot; nella *Panoramica sulle destinazioni*.

## Video e post del blog {#videos-blogs}

I video e i post del blog seguenti forniscono ulteriori informazioni sulla personalizzazione avanzata con Target e RTCDP:

### Video: Personalizzazione hit successivo con Real-Time CDP e [!DNL Adobe Target]{#RTCDP}

Scopri come personalizzare l’hit successivo con [!DNL Real-Time Customer Data Platform] e [!DNL Adobe Target]. La destinazione di [!DNL Adobe Target] in [!DNL Real-Time CDP] consente di utilizzare i segmenti di [!DNL Experience Platform] in [!DNL Adobe Target] per le personalizzazioni stessa pagina e pagina successiva con governance e supporto per la privacy.

Per ulteriori informazioni, consulta [Personalizzazione dell&#39;hit successivo con Real-Time CDP e Adobe Target](https://experienceleague.adobe.com/docs/platform-learn/tutorials/experience-cloud/next-hit-personalization.html?lang=it){target=_blank} nella *Guida ai tutorial su Platform*.

>[!VIDEO](https://video.tv.adobe.com/v/340091?quality=12&learn=on)

### Video: configurare la destinazione [!DNL Adobe Target] in [!DNL Real-Time Customer Data Platform]

Scopri come configurare la destinazione [!DNL Adobe Target] in [!DNL Real-Time Customer Data Platform] per iniziare a inviare segmenti e attributi di profilo da [!DNL Real-Time CDP] a [!DNL Target].

>[!VIDEO](https://video.tv.adobe.com/v/3449801/?learn=on&captions=ita)

### Video: attivare segmenti e attributi di profilo

Scopri come attivare segmenti e attributi di profilo da [!DNL Adobe Real-Time Customer Data Platform] a [!DNL Adobe Target] per visualizzare contenuti personalizzati in tempo reale su siti web, app per dispositivi mobili e altre proprietà digitali.

>[!VIDEO](https://video.tv.adobe.com/v/3447363/?learn=on&captions=ita)

### Video: utilizzare segmenti [!DNL Real-Time CDP] in [!DNL Target]

Scopri come utilizzare segmenti [!DNL Real-Time Customer Data Platform] in [!DNL Adobe Target] per offrire esperienze personalizzate sul sito web e sulle app per dispositivi mobili.

>[!VIDEO](https://video.tv.adobe.com/v/3446835/?learn=on&captions=ita)

### Video: utilizzare attributi di profilo [!DNL Real-Time CDP] in [!DNL Adobe Target]

Scopri come utilizzare attributi di profilo [!DNL Adobe Real-Time Customer Data Platform] in [!DNL Adobe Target] per offrire esperienze personalizzate sul sito web e sulle app per dispositivi mobili.

>[!VIDEO](https://video.tv.adobe.com/v/3451901/?learn=on&captions=ita)

### Blog e video di [!DNL Adobe Target]: Personalizzazione stessa pagina avanzata

[[!DNL Adobe] annuncia Personalization avanzato a stessa pagina con [!DNL Adobe Target] e [!DNL Real-time Customer Data Platform]](https://blog.adobe.com/en/publish/2021/10/05/adobe-announces-same-page-enhanced-personalization-with-adobe-target-real-time-customer-data-platform){target=_blank}
