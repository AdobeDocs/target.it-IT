---
keywords: pagine del sito;pagine del sito di destinazione;targeting;pagina corrente;pagina corrente target;pagina precedente;pagina precedente target;pagina di destinazione;pagina di destinazione target;intestazione http
description: Scopri come eseguire il targeting dei visitatori utilizzando Adobe [!DNL Target] che si trovano su una pagina specifica del sito.
title: Posso [!DNL Target] Visitatori in base alle pagine del sito?
feature: Tipi di pubblico
exl-id: 4c770b7b-775f-4483-aced-43f18a9a68c1
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 40%

---

# Pagine del sito

Puoi eseguire il targeting dei visitatori che si trovano su una pagina specifica del tuo sito.

1. Nell’interfaccia di [!DNL Target] fai clic su **[!UICONTROL Pubblico]** > **[!UICONTROL Crea pubblico]**.
1. Dai un nome al pubblico.
1. Fai clic su **[!UICONTROL Aggiungi regola]** > **[!UICONTROL Pagine del sito]**.

   ![Pubblico per pagine del sito](assets/target_site_pages.png)

1. Fai clic sull&#39;elenco a discesa **[!UICONTROL Seleziona]** , seleziona una delle opzioni seguenti, quindi configura la regola nel modo desiderato.

   Le opzioni disponibili e i valutatori negli elenchi a discesa successivi nella regola variano a seconda dell’opzione scelta. L&#39;illustrazione seguente mostra le opzioni disponibili se scegli [!UICONTROL Pagina corrente]:

   ![Pagina corrente](/help/c-target/c-audiences/c-target-rules/assets/current-page.png)

   Le seguenti opzioni sono disponibili nell&#39;elenco a discesa iniziale quando scegli [!UICONTROL Seleziona].

   * **Pagina corrente:** la pagina sulla quale l’utente si trova attualmente.

      Se scegli questa opzione, nel secondo elenco a discesa sono disponibili le seguenti opzioni:

      * URL (Per ulteriori informazioni su come Target valuta gli URL, consulta [Domande frequenti su destinazioni e pubblico](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * Dominio
      * Query
      * Sottodominio
      * Dominio di primo livello
      * Percorso
      * Frammento hash (#)
   * **Pagina precedente:** la pagina sulla quale si trovava l’utente prima di fare clic per passare alla pagina corrente. (L’utente deve fare clic dalla pagina precedente a quella corrente, affinché la pagina venga tracciata. La pagina precedente non viene tracciata se l’utente digita un nuovo URL nel browser). Il contenuto effettivo di questa pagina dipende dalla progettazione del sito. Ad esempio, se la pagina corrente mostra informazioni su un prodotto specifico, quella precedente potrebbe essere una pagina di categoria in cui il visitatore seleziona l’elemento specifico (ad esempio, una pagina contenente più telecamere di un certo tipo) o la pagina principale che porta alla pagina finale.

      Se scegli questa opzione, nel secondo elenco a discesa sono disponibili le seguenti opzioni:

      * URL (Per ulteriori informazioni su come Target valuta gli URL, consulta [Domande frequenti su destinazioni e pubblico](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * Dominio
      * Query
      * Sottodominio
      * Dominio di primo livello
      * Percorso
   * **Pagina di destinazione:** è la prima pagina che il visitatore vede quando accede al tuo sito. Ad esempio, se il visitatore fa clic su un collegamento su Google che porta a una pagina di categoria, la pagina di categoria è la pagina di destinazione. Se il collegamento rimanda alla pagina principale, quest’ultima corrisponde alla pagina di destinazione. La pagina di destinazione viene memorizzata per la sessione del visitatore. Puoi eseguire un targeting più approfondito nel sito in base alla pagina di destinazione del visitatore nella sessione.

      Se scegli questa opzione, nel secondo elenco a discesa sono disponibili le seguenti opzioni:

      * URL (Per ulteriori informazioni su come Target valuta gli URL, consulta [Domande frequenti su destinazioni e pubblico](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * Dominio
      * Query
      * Sottodominio
      * Dominio di primo livello
      * Percorso
      * Frammento hash (#)

      >[!NOTE]
      >
      >L’oggetto `landing.url` viene reimpostato in caso di modifica del sottodominio o di sostituzione diretta dell’URL.

   * **Intestazione HTTP:** questa opzione valuta le informazioni nell’intestazione HTTP della richiesta Target. Ad esempio, se l’intestazione HTTP contiene informazioni sulla lingua, puoi creare una regola contenente la condizione `Accept-Language: es` per indirizzare l’attività ai visitatori che accedono alla pagina in spagnolo.

      Se scegli questa opzione, nel secondo elenco a discesa sono disponibili le seguenti opzioni:

      * Accetta
      * Accept-Charset
      * Accept-Encoding
      * Accept-Language
      * Autorizzazione
      * Controllo cache
      * Connessione
      * Lunghezza del contenuto
      * Content-MDS
      * Content-Type
      * Data
      * Attesa
      * Da
      * Host
      * If-Match
      * If-Modified-Since
      * If-None-Match
      * If-Range
      * If-Unmodified-Since
      * Max-Forwards
      * Praga
      * Autorizzazione proxy
      * Intervallo
      * Referente
      * TE
      * Aggiornamento
      * Agente utente
      * Via
      * Attenzione

   Se si sceglie [!UICONTROL Pagina corrente], [!UICONTROL Pagina precedente] o [!UICONTROL Pagina di destinazione], sono disponibili le opzioni [!UICONTROL Dominio] e [!UICONTROL Query]. Quando scegli queste opzioni, considera quanto segue:

   * **Dominio:** il dominio completo della pagina. Nella specificazione di un dominio, è consigliabile utilizzare “contiene”, perché se ad esempio usi “dominio è uguale a facebook.com”, non verranno accettati né `m.facebook.com` né `www.facebook.com`. Se invece utilizzi “dominio contiene facebook.com” verrà accettata qualsiasi variante di facebook.com.
   * **Query:** il contenuto dell’URL dopo il primo punto interrogativo (?).

      `foo.html?e0a72cb2a2c7`





1. (Facoltativo) Fai clic su **[!UICONTROL Aggiungi regola]** per impostare regole aggiuntive per il pubblico.
1. Fai clic su **[!UICONTROL Salva]**.

Puoi anche creare un pubblico per le pagine del sito utilizzando un “parametro di query definito dall’utente” o una “intestazione definita dall’utente”.

Utilizza:

* Un parametro di query se la regola selezionata è Pagina corrente, Pagina di destinazione o Pagina precedente.
* Intestazione se la regola selezionata dall&#39;utente è un&#39;intestazione HTTP.

Come illustrato di seguito:

![](assets/site_pages.png)

## Risoluzione dei problemi {#ts}

* Affinché il pubblico della pagina di destinazione funzioni correttamente, le richieste devono avere il parametro `mboxReferrer` impostato (per l’API di consegna il parametro `context.address.referringUrl` ) che la libreria JavaScript at.js recupera dalla pagina utilizzando l’attributo `document.referrer` . Questo attributo `HTMLDocument` restituisce l’URI della pagina da cui l’utente ha navigato. Il valore di questo attributo è una stringa vuota quando l&#39;utente passa direttamente alla pagina (non tramite un collegamento, ma, ad esempio, tramite un segnalibro).

   Se questo comportamento non soddisfa le tue esigenze, considera l&#39;esecuzione di una delle seguenti azioni:

   * Passa i parametri [mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md) a [!DNL Target] per essere utilizzati a scopo di targeting.
   * Utilizza un’attività [Test A/B](/help/c-activities/t-test-ab/test-ab.md) invece di un’attività della pagina di destinazione. Le attività di test A/B non cambiano le esperienze per lo stesso visitatore.
   * Utilizza invece un [profilo visitatore](/help/c-target/c-audiences/c-target-rules/visitor-profile.md).

* Quando utilizzi i valutatori &quot;inizia/termina con&quot; su stringhe contenenti virgole, tieni presente che queste
sono valutati come una matrice di valori in cui viene valutato ogni valore separato da virgole. Ad esempio, se disponiamo del valore per un’intestazione: `Accept-Language: en,zh;q=0.9,en-IN;q=0.8,zh-CN;q=0.7` consente di specificare condizioni quali:
   * inizia con zh,
   * inizia con en,
   * termina con 0,7,
   * termina con 0,8.

## Video di formazione: Creazione di tipi di pubblico

Questo video contiene informazioni sull&#39;utilizzo delle categorie di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392)
