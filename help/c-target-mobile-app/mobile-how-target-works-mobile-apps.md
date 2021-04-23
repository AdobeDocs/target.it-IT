---
description: Scopri come utilizzare Adobe Mobile SDK per mostrare le esperienze ottimali ai visitatori dell’app mobile.
title: Come funziona [!DNL Target] nelle app mobili?
feature: Implementare Mobile
role: Developer
exl-id: 1a5f34dc-932d-47c7-b730-6d1658343fb4
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 83%

---

# Funzionamento di [!DNL Target] nelle applicazioni per dispositivi mobili

L’SDK di Adobe Mobile contatta il server di Target per ottenere il contenuto ed altri punti di dati per mostrare l’esperienza più appropriata all’utente.

## Posizioni di destinazione e metriche di successo {#section_A08AAB0ABA9C4568A5AFD4D27EF1CE74}

Una *posizione di destinazione* viene indicata anche come mbox. È possibile abilitare una posizione identificata nell’app a scopo di testing o personalizzazione (ad esempio, per presentare il messaggio di benvenuto nella schermata iniziale). Queste posizioni vengono identificate durante il processo di creazione del test.

Una *[metrica di successo](/help/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)* è un’azione eseguita dall’utente che identifica l’esito di una specifica attività (ad esempio la registrazione, un acquisto, la prenotazione di un biglietto e così via).

![](assets/mobile-target-location.png)

* **Posizione di destinazione:** il contenuto che compare sotto il pulsante di registrazione.

   A questo particolare utente viene offerta la spedizione gratuita fino alle 18:00. Questa posizione può essere riutilizzata in altre attività Target per eseguire test A/B e personalizzazione.

* **Metrica di successo**: azione eseguita dall’utente che preme il pulsante di registrazione.

**Funzionamento di Target nell’SDK**

![](assets/how-target-mobile-works.png)
