---
keywords: Targeting;compositore esperienza visivo;whitelist;whitelist;compositore;elenco consentiti;compositore esperienza visivo avanzato;vec;risoluzione dei problemi compositore esperienza visivo;risoluzione dei problemi;eec;esperienza avanzata;tls;tls 1.2
description: Scopri come risolvere i problemi che a volte si verificano nel [!DNL Target] [!UICONTROL Compositore esperienza visivo] (VEC) e nel [!UICONTROL Compositore esperienza avanzato] (EEC) in determinate condizioni.
title: Come posso risolvere i problemi relativi al [!UICONTROL Compositore esperienza visivo] e al [!UICONTROL Compositore esperienza avanzato]?
feature: Visual Experience Composer (VEC)
exl-id: d829cd63-950f-4bb4-aa58-0247f85de383
TQID: 'https://experienceleague.adobe.com/4v7Qe-Yzjke-GceUSRDO2SMZGkxvrkdsSXQt8TR-bic'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '1218'
ht-degree: 13%
---
# Risoluzione dei problemi relativi a [!DNL Adobe Target] [!UICONTROL Compositore esperienza visivo] e [!UICONTROL Compositore esperienza avanzato] {#vec-eec-issues}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come risolvere i problemi che interessano sia il **[!UICONTROL Compositore esperienza visivo]** (VEC) che il **[!UICONTROL Compositore esperienza avanzato]** (EEC).

>[!ENDSHADEBOX]

In determinate condizioni si verificano problemi di visualizzazione e altri problemi nel [!DNL Target] **[!UICONTROL Compositore esperienza visivo]** e nel **[!UICONTROL Compositore esperienza avanzato]**. Gli elementi seguenti descrivono i problemi che interessano entrambi i compositori e come risolverli.

## Browser e sicurezza

### Criteri per cookie SameSite di Google Chrome {#samesite}

I criteri di imposizione dei cookie SameSite di [!DNL Google Chrome] influiscono sul Compositore esperienza visivo e sul Compositore esperienza avanzato nelle seguenti versioni.

>[!NOTE]
>
>La seguente modifica si applica a tutte e tre le versioni. Impossibile utilizzare il Compositore esperienza visivo nelle pagine protette da password del sito a meno che l&#39;estensione [VEC Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) non sia installata e abilitata. I cookie di accesso del sito sono considerati cookie di terze parti, pertanto non vengono inviati con richieste di accesso nell&#39;editor del Compositore esperienza visivo in modalità **[!UICONTROL Sfoglia]**. L&#39;unica eccezione si verifica quando per i cookie di accesso sono già impostati gli attributi `SameSite=None` e `Secure`.

* **Chrome 94 (21 settembre 2021):** Per tutti gli utenti con Chrome 94 e versioni successive, il flag della riga di comando `--disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure` è stato rimosso.
* **Chrome 91 (25 maggio 2021):** Per tutti gli utenti con Chrome 91 e versioni successive, i flag `#same-site-by-default-cookies` e `#cookies-without-same-site-must-be-secure` sono stati rimossi da `chrome://flags`. Questo comportamento è ora abilitato per impostazione predefinita.
* **Chrome 80 (agosto 2020):** Per tutti gli utenti con Chrome 80 e versioni successive:

  * Impossibile scaricare [!DNL Target] librerie durante la modifica di un&#39;attività se non sono già nel sito. La chiamata di download viene effettuata dal dominio del cliente a un dominio [!DNL Adobe] protetto e viene rifiutata perché non autenticata.
  * Il Compositore esperienza avanzato non funziona perché non può impostare l&#39;attributo SameSite per i cookie nel dominio `adobemc.com`. Senza questo attributo, il browser rifiuta questi cookie, causando il mancato funzionamento del Compositore esperienza avanzato.

+++ Determinare quali cookie sono bloccati

