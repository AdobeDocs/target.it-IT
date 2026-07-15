---
title: Creare il primo flag di funzione
description: Scopri come creare un flag di funzione in Flag, impostare un pubblico e testarlo prima di distribuirlo agli utenti.
hide: true
exl-id: ae115120-8da9-465e-a556-c17591ea7054
source-git-commit: 045bd3321fd4041fe7f723ce300a400102ed7274
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 1%

---

# Creare il primo flag di funzione {#create-feature-flag}

## Prerequisiti {#prerequisites}

Prima di creare un flag di feature, effettuate le seguenti operazioni:

* Si dispone dell&#39;accesso alla console Flag. Vedere [Accedere alla console](../console/log-in-to-the-console.md)
* L&#39;applicazione è stata integrata. Vedere [Eseguire l&#39;installazione dell&#39;applicazione](../applications/onboard-your-application.md)
* Hai il ruolo **Sviluppatore** o **Proprietario versione prodotto**

## Passaggio 1: creare il flag di funzione {#create}

Per creare un nuovo flag di funzione, effettua le seguenti operazioni nella console:

1. Accedi alla console Flag e passa a **Funzionalità e versioni > Flag di funzionalità**.
1. Seleziona l&#39;applicazione dal menu a discesa **Applicazione**.
1. Seleziona **Nuova funzionalità**.
1. Compila i campi modulo:

   | Campo | Descrizione |
   | --- | --- |
   | **Nome** | Etichetta di visualizzazione per il flag di funzione. Non utilizzato nel codice. |
   | **Chiave*** | Identificatore utilizzato nel codice per valutare il flag. Non può essere modificato dopo la creazione. |
   | **Descrizione** | Descrizione facoltativa a scopo di documentazione. |
   | **Metadati** | Facoltativo. Fino a 1.024 caratteri. Utilizza questo campo per eventuali metadati aggiuntivi da associare al flag. |
   | **Identità*** | L’identità rispetto alla quale viene valutato il flag (ad esempio, ECID). Questa è l’identità passata nella richiesta di funzione. |
   | **Rollout percentuale** | La percentuale del pubblico definito a cui viene fornita questa funzione. Il valore predefinito è 100%. Consulta [Impostare una funzione per il rollout graduale](set-feature-gradual-rollout.md). |

   I campi contrassegnati con * sono obbligatori.

>[!IMPORTANT]
>
>La **Chiave** è l&#39;identificatore utilizzato nel codice e non può essere modificato dopo la creazione. Le chiavi **non possono contenere spazi** e sono **sensibili a maiuscole e minuscole**. **Name** è solo un&#39;etichetta di visualizzazione e non viene utilizzato nel codice; i due sono indipendenti (il nome non viene convertito nella chiave). L&#39;immissione di uno spazio nel campo Chiave genera l&#39;errore: _&quot;Valore non valido per la chiave di funzionalità.&quot;_

1. Facoltativamente, aggiungi un criterio di pubblico (vedi Passaggio 2).
1. Salva le impostazioni dei flag di funzione.

## Passaggio 2: aggiungere un criterio di pubblico {#audience}

I criteri di pubblico controllano quali utenti visualizzano la funzione. Puoi eseguire il targeting degli utenti con **attributi di contesto**, valori inviati dal sito Web o dall&#39;app nella richiesta di funzionalità (ad esempio `locale` o `platform`). Combinale con **AND**, **OR** e **NOT**. Vedi [Usa contesto nelle regole del pubblico](../audience/using-context-in-audience-rules.md).

Per aggiungere criteri di pubblico, vai alla scheda **Pubblico** durante la creazione o la modifica di un flag di funzione.

>[!NOTE]
>
>Il ruolo **Sviluppatore** è in modalità sandbox. Gli sviluppatori possono esporre una funzionalità solo a se stessi aggiungendo il proprio ID utente in **Pubblico > Profilo > ID utente**. Per esporre una funzionalità a utenti esterni, è necessario il ruolo **Proprietario della versione del prodotto**.

## Passaggio 3: calcolare la dimensione del pubblico {#audience-size}

Dopo aver aggiunto i criteri di pubblico, seleziona **Calcola** nella barra inferiore per ottenere un conteggio stimato degli utenti idonei per la funzione. Questo consente di convalidare il targeting prima della pubblicazione.

## Passaggio 4: pianificazione (facoltativo) {#schedule}

È possibile pianificare l&#39;attivazione di un flag di funzionalità in una data e un&#39;ora future utilizzando l&#39;opzione **Pianifica** nelle impostazioni del flag di funzionalità.

## Domande frequenti: non è possibile aggiungere un flag di funzione come sviluppatore {#faq}

Il ruolo **Sviluppatore** è in modalità sandbox. Gli sviluppatori possono testare le funzionalità privatamente aggiungendo il proprio ID utente al pubblico. Non possono esporre funzionalità a utenti esterni. Utilizza il ruolo **Proprietario versione prodotto** per rilasciare funzionalità a utenti esterni. Contatta l’amministratore per aggiornare il tuo ruolo.

## Vedi anche {#see-also}

* [Impostare una funzione per il rollout graduale](set-feature-gradual-rollout.md)
* [Creare un gruppo di funzioni](create-a-feature-group.md)

<!-- -->
