---
keywords: Targeting;eec;compositore esperienza visiva;risoluzione dei problemi compositore esperienza avanzato;risoluzione dei problemi
description: Scopri come risolvere i problemi che a volte si verificano nell’Adobe [!DNL Target] Compositore esperienza avanzato (EEC) a determinate condizioni.
title: Come posso risolvere i problemi relativi al Compositore esperienza avanzato?
feature: Visual Experience Composer (VEC)
exl-id: 7dea7707-5d9f-49c4-9ccd-618eeb7b3568
source-git-commit: 7562a1da201b570ee529db9763ef5f4b463f65a8
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 23%

---

# Risoluzione dei problemi relativi al [!UICONTROL Enhanced Experience Composer]

Talvolta si verificano problemi di visualizzazione in [!DNL Adobe Target] [!UICONTROL Enhanced Experience Composer] (CEE) a determinate condizioni.

## Il Compositore esperienza avanzato non carica un URL di controllo qualità interno che non è accessibile su IP pubblico. {#section_D29E96911D5C401889B5EACE267F13CF}

Questo problema può essere risolto inserendo nell&#39;elenco Consentiti seguenti indirizzi IP. Questi indirizzi IP sono per Adobe il server utilizzato per il proxy EEC. Sono necessari solo per modificare le attività. I visitatori del tuo sito non hanno bisogno di inserire nell&#39;elenco Consentiti questi indirizzi IP.

Inserire nell&#39;elenco Consentiti Chiedi al tuo team IT di i seguenti indirizzi IP:

* 34 254 77 200
* 54 73 207 147
* 54 229 152 123
* 3 224 194 242
* 54 90 51 39
* 34 228 136 112
* 54 150 116 11
* 18 178 142,8
* 54 199 107 77
* 99.80.139.221
* 54 78 56 224
* 54 247 179 246
* 54 80 219 243
* 34 201 235 54
* 54 196 224 236
* 35.75.212.45.
* 52 199 184 130
* 18 180 161 176

Potresti visualizzare il seguente messaggio di errore in [!DNL Target]:

`Error: Your website domain (ISP) is blocking the [!UICONTROL Enhanced Experience Composer]. You can allowlist the [!UICONTROL Enhanced Experience Composer]'s IP addresses or turn off [!UICONTROL Enhanced Experience Composer] in [!UICONTROL Configure] > [!UICONTROL Page Delivery] menu.`

![Immagine EEC_error](assets/EEC_error.png)

Di seguito sono riportati possibili cause per questo messaggio di errore e soluzioni per correggere la situazione:

* **Problema:** Il dominio del sito Web (ISP) sta bloccando [!UICONTROL Enhanced Experience Composer].

  **Rimedio:** Inserire nell&#39;elenco Consentiti gli indirizzi IP elencati sopra.

* **Problema:** Gli indirizzi IP vengono inseriti nell&#39;elenco Consentiti, ma il tuo sito Web non supporta la versione 1.2 di TLS. [!DNL Target] attualmente utilizza la configurazione predefinita di 1.2. Prima della [!DNL Target] 18.4.1 (25 aprile 2018), la configurazione predefinita supportava TLS 1.0. Per ulteriori informazioni, consulta [Modifiche alla crittografia di TLS (Transport Layer Security)](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank}.

  **Soluzione:** Vedi la domanda seguente (la [!UICONTROL Enhanced Visual Experience Composer] non viene caricato su pagine protette del mio sito che utilizzano TLS 1.2).

## Il Compositore esperienza avanzato non viene caricato su pagine protette del mio sito che utilizzano TLS 1.0. (Solo Compositore esperienza avanzato) {#section_C5B31E3D32A844F68E5A8153BD17551F}

È possibile che venga visualizzato il messaggio di errore descritto in precedenza in &quot;La [!UICONTROL Enhanced Visual Experience Composer] non si carica su pagine protette del mio sito.&quot; se gli indirizzi IP di cui sopra vengono inseriti nell&#39;elenco Consentiti ma il tuo sito web non supporta la versione 1.2 di TLS. [!DNL Target] attualmente utilizza la configurazione predefinita di 1.2. Prima della [!DNL Target] 18.4.1 (25 aprile 2018), la configurazione predefinita supportava TLS 1.0. Per ulteriori informazioni, consulta [Modifiche alla crittografia di TLS (Transport Layer Security)](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank}.

Per controllare la versione TLS sul tuo sito web con Firefox (altri browser hanno passaggi simili):

1. Apri il sito interessato in Firefox.
1. Fai clic su **[!UICONTROL Show Site Information]** sulla barra degli indirizzi del browser.

   ![immagine firefox_more_info](assets/firefox_more_info.png)

1. Clic **[!UICONTROL Show Connection Details]** > **[!UICONTROL More Information]**.

   ![immagine firefox_more_info_2](assets/firefox_more_info_2.png)

1. Verifica la versione di TLS alla voce Dettagli tecnici:

   ![immagine firefox_more_info_3](assets/firefox_more_info_3.png)

1. Se scopri che il tuo sito web mostra TLS 1.0, consulta [Modifiche alla crittografia di TLS (Transport Layer Security)](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank} per informazioni sui criteri di supporto TLS di Target. Per risolvere la situazione (valido fino al 12 settembre 2018){target=_blank}, contatta [Assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) per la configurazione con la versione di TLS e il dominio.

## Ricevo errori di timeout o “accesso negato” durante il caricamento di siti con proxy abilitato. (Solo Compositore esperienza avanzato) {#section_60CBB9022DC449F593606C0E6252302D}

Assicurati che nel tuo ambiente gli IP proxy non siano bloccati.
