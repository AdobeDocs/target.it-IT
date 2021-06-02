---
keywords: indirizzo IP;indirizzi IP;whitelist;elenco Consentiti;firewall;consigli;feed;server;Adobe Experience Cloud;consigli;recommendations
description: Visualizza un elenco di indirizzi IP utilizzati nei server di elaborazione dei feed di  [!DNL Target]  Recommendations per configurare il firewall in modo da autorizzare gli indirizzi IP provenienti dai server di Adobe.
title: Quali indirizzi IP utilizzano i server di elaborazione dei feed della funzione Recommendations (Consigli)?
feature: Recommendations
exl-id: a666cfc4-ed74-44e8-9ff5-212e4fd65c03
translation-type: ht
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: ht
source-wordcount: '137'
ht-degree: 100%

---

# ![PREMIUM](/help/assets/premium.png) Indirizzi IP utilizzati dai server di elaborazione dei feed della funzionalità per i consigli (Recommendations)

Visualizza un elenco di indirizzi IP utilizzati nei server di elaborazione dei feed di [!DNL Adobe Target] [!DNL Recommendations] per configurare il firewall in modo da autorizzare gli indirizzi IP provenienti dai server di Adobe.

Le attività [!DNL Target] [!UICONTROL Recommendations] (Consigli) utilizzano i seguenti host AWS per accedere ai server FTP dei clienti:

| Posizione | Host |
| --- | --- |
| Oregon | `44.241.237.28` |
| Oregon | `44.232.167.82` |
| Oregon | `52.41.252.205` |

Anche le API di [!DNL Target] [!UICONTROL Recommendations] utilizzano gli stessi host AWS.

>[!NOTE]
>
>Questi indirizzi IP sono stati aggiornati il 16 marzo 2021. In precedenza, i server che accedevano ai server FTP erano nel blocco CIDR dell’indirizzo IP 192.243.242.0/24. I server che ospitano le API di Recommendations si trovavano nel blocco CIDR dell’indirizzo IP 192.243.224.0/20.
