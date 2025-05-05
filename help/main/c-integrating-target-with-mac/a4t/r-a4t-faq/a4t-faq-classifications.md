---
keywords: faq;domande frequenti;analytics for target;a4T;classificazioni;classificazione;classificazioni importazione;post-tnt-action;codici evento
description: Risposte alle domande sulle classificazioni e sull'utilizzo di [!UICONTROL Analytics for Target] (A4T).
title: Dove posso trovare informazioni sulle classificazioni con A4T?
feature: Analytics for Target (A4T)
exl-id: 875f6c1c-1bda-40a9-96f2-d58c00d91d20
source-git-commit: aff96eca1380f4274dba0c1567f6e41d42f4b5ab
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 24%

---

# Classificazioni - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande più frequenti sulle classificazioni e sull&#39;utilizzo di [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target] (A4T).

## Dopo aver utilizzato [!UICONTROL Classifications Importer] per scaricare le classificazioni, come associo un nome di attività al valore post-tnt-action? {#section_6045DAC488B248418F430E663C38D001}

+++Risposta
È possibile scaricare le classificazioni per la stringa A4T/TNT dagli strumenti di amministrazione [Importazione classificazioni](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html?lang=it). La variabile è denominata &quot;TNT&quot; nell’elenco di esportazione. I dati scaricati includono i nomi descrittivi per attività, esperienze e così via.

Questo file di ricerca è utile per i clienti che ricevono il feed di dati clickstream di [!DNL Adobe]. Il file fornisce nomi descrittivi per le colonne `post_tnt` e `post_tnt_action`.

Per le attività standard [!UICONTROL A/B Test] e [!UICONTROL Experience Targeting] (XT), il formato della stringa TNT è:

```
activityID:experienceID:targettype|event
```

Per le attività [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target], il formato della stringa TNT è:

```
activityId:experienceId:targettype:algorithmId|event
```

* `targettype` = `targettype` e `algorithmId` sono identificatori interni utilizzati da [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target] attività.
* Event = 0 rappresenta l’entrata di un’esperienza.
* Event = 1 rappresenta una visita all’esperienza.
* Event = 2 rappresenta l’impression di un’attività.
* L’evento = 3-32766 rappresenta l’ID della metrica di successo di Analytics.
* Event = 32767 rappresenta una conversione di attività.
* L’evento -1 o 65535 indica che l’utente viene rimosso dall’attività o dall’esperienza. Questa situazione si verifica spesso quando il visitatore si converte. Il visitatore viene rilasciato dall’esperienza ed è ora disponibile per qualificarsi per qualsiasi altra esperienza.

Puoi importare il file di classificazione con regolarità dall&#39;interfaccia utente utilizzando [importazione browser](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/browser-import.html?lang=it) o [importazione FTP](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/import-file.html?lang=it). È inoltre possibile interagire con i Servizi di ingegneria per ottenere il file come una tabella di consultazione insieme a un feed di dati clickstream.

+++