Per determinare quali cookie sono bloccati dai criteri di imposizione dei cookie SameSite, utilizzare [!DNL Developer Tools] in [!DNL Chrome].

1. Durante la visualizzazione del Compositore esperienza visivo in [!DNL Chrome], fai clic sull&#39;icona **[!UICONTROL puntini di sospensione]** nell&#39;angolo superiore destro di Chrome > **[!UICONTROL Altri strumenti]** > **[!UICONTROL Strumenti per sviluppatori]**.
1. Fai clic sulla scheda **[!UICONTROL Rete]**, quindi cerca i cookie bloccati.

   >[!NOTE]
   >
   >Utilizzare la casella di controllo **[!UICONTROL Contiene cookie bloccati]** per semplificare la ricerca dei cookie bloccati.

+++

+++ Le intestazioni Content Security Policy (CSP) bloccano le librerie [!DNL Target] sul sito Web

Se le intestazioni CSP del sito Web bloccano le librerie [!DNL Target], il sito Web viene caricato ma non è possibile modificarlo. Verificare che le librerie [!DNL Target] non siano bloccate.

>[!NOTE]
>
>Oltre alle seguenti informazioni, è possibile utilizzare l&#39;estensione del browser [Adobe Target VEC Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) per [!DNL Google Chrome].

![Nella console del browser è visualizzata una richiesta bloccata per target.js con il messaggio di violazione della direttiva Content Security Policy](assets/cps_headers.png)

Come soluzione alternativa, configurare una regola [!DNL Requestly] per rimuovere le intestazioni CSP, come illustrato nella figura seguente.

![Finestra di dialogo Requestly, Modifica intestazioni in richieste e risposte HTTP, con una regola denominata Content-Security-Policy che rimuove l&#39;intestazione Content-Security-Policy dalla risposta](assets/cps_headers_2.png)

È possibile configurare una regola [!DNL Requestly] simile per qualsiasi intestazione che impedisca il caricamento di una risorsa nel Compositore esperienza visivo. Ogni volta che è necessario rimuovere le intestazioni con [!DNL Requestly], eseguire una delle operazioni seguenti:

* Aggiungi le regole URL per l’URL da aprire nel Compositore esperienza visivo, in modo che le intestazioni vengano rimosse solo per tali URL.
* Abilita la regola durante la modifica nel Compositore esperienza visivo e disabilita la regola quando il Compositore esperienza visivo non è in uso.

+++

+++ Gli iframe a più livelli non sono supportati

[!DNL Target] non supporta gli iframe a più livelli. Se il sito web carica un iframe che ha un iframe secondario, at.js interagisce solo con l’iframe principale. [!DNL Target] librerie non interagiscono con l&#39;iframe secondario.

Come soluzione alternativa, aggiungi una pagina nell’esperienza con l’URL dell’iframe secondario.

+++

+++ Impossibile modificare le esperienze su un sito non compatibile con iFrame o su pagine senza l&#39;implementazione [!DNL Target]

Abilita **[!UICONTROL Compositore esperienza avanzato]** (EEC) per risolvere questo problema. Fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Compositore esperienza visivo]**, quindi seleziona la casella di controllo che abilita il **[!UICONTROL Compositore esperienza avanzato]**.

Il Compositore esperienza avanzato utilizza un proxy gestito da [!DNL Adobe] per caricare la pagina da modificare. Questo proxy consente la modifica sui siti non compatibili con iFrame e su siti e pagine in cui non è stato ancora aggiunto il codice [!DNL Adobe Target]. Le attività non vengono fornite al sito fino all&#39;aggiunta del codice. Alcuni siti potrebbero non essere caricati tramite il Compositore esperienza avanzato. In questo caso, deselezionando questa opzione, la pagina viene caricata tramite un iFrame.

>[!NOTE]
>
>Le pagine ospitate localmente e le pagine non accessibili all&#39;esterno della rete non sono accessibili al server proxy [!DNL Adobe] e non possono essere aperte nel Compositore esperienza avanzato. Queste pagine potrebbero includere gli URL di staging, i test di accettazione degli utenti (TAU) o le pagine in hosting locale.

