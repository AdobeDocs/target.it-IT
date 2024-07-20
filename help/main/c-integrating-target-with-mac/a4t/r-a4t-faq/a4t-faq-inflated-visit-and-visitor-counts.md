---
keywords: FAQ;domande frequenti;analytics for target;a4t;gonfiato;visita;visitatore;hit parziale;orfano
description: Risposte alle domande sui conteggi gonfiati per visite e visitatori quando si utilizza Analytics for [!DNL Target] (A4T). Scopri come ridurre al minimo i "dati parziali".
title: Dove posso trovare domande frequenti sui conteggi gonfiati per visite e visitatori con A4T?
feature: Analytics for Target (A4T)
exl-id: e936b1f6-dc72-4ab2-9bb5-169d1710edbe
source-git-commit: 0be54d82e25eb919102f6098c1b1db76ab291675
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 45%

---

# Conteggi gonfiati per visite e visitatori - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande più frequenti sui conteggi gonfiati per visite e visitatori quando si utilizza Analytics come origine per la generazione di rapporti per Target (A4T).

## Vedo un’impennata nelle visite. Come posso sapere se queste visite sono causate da hit con dati parziali? {#section_28506672C6224ED18AC74F6A02F6F811}

+++Risposta
Contatta [l&#39;Assistenza clienti Adobe](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) per recuperare un report sui dati parziali. Queste informazioni non sono disponibili direttamente nell’interfaccia utente di [!DNL Analytics].

+++

## Quali sono le possibili cause di hit con dati parziali? {#section_C4BB9925CE6444BE8CB9FBEFE5085546}

+++Risposta
Gli hit con dati parziali sono spesso il risultato di un’implementazione non corretta, ad esempio l’errore di allineamento degli ID delle suite di rapporti. Esistono anche ragioni valide, ad esempio pagine lente, errori di pagina, offerte di reindirizzamento in un’attività o versioni obsolete della libreria.

+++

## Esistono particolari tipi di attività [!DNL Target] che hanno maggiori probabilità di causare hit con dati parziali? {#section_69837442A9B84366BEFDA4588B31E574}

+++Risposta
Le offerte con reindirizzamento inviano immediatamente un utente a una pagina diversa e questo significa che la chiamata [!DNL Analytics] non si attiva sulla prima pagina.

+++