---
keywords: Adobe Target;Collaboratore;IA;abilità;sperimentazione;Consigli
title: Competenze dei collaboratori per Adobe Target
description: Scopri le competenze di Collaboratore disponibili per Adobe Target, tra cui l’individuazione delle attività, la creazione di test, l’analisi, la composizione del pubblico e la risoluzione dei problemi relativi ai Consigli.
feature: Overview
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
source-git-commit: 4b90f47050b63c7e1e6ac5019d45a7b99b3a33b8
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 2%
---

# Competenze dei collaboratori per Adobe Target {#coworker-skills}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri le abilità di coorker disponibili per Adobe Target, incluse le abilità per esplorare attività e pubblico, creare e configurare test, analizzare le prestazioni, comporre tipi di pubblico e gestire consigli.

>[!ENDSHADEBOX]

Le competenze dei collaboratori consentono ai professionisti di Adobe Target di utilizzare il linguaggio naturale per esplorare i programmi di test e personalizzazione, creare e configurare attività, analizzare i risultati e risolvere problemi di consegna. Descrivi cosa desideri fare in Chat con i collaboratori, quindi controlla i consigli, la configurazione o l’analisi restituiti prima di agire.

Gli strumenti MCP di [!DNL Adobe Target] e il collaboratore sono documentati separatamente e forniscono diverse funzionalità:

