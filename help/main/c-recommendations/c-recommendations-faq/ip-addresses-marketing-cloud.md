---
keywords: indirizzo IP;indirizzi IP;whitelist;elenco Consentiti;firewall;consigli;feed;server;Adobe Experience Cloud;consigli;recommendations
description: Visualizza un elenco di indirizzi IP utilizzati nei server di elaborazione dei feed di  [!DNL Target]  Recommendations per configurare il firewall in modo da autorizzare gli indirizzi IP provenienti dai server di Adobe.
title: Quali indirizzi IP utilizzano i server di elaborazione dei feed della funzione Recommendations (Consigli)?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: a666cfc4-ed74-44e8-9ff5-212e4fd65c03
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 100%

---

# Indirizzi IP utilizzati dai server di elaborazione dei feed della funzionalità per i consigli (Recommendations)

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
