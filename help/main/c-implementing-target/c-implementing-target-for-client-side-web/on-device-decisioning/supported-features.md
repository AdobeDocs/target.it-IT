---
keywords: implementazione;libreria javascript;js;atjs;decisioni su dispositivi;decisioni su dispositivi;funzioni supportate
description: Scopri quali funzioni sono supportate per le decisioni sui dispositivi.
title: Quali funzioni sono supportate in On-Device Decisioning
feature: at.js
role: Developer
exl-id: 3531ff55-c3db-44c1-8d0a-d7ec2ccb6505
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 13%

---

# Funzioni supportate per il decisioning sul dispositivo

La [!DNL Adobe Target] L’SDK di JS offre ai clienti la flessibilità di scegliere tra prestazioni e aggiornamento dei dati per le decisioni. In altre parole, se la distribuzione di contenuti personalizzati più rilevanti e coinvolgenti tramite l’apprendimento automatico è per te più importante, è necessario effettuare una chiamata al server live. Ma quando le prestazioni sono più importanti, è necessario prendere una decisione su dispositivo e in memoria. Affinché le decisioni sul dispositivo funzionino, consulta le sezioni seguenti che elencano le funzioni supportate.

## Tipi di attività supportati

La tabella seguente indica quale [tipi di attività](/help/main/c-activities/target-activities-guide.md) creato da [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md) o [Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) sono supportati o non sono supportati per le decisioni su dispositivi.

| Tipo di attività | Supportate? |
| --- | --- |
| [Test A/B](/help/main/c-activities/t-test-ab/test-ab.md) | Sì |
| [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | No |
| [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) ![Premium](/help/main/assets/premium.png) | No |
| [Test multivariato](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | No |
| [Targeting esperienza](/help/main/c-activities/t-experience-target/experience-target.md) (XT) | Sì |
| [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) ![Premium](/help/main/assets/premium.png) | No |
| [Recommendations](/help/main/c-recommendations/recommendations.md) ![Premium](/help/main/assets/premium.png) | No |
| [Attività che utilizzano Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) | Sì |

## Targeting del pubblico

La tabella seguente indica quali regole di pubblico sono supportate o non supportate per le decisioni sui dispositivi.

| Regola di pubblico | Supportate? |
| --- | --- |
| [Geo](/help/main/c-target/c-audiences/c-target-rules/geo.md) | Sì |
| [Rete](/help/main/c-target/c-audiences/c-target-rules/network.md) | No |
| [Mobile](/help/main/c-target/c-audiences/c-target-rules/mobile.md) | No |
| [Parametri personalizzati](/help/main/c-target/c-audiences/c-target-rules/custom-parameters.md) | Sì |
| [Sistema operativo](/help/main/c-target/c-audiences/c-target-rules/operating-system.md) | Sì |
| [Pagine del sito](/help/main/c-target/c-audiences/c-target-rules/site-pages.md) | Sì |
| [Browser](/help/main/c-target/c-audiences/c-target-rules/browser.md) | Sì |
| [Profilo visitatore](/help/main/c-target/c-audiences/c-target-rules/visitor-profile.md) | No |
| [Origini del traffico](/help/main/c-target/c-audiences/c-target-rules/traffic-sources.md) | No |
| [Intervallo temporale](/help/main/c-target/c-audiences/c-target-rules/time-frame.md) | Sì |
| Pubblico Adobe Experience Cloud<br>(Tipi di pubblico da [!DNL Adobe Analytics], [!DNL Adobe Audience Manager]e [!DNL Adobe Experience Manager] | No |

### Geotargeting per le decisioni su dispositivi

Per mantenere una latenza minima per le attività di decisione sui dispositivi con tipi di pubblico basati su geo, l’Adobe consiglia di fornire i valori geo direttamente nella chiamata a [getOffers](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md). Impostare l&#39;oggetto Geo nel contesto della richiesta. Questo significa che dal browser, un modo per determinare la posizione di ogni visitatore. Ad esempio, puoi eseguire una ricerca IP-to-Geo utilizzando un servizio configurato. Alcuni provider di hosting, come Google Cloud, forniscono questa funzionalità tramite intestazioni personalizzate in ogni `HttpServletRequest`.

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

Tuttavia, se non sei in grado di eseguire ricerche IP-to-Geo sul server, ma desideri comunque eseguire le decisioni sul dispositivo per [getOffers](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) sono supportate anche le richieste che contengono tipi di pubblico basati su geo. Il lato negativo di questo approccio è che utilizza una ricerca IP-to-Geo remota, che aggiunge latenza a ogni `getOffers` chiama. Questa latenza deve essere inferiore a un `getOffers` chiama con le decisioni lato server, perché ha un hit per una rete CDN che si trova vicino al tuo server. Specifica solo il campo &quot;ipAddress&quot; nell’oggetto Geo nel contesto della richiesta dell’SDK per recuperare la geolocalizzazione dell’indirizzo IP del visitatore. Se viene fornito un qualsiasi altro campo oltre a &quot;ipAddress&quot;, la variabile [!DNL Target] L&#39;SDK non recupera i metadati di geolocalizzazione per la risoluzione.

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
| [Allocazione automatica all’esperienza migliore](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | No |
| [Targeting automatico per esperienze personalizzate](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | No |
