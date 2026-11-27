---
keywords: Targeting;eec;compositore esperienza visiva;risoluzione dei problemi compositore esperienza avanzato;risoluzione dei problemi
description: Scopri come risolvere i problemi che a volte si verificano nel [!DNL Adobe Target] [!UICONTROL Compositore esperienza avanzato] (EEC) in determinate condizioni.
title: Come posso risolvere i problemi relativi a [!UICONTROL Compositore esperienza avanzato]?
feature: Visual Experience Composer (VEC)
exl-id: 7dea7707-5d9f-49c4-9ccd-618eeb7b3568
TQID: 'https://experienceleague.adobe.com/Yan2cKWjs-u9JHQzT-PiRAFdxUJa1JSHS-fT68yxIjg'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 5%
---
# Risoluzione dei problemi relativi a [!UICONTROL Compositore esperienza avanzato] {#eec-issues}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come risolvere i problemi che interessano solo il **[!UICONTROL Compositore esperienza avanzato]** (EEC), ad esempio le pagine che non vengono caricate perché gli indirizzi IP del proxy EEC sono bloccati.

>[!ENDSHADEBOX]

In determinate condizioni in [!DNL Adobe Target] **[!UICONTROL Compositore esperienza avanzato]** (EEC) si verificano a volte problemi di visualizzazione. Gli elementi seguenti descrivono i problemi che interessano solo il Compositore esperienza avanzato e come risolverli.

## Inserire nell&#39;elenco Consentiti gli indirizzi IP del proxy EEC {#eec-ip-addresses}

Il Compositore esperienza avanzato non carica un URL di controllo qualità interno che non è accessibile su un indirizzo IP pubblico. Per risolvere il problema, è necessario Inserire nell&#39;elenco Consentiti gli indirizzi IP del server [!DNL Adobe] utilizzato per il proxy EEC. Questi indirizzi IP sono necessari solo per la modifica delle attività e i visitatori del sito non ne hanno bisogno per essere inseriti nell&#39;elenco Consentiti. Chiedi al team IT di inserire nell&#39;elenco Consentiti i seguenti indirizzi IP.

### Stati Uniti (va7)

```
40.70.154.136/29
52.254.106.240/28
52.254.106.160/28
52.254.107.16/28
20.186.185.181
20.22.83.112
20.186.185.227
52.254.106.192/28
52.254.106.0/28
52.254.107.128/28
52.254.107.80/28
52.254.106.176/28
52.254.107.32/28
52.254.105.192/28
52.254.107.64/28
52.254.106.208/28
52.254.107.0/28
52.254.106.224/28
20.14.241.153
20.186.185.239
4.152.211.251
52.254.107.144/28
52.254.106.144/28
```

### EMEA (nld2)

```
51.138.17.16/28
51.138.17.48/28
51.138.16.128/28
51.138.17.32/28
51.138.16.240/28
51.138.17.112/28
51.138.16.160/28
51.138.16.208/28
51.138.17.80/28
51.138.17.0/28
51.138.17.96/28
51.138.16.144/28
20.31.145.248
20.126.189.248
51.138.16.224/28
51.138.16.192/28
51.138.12.94
51.138.12.11
51.138.16.176/28
51.138.12.100
51.138.17.64/28
51.138.12.160/28
```

### APAC (aus)

```
20.43.104.160/28
20.227.35.177
20.40.188.227
20.43.104.112/28
20.43.104.128/28
20.43.104.144/28
20.40.188.166
20.53.206.128
20.43.104.80/28
20.43.104.16/28
20.43.105.48/28
20.43.104.96/28
20.43.104.48/28
20.40.188.194
20.43.104.32/28
20.40.191.224/28
20.43.105.16/28
20.40.191.96/28
20.43.104.176/28
20.40.191.240/28
20.43.104.64/28
20.43.105.32/28
20.43.104.192/28
20.43.105.0/28
20.43.104.0/28
```

### Indirizzi IP legacy

I seguenti indirizzi IP legacy devono continuare a essere inseriti nell&#39;elenco Consentiti fino a nuovo avviso.

