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
source-git-commit: 53dc7056ca62339a682756fe1b39e6af349f3ae6
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 1%

---

# Server MCP [!DNL Adobe Target]: casi d&#39;uso e procedure dettagliate {#target-mcp-use-cases}

>[!AVAILABILITY]
>
>Il server MCP [!DNL Adobe Target] è disponibile per tutti i clienti in **Beta pubblico**. Attualmente è supportato in **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor** e **ChatGPT**.

In questa pagina sono illustrate le operazioni che è possibile eseguire con il server MCP [!DNL Adobe Target] utilizzando prompt in linguaggio naturale, dalle ricerche rapide alle attività di analisi e reporting in più passaggi.

>[!IMPORTANT]
>
>Il Model Context Protocol (MCP) è uno standard open source emergente e può presentare rischi per la sicurezza o l&#39;affidabilità. Le integrazioni server MCP di Adobe e la relativa documentazione vengono fornite &quot;così come sono&quot;, senza garanzie di alcun tipo.
>
>La connessione di client o server MCP ai prodotti Adobe è una configurazione scelta dal cliente e i clienti sono responsabili della valutazione della sicurezza e dell’idoneità di qualsiasi integrazione MCP. Adobe non è responsabile dei problemi derivanti da configurazione errata, utilizzo errato di MCP, vulnerabilità in implementazioni di terze parti o azioni non intenzionali eseguite tramite flussi di lavoro abilitati per MCP.
>
>Per ridurre i rischi, Adobe incoraggia a testare le integrazioni in un ambiente sandbox prima di utilizzarle in modo produttivo e a rivedere e convalidare attentamente tutte le azioni e le risposte avviate da MCP prima di confermarle o di fare affidamento su di esse.

## Casi d’uso {#mcp-use-cases}

Gli esempi seguenti mostrano come interagire con il server MCP [!DNL Adobe Target] utilizzando il linguaggio naturale:

| Obiettivo | Esempio di prompt |
|---|---|
| **Verifica stato esperimento** | &quot;Quali test A/B sono attualmente attivi nella home page? Mostrami lo stato, l’allocazione del traffico e per quanto tempo ciascuno è in esecuzione.&quot; |
| **Valutazione delle prestazioni** | &quot;Mostrami tutti i test attivi che hanno raggiunto una rilevanza statistica — quali esperienze sono vincenti?&quot; |
| **Analisi ricavi** | &quot;Ottieni il rapporto sugli ordini e sui ricavi per l’attività AT4821 e riepiloga quale esperienza genera il maggior numero di ricavi per visitatore.&quot; |
| **Generazione rapporti A4T** | &quot;Estrai il rapporto A4T per il test di ottimizzazione del pagamento e riepiloga i dati di conversione lato Analytics.&quot; |
| **Informazioni sull&#39;attività** | &quot;Ottieni informazioni sul test &#39;Banner per la vendita estiva&#39;: come sono le prestazioni e ci sono anomalie?&quot; |
| **Gestione dell&#39;audience** | &quot;Elenca tutti i tipi di pubblico destinati agli utenti di dispositivi mobili e mostra a quali attività sono associati.&quot; |
| **Controllo qualità e anteprima** | &quot;Genera URL di anteprima Controllo di qualità per le 12345 di attività in modo da poter esaminare tutte le varianti prima dell’attivazione.&quot; |
<!-- | **Recommendations review** | "List all Recommendations criteria configured in this account and summarize the algorithm types in use." | -->
| **Audit dell&#39;implementazione** | &quot;Quale versione di at.js è configurata e quali token di risposta sono attualmente attivi?&quot; |
| **Modifica controllo** | &quot;Mostra tutte le modifiche apportate alle 98765 di attività negli ultimi 30 giorni e chi le ha apportate.&quot; |

## Procedure dettagliate sui casi d’uso {#mcp-use-case-walkthroughs}

Nelle procedure dettagliate seguenti viene illustrato come completare le attività comuni utilizzando prompt in linguaggio naturale con il server MCP [!DNL Adobe Target].

<!--
+++Creating an A/B test

**Prompt:**
"Create an A/B test called 'Homepage Hero Image Test' with two experiences: 'Control' showing the current hero and 'Variant' showing a new summer-themed hero image. Target the homepage mbox."

The AI assistant uses the `create_ab_activity` tool to create the activity with the configuration you described. The tool returns the new activity ID and a confirmation of the created experiences.

+++
-->

+++Verifica delle prestazioni dell’attività

**Richiesta:**
&quot;Mostra le metriche delle prestazioni per l&#39;attività &#39;Ottimizzazione del flusso di cassa&#39; negli ultimi 30 giorni.&quot;

L&#39;assistente AI utilizza `get_ab_performance_report` o `get_xt_performance_report` (a seconda del tipo di attività) per recuperare i tassi di conversione, i conteggi dei visitatori e altre metriche per l&#39;intervallo di tempo specificato.

+++

<!--
+++Managing offers

**Prompt:**
"Create an HTML offer called 'Summer Sale Banner' with a promotional banner that says '20% off all summer items'."

The AI assistant uses the `create_target_offer` tool to create the offer with your specified HTML content and returns a confirmation with the new offer ID.

+++

+++Building an audience

**Prompt:**
"Create an audience called 'Mobile Visitors from California' that targets users on mobile devices located in California."

The AI assistant uses the `create_target_audience` tool with the appropriate targeting rules derived from your description.

+++
-->

+++Generazione di collegamenti di anteprima Controllo di qualità

**Richiesta:**
&quot;Genera URL di anteprima per 12345 attività in modo da poter testare ogni esperienza.&quot;

L&#39;assistente AI utilizza lo strumento `preview_activity` per generare URL cliccabili che ignorano il targeting del pubblico, consentendo di visualizzare ogni esperienza direttamente nel browser.

+++

<!--
+++Creating an Experience Targeting activity

**Prompt:**
"Create an Experience Targeting activity called 'Geo Personalization' that shows different hero banners to visitors from different regions."

The AI assistant uses `create_xt_activity` to build the activity with audience-based experience mapping according to the regions you describe.

+++

+++Scheduling an activity

**Prompt:**
"Update the schedule for activity 12345 to start on May 1st and end on May 31st."

The AI assistant uses the `update_activity_schedule` tool to apply the new start and end dates to the activity.

+++
-->

## Risorse correlate {#mcp-use-cases-related}

* [Panoramica](target-mcp.md)
* [Introduzione](target-mcp-get-started.md)
* [Riferimento strumenti server MCP](target-mcp-tools-reference.md)
* [Documentazione di Model Context Protocol](https://modelcontextprotocol.io/introduction){target="_blank"}
* [Riferimento API amministratore [!DNL Adobe Target]](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
