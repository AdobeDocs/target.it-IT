---
keywords: indirizzo IP;indirizzi IP;whitelist;elenco Consentiti;firewall;consigli;feed;server;Adobe Experience Cloud;consigli;recommendations
description: Visualizza un elenco di indirizzi IP utilizzati nei server di elaborazione dei feed di  [!DNL Target]  Recommendations per configurare il firewall in modo da autorizzare gli indirizzi IP provenienti dai server di Adobe.
title: Quali indirizzi IP utilizzano i server di elaborazione dei feed della funzione Recommendations (Consigli)?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: a666cfc4-ed74-44e8-9ff5-212e4fd65c03
source-git-commit: be5b3158c758fa08802c1dc0541c9e989a2c7740
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 35%

---

# Indirizzi IP utilizzati da [!DNL Recommendations] server di elaborazione dei feed

Elenco di indirizzi IP utilizzati nei server di elaborazione dei feed [!DNL Adobe Target] di [!DNL Recommendations] per configurare il firewall per l&#39;autorizzazione degli indirizzi IP provenienti dai server [!DNL Adobe].

>[!IMPORTANT]
>
>Il team [!DNL Target] sta aggiornando gli indirizzi gateway NAT per il download di [!DNL Recommendations] feed. Inserire nell&#39;elenco Consentiti inserire nell&#39;elenco Consentiti Se implementi l’IP, assicurati di i seguenti nuovi host AWS. La disattivazione degli host esistenti è prevista per il 30 giugno 2024. Per garantire una transizione fluida, inserisce nell&#39;elenco Consentiti tutti e nove gli indirizzi. Non vi è alcuna urgenza di rimuovere gli indirizzi esistenti.

Le attività di [!DNL Target] [!UICONTROL Recommendations] utilizzano i seguenti host AWS per accedere ai server FTP dei clienti:

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
