---
keywords: Panoramica e riferimento;WebKit;cookie;prime parti;terze parti;1st-party;3rd-party
description: Scopri il comportamento dei cookie  [!DNL Target] di prima parte (cookie di prima parte, cookie di terze parti con cookie di prima parte o solo cookie di terze parti).
title: Dove posso trovare informazioni su [!DNL Target] Cookie?
feature: at.js
role: Developer
exl-id: 1c4e5b0b-8ae4-4526-aea0-318a33f4d247
source-git-commit: e773db20ac593108aa3e54aae1bcb2c0f713e387
workflow-type: tm+mt
source-wordcount: '1542'
ht-degree: 58%

---

# Cookie di Target

Il comportamento del cookie dipende dal fatto di essere un cookie di prima parte, un cookie di terze parti con un cookie di prima parte oppure un cookie di terze parti.

>[!NOTE]
>
>Questo argomento contiene informazioni su `mboxSession` e `mboxPC`. Le best practice di implementazione consigliano di non collegare o archiviare informazioni sensibili con i dati dei cookie: `mboxSession` o `mboxPC`.

Vedi anche [Elimina il cookie di Target](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cookie-deleting.md).

## Quando utilizzare un cookie di prima parte o di terze parti {#section_F71B29420C004A7FA3B1921E619B326E}

