---
keywords: faq;domande frequenti;analytics for target;a4T;classificazioni;classificazione;importatore di classificazioni;post-tnt-action
description: Trova le risposte alle domande sulle classificazioni e sull’utilizzo di Analytics per le attività [!DNL Target] (A4T). A4T lets you use Analytics reporting for [!DNL Target] .
title: Dove posso trovare informazioni sulle classificazioni con A4T?
feature: Analytics for Target (A4T)
exl-id: 875f6c1c-1bda-40a9-96f2-d58c00d91d20
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 59%

---

# Classificazioni - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande più frequenti sulle classificazioni e sull’utilizzo di [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target] (A4T).

## Dopo aver utilizzato la funzione di importazione classificazioni per scaricare le classificazioni, come associo un nome di attività al valore post-tnt-action? {#section_6045DAC488B248418F430E663C38D001}

È possibile scaricare le classificazioni per la stringa A4T/TNT dalla funzione di [importazione classificazioni](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html) degli Strumenti di amministrazione. La variabile è denominata “TNT” nell’elenco di esportazione. I dati scaricati includono i nomi descrittivi per attività, esperienze e così via.

Questo file di consultazione è utile per i clienti che ricevono il feed di dati clickstream di Adobe. Il file fornisce nomi descrittivi per le colonne `post_tnt` e `post_tnt_action`.

Il formato stringa della variabile TNT è `activityID:experienceID:targettype|event`.

* targettype = 0 (control/random) o 1 (target) per le attività [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico].
* Event = 0 rappresenta l’entrata di un’esperienza.
* Event = 1 rappresenta una visita all’esperienza.
* Event = 2 rappresenta l’impression di un’attività.
* Event = 3-32766 rappresenta l’id della metrica di successo di analytics.
* Event = 32767 rappresenta una conversione di attività.

Puoi importare il file di classificazione con frequenza dall&#39;interfaccia utente utilizzando un [importazione browser](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/browser-import.html) o un [importazione FTP](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/import-file.html). È inoltre possibile interagire con i Servizi di ingegneria per ottenere il file come una tabella di consultazione insieme a un feed di dati clickstream.
