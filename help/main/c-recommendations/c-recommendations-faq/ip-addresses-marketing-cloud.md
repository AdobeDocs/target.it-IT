---
keywords: indirizzo IP;indirizzi IP;whitelist;elenco Consentiti;firewall;consigli;feed;server;Adobe Experience Cloud;consigli;recommendations
description: Visualizza un elenco di indirizzi IP utilizzati nei server di elaborazione dei feed di  [!DNL Target]  Recommendations per configurare il firewall in modo da autorizzare gli indirizzi IP provenienti dai server di Adobe.
title: Quali indirizzi IP utilizzano i server di elaborazione dei feed della funzione Recommendations (Consigli)?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Recommendations
exl-id: a666cfc4-ed74-44e8-9ff5-212e4fd65c03
source-git-commit: be5b3158c758fa08802c1dc0541c9e989a2c7740
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 46%

---

# Indirizzi IP utilizzati da [!DNL Recommendations] server di elaborazione dei feed

Elenco di indirizzi IP utilizzati in [!DNL Adobe Target] [!DNL Recommendations] server di elaborazione dei feed per configurare il firewall in modo da autorizzare gli indirizzi IP provenienti da [!DNL Adobe] server.

>[!IMPORTANT]
>
>Il [!DNL Target] Il team sta aggiornando gli indirizzi gateway NAT per il download [!DNL Recommendations] feed. Se implementi l’IP, assicurati di inserire nell&#39;elenco Consentiti inserire nell&#39;elenco Consentiti i seguenti nuovi host AWS. La disattivazione degli host esistenti è prevista per il 30 giugno 2024. Per garantire una transizione fluida, inserisce nell&#39;elenco Consentiti tutti e nove gli indirizzi di, in quanto tutti i messaggi sono stati inseriti in un unico file. Non vi è alcuna urgenza di rimuovere gli indirizzi esistenti.

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