Il cookie da utilizzare dipende dalla configurazione del sito. Per comprendere i cookie di prima parte e di terze parti, è utile comprendere il funzionamento di [!DNL Target] . Per ulteriori informazioni, consulta [Come [!DNL Adobe Target] funziona](/help/c-intro/how-target-works.md#concept_459AB4DEE7364A9290C2FD405DC29584) .

I casi d’uso principali per i cookie sono tre:

1. Un dominio.

   Tutti i test vengono eseguiti all’interno di un dominio di primo livello (`www.domain.com`, `store.domain.com`, `anysub.domain.com` e così via).

   Approccio: Utilizza solo cookie di prime parti (impostazione predefinita).

1. Gli utenti passano da un dominio all’altro e tu intendi tenere traccia e sottoporre a test il loro comportamento tra i diversi domini.

   Esempio: un utente accede al sito per acquistare, ma finalizza l’acquisto attraverso i negozi Yahoo. Tre approcci possibili (consulta il rappresentante commerciale di riferimento per determinare quello più adatto):

   * Abilitare i cookie di prima parte e di terze parti.
   * Abilitare solo i cookie di terze parti (raro, ma ha il vantaggio di mantenere il cookie mbox fuori dal tuo dominio).
   * Abilitare solo i cookie di prima parte e trasmettere il parametro `mboxSession` quando si passa a un altro dominio.

      Il parametro `mboxSession` deve essere trasmesso a una pagina di destinazione e riferito dalla libreria JavaScript (Adobe Experience Platform Web SDK o at.js). Non può trattarsi di una pagina di reindirizzamento intermedia.

1. Utilizzi solo adbox o Flashbox su un sito di terze parti.

   Due approcci possibili (collabora con il rappresentante commerciale di riferimento per determinare quello più adatto):

   * Abilitare i cookie di prima parte e di terze parti.

      I cookie di prima parte e di terze parti sono necessari per Flashbox e risorse creative dinamiche.

   * Abilitare solo i cookie di terze parti.

      Questo approccio è adatto solo nel raro caso in cui le implementazioni AdBox vengano utilizzate senza destinazione sul sito.

## Comportamento del cookie di prima parte {#section_CE6313D979EA4D0897D2F661E7A8AFA7}

Il cookie di prima parte viene memorizzato in [!DNL clientdomain.com], dove `clientdomain` rappresenta il tuo dominio.

La libreria JavaScript genera un `mboxSession ID` e lo memorizza nel cookie [!DNL Target] . La prima risposta mbox contiene l&#39;offerta e il JavaScript per memorizzare l&#39; `mboxPC ID` generato dall&#39;applicazione, nel cookie mbox.

>[!NOTE]
>
>Il cookie di prima parte [!DNL AMCV_###@AdobeOrg] è sempre impostato con l’[!DNL Experience Cloud Visitor ID].

## Comportamento di cookie di terze parti {#section_4C3A83990BF8415BB1806602D84AED48}

Il cookie di terze parti viene memorizzato in [!DNL clientcode.tt.omtrdc.net] e il cookie di prima parte in [!DNL clientdomain.com], dove `clientdomain` rappresenta il tuo dominio.

La libreria JavaScript genera un `mboxSession ID`. La prima richiesta di posizione restituisce intestazioni di risposta HTTP che tentano di impostare cookie di terze parti denominati `mboxSession` e `mboxPC` e viene inviata nuovamente una richiesta di reindirizzamento con un parametro aggiuntivo (`mboxXDomainCheck=true`).

Se il browser accetta cookie di terze parti, la richiesta di reindirizzamento li include e viene restituita l’offerta.

Se il browser rifiuta i cookie di terze parti, la richiesta di reindirizzamento non include i cookie e viene visualizzato il contenuto predefinito per tutte le posizioni nella pagina. Data l’assenza di cookie impostati, lo stesso processo di cui sopra si ripete a ogni richiesta di pagina.

>[!NOTE]
>
>Il cookie [!DNL demdex.net] viene impostato se i cookie di terze parti non sono bloccati.

## Comportamento di cookie di terze parti e di prima parte {#section_F0C9AD8BFDF8457A999C4A07A0F7A981}

Il cookie di terze parti viene memorizzato in [!DNL clientcode.tt.omtrdc.net] e il cookie di prima parte in [!DNL clientdomain.com], dove `clientdomain` rappresenta il tuo dominio.

La libreria JavaScript genera un `mboxSession ID`. La prima richiesta di posizione restituisce intestazioni di risposta HTTP che tentano di impostare cookie di terze parti denominati `mboxSession` e `mboxPC` e viene inviata nuovamente una richiesta di reindirizzamento con un parametro aggiuntivo (`mboxXDomainCheck=true`).

Se il browser accetta cookie di terze parti, la richiesta di reindirizzamento li include e viene restituita l’offerta.

Alcuni browser rifiutano i cookie di terze parti. Se il cookie di terze parti è bloccato, il cookie di prima parte continua a funzionare. [!DNL Target] tenta di impostare il cookie di terze parti e, se non è in grado di farlo, [!DNL Target] può solo tenere traccia del dominio specifico del cliente. Il tracciamento tra domini diversi non funziona se il cookie di terze parti è bloccato, a meno che il `mboxSession` non venga aggiunto al collegamento che attraversa più domini. In questo caso, un altro cookie di prima parte viene impostato e sincronizzato con il cookie di prima parte del dominio precedente.

## Impostazioni dei cookie {#section_B498B8D1A34A444BBF84CC720EE9D87F}

Il cookie dispone di diverse impostazioni predefinite. Puoi modificare queste impostazioni, se necessario, fatta eccezione per la durata del cookie. In caso di modifica delle impostazioni dei cookie, rivolgiti al rappresentante di riferimento per il tuo account.

| Impostazione | Informazioni |
|--- |--- |
| Nome cookie | mbox. |
| Dominio cookie | Il primo e il secondo livello dei domini da cui viene distribuito il contenuto. Dato che viene distribuito dal dominio della società, il cookie è un cookie di prime parti.<br>Esempio: `mycompany.com`. |
| Dominio server | `clientcode.tt.omtrdc.net`, utilizzando il codice cliente per il tuo account. |
| Durata cookie | Il cookie rimane sul browser del visitatore due settimane dall’ultimo accesso. Non puoi modificare la durata del cookie. |
| Policy P3P | Il cookie viene pubblicato con una policy P3P, come richiesto dall’impostazione predefinita nella maggior parte dei browser. Una policy P3P indica a un browser chi sta servendo il cookie e come vengono utilizzate le informazioni. |

Il cookie mantiene diversi valori per gestire l’esperienza dei visitatori nelle campagne:

| Valore | Definizione |
|--- |--- |
| session ID | Un ID univoco per una sessione utente. Per impostazione predefinita, l&#39;ID dura 30 minuti. |
| pc ID | Un ID semi-permanente per il browser di un visitatore. Dura 14 giorni. |
| check | Un semplice valore di test utilizzato per determinare se un visitatore supporta i cookie. Impostato ogni volta che un visitatore richiede una pagina. |
| disable | Impostato se il tempo di caricamento del visitatore supera il timeout configurato nel file di libreria JavaScript. Per impostazione predefinita, questo valore dura un&#39;ora. |

## Impatto su [!DNL Target] per i visitatori di Safari a causa di modifiche nel monitoraggio di Apple WebKit {#section_2A2E5730ED7D4A0985C904AFEA310AAE}

**Come funziona  [!DNL Adobe Target] il tracciamento?**

| Cookie | Dettagli |
|--- |--- |
| Domini di prima parte | Implementazione standard per i clienti [!DNL Target] . I cookie &quot;mbox&quot; sono impostati nel dominio del cliente. |
| Tracciamento di terze parti | Il tracciamento di terze parti è importante per i casi di utilizzo per pubblicità e targeting in [!DNL Target] e in [!DNL Adobe Audience Manager] (AAM). Il tracciamento di terze parti richiede tecniche di scripting tra siti. [!DNL Target] utilizza due cookie, &quot;mboxSession&quot; e &quot;mboxPC&quot;, impostati nel dominio `clientcode.tt.omtrd.net`. |
**Qual è l’approccio di Apple?**

Da Apple:

“Intelligent Tracking Prevention è una nuova funzionalità di WebKit che riduce il tracciamento tra siti limitando ulteriormente i cookie e altri dati del sito Web.”

“Questo è ciò che viene chiamato tracciamento tra siti e il cookie utilizzato da `example-tracker.com` è chiamato un cookie di terze parti. Durante i test abbiamo trovato siti Web popolari con oltre 70 tracker simili, che raccolgono in silenzio dati sugli utenti.”

| Approccio | Dettagli |
|--- |--- |
| Intelligent Tracking Prevention | Per ulteriori informazioni, consulta [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention/) sul sito web del motore di ricerca open source WebKit. |
| Cookie | Come Safari gestisce i cookie:<ul><li>I cookie di terze parti che non si trovano in un dominio a cui l’utente accede direttamente non vengono mai salvati. Questo comportamento non è una novità. I cookie di terze parti già non sono supportati in Safari.</li><li>I cookie di terze parti impostati in un dominio a cui l’utente accede direttamente vengono eliminati dopo 24 ore.</li><li>I cookie di prima parte vengono eliminati dopo 30 giorni se il dominio di prima parte è stato classificato come dominio che traccia gli utenti tra siti diversi. Questo problema può essere applicato alle grandi aziende che inviano utenti a diversi domini online. Apple non ha chiarito come esattamente questi domini vengono classificati, o come un dominio può determinare se sono stati classificati come responsabili del tracciamento degli utenti tra siti diversi.</li></ul> |
| Apprendimento automatico per identificare i domini che sono tra siti diversi | Da Apple:<br>Classificatore di apprendimento automatico: Un modello di apprendimento automatico viene utilizzato per classificare quali domini principali controllati privatamente possono tracciare l’utente tra siti diversi, in base alle statistiche raccolte. Dalle varie statistiche raccolte, sono emersi tre vettori con un segnale forte per la classificazione basata sulle pratiche di tracciamento correnti: sottorisorsa per il numero di domini univoci, sottostruttura per il numero di domini univoci e infine numero di domini univoci di reindirizzamento. La raccolta e la classificazione di tutti i dati avviene sul dispositivo.<br>Tuttavia, se l’utente interagisce con  `example.com` come dominio principale, spesso denominato dominio di prima parte, Intelligent Tracking Prevention lo considera un segnale di interesse dell’utente verso il sito web e regola temporaneamente il suo comportamento come descritto in questa timeline:<br>Se l’utente ha interagito con  `example.com` le ultime 24 ore, i suoi cookie sono disponibili quando  `example.com` è di terze parti. Questa pratica consente scenari di login come &quot;Accedi con il mio account X su Y&quot;.<ul><li>I domini che vengono visitati come dominio di primo livello non sono interessati. Ad esempio, siti come OKTA</li><li>Identifica i domini che sono sottodominio o sottostruttura della pagina corrente in più domini univoci.</li></ul> |

**In che modo viene influenzato l’Adobe?**

| Funzionalità interessate | Dettagli |
|--- |--- |
| Supporto per rinuncia | Le modifiche di tracciamento WebKit di Apple interrompono il supporto dell’opzione di rinuncia.<br>[!DNL Target]La funzione di rinuncia di utilizza un cookie nel dominio `clientcode.tt.omtrdc.net`. Per ulteriori dettagli, consulta [Privacy](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md).<br>[!DNL Target] supporta due tipi di rinuncia:<ul><li>Uno per il cliente (il cliente gestisce il collegamento di rinuncia).</li><li>Una tramite [!DNL Adobe] che esclude l’utente da tutte le funzionalità [!DNL Target] per tutti i clienti.</li></ul>Entrambi i metodi utilizzano il cookie di terze parti. |
| [!DNL Target] attività | I clienti possono scegliere la [durata del profilo](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md) per i propri account [!DNL Target] (fino a 90 giorni). Il problema è che se la durata del profilo dell’account è superiore a 30 giorni e il cookie di prima parte viene eliminato perché il dominio del cliente è stato contrassegnato come dominio di tracciamento degli utenti tra siti diversi, i visitatori Safari saranno interessati dalle seguenti aree in [!DNL Target]:<br>**[!DNL Target] reports **: Se un utente Safari accede a un’attività , ritorna dopo 30 giorni e quindi si converte, viene conteggiato come due visitatori e una conversione.<br>[!DNL Analytics]Questo comportamento è lo stesso per le attività che utilizzano come origine per la generazione di rapporti (A4T).<br>** Profilo e appartenenza **all’attività:<ul><li>I dati del profilo vengono cancellati quando scade il cookie di prima parte.</li><li>L’appartenenza all’attività viene cancellata quando scade il cookie di prima parte.</li><li> [!DNL Target] non funziona in Safari per gli account che utilizzano un’implementazione di cookie di terze parti oppure di cookie di prima parte e di terze parti. Questo comportamento non è una novità. Safari non consente i cookie di terze parti da un po&#39;.</li></ul><br>**Suggerimenti**: Se si teme che il dominio del cliente possa essere contrassegnato come un dominio che tiene traccia dei visitatori attraverso sessioni diverse, è più sicuro impostare la durata del profilo in  [!DNL Target] a un massimo di 30 giorni. Questo limite garantisce che gli utenti siano tracciati in modo simile in Safari e in tutti gli altri browser. |
