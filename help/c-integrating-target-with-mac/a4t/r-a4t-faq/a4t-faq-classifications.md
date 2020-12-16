---
keywords: faq;frequently asked questions;analytics for target;a4T;classifications;classification;classifications importer;post-tnt-action
description: Questo argomento contiene le risposte alle domande più frequenti sulle classificazioni e sull’utilizzo di Analytics come origine per la generazione di rapporti per Target (A4T).
title: Classificazioni - Domande frequenti su A4T
feature: a4t troubleshooting
translation-type: tm+mt
source-git-commit: 403a56da912fa143cf6c20b078c0bba63c6f4420
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 65%

---


# Classificazioni - Domande frequenti su A4T{#classifications-a-t-faq}

Questo argomento contiene le risposte alle domande frequenti sulle classificazioni e sull&#39;utilizzo di [!DNL Analytics] come origine di reporting per [!DNL Target] (A4T).

## Dopo aver utilizzato la funzione di importazione classificazioni per scaricare le classificazioni, come associo un nome di attività al valore post-tnt-action? {#section_6045DAC488B248418F430E663C38D001}

È possibile scaricare le classificazioni per la stringa A4T/TNT dalla funzione di [importazione classificazioni](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html) degli Strumenti di amministrazione. La variabile è denominata “TNT” nell’elenco di esportazione. I dati scaricati includono i nomi descrittivi per attività, esperienze e così via.

Questo file di consultazione è utile per i clienti che ricevono il feed di dati clickstream di Adobe. Il file fornisce nomi descrittivi per le colonne `post_tnt` e `post_tnt_action`.

Il formato stringa della variabile TNT è `activityID:experienceID:targettype|event`.

* targettype = 0 (control/random) o 1 (targeting) per le attività [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target].
* Event = 0 rappresenta l’entrata di un’esperienza.
* Event = 1 rappresenta una visita all’esperienza.
* Event = 2 rappresenta l’impression di un’attività.
* Evento = 3-32766 rappresenta l&#39;ID della metrica di successo dell&#39;analisi.
* Event = 32767 rappresenta una conversione di attività.

È possibile importare il file di classificazione in modo frequente dall&#39;interfaccia utente utilizzando un [browser import](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/browser-import.html) o un [FTP import](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/import-file.html). È inoltre possibile interagire con i Servizi di ingegneria per ottenere il file come una tabella di consultazione insieme a un feed di dati clickstream.
