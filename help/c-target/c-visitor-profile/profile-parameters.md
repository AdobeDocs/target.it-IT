---
keywords: Profile script;profile script attributes;profile script best practices;debug;debugging;scripts;profile scripts;attributes;attribute;parameter
description: Gli attributi del profilo sono parametri specifici del visitatore. Tali attributi vengono memorizzati nel profilo del visitatore in modo da fornire informazioni che puoi usare nelle attività di Adobe Target.
title: Attributi di profilo in Adobe Target
topic: Advanced,Standard,Classic
uuid: a76ed523-32cb-46a2-a2a3-aba7f880248b
translation-type: tm+mt
source-git-commit: 6586d49118ff5a598b699dfb9f5a23ef9da4cce7

---


# Attributi del profilo{#profile-attributes}

Gli attributi del profilo sono parametri specifici di un visitatore. Tali attributi vengono memorizzati nel profilo del visitatore in modo da fornire informazioni che puoi usare nelle attività.

Quando un visitatore naviga nel tuo sito o ritorna per un’altra sessione, puoi usare gli attributi salvati nel suo profilo per presentargli specifici contenuti oppure per registrare informazioni a scopo di filtro dei segmenti.

Per impostare gli attributi del profilo, fai clic su **[!UICONTROL Tipi di pubblico]** &gt; **[!UICONTROL Script di profilo]**.

![Scheda Script di profilo](/help/c-target/c-visitor-profile/assets/profile-scripts.png)

Sono disponibili i seguenti tipi di attributi di profilo:

