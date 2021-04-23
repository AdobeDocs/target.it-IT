---
keywords: multivalore;attributi;consigli;valore multiplo;multivalore;multivalore
description: Scopri come utilizzare un campo multivalore in Adobe [!DNL Target] Recommendations utilizzando operatori multivalore speciali, ad esempio per consigliare filmati con più attori.
title: Posso utilizzare attributi con più valori in Recommendations?
feature: Consigli
exl-id: 82018a9a-0983-458c-9387-3602dab4409b
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 1%

---

# Utilizzo di attributi con più valori

A volte può essere utile utilizzare un campo con più valori. Prendi in considerazione gli esempi seguenti:

* Offri film agli utenti. Un dato film ha più attori.
* Vende biglietti per concerti. Un dato utente ha più bande preferite.
* Vende vestiti. Una camicia è disponibile in più dimensioni.

Per gestire i consigli in questi scenari, puoi trasmettere dati con più valori a [!DNL Target Recommendations] e utilizzare operatori multivalore speciali.

Per consentire a [!DNL Recommendations] di identificare dati con più valori, questi devono essere inviati come array JSON, come negli esempi di codice riportati di seguito.

## Trasmettere un parametro con più valori in JavaScript

```
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

Per ulteriori informazioni, consulta [Implementazione di attributi con più valori](/help/c-recommendations/c-products/custom-entity-attributes.md#section_80FEFE49E8AF415D99B739AA3CBA2A14) in *Attributi di entità personalizzati*.

## Trasmettere un attributo di entità con più valori in un file CSV

```
## RECSRecommendations Upload File,,,,,,,,,,,,,,,,,,,
## RECS''## RECS'' indicates a Recommendations pre-process header. Please do not remove these lines.,,,,,,,,,,,,,,,,,,,
## RECS,,,,,,,,,,,,,,,,,,,
## RECSUse this file to upload product display information to Recommendations. Each product has its own row. Each line must contain 19 values and if not all are filled a space should be left.,,,,,,,,,,,,,,,,,,,
## RECSThe last 100 columns (entity.custom1 - entity.custom100) are custom. The name 'customN' can be replaced with a custom name such as 'onSale' or 'brand'.,,,,,,,,,,,,,,,,,,,
## RECSIf the products already exist in Recommendations then changes uploaded here will override the data in Recommendations. Any new attributes entered here will be added to the product''s entry in Recommendations.,,,,,,,,,,,,,,,,,,,
## RECSentity.id ,entity.name,entity. categoryId ,entity. message ,entity.thumbnailUrl ,entity.value ,entity.pageUrl ,entity.inventory ,entity.margin ,entity.custom1 ,entity.custom2 ,entity.custom3 ,entity.custom4,entity.custom5,entity.custom6,entity.custom7,entity.custom8,entity.custom9,entity.custom10,
1,Sample Product 1,category1,Save 10%,http://sample.store/products/images/product1_th.jpg,325,http://sample.store/products/product_detail.jsp?productId=1,1000,48,a,"[ ""v1"", ""v2"" ]",, , , , , , , ,
2,Sample Product 2,category1,Save 10%,http://sample.store/products/images/product2_th.jpg,369,http://sample.store/products/product_detail.jsp?productId=2,1000,52,a,"[ ""v1"", ""v2"" ]",, , , , , , , ,
3,Sample Product 3,category1,Save 10%,http://sample.store/products/images/product3_th.jpg,479,http://sample.store/products/product_detail.jsp?productId=3,1000,78,a,"[ ""v1"", ""v2"" ]",,,,,,,,,
4,Sample Product 4,category1,Save 10%,http://sample.store/products/images/product4_th.jpg,409,http://sample.store/products/product_detail.jsp?productId=4,1000,66,a,"[ ""v1"", ""v2"" ]",,,,,,,,,
5,Sample Product 5,category1,Save 10%,http://sample.store/products/images/product5_th.jpg,325,http://sample.store/products/product_detail.jsp?productId=5,1000,45,a,"[ ""v1"", ""v2"" ]",,,,,,,,, 
```

Quando un attributo di entità, un attributo di profilo o un parametro mbox viene fornito come valore multiplo in base al formato di cui sopra, [!DNL Recommendations] deduce automaticamente che il campo è multivalore.

I seguenti operatori sono disponibili per l’utilizzo con attributi di entità con più valori, profili e mbox:

* [!UICONTROL è contenuto nell&#39;elenco]
* [!UICONTROL non è contenuto nell&#39;elenco]

## Utilizzo di attributi con più valori nelle regole di inclusione

>[!NOTE]
>
>Il supporto per la corrispondenza dinamica agli attributi con più valori è attualmente disponibile solo nei criteri quando si utilizza una regola di corrispondenza degli attributi di profilo o degli attributi di parametro (mbox) quando si confronta un singolo valore a sinistra con un lato destro con più valori. Gli attributi con più valori non sono attualmente supportati nelle promozioni, nella corrispondenza degli attributi di entità o negli elenchi sul lato sinistro delle regole di inclusione.

### Esempio: Escludere gli elementi guardati di recente

Supponiamo di voler evitare che vengano consigliati tutti i film presenti negli ultimi dieci film visualizzati dall’utente. Innanzitutto, scrivi uno script di profilo denominato `user.lastWatchedMovies` per tenere traccia degli ultimi dieci film visualizzati come array JSON. Quindi, puoi escludere gli elementi utilizzando la seguente regola di inclusione:

```
`Profile Attribute Matching`
`id - is not contained in list - user.lastWatchedMovies`
```

Rappresentazione API JSON della regola di inclusione:

```
{
    "attribute": "id",
    "operation": "isNotContainedInList",
    "source": {
        "name": "user.lastWatchedMovies",
        "type": "PROFILE"
    }
} 
```

### Esempio: Consiglia gli elementi dai preferiti dell’utente

Supponiamo che tu voglia consigliare i biglietti solo ai concerti se la band è una delle band preferite dall&#39;utente. In primo luogo, assicurati di disporre di una variabile di profilo denominata `profile.favoriteBands` che contiene le bande preferite dell’utente. Quindi, assicurati che il catalogo includa un attributo `entity.artistPerforming` che includa l&#39;artista che esegue il concerto. Quindi, puoi utilizzare la seguente regola di inclusione:

```
`Profile Attribute Matching`
`artistPerforming - is contained in list - profile.favoriteBands`
```

Rappresentazione API JSON della regola di inclusione:

```
{
    "attribute": "artistPerforming",
    "operation": "isContainedInList",
    "source": {
        "name": "profile.favoriteBands",
        "type": "PROFILE"
    }
}
```

### Esempio: Creazione API di criteri per la raccomandazione di elementi dai preferiti di un utente

I criteri che utilizzano regole di filtro con più valori, come tutti i criteri, possono essere creati tramite API di Adobe I/O. Una chiamata API di esempio per creare un criterio in cui l’attributo di entità `id` è contenuto nell’elenco dei parametri mbox `favorites` è fornita qui:

```
curl -X POST \
  https://<serverhost>/api/recs/<client>/criteria/item \
  -H 'Accept: application/vnd.adobe.target.v1+json' \
  -H 'Accept-Encoding: gzip, deflate' \
  -H 'Cache-Control: no-cache' \
  -H 'Connection: keep-alive' \
  -H 'Content-Type: application/json' \
  -H 'User-Agent: <from API client>' \
  -H 'X-Target-user-email: <email address>' \
  -H 'cache-control: no-cache' \
  -d '{
    "name": "viewed criteria",
    "criteriaTitle": "test title",
    "type": "VIEWED_CF",
    "key": "CURRENT",
    "daysCount": "TWO_WEEKS",
    "aggregation": "NONE",
    "backupDisabled": false,
    "partialDesignAllowed": true,
    "configuration": {
        "inclusionRules": [
            {
                "attribute": "id",
                "operation": "isContainedInList",
                "source": {
                    "name": "mbox.favorites",
                    "type": "MBOX"
                }
            }
        ]
    }
}'
```

Questo verrebbe associato a JavaScript nella pagina per passare il contenuto dei preferiti:

```
<!-- pass in the value of mbox parameter “favorites” as JSON array -->
<script type="text/javascript">
   mboxCreate('myMbox','entity.id=<key>','favorites=["a","b","c"]');
</script>
```