```
34.254.77.200
54.73.207.147
54.229.152.123
3.224.194.242
54.90.51.39
34.228.136.112
54.150.116.11
18.178.142.8
54.199.107.77
99.80.139.221
54.78.56.224
54.247.179.246
54.80.219.243
34.201.235.54
54.196.224.236
35.75.212.45
52.199.184.130
18.180.161.176
```

+++ Il Compositore esperienza avanzato visualizza un messaggio di errore che indica che il dominio del sito Web lo sta bloccando

Il seguente messaggio di errore può essere visualizzato in [!DNL Target]:

`Error: Your website domain (ISP) is blocking the Enhanced Experience Composer. You can allowlist the Enhanced Experience Composer's IP addresses or turn off Enhanced Experience Composer in Configure > Page Delivery menu.`

![Compositore esperienza con il messaggio di errore che il dominio del sito Web (ISP) sta bloccando il Compositore esperienza avanzato, con un suggerimento per inserire nell&#39;elenco Consentiti gli indirizzi IP o disattivare il Compositore nel menu Configura consegna pagine](assets/EEC_error.png).

Questo messaggio di errore ha due possibili cause:

* Il dominio del sito web (ISP) blocca il Compositore esperienza avanzato. Per risolvere il problema, inserire nell&#39;elenco Consentiti gli indirizzi IP elencati in [Inserire nell&#39;elenco Consentiti gli indirizzi IP del proxy EEC](#eec-ip-addresses).
* Gli indirizzi IP vengono inseriti nell&#39;elenco Consentiti, ma il sito Web non supporta TLS 1.2. Per risolvere il problema, vedi la voce seguente.

+++

+++ Il Compositore esperienza avanzato non viene caricato su pagine sicure di un sito che utilizza TLS 1.0

Il messaggio di errore descritto nell’elemento precedente può essere visualizzato quando gli indirizzi IP vengono inseriti nell&#39;elenco Consentiti ma il sito web non supporta TLS 1.2. [!DNL Target] utilizza attualmente la versione 1.2 come configurazione predefinita. Prima di [!DNL Target] 18.4.1 (25 aprile 2018), la configurazione predefinita supportava TLS 1.0. Per ulteriori informazioni, consulta [Modifiche alla crittografia TLS](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank}.

Per controllare la versione TLS di un sito web in Firefox (altri browser hanno passaggi simili):

1. Apri il sito interessato in Firefox.
1. Fai clic sull&#39;icona **[!UICONTROL Mostra informazioni sito]** nella barra degli indirizzi del browser.

   ![Barra degli indirizzi di Firefox con l&#39;icona Mostra informazioni sito evidenziata a sinistra dell&#39;URL](assets/firefox_more_info.png)

1. Fai clic su **[!UICONTROL Mostra dettagli di connessione]** > **[!UICONTROL Ulteriori informazioni]**.

   ![Pannello informazioni sito Firefox con la freccia Mostra dettagli connessione evidenziata accanto a Connessione protetta](assets/firefox_more_info_2.png)

1. Esaminare le informazioni sulla versione di TLS in **[!UICONTROL Dettagli tecnici]**.

   ![Finestra Informazioni pagina Firefox, scheda Sicurezza, con la versione di TLS evidenziata in Dettagli tecnici](assets/firefox_more_info_3.png)

1. Se il sito Web mostra TLS 1.0, vedere [Modifiche alla crittografia di TLS (Transport Layer Security)](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank} per informazioni sui criteri di supporto TLS di [!DNL Target]. Per risolvere la situazione (valido fino al 12 settembre 2018), rivolgiti a [Assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) per la configurazione con la versione di TLS e il dominio.

+++

+++ Timeout o errori di &quot;accesso negato&quot; vengono visualizzati quando i siti vengono caricati con il proxy abilitato

Assicurati che gli indirizzi IP proxy non siano bloccati nell’ambiente. Gli indirizzi sono elencati in [Inserire nell&#39;elenco Consentiti gli indirizzi IP del proxy EEC](#eec-ip-addresses).

+++
