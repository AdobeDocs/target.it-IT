---
keywords: pagine del sito;pagine del sito target;targeting;pagina corrente;pagina corrente target;pagina precedente;pagina precedente target;pagina precedente;pagina di destinazione target;pagina di destinazione target;intestazione http
description: Scopri come eseguire il targeting dei visitatori utilizzando [!DNL Adobe Target] che si trovano in una pagina specifica del sito.
title: Posso indirizzare i visitatori in base alle pagine del sito?
feature: Audiences
exl-id: 4c770b7b-775f-4483-aced-43f18a9a68c1
source-git-commit: 1383088bb2f6be0432e6f140400d8723048c8530
workflow-type: tm+mt
source-wordcount: '891'
ht-degree: 22%

---

# Pagine del sito

Puoi eseguire il targeting dei visitatori utilizzando [!DNL Adobe Target] che accedono a una pagina specifica del sito.

1. Nell’interfaccia di [!DNL Target] fai clic su **[!UICONTROL Pubblico]** > **[!UICONTROL Crea pubblico]**.
1. Assegna un nome al pubblico e aggiungi una descrizione facoltativa.
1. Trascina **[!UICONTROL Pagine del sito]** nel riquadro audience builder.

   ![Pubblico per pagine del sito](assets/target_site_pages.png)

