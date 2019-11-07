---
description: L’SDK di Adobe Mobile contatta il server di Target per ottenere il contenuto ed altri punti di dati per mostrare l’esperienza più appropriata all’utente.
title: Funzionamento di Target nelle applicazioni per dispositivi mobili
uuid: 8b302292-2cc0-46b9-b29c-088006721c7f
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Funzionamento di Target nelle applicazioni per dispositivi mobili{#how-target-works-in-mobile-apps}

L’SDK di Adobe Mobile contatta il server di Target per ottenere il contenuto ed altri punti di dati per mostrare l’esperienza più appropriata all’utente.

## Posizioni di destinazione e metriche di successo {#section_A08AAB0ABA9C4568A5AFD4D27EF1CE74}

Una *posizione di destinazione* viene indicata anche come mbox. È possibile abilitare una posizione identificata nell’app a scopo di testing o personalizzazione (ad esempio, per presentare il messaggio di benvenuto nella schermata iniziale). Queste posizioni vengono identificate durante il processo di creazione del test.

Una *[metrica di successo](../c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)* è un’azione eseguita dall’utente che identifica l’esito di una specifica attività (ad esempio la registrazione, un acquisto, la prenotazione di un biglietto e così via).

![](assets/mobile-target-location.png)

* **Posizione di destinazione:** il contenuto che compare sotto il pulsante di registrazione.

   A questo particolare utente viene offerta la spedizione gratuita fino alle 18:00. Questa posizione può essere riutilizzata in altre attività Target per eseguire test A/B e personalizzazione.

* **Metrica di successo**: azione eseguita dall’utente che preme il pulsante di registrazione.

**Funzionamento di Target nell’SDK**

![](assets/how-target-mobile-works.png)

