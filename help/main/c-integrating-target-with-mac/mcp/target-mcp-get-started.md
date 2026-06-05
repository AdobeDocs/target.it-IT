---
solution: Target
product: target
title: Introduzione al server Adobe Target MCP
description: Scopri come collegare il server Adobe Target MCP all’assistente AI, compresi i prerequisiti, la configurazione client e la risoluzione dei problemi.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
source-git-commit: d5d7a57ce6a3188f02e680c24849d773cb53457a
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%

---

# Introduzione al server MCP [!DNL Adobe Target] {#target-mcp-get-started}

>[!AVAILABILITY]
>
>Il server MCP [!DNL Adobe Target] è disponibile per tutti i clienti in **Beta pubblico**. Attualmente è supportato in **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor** e **ChatGPT**.

In questa pagina vengono illustrati tutti gli elementi necessari per connettere il server MCP [!DNL Adobe Target] all&#39;assistente AI e verificare la configurazione.

>[!IMPORTANT]
>
>Il Model Context Protocol (MCP) è uno standard open source emergente e può presentare rischi per la sicurezza o l&#39;affidabilità. Le integrazioni server MCP di Adobe e la relativa documentazione vengono fornite &quot;così come sono&quot;, senza garanzie di alcun tipo.
>
>La connessione di client o server MCP ai prodotti Adobe è una configurazione scelta dal cliente e i clienti sono responsabili della valutazione della sicurezza e dell’idoneità di qualsiasi integrazione MCP. Adobe non è responsabile dei problemi derivanti da configurazione errata, utilizzo errato di MCP, vulnerabilità in implementazioni di terze parti o azioni non intenzionali eseguite tramite flussi di lavoro abilitati per MCP.
>
>Per ridurre i rischi, Adobe incoraggia a testare le integrazioni in un ambiente sandbox prima di utilizzarle in modo produttivo e a rivedere e convalidare attentamente tutte le azioni e le risposte avviate da MCP prima di confermarle o di fare affidamento su di esse.

## Prerequisiti {#mcp-prerequisites}

Prima di collegare il server MCP [!DNL Adobe Target] al client MCP, verificare quanto segue:

* Hai una licenza [!DNL Adobe Target] attiva (abbonamento Adobe Experience Cloud) con un&#39;organizzazione Adobe Experience Platform.
* Hai un’applicazione compatibile con MCP supportata (attualmente Claude Web, Claude Desktop, Claude Code, Cursor o ChatGPT).
* Hai [!DNL Adobe Target] autorizzazioni configurate in Adobe Admin Console. In Public Beta, tutti i 23 strumenti disponibili sono di sola lettura. **Il ruolo osservatore** o superiore è sufficiente per utilizzare il server MCP.

>[!NOTE]
>
>Gli strumenti di scrittura (creazione, aggiornamento, attivazione, disattivazione) non sono esposti tramite il catalogo MCP pubblico in Public Beta. I privilegi del ruolo Editor e Approvatore non consentono di sbloccare strumenti aggiuntivi in questo momento. L’accesso in scrittura sarà disponibile in una versione futura.

## Connetti il server MCP [!DNL Adobe Target] {#mcp-connect}

>[!NOTE]
>
>Il server MCP [!DNL Adobe Target] utilizza OAuth 2.0 per l&#39;autenticazione. Quando utilizzi uno strumento MCP di Target per la prima volta, vieni reindirizzato ad Adobe Experience Cloud per effettuare l’accesso, selezionare la tua organizzazione e concedere le autorizzazioni richieste. Non sono richieste credenziali statiche.

**Per connettersi da Claude Desktop o Claude Web:**

1. Apri le impostazioni del client MCP e aggiungi un nuovo server MCP.
1. Immettere l&#39;URL del server: `https://targetmcp.adobe.io/mcp`
1. Quando richiesto, completa l’accesso Adobe IMS OAuth con le credenziali Adobe Experience Cloud.
1. Una volta autenticati, tutti gli strumenti sono immediatamente disponibili. Prova &quot;Elenca tutte le attività Target attive&quot; per verificare la connessione.