1. Fai clic su **[!UICONTROL Seleziona]** , seleziona una delle seguenti opzioni, quindi configura la regola come desiderato.

   Le opzioni e i valutatori disponibili nei successivi elenchi a discesa nella regola variano a seconda dell’opzione scelta. Nella figura seguente sono illustrate le opzioni disponibili se si sceglie [!UICONTROL Pagina corrente]:

   ![Pagina corrente](assets/current-page.png)

   Le seguenti opzioni sono disponibili nell’elenco a discesa iniziale quando scegli [!UICONTROL Seleziona].

   * **[!UICONTROL Pagina corrente]:** Pagina visualizzata dall&#39;utente.

      Se si sceglie questa opzione, nel secondo elenco a discesa sono disponibili le seguenti opzioni:

      * [!UICONTROL URL] (Per ulteriori informazioni su come [!DNL Target] valuta gli URL, vedi [Domande frequenti su destinazioni e pubblico](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * [!UICONTROL Dominio]
      * [!UICONTROL Query]
      * [!UICONTROL Sottodominio]
      * [!UICONTROL Dominio di primo livello]
      * [!UICONTROL Percorso]
      * [!UICONTROL Frammento hash (#)]
   * **[!UICONTROL Pagina precedente]:** La pagina che l’utente ha visualizzato prima di fare clic su per passare alla pagina corrente. Per tenere traccia della pagina, l’utente deve fare clic sulla pagina precedente per passare alla pagina corrente. La pagina precedente non viene tracciata se l’utente digita un nuovo URL nel browser. Il contenuto effettivo di questa pagina dipende dalla progettazione del sito. Ad esempio, se nella pagina corrente sono visualizzate informazioni su un prodotto specifico, la pagina precedente potrebbe essere una pagina categoria in cui il visitatore seleziona l’elemento specifico. Ad esempio, una pagina che mostra diverse fotocamere di un certo tipo, oppure potrebbe essere la home page che porta alla pagina finale.

      Se si sceglie questa opzione, nel secondo elenco a discesa sono disponibili le seguenti opzioni:

      * [!UICONTROL URL] Per ulteriori informazioni sulla valutazione degli URL da parte di Target, consulta [Domande frequenti su destinazioni e pubblico](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * [!UICONTROL Dominio]
      * [!UICONTROL Query]
      * [!UICONTROL Sottodominio]
      * [!UICONTROL Dominio di primo livello]
      * [!UICONTROL Percorso]
   * **[!UICONTROL Pagina di destinazione]:** La pagina di destinazione è la prima pagina che il visitatore vede quando accede al tuo sito. Ad esempio, se il visitatore fa clic su un collegamento su Google che porta a una pagina di categoria, la pagina di categoria è la pagina di destinazione. Se il collegamento rimanda alla pagina principale, quest’ultima corrisponde alla pagina di destinazione. La pagina di destinazione viene memorizzata per la sessione del visitatore. Puoi eseguire un targeting più approfondito nel sito in base alla pagina di destinazione del visitatore nella sessione.

      Se si sceglie questa opzione, nel secondo elenco a discesa sono disponibili le seguenti opzioni:

      * [!UICONTROL URL] Per ulteriori informazioni sulla valutazione degli URL da parte di Target, consulta [Domande frequenti su destinazioni e pubblico](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * [!UICONTROL Dominio]
      * [!UICONTROL Query]
      * [!UICONTROL Sottodominio]
      * [!UICONTROL Dominio di primo livello]
      * [!UICONTROL Percorso]
      * [!UICONTROL Frammento hash (#)]

      >[!NOTE]
      >
      >L’oggetto `landing.url` viene reimpostato in caso di modifica del sottodominio o di sostituzione diretta dell’URL.

   * **[!UICONTROL Intestazione HTTP]:** Questa opzione valuta le informazioni nell’intestazione HTTP del [!DNL Target] richiesta. Ad esempio, se l’intestazione HTTP contiene informazioni sulla lingua, puoi creare una regola che contiene `Accept-Language: es` per eseguire il targeting dei visitatori che accedono alla pagina in spagnolo.

      Se si sceglie questa opzione, nel secondo elenco a discesa sono disponibili le seguenti opzioni:

      * [!UICONTROL Accetta]
      * [!UICONTROL Accept-Charset]
      * [!UICONTROL Accept-Encoding]
      * [!UICONTROL Accept-Language]
      * [!UICONTROL Autorizzazione]
      * [!UICONTROL Cache-Control]
      * [!UICONTROL Connessione]
      * [!UICONTROL Content-Length]
      * [!UICONTROL Content-MDS]
      * [!UICONTROL Tipo di contenuto]
      * [!UICONTROL Date]
      * [!UICONTROL Expect]
      * [!UICONTROL Da]
      * [!UICONTROL Host]
      * [!UICONTROL Se corrisponde]
      * [!UICONTROL If-Modified-Since]
      * [!UICONTROL If-None-Match]
      * [!UICONTROL If-Range]
      * [!UICONTROL If-Unmodified-Since]
      * [!UICONTROL Max-Forwards]
      * [!UICONTROL Pragma]
      * [!UICONTROL Proxy-Authorization]
      * [!UICONTROL Intervallo]
      * [!UICONTROL Referrer]
      * [!UICONTROL TE]
      * [!UICONTROL Aggiorna]
      * [!UICONTROL User-Agent]
      * [!UICONTROL Via]
      * [!UICONTROL Attenzione]

   Se si sceglie [!UICONTROL Pagina corrente], [!UICONTROL Pagina precedente], o [!UICONTROL Pagina di destinazione], il [!UICONTROL Dominio] e [!UICONTROL Query] sono disponibili delle opzioni. Quando si selezionano queste opzioni, tenere presente quanto segue:

   * **Dominio:** il dominio completo della pagina. Nella specificazione di un dominio, è consigliabile utilizzare “contiene”, Ad esempio, &quot;Dominio è uguale a facebook.com&quot; non accetta `m.facebook.com` o `www.facebook.com`. &quot;Il dominio contiene facebook.com&quot; accetta qualsiasi variante di facebook.com.
   * **Query:** il contenuto dell’URL dopo il primo punto interrogativo (?).

      `foo.html?e0a72cb2a2c7`





1. (Facoltativo) Imposta regole aggiuntive per il pubblico.
1. Fai clic su **[!UICONTROL Fine]**.

Puoi anche creare un pubblico per le pagine del sito utilizzando un “parametro di query definito dall’utente” o una “intestazione definita dall’utente”.

Utilizza:

* Parametro di query se la regola selezionata dall&#39;utente è [!UICONTROL Pagina corrente], [!UICONTROL Pagina di destinazione], o [!UICONTROL Pagina precedente]
* Intestazione se la regola selezionata dall’utente è un’intestazione HTTP

## Risoluzione dei problemi relativi al {#ts}

* Affinché i tipi di pubblico delle pagine di destinazione funzionino correttamente, le richieste devono avere `mboxReferrer` set di parametri (per l’API di consegna il `context.address.referringUrl` che la libreria JavaScript at.js prende dalla pagina utilizzando il `document.referrer` attributo. Questo `HTMLDocument` attribute restituisce l’URI della pagina da cui l’utente si è spostato. Il valore di questo attributo è una stringa vuota quando l’utente passa direttamente alla pagina (non tramite un collegamento, ma, ad esempio, tramite un segnalibro).

   Se questo comportamento non soddisfa le tue esigenze, prendi in considerazione l’esecuzione di una delle seguenti azioni:

   * Superato [Parametri mbox](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/global-mbox/pass-parameters-to-global-mbox.html?lang=it){target=_blank} a [!DNL Target] da utilizzare a scopo di targeting.
   * Utilizza un [Attività test A/B](/help/main/c-activities/t-test-ab/test-ab.md) invece di un’attività di pagina di destinazione. Le attività di test A/B non cambiano le esperienze per lo stesso visitatore.
   * Utilizza un [profilo visitatore](/help/main/c-target/c-audiences/c-target-rules/visitor-profile.md) invece.

* Quando si utilizzano i valutatori &quot;starts/ends with&quot; sulle stringhe contenenti virgole, queste stringhe vengono valutate come una matrice di valori, in cui viene valutato ogni valore separato da virgole. Ad esempio, se disponi del valore per un’intestazione: `Accept-Language: en,zh;q=0.9,en-IN;q=0.8,zh-CN;q=0.7` è idoneo per condizioni quali:
   * inizia con zh,
   * inizia con en,
   * termina con 0,7,
   * termina con 0,8.

## Video di formazione: Creazione di tipi di pubblico

Questo video contiene informazioni sull&#39;utilizzo delle categorie di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392)
