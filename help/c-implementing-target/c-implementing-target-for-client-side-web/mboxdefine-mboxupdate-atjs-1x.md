---
description: 'Informazioni sulle funzioni mboxdefine () e mboxupdate () per at. js. '
keywords: adobe.target.notification;element;selector;notification;extension
seo-description: Informazioni sulle funzioni mboxdefine () e mboxupdate () per la libreria javascript di Adobe Target nella libreria javascript. js.
seo-title: Informazioni sulle funzioni mboxdefine () e mboxupdate () per la libreria javascript di Adobe Target nella libreria javascript. js.
solution: Target
subtopic: Introduzione
title: mboxDefine() e mboxUpdate() - at.js 1.x
topic: Standard
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# mboxDefine() e mboxUpdate() - at.js 1.x

Definire e aggiornare una mbox in Adobe Target.

>[!NOTE]
>
>Queste funzioni sono disponibili per at.js versione 1.Solo *x*. Queste funzioni sono state dichiarate obsolete con il rilascio di at. js 2. x. Queste funzioni restituiscono il contenuto predefinito se utilizzato con at. js 2. x.

`mboxDefine()` e `mboxCreate()` sono legate agli elementi DIV HTML in cui l’offerta deve essere visualizzata. Questi elementi DIV HTML devono avere la classe `mboxDefault`. Se gli elementi HTML non hanno questa classe collegata, è possibile che venga visualizzato momentaneamente altro contenuto.

## mboxDefine  {#section_134BAAE8EE9D49D8BAFEA5E7EAB93BA7}

Crea una mappatura interna tra un nodeId e un nome mbox, ma non esegue la richiesta. Utilizzato in combinazione con `mboxUpdate()`. Incorporata in [!DNL at.js]per lo più per facilitare la transizione da [!DNL mbox.js] ad [!DNL at.js].

## mboxUpdate {#section_D20B3E551884452A996305C12D5959D5}

Esegue la richiesta e applica l&#39;offerta all&#39;elemento identificato da `nodeId` in `mboxDefine()`. Può essere utilizzato anche per aggiornare una mbox iniziata da `mboxCreate`. Incorporata in [!DNL at.js] per lo più per facilitare la transizione da [!DNL mbox.js] ad [!DNL at.js]. `mboxDefine()`/ `mboxUpdate()` può essere sostituito da [adobe. target. getoffer ()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffer.md) e [adobe. target. applyoffer ()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-applyoffer.md) mediante l&#39;opzione del selettore.

## Esempio {#section_9C1E75D9E4BA4DC7879D2B69877EB01A}

```
<div id="someId" class="mboxDefault"></div> 
<script> 
 mboxDefine('someId','mboxName','param1=value1','param2=value2'); 
 mboxUpdate('mboxName','param3=value3','param4=value4'); 
</script>
```
