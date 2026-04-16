---
solution: Target
product: target
title: Hosting autonomo del server Adobe Target MCP
description: Scopri come eseguire la tua istanza del server MCP di Adobe Target utilizzando Python, Docker o un ambiente di sviluppo locale.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: Developer
level: Experienced
hide: true
source-git-commit: 782256b734068075795d5e9c1f3f552ca48918e6
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 2%

---

# Hosting autonomo del server MCP [!DNL Adobe Target] {#target-mcp-self-hosted}

>[!BEGINSHADEBOX]

Sommario:

* [Utilizzo dei client MCP](target-mcp.md)
* [Riferimento strumenti server MCP](target-mcp-tools-reference.md)
* **[Hosting autonomo del server MCP](target-mcp-self-hosted.md)**

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>La distribuzione self-hosted è destinata agli sviluppatori e agli utenti avanzati che richiedono il controllo completo del runtime del server MCP [!DNL Adobe Target]. Per la maggior parte degli utenti, si consiglia l&#39;endpoint ospitato (`https://targetmcp.adobe.io/mcp`). Vedi [Operazioni con i client MCP](target-mcp.md).

In questa pagina viene illustrato come clonare, configurare ed eseguire un&#39;istanza personalizzata del server MCP [!DNL Adobe Target]. L&#39;hosting autonomo è utile quando hai bisogno di un ambiente di sviluppo locale, di una configurazione di rete personalizzata o desideri contribuire alla base di codice del server.

## Prerequisiti {#self-hosted-prereqs}

Prima di iniziare, assicurati di avere i seguenti elementi:

* **Python 3.13 o versione successiva**
* **[uv](https://github.com/astral-sh/uv){target="_blank"}** — Gestione progetti e pacchetto Fast Python

  ```bash
  curl -LsSf https://astral.sh/uv/install.sh | sh
  ```

* Una licenza [!DNL Adobe Target] attiva con accesso a Adobe Experience Cloud
* **Credenziali artifactory** (solo per utenti interni Adobe): necessarie per installare dipendenze interne

## Installazione {#self-hosted-install}

**1. Clona l&#39;archivio:**

```bash
git clone https://github.com/Adobe-TnT/target-mcp.git
cd target-mcp
```

**2. Crea e attiva un ambiente virtuale:**

```bash
uv venv --python 3.13
source .venv/bin/activate
```

**3. Configura variabili di ambiente:**

```bash
cp env.example .env
```

Apri `.env` e sostituisci i valori dei segnaposto con le credenziali e le impostazioni dell&#39;organizzazione.

**4. Dipendenze di installazione:**

```bash
make uv-install
```

**5. Avvia il server:**

Scegli la modalità che corrisponde al tuo caso d’uso:

| Modalità | Comando | Usa quando |
|---|---|---|
| StreamableHTTP (server API) | `make run-api-server` | Connessione di un client MCP tramite HTTP |
| STDIO (client MCP locale) | `make run-mcp-stdio` | Utilizzo della comunicazione diretta dei processi |

## Connettere un client MCP a un server locale {#self-hosted-connect}

### Cursore

Aggiungi quanto segue alla configurazione MCP cursore. Sostituisci i valori dei segnaposto con il token IMS e l’ID organizzazione effettivi:

```json
{
  "mcpServers": {
    "target-local": {
      "url": "http://localhost:8080/mcp",
      "headers": {
        "Authorization": "Bearer {IMS_USER_TOKEN}",
        "x-gw-ims-org-id": "{IMS_ORGANIZATION_ID}"
      }
    }
  }
}
```

### Claude Code

Aggiungi una voce al file di configurazione MCP Claude Code che punta al server locale:

```json
{
  "mcpServers": {
    "target-local": {
      "url": "http://localhost:8080/mcp"
    }
  }
}
```

>[!NOTE]
>
>Quando ci si connette a un server locale, le intestazioni di autenticazione devono essere passate manualmente (come mostrato nell’esempio Cursore precedente). Il flusso del browser OAuth è disponibile solo con l&#39;endpoint `https://targetmcp.adobe.io/mcp` ospitato.

## Distribuzione Docker {#self-hosted-docker}

L’archivio include una configurazione Docker Compose per le distribuzioni in contenitori.

**Esegui con Docker composto:**

```bash
make run-dc
```

**Generare ed eseguire direttamente l&#39;immagine Docker:**

```bash
make build
make run-docker
```

## Endpoint API {#self-hosted-endpoints}

Il server con hosting autonomo espone i seguenti endpoint HTTP:

| Endpoint | Descrizione |
|---|---|
| `/mcp` | Endpoint del protocollo MCP per i client di IA |
| `/ping` | Controllo Liveness — restituisce `"Pong"` |
| `/health` | Verifica stato — restituisce `{"status": "healthy"}` |
| `/validate` | Endpoint di convalida input |
| `/authorize` | Endpoint di autorizzazione OAuth |
| `/token` | Endpoint token OAuth |

**Esempio di verifica stato:**

```bash
curl http://localhost:8080/health
# Response: {"status": "healthy"}
```

## Risoluzione dei problemi relativi al {#self-hosted-troubleshoot}

+++Avvio del server non riuscito

1. Verificare che Python 3.13+ sia installato: `python --version`
1. Verificare che l&#39;ambiente virtuale sia attivato: `source .venv/bin/activate`
1. Verificare che tutte le variabili di ambiente in `.env` siano impostate correttamente.
1. Eseguire di nuovo `make uv-install` per assicurarsi che tutte le dipendenze siano presenti.

+++

+++Impossibile connettersi dal client MCP

1. Verificare che il server sia in esecuzione e che la porta sia accessibile: `curl http://localhost:8080/ping`
1. Verifica che l’URL del server nella configurazione del client MCP corrisponda all’indirizzo del server in esecuzione.
1. Per Cursor, accertati che l&#39;intestazione `Authorization` contenga un token IMS valido e non scaduto.

+++

+++Installazione delle dipendenze non riuscita (utenti interni di Adobe)

1. Conferma che le credenziali dell’artifactory siano configurate correttamente.
1. Verifica la connessione di rete all’istanza interna Artifactory.
1. Contatta il contatto DevOps del tuo team o il contatto di progettazione della piattaforma per l’accesso agli artefatti.

+++

## Risorse correlate {#self-hosted-related}

* [Operazioni con i client MCP](target-mcp.md): configurazione dell&#39;endpoint ospitato e riferimento allo strumento
* [Documentazione di Model Context Protocol](https://modelcontextprotocol.io/introduction){target="_blank"}
* [[!DNL Adobe Target] Riferimento API amministratore](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
