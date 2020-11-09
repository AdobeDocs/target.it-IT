---
keywords: host;hosts;host group;troubleshooting;best practices;ubox;redirects;redirect;whitelist;allowlist;blacklist;blocklist
description: Organizza siti e ambienti di preproduzione per gestirli facilmente e per generare rapporti separati.
title: Host
feature: hosts and environments
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 27%

---


# Host{#hosts}

Organizza siti e ambienti di preproduzione per gestirli facilmente e per generare rapporti separati.

L’obiettivo principale della gestione host è quello di garantire che nessun contenuto inattivo venga visualizzato accidentalmente sui siti web. Host management also lets you separate report data by [environment](/help/administrating-target/environments.md).

Un host è qualsiasi dominio da cui viene [!DNL Target] eseguita una richiesta. In un sito Web, si tratta in genere della `location.hostname` proprietà dell’URL che effettua la [!DNL Target] richiesta.

Per impostazione predefinita, [!DNL Target] non limita un ospitante che può effettuare [!DNL Target] richieste e ricevere [!DNL Target] risposte. Quando i nuovi ospitanti effettuano delle richieste, queste funzionano automaticamente. Questo consente anche di eseguire test su domini diversi che non conosci o che non puoi prevedere. Se si desidera ignorare questo comportamento predefinito, è possibile impostare un  inserire nell&#39;elenco Consentiti o  inserii nell&#39;elenco Bloccati per limitare gli host con cui lavorare [!DNL Target].

Per gestire gli host, fate clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Ospitanti]**.

![](assets/hosts_list.png)

## Recognizing hosts {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

Per riconoscere un host e aggiungerlo all&#39;elenco [!UICONTROL Ospitanti] , è necessario soddisfare le seguenti condizioni:

* At least one [!DNL Target] request must exist on the host
* Una pagina sull’host deve avere quanto segue:

   * Un riferimento preciso a at.js o mbox.js
   * Una [!DNL Target] richiesta o una richiesta globale generata automaticamente [!DNL Target]

* The page with the [!DNL Target] request must be viewed in a browser

After the page is viewed, the host is listed in the [!UICONTROL Hosts] list, allowing you to manage it in an environment, as well as preview and launch activities and tests.

>[!NOTE]
>
>Questo include tutti i server di sviluppo personali.

Dopo aver aggiunto un host all’elenco degli [!UICONTROL host], assicurati che l’host sia riconosciuto.

1. Fate clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Ospitanti]**.
1. Se l’host non è elencato, aggiorna il browser. 


   By default, a newly recognized host is placed in the [!UICONTROL Production] environment. Questo è l’ambiente più sicuro perché non consente di visualizzare le attività inattive da questi host.

1. (Condizionale) Fate clic sull&#39;icona **[!UICONTROL Sposta]** ( icona ![](/help/administrating-target/assets/icon-move.png) Sposta ) per spostare l&#39;host nello [!UICONTROL sviluppo], nell&#39; [!UICONTROL area]di gestione temporanea o in un altro ambiente.

>[!NOTE]
>
>The [!UICONTROL Production] environment cannot be deleted, even if you rename it. Si presuppone che è qui che verranno eseguiti attività e test attivi e finali. L’ambiente predefinito non consente di visualizzare le campagne inattive.

## Sort or search the Hosts list {#section_068B23C9D8224EB78BC3B7C8580251B0}

To sort the [!UICONTROL Hosts] list, click any column header ([!UICONTROL Name], [!UICONTROL Environment], or [!UICONTROL Last Requested]) to sort the list in ascending or descending order.

To search the [!UICONTROL Hosts] list, type a search term in the [!UICONTROL Search Hosts] box.

## Create allowlists that specify hosts that are authorized to send Target requests to Target. {#allowlist}

You can create an allowlist that specifies hosts (domains) that are authorized to send [!DNL Target] requests to [!DNL Target]. Tutti gli altri host che generano richieste riceveranno una risposta di errore di autorizzazione con commenti. By default, any host that contains a [!DNL Target] request registers with [!DNL Target] in the [!UICONTROL Production] environment and has access to all active and approved activities. If this is not the desired approach, you can instead use the allowlist to record specific hosts that are eligible to make [!DNL Target] requests and receive [!DNL Target] content. All hosts will continue to display in the [!UICONTROL Hosts] list, and environments can still be used to group these hosts and assign different levels to each, such as whether the host can see active and/or inactive activities.

Per creare un inserire nell&#39;elenco Consentiti di :

1. Dall&#39;elenco [!UICONTROL Ospitanti] , fate clic su **[!UICONTROL Autorizza ospitanti]**.
1. Attivate l&#39;opzione **[!UICONTROL Abilita ospitanti autorizzati per la distribuzione]** del contenuto.
1. Add the desired hosts in the **[!UICONTROL Host contains]** box, as desired.

   È possibile elencare più host, ciascuno sulla propria linea.

