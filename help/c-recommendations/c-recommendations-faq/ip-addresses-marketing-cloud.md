---
keywords: Indirizzo IP;indirizzi IP;whitelist;inserire nell'elenco Consentiti;firewall;recs;feed;server;adobe marketing cloud;consigli
description: Visualizza un elenco di indirizzi IP utilizzati nei server di elaborazione dei feed Recommendations di Target per consentirti di configurare il firewall per l’autorizzazione degli indirizzi IP provenienti dai server di Adobe.
title: Quali indirizzi IP utilizzano i server di elaborazione dei feed Recommendations?
feature: Consigli
translation-type: tm+mt
source-git-commit: 55b246f5f0d660e6c4f71352c5b638347d55ac28
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 13%

---


# ![PREMIUM](/help/assets/premium.png) Indirizzi IP utilizzati dai server di elaborazione dei feed della funzionalità per i consigli (Recommendations)

Elenco di indirizzi IP utilizzati nei server di elaborazione dei feed [!DNL Adobe Target] [!DNL Recommendations] per consentirti di configurare il firewall per l’autorizzazione degli indirizzi IP provenienti dai server di Adobe.

[!DNL Target]  Le attività Consigli utilizzano i seguenti indirizzi IP per accedere ai server FTP dei clienti:

| Notazione CIDR |
|---|
| 44.241.237.28/32 |
| 44.232.167.82/32 |
| 52.41.252.205/32 |

[!DNL Target]  Le API di Recommendations utilizzano i seguenti indirizzi IP:

| Notazione CIDR |
|---|
| 44.241.237.28/32 |
| 44.232.167.82/32 |
| 52.41.252.205/32 |

>[!NOTE]
>
>Questi indirizzi IP sono stati aggiornati da ultimo il 16 marzo 2021. In precedenza, i server che accedevano ai server FTP erano nel blocco CIDR dell&#39;indirizzo IP 192.243.242.0/24. I server che ospitano le API Recommendations si trovavano nel blocco CIDR dell’indirizzo IP 192.243.224.0/20.

