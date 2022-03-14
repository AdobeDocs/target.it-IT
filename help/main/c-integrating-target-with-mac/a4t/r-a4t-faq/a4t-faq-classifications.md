---
keywords: FAQ;domande frequenti;analytics for target;a4T;classificazioni;classificazione;importatore di classificazioni;post-tnt-action;codici evento
description: Trova risposte alle domande sulle classificazioni e sull’utilizzo [!UICONTROL Analytics for Target] (A4T).
title: Dove posso trovare informazioni sulle classificazioni con A4T?
feature: Analytics for Target (A4T)
exl-id: 875f6c1c-1bda-40a9-96f2-d58c00d91d20
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 29%

---

# Classificazioni - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande più frequenti sulle classificazioni e sull’utilizzo [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target] (A4T).

## Dopo aver utilizzato [!UICONTROL Importazione classificazioni] per scaricare le classificazioni, come associo il valore post-tnt-action a un nome di attività? {#section_6045DAC488B248418F430E663C38D001}

È possibile scaricare le classificazioni per la stringa A4T/TNT dalla funzione di [importazione classificazioni](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html) degli Strumenti di amministrazione. La variabile è denominata “TNT” nell’elenco di esportazione. I dati scaricati includono i nomi descrittivi per attività, esperienze e così via.

Questo file di ricerca è utile per i clienti che ricevono [!DNL Adobe]Feed di dati clickstream di . Il file fornisce nomi descrittivi per le colonne `post_tnt` e `post_tnt_action`.

Per standard [!UICONTROL Test A/B] e [!UICONTROL Targeting esperienza] (XT), il formato della stringa TNT è:

```
activityID:experienceID:targettype|event
```

Per [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] attività, il formato della stringa TNT è:

```
activityId:experienceId:targettype:algorithmId|event
```

* `targettype` = `targettype` e `algorithmId` sono identificatori interni utilizzati da [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] attività.
* Event = 0 rappresenta l’entrata di un’esperienza.
* Event = 1 rappresenta una visita all’esperienza.
* Event = 2 rappresenta l’impression di un’attività.
* Event = 3-32766 rappresenta l’id della metrica di successo di analytics.
* Event = 32767 rappresenta una conversione di attività.
* L’evento -1 o 65535 rappresenta la rimozione dell’utente dall’attività o dall’esperienza. Questa situazione si verifica spesso quando il visitatore si converte. Il visitatore viene rilasciato dall’esperienza ed è ora disponibile per qualificarsi per qualsiasi altra esperienza.

Puoi importare frequentemente il file di classificazione dall’interfaccia utente utilizzando un [importazione browser](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/browser-import.html?lang=en) o [Importazione FTP](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/import-file.html?lang=en). È inoltre possibile interagire con i Servizi di ingegneria per ottenere il file come una tabella di consultazione insieme a un feed di dati clickstream.
