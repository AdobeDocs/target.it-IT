---
description: Sono necessari diversi passaggi per implementare Adobe Analytics come origine per la generazione di rapporti per Target (A4T).
keywords: A4T;Adobe Analytics;attività basata su Analytics;suite di rapporti di Analytics;suite di rapporti;integrazione di Target Analytics;configurazione di suite di rapporti
seo-description: Sono necessari diversi passaggi per implementare Adobe Analytics come origine per la generazione di rapporti per Target (A4T).
seo-title: Implementazione di Analytics for Target
solution: Target
title: Implementazione di Analytics for Target
topic: Premium
uuid: da6498c8-1549-4c36-ae42-38c731a28f08
translation-type: tm+mt
source-git-commit: 1be00210754e8fa3237fdbccf48af625c2aafe65

---


# Implementazione di Analytics for Target{#analytics-for-target-implementation}

Sono necessari diversi passaggi per implementare Adobe Analytics come origine per la generazione di rapporti per Target (A4T).

## Passaggi di implementazione {#section_73961BAD5BB4430A95E073DE5C026277}

Nella tabella seguente sono illustrati i passaggi necessari per implementare questa integrazione nel sito.

## Passaggio 1: Richiedere il provisioning per Analytics e Target

Dopo aver implementato Analytics come origine di reporting per Target, è necessario ottenere il provisioning per entrambi. [Utilizza questo modulo per richiedere il provisioning](http://www.adobe.com/go/audiences).

## Passaggio 2: Configurare le autorizzazioni utente

I requisiti dell&#39;account utente devono essere soddisfatti prima di procedere alla creazione di un&#39;attività basata su Adobe Analytics in Adobe Target. Vedete [Requisiti delle autorizzazioni utente](/help/c-integrating-target-with-mac/a4t/account-reqs.md).

## Passaggio 3: Implementare il servizio ID visitatore di Experience Cloud

Il servizio ID visitatore consente di identificare gli utenti attraverso le diverse soluzioni Experience Cloud. È necessario implementare o eseguire la migrazione alla versione richiesta del servizio ID visitatore di Experience Cloud. Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Consulta [Implementazione del servizio Experience Cloud ID per Target](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-setup-target.html) nella documentazione del servizio ID visitatore di Experience Cloud.

## Passaggio 4: Aggiornare AppMeasurement per JavaScript o s_code

È necessario implementare o eseguire la migrazione alla versione richiesta di appMeasurement.js. Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Per nuove implementazioni, consulta [Implementazione di Analytics JavaScript](https://marketing.adobe.com/resources/help/en_US/sc/implement/js_implementation.html).

Per una migrazione, consulta [Migrazione ad AppMeasurement per JavaScript](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=appmeasure_mjs_migrate).

## Passaggio 5: Scaricare e aggiornare at.js o mbox.js

Devi implementare o eseguire la migrazione alla versione richiesta di at.js o mbox.js utilizzando il tuo account di produzione. Non sono richieste modifiche al codice.

Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md).

## Passaggio 6: Hosting di at.js o mbox.js

Se at.js o mbox.js è stato distribuito in precedenza, puoi sostituire il file esistente con la versione aggiornata. Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md).

In caso contrario, il file può essere incluso in hosting insieme al servizio ID visitatore e AppMeasurement per file JavaScript. Questi file devono essere in hosting su un server web accessibile a tutte le pagine del sito. È necessario definire il percorso di questi file nella fase successiva.

## Passaggio 7: Includere un riferimento a at.js o mbox.js in tutte le pagine del sito

Includi at.js o mbox.js sotto VisitorAPI.js aggiungendo la seguente riga di codice nel <head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8"> tag in ogni pagina:

Per at.js:

```
<script language="JavaScript" type="text/javascript" 
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

Per mbox.js:

```
<script language="JavaScript" type="text/javascript" 
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/mbox.js"></script>
```

È essenziale che VisitorAPI.js sia caricato prima di at.js o mbox.js, quindi se stai aggiornando un file at.js o mbox.js esistente, assicurati di verificare l’ordine di caricamento.

## Passaggio 8: Convalidare l’implementazione

Carica le pagine dopo aver aggiornato le librerie JavaScript per confermare che i valori dei parametri mboxMCSDID nelle chiamate di Target corrispondano al valore del parametro sdid nella chiamata di visualizzazione della pagina Analytics.

Tale conferma è particolarmente importante in applicazioni a pagina singola (SPA) in cui l’ordine delle chiamate non è sempre prevedibile.

**Nota:** la corrispondenza di questi valori è necessaria per il corretto funzionamento di A4T.

## Passaggio 9: (Facoltativo) Rimuovere il codice di integrazione precedente

È consigliabile rimuovere l’integrazione precedente per semplificare l’implementazione ed eliminare la necessità di risolvere eventuali discrepanze tra i sistemi. Puoi rimuovere eventuale codice che potrebbe essere stato distribuito da una precedente integrazione tra SC e T&amp;T, incluso `mboxLoadSCPlugin`.

## Passaggio 10: Abilitare le opzioni per l’utilizzo di Analytics come origine per la creazione di rapporti per Target

In Target, fai clic su [!UICONTROL Configurazione &gt; Preferenze] e scegli [!UICONTROL Seleziona per attività] o [!UICONTROL Adobe Analytics].

* Seleziona per attività consente di scegliere tra Target e Analytics per la creazione di ogni attività.
* Adobe Analytics imposta Analytics come origine dei rapporti per tutte le attività che hai creato.

