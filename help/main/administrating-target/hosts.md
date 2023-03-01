---
keywords: host;host;gruppo host;risoluzione dei problemi;best practice;ubox;reindirizzamenti;reindirizzare;whitelist;inserire nell'elenco Consentiti;blacklist;inserire nell'elenco Bloccati;host;hosts;host group;problem eshooting;best practice;ubox;redirect;whitelist;whitelist;;blacklist;
description: Scopri come organizzare i siti web e gli ambienti di preproduzione per gestirli facilmente e per creare rapporti separati all’interno di Adobe Target.
title: Cosa sono gli host e come li utilizzo?
feature: Administration & Configuration
role: Admin
exl-id: 31c661c0-686d-440e-ad58-864fb853b1c4
source-git-commit: 3ac61272ee1ccd72a8670966f181e7798cbe9f76
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 22%

---

# Host

Organizza siti e ambienti di pre-produzione per gestirli facilmente e generare rapporti separati in [!DNL Adobe Target].

L’obiettivo principale della gestione host è quello di garantire che nessun contenuto inattivo venga visualizzato accidentalmente sui siti web. La gestione degli host consente inoltre di separare i dati dei rapporti in base a [ambiente](/help/main/administrating-target/environments.md).

Un host è qualsiasi dominio da cui un [!DNL Target] richiesta effettuata. In un sito Web, in genere è `location.hostname` proprietà dell’URL che crea [!DNL Target] richiesta.

Per impostazione predefinita, [!DNL Target] non limita un host che può [!DNL Target] richieste e ricezione [!DNL Target] risposte. Quando nuovi host effettuano richieste, queste funzionano automaticamente. Questo processo consente anche di eseguire test su domini diversi che non conosci o che non puoi prevedere. Se si desidera ignorare questo comportamento predefinito, è possibile impostare un inserire nell&#39;elenco Consentiti inserisco nell&#39;elenco Bloccati di o di per limitare gli host con cui lavorare [!DNL Target].

Per gestire gli host, fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Host]**.

![immagine hosts_list](assets/hosts_list.png)

## Riconoscere gli host {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

Per riconoscere un host e aggiungerlo al [!UICONTROL Host] devono essere soddisfatte le seguenti condizioni:

* Almeno uno [!DNL Target] la richiesta deve esistere sull&#39;host
* Una pagina sull’host deve avere quanto segue:

   * Un preciso riferimento at.js
   * A [!DNL Target] richiesta o un globale generato automaticamente [!DNL Target] richiesta

* La pagina con [!DNL Target] La richiesta deve essere visualizzata in un browser

Una volta visualizzata la pagina, l’host viene elencato in [!UICONTROL Host] , che consente di gestirlo in un ambiente e di visualizzare in anteprima e avviare attività e test.

>[!NOTE]
>
>Questo include tutti i server di sviluppo personali.

Dopo aver aggiunto un host all’elenco degli [!UICONTROL host], assicurati che l’host sia riconosciuto.

1. Clic **[!UICONTROL Amministrazione]** > **[!UICONTROL Host]**.
1. Se l’host non è elencato, aggiorna il browser. 


   Per impostazione predefinita, un host appena riconosciuto viene posizionato nel [!UICONTROL Produzione] ambiente. Il [!UICONTROL Produzione] L’ambiente è l’ambiente più sicuro perché non consente la visualizzazione delle attività inattive da questi host.

1. (Condizionale) Fai clic su **[!UICONTROL Sposta]** icona ( ![icona sposta](/help/main/administrating-target/assets/icon-move.png) ) per spostare l&#39;host in [!UICONTROL Sviluppo], [!UICONTROL Staging]o in un altro ambiente.

>[!NOTE]
>
>Il [!UICONTROL Produzione] L’ambiente non può essere eliminato, anche se lo si rinomina. Si presume che questo ambiente sia il luogo in cui vengono eseguiti attività e test finali e attivi. L’ambiente predefinito non consente di visualizzare le campagne inattive.

## Ordinare o cercare nell’elenco Host {#section_068B23C9D8224EB78BC3B7C8580251B0}

Per ordinare [!UICONTROL Host] , fare clic su un&#39;intestazione di colonna ([!UICONTROL Nome], [!UICONTROL Ambiente], o [!UICONTROL Ultima richiesta]) per ordinare l&#39;elenco in ordine crescente o decrescente.

Per eseguire ricerche in [!UICONTROL Host] digitare un termine di ricerca nell&#39; [!UICONTROL Cerca host] casella.

## Inserire nell&#39;elenco Consentiti Creazione di che specificano gli host autorizzati per l&#39;invio [!DNL Target] richieste a [!DNL Target]. {#allowlist}

È possibile creare un inserisco nell&#39;elenco Consentiti di che specifichi gli host (domini) autorizzati all&#39;invio [!DNL Target] richieste a [!DNL Target]. Tutti gli altri host che generano richieste ricevono una risposta di errore di autorizzazione commentata. Per impostazione predefinita, qualsiasi host che contiene [!DNL Target] registri di richieste con [!DNL Target] nel [!UICONTROL Produzione] e ha accesso a tutte le attività attive e approvate. Se questo approccio non è desiderato, è invece possibile utilizzare il inserisco nell&#39;elenco Consentiti di per registrare host specifici che sono idonei a effettuare [!DNL Target] richieste e ricezione [!DNL Target] contenuto. Tutti gli host continuano a essere visualizzati in [!UICONTROL Host] Gli ambienti, e, possono comunque essere utilizzati per raggruppare questi host e assegnare diversi livelli a ciascuno, ad esempio se l’host può visualizzare le attività attive e/o inattive.

