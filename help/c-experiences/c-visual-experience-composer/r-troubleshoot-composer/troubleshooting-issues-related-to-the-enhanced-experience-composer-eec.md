---
keywords: Targeting;eec;compositore esperienza visiva;risoluzione dei problemi compositore esperienza avanzato;risoluzione dei problemi
description: Scopri come risolvere i problemi che a volte si verificano in Adobe [!DNL Target] Compositore esperienza avanzato (EEC) in determinate condizioni.
title: Come posso risolvere i problemi relativi al Compositore esperienza avanzato?
feature: Compositore esperienza visivo
exl-id: 7dea7707-5d9f-49c4-9ccd-618eeb7b3568
source-git-commit: b14c9bb4bc0363c77de084c7ae7110e73c5f2f13
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 53%

---

# Risoluzione dei problemi relativi al [!UICONTROL Compositore esperienza avanzato]

A volte si verificano problemi di visualizzazione nel [!DNL Adobe Target] [!UICONTROL Compositore esperienza avanzato] (EEC) a determinate condizioni.

## Il Compositore esperienza avanzato non carica un URL di controllo qualità interno che non è accessibile su IP pubblico. {#section_D29E96911D5C401889B5EACE267F13CF}

Questo problema può essere risolto inserire nell&#39;elenco Consentiti i seguenti indirizzi IP. Questi indirizzi IP sono per il server di Adobe utilizzato per il proxy EEC. Sono necessari solo per modificare le attività. I visitatori del tuo sito non hanno bisogno di questi indirizzi IP inseriti nell&#39;elenco Consentiti.

Chiedi al team IT di inserire nell&#39;elenco Consentiti i seguenti indirizzi IP:

* 52.55.99.45
* 52.51.238.221
* 52.193.67.35

È possibile visualizzare il seguente messaggio di errore in [!DNL Target]:

`Error: Your website domain (ISP) is blocking the [!UICONTROL Enhanced Experience Composer]. You can allowlist the [!UICONTROL Enhanced Experience Composer]'s IP addresses or turn off [!UICONTROL Enhanced Experience Composer] in [!UICONTROL Configure] > [!UICONTROL Page Delivery] menu.`

![](assets/EEC_error.png)

Di seguito sono riportati possibili cause per questo messaggio di errore e soluzioni per correggere la situazione:

* **Problema:**[!UICONTROL  il dominio del sito Web (ISP) sta bloccando il Compositore esperienza avanzato].

   **Soluzione:** Inserire nell&#39;elenco Consentiti gli indirizzi IP elencati sopra.

* **Problema:** gli indirizzi IP vengono inseriti nell&#39;elenco Consentiti ma il tuo sito web non supporta la versione 1.2 di TLS.  [!DNL Target] attualmente utilizza la configurazione predefinita di 1.2. Prima della versione  [!DNL Target] 18.4.1 (25 aprile 2018), la configurazione predefinita supportava TLS 1.0. Per ulteriori informazioni, consulta Modifiche alla crittografia di  [TLS (Transport Layer Security)](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451).

   **Soluzione:**[!UICONTROL  consulta la domanda seguente (il Compositore esperienza visivo avanzato non viene caricato su pagine protette del mio sito che utilizzano TLS 1.2).]

## Il Compositore esperienza avanzato non viene caricato su pagine protette del mio sito che utilizzano TLS 1.0. (Solo Compositore esperienza avanzato) {#section_C5B31E3D32A844F68E5A8153BD17551F}

È possibile che venga visualizzato il messaggio di errore descritto in precedenza in &quot;Il [!UICONTROL Compositore esperienza visivo avanzato] non viene caricato su pagine protette del mio sito.&quot; se gli indirizzi IP di cui sopra sono inseriti nell&#39;elenco Consentiti ma il tuo sito web non supporta la versione 1.2 di TLS. [!DNL Target] attualmente utilizza la configurazione predefinita di 1.2. Prima di [!DNL Target] 18.4.1 (25 aprile 2018), la configurazione predefinita supportava TLS 1.0. Per ulteriori informazioni, consulta [Modifiche alla crittografia TLS (Transport Layer Security)](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451).

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
