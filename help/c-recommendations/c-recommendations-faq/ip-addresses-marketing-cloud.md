---
keywords: Indirizzo IP;indirizzi IP;whitelist;inserire nell'elenco Consentiti;firewall;recs;feed;server;adobe marketing cloud;consigli
description: Visualizza un elenco di indirizzi IP utilizzati nei server di elaborazione dei feed Recommendations di Target per consentirti di configurare il firewall per l’autorizzazione degli indirizzi IP provenienti dai server di Adobe.
title: Quali indirizzi IP utilizzano i server di elaborazione dei feed Recommendations?
feature: Recommendations
translation-type: tm+mt
source-git-commit: d90069169a23bc432c7731b3129ca7c9572f6cf4
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 7%

---


# ![PREMIUM](/help/assets/premium.png) Indirizzi IP utilizzati dai server di elaborazione dei feed della funzionalità per i consigli (Recommendations)

Elenco di indirizzi IP utilizzati nei server di elaborazione dei feed [!DNL Adobe Target] [!DNL Recommendations] per consentirti di configurare il firewall per l’autorizzazione degli indirizzi IP provenienti dai server di Adobe.

[!DNL Target]  Le attività Consigli utilizzano i seguenti host AWS per accedere ai server FTP dei clienti:

| Posizione | Host |
| --- | --- |
| Oregon | `44.241.237.28` |
| Oregon | `44.232.167.82` |
| Oregon | `52.41.252.205` |

[!DNL Target]  Le API di Recommendations utilizzano anche gli stessi host AWS.

>[!NOTE]
>
>Questi indirizzi IP sono stati aggiornati da ultimo il 16 marzo 2021. In precedenza, i server che accedevano ai server FTP erano nel blocco CIDR dell&#39;indirizzo IP 192.243.242.0/24. I server che ospitano le API Recommendations si trovavano nel blocco CIDR dell’indirizzo IP 192.243.224.0/20.

