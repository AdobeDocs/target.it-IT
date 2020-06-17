---
keywords: host;hosts;host group;troubleshooting;best practices;ubox;redirects;redirect;whitelist;allowlist;blacklist;blocklist
description: Organizza siti e ambienti di preproduzione per gestirli facilmente e per generare rapporti separati.
title: Host
topic: Standard
uuid: c7682269-4ec2-4a0f-b053-7e0ec77f4604
translation-type: tm+mt
source-git-commit: 44d9024cb9c1f6a1e28845f9545fed0d56fe176a
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Host{#hosts}

Organizza siti e ambienti di preproduzione per gestirli facilmente e per generare rapporti separati.

>[!NOTE]
>
>Le informazioni riportate in questo argomento sono state aggiornate per fornire un picco spettacolare delle modifiche all&#39;interfaccia utente in arrivo nella release Target Standard/Premium 20.6.1 (luglio 2020). La maggior parte delle informazioni presentate in questo argomento si applica all’interfaccia utente corrente; tuttavia, le opzioni potrebbero trovarsi in posizioni leggermente diverse.

L’obiettivo principale della gestione host è quello di garantire che nessun contenuto inattivo venga visualizzato accidentalmente sui siti web. Host management also lets you separate report data by [environment](/help/administrating-target/environments.md).

Un host è un qualsiasi server web (o dominio web) dal quale viene trasmesso il contenuto durante qualsiasi fase del progetto. Viene riconosciuto qualsiasi host che trasmette una mbox.

Per facilitare la gestione, gli host sono raccolti in ambienti. Ad esempio, si potrebbero avere decine di host raggruppati in due o tre ambienti. The preset environments include [!UICONTROL Production], [!UICONTROL Staging], and [!UICONTROL Development]. È anche possibile aggiungere nuovi ambienti e rinominare gli ambienti.

One environment, the default environment, is pre-named [!UICONTROL Production]. Questo ambiente predefinito non può essere eliminato, anche se lo si rinomina. [!DNL Target] presuppone che è qui che verranno eseguiti attività e test finali e approvati.

When an mbox request is received from new websites or domains, these new domains always appear in the [!UICONTROL Production] environment. The [!UICONTROL Production] environment cannot have its settings changed, so unknown or new sites are guaranteed to see only content that is active and ready. La gestione degli host consente inoltre di garantire facilmente la qualità di nuove attività e contenuti nei test, nella gestione temporanea (staging) e negli ambienti di sviluppo prima di attivare le attività.

[!DNL Target] non limita un host che può inviare e ricevere mbox, pertanto quando nuovi server o domini vengono visualizzati, funzionano automaticamente (a meno che non abbiate impostato un elenco di autorizzazioni o un elenco di blocchi). Ciò consente inoltre di testare gli annunci su domini diversi che non si conoscono o non si possono anticipare.

Per gestire gli host, fate clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Ospitanti]**.

![](assets/hosts_list.png)

## Recognizing hosts {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

Per riconoscere un host e aggiungerlo all&#39;elenco [!UICONTROL Ospitanti] , è necessario soddisfare le seguenti condizioni:

* Almeno una mbox deve esistere sull’host
* Una pagina sull’host deve avere quanto segue:

   * Un riferimento preciso a at.js o mbox.js
   * Una mbox o una chiamata mbox globale generata automaticamente

* La pagina con la mbox deve essere visualizzata in un browser

Dopo aver visualizzato la pagina, l’host è presente nell’elenco degli [!UICONTROL host]; è quindi possibile gestirlo in un ambiente, nonché visualizzare in anteprima e avviare attività e test.

>[!NOTE] {class=“- topic/note ”}
>
>Questo include tutti i server di sviluppo personali.

Dopo aver aggiunto un host all’elenco degli [!UICONTROL host], assicurati che l’host sia riconosciuto.

1. Fate clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Ospitanti]**.
1. Se l’host non è elencato, aggiorna il browser. 


   By default, a newly recognized host is placed in the [!UICONTROL Production] environment. Questo è l’ambiente più sicuro perché non consente di visualizzare le attività inattive da questi host.

1. (Condizionale) Fate clic sull&#39;icona Sposta (icona ![](/help/administrating-target/assets/icon-move.png) Sposta) per spostare l&#39;host in [!UICONTROL Sviluppo], [!UICONTROL Staging]o altro ambiente.

>[!NOTE]
>
>The [!UICONTROL Production] environment cannot be deleted, even if you rename it. Si presuppone che è qui che verranno eseguiti attività e test attivi e finali. L’ambiente predefinito non consente di visualizzare le campagne inattive.

## Sort or search the Hosts list {#section_068B23C9D8224EB78BC3B7C8580251B0}

To sort the [!UICONTROL Hosts] list, click any column header ([!UICONTROL Name], [!UICONTROL Environment], or [!UICONTROL Last Requested]) to sort the list in ascending or descending order.

To search the [!UICONTROL Hosts] list, type a search term in the [!UICONTROL Search Hosts] box.

## Create allowlists that specify hosts that are authorized to send mbox calls to Target. {#allowlist}

