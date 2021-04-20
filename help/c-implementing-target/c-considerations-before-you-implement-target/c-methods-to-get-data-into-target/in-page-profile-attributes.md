---
keywords: implementare;implementazione;configurazione;configurazione;parametro di pagina
description: Inserire dati in Target utilizzando gli attributi di profilo nella pagina.
title: Come posso inserire dati in Target utilizzando gli attributi di profilo nella pagina?
feature: Implementation
role: Developer
exl-id: c6000720-a862-4e9c-96a5-055963a79544
translation-type: tm+mt
source-git-commit: 20daf4510e754d77cd16be64770105932178fec5
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 56%

---

# Attributi di profilo nella pagina

Gli attributi di profilo nella pagina in [!DNL Adobe Target] (detti anche &quot;attributi di profilo nella mbox&quot;) sono coppie di nome e valore passate direttamente attraverso il codice della pagina memorizzate nel profilo del visitatore per un utilizzo futuro.

Gli attributi di profilo nella pagina consentono l&#39;archiviazione dei dati specifici dell&#39;utente nel profilo di Target per targeting e segmentazione in un secondo momento.

## Formato

Gli attributi di profilo nella pagina vengono passati a Target tramite una chiamata al server come stringa di coppia di nome e valore con il prefisso “profile.” prima del nome dell&#39;attributo.

I nomi e i valori degli attributi sono personalizzabili (sebbene esistano alcuni “nomi riservati” per usi specifici).

### Esempi

* `profile.membershipLevel=silver`
* `profile.visitCount=3`

## Esempi di casi d’uso

* **Informazioni di login**: condividi dati non-PII (personalmente identificabili) con Target in base al login dell’utente. Questi dati possono essere lo stato di appartenenza, la cronologia degli ordini o altro ancora.
* **Informazioni sul negozio**: tracciare quale negozio è la posizione preferita dell’utente.
* **Interazioni precedenti**: tenere traccia di ciò che l’utente ha fatto precedentemente sul sito per informare le future personalizzazioni.

## Vantaggi del metodo

I dati vengono inviati a Target in tempo reale e possono essere utilizzati nella stessa chiamata al server in cui i dati entrano.

## Avvertenze

Richiede aggiornamenti del codice della pagina (direttamente o tramite un sistema di gestione dei tag).

Gli attributi e i valori sono visibili nelle chiamate al server, pertanto un visitatore può visualizzare i valori. Se condividi informazioni quali gamme di credito o altre informazioni potenzialmente private, questo metodo potrebbe non essere l’approccio migliore.

## Esempi di codice

targetPageParamsAll (aggiunge gli attributi a tutte le chiamate mbox nella pagina):

`function targetPageParamsAll() { return "profile.param1=value1&profile.param2=value2&profile.p3=hello%20world"; }`

targetPageParams (aggiunge gli attributi alla mbox globale nella pagina):

`function targetPageParams() { return profile.param1=value1&profile.param2=value2&profile.p3=hello%20world"; }`

Attributi nel codice mboxCreate:

`<div class="mboxDefault"> default content to replace by offer </div> <script> mboxCreate('mboxName','profile.param1=value1','profile.param2=value2'); </script>`

## Link a informazioni rilevanti

[Attributi del profilo](/help/c-target/c-visitor-profile/profile-parameters.md#concept_01A30B4762D64CD5946B3AA38DC8A201)

[Profilo visitatore](/help/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E)
