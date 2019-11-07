---
keywords: client care;cname;certificate program;canonico name;cookies;certificate;amc;adobe manage certificate
description: Informazioni sull’utilizzo di Adobe Client Care per implementare il supporto CNAME (Canonical Name) in Adobe Target.
title: CNAME e Adobe Target
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# CNAME e Adobe Target {#cname-and-adobe-target}

Informazioni sull’utilizzo di Adobe Client Care per implementare il supporto CNAME (Canonical Name) in [!DNL Target]. Per gestire al meglio i problemi di blocco degli annunci o i criteri dei cookie relativi a ITP, viene utilizzato un CNAME per cui le chiamate vengono effettuate a un dominio di proprietà del cliente anziché a un dominio di proprietà di Adobe.

Esegui la procedura seguente per richiedere il supporto CNAME in [!DNL Target]:

1. Open a [Customer Care ticket requesting CNAME support](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) for your [!DNL Target] calls.

1. Creare record CNAME (vedere le istruzioni riportate di seguito).

   Dopo aver ricevuto il biglietto, uno specialista FPSSL dovrebbe fornirvi un paio di record CNAME. Questi record devono essere configurati sul server DNS della società prima che Adobe possa acquistare il certificato per conto dell'utente.

   I CNAME saranno simili al seguente esempio:

   `DNS record: metrics.example.com IN CNAME metricsexample-fpssl.tt.omtrdc.net`

1. Una volta installati questi CNAME, Adobe collaborerà con DigiCert per acquistare e installare un certificato sui server di produzione Adobe.

1. Dopo aver completato le attività precedenti, in at.js devi aggiornare `serverDomain` al nuovo CNAME.