1. Add the desired hosts in the **[!UICONTROL Host does not contains]** box, as desired.

   È possibile elencare più host, ciascuno sulla propria linea.

1. Fai clic su **[!UICONTROL Salva]**.

If a [!DNL Target] request is made on an unauthorized host, the call will respond with `/* no display - unauthorized mbox host */`.

>[!IMPORTANT]
>
>**Best practice** di protezione: Se utilizzate la funzionalità ubox di [!DNL Target], tenete presente che questo  inserì nell&#39;elenco Consentiti controllerà anche l&#39;elenco dei domini a cui i [redirector](/help/c-implementing-target/c-non-javascript-based-implementation/working-with-redirectors.md) possono navigare. Accertati di aggiungere eventuali domini a cui vuoi reindirizzare quando utilizzi ubox come parte dell&#39;implementazione. Se il inserire nell&#39;elenco Consentiti di  non viene specificato, [!DNL Adobe] non sarà in grado di verificare gli URL di reindirizzamento e di proteggere da potenziali reindirizzamenti dannosi.
>
>Il inserire nell&#39;elenco Consentiti  ha la precedenza sugli ambienti. Prima di utilizzare la funzione di inserire nell&#39;elenco Consentiti di , è necessario eliminare tutti gli host, quindi solo gli host consentiti dal inserire nell&#39;elenco Consentiti di  vengono visualizzati nell&#39;elenco degli host. A questo punto puoi spostare gli host nell’ambiente desiderato.

A volte i domini da altri siti appaiono negli ambienti. Un dominio viene visualizzato nell&#39;elenco se il dominio effettua una chiamata al tuo at.js o mbox.js. Ad esempio, se qualcuno copia una delle tue pagine web sul suo server, tale dominio verrà visualizzato nel tuo ambiente. Potrebbe anche essere possibile vedere domini da motori spider, siti di traduzione linguistica o unità disco locali.

Nei casi in cui `mboxHost` viene passato in una chiamata API, la conversione viene registrata per l’ambiente passato. If no environment is passed, the host in the call defaults to [!UICONTROL Production].

You can also create a denylist that specifies hosts (domains) than cannot send [!DNL Target] requests to [!DNL Target] by adding the desired hosts in the [!UICONTROL Host Does Not Contain] box.

>[!NOTE]
>
>Poiché l&#39;elenco Host autorizzati è utilizzato sia per [!DNL Target] gli host che per gli host di reindirizzamento predefiniti, è necessario aggiungere tutti i domini esistenti approvati per utilizzare l&#39;SDK [!DNL Adobe Target] Javascript (at.js) *AND* tutti i domini utilizzati negli URL di reindirizzamento predefiniti ubox. È inoltre necessario aggiungere nuovi domini simili al inserire nell&#39;elenco Consentiti  in futuro.

## Delete a host {#section_F56355BA4BC54B078A1A8179BC954632}

Quando un host non è più necessario, è possibile eliminarlo.

1. From the [!UICONTROL Hosts] list, click the **[!UICONTROL Delete]** icon.
1. Fai clic su **[!UICONTROL Elimina]** per confermare l’eliminazione.

>[!NOTE]
>
>L’ospitante verrà elencato di nuovo se qualcuno passa a una pagina che contiene una [!DNL Target] richiesta sull’ospitante.

## Risoluzione dei problemi relativi agli host {#concept_B3D7583FA4BB480382CC7453529FE1B7}

Se si verificano problemi con gli host, prova i seguenti suggerimenti di risoluzione:

**L&#39;host non viene visualizzato nell&#39;elenco dell&#39;account.**

* Aggiorna la pagina [!UICONTROL Host] nel browser.
* Verificate che la [!DNL Target] richiesta sia corretta, compreso il riferimento at.js o mbox.js.
* Try browsing to one of the [!DNL Target] requests on the host. It&#39;s possible that no [!DNL Target] request on the host was ever rendered in a browser.

**Domini casuali o sconosciuti vengono visualizzati nell&#39;elenco [!UICONTROL Host].**

A domain appears in this list if a request to [!DNL Target] is made from the domain. Spesso, è possibile vedere domini da motori spider, siti di traduzione linguistica o unità disco locali. Se il dominio elencato non è tra quelli utilizzati dal team, è possibile fare clic su [!UICONTROL Elimina] per rimuoverlo.

**La mia [!DNL Target] richiesta restituisce /* nessun display - host mbox non autorizzato */.**

If a [!DNL Target] request is made on an unauthorized host, the request will respond with /* no display - unauthorized mbox host */.
