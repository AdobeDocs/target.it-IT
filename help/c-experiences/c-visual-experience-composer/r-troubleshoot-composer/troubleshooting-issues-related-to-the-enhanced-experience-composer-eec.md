---
keywords: Targeting;eec;visual experience composer;troubleshoot enhanced experience composer;troubleshooting
description: In determinate condizioni in Compositore esperienza avanzato si verificano a volte problemi di visualizzazione.
title: Risoluzione dei problemi relativi al Compositore esperienza avanzato
feature: vec
uuid: 2ea9a91f-08ca-4a06-ad5d-35ced140db14
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 71%

---


# Risoluzione dei problemi relativi al Compositore esperienza avanzato{#troubleshooting-issues-related-to-the-enhanced-experience-composer}

In determinate condizioni in Compositore esperienza avanzato si verificano a volte problemi di visualizzazione.

## Il Compositore esperienza avanzato non carica un URL di controllo qualità interno che non è accessibile su IP pubblico. (Solo Compositore esperienza avanzato) {#section_D29E96911D5C401889B5EACE267F13CF}

Questo problema può essere risolto  inserire nell&#39;elenco Consentiti i seguenti indirizzi IP. Si tratta degli indirizzi IP per il server Adobe utilizzato per il proxy del Compositore esperienza avanzato. Sono necessari solo per modificare le attività. I visitatori del sito non necessitano di questi indirizzi IP inseriti nell&#39;elenco Consentiti

Chiedete al team IT di  inserire nell&#39;elenco Consentiti i seguenti indirizzi IP:

| Area geografica | Indirizzi IP | Nomi host |
|--- |--- |--- |
| Stati Uniti | 52.55.99.45 | `us1-proxy.adobemc.com` |
| Europa, Medio Oriente e Africa (EMEA) | 52.51.238.221 | `emea1-proxy.adobemc.com` |
| Asia-Pacifico (APAC) | 52.193.67.35 | `apac1-proxy.adobemc.com` |

È possibile visualizzare il seguente messaggio di errore in Target:

`Error: Your website domain (ISP) is blocking the Enhanced Experience Composer. You can allowlist the Enhanced Experience Composer's IP addresses or turn off Enhanced Experience Composer in [!UICONTROL Configure] > [!UICONTROL Page Delivery] menu.`

![](assets/EEC_error.png)

Di seguito sono riportati possibili cause per questo messaggio di errore e soluzioni per correggere la situazione:

* **Problema:** il dominio del sito Web (ISP) sta bloccando il Compositore esperienza avanzato.

   **Rimedio:**   gli indirizzi IP elencati sopra.

* **Problema:** Gli indirizzi IP vengono inseriti nell&#39;elenco Consentiti, ma il sito Web non supporta TLS versione 1.2. In Target è attualmente utilizzata la configurazione predefinita di 1.2. Prima di Target 18.4.1 (25 aprile 2018), la configurazione predefinita supportava TLS 1.0. Per ulteriori informazioni, consultate Modifiche [alla crittografia](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451)TLS (Transport Layer Security).

   **Soluzione:** consulta la domanda seguente (il Compositore esperienza visivo avanzato non viene caricato su pagine protette del mio sito che utilizzano TLS 1.2).

## Il Compositore esperienza avanzato non viene caricato su pagine protette del mio sito che utilizzano TLS 1.0. (Solo Compositore esperienza avanzato) {#section_C5B31E3D32A844F68E5A8153BD17551F}

È possibile che venga visualizzato il messaggio di errore descritto in precedenza al punto “Il Compositore esperienza visivo avanzato non viene caricato su pagine sicure del mio sito” if the above IP addresses are allowlisted but your website does not support TLS version 1.2. Target currently uses the default configuration of 1.2. Prior to the Target 18.4.1 (April 25, 2018), the default configuration supported TLS 1.0. For more information, see [TLS (Transport Layer Security) Encryption Changes](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451).

Per controllare la versione TLS sul tuo sito web con Firefox (altri browser hanno passaggi simili):

1. Apri il sito interessato in Firefox.
1. Fai clic sull&#39;icona **[!UICONTROL Mostra informazioni del sito]** nella barra degli indirizzi del browser.

   ![](assets/firefox_more_info.png)

1. Fai clic su **[!UICONTROL Mostra dettagli di connessione]** > **[!UICONTROL Ulteriori informazioni]**.

   ![](assets/firefox_more_info_2.png)

1. Verifica la versione di TLS alla voce Dettagli tecnici:

   ![](assets/firefox_more_info_3.png)

1. Se scopri che il tuo sito web visualizza TLS 1.0, consulta: [Modifiche alla crittografia di TLS (Transport Layer Security)](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451) per informazioni sull’informativa sul supporto per TLS di Target. Per risolvere la situazione (valido fino al 12 settembre 2018), rivolgiti all’[Assistenza clienti](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) per la configurazione con la versione di TLS e il dominio.

## Ricevo errori di timeout o “accesso negato” durante il caricamento di siti con proxy abilitato. (Solo Compositore esperienza avanzato) {#section_60CBB9022DC449F593606C0E6252302D}

Assicurati che nel tuo ambiente gli IP proxy non siano bloccati.
