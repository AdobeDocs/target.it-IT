---
keywords: implementazione;libreria javascript;js;atjs;decisioni su dispositivi;decisioni su dispositivi;funzioni supportate
description: Scopri quali funzioni sono supportate per le decisioni sui dispositivi.
title: Quali funzioni sono supportate in On-Device Decisioning
feature: at.js
role: Developer
exl-id: 3531ff55-c3db-44c1-8d0a-d7ec2ccb6505
translation-type: tm+mt
source-git-commit: 62a3b387445977a1bdcd2cf45306c8ff032fca50
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 11%

---

# Funzioni supportate per le decisioni su dispositivi

L’ [!DNL Adobe Target] SDK JS offre ai clienti la flessibilità di scegliere tra prestazioni e aggiornamento dei dati per le decisioni. In altre parole, se la distribuzione di contenuti personalizzati più rilevanti e coinvolgenti tramite l’apprendimento automatico è per te più importante, è necessario effettuare una chiamata al server live. Ma quando le prestazioni sono più importanti, è necessario prendere una decisione su dispositivo e in memoria. Affinché le decisioni sul dispositivo funzionino, consulta le sezioni seguenti che elencano le funzioni supportate.

## Tipi di attività supportati

La tabella seguente indica quali [tipi di attività](/help/c-activities/target-activities-guide.md) creati dal [Compositore esperienza basato su moduli](/help/c-experiences/form-experience-composer.md) o [Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) sono supportati o non sono supportati per le decisioni sul dispositivo.

| Tipo di attività | Supportate? |
| --- | --- |
| [Test A/B](/help/c-activities/t-test-ab/test-ab.md) | Sì |
| [Allocazione automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | No |
| [Targeting automatico](/help/c-activities/auto-target/auto-target-to-optimize.md) ![Premium](/help/assets/premium.png) | No |
| [Test multivariato](/help/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | No |
| [](/help/c-activities/t-experience-target/experience-target.md)Targeting esperienza (XT) | Sì |
| [Personalizzazione automatizzata ](/help/c-activities/t-automated-personalization/automated-personalization.md) ![Premium](/help/assets/premium.png) | No |
| [](/help/c-recommendations/recommendations.md) ![RecommendationsPremium](/help/assets/premium.png) | No |
| [Attività che utilizzano Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md)  (A4T) | Sì |

## Targeting del pubblico

La tabella seguente indica quali regole di pubblico sono supportate o non supportate per le decisioni sui dispositivi.

| Regola di pubblico | Supportate? |
| --- | --- |
| [Geo](/help/c-target/c-audiences/c-target-rules/geo.md) | Sì |
| [Rete](/help/c-target/c-audiences/c-target-rules/network.md) | No |
| [Mobile](/help/c-target/c-audiences/c-target-rules/mobile.md) | No |
| [Parametri personalizzati](/help/c-target/c-audiences/c-target-rules/custom-parameters.md) | Sì |
| [Sistema operativo](/help/c-target/c-audiences/c-target-rules/operating-system.md) | Sì |
| [Pagine del sito](/help/c-target/c-audiences/c-target-rules/site-pages.md) | Sì |
| [Browser](/help/c-target/c-audiences/c-target-rules/browser.md) | Sì |
| [Profilo visitatore](/help/c-target/c-audiences/c-target-rules/visitor-profile.md) | No |
| [Origini del traffico](/help/c-target/c-audiences/c-target-rules/traffic-sources.md) | No |
| [Intervallo temporale](/help/c-target/c-audiences/c-target-rules/time-frame.md) | Sì |
| Tipi di pubblico Adobe Experience Cloud<br>(tipi di pubblico da [!DNL Adobe Analytics], [!DNL Adobe Audience Manager] e [!DNL Adobe Experience Manager] | No |

### Geotargeting per le decisioni su dispositivi

Per mantenere una latenza minima per le attività di decisione sui dispositivi con tipi di pubblico basati su geo, l’Adobe consiglia di fornire i valori geografici nella chiamata a [getOffers](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md). Impostare l&#39;oggetto Geo nel contesto della richiesta. Questo significa che dal browser, un modo per determinare la posizione di ogni visitatore. Ad esempio, puoi eseguire una ricerca IP-to-Geo utilizzando un servizio configurato. Alcuni provider di hosting, come Google Cloud, forniscono questa funzionalità tramite intestazioni personalizzate in ogni `HttpServletRequest`.

```javascript
window.adobe.target.getOffers({ 
	decisioningMethod: "on-device", 
	request: { 
		context: { 
			geo: { 
				city: "SAN FRANCISCO", 
				countryCode: "US", 
				stateCode: "CA", 
				latitude: 37.75, 
				longitude: -122.4 
			} 
		}, 
		execute: { 
			pageLoad: {} 
		} 
	} 
})
```

Tuttavia, se non sei in grado di eseguire ricerche IP-to-Geo sul server, ma desideri comunque eseguire le decisioni sul dispositivo per le richieste [getOffers](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) che contengono tipi di pubblico basati su geo, è supportato anche questo. Il lato negativo di questo approccio è che utilizza una ricerca IP-to-Geo remota, che aggiunge latenza a ogni chiamata `getOffers`. Questa latenza deve essere inferiore a una chiamata `getOffers` con decisioni lato server, perché raggiunge una rete CDN situata vicino al server. Specifica solo il campo &quot;ipAddress&quot; nell’oggetto Geo nel contesto della richiesta dell’SDK per recuperare la geolocalizzazione dell’indirizzo IP del visitatore. Se viene fornito un qualsiasi altro campo oltre a &quot;ipAddress&quot;, l’ [!DNL Target] SDK non recupererà i metadati di geolocalizzazione per la risoluzione.

```javascript
window.adobe.target.getOffers({ 
	decisioningMethod: "on-device", 
	request: { 
		context: { 
			geo: { 
				ipAddress: "127.0.0.1" 
			} 
		}, 
		execute: { 
			pageLoad: {} 
		} 
	} 
})
```

### Metodo di allocazione

La tabella seguente indica quali metodi di allocazione sono supportati o non supportati per le decisioni sul dispositivo.

| Metodo di allocazione | Supportate? |
| --- | --- |
| Manuale | Sì |
| [Allocazione automatica all’esperienza migliore](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | No |
| [Targeting automatico per esperienze personalizzate](/help/c-activities/auto-target/auto-target-to-optimize.md) | No |
