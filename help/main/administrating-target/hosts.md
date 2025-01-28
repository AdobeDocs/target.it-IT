---
keywords: host;host;gruppo host;risoluzione dei problemi;best practice;ubox;reindirizzamenti;reindirizzare;whitelist;inserire nell'elenco Consentiti la blacklist;inserire nell'elenco Bloccati la blacklist;
description: Scopri come organizzare i siti web e gli ambienti di preproduzione per gestirli facilmente e per creare rapporti separati all’interno di Adobe Target.
title: Cosa sono gli host e come li utilizzo?
feature: Administration & Configuration
role: Admin
exl-id: 31c661c0-686d-440e-ad58-864fb853b1c4
source-git-commit: 484971ab0fcd07205935c0fef3ea1484f40c3e96
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 18%

---

# Host

Organizza i tuoi siti e gli ambienti di pre-produzione per gestirli facilmente e creare rapporti separati in [!DNL Adobe Target].

L’obiettivo principale della gestione host è quello di garantire che nessun contenuto inattivo venga visualizzato accidentalmente sui siti web. La gestione host consente inoltre di separare i dati del report per [ambiente](/help/main/administrating-target/environments.md).

Un host è qualsiasi dominio da cui viene effettuata una richiesta [!DNL Target]. In un sito Web è in genere la proprietà `location.hostname` dell&#39;URL che effettua la richiesta [!DNL Target].

Per impostazione predefinita, [!DNL Target] non limita un host in grado di effettuare [!DNL Target] richieste e ricevere [!DNL Target] risposte. Quando nuovi host effettuano richieste, queste funzionano automaticamente. Questo processo consente anche di eseguire test su domini diversi che non conosci o che non puoi prevedere. Se si desidera ignorare questo comportamento predefinito, è possibile impostare un inserisco nell&#39;elenco Consentiti di o di elenco Bloccati per limitare quali host funzionano con [!DNL Target].

Per gestire gli host, scegliere **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.

## Riconoscere gli host {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

Per riconoscere un host e aggiungerlo all&#39;elenco [!UICONTROL Hosts], è necessario soddisfare le seguenti condizioni:

* Deve esistere almeno una richiesta [!DNL Target] nell&#39;host
* Una pagina sull’host deve avere quanto segue:

   * Un preciso riferimento at.js
   * Una richiesta [!DNL Target] o una richiesta [!DNL Target] globale generata automaticamente

* La pagina con la richiesta [!DNL Target] deve essere visualizzata in un browser

Dopo aver visualizzato la pagina, l&#39;host è elencato nell&#39;elenco [!UICONTROL Hosts], che consente di gestirlo in un ambiente e di visualizzare in anteprima e avviare attività e test.

>[!NOTE]
>
>Questo include tutti i server di sviluppo personali.

Dopo aver aggiunto un host all&#39;elenco [!UICONTROL Host], assicurarsi che l&#39;host sia riconosciuto.

1. Fare clic su **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.
1. Se l’host non è elencato, aggiorna il browser.

   Per impostazione predefinita, un host appena riconosciuto viene inserito nell&#39;ambiente [!UICONTROL Production]. L&#39;ambiente [!UICONTROL Production] è l&#39;ambiente più sicuro perché non consente la visualizzazione delle attività inattive da questi host.

1. (Condizionale) Fai clic sull&#39;icona **[!UICONTROL Move]** ( ![icona Sposta](/help/main/administrating-target/assets/icon-move.png) ) per spostare l&#39;host in [!UICONTROL Development], [!UICONTROL Staging] o in un altro ambiente.

>[!NOTE]
>
>L&#39;ambiente [!UICONTROL Production] non può essere eliminato, anche se viene rinominato. Si presume che questo ambiente sia il luogo in cui vengono eseguiti attività e test finali e attivi. L’ambiente predefinito non consente di visualizzare le campagne inattive.

## Ordinare o cercare nell’elenco Host {#section_068B23C9D8224EB78BC3B7C8580251B0}

Per ordinare l&#39;elenco [!UICONTROL Hosts], fare clic su un&#39;intestazione di colonna ([!UICONTROL Name], [!UICONTROL Environment] o [!UICONTROL Last Requested]) per ordinare l&#39;elenco in ordine crescente o decrescente.

Per cercare nell&#39;elenco [!UICONTROL Hosts], digitare un termine di ricerca nella casella [!UICONTROL Search Hosts].

## Inserire nell&#39;elenco Consentiti Creazione di che specificano gli host autorizzati per l&#39;invio di [!DNL Target] richieste a [!DNL Target]. {#allowlist}

È possibile creare un inserisco nell&#39;elenco Consentiti di che specifichi gli host (domini) autorizzati a inviare [!DNL Target] richieste a [!DNL Target]. Tutti gli altri host che generano richieste ricevono una risposta di errore di autorizzazione commentata. Per impostazione predefinita, qualsiasi host che contiene una richiesta [!DNL Target] si registra con [!DNL Target] nell&#39;ambiente [!UICONTROL Production] e ha accesso a tutte le attività attive e approvate. Se questo approccio non è desiderato, è invece possibile utilizzare il inserisco nell&#39;elenco Consentiti di per registrare host specifici idonei a effettuare [!DNL Target] richieste e a ricevere il contenuto di [!DNL Target]. Tutti gli host continuano a essere visualizzati nell&#39;elenco [!UICONTROL Hosts] e gli ambienti possono ancora essere utilizzati per raggruppare questi host e assegnare livelli diversi a ciascuno, ad esempio se l&#39;host può visualizzare le attività attive e/o inattive.

