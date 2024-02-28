---
keywords: script di profilo;attributi degli script di profilo;best practice per gli script di profilo;debug;eseguire il debug;script;script di profilo;attributi;attributo;parametro
description: Scopri gli attributi specifici del visitatore che vengono memorizzati nel suo profilo in modo da fornire informazioni che puoi usare nelle attività di Adobe [!DNL Target] .
title: Cosa sono gli attributi del profilo?
feature: Audiences
exl-id: 6c689629-bbd3-461e-9a68-5b16d4eb4250
source-git-commit: 356b04745b58670b4bf39be929e785b8490d78ff
workflow-type: ht
source-wordcount: '2465'
ht-degree: 100%

---

# Attributi del profilo

Gli attributi del profilo in [!DNL Adobe Target] sono parametri specifici di un visitatore. Tali attributi vengono memorizzati nel profilo del visitatore in modo da fornire informazioni che puoi usare nelle attività.

Un profilo utente contiene informazioni demografiche e comportamentali relative a un visitatore di una pagina web. Queste informazioni possono includere età, genere, prodotti acquistati, ultima visita e così via. [!DNL Target] utilizza queste informazioni per personalizzare il contenuto che fornisce al visitatore.

Quando un visitatore naviga nel tuo sito web o ritorna per un’altra sessione, puoi usare gli attributi del profilo salvati per presentargli contenuti specifici oppure per registrare informazioni per filtrare i segmenti.

Configurazione degli attributi del profilo:

1. Fai clic su **[!UICONTROL Tipi di pubblico]** > **[!UICONTROL Script di profilo.]**

   ![Scheda Script di profilo](/help/main/c-target/c-visitor-profile/assets/create-script.png)