| Tipo di parametro | Descrizione |
|--- |--- |
| mbox | Passaggio diretto attraverso il codice della pagina quando viene creata la mbox. Consulta [Trasmettere parametri a una mbox globale](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md).<br>**Nota**: Target ha un limite di 50 attributi univoci di profilo per chiamata mbox. Se devi passare più di 50 attributi di profilo a Target, puoi farlo utilizzando il metodo API Aggiornamento profilo. Per ulteriori informazioni, vedi [Aggiornamento profilo nella documentazione API di Adobe Target](http://developers.adobetarget.com/api/#updating-profiles). |
| Script | Definito direttamente con uno snippet di codice JavaScript. Possono memorizzare i totali correnti come il denaro totale speso dal consumatore ed è eseguito dietro ogni richiesta mbox. Consulta Attributi degli script di profilo qui di seguito. |

## Attributi degli script di profilo {#concept_8C07AEAB0A144FECA8B4FEB091AED4D2}

Definizione di un attributo di script del profilo con il relativo frammento di codice JavaScript associato.

Puoi utilizzare gli script di profilo per acquisire gli attributi di un visitatore attraverso più visite. Gli script di profilo sono frammenti di codice definiti in Target mediante una forma di JavaScript lato server. Ad esempio, puoi utilizzare uno script di profilo per acquisire la frequenza con cui un visitatore visita il sito e quando è stata effettuata l’ultima visita.

Gli script di profilo sono diversi dai parametri di profilo. I parametri di profilo acquisiscono informazioni sui visitatori utilizzando l’implementazione del codice mbox di Target.

>[!NOTE]
>
>[!DNL Target] dispone di un limite di 1,000 script di profilo per account.

## Creare gli script di profilo {#section_CB02F8B97CAF407DA84F7591A7504810}

Gli script di profilo sono disponibili nella scheda [!UICONTROL Tipi di pubblico] dell’interfaccia di [!DNL Target].

Per aggiungere un nuovo script di profilo, fai clic sulla scheda **[!UICONTROL Script di profilo]**, **[!UICONTROL Crea script]**, quindi scrivi lo script.

Oppure

Per copiare uno script di profilo esistente, passa il mouse sullo script desiderato nell’elenco [!UICONTROL Script di profilo] e fai clic sull’icona **[!UICONTROL Copia]**: (assets/icon_copy.png)

Ora puoi modificare il pubblico per crearne uno simile.

![Finestra di dialogo Crea script di profilo](assets/profile-script.png)

Gli script di profilo eseguono dei “catcher” per acquisire attributi di profilo per ogni richiesta di posizione. Quando viene ricevuta una richiesta di posizione, Target determina quale attività deve essere eseguita e visualizza il contenuto appropriato per l’attività e l’esperienza, tiene traccia del successo dell’attività ed esegue eventuali script di profilo rilevanti. Questo consente di tenere traccia di informazioni sulla visita: la posizione del visitatore, l’ora del giorno, quante volte ha visitato il sito, se ha effettuato acquisti in passato e così via. Queste informazioni vengono poi aggiunte al profilo del visitatore, in modo da poter monitorare meglio la sua attività sul sito.

Gli attributi degli script di profilo hanno il tag `user.` inserito prima del nome dell’attributo. Ad esempio:

```
if (mbox.name == 'Track_Interest') { 
    if (profile.get('model') == "A5" &&; profile.get('subcat') == "KS6") { 
        return (user.get('A5KS6') || 0) + 1; 
    } 
}
```

* Fai riferimento agli attributi dello script di profilo (incluso se stesso) nel codice con `user.get('parameterName')`
* Salva le variabili che possono essere accessibili alla successiva esecuzione dello script (alla successiva richiesta mbox) con `user.setLocal('variable_name', 'value')`. Fai riferimento alla variabile con `user.getLocal('variable_name')`. Questo è utile nelle situazioni in cui vuoi fare riferimento alla data e all’ora dell’ultima richiesta.
* I parametri e i valori sono sensibili all’uso di maiuscole e minuscole. Usa le stesse maiuscole e minuscole dei parametri e dei valori che verranno ricevuti durante l’attività o il test.
* Per ulteriore sintassi JavaScript, vedi la sezione “Riferimento JavaScript per i parametri del profilo di script”, più avanti.

## Visualizzazione delle schede di informazioni sugli script di profilo {#section_18EA3B919A8E49BBB09AA9215E1E3F17}

Puoi visualizzare schede a comparsa di script di profilo simili come schede informative. Queste schede informative sullo script di profilo ti permettono di visualizzare l’elenco delle attività che si riferiscono allo script di profilo selezionato, insieme ad altri metadati utili.

Ad esempio, se si passa il cursore su uno script di profilo nell'Elenco script di profilo (Destinatari &gt; Script di profilo) e poi si fa clic sull'icona Informazioni, si accede alla seguente scheda di informazioni sullo script di profilo.

La scheda [!UICONTROL Informazioni script] contiene le seguenti informazioni: Nome, Stato, Tipo token, ID script, Sostituisci registro e Descrizione.

![Scheda di informazioni Script di profilo](assets/profile_script_info_card.png)

La scheda [!UICONTROL Utilizzo script] elenca le attività (e aree di lavoro) relative allo script di profilo selezionato.

![Scheda di informazioni Script di profilo &gt; Scheda Utilizzo script](assets/profile_script_info_card_usage_tab.png)

>[!Note]
>
>La scheda Utilizzo script non visualizza le attività che fanno riferimento allo script di profilo selezionato nelle situazioni seguenti:
> * L'attività è nello stato Bozza.
> * Il contenuto o l'offerta utilizzato/a nell'attività impiega variabili di script (o un'offerta in linea all'interno dell'attività o un'offerta nel catalogo Offerte).



## Target disabilita gli script di profilo in determinate situazioni {#section_C0FCB702E60D4576AD1174D39FBBE1A7}

[!DNL Target] disabilita automaticamente gli script di profilo in determinate situazioni, ad esempio se richiedono troppo tempo o hanno troppe istruzioni.

Quando uno script di profilo è disabilitato, viene contrassegnato da un’icona gialla di avviso nell’interfaccia utente di Target, come illustrato di seguito:

![](assets/profile_script_invalid.png)

Al passaggio del mouse puoi visualizzare dettagli sugli errori, come illustrato di seguito:

![](assets/profile_script_hover.png)

Il sistema disabilita gli script di profilo in alcune circostanze. I motivi più frequenti sono:

* Riferimento a una variabile non definita.
* Riferimento a un valore non valido. Questo fatto è spesso causato dal riferimento a valori URL e ad altri dati immessi dall’utente senza una corretta convalida.
* Troppe istruzioni JavaScript. Target ha un limite di 2.000 istruzioni JavaScript per ogni script, ma è difficile calcolarle con la semplice lettura manuale del codice JavaScript. Ad esempio, Rhino tratta tutte le chiamate di funzione e le chiamate “nuove” come 100 istruzioni. Ciò significa che qualsiasi chiamata a una funzione richiede 100 istruzioni. Inoltre, la dimensione dei dati immessi, ad esempio i valori URL, può influire sul conteggio delle istruzioni.
* Mancato rispetto delle istruzioni evidenziate nella sezione [Best practice](../../c-target/c-visitor-profile/profile-parameters.md#section_64AFE5D2B0C8408A912FC2A832B3AAE0) qui sotto.

## Best practice {#best}

Le seguenti linee guida hanno lo scopo di facilitare la scrittura di script di profilo semplificati, il più possibile privi di errori, mediante la scrittura di codice che genera un errore controllato in modo da consentire l’elaborazione degli script senza determinare un blocco di sistema. Queste linee guida sono il risultato di best practice collaudate in termini di efficienza. Applica queste linee guida unitamente ai principi e alle raccomandazioni stilati dalla community di sviluppo Rhino.

* Imposta il valore dello script corrente su una variabile locale nello script utente, imposta un failover in caso di stringa vuota.
* Convalida la variabile locale verificando che non si tratti di una stringa vuota.
* Utilizza le funzioni di manipolazione basate su stringa anziché le espressioni regolari.
* Utilizza cicli limitati “for” invece di cicli aperti “for” o “while”.
* Non superare 1.300 caratteri o 50 iterazioni di ciclo.
* Non superare 2.000 istruzioni JavaScript. Target ha un limite di 2.000 istruzioni JavaScript per ogni script, ma è difficile calcolarle con la semplice lettura manuale del codice JavaScript. Ad esempio, Rhino tratta tutte le chiamate di funzione e le chiamate “nuove” come 100 istruzioni. Inoltre, la dimensione dei dati immessi, ad esempio i valori URL, può influire sul conteggio delle istruzioni.
* Presta attenzione non solo alle prestazioni dello script, ma anche alle prestazioni combinate di tutti gli script. Come procedura ottimale, si consigliano meno di 5.000 istruzioni in totale. Contare il numero di istruzioni non è ovvio, ma è importante notare che gli script superiori ai 2 KB vengono disattivati automaticamente. Non esiste un limite al numero di script eseguibili, ma ogni script viene eseguito con ogni singola chiamata mbox. Esegui solo il numero di script necessario.
* In un’espressione regex, non è quasi mai necessario iniziare con punto-asterisco (ad esempio: `/.*match/`, `/a|.*b/`). La ricerca regex inizia da tutte le posizioni in una stringa (a meno che non sia delimitata con `^`), e punto-asterisco è quindi implicito. L’esecuzione dello script può essere interrotta se a un’espressione regex corrispondono dati di input sufficientemente lunghi (anche solo di qualche centinaia di caratteri).
* In caso di esito negativo, inserisci lo script in un try/catch.
* See the JS Rhino engine documentation for more information: [https://www.mozilla.org/rhino/doc.html](https://www.mozilla.org/rhino/doc.html).

## Script di profilo per testare attività reciprocamente esclusive {#section_FEFE50ACA6694DE7BF1893F2EFA96C01}

Puoi utilizzare gli attributi del profilo per impostare test che confrontano due o più attività ma non consentono a uno stesso visitatore di partecipare a ciascuna attività.

La verifica delle attività reciprocamente esclusive impedisce al visitatore di un’attività di influenzare i risultati del test per le altre attività. Quando un visitatore partecipa a più attività, può essere difficile determinare se l’incremento positivo o negativo deriva dall’esperienza del visitatore con una sola attività o se le interazioni tra più attività ne hanno influenzato i risultati.

Ad esempio, puoi testare due aree del tuo sistema di e-commerce. Puoi provare l’effetto di un pulsante “Aggiungi al carrello” rosso invece che blu. Oppure, potresti voler testare un nuovo processo di pagamento che prevede solo due passaggi, invece degli attuali cinque passaggi. Se entrambe le attività hanno lo stesso evento di successo (un acquisto completato), può essere difficile determinare se le conversioni sono state determinate dal pulsante rosso o dal miglioramento del processo di pagamento. Separando i test in attività reciprocamente esclusive, è possibile testare ogni modifica in modo indipendente.

Quando utilizzi uno degli script di profilo seguenti, considera quanto segue:

* Lo script di profilo deve essere eseguito prima dell’avvio dell’attività e deve rimanere invariato per tutta la durata dell’attività.
* Questa tecnica ridurrà la quantità di traffico nell’attività che potrebbe richiedere una durata di esecuzione più lunga. Tieni conto di questo fatto quando stimi la durata dell’attività.

### Impostazione di due attività

Per suddividere i visitatori in gruppi che vedono rispettivamente attività diverse devi creare un attributo di profilo. Un attributo di profilo può indirizzare un visitatore verso uno di due o più gruppi. Per impostare un attributo di profilo denominato “twogroups”, crea lo script seguente:

```
if (!user.get('twogroups')) { 
    var ran_number = Math.floor(Math.random() * 99); 
    if (ran_number <= 49) { 
        return 'GroupA'; 
    } else { 
        return 'GroupB'; 
    } 
}
```

`if (!user.get('twogroups'))` determina se l’attributo di profilo *twogroups* è impostato per il visitatore corrente. In caso affermativo, non è necessaria alcuna ulteriore azione.

`var ran_number=Math.floor(Math.random() *99)` dichiara una nuova variabile chiamata ran_number, imposta il suo valore su un decimale casuale tra 0 e 1, poi lo moltiplica per 99 e lo arrotonda verso il basso per creare un intervallo di 100 (0-99), utile per specificare una percentuale di visitatori che vedono l’attività.

`if (ran_number <= 49)` inizia una routine che determina il gruppo a cui appartiene il visitatore. Se il numero restituito è 0-49, il visitatore viene assegnato a GroupA. Se il numero è 50-99, il visitatore viene assegnato a GroupB. Il gruppo determina l’attività che verrà visualizzata dal visitatore.

Dopo aver creato l’attributo di profilo, imposta la prima attività per indirizzare la popolazione desiderata richiedendo che il parametro del profilo utente user.twogroups corrisponda al valore specificato per GroupA.

>[!NOTE]
>
>Scegli una mbox all’inizio della pagina. Questo codice determina se un visitatore sperimenta la campagna. Se il browser incontra subito una mbox, questa può essere utilizzata per impostare questo valore.

Imposta la seconda campagna in modo che il parametro `user.twogroups` del profilo utente corrisponda al valore specificato per GroupB.

### Impostazione di tre o più attività

L’impostazione di tre o più attività mutuamente esclusive è simile alla configurazione di due, ma devi modificare il JavaScript dell’attributo del profilo per creare un gruppo separato per ogni attività e determinare chi le vede. La generazione di numeri casuali è diversa a seconda che si crei un numero di gruppi pari o dispari.

Ad esempio, per creare quattro gruppi, utilizza il seguente JavaScript:

```
if (!user.get('fourgroups')) { 
    var ran_number = Math.floor​(Math.random() * 99); 
    if (ran_number <= 24) { 
        return 'GroupA'; 
    } else if (ran_number <= 49) { 
        return 'GroupB'; 
    } else if (ran_number <= 74) { 
        return 'GroupC'; 
    } else { 
        return 'GroupD'; 
    } 
}
```

In questo esempio, la matematica utilizzata per generare il numero casuale che assegna un visitatore a un gruppo è identica a quella con solo due gruppi. Si genera un decimale casuale, che viene quindi arrotondato per creare un numero intero.

Se crei un numero dispari di gruppi o un numero che non è divisore di 100, non devi arrotondare il decimale a un intero. Il mancato arrotondamento del decimale consente di specificare intervalli non interi. A tale scopo, modifica questa riga:

`var ran_number=Math.floor(Math.random()*99);`

in:

`var ran_number=Math.random()*99;`

Ad esempio, per suddividere i visitatori in tre gruppi uguali, utilizza il codice seguente:

```
if (!user.get('threegroups')) { 
    var ran_number = Math.random() * 99; 
    if (ran_number <= 32.33) { 
        return 'GroupA'; 
    } else if (ran_number <= 65.66) { 
        return 'GroupB'; 
    } else { 
        return 'GroupC'; 
    } 
}
```

## Debug degli script di profilo {#section_E9F933DE47EC4B4E9AF2463B181CE2DA}

Per eseguire il debug degli script di profilo possono essere utilizzati i seguenti metodi:

>[!NOTE]
>
>L’uso di [!DNL console.log] all’interno di uno script di profilo non genera il valore del profilo, perché gli script di profilo vengono eseguiti dal lato server.

* **Aggiungi script di profilo come token di risposta per eseguire il debug degli script di profilo:**

   In Target, fai clic su **[!UICONTROL Configurazione]**, poi su **[!UICONTROL Token di risposta]**, quindi attiva lo script di profilo su cui vuoi eseguire il debug.

   Ogni volta che carichi una pagina del sito con Target, una parte della risposta di Target conterrà il valore dello script di profilo specificato, come illustrato di seguito:

   ![](assets/debug_profile_script_1.png)

* **Utilizza lo strumento di debug mboxTrace per eseguire il debug degli script di profilo.**

   Questo metodo richiede un token di autorizzazione che può essere generato facendo clic su **[!UICONTROL Target]** &gt; **[!UICONTROL Configurazione]** &gt; **[!UICONTROL Implementazione]** &gt; **[!UICONTROL Genera token di autorizzazione]**.

   Poi aggiungi questi due parametri all'URL della tua pagina dopo il "?": `mboxTrace=window&authorization=YOURTOKEN`.

   In questo modo si ha qualche informazione in più rispetto al token di risposta, perché si ottiene un'istantanea del profilo precedente all'esecuzione e una successiva. Vengono inoltre visualizzati tutti i profili disponibili.

   ![](assets/debug_profile_script_2.png)

## Domande frequenti sugli script di profilo {#section_1389497BB6D84FC38958AE43AAA6E712}

**È possibile utilizzare script di profilo per acquisire informazioni da una pagina che si trova in un livello di dati?**

Gli script di profilo non sono in grado di leggere la pagina direttamente poiché vengono eseguiti lato server. I dati devono essere trasmessi mediante una richiesta mbox o altri [metodi per l’immissione di dati in Target](../../c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17). Una volta che i dati sono in Target, gli script di profilo possono leggerli come un parametro mbox o un parametro di profilo.

## Riferimento JavaScript per parametri del profilo di script

È necessaria una conoscenza semplice di JavaScript per utilizzare in modo efficace i parametri del profilo di script. Questa sezione serve come riferimento rapido per consentirti di utilizzare questa funzionalità in pochi minuti.

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

Crea una variabile per il giorno misurato in millisecondi. Se il nome della mbox è `orderThankyouPage`, imposta un attributo locale (invisibile) del profilo utente denominato `lastPurchaseTime` per ottenere il valore della data e dell’ora corrente. Il valore dell’ultimo orario di acquisto viene letto e, se è definito, si ottiene il tempo trascorso dall’ultimo acquisto, diviso per il numero di millisecondi in un giorno (che si traduce nel numero di giorni dall’ultimo acquisto).

**Nome:** *user.frequency*

```
var frequency = user.get('frequency') || 0;
if (mbox.name == 'orderThankyouPage') {
    return frequency + 1;
}
```

Creates a variable called `frequency`, initializing it to either the previous value or 0, if there was no previous value. Se il nome della mbox è `orderThankyouPage`, viene restituito il valore incrementale.

**Nome:** *user.monetaryValue*

```
var monetaryValue = user.get('monetaryValue') || 0;
if (mbox.name == 'orderThankyouPage') {
    return monetaryValue + parseInt(mbox.param('orderTotal'));
}
```

Crea una variabile chiamata `monetaryValue`, che cerca il valore corrente per un visitatore specificato (o impostata su 0 in assenza di un valore precedente). Se il nome della mbox è `orderThankyouPage`, viene restituito nuovo valore monetario aggiungendo il precedente e il valore del parametro `orderTotal` trasmesso alla mbox.

**** Nome: adobeQA

```
if (page.param("adobeQA"))
     return page.param("adobeQA");
else if (page.param("adobeqa"))
     return page.param("adobeqa");
else if (mbox.param("adobeQA"))
     return mbox.param("adobeQA");
```

Crea una variabile chiamata `adobeQA` per monitorare un utente per il QA [dell'](/help/c-activities/c-activity-qa/activity-qa.md)attività.


### Oggetti e metodi

I parametri del profilo di script possono fare riferimento alle proprietà e ai metodi seguenti:

| Oggetto o metodo | Dettagli |
| --- | --- |
| `page.url` | L’URL corrente. |
| `page.protocol` | Il protocollo utilizzato per la pagina (http o https). |
| page.domain | Il dominio dell’URL corrente (tutto ciò che precede la prima barra). Ad esempio, `www.acme.com` in `http://www.acme.com/categories/men_jeans?color=blu e&size=small`. |
| `page.query` | La stringa di query per la pagina corrente. Tutto ciò che segue il segno “?”. Ad esempio, `blue&size=small` in `http://www.acme.com/categories/mens_jeans?color=blue&size=small`. |
| `page.param(‘<par_name>’)` | Il valore del parametro indicato da `<par_name>`. Se l’URL corrente è la pagina di ricerca di Google e hai inserito `page.param('hl')`, riceverai “en” per l’URL `http://www.google.com/search?hl=en& q=what+is+asdf&btnG=Google+Search`. |
| `page.referrer` | Le stesse operazioni di cui sopra valgono per la pagina di provenienza e la destinazione (ad esempio referrer.url sarà l’indirizzo URL della pagina di provenienza). |
| `landing.url`, `landing.protocol`, `landing.query` e `landing.param` | Simile a quella della pagina, ma per la pagina di destinazione. |
| `mbox.name` | Il nome della mbox attiva. |
| `mbox.param(‘<par_name>’)` | Un parametro mbox in base al nome specificato nella mbox attiva. |
| `profile.get(‘<par_name>’)` | Il parametro del profilo utente creato dal client in base al nome `<par_name>`. Ad esempio, se l’utente imposta un parametro di profilo denominato “gender”, il valore può essere estratto utilizzando “profile.gender”. Restituisce il valore del “`profile.<par_name>`” impostato per il visitatore corrente; restituisce null se non è stato impostato alcun valore. Nota che `profile.get(<par_name>)` è qualificata come chiamata di funzione. |
| `user.get(‘<par_name>’)` | Restituisce il valore del “`user.<par_name>`” impostato per il visitatore corrente; restituisce null se non è stato impostato alcun valore. |
| `user.categoryAffinity` | Restituisce il nome della categoria migliore. |
| `user.categoryAffinities` | Restituisce un array con le categorie migliori. |
| `user.isFirstSession` | Restituisce true se è la prima sessione del visitatore. |
| `user.browser` | Restituisce l’agente utente nell’intestazione HTTP. Ad esempio, puoi creare una destinazione dell’espressione rivolta solo agli utenti Safari: `if (user.browser != null && user.browser.indexOf('Safari') != -1) { return true; }` |

### Operatori comuni


Tutti gli operatori JavaScript standard sono presenti e utilizzabili. Gli operatori JavaScript possono essere utilizzati su stringhe e numeri (oltre che su altri tipi di dati). Una rapida descrizione:

| Operatore | Descrizione |
| --- | --- |
| `==` | Indica uguaglianza. È vero se gli operandi da entrambe le parti sono uguali. |
| `!=` | Indica disuguaglianza. È vero se gli operandi da entrambe le parti non sono uguali. |
| `<` | Indica che la variabile a sinistra è inferiore alla variabile a destra. Restituisce false se le variabili sono uguali. |
| `>` | Indica che la variabile a sinistra è maggiore della variabile a destra. Restituisce false se le variabili sono uguali. |
| `<=` | Come `<` a meno che le variabili non siano uguali, nel qual caso la valutazione è true. |
| `>=` | Come `>` a meno che le variabili non siano uguali, nel qual caso la valutazione è true. |
| `&&` | Stabilisce una relazione logica di tipo “AND” tra le espressioni alla sua sinistra e alla sua desta: restituisce true solo quando entrambe le parti sono vere (in caso contrario restituisce false). |
| `||` | Stabilisce una relazione logica di tipo “OR” tra le espressioni alla sua sinistra e alla sua desta: restituisce true solo quando una delle parti è vera (in caso contrario restituisce false). |
| `//` | Controlla se la sorgente contiene tutti gli elementi del formato booleano di destinazione (origine Array, destinazione Array).<br>`//` estrae la sottostringa dalla destinazione (corrispondente a regexp) e la decodifica `Array/*String*/ decode(String encoding, String regexp, String target)`.<br>La funzione supporta anche l’uso di valori stringa costanti, raggruppamenti (`condition1 || condition2) && condition3` ed espressioni regolari (`/[^a-z]$/.test(landing.referring.url)`. |

## Video di formazione: Script di profilo

Questo video include informazioni sull'utilizzo e sulla creazione degli script di profilo.

* Cos’è uno script di profilo
* Differenza tra script di profilo e parametro di profilo
* Creare uno script di profilo semplice
* Utilizzare il menu Token disponibile per accedere alle opzioni disponibili
* Abilitare e disabilitare gli script di profilo

>[!VIDEO](https://video.tv.adobe.com/v/17394?captions=ita)