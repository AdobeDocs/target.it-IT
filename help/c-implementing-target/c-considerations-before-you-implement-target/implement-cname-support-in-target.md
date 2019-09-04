---
description: Informazioni sull'utilizzo di Adobe Client Care per implementare il supporto CNAME (Canonical Name) in Adobe Target.
keywords: client care;cname;programma di certificato;canonical name;cookie;certificato; amc; certificato gestito adobe
seo-description: Informazioni sull'utilizzo di Adobe Client Care per implementare il supporto CNAME (Canonical Name) in Adobe Target.
seo-title: CNAME e Adobe Target
solution: Target
title: CNAME e Adobe Target
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
translation-type: tm+mt
source-git-commit: b7a80326b0b89f6fe3bac70ccc6941be09d14ac1

---


# CNAME e Adobe Target {#cname-and-adobe-target}

Informazioni sull’utilizzo di Adobe Client Care per implementare il supporto CNAME (Canonical Name) in [!DNL Target]. Per gestire meglio i problemi di blocco degli annunci, o i criteri dei cookie correlati ITP, viene utilizzato un CNAME che consente di effettuare chiamate a un dominio di proprietà del cliente anziché di un dominio di proprietà di Adobe.

Esegui la procedura seguente per richiedere il supporto CNAME in [!DNL Target]:

1. Open a [Customer Care ticket requesting CNAME support](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) for your [!DNL Target] calls.

1. Creare record CNAME (consultate le istruzioni di seguito).

   Quando ricevi il ticket, uno specialista FPSSL deve fornire una coppia di record CNAME. Questi record devono essere configurati sul server DNS della tua azienda prima che Adobe possa acquistare il certificato per conto tuo.

   I CNAME saranno simili al seguente esempio:

   `DNS record: metrics.example.com IN CNAME metricsexample-fpssl.tt.omtrdc.net`

1. Quando questi CNAME saranno attivi, Adobe collaborerà con digicert per acquistare e installare un certificato sui server di produzione di Adobe.

1. Dopo aver completato le attività precedenti, devi aggiornare il `serverDomain` nuovo CNAME in at. js.
