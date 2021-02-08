---
keywords: mboxDefine;mboxdefine;definizione mbox;mboxUpdate;mboxupdate;aggiornamento mbox;at.js;funzioni;funzione
description: Utilizzate le funzioni mboxDefine() e mboxUpdate() per la libreria JavaScript di Adobe Target at.js  per definire o aggiornare una mbox. (at.js 1.x)
title: Come si utilizzano le funzioni mboxDefine() e mboxUpdate()?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 85%

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

Esegue la richiesta e applica l&#39;offerta all&#39;elemento identificato da `nodeId` in `mboxDefine()`. Può essere utilizzato anche per aggiornare una mbox iniziata da `mboxCreate`. Incorporata in [!DNL at.js] per lo più per facilitare la transizione da [!DNL mbox.js] ad [!DNL at.js]. È possibile sostituire `mboxDefine()`/`mboxUpdate()` con [adobe.target.getOffer()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffer.md) e [adobe.target.applyOffer()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-applyoffer.md) utilizzando l’opzione del selettore.

## Esempio {#section_9C1E75D9E4BA4DC7879D2B69877EB01A}

```javascript
<div id="someId" class="mboxDefault"></div> 
<script> 
 mboxDefine('someId','mboxName','param1=value1','param2=value2'); 
 mboxUpdate('mboxName','param3=value3','param4=value4'); 
</script>
```
