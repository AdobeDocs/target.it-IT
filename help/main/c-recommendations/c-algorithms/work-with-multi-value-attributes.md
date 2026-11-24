---
keywords: multivalore;attributi;consigli;multivalore;multivalore;attributi;consigli;multivalore
description: Scopri come utilizzare un campo con più valori in [!DNL Target Recommendations] utilizzando operatori speciali con più valori.
title: Utilizzo di attributi con più valori
feature: Recommendations
exl-id: 82018a9a-0983-458c-9387-3602dab4409b
TQID: 'https://experienceleague.adobe.com/FrjVxvYfGh2o-qomXRbVh6WS6f65Mja41gBMhejEPlE'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 2%
---
# Utilizzo di attributi con più valori {#multi-value-attributes}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come inviare dati con più valori a [!DNL Adobe Target Recommendations] e come utilizzarli nelle regole di inclusione con gli operatori con più valori.

>[!ENDSHADEBOX]

Un campo multivalore contiene diversi valori per lo stesso elemento o visitatore. Ad esempio:

* Film offerti agli utenti: un dato film ha più attori.
* Biglietti venduti per concerti: un dato utente ha più band preferite.
* Abbigliamento venduto: una camicia è disponibile in più taglie.

Per gestire i consigli in questi scenari, è possibile passare dati con più valori a [!DNL Target Recommendations] e utilizzarli con operatori speciali con più valori.

## Inviare dati con più valori {#send}

Per consentire a [!DNL Recommendations] di identificare dati con più valori, è necessario inviarli come array JSON.

Per un parametro con più valori in JavaScript (`targetPageParams`), vedere [Implementazione di attributi con più valori](/help/main/c-recommendations/c-products/custom-entity-attributes.md#section_80FEFE49E8AF415D99B739AA3CBA2A14) in *Attributi di entità personalizzati*.

In un file CSV, un attributo di entità con più valori viene inviato come array JSON nella cella dell’attributo, come nell’esempio seguente.

+++ File CSV di esempio con un attributo con più valori

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

+++

Quando un attributo di entità, un attributo di profilo o un parametro mbox viene fornito come multivalore in questo formato, [!DNL Recommendations] deduce automaticamente che il campo è multivalore.

## Utilizzare attributi con più valori nelle regole di inclusione {#multi-value-inclusion-rules}

I seguenti operatori sono disponibili per l’utilizzo con attributi di entità, profili e mbox con più valori:

* **[!UICONTROL è contenuto nell&#39;elenco]**
* **[!UICONTROL non è contenuto nell&#39;elenco]**

>[!NOTE]
>
>Il supporto per la corrispondenza dinamica ad attributi con più valori è attualmente disponibile solo nei criteri che utilizzano una regola di corrispondenza degli attributi di profilo o di parametro (mbox) che confronta un singolo valore sul lato sinistro con un valore multiplo sul lato destro. Gli attributi con più valori non sono attualmente supportati nelle promozioni, nella corrispondenza degli attributi di entità o per gli elenchi sul lato sinistro delle regole di inclusione.

### Esempio: escludere gli articoli guardati di recente

Per evitare che vengano consigliati film degli ultimi dieci film guardati dall&#39;utente, scrivere innanzitutto uno script di profilo denominato `user.lastWatchedMovies` che tenga traccia degli ultimi dieci film visualizzati come array JSON. Gli elementi possono quindi essere esclusi con la seguente regola di inclusione:

```
Profile Attribute Matching
id - is not contained in list - user.lastWatchedMovies
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

### Esempio: consigliare gli elementi dai preferiti dell’utente

Per consigliare i biglietti per il concerto solo quando la band che esegue è una delle band preferite dell&#39;utente, sono necessari due elementi: una variabile di profilo denominata `profile.favoriteBands` che contiene le band preferite dell&#39;utente e un attributo `entity.artistPerforming` nel catalogo che contiene l&#39;artista che esegue il concerto. È quindi possibile utilizzare la seguente regola di inclusione:

```
Profile Attribute Matching
artistPerforming - is contained in list - profile.favoriteBands
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

### Esempio: creazione da parte dell’API di criteri che consigliano gli elementi dai preferiti di un utente

I criteri che utilizzano regole di filtro con più valori possono essere creati tramite le API [!DNL Adobe Target], come tutti i criteri. La chiamata API di esempio seguente crea un criterio in cui l&#39;attributo di entità `id` è contenuto nell&#39;elenco di parametri mbox `favorites`:

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

Questa chiamata è associata a JavaScript sulla pagina che trasmette il contenuto dei preferiti:

```
<!-- pass in the value of mbox parameter "favorites" as JSON array -->
<script type="text/javascript">
   mboxCreate('myMbox','entity.id=<key>','favorites=["a","b","c"]');
</script>
```
