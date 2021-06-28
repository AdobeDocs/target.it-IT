---
keywords: Browser;prerequisiti;requisiti;Internet Explorer;Chrome;Firefox;Safari;Android;Surface
description: Scopri quali browser Internet Adobe [!DNL Target] supporta per la sua interfaccia e per la distribuzione dei contenuti.
title: Quali browser supporta [!DNL Target] ?
feature: Implementazione
role: Developer
exl-id: 8a366c79-d944-4d44-be5a-7c4f65385beb
source-git-commit: f028d2b439fee5c2a622748126bb0a34d550a395
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 46%

---

# Browser supportati

L’applicazione [!DNL Adobe Target] e la consegna dei contenuti sono stati testati su una vasta gamma di browser e dispositivi.

Per informazioni più importanti su TLS, consulta [Modifiche alla crittografia di TLS (Transport Layer Security)](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451).

## [!DNL Target]Interfaccia di Standard/Premium  {#section_1B73CA4B7BBC460BB7009DF00A2AFC4D}

L&#39;interfaccia [!DNL Target] supporta i seguenti browser e dispositivi:

| Tipo di dispositivo | Versione del browser |
|--- |--- |
| Windows | <ul><li>Microsoft Edge</li><li>Google Chrome (più recente, meno 1)</li><li>Mozilla Firefox (ultima, ultima meno 1)</li></ul> |
| Mac | <ul><li>Firefox (più recente, meno 1)</li><li>Chrome (più recente, meno 1)</li></ul> |

## Consegna dei contenuti {#section_1045A946056441268D40025529918D3D}

La consegna dei contenuti è stata testata attraverso i seguenti browser e dispositivi:

| Tipo di dispositivo | Versione del browser |
|--- |--- |
| Windows | <ul><li>Microsoft Internet Explorer 9 e 10. Testato in modalità emulazione.<br>**Nota**: La distribuzione dei contenuti su IE 9 non è più supportata con at.js 1.3.0 (e versioni successive). La distribuzione dei contenuti su IE 10, 11 e tutte le versioni precedenti non è più supportata con at.js 2.5.0 (e versioni successive).</li><li>Internet Explorer 11 <br>**Nota**: La distribuzione dei contenuti su IE 10, 11 e tutte le versioni precedenti non è più supportata con at.js 2.5.0 (e versioni successive).</li><li>Microsoft Edge</li><li>Chrome (più recente, meno 1)</li><li>Firefox (più recente, meno 1)</li></ul> |
| Mac | <ul><li>Apple Safari (ultima)<br>**Nota**: Per ulteriori informazioni su come Safari gestisce i cookie di prima e terze parti, consulta [Cookie di Target](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/cookie-behavior.md).</li><li>Firefox (più recente, meno 1)</li><li>Chrome (più recente, meno 1)</li></ul> |
| Cellulare/Tablet | <ul><li>Apple iOS (più recente)</li><li>Dispositivi Android e Tablet (Android 4 e versioni successive)</li><li>Microsoft Surface (Windows 8.1)</li></ul> |

Tieni presente quanto segue:

* Per le implementazioni di [!DNL at.js], [!DNL Target] mostra il contenuto predefinito nelle versioni precedenti di Internet Explorer e possibilmente nelle versioni precedenti dei browser sopra elencati.
* Internet Explorer considera tutti gli elementi sconosciuti (come gli elementi personalizzati) come lo stesso tipo di elemento. Di conseguenza, la consegna non funziona con elementi personalizzati.
* [!DNL Target] mostra il contenuto predefinito nei browser non elencati sopra e nei browser che utilizzano modalità [non standard](https://en.wikipedia.org/wiki/Quirks_mode). at.js richiede un doctype che esegua il rendering in modalità standard, ad esempio: `<!DOCTYPE html>`.
* L’infrastruttura di Adobe Delivery è stata protetta per NON supportare i dispositivi e i browser TLS 1.0 dopo il 12 settembre 2018. Consulta [Modifiche alla crittografia di TLS (Transport Layer Security)](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451) per capire l’impatto complessivo di questa modifica.