+++

## Caricamento e visualizzazione della pagina

+++ Quando si modifica una pagina, viene visualizzato un rotatore invece della pagina

Questa situazione può verificarsi se l’URL contiene un carattere #. Per risolvere il problema, passa alla modalità **[!UICONTROL Sfoglia]** nel Compositore esperienza visivo o Compositore esperienza avanzato, quindi torna alla modalità **[!UICONTROL Componi]**. L’icona che ruota scompare e la pagina viene caricata correttamente.

+++

+++ Il Compositore esperienza visivo o Compositore esperienza avanzato sembra non funzionare o non viene inizializzato quando un’attività salvata viene nuovamente modificata

Se il sito web è stato modificato all’esterno del Compositore esperienza visivo dopo la definizione dell’esperienza, non è possibile trovare i selettori su cui sono state eseguite le azioni in precedenza quando l’attività viene aperta per la modifica. La pagina apparentemente non funziona, senza che venga visualizzato alcun avviso.

+++

+++ I banner rotanti e gli altri contenuti che contengono JavaScript non vengono visualizzati nel Compositore esperienza visivo o Compositore esperienza avanzato

Per impostazione predefinita, il Compositore esperienza visivo blocca gli elementi di JavaScript. La disattivazione di JavaScript consente di lavorare con questi elementi. In base alla configurazione del sito, alcuni elementi potrebbero continuare a essere visualizzati in modo non corretto o rimanere non disponibili.

+++

+++ Per le attività Automated Personalization, lo scambio di immagini nel Compositore esperienza visivo o Compositore esperienza avanzato sembra non funzionare

L&#39;aggiunta dell&#39;offerta di un immagine a una posizione prende la dimensione totale dello spazio immagine originale nel Compositore esperienza visivo e Compositore esperienza avanzato. Alla consegna, l&#39;immagine non viene espansa ed è mostrata così com&#39;è, quindi non c&#39;è impatto sulla consegna.

+++

## Modifica dei risultati

+++ La modifica di un elemento nella pagina cambia più elementi

Se lo stesso ID di elemento DOM è utilizzato in più elementi della pagina, la modifica di uno di questi elementi influenza tutti gli elementi con lo stesso ID. Per evitare questo problema, utilizza un ID una sola volta su ogni pagina. Questa è una best practice HTML standard. Per ulteriori informazioni, vedere [Scenari di modifica delle pagine](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#vec-scenarios).

+++

+++ Gli stili di testo grassetto e corsivo non vengono visualizzati o il testo scompare dopo aver applicato Modifica testo/Modifica HTML o Modifica testo/Cambia HTML

Quando si utilizza **[!UICONTROL Modifica testo]**/**[!UICONTROL Modifica HTML]** nel Compositore esperienza visivo per **[!UICONTROL Test A/B]** o **[!UICONTROL Attività Targeting esperienza]** oppure **[!UICONTROL Modifica testo]**/**[!UICONTROL Modifica HTML]** per **[!UICONTROL Attività Automated Personalization]** o **[!UICONTROL Test multivariato]**, per rendere il testo in grassetto o corsivo, gli stili potrebbero non essere applicati alla pagina o il testo potrebbe scomparire dalla pagina nel Compositore esperienza visivo. Ciò accade perché il modo in cui l’editor Rich Text applica questi stili potrebbe interferire con il markup del sito web.

Se si verifica questo problema:

1. Fai clic sul pulsante **[!UICONTROL HTML]** nell&#39;editor rich-text per accedere alla modalità di modifica della sorgente.
1. Trovare gli elementi di testo con stili.

   * Per il testo in grassetto, modifica gli elementi `<strong>` in `<b>`.
   * Per il testo in corsivo, modifica gli elementi `<em>` in `<i>`.

+++
