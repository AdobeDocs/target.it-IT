---
keywords: faq;frequently asked questions;analytics for target;a4T;classifications;classification;classifications importer;post-tnt-action
description: Questo argomento contiene le risposte alle domande più frequenti sulle classificazioni e sull’utilizzo di Analytics come origine per la generazione di rapporti per Target (A4T).
title: Classificazioni - Domande frequenti su A4T
feature: null
topic: Standard
uuid: 4b42adbc-4fa8-4b62-86c8-bb8f8bec7e54
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 66%

---


# Classificazioni - Domande frequenti su A4T{#classifications-a-t-faq}

This topic contains answers to questions that are frequently asked about classifications and using [!DNL Analytics] as the reporting source for [!DNL Target] (A4T).

## Dopo aver utilizzato la funzione di importazione classificazioni per scaricare le classificazioni, come associo un nome di attività al valore post-tnt-action? {#section_6045DAC488B248418F430E663C38D001}

È possibile scaricare le classificazioni per la stringa A4T/TNT dalla funzione di [importazione classificazioni](https://docs.adobe.com/content/help/en/analytics/components/classifications/classifications-importer/c-working-with-saint.html) degli Strumenti di amministrazione. La variabile è denominata “TNT” nell’elenco di esportazione. I dati scaricati includono i nomi descrittivi per attività, esperienze e così via.

Questo file di consultazione è utile per i clienti che ricevono il feed di dati clickstream di Adobe. Il file fornisce nomi descrittivi per le colonne `post_tnt` e `post_tnt_action`.

Il formato stringa della variabile TNT è `activityID:experienceID:targettype|event`.

* targettype = 0 (control/random) o 1 (targeting) per le attività di allocazione [!UICONTROL automatica] e [!UICONTROL targeting] automatico.
* Event = 0 rappresenta l’entrata di un’esperienza.
* Event = 1 rappresenta una visita all’esperienza.
* Event = 2 rappresenta l’impression di un’attività.
* Event = 32767 rappresenta una conversione di attività.

You can import the classification file on a frequent basis from the UI using a [browser import](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/browser-import.html) or an [FTP import](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/import-file.html). È inoltre possibile interagire con i Servizi di ingegneria per ottenere il file come una tabella di consultazione insieme a un feed di dati clickstream.