1. Fai clic su **[!UICONTROL Crea script]**.

   ![Finestra di dialogo Crea script profilo](/help/main/c-target/c-visitor-profile/assets/profile-script.png)

   Sono disponibili i seguenti tipi di attributi di profilo:

   | Tipo di parametro | Descrizione |
   |--- |--- |
   | mbox | Passaggio diretto attraverso il codice della pagina quando viene creata la mbox. Consulta [Trasmettere i parametri a una mbox globale](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/global-mbox/pass-parameters-to-global-mbox.html?lang=it){target=_blank} nella *Guida per gli sviluppatori di Target*.<P>**Nota**: [!DNL Target] ha un limite di 50 attributi di profilo univoci per chiamata mbox. Se devi trasmettere più di 50 attributi di profilo a [!DNL Target], utilizza il metodo [!UICONTROL API Aggiornamento profilo]. Per ulteriori informazioni, consulta [Aggiornare profili](https://experienceleague.adobe.com/docs/target-dev/developer/api/profile-apis/profile-api-overview.html?lang=it){target=_blank} nella *Guida per gli sviluppatori di Target*. |
   | Profilo | Definito direttamente con uno snippet di codice JavaScript. Questi snippet possono memorizzare i totali correnti come il denaro totale speso dal consumatore e sono eseguiti dietro ogni richiesta mbox. Consulta *Attributi degli script di profilo* qui di seguito. |

## Attributi degli script di profilo {#concept_8C07AEAB0A144FECA8B4FEB091AED4D2}

Definizione di un attributo di script del profilo con il relativo frammento di codice JavaScript associato.

Puoi utilizzare gli script di profilo per acquisire gli attributi di un visitatore attraverso più visite. Gli script di profilo sono snippet di codice definiti in [!DNL Target] mediante una forma di JavaScript lato server. Ad esempio, puoi utilizzare uno script di profilo per acquisire la frequenza con cui un visitatore visita il sito e quando è stata effettuata l’ultima visita.

Gli script di profilo sono diversi dai parametri di profilo. I parametri di profilo acquisiscono informazioni sui visitatori utilizzando l’implementazione del codice mbox di [!DNL Target].

## Creazione di script di profilo {#section_CB02F8B97CAF407DA84F7591A7504810}

Gli script di profilo sono disponibili nella scheda [!UICONTROL Tipi di pubblico] dell’interfaccia di [!DNL Target].

Per aggiungere uno script di profilo, fai clic sulla scheda **[!UICONTROL Script di profilo]**, **[!UICONTROL Crea script]**, quindi scrivi lo script.

Oppure

Per copiare uno script di profilo esistente, dall’elenco [!UICONTROL Script di profilo] fai clic sull&#39;icona dei puntini di sospensione dello script desiderato, quindi fai clic su **[!UICONTROL Duplica]**.

Ora puoi modificare il pubblico per crearne uno simile.

Gli script di profilo eseguono dei “catcher” per acquisire attributi di profilo per ogni richiesta di posizione. Quando viene ricevuta una richiesta di posizione, [!DNL Target] determina l’attività da eseguire e visualizza il contenuto appropriato per l’attività e l’esperienza. [!DNL Target] tiene inoltre traccia del successo dell’attività ed esegue eventuali script di profilo pertinenti. Questo processo ti consente di tenere traccia di informazioni sulla visita: la posizione del visitatore, l’ora del giorno, quante volte ha visitato il sito, se ha effettuato acquisti in passato e così via. Queste informazioni vengono poi aggiunte al profilo del visitatore, in modo da poter monitorare meglio la sua attività sul sito.

Gli attributi degli script di profilo hanno il tag `user.` inserito prima del nome dell’attributo. Ad esempio:

```
if (mbox.name == 'Track_Interest') { 
    if (profile.get('model') == "A5" &&; profile.get('subcat') == "KS6") { 
        return (user.get('A5KS6') || 0) + 1; 
    } 
}
```

Considera le seguenti informazioni:

* Fai riferimento agli attributi dello script di profilo (incluso se stesso) nel codice con `user.get('parameterName')`.
* Salva le variabili che possono essere accessibili alla successiva esecuzione dello script (alla successiva richiesta mbox) con `user.setLocal('variable_name', 'value')`. Fai riferimento alla variabile con `user.getLocal('variable_name')`. Questo processo è utile nelle situazioni in cui vuoi fare riferimento alla data e all’ora dell’ultima richiesta.

  Questi valori persistono come uno script di profilo, ma puoi accedervi solo all’interno dello script in cui sono stati impostati.

* I parametri e i valori fanno distinzione tra maiuscole e minuscole. Usa le stesse maiuscole e minuscole dei parametri e dei valori che ricevi durante l’attività o il test.
* Per ulteriore sintassi JavaScript, consulta la sezione “Riferimento JavaScript per i parametri del profilo di script” qui di seguito.
* Il parametro rimane nel profilo dopo aver disabilitato lo script. Gli utenti i cui profili contengono già un parametro utilizzato nel pubblico di un’attività si qualificano in tale attività.
* Gli script di profilo non possono essere eliminati mentre sono utilizzati in un’attività.
* La creazione di script di profilo dipendenti che utilizzano il risultato di uno script di profilo in un altro script di profilo non è consigliata. L’ordine di esecuzione dello script di profilo non è garantito.

## Visualizzazione delle schede di informazioni sugli script di profilo {#section_18EA3B919A8E49BBB09AA9215E1E3F17}

Puoi visualizzare schede a comparsa di script di profilo simili come schede informative. Queste schede informative sullo script di profilo ti permettono di visualizzare l’elenco delle attività che si riferiscono allo script di profilo selezionato, insieme ad altri metadati utili.

Ad esempio, per accedere alla scheda di informazioni sullo script di profilo seguente fai clic sull’icona [!UICONTROL Informazioni] dello script di profilo desiderato dall’elenco ([!UICONTROL Tipi di pubblico] > [!UICONTROL Script di profilo]).

La scheda [!UICONTROL Info script] contiene le seguenti informazioni: nome, descrizione e codice script.

![Scheda di informazioni Script di profilo](assets/profile_script_info_card.png)

Fai clic su **[!UICONTROL Visualizza dettagli completi]** per visualizzare i tipi di pubblico e le attività che si riferiscono allo script di profilo selezionato.

![Scheda di informazioni Script di profilo > scheda Utilizzo script](assets/profile_script_info_card_usage_tab.png)

>[!NOTE]
>
>La scheda [!UICONTROL Utilizzo script] non mostra le attività che fanno riferimento allo script di profilo selezionato nelle situazioni seguenti:
>
> * L’attività è nello stato [!UICONTROL Bozza].
> * Il contenuto o l’offerta utilizzati nell&#39;attività impiegano variabili di script (un’offerta in linea all’interno dell’attività o un’offerta nella libreria Offerte).

## Target disabilita gli script di profilo in determinate situazioni {#section_C0FCB702E60D4576AD1174D39FBBE1A7}

[!DNL Target] disabilita automaticamente gli script di profilo in determinate situazioni, ad esempio se richiedono troppo tempo o hanno troppe istruzioni.

Quando uno script di profilo è disabilitato, viene contrassegnato da un’icona gialla di avviso nell’interfaccia utente di Target, come illustrato di seguito:

![immagine profile_script _invalid](assets/profile_script_invalid.png)

Al passaggio del mouse puoi visualizzare dettagli sugli errori, come illustrato di seguito:

![immagine profile_script_hover](assets/profile_script_hover.png)

Il sistema disabilita gli script di profilo in alcune circostanze. I motivi più frequenti sono:

* Riferimento a una variabile non definita.
* Riferimento a un valore non valido. Questo errore è spesso causato dal riferimento a valori URL e ad altri dati immessi dall’utente senza una corretta convalida.
* Troppe istruzioni JavaScript utilizzate. [!DNL Target] ha un limite di 2.000 istruzioni JavaScript per ogni script, ma è difficile calcolare questo limite con la semplice lettura manuale del codice JavaScript. Ad esempio, Rhino tratta tutte le chiamate di funzione e le chiamate “nuove” come 100 istruzioni. Qualsiasi chiamata a qualsiasi funzione richiede 100 istruzioni. Inoltre, la dimensione dei dati immessi, ad esempio i valori URL, può influire sul conteggio delle istruzioni.
* Mancato rispetto delle istruzioni evidenziate nella sezione [Best practice](/help/main/c-target/c-visitor-profile/profile-parameters.md#section_64AFE5D2B0C8408A912FC2A832B3AAE0) qui sotto.

## Best practice {#best}

Le seguenti linee guida hanno lo scopo di facilitare la scrittura di script di profilo semplificati, il più possibile privi di errori, mediante la scrittura di codice che genera un errore controllato in modo da consentire l’elaborazione degli script senza determinare un blocco di sistema. Queste linee guida sono il risultato di best practice collaudate in termini di efficienza. Applica queste linee guida unitamente ai principi e alle raccomandazioni stilati dalla community di sviluppo Rhino.

* Imposta il valore dello script corrente su una variabile locale nello script utente, imposta un failover in caso di stringa vuota.
* Convalida la variabile locale verificando che non si tratti di una stringa vuota.
* Utilizza le funzioni di manipolazione basate su stringa anziché le espressioni regolari.
* Utilizza cicli limitati “for” invece di cicli aperti “for” o “while”.
* Non superare 1.300 caratteri o 50 iterazioni di ciclo.
* Non superare 2.000 istruzioni JavaScript. [!DNL Target] ha un limite di 2.000 istruzioni JavaScript per ogni script, ma è difficile calcolare questo limite con la semplice lettura manuale del codice JavaScript. Ad esempio, Rhino tratta tutte le chiamate di funzione e le chiamate “nuove” come 100 istruzioni. Inoltre, la dimensione dei dati immessi, ad esempio i valori URL, può influire sul conteggio delle istruzioni.
* Presta attenzione non solo alle prestazioni dello script, ma anche alle prestazioni combinate di tutti gli script. Come best practice, [!DNL Adobe] consiglia meno di 5.000 istruzioni in totale. Contare il numero di istruzioni non è scontato, ma è importante notare che gli script con più di 2.000 istruzioni vengono disattivati automaticamente. Il numero di script di profilo attivi non deve superare 300. Ogni script viene eseguito con ogni singola chiamata mbox. Esegui solo il numero di script necessario.
* In un’espressione regex, non è quasi mai necessario iniziare con punto-asterisco (ad esempio: `/.*match/`, `/a|.*b/`). La ricerca regex inizia da tutte le posizioni in una stringa (a meno che non sia delimitata con `^`), e punto-asterisco è quindi implicito. L’esecuzione dello script può essere interrotta se a un’espressione regex corrispondono dati di input sufficientemente lunghi (anche solo di qualche centinaia di caratteri).
* In caso di esito negativo, inserisci lo script in un try/catch.
* I consigli seguenti possono aiutarti a limitare la complessità degli script di profilo. Gli script di profilo possono eseguire un numero limitato di istruzioni.

  Best practice:

   * Mantieni gli script di profilo piccoli e il più semplici possibile.
   * Evita espressioni regolari o utilizza solo espressioni regolari semplici. Anche le espressioni semplici possono richiedere molte istruzioni per la valutazione.
   * Evita la ricorsione.
   * Gli script di profilo devono essere testati in termini di prestazioni prima di essere aggiunti a [!DNL Target]. Tutti gli script di profilo vengono eseguiti dietro ogni richiesta mbox. Se gli script di profilo non vengono eseguiti correttamente, l’esecuzione delle richieste mbox richiede più tempo, il che può influire sul traffico e sulla conversione.
   * Se gli script di profilo diventano troppo complessi, puoi utilizzare al loro posto i [token di risposta](/help/main/administrating-target/response-tokens.md).

* Per ulteriori informazioni, consulta la documentazione sul motore JS Rhino.

## Debug degli script di profilo {#section_E9F933DE47EC4B4E9AF2463B181CE2DA}

Per eseguire il debug degli script di profilo possono essere utilizzati i seguenti metodi:

>[!NOTE]
>
>L’uso di [!DNL console.log] all’interno di uno script di profilo non genera il valore del profilo, perché gli script di profilo vengono eseguiti dal lato server.

* **Aggiungi script di profilo come token di risposta per eseguire il debug degli script di profilo:**

  In [!DNL Target], fai clic su **[!UICONTROL Amministrazione]**, poi su **[!UICONTROL Token di risposta]**, quindi attiva lo script di profilo su cui vuoi eseguire il debug.

  Ogni volta che carichi una pagina del sito con [!DNL Target], una parte della risposta di [!DNL Target] contiene il valore dello script di profilo specificato, come illustrato di seguito:

  ![immagine debug_profile_script_1](assets/debug_profile_script_1.png)

* **Utilizza lo strumento di debug mboxTrace per eseguire il debug degli script di profilo.**

  Questo metodo richiede un token di autorizzazione che può essere generato facendo clic su **[!UICONTROL Target]** > **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]** > **[!UICONTROL Genera token di autorizzazione]** nella sezione [!UICONTROL Strumenti di debug].

  Quindi aggiungi questi due parametri all’URL della tua pagina dopo il “?”: `mboxTrace=window&authorization=YOURTOKEN`.

  L’aggiunta di questi parametri fornisce qualche informazione in più rispetto al token di risposta, perché si ottiene un’istantanea del profilo precedente all&#39;esecuzione e una successiva. Vengono inoltre visualizzati tutti i profili disponibili.

  ![immagine debug_profile_script_2](assets/debug_profile_script_2.png)

## Domande frequenti sugli script di profilo {#section_1389497BB6D84FC38958AE43AAA6E712}

**È possibile utilizzare script di profilo per acquisire informazioni da una pagina che si trova in un livello di dati?**

Gli script di profilo non sono in grado di leggere la pagina direttamente poiché vengono eseguiti lato server. I dati devono essere trasmessi tramite una richiesta mbox o tramite altri [metodi per immettere i dati in Target](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=it){target=_blank}. Una volta che i dati sono in [!DNL Target], gli script di profilo possono leggerli come un parametro mbox o un parametro di profilo.

## Riferimento JavaScript per i parametri del profilo di script

È necessaria una conoscenza base di JavaScript per utilizzare in modo efficace i parametri del profilo di script. Questa sezione serve come riferimento rapido per consentirti di utilizzare questa funzionalità in pochi minuti.

I parametri del profilo di script si trovano nella scheda mbox/profiles. È possibile scrivere programmi JavaScript che restituiscono qualsiasi tipo di valore JavaScript (stringa, numero intero, array e così via).

### Esempi di parametri di profilo di script {#examples}

**Nome:** *user.recency*

```
var dayInMillis = 3600 * 24 * 1000;
if (mbox.name == 'orderThankyouPage') {
    user.setLocal('lastPurchaseTime', new Date().getTime());
}
var lastPurchaseTime = user.getLocal('lastPurchaseTime');
if (lastPurchaseTime) {
    return ((new Date()).getTime() - lastPurchaseTime) / dayInMillis;
}
```

Crea una variabile per il giorno misurato in millisecondi. Se il nome della mbox è `orderThankyouPage`, imposta un attributo locale (invisibile) del profilo utente denominato `lastPurchaseTime` per mostrare il valore della data e dell’ora corrente. Il valore dell’ultimo orario di acquisto viene letto e, se è definito, [!DNL Target] restituisce il tempo trascorso dall’ultimo acquisto, diviso per il numero di millisecondi in un giorno (che si traduce nel numero di giorni dall’ultimo acquisto).

**Nome:** *user.frequency*

```
var frequency = user.get('frequency') || 0;
if (mbox.name == 'orderThankyouPage') {
    return frequency + 1;
}
```

Crea una variabile denominata `frequency`, inizializzandola al valore precedente oppure a 0, in assenza di un valore precedente. Se il nome della mbox è `orderThankyouPage`, viene restituito il valore incrementale.

**Nome:** *user.monetaryValue*

```
var monetaryValue = user.get('monetaryValue') || 0;
if (mbox.name == 'orderThankyouPage') {
    return monetaryValue + parseInt(mbox.param('orderTotal'));
}
```

Crea una variabile chiamata `monetaryValue`, che cerca il valore corrente per un visitatore specificato (o impostata su 0 in assenza di un valore precedente). Se il nome della mbox è `orderThankyouPage`, viene restituito nuovo valore monetario aggiungendo il precedente e il valore del parametro `orderTotal` trasmesso alla mbox.

**Nome:** adobeQA

```
if (page.param("adobeQA"))
     return page.param("adobeQA");
else if (page.param("adobeqa"))
     return page.param("adobeqa");
else if (mbox.param("adobeQA"))
     return mbox.param("adobeQA");
```

Crea una variabile denominata `adobeQA` per monitorare un utente per il [Controllo di qualità attività](/help/main/c-activities/c-activity-qa/activity-qa.md).

### Oggetti e metodi {#objects}

I parametri del profilo di script possono fare riferimento agli oggetti e ai metodi seguenti:

| Oggetto o metodo | Dettagli |
| --- | --- |
| `page.url` | L’URL corrente. |
| `page.protocol` | Il protocollo utilizzato per la pagina (http o https). |
| `page.domain` | Il dominio dell’URL corrente (tutto ciò che precede la prima barra). Ad esempio, `www.acme.com` in `http://www.acme.com/categories/men_jeans?color=blue&size=small`. |
| `page.query` | La stringa di query per la pagina corrente. Tutto ciò che segue il segno “?”. Ad esempio, `blue&size=small` in `http://www.acme.com/categories/mens_jeans?color=blue&size=small`. |
| `page.param('<par_name>')` | Il valore del parametro indicato da `<par_name>`. Se l’URL corrente è la pagina di ricerca di Google e hai inserito `page.param('hl')`, riceverai “en” per l’URL `http://www.google.com/search?hl=en& q=what+is+asdf&btnG=Google+Search`. |
| `page.referrer` | Le stesse operazioni di cui sopra valgono per la pagina di provenienza e quella di destinazione (ad esempio referrer.url è l’indirizzo URL della pagina di provenienza). |
| `landing.url`, `landing.protocol`, `landing.query` e `landing.param` | Simile a quella della pagina, ma per la pagina di destinazione.<P>Affinché l’URL della pagina di destinazione funzioni come previsto, imposta la variabile `context` > `browser` > `host`. |
| `mbox.name` | Il nome della mbox attiva. |
| `mbox.param('<par_name>')` | Un parametro mbox in base al nome specificato nella mbox attiva. |
| `profile.get('<par_name>')` | Il parametro del profilo utente creato dal client in base al nome `<par_name>`. Ad esempio, se l’utente imposta un parametro di profilo denominato “gender”, il valore può essere estratto utilizzando &quot;profile.gender&quot;. Restituisce il valore del “`profile.<par_name>`” impostato per il visitatore corrente; restituisce null se non è stato impostato alcun valore. Tieni presente che `profile.get(<par_name>)` è qualificato come chiamata di funzione. |
| `user.get('<par_name>')` | Restituisce il valore del “`user.<par_name>`” impostato per il visitatore corrente; restituisce null se non è stato impostato alcun valore. |
| `user.categoryAffinity` | Restituisce il nome della categoria migliore. |
| `user.categoryAffinities` | Restituisce un array con le categorie migliori. |
| `user.isFirstSession` | Restituisce true se è la prima sessione del visitatore. |
| `user.browser` | Restituisce l’agente utente nell’intestazione HTTP. Ad esempio, puoi creare una destinazione dell’espressione rivolta solo agli utenti Safari: `if (user.browser != null && user.browser.indexOf('Safari') != -1) { return true; }` |

### Operatori comuni

Tutti gli operatori JavaScript standard sono presenti e utilizzabili. Gli operatori JavaScript possono essere utilizzati su stringhe e numeri (e su altri tipi di dati). Una rapida descrizione:

| Operatore | Descrizione |
| --- | --- |
| `==` | Indica uguaglianza. È vero se gli operandi da entrambe le parti sono uguali. |
| `!=` | Indica disuguaglianza. È vero se gli operandi da entrambe le parti non sono uguali. |
| `<` | Indica che la variabile a sinistra è inferiore alla variabile a destra. Restituisce false se le variabili sono uguali. |
| `>` | Indica che la variabile a sinistra è maggiore della variabile a destra. Restituisce false se le variabili sono uguali. |
| `<=` | Come `<` a meno che le variabili non siano uguali, nel qual caso restituisce true. |
| `>=` | Come `>` a meno che le variabili non siano uguali, nel qual caso restituisce true. |
| `&&` | Stabilisce una relazione logica di tipo “AND” tra le espressioni alla sua sinistra e alla sua desta: restituisce true solo quando entrambe le parti sono vere (in caso contrario restituisce false). |
| `||` | Stabilisce una relazione logica di tipo “OR” tra le espressioni alla sua sinistra e alla sua desta: restituisce true solo quando una delle parti è true (in caso contrario restituisce false). |
| `//` | Controlla se la sorgente contiene tutti gli elementi del formato booleano di destinazione (origine Array, destinazione Array).<br>`//` estrae la sottostringa dalla destinazione (corrispondente a regexp) e la decodifica `Array/*String*/ decode(String encoding, String regexp, String target)`.<br>La funzione supporta anche l’uso di valori stringa costanti, raggruppamenti (`condition1 || condition2) && condition3` ed espressioni regolari `/[^a-z]$/.test(landing.referring.url)`). |

## Video di formazione: script di profilo ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video include informazioni sull’utilizzo e sulla creazione degli script di profilo.

* Cos’è uno script di profilo
* Differenza tra script di profilo e parametro di profilo
* Creare uno script di profilo semplice
* Utilizzare il menu Token disponibile per accedere alle opzioni disponibili
* Abilitare e disabilitare gli script di profilo

>[!VIDEO](https://video.tv.adobe.com/v/17394)
