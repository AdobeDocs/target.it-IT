---
keywords: mboxDefine;mboxdefine;definizione mbox;mboxUpdate;mboxupdate;aggiornamento mbox;at.js;funzioni;funzione
description: Utilizza le funzioni mboxDefine() e mboxUpdate() per l'Adobe [!DNL Target] Libreria JavaScript at.js per definire o aggiornare una mbox. (at.js 1.x)
title: Come si utilizzano le funzioni mboxDefine() e mboxUpdate()?
feature: at.js
role: Developer
exl-id: 48261be0-c4d0-4961-9712-ef7e0d2cb1c0
source-git-commit: 719eb95049dad3bee5925dff794871cd65969f79
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 63%

---

# mboxDefine() e mboxUpdate() - at.js 1.x

Definisce e aggiorna una mbox in Adobe Target.

>[!NOTE]
>
>Queste funzioni sono disponibili solo per at.js versione 1.Solo *x*. Queste funzioni sono state rimosse con il rilascio di at.js 2.x. Restituiscono il contenuto predefinito se utilizzate con at.js 2.x.

`mboxDefine()` e `mboxCreate()` sono legate agli elementi DIV HTML in cui l’offerta deve essere visualizzata. Questi elementi DIV HTML devono avere la classe `mboxDefault`. Se gli elementi HTML non hanno questa classe collegata, è possibile che venga visualizzato momentaneamente altro contenuto.

## mboxDefine {#section_134BAAE8EE9D49D8BAFEA5E7EAB93BA7}

Crea una mappatura interna tra un nodeId e un nome mbox, ma non esegue la richiesta. Utilizzato in combinazione con `mboxUpdate()`. Incorporato in [!DNL at.js] principalmente per facilitare la transizione da [!DNL mbox.js] (ora obsoleto) in [!DNL at.js].

## mboxUpdate {#section_D20B3E551884452A996305C12D5959D5}

Esegue la richiesta e applica l&#39;offerta all&#39;elemento identificato da `nodeId` in `mboxDefine()`. Può essere utilizzato anche per aggiornare una mbox iniziata da `mboxCreate`. Incorporato in [!DNL at.js] principalmente per facilitare la transizione da [!DNL mbox.js] (ora obsoleto) in [!DNL at.js]. `mboxDefine()`/ `mboxUpdate()` potrebbe essere sostituito da [adobe.target.getOffer()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffer/){target=_blank} e [adobe.target.applyOffer(){target=_blank}](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-applyoffer/){target=_blank} utilizzando l&#39;opzione del selettore.

## Esempio {#section_9C1E75D9E4BA4DC7879D2B69877EB01A}

```javascript
<div id="someId" class="mboxDefault"></div> 
<script> 
 mboxDefine('someId','mboxName','param1=value1','param2=value2'); 
 mboxUpdate('mboxName','param3=value3','param4=value4'); 
</script>
```