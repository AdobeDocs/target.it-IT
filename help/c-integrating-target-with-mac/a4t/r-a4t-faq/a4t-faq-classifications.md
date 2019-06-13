---
description: Questo argomento contiene le risposte alle domande più frequenti sulle classificazioni e sull’utilizzo di Analytics come origine per la generazione di rapporti per Target (A4T).
keywords: faq;domande frequenti;analytics for target;a4T;classificazioni;classificazione;importatore di classificazioni;post-tnt-action
seo-description: Questo argomento contiene le risposte alle domande più frequenti sulle classificazioni e sull’utilizzo di Analytics come origine per la generazione di rapporti per Target (A4T).
seo-title: Classificazioni - Domande frequenti su A4T
solution: Target
title: Classificazioni - Domande frequenti su A4T
topic: Standard
uuid: 4b42adbc-4fa8-4b62-86c8-bb8f8bec7e54
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Classificazioni - Domande frequenti su A4T{#classifications-a-t-faq}

Questo argomento contiene le risposte alle domande più frequenti sulle classificazioni e sull’utilizzo di Analytics come origine per la generazione di rapporti per Target (A4T).

## Dopo aver utilizzato la funzione di importazione classificazioni per scaricare le classificazioni, come associo un nome di attività al valore post-tnt-action? {#section_6045DAC488B248418F430E663C38D001}

Scarica le classificazioni per la stringa A4T/TNT dalla [funzione di importazione classificazioni](https://marketing.adobe.com/resources/help/it_IT/reference/c_working_with_saint.html) degli strumenti di amministrazione. La variabile è denominata “TNT” nell’elenco di esportazione. I dati scaricati includono i nomi descrittivi per attività, esperienze e così via.

Questo file di consultazione è utile per i clienti che ricevono il feed di dati clickstream di Adobe. Il file fornisce nomi descrittivi per le colonne `post_tnt` e `post_tnt_action`.

Il formato stringa della variabile TNT è `activityID:experienceID:targettype|event`.

* targettype sarà sempre 0 per A4T.
* Event = 0 rappresenta l’entrata di un’esperienza.
* Event = 1 rappresenta una visita all’esperienza.
* Event = 2 rappresenta l’impression di un’attività.
* Event = 32767 rappresenta una conversione di attività.

Scarica il file delle classificazioni con regolarità dall’interfaccia utente tramite un’[esportazione del browser](https://marketing.adobe.com/resources/help/it_IT/reference/browser_export.html) o un’[esportazione FTP](https://marketing.adobe.com/resources/help/it_IT/reference/ftp_export.html). È inoltre possibile interagire con i Servizi di ingegneria per ottenere il file come una tabella di consultazione insieme a un feed di dati clickstream.