* [MCP](../c-integrating-target-with-mac/mcp/target-mcp-tools-reference.md) di destinazione documenta i singoli strumenti esposti dal server MCP diretto, inclusi i tipi di attività, i parametri, le autorizzazioni e l&#39;ambito di lettura o scrittura supportati.
* [Collaboratore](https://experienceleague.adobe.com/it/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/overview#target-activities-and-audiences) fornisce un livello di orchestrazione del linguaggio naturale separato che può combinare le funzionalità e applicare flussi di lavoro aggiuntivi.

La tabella seguente presenta un confronto ad alto livello delle funzionalità correlate.

| Funzionalità | MCP di destinazione | Collaboratore |
| --- | --- | --- |
| Elencare esperimenti in esecuzione, pubblico, offerte o elementi modificati di recente | Sì | Sì |
| Creare un’attività di Automated Personalization | No | No |
| Creare un pubblico Target | Sì | Sì |
| Creare un’attività VEC di Target, un’attività Targeting esperienza o un test A/B | Sì | Sì |
| Creare un’attività Consigli di Target | Sì | Sì |
| Creare un’offerta HTML o JSON in Target | Sì | Sì |
| Utilizzare un frammento di contenuto di AEM in un’attività Target | No | Sì |
| Consigliare cosa funziona e cosa testare dopo | Nessun consiglio o consiglio generico | Sì |


## Plug-in di Target

Le seguenti abilità sono disponibili nel plug-in **Target**:

* **Sfoglia Target**

  Rilevamento, ispezione e conteggio in sola lettura delle entità Target, incluse attività, tipi di pubblico, offerte e configurazione correlata.

>[!BEGINSHADEBOX]

*Esempi di prompt:*

* &quot;Elencare le attività attive&quot;
* &quot;Quante attività sono attualmente in esecuzione?&quot;
* &quot;Mostrami i tipi di pubblico e le offerte utilizzati da questa attività.&quot;

>[!ENDSHADEBOX]

* **Verdetto attività Target**

  Determina se un&#39;attività è pronta per essere spedita, deve attendere ulteriori dati, deve arrestarsi o richiede una correzione, utilizzando calcoli di significatività e controlli di configurazione.

>[!BEGINSHADEBOX]

*Esempi di prompt:*

* &quot;Dovrei spedire questo test?&quot;
* &quot;Questa attività è pronta per essere interrotta?&quot;
* &quot;La configurazione dell’attività corrente presenta problemi?&quot;

>[!ENDSHADEBOX]

* **Progettazione destinazione**

  Crea e configura attività e offerte, genera URL di controllo qualità e crea o ottimizza il contenuto delle offerte.

>[!BEGINSHADEBOX]

*Esempi di prompt:*

* &quot;Crea un test A/B per la pagina home.&quot;
* &quot;Crea un’offerta per l’esperienza del visitatore di ritorno.&quot;
* &quot;Genera un URL di controllo qualità per questa attività.&quot;

>[!ENDSHADEBOX]

* **VEC di Target**

  Crea e modifica le attività del Compositore esperienza visivo e i relativi tipi di pubblico per la distribuzione delle pagine.

>[!BEGINSHADEBOX]

*Esempi di prompt:*

* &quot;Crea un test A/B VEC per la home page.&quot;
* &quot;Modifica il titolo principale protagonista nell’attività del Compositore esperienza visivo.&quot;
* &quot;Crea un pubblico per la consegna delle pagine per questa attività del Compositore esperienza visivo.&quot;

>[!ENDSHADEBOX]

* **Installazione di Target**

  Le guide completano la creazione di attività A/B, Targeting esperienza o Compositore esperienza visivo, inclusi i prerequisiti, la pianificazione, il QA e l’attivazione.

>[!BEGINSHADEBOX]

    *Esempi di prompt:*
    
    * &quot;Aiutaci a creare il mio primo test.&quot;
    * &quot;Cosa mi serve prima di creare un&#39;attività Targeting esperienza?&quot;
    * &quot;Fammi vedere durante la pianificazione, il controllo qualità e l&#39;attivazione di questa attività.&quot;

>[!ENDSHADEBOX]

* **Informazioni di Target**

  Audit Programmi di Target per rischi, collisioni, configurazioni errate, problemi di igiene e risultati positivi rapidi.

>[!BEGINSHADEBOX]

*Esempi di prompt:*

* &quot;Controlla le attività Target&quot;
* &quot;Trovare conflitti o rischi di configurazione tra le mie attività.&quot;
* &quot;Quali risultati rapidi possono migliorare l’igiene del mio programma Target?&quot;

>[!ENDSHADEBOX]

* **Stratega target**

  Analizza i dati storici di Target per i pattern vincenti e consiglia test futuri.

>[!BEGINSHADEBOX]

*Esempi di prompt:*

* &quot;Cosa devo testare dopo in base ai risultati passati?&quot;
* &quot;Quali modelli vengono visualizzati nei test con le prestazioni più elevate?&quot;
* &quot;Consiglia un test di follow-up basato sui risultati di questa attività.&quot;

>[!ENDSHADEBOX]

* **Calcolatore test di destinazione**

  Pianifica la dimensione del campione A/B/n, la durata e l&#39;incremento rilevabile per le metriche di conversione e ricavi, con la correzione Bonferroni per più confronti.

>[!BEGINSHADEBOX]

*Esempi di prompt:*

* &quot;Di quale dimensione campione ho bisogno?&quot;
* &quot;Per quanto tempo devo eseguire questo test A/B per rilevare un incremento del 5%?&quot;
* &quot;Quale incremento rilevabile posso misurare con questo traffico?&quot;

>[!ENDSHADEBOX]

* **Report Portfolio di destinazione**

  Fornisce aggregazioni delle prestazioni di sola lettura a livello di programma, analisi delle tendenze delle attività e dello slancio.

>[!BEGINSHADEBOX]

*Esempi di prompt:*

* &quot;Quali sono i miei test migliori e peggiori?&quot;
* &quot;Mostrami le tendenze delle prestazioni nelle mie attività.&quot;
* &quot;Quali attività hanno guadagnato o perso slancio di recente?&quot;

>[!ENDSHADEBOX]

* **Compositore pubblico di destinazione**

  Crea o modifica i tipi di pubblico nativi di Target da descrizioni in linguaggio naturale o da regole esplicite.

>[!BEGINSHADEBOX]

*Esempi di prompt:*

* &quot;Crea un pubblico per i visitatori di ritorno da dispositivi mobili.&quot;
* &quot;Modifica questo pubblico per includere i visitatori della ricerca organica.&quot;
* &quot;Crea un pubblico Target per i visitatori che hanno visualizzato la pagina dei prezzi.&quot;

>[!ENDSHADEBOX]

* **Consigli di Target**

  Gestisce e lavora con le attività e le configurazioni di Target Recommendations.

>[!BEGINSHADEBOX]

*Esempi di prompt:*

* &quot;Creare un’attività Consigli.&quot;
* &quot;Mostra le attività e le configurazioni consigliate&quot;.
* &quot;Aggiorna le impostazioni per questa attività Consigli.&quot;

>[!ENDSHADEBOX]

* **Diagnosi consigli di destinazione**

  Diagnostica i problemi relativi a distribuzione, configurazione, catalogo e feed dei consigli.

>[!BEGINSHADEBOX]

*Esempi di prompt:*

* &quot;Perché i miei consigli non vengono visualizzati?&quot;
* &quot;Diagnosticare la configurazione del feed e del catalogo per questa attività Consigli.&quot;
* &quot;I problemi di consegna o configurazione influiscono sui consigli?&quot;

>[!ENDSHADEBOX]
