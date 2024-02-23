---
keywords: indirizzo IP;indirizzi IP;whitelist;elenco Consentiti;firewall;consigli;feed;server;Adobe Experience Cloud;consigli;recommendations
description: Visualizza un elenco di indirizzi IP utilizzati nei server di elaborazione dei feed di  [!DNL Target]  Recommendations per configurare il firewall in modo da autorizzare gli indirizzi IP provenienti dai server di Adobe.
title: Quali indirizzi IP utilizzano i server di elaborazione dei feed della funzione Recommendations (Consigli)?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Recommendations
exl-id: a666cfc4-ed74-44e8-9ff5-212e4fd65c03
source-git-commit: 558de92e672c276474bc76fad19e5461ae7d4c88
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 49%

---

# Indirizzi IP utilizzati da [!DNL Recommendations] server di elaborazione dei feed

Elenco di indirizzi IP utilizzati in [!DNL Adobe Target] [!DNL Recommendations] server di elaborazione dei feed per configurare il firewall in modo da autorizzare gli indirizzi IP provenienti da [!DNL Adobe] server.

>[!IMPORTANT]
>
>23 febbraio 2023: The [!DNL Target] Il team sta aggiornando gli indirizzi gateway NAT per il download [!DNL Recommendations] feed. Se implementi l’IP, assicurati di inserire nell&#39;elenco Consentiti inserire nell&#39;elenco Consentiti i seguenti nuovi host AWS. In futuro è prevista la disattivazione degli host esistenti. Tutti e nove gli host sono ora operativi.

Le attività [!DNL Target] [!UICONTROL Recommendations] (Consigli) utilizzano i seguenti host AWS per accedere ai server FTP dei clienti:

**Nuovi host**:

| Posizione | Host |
| --- | --- |
| Oregon | `52.40.124.129` |
| Oregon | `54.148.219.69` |
| Oregon | `54.189.208.212` |
| Oregon | `44.230.236.35` |
| Oregon | `54.190.78.243` |
| Oregon | `52.41.73.133` |

**Host esistenti**:

| Posizione | Host |
| --- | --- |
| Oregon | `44.241.237.28` |
| Oregon | `44.232.167.82` |
| Oregon | `52.41.252.205` |

Anche le API di [!DNL Target] [!UICONTROL Recommendations] utilizzano gli stessi host AWS.
