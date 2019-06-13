---
description: Organizza siti e ambienti di preproduzione per gestirli facilmente e per generare rapporti separati.
keywords: host;gruppo host;ambiente;risoluzione dei problemi;best practice
seo-description: Organizza siti e ambienti di preproduzione per gestirli facilmente e per generare rapporti separati.
seo-title: Host
solution: Target
title: Host
topic: Standard
uuid: c7682269-4ec2-4a0f-b053-7e0ec77f4604
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Host{#hosts}

Organizza siti e ambienti di preproduzione per gestirli facilmente e per generare rapporti separati.

## Host {#concept_516BB01EBFBD4449AB03940D31AEB66E}

Organizza siti e ambienti di preproduzione per gestirli facilmente e per generare rapporti separati.

Funzionalità simili erano già presenti in [!DNL Target Classic]. I gruppi di host in [!DNL Target Classic] si chiamavano “ambienti” in [!DNL Target Standard/Premium].

L’obiettivo principale della gestione host è quello di garantire che nessun contenuto inattivo venga visualizzato accidentalmente sui siti web. La gestione host consente inoltre di separare i dati dei rapporti per ambiente.

Un host è un qualsiasi server web (o dominio web) dal quale viene trasmesso il contenuto durante qualsiasi fase del progetto. Viene riconosciuto qualsiasi host che trasmette una mbox.

Per facilitare la gestione, gli host sono raccolti in ambienti. Ad esempio, si potrebbero avere decine di host raggruppati in due o tre ambienti. Gli ambienti preimpostati includono Produzione, Staging e Sviluppo. È anche possibile aggiungere nuovi ambienti e rinominare gli ambienti.

Un ambiente, quello predefinito, è predenominato Produzione. Questo ambiente predefinito non può essere eliminato, anche se lo si rinomina. [!DNL Target] presuppone che è qui che verranno eseguiti attività e test finali e approvati.

Quando una richiesta mbox viene ricevuta da nuovi siti web o domini, questi nuovi domini appaiono sempre nell’ambiente Produzione. Non è possibile modificare le impostazioni dell’ambiente Produzione; in tal modo siti nuovi o sconosciuti visualizzano sicuramente solo il contenuto che è attivo e pronto. La gestione degli host consente inoltre di garantire facilmente la qualità di nuove attività e contenuti nei test, nella gestione temporanea (staging) e negli ambienti di sviluppo prima di attivare le attività.

Target non limita un host che può inviare e ricevere mbox. Quindi, quando compaiono nuovi server o domini, questi funzionano automaticamente (a meno che non sia impostata una whitelist o blacklist). Ciò consente inoltre di testare gli annunci su domini diversi che non si conoscono o non si possono anticipare.

Per gestire gli host e gli ambienti, fai clic su **[!UICONTROL Configurazione]** &gt; **[!UICONTROL Host]**.

![](assets/hosts_list.png)

## Riconoscere gli host {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

Informazioni sulle condizioni che devono essere soddisfatte affinché [!DNL Target] possa riconoscere un host e aggiungerlo all’elenco degli host.

Per riconoscere un host, devono essere soddisfatte le seguenti condizioni:

* Almeno una mbox deve esistere sull’host
* Una pagina sull’host deve avere quanto segue:

   * Un preciso riferimento a [!DNL mbox.js]
   * Una mbox o una chiamata mbox globale generata automaticamente

* La pagina con la mbox deve essere visualizzata in un browser

Dopo aver visualizzato la pagina, l’host è presente nell’elenco degli [!UICONTROL host]; è quindi possibile gestirlo in un ambiente, nonché visualizzare in anteprima e avviare attività e test.

>[!NOTE] {class=“- topic/note ”}
>
>Questo include tutti i server di sviluppo personali.

Dopo aver aggiunto un host all’elenco degli [!UICONTROL host], assicurati che l’host sia riconosciuto.

1. Fai clic su **[!UICONTROL Configurazione]** &gt; **[!UICONTROL Host]**.
1. Se l’host non è elencato, aggiorna il browser. 
Per impostazione predefinita, un host appena riconosciuto viene inserito nell’ambiente Produzione. Questo è l’ambiente più sicuro perché non consente di visualizzare le attività inattive da questi host.
1. (Condizionale) Sposta l’host nell’ambiente Sviluppo o Staging.

>[!NOTE]
>
>L’ambiente Produzione non può essere eliminato, anche se lo si rinomina. Si presuppone che è qui che verranno eseguiti attività e test attivi e finali. L’ambiente predefinito non consente di visualizzare le campagne inattive.

## Gestire host e ambienti {#concept_90573F5A52E04600A8C3C5897880C10F}

Informazioni su come gestire host e ambienti (gruppi host), tra cui impostazione dell’host predefinito per la generazione dei rapporti, creazione di whitelist, modifica del nome di un ambiente, spostamento di un host in un altro ambiente ed eliminazione di un host o un ambiente.


Per accedere all’elenco [!UICONTROL Host], fai clic su **[!UICONTROL Configurazione]** &gt; **[!UICONTROL Host]**.

![](assets/hosts_list.png)

## Filtrare, ordinare o cercare nell’elenco Host {#section_068B23C9D8224EB78BC3B7C8580251B0}

Per filtrare gli elenchi [!UICONTROL Host] in base all’ambiente, fai clic sul menu a discesa **[!UICONTROL Tutto]**, quindi seleziona l’ambiente desiderato (produzione, gestione temporanea, sviluppo o un ambiente personalizzato già creato).

Per ordinare l’elenco [!UICONTROL Host], fai clic su qualsiasi intestazione di colonna (Nome, Ambiente o Ultima richiesta) per ordinare l’elenco in ordine crescente o decrescente.

Per cercare nell’elenco [!UICONTROL Host], digita un termine nella casella di ricerca.

## Selezionare più host {#section_EF3B458475184B7EA997C3559714397C}

Per selezionare più host, seleziona le caselle di controllo accanto alla colonna [!UICONTROL Nome] per gli host desiderati. È quindi possibile spostare o eliminare tutti gli host selezionati.

## Creare un ambiente {#section_32097D0993724DF3A202D164D3F18674}

1. Dall’elenco [!UICONTROL Host], fai clic sulla scheda **[!UICONTROL Ambienti]**.
1. Fai clic su **[!UICONTROL Crea ambiente]**.
1. Specifica un nome descrittivo per l’ambiente.
1. Specifica la modalità attiva desiderata per l’ambiente: [!UICONTROL Attività attive] o [!UICONTROL Attività attive e inattive].
1. Fai clic su **[!UICONTROL Salva]**.

## Impostare l’host predefinito per la creazione dei rapporti {#section_4F8539B07C0C45E886E8525C344D5FB0}

È possibile selezionare l’ambiente che si desidera utilizzare come impostazione predefinita per tutti i rapporti di attività.

Se si utilizza la produzione come predefinita, tutti gli host sconosciuti vengono aggiunti automaticamente qui e i dati del rapporto sono inclusi nella visualizzazione di rapporti predefinita. Invece, la creazione di un ambiente “pulito” assicura che siano inclusi solo i siti e domini principali.

Per impostare l’ambiente predefinito per la segnalazione:

1. Dall’elenco [!UICONTROL Host], fai clic sulla scheda **[!UICONTROL Impostazioni]**.
1. Seleziona l’host predefinito dal menu a discesa **[!UICONTROL Impostazioni ambiente]**.
1. Fai clic su **[!UICONTROL Salva]**.

>[!NOTE]
>
>Se gli host passano ad altri gruppi host, gli utenti che usano la funzionalità [!DNL Recommendations] devono rigenerare il database dei comportamenti e quello dei prodotti.

## Creare whitelist che specificano gli host autorizzati per l’invio di chiamate mbox a Target. {#section_0AF7F56C386A42C381AF704DEF08D5CC}

È possibile creare una whitelist che specifichi gli host (domini) autorizzati a inviare chiamate mbox a [!DNL Target]. Tutti gli altri host che generano chiamate riceveranno una risposta di errore di autorizzazione, inserita come riga di commento. Per impostazione predefinita, qualsiasi host che contiene una chiamata mbox si registra con [!DNL Target] nell’Ambiente di produzione e ha accesso a tutte le attività attive e approvate. Se questo non è l’approccio desiderato, è invece possibile utilizzare la whitelist per registrare host specifici idonei a fare chiamate mbox e a ricevere i contenuti di [!DNL Target]. Tutti gli host continuano a essere visualizzati nell’elenco [!UICONTROL Host] e gli ambienti possono comunque essere utilizzati per raggruppare questi host e assegnare diversi livelli a ciascuno, ad esempio se l’host può visualizzare campagne attive e/o inattive.

Per creare una whitelist:

1. Dall’elenco [!UICONTROL Host], fai clic sulla scheda **[!UICONTROL Impostazioni]**.
1. Seleziona la casella di controllo **[!UICONTROL Abilita host autorizzati per la distribuzione dei contenuti]**.
1. Aggiungi gli host desiderati nella casella **[!UICONTROL L’host contiene]**, come desiderato.

   È possibile elencare più host, ciascuno sulla propria linea.

1. Fai clic su **[!UICONTROL Salva]**.

Se una chiamata mbox viene effettuata su un host non autorizzato, la chiamata risponderà con `/* no display - unauthorized mbox host */`.

La whitelist prevale sugli ambienti. È necessario cancellare tutti gli host prima di utilizzare la funzione whitelist: nell’elenco Host verranno quindi elencati solo gli host consentiti dalla whitelist. A questo punto puoi spostare gli host nell’ambiente desiderato.

A volte i domini da altri siti appaiono negli ambienti. Un dominio viene incluso nell’elenco se effettua una chiamata al tuo mbox. js. Ad esempio, se qualcuno copia una delle tue pagine web sul suo server, tale dominio verrà visualizzato nel tuo ambiente. Potrebbe anche essere possibile vedere domini da motori spider, siti di traduzione linguistica o unità disco locali.

Nei casi in cui `mboxHost` viene passato in una chiamata API, la conversione viene registrata per l’ambiente passato. Se non viene passato alcun ambiente, l’host nella chiamata viene impostato automaticamente su Produzione.

È inoltre possibile creare una lista nera che specifichi gli host (domini) che non possono inviare le chiamate mbox a [!DNL Target] aggiungendo gli host desiderati nell’host nella casella [!UICONTROL L’host non contiene].

## Modificare il nome di un ambiente {#section_9F5F94285F8E495E9CE69810CE94CA08}

1. Dall’elenco [!UICONTROL Host], fai clic sulla scheda **[!UICONTROL Ambienti]**.
1. Passa il cursore del mouse sull’ambiente desiderato, quindi fai clic sull’icona **[!UICONTROL Modifica]**.
1. Modifica il nome dell’ambiente.
1. Fai clic su **[!UICONTROL Salva]**.

## Spostare un host in un ambiente diverso {#section_9F52549958BD485EB74FE78C32773D2A}

1. Nell’elenco [!UICONTROL Host], passa il cursore del mouse sull’host da spostare.
1. Fai clic sull’icona **[!UICONTROL Sposta]**.
1. Seleziona l’ambiente desiderato dal menu a discesa, quindi fai clic sul segno di spunta.

## Eliminare un host {#section_F56355BA4BC54B078A1A8179BC954632}

Quando un host non è più necessario, è possibile eliminarlo.

1. Nell’elenco [!UICONTROL Host], passa il cursore del mouse sull’host da eliminare.
1. Fai clic sull’icona **[!UICONTROL Elimina]**.
1. Fai clic su **[!UICONTROL Elimina]** per confermare l’eliminazione.

>[!NOTE]
>
>L’host sarà elencato di nuovo se qualcuno passa a una pagina con mbox sull’host.

## Eliminare un ambiente {#section_737F8869612047868D03FC755B1223D3}

Quando un ambiente non è più necessario, è possibile eliminarlo.

1. Dall’elenco [!UICONTROL Host], fai clic sulla scheda **[!UICONTROL Ambienti]**.
1. Passa il cursore del mouse sull’ambiente da eliminare.
1. Fai clic sull’icona **[!UICONTROL Elimina]**.
1. Fai clic su **[!UICONTROL Elimina]** per confermare l’eliminazione.

>[!NOTE]
>
>Non è possibile eliminare l’ambiente di produzione, ma è possibile rinominarlo.

## Risoluzione dei problemi relativi agli host {#concept_B3D7583FA4BB480382CC7453529FE1B7}

Procedure consigliate per la gestione e la risoluzione dei problemi relativi agli host in [!DNL Adobe Target].

Se si verificano problemi con gli host, prova i seguenti suggerimenti di risoluzione:

**L’host non compare nell’elenco delle mbox per il tuo account.**

* Aggiorna la pagina [!UICONTROL Host] nel browser.
* Verifica che il codice della mbox sia corretto, incluso il riferimento a [!DNL mbox.js].
* Prova a passare a una delle mbox sull&#39;host. È possibile che sia ancora stato eseguito il rendering in un browser per nessuna mbox dell’host.

**Domini casuali o sconosciuti vengono visualizzati nell&#39;elenco[!UICONTROL Host].**

Un dominio viene visualizzato in questo elenco se viene effettuata una chiamata a [!DNL Target] dal dominio. Spesso, è possibile vedere domini da motori spider, siti di traduzione linguistica o unità disco locali. Se il dominio elencato non è tra quelli utilizzati dal team, è possibile fare clic su [!UICONTROL Elimina] per rimuoverlo.

**La mia chiamata mbox restituisce /* no display - unauthorized mbox host */.**

Se una chiamata mbox viene effettuata su un host non autorizzato, la chiamata risponderà con /* no display - unauthorized mbox host */.

## Recommendations: filtrare raccolte ed esclusioni per ambiente (gruppo di host)

![Badge Premium](/help/assets/premium.png)

Puoi visualizzare in anteprima il contenuto delle raccolte ed esclusioni di Consigli per un ambiente selezionato (gruppo di host).

>[!NOTE]
>Le attività Consigli sono disponibili come parte della soluzione Target Premium. Non sono disponibili in Target Standard senza una licenza di Target Premium.

Il gruppo di host può essere utilizzato per separare gli elementi disponibili nel catalogo per usi diversi. Ad esempio, puoi utilizzare i gruppi di host per ambienti di sviluppo e produzione, marchi diversi o diverse aree geografiche. Per impostazione predefinita, i risultati dell&#39;anteprima in Ricerca nel catalogo, Raccolte ed Esclusioni si basano sul gruppo di host predefinito. Puoi anche selezionare un gruppo di host diverso per visualizzare in anteprima i risultati, utilizzando il filtro Ambiente. Per impostazione predefinita, gli elementi appena aggiunti sono disponibili in tutti i gruppi di host, a meno che non sia specificato un ID ambiente al momento della creazione o dell&#39;aggiornamento dell&#39;elemento. I consigli distribuiti dipendono dal gruppo di host specificato nella richiesta.

Se i prodotti non vengono visualizzati, assicurati di utilizzare il gruppo host corretto. Ad esempio, se imposti che il consiglio usi un ambiente di gestione temporanea e imposti il gruppo host su Gestione temporanea, potrebbe essere necessario ricreare le raccolte nell&#39;ambiente di gestione temporanea perché si visualizzino i prodotti. Per visualizzare i prodotti disponibili in ogni ambiente, utilizza Ricerca catalogo con ogni ambiente. Puoi anche visualizzare in anteprima il contenuto delle raccolte ed esclusioni di Recommendations per un ambiente selezionato (gruppo di host).

>[!NOTE]
>Dopo aver modificato l’ambiente selezionato, fai clic su Cerca per aggiornare i risultati restituiti.

Il filtro Ambiente è disponibile nelle seguenti posizioni nell’interfaccia utente di Target:

* Ricerca nel catalogo ([!UICONTROL Recommendations &gt; Ricerca nel catalogo])
* Finestra di dialogo Crea raccolta ([!UICONTROL Recommendations &gt; Raccolte &gt; Crea nuova])
* Finestra di dialogo Aggiorna raccolta ([!UICONTROL Recommendations &gt; Raccolte &gt; Modifica])
* Finestra di dialogo Crea esclusione ([!UICONTROL Recommendations &gt; Esclusioni &gt; Crea nuova])
* Finestra di dialogo Aggiorna esclusione ([!UICONTROL Recommendations &gt; Esclusioni &gt; Modifica])
