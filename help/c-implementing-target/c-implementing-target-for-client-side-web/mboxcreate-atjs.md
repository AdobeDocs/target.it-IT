---
description: 'Informazioni sulla funzione mboxcreate (mbox, params) per at. js. '
keywords: adobe.target.notification;element;selector;notification;extension
seo-description: Informazioni sulla funzione mboxcreate (mbox, params) per la libreria di Adobe Target nella libreria javascript. js.
seo-title: Informazioni sulla funzione mboxcreate (mbox, params) per la libreria di Adobe Target nella libreria javascript. js.
solution: Target
subtopic: Introduzione
title: mboxCreate(mbox,params) - at.js 2.x
topic: Standard
translation-type: tm+mt
source-git-commit: 126f62d8966beb8157f54f87cf68b092fe976c51

---


# mboxCreate(mbox,params) - at.js 1.x {#reference_E68805FE86C64792B2066DB17B253D74}

Esegue una richiesta e applica l’offerta all’elemento DIV più vicino con il nome della classe mboxDefault.

>[!NOTE]
>
>Questa funzione è disponibile per at.js versione 1.Solo *x*. Questa funzione è stata rimossa dal rilascio di at. js 2. x. Questa funzione restituisce il contenuto predefinito se utilizzato con at. js 2. x.

Questa funzione è incorporata in [!DNL at.js] per lo più per facilitare la transizione da [!DNL mbox.js] ad [!DNL at.js]. Un’alternativa più recente a `mboxCreate()` è `adobe.target.getOffer()`/`adobe.target.applyOffer()` o la direttiva angolare.

## Esempio 

```
<div class="mboxDefault"> 
  default content to replace by offer 
</div> 
<script> 
  mboxCreate('mboxName','param1=value1','param2=value2'); 
</script>
```

## Note

`mboxCreate()` usa ora l&#39;endpoint “json” invece di quello “standard” e si attiva in modo asincrono. Per questo motivo:

* [Il debug](../../c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md#concept_CAE591DA8C404C22917584ECD4F7494F) è un po&#39; diverso.
* Evita di usare codice di offerte che richiede chiamate sincrone e bloccanti.

   Ad esempio, offerte che impostano variabili JavaScript che vengono utilizzate dal codice del sito o altre mbox che compaiono più avanti nella pagina.

* Assicurati di avere un `<div class="mboxDefault"></div>`prima di richiamare `mboxCreate()`, poiché [!DNL at.js] non ne aggiungerà una per te.

* Le funzioni vuote di `mboxCreate()` non sono consigliate come mbox globale.

   È preferibile utilizzare una mbox globale creata automaticamente in [!DNL at.js] perché si attiva dalla sezione `<head>` e può restituire prima il contenuto.