Per creare un inserisco nell&#39;elenco Consentiti di:

1. Dalla sezione [!UICONTROL Host] , fare clic su **[!UICONTROL Autorizza host]**.
1. Abilita **[!UICONTROL Abilita host autorizzati per la distribuzione dei contenuti]** attivare/disattivare.
1. Aggiungi gli host desiderati nel **[!UICONTROL L’host contiene]** a seconda delle esigenze.

   È possibile elencare più host, ciascuno sulla propria linea.

1. Aggiungi gli host desiderati nel **[!UICONTROL L’host non contiene]** a seconda delle esigenze.

   È possibile elencare più host, ciascuno sulla propria linea.

1. Fai clic su **[!UICONTROL Salva]**.

Se un [!DNL Target] viene effettuata su un host non autorizzato, la chiamata risponde con `/* no display - unauthorized mbox host */`.

>[!IMPORTANT]
>
>**Best practice per la sicurezza**: se utilizzi la funzionalità ubox di [!DNL Target], questo inserisco nell&#39;elenco Consentiti di controlla anche l’elenco dei domini a cui [redirector](https://developer.adobe.com/target/implement/email/working-with-redirectors/){target=_blank} può navigare. Assicurati di aggiungere tutti i domini a cui desideri reindirizzare quando utilizzi ubox come parte dell’implementazione. Se il inserisco nell&#39;elenco Consentiti di viene lasciato non specificato, [!DNL Adobe] non è in grado di verificare gli URL di reindirizzamento e di proteggere da potenziali reindirizzamenti dannosi.
>
>Il inserisco nell&#39;elenco Consentiti di ha la precedenza sugli ambienti. Cancella tutti gli host prima di utilizzare la funzione di inserisce nell&#39;elenco Consentiti di, quindi nell’elenco degli host vengono visualizzati solo gli host consentiti dal inserisco nell&#39;elenco Consentiti di. A questo punto puoi spostare gli host nell’ambiente desiderato.

A volte i domini da altri siti appaiono negli ambienti. Un dominio viene visualizzato nell’elenco se chiama at.js. Ad esempio, se qualcuno copia una delle tue pagine web sul suo server, tale dominio verrà visualizzato nel tuo ambiente. Potrebbe anche essere possibile vedere domini da motori spider, siti di traduzione linguistica o unità disco locali.

Nei casi in cui `mboxHost` viene passato in una chiamata API, la conversione viene registrata per l’ambiente passato. Se non viene passato alcun ambiente, l’host nella chiamata viene impostato come predefinito su [!UICONTROL Produzione].

È inoltre possibile creare un inserisco nell&#39;elenco Bloccati di che specifichi gli host (domini) che non possono inviare [!DNL Target] richieste a [!DNL Target] aggiungendo gli host desiderati nel [!UICONTROL L’host non contiene] casella.

>[!NOTE]
>
>Il [!UICONTROL Host autorizzati] l’elenco è utilizzato per entrambi [!DNL Target] host e host di reindirizzamento predefiniti. Aggiungi tutti i domini esistenti approvati per l&#39;utilizzo di [!DNL Adobe Target] SDK JavaScript (at.js) *E* tutti i domini utilizzati negli URL di reindirizzamento predefiniti della ubox. Aggiungi eventuali nuovi domini simili al inserisco nell&#39;elenco Consentiti di in futuro.

## Eliminare un host {#section_F56355BA4BC54B078A1A8179BC954632}

Quando un host non è più necessario, è possibile eliminarlo.

1. Dalla sezione [!UICONTROL Host] , fare clic sul pulsante **[!UICONTROL Elimina]** icona.
1. Fai clic su **[!UICONTROL Elimina]** per confermare l’eliminazione.

>[!NOTE]
>
>L’host viene elencato di nuovo se qualcuno passa a una pagina che contiene [!DNL Target] sull&#39;host.

## Risoluzione dei problemi relativi agli host {#concept_B3D7583FA4BB480382CC7453529FE1B7}

Se si verificano problemi con gli host, prova i seguenti suggerimenti di risoluzione:

**L’host non viene visualizzato nell’elenco per il tuo account.**

* Aggiorna la pagina [!UICONTROL Host] nel browser.
* Confermare che [!DNL Target] richiesta corretta, incluso il riferimento at.js.
* Prova a passare a uno dei [!DNL Target] richieste sull’host. È possibile che no [!DNL Target] richiesta sull’host è mai stata sottoposta a rendering in un browser.

**Domini casuali o sconosciuti vengono visualizzati nell&#39;elenco [!UICONTROL Host].**

Un dominio viene visualizzato in questo elenco se una richiesta a [!DNL Target] viene creato dal dominio. Spesso, è possibile vedere domini da motori spider, siti di traduzione linguistica o unità disco locali. Se il dominio elencato non è tra quelli utilizzati dal team, è possibile fare clic su [!UICONTROL Elimina] per rimuoverlo.

**I miei [!DNL Target] restituisce richiesta /&#42; nessuna visualizzazione - host mbox non autorizzato &#42;/.**

Se un [!DNL Target] richiesta effettuata su un host non autorizzato, la richiesta risponde con /&#42; nessuna visualizzazione - host mbox non autorizzato &#42;/.
