---
keywords: host;hosts;host group;troubleshooting;best practices;ubox;redirects;redirect;whitelist;allowlist;blacklist;blocklist
description: Organizzate i siti e gli ambienti di pre-produzione per semplificare la gestione e la creazione di report separati in  Adobe Target.
title: Host
feature: Administration & Configuration
translation-type: tm+mt
source-git-commit: 9b57d5554884b06d278c3baef3b2c1d5f37bdeb5
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 26%

---


# Host{#hosts}

Organizza siti e ambienti di preproduzione per gestirli facilmente e per generare rapporti separati.

L’obiettivo principale della gestione host è quello di garantire che nessun contenuto inattivo venga visualizzato accidentalmente sui siti web. La gestione dell&#39;host consente inoltre di separare i dati dei report per [ambiente](/help/administrating-target/environments.md).

Un host è qualsiasi dominio da cui viene eseguita una richiesta [!DNL Target]. In un sito Web, si tratta in genere della proprietà `location.hostname` dell&#39;URL che effettua la richiesta [!DNL Target].

Per impostazione predefinita, [!DNL Target] non limita un host in grado di effettuare richieste [!DNL Target] e ricevere risposte [!DNL Target]. Quando i nuovi ospitanti effettuano delle richieste, queste funzionano automaticamente. Questo consente anche di eseguire test su domini diversi che non conosci o che non puoi prevedere. Se si desidera ignorare questo comportamento predefinito, è possibile impostare un  inserire nell&#39;elenco Consentiti o  inserii nell&#39;elenco Bloccati per limitare gli host con cui lavorare [!DNL Target].

Per gestire gli host, fare clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Host]**.

![](assets/hosts_list.png)

## Riconoscimento host {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

Per riconoscere un host e aggiungerlo all&#39;elenco [!UICONTROL Host], è necessario soddisfare le seguenti condizioni:

* Almeno una richiesta [!DNL Target] deve esistere sull&#39;host
* Una pagina sull’host deve avere quanto segue:

   * Un riferimento preciso a at.js o mbox.js
   * Una richiesta [!DNL Target] o una richiesta globale generata automaticamente[!DNL Target]

* La pagina con la richiesta [!DNL Target] deve essere visualizzata in un browser

Dopo che la pagina è stata visualizzata, l&#39;host è elencato nell&#39;elenco [!UICONTROL Host], che consente di gestirla in un ambiente, nonché attività di anteprima e avvio e test.

>[!NOTE]
>
>Questo include tutti i server di sviluppo personali.

Dopo aver aggiunto un host all’elenco degli [!UICONTROL host], assicurati che l’host sia riconosciuto.

1. Fare clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Host]**.
1. Se l’host non è elencato, aggiorna il browser. 


   Per impostazione predefinita, un nuovo host riconosciuto viene posizionato nell&#39;ambiente [!UICONTROL Produzione]. Questo è l’ambiente più sicuro perché non consente di visualizzare le attività inattive da questi host.

1. (Condizionale) Fare clic sull&#39;icona **[!UICONTROL Sposta]** ( ![icona Sposta](/help/administrating-target/assets/icon-move.png) ) per spostare l&#39;host in [!UICONTROL Sviluppo], [!UICONTROL Gestione temporanea] o in un altro ambiente.

>[!NOTE]
>
>L&#39;ambiente [!UICONTROL Produzione] non può essere eliminato, anche se lo si rinomina. Si presuppone che è qui che verranno eseguiti attività e test attivi e finali. L’ambiente predefinito non consente di visualizzare le campagne inattive.

## Ordinare o cercare l&#39;elenco Host {#section_068B23C9D8224EB78BC3B7C8580251B0}

Per ordinare l&#39;elenco [!UICONTROL Ospitanti], fare clic sull&#39;intestazione di una colonna ([!UICONTROL Nome], [!UICONTROL Ambiente] o [!UICONTROL Ultima richiesta]) per ordinare l&#39;elenco in ordine crescente o decrescente.

Per cercare nell&#39;elenco [!UICONTROL Host], digitare un termine di ricerca nella casella [!UICONTROL Host di ricerca].

## Create inserire nell&#39;elenco Consentiti  che specificano gli host autorizzati a inviare richieste Target a Target. {#allowlist}

Potete creare un inserire nell&#39;elenco Consentiti  che specifica gli host (domini) autorizzati a inviare richieste [!DNL Target] a [!DNL Target]. Tutti gli altri host che generano richieste riceveranno una risposta di errore di autorizzazione con commenti. Per impostazione predefinita, qualsiasi host che contiene una richiesta [!DNL Target] si registra con [!DNL Target] nell&#39;ambiente [!UICONTROL Produzione] e ha accesso a tutte le attività attive e approvate. Se questo non è l&#39;approccio desiderato, potete utilizzare il inserire nell&#39;elenco Consentiti  per registrare host specifici idonei a effettuare richieste [!DNL Target] e ricevere contenuto [!DNL Target]. Tutti gli host continueranno a essere visualizzati nell&#39;elenco [!UICONTROL Ospitanti] e gli ambienti possono ancora essere utilizzati per raggruppare questi host e assegnare livelli diversi a ciascuno di essi, ad esempio se l&#39;ospitante può visualizzare attività attive e/o inattive.

Per creare un inserire nell&#39;elenco Consentiti di :

