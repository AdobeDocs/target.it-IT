---
title: Creazione degli attributi di contesto
description: Scopri come creare e organizzare gli attributi di contesto e i gruppi di contesto nei flag in modo da poterli utilizzare nei criteri di pubblico.
hide: true
source-git-commit: 9c6f2b72f964b06da51e1f3655545147d7240a93
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 5%

---

# Creazione degli attributi di contesto {#creating-your-context-attributes}

Gli attributi di contesto sono campi dati personalizzati che descrivono il contesto dell’utente, della sessione o dell’applicazione (ad esempio, il livello di abbonamento, la versione dell’app o l’area geografica). Utilizza gli attributi di contesto per definire i criteri di pubblico per i flag di funzione.

I gruppi di contesto organizzano gli attributi di contesto correlati in una gerarchia logica. Utilizzare i gruppi di contesto per semplificare la ricerca e la gestione degli attributi durante la configurazione delle feature.

| Termine | Descrizione | Utilizzato in |
| --- | --- | --- |
| **Attributo contesto** | Un campo denominato con un tipo di dati e valori predefiniti facoltativi. | Criteri di pubblico, configurazione della funzione |
| **Gruppo di contesto** | Categoria che organizza gli attributi di contesto correlati. | Selezione del contesto durante la creazione di una feature |
| **Etichetta interfaccia utente** | Il nome visualizzato nell’interfaccia utente. | Pagine per i criteri e l’amministrazione del pubblico |
| **ID** | Un identificatore tecnico univoco. | Richieste di applicazione |
| **Valori predefiniti** | Elenco facoltativo di valori consentiti con etichette di visualizzazione. | Elenchi a discesa e generatori di regole per il pubblico |

## Prerequisiti {#prerequisites}

Prima di gestire gli attributi di contesto e i gruppi di contesto, completare le operazioni seguenti:

* Hai accesso alla **console Flag** nella sandbox corretta.
* Hai il ruolo **Amministratore** necessario per creare e gestire attributi di contesto e gruppi di contesto.

## Passa ad Attributi contestuali {#navigate}

1. Accedi alla **console Flag**.
1. Nel menu di navigazione a sinistra, in **Dashboard**, seleziona **Attributi contestuali**.

Sei nella pagina **Attributi contestuali**. Utilizzare questa pagina per creare gruppi e attributi di contesto.

## Creare un gruppo di contesto {#create-group}

Ogni attributo di contesto deve appartenere a un gruppo.

1. Nel menu di navigazione a sinistra, in **Dashboard**, seleziona **Attributi contestuali**.
1. Nella scheda **Attributi contesto utente** selezionare **Aggiungi gruppo**.
1. Completate i campi richiesti.
1. Seleziona **Crea**.

### Raggruppa campi {#group-fields}

| Campo | Descrizione |
| --- | --- |
| **Nome gruppo** | Immettere un nome univoco per il gruppo. |
| **Crea un sottogruppo di** | Selezionare un gruppo padre per organizzare la gerarchia. È inoltre possibile creare un gruppo durante la creazione di un attributo. |

## Creare un attributo di contesto {#create-attribute}

1. Nella scheda **Attributi contesto utente** selezionare **Nuovo attributo contesto**.
1. Completate i campi richiesti.
1. Seleziona **Invia**.

### Campi attributo {#attribute-fields}

| Campo | Descrizione |
| --- | --- |
| **Etichetta interfaccia utente** | Inserisci il nome visualizzato utilizzato nei criteri di pubblico. |
| **ID** | Immettere un identificatore tecnico univoco utilizzato nelle richieste di applicazione. |
| **Gruppo di contesto** | Selezionare un gruppo o crearne uno nuovo in linea. |
| **Tipo di dati** | Seleziona il tipo che corrisponde ai dati inviati dall&#39;applicazione. |

| Tipo di dati | Esempio |
| --- | --- |
| STRINGA | `gold` |
| NUMERO INTERO | `42` |
| BOOLEANO | `true` |
| DECIMALE | `9.99` |
| DATA | `2026-07-17` |
| VERSIONE | `1.2.0` |

### Valori predefiniti (facoltativo) {#predefined-values}

Utilizzare valori predefiniti per limitare un attributo a un set fisso di valori. Selezionare **Aggiungi valori predefiniti**.

| Campo | Descrizione |
| --- | --- |
| **Etichetta interfaccia utente** | Inserisci il nome visualizzato. |
| **Valore** | Immettere il valore tecnico inviato dall&#39;applicazione. |

Seleziona **Salva** per applicare le modifiche.

## Risoluzione dei problemi relativi al {#troubleshooting}

| Problema | Risoluzione |
| --- | --- |
| **Crea** è disabilitato | Completa sia **Nome gruppo** che **Crea un sottogruppo di**. |
| Impossibile inviare un attributo | Completare **ID** e **Gruppo contesto**. |
| Gruppo non visibile nel menu a discesa | Aggiorna la pagina o crea il gruppo in linea dal modulo dell’attributo. |
| Valori predefiniti non salvati | Seleziona **Salva** nel modale prima di inviare l&#39;attributo. |

## Vedi anche {#see-also}

* [Creazione e utilizzo dei set di regole](creating-and-using-rule-sets.md)
* [Usa contesto nelle regole del pubblico](using-context-in-audience-rules.md)
* [Pubblico nei flag di funzione e nei gruppi di funzioni](audience-in-feature-flags-and-feature-groups.md)

<!-- -->
