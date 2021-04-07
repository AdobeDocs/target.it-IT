---
keywords: implementare;implementazione;configurazione;configurazione;parametro di pagina
description: Inserire dati in Target utilizzando i parametri di pagina.
title: Come posso inserire dati in Target utilizzando i parametri di pagina?
feature: Implementazione
role: Developer
exl-id: a285eadc-b71e-49a8-9071-397ada283baf
translation-type: tm+mt
source-git-commit: d9cfdf397fb4f4d9d1f5632b4fec828edd95444e
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 45%

---

# Parametri di pagina

I parametri di pagina (detti anche &quot;parametri mbox&quot;) sono coppie nome/valore passate direttamente attraverso il codice di pagina e non memorizzate nel profilo del visitatore per un utilizzo futuro.

I parametri di pagina sono utili per inviare dati di pagina a Target che non devono essere memorizzati con il profilo del visitatore per un utilizzo futuro del targeting. Questi valori vengono invece utilizzati per descrivere la pagina o l&#39;azione che l&#39;utente ha assunto nella pagina specifica.

## Formato

I parametri di pagina vengono passati alla destinazione tramite una chiamata al server come stringa di coppia nome e valore. I nomi dei parametri e i valori sono personalizzabili (anche se ci sono alcuni “nomi riservati” per usi specifici).

### Esempi

* `page=productPage`

* `categoryId=homeLoans`

## Esempi di casi d’uso

* **Pagine** dei prodotti: Inviare informazioni sul prodotto specifico visualizzato (questo metodo è il funzionamento di Recommendations)
* **Dettagli** ordine: Invia ID ordine, orderTotal e così via per la raccolta degli ordini
* **Affinità tra categorie**: invia informazioni visualizzate per categoria a Target per conoscere l’affinità dell’utente a particolari categorie di siti
* **Dati di terze parti**: invia informazioni da fonti di dati di terze parti, ad esempio i provider di targeting del meteo, i dati dell’account (DemandBase), i dati demografici (ad esempio Experian) e altro ancora.

## Vantaggi del metodo

I dati vengono inviati a Target in tempo reale e possono essere utilizzati nella stessa chiamata server per i dati su cui entrano.

## Avvertenze

* Richiede l&#39;aggiornamento del codice della pagina (direttamente o tramite un sistema di gestione dei tag).
* Se i dati devono essere utilizzati per il targeting in una successiva chiamata a una pagina/server, devono essere tradotti in uno script di profilo.
* Le stringhe di query possono contenere solo caratteri che rispettano lo [standard Internet Engineering Task Force (IETF)](https://www.ietf.org/rfc/rfc3986.txt).

   Oltre ai caratteri menzionati sul sito IETF, Target consente i seguenti caratteri nelle stringhe di query:

   `&lt; > # % ” { } | \\ ^ \[\] \``

   Tutto il resto deve avere la codifica URL. Lo standard specifica il formato seguente ( [https://www.ietf.org/rfc/rfc1738.txt](https://www.ietf.org/rfc/rfc1738.txt) ), come illustrato di seguito:

   ![](assets/ietf1.png)

   Oppure, l&#39;elenco completo per semplicità:

   ![](assets/ietf2.png)

## Esempi di codice

targetPageParamsAll (aggiunge i parametri a tutte le chiamate mbox nella pagina):

`function targetPageParamsAll() { return "param1=value1&param2=value2&p3=hello%20world";`

targetPageParams (aggiunge i parametri alla MBOX globale nella pagina):

`function targetPageParams() { return "param1=value1&param2=value2&p3=hello%20world";`

Parametri nel codice mboxCreate:

`<div class="mboxDefault"> default content to replace by offer </div> <script> mboxCreate('mboxName','param1=value1','param2=value2'); </script>`

## Link a informazioni rilevanti

Consigli: [Implementazione in base al tipo di pagina](/help/c-recommendations/plan-implement.md#reference_DE38BB07BD3C4511B176CDAB45E126FC)

Conferma ordine: [Tracciare le conversioni](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053)

Affinità tra categorie: [Affinità tra categorie](/help/c-target/c-visitor-profile/category-affinity.md#concept_75EC1E1123014448B8B92AD16B2D72CC)
