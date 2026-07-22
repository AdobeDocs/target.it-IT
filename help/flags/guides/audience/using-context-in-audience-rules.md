---
title: Usa contesto nelle regole del pubblico
description: Scopri come utilizzare gli attributi di contesto nelle regole per il pubblico per i flag di funzione e i gruppi di funzioni nei flag.
badge: label="Beta" type="Informative"
hide: true
exl-id: 0367f475-9209-4d53-86b4-a739a73a23a7
source-git-commit: 8fffd619232b2cae2f5dd0aa1e0a55183c4be698
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 1%

---

# Usa contesto nelle regole del pubblico {#context-in-audience-rules}

Gli attributi di contesto sono valori forniti dall’applicazione client in fase di esecuzione. Consentono di eseguire il targeting degli utenti in base a informazioni dinamiche a livello di sessione, come la lingua attiva dell’utente, il tipo di dispositivo o lo stato dell’applicazione.

Gli attributi di contesto sono pertinenti per i client web e mobili.

## Funzionamento degli attributi di contesto {#how-context-attributes-work}

Quando si valuta un flag di funzione, l’applicazione trasmette gli attributi di contesto ai flag. Nella console puoi definire le regole che controllano questi valori, che verranno utilizzate dalla piattaforma al momento della valutazione per determinare se l’utente è idoneo.

## Aggiunta di un attributo di contesto {#adding-context-attribute}

Per aggiungere un attributo di contesto a una regola di pubblico:

1. Apri il flag di funzione o il gruppo di funzioni nella console.
2. Passa alla scheda **Pubblico**.
3. In **Contesto**, aggiungi una nuova condizione.
4. Seleziona l’attributo di contesto, l’operatore e il valore.

Se l&#39;attributo di contesto necessario non viene visualizzato nell&#39;elenco, è possibile crearne uno nuovo. Vedere [Creazione degli attributi di contesto](creating-your-context-attributes.md).

## Vedi anche {#see-also}

* [Pubblico nei flag di funzione e nei gruppi di funzioni](audience-in-feature-flags-and-feature-groups.md)

<!-- -->
