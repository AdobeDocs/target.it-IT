---
description: 'Informazioni sulla funzione mboxCreate(mbox,params) per at.js. '
keywords: adobe.target.notification;element;selector;notification;extension
seo-description: Informazioni sulla funzione mboxCreate(mbox,params) per la libreria JavaScript at.js di Adobe Target.
seo-title: Informazioni sulla funzione mboxCreate(mbox,params) per la libreria JavaScript at.js di Adobe Target.
solution: Target
subtopic: Introduzione
title: mboxCreate(mbox,params) - at.js 2.x
topic: Standard
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# mboxCreate(mbox,params) - at.js 1.x {#reference_E68805FE86C64792B2066DB17B253D74}

Esegue una richiesta e applica l’offerta all’elemento DIV più vicino con il nome della classe mboxDefault.

>[!NOTE]
>
>Questa funzione è disponibile per at.js versione 1.Solo *x*. Questa funzione è stata rimossa con il rilascio di at.js 2.x e restituisce il contenuto predefinito se utilizzata con at.js 2.x.

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