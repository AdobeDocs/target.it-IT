---
solution: Target
product: target
title: 'Server MCP Adobe Target: casi d’uso e procedure dettagliate'
description: Esplora i casi d’uso comuni e le procedure dettagliate per la richiesta di informazioni dettagliate per il server MCP di Adobe Target.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
hide: true
source-git-commit: ecb51d828807735b990b8f3a52102feb005bc61b
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 1%

---

# Server MCP [!DNL Adobe Target]: casi d&#39;uso e procedure dettagliate {#target-mcp-use-cases}

>[!BEGINSHADEBOX]

Sommario:

* [Panoramica](target-mcp.md)
* [Introduzione](target-mcp-get-started.md)
* **[Casi d&#39;uso e procedure dettagliate](target-mcp-use-cases.md)**
* [Riferimento strumenti server MCP](target-mcp-tools-reference.md)

>[!ENDSHADEBOX]


>[!IMPORTANT]
>
>Il Model Context Protocol (MCP) è uno standard open source emergente e può presentare rischi per la sicurezza o l&#39;affidabilità. Le integrazioni server MCP di Adobe e la relativa documentazione vengono fornite &quot;così come sono&quot;, senza garanzie di alcun tipo.
>
>La connessione di client o server MCP ai prodotti Adobe è una configurazione scelta dal cliente e i clienti sono responsabili della valutazione della sicurezza e dell’idoneità di qualsiasi integrazione MCP. Adobe non è responsabile dei problemi derivanti da configurazione errata, utilizzo errato di MCP, vulnerabilità in implementazioni di terze parti o azioni non intenzionali eseguite tramite flussi di lavoro abilitati per MCP.
>
>Per ridurre i rischi, Adobe incoraggia a testare le integrazioni in un ambiente sandbox prima di utilizzarle in modo produttivo e a rivedere e convalidare attentamente tutte le azioni e le risposte avviate da MCP prima di confermarle o di fare affidamento su di esse.

In questa pagina vengono illustrate le operazioni che è possibile eseguire con il server MCP [!DNL Adobe Target] utilizzando prompt in linguaggio naturale, dalle ricerche rapide alle attività di gestione attività in più passaggi.

## Casi d’uso {#mcp-use-cases}

Gli esempi seguenti mostrano come interagire con il server MCP [!DNL Adobe Target] utilizzando il linguaggio naturale:

| Obiettivo | Esempio di prompt |
|---|---|
| **Verifica stato esperimento** | &quot;Quali test A/B sono attualmente attivi nella home page? Mostrami lo stato, l’allocazione del traffico e per quanto tempo ciascuno è in esecuzione.&quot; |
| **Valutazione delle prestazioni** | &quot;Mostrami tutti i test attivi che hanno raggiunto una rilevanza statistica — quali esperienze sono vincenti?&quot; |
| **Analisi ricavi** | &quot;Ottieni il rapporto sugli ordini e sui ricavi per l’attività AT4821 e riepiloga quale esperienza genera il maggior numero di ricavi per visitatore.&quot; |
| **Generazione di rapporti per A4T** | &quot;Estrai il rapporto A4T per il test di ottimizzazione del pagamento e riepiloga i dati di conversione lato Analytics.&quot; |
| **Gestione attività** | &quot;Sospendi la 98765 dell’attività e aggiorna la priorità dell’attività 11111 a 200.&quot; |
| **Informazioni sull&#39;attività** | &quot;Ottieni informazioni sul test &#39;Banner per la vendita estiva&#39;: come sono le prestazioni e ci sono anomalie?&quot; |
| **Gestione dell&#39;audience** | &quot;Elenca tutti i tipi di pubblico destinati agli utenti di dispositivi mobili e mostra a quali attività sono associati.&quot; |
| **Controllo qualità e anteprima** | &quot;Genera URL di anteprima Controllo di qualità per le 12345 di attività in modo da poter esaminare tutte le varianti prima dell’attivazione.&quot; |
| **Revisione consigli** | &quot;Elenca tutti i criteri di Recommendations configurati in questo account e riepiloga i tipi di algoritmo in uso.&quot; |
| **Audit dell&#39;implementazione** | &quot;Quale versione di at.js è configurata e quali token di risposta sono attualmente attivi?&quot; |
| **Modifica controllo** | &quot;Mostra tutte le modifiche apportate alle 98765 attività negli ultimi 30 giorni e chi le ha apportate&quot;. |

## Procedure dettagliate sui casi d’uso {#mcp-use-case-walkthroughs}

Nelle procedure dettagliate seguenti viene illustrato come completare le attività comuni utilizzando prompt in linguaggio naturale con il server MCP [!DNL Adobe Target].

+++Creazione di un test A/B

**Prompt:**
&quot;Crea un test A/B denominato &quot;Homepage Hero Image Test&quot; con due esperienze: &quot;Control&quot; che mostra l’eroe corrente e &quot;Variant&quot; che mostra una nuova immagine protagonista a tema estivo. Eseguire il targeting della mbox della pagina home.&quot;

L&#39;assistente AI utilizza lo strumento `create_ab_activity` per creare l&#39;attività con la configurazione descritta. Lo strumento restituisce il nuovo ID attività e una conferma delle esperienze create.

+++

+++Verifica delle prestazioni dell’attività

**Prompt:**
&quot;Mostra le metriche delle prestazioni per l&#39;attività &#39;Ottimizzazione del flusso di cassa&#39; negli ultimi 30 giorni.&quot;

L&#39;assistente AI utilizza `get_ab_performance_report` o `get_xt_performance_report` (a seconda del tipo di attività) per recuperare i tassi di conversione, i conteggi dei visitatori e altre metriche per l&#39;intervallo di tempo specificato.

+++

+++Gestione delle offerte

**Prompt:**
&quot;Crea un&#39;offerta HTML denominata &#39;Banner sulla vendita estiva&#39; con un banner promozionale che riporta &#39;Sconto del 20% su tutti gli articoli estivi&#39;.&quot;

L&#39;assistente AI utilizza lo strumento `create_target_offer` per creare l&#39;offerta con il contenuto HTML specificato e restituisce una conferma con il nuovo ID offerta.

+++

+++Creazione di un pubblico

**Prompt:**
&quot;Crea un pubblico denominato &quot;Mobile Visitors from California&quot; (Visitatori mobili dalla California) che esegue il targeting degli utenti su dispositivi mobili situati in California.&quot;

L&#39;assistente AI utilizza lo strumento `create_target_audience` con le regole di targeting appropriate derivate dalla descrizione.

+++

+++Generazione di collegamenti di anteprima Controllo di qualità

**Prompt:**
&quot;Genera URL di anteprima per 12345 attività in modo da poter testare ogni esperienza.&quot;

L&#39;assistente AI utilizza lo strumento `preview_activity` per generare URL cliccabili che ignorano il targeting del pubblico, consentendo di visualizzare ogni esperienza direttamente nel browser.

+++

+++Creazione di un’attività Targeting esperienze

**Prompt:**
&quot;Crea un’attività Targeting esperienze denominata &quot;Geo Personalization&quot; che mostra diversi banner principali ai visitatori provenienti da aree geografiche diverse.&quot;

L&#39;assistente AI utilizza `create_xt_activity` per creare l&#39;attività con la mappatura dell&#39;esperienza basata sul pubblico in base alle aree che descrivi.

+++

+++Pianificazione di un’attività

**Prompt:**
&quot;Aggiornare la pianificazione delle 12345 di attività che inizieranno il 1° maggio e termineranno il 31 maggio.&quot;

L&#39;assistente AI utilizza lo strumento `update_activity_schedule` per applicare le nuove date di inizio e fine all&#39;attività.

+++

## Risorse correlate {#mcp-use-cases-related}

* [Panoramica](target-mcp.md)
* [Introduzione](target-mcp-get-started.md)
* [Riferimento strumenti server MCP](target-mcp-tools-reference.md)
* [Documentazione di Model Context Protocol](https://modelcontextprotocol.io/introduction){target="_blank"}
* [[!DNL Adobe Target] Riferimento API amministratore](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
