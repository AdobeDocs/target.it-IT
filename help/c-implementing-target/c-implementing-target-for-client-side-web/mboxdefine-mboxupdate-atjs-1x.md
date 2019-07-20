---
description: 'Informazioni sulle funzioni mboxDefine() e mboxUpdate() per at.js. '
keywords: adobe.target.notification;element;selector;notification;extension
seo-description: Informazioni sulle funzioni mboxDefine() e mboxUpdate() per la libreria JavaScript at.js di Adobe Target.
seo-title: Informazioni sulle funzioni mboxDefine() e mboxUpdate() per la libreria JavaScript at.js di Adobe Target.
solution: Target
subtopic: Introduzione
title: mboxDefine() e mboxUpdate() - at.js 1.x
topic: Standard
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# mboxDefine() e mboxUpdate() - at.js 1.x

Definisce e aggiorna una mbox in Adobe Target.

>[!NOTE]
>
>Queste funzioni sono disponibili solo per at.js versione 1.Solo *x*. Queste funzioni sono state rimosse con il rilascio di at.js 2.x. Restituiscono il contenuto predefinito se utilizzate con at.js 2.x.

`mboxDefine()` e `mboxCreate()` sono legate agli elementi DIV HTML in cui l’offerta deve essere visualizzata. Questi elementi DIV HTML devono avere la classe `mboxDefault`. Se gli elementi HTML non hanno questa classe collegata, è possibile che venga visualizzato momentaneamente altro contenuto.

## mboxDefine {#section_134BAAE8EE9D49D8BAFEA5E7EAB93BA7}

Crea una mappatura interna tra un nodeId e un nome mbox, ma non esegue la richiesta. Utilizzato in combinazione con `mboxUpdate()`. Incorporata in [!DNL at.js]per lo più per facilitare la transizione da [!DNL mbox.js] ad [!DNL at.js].

## mboxUpdate {#section_D20B3E551884452A996305C12D5959D5}

Esegue la richiesta e applica l'offerta all'elemento identificato da `nodeId` in `mboxDefine()`. Può essere utilizzato anche per aggiornare una mbox iniziata da `mboxCreate`. Incorporata in [!DNL at.js] per lo più per facilitare la transizione da [!DNL mbox.js] ad [!DNL at.js]. È possibile sostituire `mboxDefine()`/`mboxUpdate()` con [adobe.target.getOffer()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffer.md) e [adobe.target.applyOffer()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-applyoffer.md) utilizzando l’opzione del selettore.

## Esempio {#section_9C1E75D9E4BA4DC7879D2B69877EB01A}

```
<div id="someId" class="mboxDefault"></div> 
<script> 
 mboxDefine('someId','mboxName','param1=value1','param2=value2'); 
 mboxUpdate('mboxName','param3=value3','param4=value4'); 
</script>
```
