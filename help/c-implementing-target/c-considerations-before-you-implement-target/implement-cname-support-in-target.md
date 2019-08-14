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
source-git-commit: d21838bdf17327b394f6e3106ea5ce4bc72605e6

---


# CNAME e Adobe Target{#cname-and-adobe-target}

Informazioni sull'utilizzo di Adobe Client Care per implementare il supporto CNAME (Canonical Name) in Adobe Target. Per gestire in modo ottimale i problemi di blocco degli annunci, viene utilizzato un CNAME che consente di effettuare chiamate a un dominio di proprietà del cliente anziché di un dominio di proprietà di Adobe.

Esegui la procedura seguente per richiedere il supporto CNAME in Target:

1. Apri una [Segnalazione per l’Assistenza clienti](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) per richiedere il supporto CNAME per le chiamate Adobe Target.
1. Registrarsi al [programma Adobe Managed Certificate (AMC)](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/adobe_managed_cert_pgm.html) e seguire le istruzioni di implementazione fornite nella guida sui [!DNL Adobe Analytics]*cookie di prima parte.* [!DNL Target] utilizza lo stesso metodo utilizzato dal supporto [!DNL Analytics] CNAME.

   Il programma AMC aiuta a semplificare l’implementazione dei cookie di prima parte. Dopo la registrazione a questo programma, Adobe acquisterà e rilascerà il certificato da installare su server sicuri.

   >[!NOTE]
   >
   >CNAME deve essere configurato prima di iscriversi al programma AMC.

1. Dopo aver completato le attività precedenti, devi aggiornare il `serverDomain` nuovo CNAME in at. js.

## Video formazione: Cookie di prime parti e Utilizzo dei certificati gestiti Adobe

This video is a recording of [Office Hours](/help/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7), an initiative led by the Adobe Customer Care team. La discussione del programma di certificato gestito Adobe inizia da 10:21.

[Adobe Analytics: Cookie di prime parti e Utilizzo dei certificati gestiti Adobe](https://helpx.adobe.com/customer-care-office-hours/analytics/first-party-cookies-adobe-managed-certificates.html)
