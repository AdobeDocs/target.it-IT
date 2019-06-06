---
description: L’applicazione Adobe Target e la consegna dei contenuti sono stati testati su una vasta gamma di browser e dispositivi.
keywords: Browser;prerequisiti;requisiti;Internet Explorer;Chrome;Firefox;Safari;Android;Surface
seo-description: L’applicazione Adobe Target e la consegna dei contenuti sono stati testati su una vasta gamma di browser e dispositivi.
seo-title: Browser supportati
solution: Target
subtopic: Introduzione
title: Browser supportati
topic: Standard
uuid: 614088da-412c-45e3-9f2d-6985391973be
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Browser supportati{#supported-browsers}

L’applicazione [!DNL Adobe Target] e la consegna dei contenuti sono stati testati su una vasta gamma di browser e dispositivi.

Per ulteriori, importanti informazioni su TLS, vedi [Modifiche alla crittografia di TLS (Transport Layer Security)](../../c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451).

## [!DNL Target] Interfaccia di Standard/Premium {#section_1B73CA4B7BBC460BB7009DF00A2AFC4D}

L’interfaccia di [!DNL [!DNL Target]] Standard/Premium supporta i seguenti browser e dispositivi:

| Tipo di dispositivo | Versione del browser |
|--- |--- |
| Windows | <ul><li>Microsoft Internet Explorer 11.<br>**Nota**: [!DNL Target] e Adobe Experience Cloud abbandoneranno il supporto per Microsoft Internet Explorer 11 a partire da marzo 2019. Questa modifica influisce solo sull&#39;authoring di [!DNL Target] senza influire sulla distribuzione delle esperienze. Passa a Microsoft Edge o a un altro browser supportato.</li><li>Microsoft Edge</li><li>Google Chrome (ultima, ultima meno 1)</li><li>Mozilla Firefox (ultima, ultima meno 1)</li></ul> |
| Mac | <ul><li>Firefox (ultima, ultima meno 1)</li><li>Chrome (ultima, ultima meno 1)</li></ul> |

## Consegna dei contenuti {#section_1045A946056441268D40025529918D3D}

La consegna dei contenuti è stata testata attraverso i seguenti browser e dispositivi:

| Tipo di dispositivo | Versione del browser |
|--- |--- |
| Windows | <ul><li>Internet Explorer 9 e 10. Testato in modalità emulazione.<br>**Nota**: at.js 1.3.0 (e versioni successive) non supporta più la consegna di contenuto in Microsoft Internet Explorer 9.</li><li>Internet Explorer 11</li><li>Microsoft Edge</li><li>Chrome (ultima, ultima meno 1)</li><li>Firefox (ultima, ultima meno 1)</li></ul> |
| Mac | <ul><li>Apple Safari (ultima)<br>**Nota**: per ulteriori informazioni su come Safari gestisce i cookie di prima e terze parti, consulta [Cookie di Target](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/cookie-behavior.md).</li><li>Firefox (ultima, ultima meno 1)</li><li>Chrome (ultima, ultima meno 1)</li></ul> |
| Cellulare/Tablet | <ul><li>Apple iOS (ultima)</li><li>Dispositivi Android e Tablet (Android 4 e versioni successive)</li><li>Microsoft Surface (Windows 8.1)</li></ul> |

Per le implementazioni di [!DNL at.js], [!DNL Target] mostra il contenuto predefinito nelle versioni precedenti di Internet Explorer e possibilmente nelle versioni precedenti dei browser sopra elencati. Per le implementazioni di [!DNL mbox.js], [!DNL Target] tenta di eseguire il rendering del contenuto ma l’operazione potrebbe non avere esito positivo.

[!DNL Target] visualizza il contenuto predefinito nei browser non elencati sopra e nei browser che sfruttano la tecnica [Quirks Mode](https://it.wikipedia.org/wiki/Quirks_Mode) at.js richiede un doctype che esegua il rendering in modalità standard, ad esempio: `<!DOCTYPE html>`.

>[!NOTE]
>
>L’infrastruttura di Adobe Delivery è stata protetta per NON supportare i dispositivi e i browser TLS 1.0 dopo il 12 settembre 2018. Consulta [Modifiche alla crittografia di TLS (Transport Layer Security)](../../c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451) per capire l’impatto complessivo di questa modifica.
