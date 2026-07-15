---
title: Eseguire l’onboarding dell’applicazione
description: Scopri come integrare una nuova applicazione nei flag per iniziare a creare e gestire i flag di funzioni.
hide: true
exl-id: d88c27a5-f490-4504-9764-5e4ce98fdf20
source-git-commit: 35fa45d2a5374dcc47a02bb737f28f24847d7fc6
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---

# Eseguire l’onboarding dell’applicazione {#onboard-your-application}

Per aggiungere una nuova applicazione è necessario avere il ruolo **Amministratore**. Contatta l’amministratore se devi verificare o aggiornare il tuo ruolo.

## Aggiungi una nuova applicazione {#add-application}

1. Accedi alla console Flag e passa a **Flag > Applicazioni**.

   >[!NOTE]
   >
   >Se il pulsante **Nuova applicazione** non è visibile, verificare di disporre del ruolo **Amministratore**.

2. Selezionare **Nuova applicazione**.

3. Seleziona la **piattaforma** che corrisponde al tipo di applicazione (web o mobile).

4. Fornisci le seguenti informazioni:

   I campi contrassegnati con * sono obbligatori.

   | Campo | Descrizione |
   | --- | --- |
   | **Nome applicazione*** | Nome visualizzato per l&#39;applicazione. |
   | **ID applicazione*** | Identificatore univoco utilizzato per chiamare i flag dal codice. Utilizza l’ID client dell’applicazione. |
   | **Intervallo di polling** | Intervallo di polling (in secondi) per l&#39;aggiornamento della cache per applicazione. Si applica solo agli SDK lato server. |

5. Seleziona **Aggiungi**. L’applicazione è ora registrata ed è pronta per la configurazione del flag di funzione.

## Cosa succede dopo {#next-steps}

Dopo aver effettuato l’onboarding dell’applicazione, puoi iniziare a creare i flag di funzione:

* [Creare il primo flag di funzione](../feature-flags/create-your-first-feature-flag.md)
* [Integrare i flag nell’app](../integrate/integrating-in-your-app.md)

## Vedi anche {#see-also}

* [Gestire le applicazioni](manage-applications.md)
* [Accedi alla console](../console/log-in-to-the-console.md)

<!-- -->
