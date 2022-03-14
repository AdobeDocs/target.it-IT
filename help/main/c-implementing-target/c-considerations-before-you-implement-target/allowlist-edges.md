---
keywords: implementare;implementazione;whitelist;whitelist;white list;inserire nell'elenco Consentiti;elenco consentiti;edge;edge
description: Visualizza un elenco di host per aiutarti inserire nell'elenco Consentiti Adobe [!DNL Target] edge (nodi di servizio distribuiti geograficamente che garantiscono tempi di risposta ottimali agli utenti finali).
title: Come Inserire nell'elenco Consentiti [!DNL Target] Nodi Edge?
feature: Privacy & Security
role: Developer
exl-id: 2d8399b9-eec8-40b0-8b35-2812f83ff4dc
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 6%

---

# Inserire nell&#39;elenco Consentiti [!DNL Target] nodi edge

Informazioni e un elenco aggiornato di host per aiutarti a inserire nell&#39;elenco Consentiti [!DNL Adobe Target] bordi.

Un edge è un’architettura di servizio geograficamente distribuita che garantisce agli utenti finali che richiedono contenuti in tempi di risposta ottimali, indipendentemente da dove si trovano. Ogni nodo perimetrale dispone di tutte le informazioni necessarie per rispondere alla richiesta di contenuto dell’utente e per tenere traccia dei dati di analisi relativi a tale richiesta. Le richieste degli utenti vengono indirizzate al nodo perimetrale più vicino. Per ulteriori informazioni, consulta [La rete Edge](/help/main/c-intro/how-target-works.md#concept_0AE2ED8E9DE64288A8B30FCBF1040934) in *Adobe [!DNL Target] lavori*.

Puoi inserire nell&#39;elenco Consentiti [!DNL Target] nodi edge, se necessario.

## Indirizzi IP NAT (Network Address Translation) di [!DNL Target] bordi

Elenco degli indirizzi IP in uscita di [!DNL Target] bordi. Inserire nell&#39;elenco Consentiti questi IP se intendi far sì che Target raggiunga i tuoi servizi.

| Posizione Edge | Indirizzi IP Egress |
| --- | --- |
| Edge31 (Mumbai) | 13.126.131.246<br>13,234,229,8 |
| Edge32 (Tokyo) | 3.115.154.28<br>3.115.227.146 |
| Edge34 (Stati Uniti) | 34.232.149.249<br>52.21.139.93 |
| Edge35 (costa occidentale USA) | 52.10.11.139<br>44.231.171.161 |
| Edge36 (Sydney) | 13.237.227.20<br>13.210.93.142 |
| Edge37 (Irlanda) | 54.72.21.68<br>52.208.139.19 |
| Edge38 (Singapore) | 18.141.132.96<br>54.179.187.167 |

## Indirizzi IP edge di Target

Elenco degli indirizzi IP di [!DNL Target] bordi. Inserire nell&#39;elenco Consentiti questi IP se desideri effettuare chiamate API ai bordi di Target.

| Posizione Edge | Dominio | Indirizzi IP |
| --- | --- | --- |
|  | `CLIENTCODE.tt.omtrdc.net`<br>(dove CLIENTCODE è il tuo [!DNL Target] ID client) |  |
| Edge31 (Mumbai) | `mboxedge31.tt.omtrdc.net` | 15.207.157.131<br>15.206.8.201 |
| Edge32 (Tokyo) | `mboxedge32.tt.omtrdc.net` | 54.199.66.101<br>54.64.93.37 |
| Edge34 (Stati Uniti) | `mboxedge34.tt.omtrdc.net` | 3 225 56 36<br>3.230.207.249<br>34.198.55.51<br>52.3.14.12<br>52.21.222.93<br>52.55.235.132<br>52.70.52.52<br>54.165.204.89 |
| Edge35 (costa occidentale USA) | `mboxedge35.tt.omtrdc.net` | 52.10.244.20<br>52,36,232,38<br>52.88.209.29<br>54.214.180.56<br>35.162.74.35<br>34.214.12.211<br>52.42.35.202<br>54.148.71.13 |
| Edge36 (Sydney) | `mboxedge36.tt.omtrdc.net` | 13.238.34.185<br>3.24.250.17<br>3.104.234.91<br>13.211.248.241 |
| Edge37 (Irlanda) | `mboxedge37.tt.omtrdc.net` | 52.212.193.208<br>52.19.133.54<br>52.51.251.137<br>34.252.156.174<br>52.213.168.74<br>34,252,166,160<br>52.18.150.20<br>18.203.205.32 |
| Edge38 (Singapore) | `mboxedge38.tt.omtrdc.net` | 52.221.145.65<br>52 220 44 99<br>13.250.75.226<br>54.151.139.123 |
