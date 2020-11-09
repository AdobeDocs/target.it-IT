---
keywords: Profile script;profile script attributes;mutually exclusive activities
description: Puoi utilizzare gli attributi del profilo per impostare test che confrontano due o più attività ma non consentono a uno stesso visitatore di partecipare a ciascuna attività.
title: 'Utilizzare gli script di profilo per testare attività reciprocamente esclusive '
feature: visitor profiles
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 84%

---


# Utilizzare gli script di profilo per testare attività reciprocamente esclusive {#section_FEFE50ACA6694DE7BF1893F2EFA96C01}

Puoi utilizzare gli attributi del profilo per impostare test che confrontano due o più attività ma non consentono a uno stesso visitatore di partecipare a ciascuna attività.

La verifica delle attività reciprocamente esclusive impedisce al visitatore di un’attività di influenzare i risultati del test per le altre attività. Quando un visitatore partecipa a più attività, può essere difficile determinare se l’incremento positivo o negativo deriva dall’esperienza del visitatore con una sola attività o se le interazioni tra più attività ne hanno influenzato i risultati.

Ad esempio, puoi testare due aree del tuo sistema di e-commerce. Potrebbe essere utile verificare se il pulsante &quot;Aggiungi al carrello&quot; è rosso invece che blu. Oppure, potresti voler testare un nuovo processo di pagamento che prevede solo due passaggi, invece degli attuali cinque passaggi. Se entrambe le attività hanno lo stesso evento di successo (un acquisto completato), può essere difficile determinare se il pulsante rosso migliora le conversioni, o se le stesse conversioni sono state aumentate a causa del miglioramento del processo di estrazione. Separando i test in attività reciprocamente esclusive, è possibile testare ogni modifica in modo indipendente.

Quando utilizzi uno degli script di profilo seguenti, considera quanto segue:

* Lo script di profilo deve essere eseguito prima dell’avvio dell’attività e deve rimanere invariato per tutta la durata dell’attività.
* Questa tecnica riduce la quantità di traffico nell&#39;attività, che potrebbe richiedere un&#39;esecuzione più lunga dell&#39;attività. Tieni conto di questo fatto quando stimi la durata dell’attività.

## Impostazione di due attività

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

* `if (!user.get('twogroups'))` determina se l’attributo di profilo *twogroups* è impostato per il visitatore corrente. In caso affermativo, non è necessaria alcuna ulteriore azione.

* `var ran_number=Math.floor(Math.random() *99)` dichiara una nuova variabile chiamata ran_number, imposta il suo valore su un decimale casuale tra 0 e 1, poi lo moltiplica per 99 e lo arrotonda verso il basso per creare un intervallo di 100 (0-99), utile per specificare una percentuale di visitatori che vedono l’attività.

* `if (ran_number <= 49)` inizia una routine che determina il gruppo a cui appartiene il visitatore. Se il numero restituito è 0-49, il visitatore viene assegnato a GroupA. Se il numero è 50-99, il visitatore viene assegnato a GroupB. Il gruppo determina l’attività che verrà visualizzata dal visitatore.

After you create the profile attribute, set up the first activity to target the desired population by requiring that the user profile parameter `user.twogroups` matches the value specified for GroupA.

>[!NOTE]
>
>Scegli una mbox all’inizio della pagina. Questo codice determina se un visitatore esegue o meno l&#39;attività. Se il browser incontra subito una mbox, questa può essere utilizzata per impostare questo valore.

Imposta la seconda campagna in modo che il parametro `user.twogroups` del profilo utente corrisponda al valore specificato per GroupB.

## Impostazione di tre o più attività

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
