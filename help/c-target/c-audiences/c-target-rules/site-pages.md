---
description: Puoi indirizzare l’attività ai visitatori che si trovano su una pagina specifica o con un parametro mbox specifico.
keywords: pagine del sito;pagine del sito target;targeting;pagina corrente;pagina corrente target;pagina precedente;pagina precedente target;pagina di destinazione;pagina di destinazione target;mbox;mbox target
seo-description: Potete eseguire il targeting dei visitatori che si trovano su una pagina specifica o che dispongono di un parametro mbox specifico utilizzando Adobe Target.
seo-title: Pagine del sito in Adobe Target
solution: Target
title: Pagine del sito
topic: Standard
uuid: 1cf9fa94-dbec-4719-9a0a-79c1eb91a233
translation-type: tm+mt
source-git-commit: a1732632ad85a0f3742177663ee7d9a617098ff5

---


# Pagine del sito{#site-pages}

Potete eseguire il targeting dei visitatori che si trovano su una pagina specifica o che dispongono di un parametro mbox specifico.

>[!NOTE]
>
>I tipi di pagina del sito e gli operatori di confronto del pubblico ora corrispondono ai tipi e agli operatori di confronto di Target Classic. Puoi creare un pubblico per la pagina del sito utilizzando un “parametro di query definito dall’utente” o una “intestazione definita dall’utente”.

1. Nell’interfaccia di [!DNL Target], fai clic su **[!UICONTROL Pubblico]** &gt; **[!UICONTROL Crea pubblico]**.
1. Dai un nome al pubblico.
1. Fai clic su **[!UICONTROL Aggiungi regola]** &gt; **[!UICONTROL Pagine del sito]**.

   ![Pubblico per pagine del sito](assets/target_site_pages.png)

1. Fai clic su **[!UICONTROL Seleziona]**, quindi scegli una delle seguenti opzioni:

   * **Pagina corrente:** la pagina sulla quale l’utente si trova attualmente, cioè la pagina che contiene una mbox nell’attività. In caso di targeting a livello di attività, potrebbe essere una pagina con una mbox utilizzata per definire le condizioni di ingresso, o una pagina che visualizza il contenuto. Se esegui il targeting per esperienza, la pagina corrente è quella che include la mbox di visualizzazione. Per il targeting basato su metrica di successo o conversione, si tratta della pagina sulla quale si trovano tali mbox.
   * **Pagina precedente:** la pagina sulla quale si trovava l’utente prima di fare clic per passare alla pagina corrente. (L’utente deve fare clic dalla pagina precedente a quella corrente, affinché la pagina venga tracciata. La pagina precedente non viene tracciata se l’utente digita un nuovo URL nel browser). Il contenuto effettivo di questa pagina dipende dalla progettazione del sito. Ad esempio, se la pagina corrente mostra informazioni su un prodotto specifico, quella precedente potrebbe essere una pagina di categoria in cui il visitatore seleziona l’elemento specifico (ad esempio, una pagina contenente più telecamere di un certo tipo) o la pagina principale che porta alla pagina finale.
   * **Pagina di destinazione:** è la prima pagina che il visitatore vede quando accede al tuo sito. Ad esempio, se il visitatore fa clic su un collegamento su Google che porta a una pagina di categoria, la pagina di categoria è la pagina di destinazione. Se il collegamento rimanda alla pagina principale, quest’ultima corrisponde alla pagina di destinazione. La pagina di destinazione viene memorizzata per la sessione del visitatore. Puoi eseguire un targeting più approfondito nel sito in base alla pagina di destinazione del visitatore nella sessione.

      >[!NOTE]
      >
      >L’oggetto `landing.url` viene reimpostato in caso di modifica del sottodominio o di sostituzione diretta dell’URL.

   * **Mbox:** la mbox su cui esegui il targeting. Ad esempio, per conteggiare gli ordini con un totale di 100 $ o più, devi passare `orderTotal` come parametro mbox con il targeting qui specificato.
   * **Dominio:** il dominio completo della pagina. Nella specificazione di un dominio, è consigliabile utilizzare “contiene”, perché se ad esempio usi “dominio è uguale a facebook.com”, non verranno accettati né `m.facebook.com` né `www.facebook.com`. Se invece utilizzi “dominio contiene facebook.com” verrà accettata qualsiasi variante di facebook.com.
   * **Query:** il contenuto dell’URL dopo il primo punto interrogativo (?).

      `foo.html?e0a72cb2a2c7`

1. (Facoltativo) Fai clic su **[!UICONTROL Aggiungi regola]** per impostare regole aggiuntive per il pubblico.
1. Fai clic su **[!UICONTROL Salva]**.

Puoi anche creare un pubblico per le pagine del sito utilizzando un “parametro di query definito dall’utente” o una “intestazione definita dall’utente”.

Utilizza:

* Un parametro di query se la regola selezionata è Pagina corrente, Pagina di destinazione o Pagina precedente.
* Un’intestazione se la regola selezionata è un’intestazione HTTP.

Come illustrato di seguito:

![](assets/site_pages.png)

## Risoluzione dei problemi {#ts}

* Affinché il pubblico della pagina di destinazione funzioni correttamente, le richieste devono avere il `mboxReferrer` parametro impostato (per l'API di consegna il `context.address.referringUrl` parametro) che la libreria JavaScript at.js prende dalla pagina utilizzando l' `document.referrer` attributo. Questo `HTMLDocument` attributo restituisce l’URI della pagina da cui l’utente ha navigato. Il valore di questo attributo è una stringa vuota quando l'utente si sposta direttamente sulla pagina (non attraverso un collegamento, ma, ad esempio, tramite un segnalibro).

   Se questo comportamento non soddisfa i requisiti dell'utente, effettuare una delle seguenti operazioni:

   * Trasmettete i parametri [](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md) mbox da [!DNL Target] utilizzare per il targeting.
   * Utilizzate un'attività [Test](/help/c-activities/t-test-ab/test-ab.md) A/B invece di un'attività sulla pagina di destinazione. Le attività di test A/B non modificano le esperienze per lo stesso visitatore.
   * Utilizzate invece un profilo [](/help/c-target/c-audiences/c-target-rules/visitor-profile.md) visitatore.

## Video di formazione: Creazione di tipi di pubblico

Questo video contiene informazioni sull'utilizzo delle categorie di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392?captions=ita)
