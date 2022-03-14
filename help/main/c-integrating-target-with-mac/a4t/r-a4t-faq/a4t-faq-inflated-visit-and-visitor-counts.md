---
keywords: FAQ;domande frequenti;analytics for target;a4t;gonfiato;visita;visitatore;hit parziale;orfano
description: Trova le risposte alle domande sui conteggi gonfiati per visite e visitatori quando utilizzi Analytics per [!DNL Target] (A4T). Scopri come ridurre al minimo i "dati parziali".
title: Dove posso trovare le domande frequenti sui conteggi gonfiati per visite e visitatori con A4T?
feature: Analytics for Target (A4T)
exl-id: e936b1f6-dc72-4ab2-9bb5-169d1710edbe
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 61%

---

# Conteggi gonfiati per visite e visitatori - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande più frequenti sui conteggi gonfiati per visite e visitatori quando si utilizza Analytics come origine per la generazione di rapporti per Target (A4T).

## Perché i dati di Analytics mostrano visite che non hanno visualizzazioni di pagina o altri valori variabili? {#section_4D8C2C2D766842E6B12F3ECC774A64D5}

Quando [!DNL Adobe Analytics] viene utilizzato per misurare [!DNL Target] attività (denominate A4T), [!DNL Analytics] raccoglie dati non disponibili in assenza di [!DNL Target] attività nella pagina. Ciò è dovuto al fatto che l’attività di [!DNL Target] innesca una chiamata nella parte superiore della pagina, ma solitamente [!DNL Analytics] genera le chiamate di raccolta dati nella parte inferiore della pagina. Nell’implementazione di A4T fino a oggi, l’Adobe include questi dati aggiuntivi ogni volta che un [!DNL Target] attività attiva.

Per ulteriori informazioni, consulta [Minimizzare i conteggi gonfiati per visite e visitatori in A4T](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Che cos’è un hit con dati parziali? {#section_59A203E289564576BF6821F96B0B9E11}

Un hit con dati parziali si verifica quando un tag di [!DNL Target] si attiva nella parte superiore della pagina, ma un tag [!DNL Analytics] non si genera nella parte inferiore della pagina. Ci sono varie ragioni per cui questa situazione si verifica. In [!DNL A4T] fino ad oggi, l’Adobe include i dati parziali relativi a questi hit ogni volta che un [!DNL Target] attività attiva. In futuro, Adobe includerà questi dati aggiuntivi solo quando entrambi i [!DNL Target] e [!DNL Analytics] Sono state attivate delle etichette.

Per ulteriori informazioni, consulta [Minimizzare i conteggi gonfiati per visite e visitatori in A4T](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Vedo un’impennata nelle visite. Come posso sapere se queste visite sono causate da hit con dati parziali? {#section_28506672C6224ED18AC74F6A02F6F811}

Contatta l’[Assistenza clienti Adobe](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) per recuperare un rapporto sui dati parziali. Queste informazioni non sono disponibili direttamente nell’interfaccia utente di [!DNL Analytics].

## Quali sono le possibili cause di hit con dati parziali? {#section_C4BB9925CE6444BE8CB9FBEFE5085546}

Gli hit con dati parziali sono spesso dovuti a un’implementazione errata, ad esempio ID di suite di rapporti non allineati correttamente. Esistono anche ragioni valide, ad esempio pagine lente, errori di pagina, offerte di reindirizzamento in un’attività o versioni obsolete della libreria.

Per ulteriori informazioni, consulta “Cosa contribuisce ai dati parziali” in [Minimizzare i conteggi gonfiati per visite e visitatori in A4T](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Ho degli hit con dati parziali. Cosa posso fare per ripulire i miei dati? {#section_CBE778A9D07A469E8FF98F68BACC7124}

È possibile creare una suite di rapporti virtuale per escludere dai rapporti i dati parziali della cronologia.

Per ulteriori informazioni, consulta “Come posso visualizzare le tendenze della cronologia senza dati parziali?” in [Minimizzare i conteggi gonfiati per visite e visitatori in A4T](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Come posso evitare che le mie pagine generino hit con dati parziali? {#section_4B00E7E618444BE98A0798DE98F08B21}

A partire dal 14 novembre 2016, in Adobe saranno inclusi i dati solo quando entrambi [!DNL Target] e [!DNL Analytics] Sono state attivate delle etichette. Questo cambiamento non è retroattivo. Se i rapporti cronologici mostrano conteggi gonfiati, puoi escluderli dai rapporti creando una suite di rapporti virtuale. Consulta &quot;Come posso visualizzare le tendenze della cronologia senza dati parziali?&quot; in [Minimizzare i conteggi gonfiati per visite e visitatori in A4T](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

È possibile inoltre eseguire alcuni passaggi per ridurre al minimo gli hit con dati parziali. Per ulteriori informazioni, consulta “Quali sono le best practice per ridurre i dati parziali?” in [Minimizzare i conteggi gonfiati per visite e visitatori in A4T](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Se i dati parziali vengono rimossi dal rapporto, non si rischia di perdere valore [!DNL Target] o i dati di Analytics? {#section_EBC39E8A0F6A40E58F51E776936F7D9E}

Inclusione di dati parziali in [!DNL Analytics] il reporting fornisce informazioni aggiuntive, ma genera anche hit incoerenti per i dati precedenti relativi a periodi in cui non vi erano [!DNL Target] attività in esecuzione. L’inclusione dei dati con hit parziali può causare problemi per [!DNL Analytics] utenti che analizzano le tendenze nel tempo.

È possibile eseguire alcuni passaggi per ridurre al minimo gli hit con dati parziali. Per ulteriori informazioni, consulta “Quali sono le best practice per ridurre i dati parziali?” in [Minimizzare i conteggi gonfiati per visite e visitatori in A4T](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Esistono particolari tipi di [!DNL Target] attività che hanno maggiori probabilità di causare hit con dati parziali? {#section_69837442A9B84366BEFDA4588B31E574}

Le offerte con reindirizzamento inviano immediatamente un utente a una pagina diversa e questo significa che [!DNL Analytics] non si attiva sulla prima pagina.
