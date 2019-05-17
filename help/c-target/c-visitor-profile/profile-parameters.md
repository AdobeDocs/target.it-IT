---
description: Gli attributi del profilo sono parametri specifici del visitatore. Il profilo del visitatore memorizza questi attributi fornendo così informazioni su di lui che puoi usare nelle tue campagne.
keywords: script di profilo;attributi degli script di profilo;procedure consigliate per gli script di profilo;debug;debugging
seo-description: Gli attributi del profilo sono parametri specifici del visitatore. Il profilo del visitatore memorizza questi attributi fornendo così informazioni su di lui che puoi usare nelle tue campagne.
seo-title: Attributi del profilo
solution: Target
title: Attributi del profilo
topic: Advanced,Standard,Classic
uuid: a76ed523-32cb-46a2-a2a3-aba7f880248b
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Attributi del profilo{#profile-attributes}

Gli attributi del profilo sono parametri specifici del visitatore. Il profilo del visitatore memorizza questi attributi fornendo così informazioni su di lui che puoi usare nelle tue campagne.

## Attributi del profilo {#concept_01A30B4762D64CD5946B3AA38DC8A201}

Gli attributi del profilo sono parametri specifici del visitatore. Il profilo del visitatore memorizza questi attributi fornendo così informazioni su di lui che puoi usare nelle tue campagne.

Quando il visitatore naviga o ritorna per un&#39;altra sessione, puoi indirizzare il contenuto o registrare le informazioni per il filtro dei segmenti tramite gli attributi del profilo salvati.

Per impostare gli attributi del profilo, fai clic su **[!UICONTROL Pubblico]** &gt; **[!UICONTROL Script di profilo]**.

Sono disponibili i seguenti tipi di attributi di profilo:

| Tipo di parametro | Descrizione |
|--- |--- |
| Mbox | Passaggio diretto attraverso il codice della pagina quando viene creata la mbox. Consulta [Trasmettere parametri a una mbox globale](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md).<br>Nota: Target ha un limite di 50 attributi univoci di profilo per chiamata mbox. Se devi passare più di 50 attributi di profilo a Target, puoi farlo utilizzando il metodo API Aggiornamento profilo. Per ulteriori informazioni, vedi [Aggiornamento profilo nella documentazione API di Adobe Target](http://developers.adobetarget.com/api/#updating-profiles). |
| Script | Definito direttamente con uno snippet di codice JavaScript. Possono memorizzare i totali correnti come il denaro totale speso dal consumatore ed è eseguito dietro ogni richiesta mbox. Consulta Attributi degli script di profilo qui di seguito. |

## Attributi degli script di profilo {#concept_8C07AEAB0A144FECA8B4FEB091AED4D2}

Definizione di un attributo di script del profilo con il relativo frammento di codice JavaScript associato.

Puoi utilizzare gli script di profilo per acquisire gli attributi di un visitatore attraverso più visite. Gli script di profilo sono frammenti di codice definiti in Target mediante una forma di JavaScript lato server. Ad esempio, puoi utilizzare uno script di profilo per acquisire la frequenza con cui un visitatore visita il sito e quando è stata effettuata l’ultima visita.

Gli script di profilo sono diversi dai parametri di profilo. I parametri di profilo acquisiscono informazioni sui visitatori utilizzando l’implementazione del codice mbox di Target.

>[!NOTE]
>
>[!DNL Target] dispone di un limite di 1,000 script di profilo per account.

## Creare script di profilo {#section_CB02F8B97CAF407DA84F7591A7504810}

Gli script di profilo sono disponibili nella scheda [!UICONTROL Tipi di pubblico] dell’interfaccia di [!DNL Target].

Per aggiungere un nuovo script di profilo, fai clic sulla scheda **[!UICONTROL Script di profilo]**, **[!UICONTROL Crea script]**, quindi scrivi lo script.

Oppure

Per copiare uno script di profilo esistente, passa il mouse sullo script desiderato nell’elenco [!UICONTROL Script di profilo] e fai clic sull’icona **[!UICONTROL Copia]**: (assets/icon_copy.png)

Ora puoi modificare il pubblico per crearne uno simile.

![](assets/profile-script.png)

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
* I parametri e i valori sono sensibili all’uso di maiuscole e minuscole. Usa le stesse maiuscole e minuscole dei parametri e dei valori che verranno ricevuti durante la campagna o il test.
* Per ulteriori sintassi javascript vedere la sezione «Riferimento javascript per i parametri di profilo di script».

## Visualizzazione delle schede di informazioni relative allo script del profilo {#section_18EA3B919A8E49BBB09AA9215E1E3F17}

Puoi visualizzare schede a comparsa di script di profilo simili come schede informative. Queste schede informative sullo script di profilo ti permettono di visualizzare l&#39;elenco delle attività che si riferiscono allo script di profilo selezionato, insieme ad altri metadati utili.

Ad esempio, se si passa il cursore su uno script di profilo nell&#39;Elenco script di profilo (Destinatari &gt; Script di profilo) e poi si fa clic sull&#39;icona Informazioni, si accede alla seguente scheda di informazioni sullo script di profilo.

La scheda [!UICONTROL Informazioni script] contiene le seguenti informazioni: Nome, Stato, Tipo token, ID script, Sostituisci registro e Descrizione.

![](assets/profile_script_info_card.png)

La scheda [!UICONTROL Utilizzo script] elenca le attività (e aree di lavoro) relative allo script di profilo selezionato.

![](assets/profile_script_info_card_usage_tab.png)

>[!Note]
>
>La scheda Utilizzo script non visualizza le attività che fanno riferimento allo script di profilo selezionato nelle situazioni seguenti:
> * L&#39;attività è nello stato Bozza.
> * Il contenuto o l&#39;offerta utilizzato/a nell&#39;attività impiega variabili di script (o un&#39;offerta in linea all&#39;interno dell&#39;attività o un&#39;offerta nel catalogo Offerte).



## In alcune situazioni, in Target vengono disattivati gli script di profilo {#section_C0FCB702E60D4576AD1174D39FBBE1A7}

[!DNL Target] disabilita automaticamente gli script di profilo in determinate situazioni, ad esempio se richiedono troppo tempo o hanno troppe istruzioni.

Quando uno script di profilo è disabilitato, viene contrassegnato da un’icona gialla di avviso nell’interfaccia utente di Target, come illustrato di seguito:

![](assets/profile_script_invalid.png)

Al passaggio del mouse puoi visualizzare dettagli sugli errori, come illustrato di seguito:

![](assets/profile_script_hover.png)

Il sistema disabilita gli script di profilo in alcune circostanze. I motivi più frequenti sono:

* Riferimento a una variabile non definita.
* Riferimento a un valore non valido. Questo fatto è spesso causato dal riferimento a valori URL e ad altri dati immessi dall’utente senza una corretta convalida.
* Troppe istruzioni JavaScript. Target ha un limite di 2.000 istruzioni JavaScript per ogni script, ma è difficile calcolarle con la semplice lettura manuale del codice JavaScript. Ad esempio, Rhino tratta tutte le chiamate di funzione e le chiamate “nuove” come 100 istruzioni. Inoltre, la dimensione dei dati immessi, ad esempio i valori URL, può influire sul conteggio delle istruzioni.
* Mancato rispetto delle istruzioni evidenziate nella sezione [Best practice](../../c-target/c-visitor-profile/profile-parameters.md#section_64AFE5D2B0C8408A912FC2A832B3AAE0) qui sotto.

## Procedure ottimali {#section_64AFE5D2B0C8408A912FC2A832B3AAE0}

Le seguenti linee guida hanno lo scopo di facilitare la scrittura di script di profilo semplificati, il più possibile privi di errori, mediante la scrittura di codice che genera un errore controllato in modo da consentire l’elaborazione degli script senza determinare un blocco di sistema. Queste linee guida sono il risultato di best practice collaudate in termini di efficienza. Applica queste linee guida unitamente ai principi e alle raccomandazioni stilati dalla community di sviluppo Rhino.

* Imposta il valore dello script corrente su una variabile locale nello script utente, imposta un failover in caso di stringa vuota.
* Convalida la variabile locale verificando che non si tratti di una stringa vuota.
* Utilizza le funzioni di manipolazione basate su stringa anziché le espressioni regolari.
* Utilizza cicli limitati “for” invece di cicli aperti “for” o “while”.
* Non superare 1.300 caratteri o 50 iterazioni di ciclo.
* Non superare 2.000 istruzioni JavaScript. Target ha un limite di 2.000 istruzioni JavaScript per ogni script, ma è difficile calcolarle con la semplice lettura manuale del codice JavaScript. Ad esempio, Rhino tratta tutte le chiamate di funzione e le chiamate “nuove” come 100 istruzioni. Inoltre, la dimensione dei dati immessi, ad esempio i valori URL, può influire sul conteggio delle istruzioni.
* Presta attenzione non solo alle prestazioni dello script, ma anche alle prestazioni combinate di tutti gli script. Come procedura ottimale, si consigliano meno di 5.000 istruzioni in totale. Contare il numero di istruzioni non è ovvio, ma è importante notare che gli script superiori ai 2 KB vengono disattivati automaticamente. Non esiste un limite al numero di script eseguibili, ma ogni script viene eseguito con ogni singola chiamata mbox. Esegui solo il numero di script necessario.
* In caso di esito negativo, inserisci lo script in un try/catch.
* Per ulteriori informazioni, consulta la documentazione del motore JS Rhino: [https://www.mozilla.org/rhino/doc.html](https://www.mozilla.org/rhino/doc.html).

## Script di profilo per testare attività mutualmente esclusive {#section_FEFE50ACA6694DE7BF1893F2EFA96C01}

Puoi utilizzare gli attributi del profilo per impostare test che confrontano due o più attività ma non consentono a uno stesso visitatore di partecipare a ciascuna attività.

La verifica delle attività reciprocamente esclusive impedisce al visitatore di un’attività di influenzare i risultati del test per le altre attività. Quando un visitatore partecipa a più attività, può essere difficile determinare se l’incremento positivo o negativo deriva dall’esperienza del visitatore con una sola attività o se le interazioni tra più attività ne hanno influenzato i risultati.

Ad esempio, puoi testare due aree del tuo sistema di e-commerce. Puoi provare l’effetto di un pulsante “Aggiungi al carrello” rosso invece che blu. Oppure, potresti voler testare un nuovo processo di pagamento che prevede solo due passaggi, invece degli attuali cinque passaggi. Se entrambe le attività hanno lo stesso evento di successo (un acquisto completato), può essere difficile determinare se le conversioni sono state determinate dal pulsante rosso o dal miglioramento del processo di pagamento. Separando i test in attività reciprocamente esclusive, è possibile testare ogni modifica in modo indipendente.

Quando utilizzi uno degli script di profilo seguenti, considera quanto segue:

* Lo script di profilo deve essere eseguito prima dell’avvio dell’attività e deve rimanere invariato per tutta la durata dell’attività.
* Questa tecnica ridurrà la quantità di traffico nell’attività che potrebbe richiedere una durata di esecuzione più lunga. Tieni conto di questo fatto quando stimi la durata dell’attività.

### Configurazione di due attività

Per suddividere i visitatori in gruppi che vedono rispettivamente attività diverse devi creare un attributo di profilo. Un attributo di profilo può indirizzare un visitatore verso uno di due o più gruppi. Per impostare un attributo di profilo denominato “twogroups”, crea lo script seguente:

```
if (!user.get('twogroups')) { 
    var ran_number = Math.floor(Math.random() * 99); 
    if (ran_number < = 49) { 
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

### Configurazione di tre o più attività

L’impostazione di tre o più attività mutuamente esclusive è simile alla configurazione di due, ma devi modificare il JavaScript dell’attributo del profilo per creare un gruppo separato per ogni attività e determinare chi le vede. La generazione di numeri casuali è diversa a seconda che si crei un numero di gruppi pari o dispari.

Ad esempio, per creare quattro gruppi, utilizza il seguente JavaScript:

```
if (!user.get('fourgroups')) { 
    var ran_number = Math.floor​(Math.random() * 99); 
    if (ran_number < = 24) { 
        return 'GroupA'; 
    } else if (ran_number < = 49) { 
        return 'GroupB'; 
    } else if (ran_number < = 74) { 
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
    if (ran_number < = 32.33) { 
        return 'GroupA'; 
    } else if (ran_number < = 65.66) { 
        return 'GroupB'; 
    } else { 
        return 'GroupC'; 
    } 
}
```

## Debug di script di profilo {#section_E9F933DE47EC4B4E9AF2463B181CE2DA}

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

   Poi aggiungi questi due parametri all&#39;URL della tua pagina dopo il &quot;?&quot;: `mboxTrace=window&authorization=YOURTOKEN`.

   In questo modo si ha qualche informazione in più rispetto al token di risposta, perché si ottiene un&#39;istantanea del profilo precedente all&#39;esecuzione e una successiva. Vengono inoltre visualizzati tutti i profili disponibili.

   ![](assets/debug_profile_script_2.png)

## Domande frequenti sugli script di profilo {#section_1389497BB6D84FC38958AE43AAA6E712}

**È possibile utilizzare script di profilo per acquisire informazioni da una pagina che si trova in un livello di dati?**

Gli script di profilo non sono in grado di leggere la pagina direttamente poiché vengono eseguiti lato server. I dati devono essere trasmessi mediante una richiesta mbox o altri  [metodi per l’immissione di dati in Target](../../c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17). Una volta che i dati sono in Target, gli script di profilo possono leggerli come un parametro mbox o un parametro di profilo.

## Riferimento javascript per parametri di profilo di script

È necessaria una semplice conoscenza Javascript per utilizzare in modo efficace i parametri di profilo
di script. Questa sezione funge da riferimento rapido per rendere produttivo questa funzionalità in pochi minuti.

I parametri di profilo di script si trovano sotto la scheda mbox/profiles. È possibile scrivere programmi Javascript che restituiscono qualsiasi tipo Javascript (stringa, integer, array e così via).

### Esempi di parametri di profilo di script

**Nome:***user. recency*

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

Crea una variabile per giorno, in millisecondi. Se il nome della mbox è `orderThankyouPage`, impostate un attributo di profilo utente locale (invisibile) denominato `lastPurchaseTime` per ottenere il valore della data e dell&#39;ora corrente. Il valore dell&#39;ultimo orario di acquisto viene letto e, se è definito, restituisce l&#39;ora passata dall&#39;ultimo momento di acquisto, diviso per il numero di millisecondi in un giorno (risultato del numero di giorni dall&#39;ultimo acquisto).

**Nome:***user. frequency*

```
var frequency = user.get('frequency') || 0;
if (mbox.name == 'orderThankyouPage') {
    return frequency + 1;
}
```

Crea una variabile denominata frequenza, inizializzandola al valore precedente o 0, se non è stato precedente alcun valore. Se il nome della mbox è `orderThankyouPage`, viene restituito il valore incrementale.

**Nome:***user. monetaryvalue*

```
var monetaryValue = user.get('monetaryValue') || 0;
if (mbox.name == 'orderThankyouPage') {
    return monetaryValue + parseInt(mbox.param('orderTotal'));
}
```

Crea una variabile richiamata `monetaryValue`, che cerca il valore corrente per un visitatore specificato (o impostata su 0 in assenza di un valore precedente). Se il nome della mbox è `orderThankyouPage`, viene restituito nuovo valore monetario aggiungendo il precedente e il valore del `orderTotal` parametro passato alla mbox.

### Oggetti e metodi

I parametri di profilo di script possono fare riferimento alle proprietà e ai metodi seguenti:

| Oggetto o metodo | Dettagli |
| --- | --- |
| `page.url` | L&#39;URL corrente. |
| `page.protocol` | Protocollo utilizzato per la pagina (http o https). |
| page.domain | Il dominio dell&#39;URL corrente (tutto prima della prima barra). `www.acme.com``http://www.acme.com/categories/men_jeans?color=blu e&size=small`Ad esempio, in. |
| `page.query` | La stringa di query per la pagina corrente. Tutto ciò che segue? &#39;. `blue&size=small``http://www.acme.com/categories/mens_jeans?color=blue&size=small`Ad esempio, in. |
| `page.param(‘<par_name>’)` | Il valore del parametro indicato da `<par_name>`. Se l&#39;URL corrente è la pagina di ricerca di Google e l&#39;utente è entrato `page.param('hl')`, riceverete «en» per l&#39;URL `http://www.google.com/search?hl=en& q=what+is+asdf&btnG=Google+Search`. |
| `page.referrer` | Lo stesso set di operazioni sopra applicato per referente e destinazione (ad es. referrer. url sarà l&#39;indirizzo url del referente). |
| `landing.url`, `landing.protocol`, `landing.query`, e `landing.param` | Simile a quella della pagina, ma per la pagina di destinazione. |
| `mbox.name` | Nome della mbox attiva. |
| `mbox.param(‘<par_name>’)` | Un parametro mbox in base al nome specificato nella mbox attiva. |
| `profile.get(‘<par_name>’)` | Il parametro del profilo utente creato dal client in base al nome `<par_name>`. Ad esempio, se l&#39;utente imposta un parametro di profilo denominato gender, il valore può essere estratto utilizzando «profile. gender». Restituisce il valore del set «`profile.<par_name>`» impostato per il visitatore corrente; restituisce null se non è stato impostato alcun valore. |
| `user.get(‘<par_name>’)` | Restituisce il valore del set «`user.<par_name>`» impostato per il visitatore corrente; restituisce null se non è stato impostato alcun valore. |
| `user.categoryAffinity` | Restituisce il nome della categoria migliore. |
| `user.categoryAffinities` | Restituisce un array con le categorie migliori. |
| `user.isFirstSession` | Restituisce true se è la prima sessione del visitatore. |
| `user.browser` | Restituisce l&#39;agente utente nell&#39;intestazione HTTP. Ad esempio, potete creare un target con espressione solo per gli utenti Safari di destinazione: `if (user.browser != null && user.browser.indexOf('Safari') != -1) { return true; }` |

### Operatori comuni


Tutti gli operatori javascript standard sono presenti e utilizzabili. Gli operatori javascript possono essere utilizzati su stringhe e numeri (oltre che su altri tipi di dati). Una rapida descrizione:

| Operatore | Descrizione |
| --- | --- |
| `==` | Indica l&#39;uguaglianza. È true se operandi su uno dei lati sono uguali. |
| `!=` | Indica la disuguaglianza. True se operandi su uno dei lati non sono uguali. |
| `<` | Indica che la variabile a sinistra è inferiore alla variabile a destra. Restituisce false se le variabili sono uguali. |
| `>` | Indica che la variabile a sinistra è maggiore della variabile a destra. Restituisce false se le variabili sono uguali. |
| `<=` | Come `<` fatta eccezione se le variabili sono uguali, la valutazione sarà true. |
| `>=` | Come `>` fatta eccezione se le variabili sono uguali, la valutazione sarà true. |
| `&&` | Le espressioni «FF» possono essere inserite in modo logico a sinistra e a destra, vale a dire se sono true (false in caso contrario). |
| `||` | Le espressioni «ORS» inserite in modo logico a sinistra e a destra sono true solo se uno dei lati è true (false in caso contrario). |
| `//` | Controlla se sorgente contiene tutti gli elementi del formato booleano di destinazione (origine Array, destinazione Array).<br>`//` estrae la sottostringa dalla destinazione (corrispondente al regexp) e la `Array/*String*/ decode(String encoding, String regexp, String target)`decodifica.<br>The feature also supports the use of constant string values, grouping (`condition1 || condition2) && condition3`, and regular expressions (`/[^a-z]$/.test(landing.referring.url)`. |

## Video di formazione: Script di profilo

Questo video include informazioni sull&#39;utilizzo e sulla creazione degli script di profilo.

* Cos’è uno script di profilo
* Differenza tra script di profilo e parametro di profilo
* Creare uno script di profilo semplice
* Utilizzare il menu Token disponibile per accedere alle opzioni disponibili
* Abilitare e disabilitare gli script di profilo

>[!VIDEO](https://video.tv.adobe.com/v/17394)