You can create an allowlist that specifies hosts (domains) that are authorized to send mbox calls to [!DNL Target]. Tutti gli altri host che generano chiamate riceveranno una risposta di errore di autorizzazione, inserita come riga di commento. Per impostazione predefinita, qualsiasi host che contiene una chiamata mbox si registra con [!DNL Target] nell’Ambiente di produzione e ha accesso a tutte le attività attive e approvate. If this is not the desired approach, you can instead use the allowlist to record specific hosts that are eligible to make mbox calls and receive [!DNL Target] content. Tutti gli host continuano a essere visualizzati nell’elenco [!UICONTROL Host] e gli ambienti possono comunque essere utilizzati per raggruppare questi host e assegnare diversi livelli a ciascuno, ad esempio se l’host può visualizzare campagne attive e/o inattive.

Per creare un elenco di autorizzazioni:

1. Dall&#39;elenco [!UICONTROL Ospitanti] , fate clic su **[!UICONTROL Autorizza ospitanti]**.
1. Attivate l&#39;opzione **[!UICONTROL Abilita ospitanti autorizzati per la distribuzione]** del contenuto.
1. Add the desired hosts in the **[!UICONTROL Host contains]** box, as desired.

   È possibile elencare più host, ciascuno sulla propria linea.

1. Add the desired hosts in the **[!UICONTROL Host does not contains]** box, as desired.

   È possibile elencare più host, ciascuno sulla propria linea.

1. Fai clic su **[!UICONTROL Salva]**.

Se una chiamata mbox viene effettuata su un host non autorizzato, la chiamata risponderà con `/* no display - unauthorized mbox host */`.

>[!IMPORTANT]
>
>**Best practice** di protezione: Se utilizzate la funzionalità ubox di [!DNL Target], tenete presente che questo elenco di autorizzazioni controllerà anche l&#39;elenco dei domini a cui i [redirector](/help/c-implementing-target/c-non-javascript-based-implementation/working-with-redirectors.md) possono navigare. Accertati di aggiungere eventuali domini a cui vuoi reindirizzare quando utilizzi ubox come parte dell&#39;implementazione. Se l&#39;elenco di autorizzazioni non viene specificato, Adobe non sarà in grado di verificare gli URL di reindirizzamento e di proteggerli da potenziali reindirizzamenti dannosi.
>
>L&#39;elenco dei permessi ha la precedenza sugli ambienti. Prima di utilizzare la funzione Elenco consentito, è necessario eliminare tutti gli host, quindi solo quelli consentiti dall&#39;elenco di host vengono visualizzati nell&#39;elenco. A questo punto puoi spostare gli host nell’ambiente desiderato.

A volte i domini da altri siti appaiono negli ambienti. Un dominio viene visualizzato nell&#39;elenco se il dominio effettua una chiamata al tuo at.js o mbox.js. Ad esempio, se qualcuno copia una delle tue pagine web sul suo server, tale dominio verrà visualizzato nel tuo ambiente. Potrebbe anche essere possibile vedere domini da motori spider, siti di traduzione linguistica o unità disco locali.

Nei casi in cui `mboxHost` viene passato in una chiamata API, la conversione viene registrata per l’ambiente passato. If no environment is passed, the host in the call defaults to [!UICONTROL Production].

È inoltre possibile creare una lista nera che specifichi gli host (domini) che non possono inviare le chiamate mbox a [!DNL Target] aggiungendo gli host desiderati nell’host nella casella [!UICONTROL L’host non contiene].

>[!NOTE]
>
>Poiché l&#39;elenco Host autorizzati è utilizzato sia per gli host mbox che per gli host di reindirizzamento predefiniti, è necessario aggiungere tutti i domini esistenti approvati per utilizzare l&#39;SDK Javascript del Adobe Target  (at.js) *E* tutti i domini utilizzati negli URL di reindirizzamento predefiniti ubox. In futuro è inoltre necessario aggiungere nuovi domini simili all&#39;elenco dei domini consentiti.

## Delete a host {#section_F56355BA4BC54B078A1A8179BC954632}

Quando un host non è più necessario, è possibile eliminarlo.

1. From the [!UICONTROL Hosts] list, click the **[!UICONTROL Delete]** icon.
1. Fai clic su **[!UICONTROL Elimina]** per confermare l’eliminazione.

>[!NOTE]
>
>L’host sarà elencato di nuovo se qualcuno passa a una pagina con mbox sull’host.

## Risoluzione dei problemi relativi agli host {#concept_B3D7583FA4BB480382CC7453529FE1B7}

Procedure consigliate per la gestione e la risoluzione dei problemi relativi agli host in [!DNL Adobe Target].

Se si verificano problemi con gli host, prova i seguenti suggerimenti di risoluzione:

**L’host non compare nell’elenco delle mbox per il tuo account.**

* Aggiorna la pagina [!UICONTROL Host] nel browser.
* Verificate che il codice mbox sia corretto, compreso il riferimento at.js o mbox.js.
* Prova a passare a una delle mbox sull&#39;host. È possibile che sia ancora stato eseguito il rendering in un browser per nessuna mbox dell’host.

**Domini casuali o sconosciuti vengono visualizzati nell&#39;elenco[!UICONTROL Host].**

Un dominio viene visualizzato in questo elenco se viene effettuata una chiamata a [!DNL Target] dal dominio. Spesso, è possibile vedere domini da motori spider, siti di traduzione linguistica o unità disco locali. Se il dominio elencato non è tra quelli utilizzati dal team, è possibile fare clic su [!UICONTROL Elimina] per rimuoverlo.

**La mia chiamata mbox restituisce /* no display - unauthorized mbox host */.**

Se una chiamata mbox viene effettuata su un host non autorizzato, la chiamata risponderà con /* no display - unauthorized mbox host */.