Per creare un inserisco nell&#39;elenco Consentiti di:

1. Dall&#39;elenco [!UICONTROL Hosts], fare clic su **[!UICONTROL Authorize Hosts]**.
1. Attiva/disattiva **[!UICONTROL Enable Authorized Hosts for content delivery]**.
1. Aggiungere gli host desiderati nella casella **[!UICONTROL Host contains]**, come desiderato.

   È possibile elencare più host, ciascuno sulla propria linea.

1. Aggiungere gli host desiderati nella casella **[!UICONTROL Host does not contains]**, come desiderato.

   È possibile elencare più host, ciascuno sulla propria linea.

1. Fare clic su **[!UICONTROL Save]**.

Se viene effettuata una richiesta [!DNL Target] su un host non autorizzato, la chiamata risponde con `/* no display - unauthorized mbox host */`.

>[!IMPORTANT]
>
>**Best practice per la sicurezza**: se utilizzi la funzionalità ubox di [!DNL Target], questo inserisco nell&#39;elenco Consentiti controlla anche l&#39;elenco di domini a cui i tuoi [redirector](https://experienceleague.adobe.com/docs/target-dev/developer/implement-email/working-with-redirectors.html){target=_blank} possono accedere. Assicurati di aggiungere tutti i domini a cui desideri reindirizzare quando utilizzi ubox come parte dell’implementazione. Se il inserisco nell&#39;elenco Consentiti di viene lasciato non specificato, [!DNL Adobe] non è in grado di verificare gli URL di reindirizzamento e di proteggere da potenziali reindirizzamenti dannosi.
>
>Il inserisco nell&#39;elenco Consentiti di ha la precedenza sugli ambienti. Cancella tutti gli host prima di utilizzare la funzione di inserisce nell&#39;elenco Consentiti di, quindi nell’elenco degli host vengono visualizzati solo gli host consentiti dal inserisco nell&#39;elenco Consentiti di. A questo punto puoi spostare gli host nell’ambiente desiderato.

A volte i domini da altri siti appaiono negli ambienti. Un dominio viene visualizzato nell’elenco se chiama at.js. Ad esempio, se qualcuno copia una delle tue pagine web sul suo server, tale dominio verrà visualizzato nel tuo ambiente. Potrebbe anche essere possibile vedere domini da motori spider, siti di traduzione linguistica o unità disco locali.

Nei casi in cui `mboxHost` viene passato in una chiamata API, la conversione viene registrata per l’ambiente passato. Se non viene passato alcun ambiente, il valore predefinito dell&#39;host nella chiamata è [!UICONTROL Production].

È inoltre possibile creare un elenco Bloccati di che specifichi gli host (domini) che non possono inviare [!DNL Target] richieste a [!DNL Target] aggiungendo gli host desiderati nella casella [!UICONTROL Host Does Not Contain].

>[!NOTE]
>
>L&#39;elenco [!UICONTROL Authorized Hosts] viene utilizzato sia per gli host [!DNL Target] che per gli host di reindirizzamento predefiniti. Aggiungi tutti i domini esistenti approvati per l&#39;utilizzo di [!DNL Adobe Target] JavaScript SDK (at.js) *AND* tutti i domini utilizzati negli URL di reindirizzamento predefiniti della posta in arrivo. Aggiungi eventuali nuovi domini simili al inserisco nell&#39;elenco Consentiti di in futuro.

## Eliminare un host {#section_F56355BA4BC54B078A1A8179BC954632}

Quando un host non è più necessario, è possibile eliminarlo.

1. Nell&#39;elenco [!UICONTROL Hosts] fare clic sull&#39;icona **[!UICONTROL Delete]**.
1. Fare clic su **[!UICONTROL Delete]** per confermare l&#39;eliminazione.

>[!NOTE]
>
>L&#39;host viene elencato di nuovo se qualcuno passa a una pagina che contiene una richiesta [!DNL Target] sull&#39;host.

## Risoluzione dei problemi relativi agli host {#concept_B3D7583FA4BB480382CC7453529FE1B7}

Se si verificano problemi con gli host, prova i seguenti suggerimenti di risoluzione:

**L&#39;host non viene visualizzato nell&#39;elenco per il tuo account.**

* Aggiorna la pagina [!UICONTROL Hosts] nel browser.
* Verifica che la richiesta [!DNL Target] sia corretta, incluso il riferimento at.js.
* Prova a passare a una delle [!DNL Target] richieste sull&#39;host. È possibile che in un browser non sia mai stato eseguito il rendering di alcuna richiesta [!DNL Target] sull&#39;host.

**I domini casuali o sconosciuti vengono visualizzati nell&#39;elenco [!UICONTROL Host].**

Un dominio viene visualizzato in questo elenco se viene effettuata una richiesta a [!DNL Target] dal dominio. Spesso, è possibile vedere domini da motori spider, siti di traduzione linguistica o unità disco locali. Se il dominio elencato non è utilizzato dal team, è possibile fare clic su [!UICONTROL Delete] per rimuoverlo.

**La mia richiesta [!DNL Target] restituisce /&#42; nessuna visualizzazione - host mbox non autorizzato &#42;/.**

Se viene effettuata una richiesta [!DNL Target] su un host non autorizzato, la richiesta risponde con /&#42; no display - unauthorized mbox host &#42;/.
