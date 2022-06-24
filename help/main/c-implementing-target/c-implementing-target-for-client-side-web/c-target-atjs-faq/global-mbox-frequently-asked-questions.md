---
keywords: risoluzione problemi;domande frequenti;FAQ;domande e risposte;globale;mbox globale
description: Leggi le domande frequenti (FAQ) e le risposte sull’Adobe [!DNL Target] mbox globali.
title: Quali sono le domande frequenti sulla mbox globale?
feature: at.js
role: Developer
exl-id: ec8399df-5222-44bd-9e61-dfce8fd1694d
source-git-commit: 719eb95049dad3bee5925dff794871cd65969f79
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 60%

---

# Domande frequenti sulla mbox globale

Elenco delle domande frequenti sulle mbox globali.

## Posso avere più di una mbox globale se [!DNL Target] l&#39;account è impostato su più domini? {#section_B7252BA6C3BB4EF4AE9E53F47FD58ABD}

L&#39;account supporta un&#39;unica mbox globale.

Puoi definire un limite per l&#39;esecuzione delle attività aggiungendo a queste delle regole URL. Per ulteriori informazioni, consulta [Includere la stessa esperienza in pagine simili](/help/main/c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781).

Puoi anche trasmettere un parametro sulla pagina utilizzando [targetPageParams](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetpageparams/){target=_blank} e quindi seleziona questi parametri nella sezione &quot;configura URL&quot; nella sezione [!UICONTROL Compositore esperienza visivo] (VEC){target=_blank} o aggiungendo i parametri come &quot;perfezionamenti&quot; nel Compositore esperienza basato su moduli.

## Come faccio a trasferire i dati dei ricavi a un [!DNL Target] mbox globale? {#section_17AEA933BADA4D169CCEDF5833C41306}

Per raccogliere le informazioni su ricavi e ordini in target-global-mbox, è necessario inviare a Target i “parametri mbox”. Questi parametri sono coppie nome/valore utilizzate per inviare ulteriori informazioni a Target. In Target viene eseguita la ricerca automatica di tali parametri (nomi riservati) allo scopo di popolare i dati dei ricavi.

Per `orderConfirmPage`, è necessario trasmettere `orderTotal`, `orderId` e `productPurchasedId`.

Questi parametri devono essere inviati a target-global-mbox tramite `targetPageParams()`. Per ulteriori informazioni, consulta [Trasmissione di parametri a una mbox globale](https://developer.adobe.com/target/implement/client-side/atjs/global-mbox/pass-parameters-to-global-mbox/){target=_blank}.

Può essere utile aggiungere il targeting all’elemento di conversione, in modo che quando viene visualizzata la pagina di conferma vengano conteggiate in Target unicamente le conversioni su target-global-mbox, come mostrato di seguito:

![](assets/revenue1.png)

Nella sezione Pagine del sito sopra illustrata sono incluse le seguenti selezioni: Pagina corrente, URL, contiene, orderconfirm.

![](assets/revenue2.png)

Nelle opzioni dell’illustrazione precedente sono incluse le seguenti impostazioni:

* **Cosa desideri misurare con questa attività:** Ricavi.
* **Vista predefinita per rapporti:** Ricavo per visitatore (RPV).
* **Qual è l&#39;azione intrapresa dal pubblico per indicare che l&#39;obiettivo è stato raggiunto?** Visualizzazione di una Mbox, target-global-mbox
