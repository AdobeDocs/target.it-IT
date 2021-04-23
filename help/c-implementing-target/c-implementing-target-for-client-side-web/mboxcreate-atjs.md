---
keywords: mboxCreate;mboxcreate;mbox create;at.js;funzioni;funzione
description: Utilizza la funzione mboxCreate() per la libreria JavaScript Adobe [!DNL Target] at.js per applicare le offerte al DIV più vicino con il nome della classe mboxDefault. (at.js 1.x)
title: Come si utilizza la funzione mboxCreate()?
feature: at.js
role: Developer
exl-id: 821ad97a-345a-4e56-9be6-ab1c7d3a651d
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 85%

---

# mboxCreate(mbox,params) - at.js 1.x

Esegue una richiesta e applica l’offerta all’elemento DIV più vicino con il nome della classe mboxDefault.

>[!NOTE]
>
>Questa funzione è disponibile per at.js versione 1.*x*. Questa funzione è stata rimossa con il rilascio di at.js 2.x e restituisce il contenuto predefinito se utilizzata con at.js 2.x.

Questa funzione è incorporata in [!DNL at.js] per lo più per facilitare la transizione da [!DNL mbox.js] ad [!DNL at.js]. Un’alternativa più recente a `mboxCreate()` è `adobe.target.getOffer()`/`adobe.target.applyOffer()` o la direttiva angolare.

## Esempio

```javascript
<div class="mboxDefault"> 
  default content to replace by offer 
</div> 
<script> 
  mboxCreate('mboxName','param1=value1','param2=value2'); 
</script>
```

## Note

`mboxCreate()` usa ora l&#39;endpoint “json” invece di quello “standard” e si attiva in modo asincrono. Per questo motivo:

* [Il debug](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md#concept_CAE591DA8C404C22917584ECD4F7494F) è un po&#39; diverso.
* Evita di usare codice di offerte che richiede chiamate sincrone e bloccanti.

   Ad esempio, offerte che impostano variabili JavaScript che vengono utilizzate dal codice del sito o altre mbox che compaiono più avanti nella pagina.

* Assicurati di avere un `<div class="mboxDefault"></div>`prima di richiamare `mboxCreate()`, poiché [!DNL at.js] non ne aggiungerà una per te.

* Le funzioni vuote di `mboxCreate()` non sono consigliate come mbox globale.

   È preferibile utilizzare una mbox globale creata automaticamente in [!DNL at.js] perché si attiva dalla sezione `<head>` e può restituire prima il contenuto.
