---
keywords: implementare;implementazione;adobe launch;launch;race;reindirizzamento;experience platform launch;platform launch;tag;adobe platform
description: Scopri come implementare il [!DNL Adobe Target] libreria at.js utilizzando [!DNL Adobe Experience Platform], il metodo preferito per implementare [!DNL Target].
title: Come si implementa  [!DNL Target]  utilizzando  [!DNL Adobe Experience Platform]?
feature: Implement Server-side
role: Developer
exl-id: 7cc1d3ab-4a68-4454-95b0-04fa547a6d9e
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 96%

---

# Implementazione di [!DNL Target] tilizzando [!DNL Adobe Experience Platform]

I tag in [!DNL Adobe Experience Platform] rappresentano la nuova generazione di funzionalità [!DNL Adobe] per la gestione dei tag. I tag offrono ai clienti un modo semplice di implementare e gestire i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate.

>[!NOTE]
>
>[!DNL Adobe Experience Platform Launch] è stato ridefinito come suite di tecnologie di raccolta dati in [!DNL Adobe Experience Platform]. Di conseguenza, sono state introdotte diverse modifiche terminologiche nella documentazione del prodotto. Per un riferimento consolidato delle modifiche terminologiche, consulta il seguente [documento](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=it).

Nella tabella seguente sono elencate diverse risorse utili:

| Risorsa | Dettagli |
|--- |--- |
| [Aggiungere [!UICONTROL Adobe Target]](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-websites-with-launch/implement-solutions/target.html?lang=it#implement-solutions) | Questo tutorial fornisce istruzioni dettagliate per implementare [!DNL Target] in un sito web con tag in [!DNL Adobe Experience Platform]. Gli argomenti includono l’aggiunta della libreria JavaScript at.js, l’attivazione della mbox globale, l’aggiunta di parametri e l’integrazione con altre soluzioni. Questo articolo fa parte di un tutorial più ampio che mostra come implementare [!DNL Adobe Experience Platform] e altre soluzioni [!DNL Adobe Experience Cloud]. |
| [Guida rapida](https://experienceleague.adobe.com/docs/experience-platform/tags/get-started/quick-start.html?lang=it) | Informazioni sull’implementazione e la gestione dei tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate. |
| [Panoramica dell’estensione Adobe  [!DNL Target] ](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target/overview.html?lang=it) | Informazioni sull’implementazione di [!DNL Target] mediante [!DNL Adobe Experience Platform]. |

## Vantaggi dell’implementazione di at.js con l’estensione [!DNL Target] {#section_48B3F938B6F8491DAF798E0DB54EF304}

I seguenti vantaggi si applicano solo se si utilizzano i tag in [!DNL Adobe Experience Platform] per implementare at.js. Per questo motivo, [!DNL Adobe] consiglia vivamente di utilizzare i tag in [!DNL Adobe Experience Platform] invece di ricorrere all’implementazione manuale di at.js.

* **Risolve una situazione di tipo “race condition” tra [!DNL Adobe Analytics] e [!DNL Target]:** poiché la chiamata di [!DNL Analytics] potrebbe essere attivata prima della chiamata di [!DNL Target], la chiamata di [!DNL Target] non viene unita alla chiamata di [!DNL Analytics] e la sequenza potrebbe generare dei dati errati. L’estensione [!DNL Target] fa sì che la chiamata beacon di [!DNL Analytics] attenda che venga completata la chiamata di [!DNL Target], a prescindere dal suo esito positivo o negativo. L’utilizzo dei tag in [!DNL Adobe Experience Platform] evita le possibili incongruenze nei dati derivanti da un’implementazione manuale.

   >[!NOTE]
   >
   >Utilizza l’azione [!UICONTROL Invia beacon] nell’estensione [!DNL Adobe Analytics] in modo che la chiamata di [!DNL Analytics] attenda la chiamata di [!DNL Target]. Se chiami direttamente `s.t()` o `s.tl()` con un codice personalizzato, le chiamate di [!DNL Analytics] non attendono il completamento delle chiamate di [!DNL Target].

* **Impedisce la gestione errata delle offerte di reindirizzamento:** se sulla pagina sono utilizzati sia [!DNL Target] che [!DNL Analytics] ed è presente un’offerta di reindirizzamento eseguita da [!DNL Target], si potrebbero riscontrare dei problemi se la funzione di tracciamento di [!DNL Analytics] genera una richiesta quando non dovrebbe (perché l’utente viene reindirizzato a un URL diverso). Se implementi [!DNL Target] e [!DNL Analytics] tramite i tag in [!DNL Adobe Experience Platform], questo problema non si verifica. Quando si utilizzano i tag in [!DNL Adobe Experience Platform], [!DNL Target] indica ad [!DNL Analytics] di interrompere la richiesta beacon di [!DNL Analytics].