**Per connettersi da Claude Code:**

Aggiungi quanto segue alla configurazione di Claude Code MCP:

```json
{
  "mcpServers": {
    "adobe-target": {
      "url": "https://targetmcp.adobe.io/mcp"
    }
  }
}
```

Quando richiesto al primo utilizzo, completa il flusso del browser OAuth.

**Per connettersi dal cursore:**

1. Apri **Cursore** e passa a **Impostazioni** → **MCP** → **Aggiungi nuovo server MCP globale**.
1. Aggiungi la seguente configurazione:

```json
{
  "mcpServers": {
    "target": {
      "type": "streamable-http",
      "url": "https://targetmcp.adobe.io/mcp"
    }
  }
}
```

1. Salva la configurazione. Il server MCP [!DNL Target] verrà visualizzato nei server MCP disponibili.

>[!TIP]
>
>Se vengono visualizzate attività o dati dell’organizzazione errata, esci completamente da Adobe Experience Cloud, ricollega il server MCP e seleziona con attenzione l’organizzazione corretta durante la riautenticazione.

## Risoluzione dei problemi relativi al {#mcp-troubleshooting}

+++Il flusso OAuth non riesce o viene reindirizzato in modo errato

1. Esci completamente da Adobe Experience Cloud.
1. Cancella i cookie del browser per i domini adobe.com.
1. Riprovare il flusso di autenticazione.
1. Quando richiesto, assicurati di selezionare l’organizzazione corretta.
+++

+++Vengono visualizzate le attività o i dati dell’organizzazione errata

1. Esci completamente da Adobe Experience Cloud.
1. Disconnettere e riconnettere il server MCP nelle impostazioni client.
1. Selezionare con attenzione l&#39;organizzazione corretta durante la riautenticazione.
+++

+++Uno strumento restituisce un messaggio di errore

1. Verifica di avere **il ruolo Osservatore** o superiore in [!DNL Adobe Target] (vedi [Prerequisiti](#mcp-prerequisites)).
1. Verifica che nell’organizzazione siano presenti le risorse, ovvero attività, offerte e tipi di pubblico, a cui si fa riferimento.
1. Verifica che gli ID attività e gli altri identificatori siano corretti.
+++

+++Impossibile connettersi al server MCP

1. Verifica la connessione Internet.
1. Verifica che l’URL del server MCP sia immesso correttamente nella configurazione client.
1. Provare a rimuovere e aggiungere nuovamente il server nelle impostazioni client MCP.
+++

## Sicurezza e autorizzazioni {#mcp-security}

Il server MCP [!DNL Adobe Target] può accedere solo ai dati per i quali l&#39;account utente Adobe dispone dell&#39;autorizzazione per visualizzare o modificare. Tutte le operazioni rispettano le assegnazioni di ruolo [!DNL Target] e le autorizzazioni dell&#39;area di lavoro.

Il server richiede i seguenti ambiti OAuth:

* `AdobeID` — Identità Adobe di base
* `openid` — Autenticazione di connessione OpenID
* `additional_info.projectedProductContext` — Individuazione tenant
* `read_organizations` — Operazioni a livello di organizzazione
* `additional_info.roles` — Controllo degli accessi basato sul ruolo

I token OAuth vengono convalidati su Adobe IMS a ogni richiesta, non vengono memorizzati in modo persistente dal server MCP e tutte le comunicazioni utilizzano HTTPS.

## Risorse correlate {#mcp-get-started-related}

* [Panoramica](target-mcp.md)
* [Casi d’uso e procedure dettagliate](target-mcp-use-cases.md)
* [Riferimento strumenti server MCP](target-mcp-tools-reference.md)
* [Documentazione di Model Context Protocol](https://modelcontextprotocol.io/introduction){target="_blank"}
* [Riferimento API amministratore [!DNL Adobe Target]](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
