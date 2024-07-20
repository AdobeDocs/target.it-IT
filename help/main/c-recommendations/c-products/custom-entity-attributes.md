---
keywords: attributi di entità multivalore;attributi di entità personalizzati;JSON valido;valore di attributo di entità;vettore JSON;array JSON;matrice JSON;multivalore;con più valori
description: Scopri come utilizzare attributi di entità personalizzati a valore singolo e multiplo per definire informazioni aggiuntive sugli elementi nel catalogo Recommendations dell'Adobe [!DNL Target] .
title: Come Si Utilizzano Gli Attributi Di Entità Personalizzati?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Recommendations
mini-toc-levels: 3
exl-id: d7d0b04a-0f50-4d30-9cbe-c0347a3d3715
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '1454'
ht-degree: 81%

---

# Attributi di entità personalizzati

Utilizzare attributi di entità personalizzati a valore singolo e multiplo in [!DNL Adobe Target Recommendations] per definire informazioni aggiuntive sugli elementi del catalogo.

## Limiti {#limits}

Per definire informazioni aggiuntive sugli elementi del catalogo, puoi includere fino a 100 attributi di entità personalizzati. Ad esempio, puoi creare un attributo personalizzato denominato `entity.genre` per definire un libro o un film. In alternativa, per la vendita di biglietti si possono creare attributi per il luogo di un evento in modo da includere un artista secondario, come la squadra ospite di un evento sportivo o il gruppo spalla di un concerto.

La lunghezza massima degli attributi personalizzati delle entità con valore singolo è di 15.000 caratteri (per lingue con codifica UTF-8 a uno e due byte, come inglese e altre lingue basate su alfabeto latino) oppure 10.000 caratteri (per lingue con codifica UTF-8 a tre byte come cinese, giapponese e coreano).

Gli attributi personalizzati delle entità con più valori possono contenere un massimo di 500 valori. Ogni singolo valore è limitato a 100 caratteri. Il numero totale di caratteri su tutti i valori deve rispettare le limitazioni di lunghezza massima degli attributi personalizzati delle entità a valore singolo (vedi sopra).

## Valori degli attributi di entità personalizzati {#section_313331A9F8194A89B5EDD89363018651}

Gli attributi di entità personalizzati possono contenere uno o più valori. I valori degli attributi di entità vengono mostrati nella visualizzazione del prodotto.

![immagine multivalore_prodotto](assets/multi-value_product.png)

Un attributo di entità personalizzato con un valore singolo è formato come un attributo di entità predefinito a valore singolo:

`entity.genre=genre1`

Un attributo di entità personalizzato con più valori deve essere inviato come array JSON valido:

`entity.genre=["genre1", "genre2"]`

Esempi di array JSON validi supportati da [!DNL Recommendations]:

* `["AB","BC"]` tutti i valori sono stringhe
* `[1,2]` tutti i valori sono numerici

>[!NOTE]
>
>[!DNL Recommendations] non supporta tipi di valore misti negli attributi di entità con più valori. Ad esempio, `["AB",1,true, [1,2,3]]` è un array JSON valido, ma non è supportato in [!DNL Recommendations] perché include tipi di valori misti (stringa, numerico, booleano, oggetto).

Dopo che un attributo personalizzato viene inviato come array JSON valido, viene considerato come un attributo con più valori per tutti i prodotti del catalogo.

>[!NOTE]
>
>Per cambiare un attributo con più valori in attributo con valore singolo, devi cancellare il catalogo e caricare i dati prodotto corretti. L’eliminazione del catalogo non comporta l’eliminazione dei dati cronologici associati agli ID dei prodotti. Per ulteriori informazioni, consulta [Eliminazione di tutti gli elementi dal sistema](/help/main/assets/adobe-recommendations-classic.pdf) nella documentazione di *Adobe Recommendations Classic*.

**Limitazioni**:

* Non è possibile utilizzare nomi di attributi di entità predefiniti per attributi di entità personalizzati. (Consulta [Attributi di entità](/help/main/c-recommendations/c-products/entity-attributes.md#reference_3BCC1383FB3F44F4A2120BB36270387F).)
* L’attributo `entity.environment` è riservato dal sistema e non può essere utilizzato per gli attributi di entità personalizzati. I tentativi di passare `entity.environment` tramite `targetPageParams`, feed o API verranno ignorati.
* Gli array devono contenere un unico tipo di valore. Gli array con valori misti (`["AB",1,true]`) non sono supportati.
* Un attributo con più valori che include un array JSON nidificato (`[10,12,[1,2,3]]`) viene considerato come un attributo a valore singolo.

## Implementazione di attributi con più valori {#section_80FEFE49E8AF415D99B739AA3CBA2A14}

Gli attributi di entità personalizzate con più valori sono supportati quando si utilizzano feed (CSV), `targetPageParams` e l’API di consegna per caricare i prodotti. I nuovi valori sostituiscono quelli correnti; non vengono aggiunti. Gli array vuoti ( [] ) vengono considerati privi di valori.

Le virgolette doppie devono essere precedute dalla sequenza di escape. Ad esempio, `"[""test"", ""value""]"` è un array JSON valido che può essere utilizzato in CSV.

Un attributo con più valori può avere fino a 500 valori.

### Utilizzo di targetPageParams

L’esempio seguente illustra come utilizzare `targetPageParams`

```javascript
function targetPageParams() { 
  return { 
    'entity.id':                   '123', 
    'entity.categoryId':            '["A", "A:B", "A:B:C", "A:B:C:D"]',        
    'entity.MultiValueAttribute':   '["X", "Y", "Z"]', 
    'entity.event.detailsOnly':     'true', 
    'excludedIds":                  '[123, 3232, 2323, 4344]', 
    'orderId":                      '123456', 
    'orderTotal":                   '195.32', 
    'productPurchaseId":            '[001,002,003]' 
  }; 
}
```

### Utilizzo di CSV

Puoi gestire i file CSV in formato raw tramite un editor di testo o un foglio di calcolo.

Il CSV raw sarà simile a questo:

![immagine multi-value_example_raw](assets/multi-value_example_raw.png)

Lo stesso catalogo si presenterà così in un foglio di calcolo:

![immagine multi-value_example_excel](assets/multi-value_example_excel.png)

Durante la conversione in formato .csv, il foglio di calcolo aggiunge virgolette doppie attorno al contenuto delle celle per evitare che le virgole all’interno della cella agiscano come separatori di colonna. Vengono inoltre aggiunte virgolette doppie intorno ai valori di stringa JSON inclusi negli attributi con più valori personalizzati. Questo può rendere complicato lavorare direttamente sul file raw. Ad esempio:

* Foglio di calcolo: `["1","2","3"]`
* Raw: `"[""1"",""2"",""3""]"`

Presta attenzione quando modifichi direttamente un file di catalogo CSV raw.

### Utilizzo delle API

Puoi trasmettere attributi con più valori utilizzando l’API di consegna in un parametro mbox come valore stringa contenente un array JSON con escape.

```javascript
"execute": {
    "mboxes": [
      {
        "index": 0,
        "name": "first-mbox",
        "parameters": {
          "entity.id": "32323",
          "entity.categoryId": "My Category",
          "entity.MultiValueAttribute": "[\"X\", \"Y\", \"Z\"]"
        }
      }
    ]
  }
```

Per informazioni sull&#39;utilizzo delle API di recapito e salvataggio di entità, consulta la [documentazione delle API di Adobe Recommendations](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}.

## Utilizzo di operatori con attributi con più valori {#section_83C2288A805242D9A02EBC4F07DEE945}

Quando applichi gli operatori agli attributi personalizzati con più valori nelle regole di inclusione degli algoritmi, di catalogo e di esclusione, il risultato sarà *vero* se almeno un valore nell’elenco deve essere soddisfatto (booleano *or*).

Nell&#39;esempio seguente, la regola è `message contains abc`.

* Caso 1: `entity.genre = ["ab", "bc", "de"]`. Il risultato è falso perché nessun valore contiene `abc`.
* Caso 2: `entity.genre = ["abcde","de","ef"]`. Il risultato è vero perché un valore contiene `abc`.

Per gli operatori negativi, tutti i valori di attributo devono essere soddisfatti (booleano *and*). Ad esempio, se l&#39;operatore è `notEquals`, il risultato sarà *false* se viene trovato un valore.

Per informazioni sul comportamento dell’operatore nelle regole di inclusione degli algoritmi, di catalogo e di esclusione, consulta le sezioni seguenti.

### È uguale a

Se un qualunque valore di attributo è uguale al valore specificato, restituisce vero.

Esempio: `genre equals abc`

* Caso 1: `entity.genre = ["ab", "bc", "de"]`. Il risultato è falso perché nessun valore è uguale a `abc`.
* Caso 2: `entity.genre = ["abc", "de", "ef"]`. Il risultato è vero perché un valore è uguale a `abc`.
* Caso 3: `entity.genre = ["abcde", "de", "ef"]`. Il risultato è falso perché `abc` non è uguale a nessun elemento dell’elenco.

### È diverso da

Se nessun valore di attributo è uguale al valore inserito, restituisce vero.

Esempio: `genre not equals abc`

* Caso 1: `entity.genre = ["ab", "bc", "de"]`. Il risultato è vero perché nessun valore è uguale a `abc`.
* Caso 2: `entity.genre = ["abc", "de", "ef"]`. Il risultato è falso perché un valore è uguale a `abc`.
* Caso 3: `entity.genre = ["abcde", "de", "ef"]`. Il risultato è vero perché `abc` non è uguale a nessun elemento dell’elenco.

### Contiene

Se un qualunque valore di attributo contiene il valore specificato, restituisce vero.

Esempio: `genre contains abc`

* Caso 1: `entity.genre = ["ab", "bc", "de"]`. Il risultato è falso perché nessun valore contiene `abc`.
* Caso 2: `entity.genre = ["abcde", "de", "ef"]`. Il risultato è vero perché un valore contiene `abc`.

### Non contiene

Se nessun valore di attributo contiene il valore specificato, restituisce vero.

Esempio: `genre does not contain abc`

* Caso 1: `entity.genre = ["ab", "bc", "de"]`. Il risultato è vero perché nessun valore contiene `abc`.
* Caso 2: `entity.genre = ["abcde", "de", "ef"]`. La regola si tradurrà in falso perché un valore contiene`abc`.

### Inizia con

Se un qualunque valore di attributo inizia con il valore specificato, restituisce vero.

Esempio: `genre starts with abc`

* Caso 1: `entity.genre = ["ab", "bc", "de"]`. Il risultato è falso perché nessun valore inizia con `abc`.
* Caso 2: `entity.genre = ["abcde", "de", "ef"]`. Il risultato è vero perché un valore inizia con `abc`.
* Caso 3: `entity.genre = ["ab", "de", "abc"]`. Il risultato è vero perché inizia un valore inizia con `abc` (non necessariamente il primo elemento dell’elenco).

### Termina con

Se un qualunque valore di attributo termina con il valore specificato, restituisce vero.

Esempio: `genre ends with abc`

* Caso 1: `entity.genre = ["ab", "bc", "de"]`. Il risultato è falso perché nessun valore termina con `abc`.
* Caso 2: `entity.genre = ["deabc", "de", "ef"]`. Il risultato è vero perché un valore termina con `abc`.

### Maggiore o uguale a (solo valori numerici)

Il valore dell’attributo viene convertito in doppio. Gli attributi che non possono essere convertiti vengono ignorati durante l’esecuzione della regola.

Dopo l’elaborazione, qualsiasi valore di attributo maggiore o uguale al valore specificato restituisce vero.

Esempio: `price greater than or equal to 100`

* Caso 1: `entity.price = ["10", "20", "45"]`. Il risultato è falso perché nessun valore è maggiore o uguale a 100. Il valore `de` viene ignorato perché non può essere convertito in doppio.
* Caso 2: `entity.price = ["100", "101", "90", "80"]`. Il risultato è vero perché due valori sono maggiori o uguali a 100.

### Minore o uguale a (solo valori numerici)

Il valore dell’attributo viene convertito in doppio. Gli attributi che non possono essere convertiti vengono ignorati durante l’esecuzione della regola.

Dopo l’elaborazione, qualsiasi valore di attributo inferiore o uguale al valore specificato restituisce vero.

Esempio: `price less than or equal to 100`

* Caso 1: `entity.price = ["101", "200", "141"]`. Il risultato è falso perché nessun valore è minore o uguale a 100. Il valore `de` viene ignorato perché non può essere convertito in doppio.
* Caso 2: `entity.price = ["100", "101", "90", "80"]`. Il risultato è vero perché due valori sono minori o uguali a 100.

### Corrisponde dinamicamente (disponibile solo negli algoritmi basati su elementi)

Se un qualunque valore di attributo corrisponde al valore specificato, restituisce vero.

Esempio: `genre matches abc`

* Caso 1: `entity.genre = ["ab", "bc", "de"]`. Il risultato è falso perché nessun valore corrisponde a `abc`.
* Caso 2: `entity.genre = ["abc", "de", "ef"]`. Il risultato è vero perché un valore corrisponde a `abc`.

### Non corrisponde dinamicamente (disponibile solo negli algoritmi basati su elementi)

Se un qualunque valore di attributo corrisponde al valore specificato, restituisce falso.

Esempio: `genre does not match abc`

* Caso 1: `entity.genre = ["ab", "bc", "de"]`. Il risultato è vero perché nessun valore corrisponde a `abc`.
* Caso 2: `entity.genre = ["abc", "de", "ef"]`. La regola si tradurrà in falso perché un valore corrisponde a `abc`.

### Rientra dinamicamente nell’intervallo (disponibile solo negli algoritmi basati su elementi, solo per valori numerici)

Se un qualunque valore di attributo numerico rientra nell’intervallo specificato, restituisce vero.

Esempio: `price dynamically ranges in 80% to 120% of 100`

* Caso 1: `entity.price = ["101", "200", "125"]`. Il risultato è vero perché `101` è compreso tra l’80% e il 120% di 100. Il valore `de` viene ignorato perché non può essere convertito in doppio.
* Caso 2: `entity.price = ["130", "191", "60", "75"]`. Il risultato è falso perché nessun valore è compreso tra l’80% e il 120% di 100.

>[!NOTE]
>
>*Doppio* è un tipo di dati Java. Per gli operatori che richiedono valori numerici, la conversione in doppio elimina i valori non numerici dalla considerazione nei risultati.

## Attributi con più valori nelle progettazioni {#section_F672E4F6E1D44B3196B7ADE89334ED4A}

Gli attributi con più valori vengono visualizzati come elenco separato da virgole quando vi si fa riferimento in una progettazione.

Esempio:

Quando `entity.genre=["genre1","genre2"]` ha un riferimento in un progetto come `$entity<N>.genre`, il risultato è `genre1, genre2`.

## Argomenti correlati:

* [Attributi di entità](/help/main/c-recommendations/c-products/entity-attributes.md#reference_3BCC1383FB3F44F4A2120BB36270387F)