1. Nell&#39;elenco [!UICONTROL Host], fare clic su **[!UICONTROL Autorizza host]**.
1. Attiva l&#39;interruttore **[!UICONTROL Abilita ospitanti autorizzati per la distribuzione del contenuto]**.
1. Aggiungere gli host desiderati nella casella **[!UICONTROL Host contiene]**, come desiderato.

   È possibile elencare più host, ciascuno sulla propria linea.

1. Aggiungere gli host desiderati nella casella **[!UICONTROL Host non contiene]**, come desiderato.

   È possibile elencare più host, ciascuno sulla propria linea.

1. Fai clic su **[!UICONTROL Salva]**.

Se una [!DNL Target] richiesta viene effettuata su un host non autorizzato, la chiamata risponderà con `/* no display - unauthorized mbox host */`.

>[!IMPORTANT]
>
>**Best practice** di protezione: Se utilizzate la funzionalità ubox di  [!DNL Target], tenete presente che questo  inserì nell&#39;elenco Consentiti controllerà anche l&#39;elenco dei domini a cui il  [](/help/c-implementing-target/c-non-javascript-based-implementation/working-with-redirectors.md) reindirizzamento naviga. Accertati di aggiungere eventuali domini a cui vuoi reindirizzare quando utilizzi ubox come parte dell&#39;implementazione. Se il inserire nell&#39;elenco Consentiti di  non viene specificato, [!DNL Adobe] non sarà in grado di verificare gli URL di reindirizzamento e di proteggere da potenziali reindirizzamenti dannosi.
>
>Il inserire nell&#39;elenco Consentiti  ha la precedenza sugli ambienti. Prima di utilizzare la funzione di inserire nell&#39;elenco Consentiti di , è necessario eliminare tutti gli host, quindi solo gli host consentiti dal inserire nell&#39;elenco Consentiti di  vengono visualizzati nell&#39;elenco degli host. A questo punto puoi spostare gli host nell’ambiente desiderato.

A volte i domini da altri siti appaiono negli ambienti. Un dominio viene visualizzato nell&#39;elenco se il dominio effettua una chiamata al tuo at.js o mbox.js. Ad esempio, se qualcuno copia una delle tue pagine web sul suo server, tale dominio verrà visualizzato nel tuo ambiente. Potrebbe anche essere possibile vedere domini da motori spider, siti di traduzione linguistica o unità disco locali.

Nei casi in cui `mboxHost` viene passato in una chiamata API, la conversione viene registrata per l’ambiente passato. Se non viene passato alcun ambiente, per impostazione predefinita l&#39;host nella chiamata è [!UICONTROL Production].

È inoltre possibile creare un elenco Bloccati che specifica gli host (domini) che non può inviare [!DNL Target] richieste a [!DNL Target] aggiungendo gli host desiderati nella casella [!UICONTROL Host non contiene].

>[!NOTE]
>
>Poiché l&#39;elenco Host autorizzati è utilizzato sia per gli host [!DNL Target] che per gli host di reindirizzamento predefiniti, è necessario aggiungere tutti i domini esistenti approvati per utilizzare l&#39;SDK [!DNL Adobe Target] Javascript (at.js) *AND* tutti i domini utilizzati negli URL di reindirizzamento predefiniti di ubox. È inoltre necessario aggiungere nuovi domini simili al inserire nell&#39;elenco Consentiti  in futuro.

## Eliminare un host {#section_F56355BA4BC54B078A1A8179BC954632}

Quando un host non è più necessario, è possibile eliminarlo.

1. Nell&#39;elenco [!UICONTROL Host], fare clic sull&#39;icona **[!UICONTROL Elimina]**.
1. Fai clic su **[!UICONTROL Elimina]** per confermare l’eliminazione.

>[!NOTE]
>
>L&#39;host verrà elencato di nuovo se qualcuno naviga in una pagina che contiene una richiesta [!DNL Target] sull&#39;host.

## Risoluzione dei problemi relativi agli host {#concept_B3D7583FA4BB480382CC7453529FE1B7}

Se si verificano problemi con gli host, prova i seguenti suggerimenti di risoluzione:

**L&#39;host non viene visualizzato nell&#39;elenco dell&#39;account.**

* Aggiorna la pagina [!UICONTROL Host] nel browser.
* Verificate che la richiesta [!DNL Target] sia corretta, compreso il riferimento at.js o mbox.js.
* Provate a individuare una delle [!DNL Target] richieste sull&#39;host. È possibile che nessuna richiesta [!DNL Target] sull&#39;host sia mai stata sottoposta a rendering in un browser.

**Domini casuali o sconosciuti vengono visualizzati nell&#39;elenco [!UICONTROL Host].**

Un dominio viene visualizzato in questo elenco se dal dominio viene effettuata una richiesta a [!DNL Target]. Spesso, è possibile vedere domini da motori spider, siti di traduzione linguistica o unità disco locali. Se il dominio elencato non è tra quelli utilizzati dal team, è possibile fare clic su [!UICONTROL Elimina] per rimuoverlo.

**La mia  [!DNL Target] richiesta restituisce /* nessun display - host mbox non autorizzato */.**

Se una [!DNL Target] richiesta viene effettuata su un host non autorizzato, la richiesta risponderà con /* nessun display - host mbox non autorizzato */.
