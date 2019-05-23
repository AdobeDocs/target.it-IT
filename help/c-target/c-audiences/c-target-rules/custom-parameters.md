---
description: I parametri personalizzati sono parametri mbox. Se li trasmetti alle mbox, o utilizzi la funzione targetPageParams, questi parametri vengono visualizzati qui e possono essere utilizzati nei tipi di pubblico.
keywords: parametri personalizzati;parametri personalizzati di target;targetpageparams;parametri mbox di targeting
seo-description: I parametri personalizzati sono parametri mbox. Se li trasmetti alle mbox, o utilizzi la funzione targetPageParams, questi parametri vengono visualizzati qui e possono essere utilizzati nei tipi di pubblico.
seo-title: Parametri personalizzati
solution: Target
title: Parametri personalizzati
topic: Standard
uuid: a9eb62a6-e86a-4e7b-922c-ad87570435ba
translation-type: tm+mt
source-git-commit: f59e96cd5afcae9d27d730aecead9eb360f04026

---


# Parametri personalizzati{#custom-parameters}

I parametri personalizzati sono parametri mbox. Se li trasmetti alle mbox, o utilizzi la funzione targetPageParams, questi parametri vengono visualizzati qui e possono essere utilizzati nei tipi di pubblico.

Per ulteriori informazioni, consulta [Trasmettere i parametri a una mbox globale](https://marketing.adobe.com/resources/help/en_US/target/ov/c_pass_parameters_to_global_mbox.html).

Durante la creazione di un pubblico personalizzato basato su un parametro mbox, `mboxParameter` non richiede più di specificare `mboxName`. Il nome dell&#39;elemento mbox è ora opzionale. Questa modifica ti consente di utilizzare parametri da più elementi mbox o di fare riferimento a un parametro che non è ancora stato registrato sul bordo.

Per selezionare il parametro desiderato:

* Mentre crei un nuovo pubblico, seleziona il nome di un parametro dall&#39;elenco, comincia a digitare i primi caratteri del parametro desiderato o il nome intero.
* Se ricordi il nome mbox ma non il nome del parametro, usa la casella di controllo per filtrare una mbox nota trasmettendo il parametro desiderato.

Con uno di questi metodi, non esiste alcun collegamento tra mbox e il parametro. Il pubblico funzionerà sulla base del parametro su tutte le mbox che trasmettono tale parametro.

Se modifichi un pubblico esistente, i criteri di filtraggio vengono visualizzati con il nome mbox fornito durante la creazione.

I [dettagli della definizione di una scheda a comparsa](../../../c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) del pubblico visualizzano il nome del parametro nella sezione Regole. Non esiste un riferimento al mbox utilizzato per il filtraggio.

>[!NOTE]
>
>Per i tipi di pubblico personalizzati creati prima della versione 18.5.1 di Target (22 maggio 2018), i nomi mbox non verranno visualizzati nella scheda a comparsa di definizione del pubblico. È necessario salvare nuovamente il pubblico personalizzato per far sì che il nome mbox venga mostrato nella scheda.

## Video di formazione: Creazione di tipi di pubblico

Questo video contiene informazioni sull&#39;utilizzo delle categorie di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392)