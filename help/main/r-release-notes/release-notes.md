---
keywords: Note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 953b511db6d2c7ccf883d8e256c4e0ab22718862
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 54%

---

# Note sulla versione di Target (corrente)

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 22.5.1 (rilascio scaglionato; (11-13 maggio 2022)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **11 maggio**: regione Asia-Pacifico (APAC)
* **12 maggio**: Regione delle Americhe
* **13 maggio**: Area Europa, Medio Oriente e Africa (EMEA)

Questa versione contiene i miglioramenti e le correzioni seguenti:

* È stato risolto un problema che causava un errore JavaScript e impediva ad alcuni clienti di accedere ai dettagli dell’attività per alcuni [!UICONTROL Automated Personalization] (AP) attività. (TGT-43526)
* È stato risolto un problema che impediva ad alcuni clienti di aggiungere (o modificare) un&#39;offerta specifica a un&#39;attività di Personalizzazione automatizzata. (TGT-43503)
* È stato risolto un problema in [!DNL Target] Interfaccia utente che ha visualizzato il seguente messaggio di errore: &quot;La mbox globale potrebbe non essere sincronizzata. Prova a salvarla di nuovo.” Questo problema era relativo a un’interfaccia utente e non aveva alcun impatto sulle implementazioni dei clienti. (TGT-43475)
* È stato risolto un problema che impediva a un cliente di modificare i perfezionamenti e i tipi di pubblico a livello di esperienza per un’attività se i perfezionamenti e i tipi di pubblico venivano creati prima del nuovo [!UICONTROL Tipi di pubblico] Interfaccia utente distribuita. (TGT-43433)
* È stato risolto un problema che consentiva ai clienti di selezionare un duplicato [!DNL Adobe Audience Manager] (AAM) tipi di pubblico durante la modifica dei tipi di pubblico di reporting per un’attività. (TGT-43430)
* È stato risolto un problema che impediva ai clienti di creare tipi di pubblico duplicati, ma in aree di lavoro diverse. (TGT-43423)
* È stato risolto un problema che impediva ai clienti di eliminare le posizioni con offerte ad hoc nelle attività create in [!UICONTROL Compositore esperienza basato su moduli]. (TGT-43315)
* È stato risolto un problema che impediva ai clienti di accedere alle offerte di codice dopo aver fatto clic su offerte di immagini e aver quindi aggiornato l’interfaccia utente. (TGT-43566)
* È stato risolto un problema che causava il ripristino dello script originale non modificato dopo la modifica, l’attivazione e la disattivazione dello script da parte delle modifiche apportate agli script di profilo. Lo script di profilo rimane ora nello stato modificato. (TGT-43249)
* È stato risolto un problema che causava il seguente errore durante il tentativo di spostare un pubblico in un&#39;altra area di lavoro: &quot;Non possiamo completare la tua richiesta. Contatta l’Assistenza clienti Adobe se il problema persiste&quot;. (TGT-43212)
* È stato corretto un errore che causava un errore durante la clonazione di modifiche al codice personalizzato per le pagine app a pagina singola (SPA). (TGT-43137)
* È stato risolto un problema che causava la modifica della promozione originale dopo la duplicazione di un’esperienza e la successiva modifica della promozione. (TGT-41775)

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| Modifiche alla documentazione | Consulta le informazioni dettagliate sugli aggiornamenti di questa guida che non sono inclusi nelle presenti note sulla versione.<br>Per ulteriori informazioni, consulta [Modifiche alla documentazione](/help/main/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Note sulla versione per le versioni precedenti | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium.<br>Per ulteriori informazioni, consulta [Note sulla versione per le versioni precedenti](/help/main/r-release-notes/release-notes-for-previous-releases.md). |
| Note sulla versione di Adobe Experience Cloud | Ultime note sulla versione per le soluzioni Adobe Experience Cloud.<br>Per ulteriori informazioni, consulta [Note sulla versione di Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=it). |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| Adobe Priority Product Update | Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Note sulle prossime versioni | Per informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease, consulta la pagina [Note sulla versione di Target (prerelease)](/help/main/r-release-notes/target-release-notes.md). |
