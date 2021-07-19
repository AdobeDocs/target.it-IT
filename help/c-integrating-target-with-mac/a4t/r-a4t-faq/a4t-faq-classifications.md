---
keywords: FAQ;domande frequenti;analytics for target;a4T;classificazioni;classificazione;importatore di classificazioni;post-tnt-action;codici evento
description: Trova le risposte alle domande sulle classificazioni e sull’utilizzo di Analytics per le attività [!DNL Target] (A4T). A4T lets you use Analytics reporting for [!DNL Target] .
title: Dove posso trovare informazioni sulle classificazioni con A4T?
feature: Analytics for Target (A4T)
exl-id: 875f6c1c-1bda-40a9-96f2-d58c00d91d20
source-git-commit: 8917fe56b7150d897e0d12b67b1914ef7cc8e92d
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 46%

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
* L’evento -1 o 65535 rappresenta la rimozione dell’utente dall’attività o dall’esperienza. Questa situazione si verifica spesso quando il visitatore si converte. Il visitatore viene rilasciato dall’esperienza ed è ora disponibile per qualificarsi per qualsiasi altra esperienza.

Puoi importare il file di classificazione con frequenza dall&#39;interfaccia utente utilizzando un [importazione browser](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/browser-import.html?lang=en) o un [importazione FTP](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/import-file.html?lang=en). È inoltre possibile interagire con i Servizi di ingegneria per ottenere il file come una tabella di consultazione insieme a un feed di dati clickstream.
