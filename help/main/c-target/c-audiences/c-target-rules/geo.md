---
keywords: targeting;a4t;geo;geotargeting;precisione geotargeting;paese;stato;città;codice postale;DMA;gestore telefonia mobile;codici città;codici area geografica;codici paese;codici metropolitana;script profilo;script profilo geotargeting;geotargeting mobile
description: Scopri come creare tipi di pubblico in [!DNL Adobe Target] per indirizzare gli utenti in base alla loro posizione geografica.
title: Posso indirizzare i visitatori in base alla posizione?
feature: Audiences
solution: Target,Analytics
exl-id: e4a71a4d-e8f3-4f94-a1a7-fd250f4d5095
source-git-commit: 195028613dec0294c816703b9145e720e3209d74
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 41%

---

# Geo

Utilizza i tipi di pubblico in [!DNL Adobe Target] per eseguire il targeting degli utenti in base alla loro posizione geografica.

I parametri di geolocalizzazione consentono di eseguire il targeting di attività ed esperienze in base alla posizione geografica dei visitatori. Puoi includere o escludere i visitatori in base al relativo paese, Stato/provincia, città, codice postale, latitudine, longitudine, DMA o gestore di telefonia mobile. Questi dati vengono inviati con ogni richiesta [!DNL Target] e si basano sull&#39;indirizzo IP del visitatore. Seleziona questi parametri come qualsiasi altro valore di targeting.

## Creare un pubblico con il geotargeting {#section_49CBFFAAC8694C4AAD3DE4B2DB7B05DE}

1. Nell&#39;interfaccia [!DNL Target], fare clic su **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Assegna un nome al pubblico e aggiungi una descrizione facoltativa.
1. Trascina **[!UICONTROL Geo]** nel riquadro Generatore di pubblico.

1. Fare clic su **[!UICONTROL Select]**, quindi selezionare una delle opzioni seguenti:

   * [!UICONTROL Country/Region]
   * [!UICONTROL State]
   * [!UICONTROL City]
   * [!UICONTROL Zip Code]
   * [!UICONTROL Longitude]
   * [!UICONTROL Latitude]
   * [!UICONTROL DMA]
   * [!UICONTROL Mobile Carrier]

   Le informazioni geografiche di un visitatore sono determinate dall’indirizzo IP di origine di una richiesta di posizione [!DNL Target] (richiesta mbox). La risoluzione IP-to-geo viene eseguita per la prima chiamata di una nuova sessione. Ciò significa che, se l’indirizzo IP di un visitatore cambia durante la sessione di una visita, le informazioni geografiche si basano comunque sull’indirizzo IP della prima chiamata.

   Per [!UICONTROL Mobile Carrier], [!DNL Target] utilizza i dati di registrazione dell&#39;indirizzo IP (chi possiede il blocco di indirizzi IP) per determinare il gestore di telefonia mobile appropriato utilizzando [codici nazionali (MCC, Mobile Country Code) e codici di rete mobile (MCC, Mobile Network Code)](https://www.mcc-mnc.com).

1. Specifica un operatore e il valore appropriato.
1. (Facoltativo) Imposta regole aggiuntive per il pubblico.
1. Fare clic su **[!UICONTROL Done]**.

L’illustrazione seguente mostra un pubblico che include gli utenti che accedono all’attività da una latitudine superiore a 44° e una longitudine inferiore a 22°.

![immagine target_geo](assets/target_geo.png)

## Precisione {#section_D63D5FFCB49C42F9933AFD0BD7C79DF1}

La precisione del geotargeting dipende da diversi fattori. Le connessioni Wi-Fi sono più accurate delle reti cellulari. Quando un visitatore utilizza una connessione dati cellulare, la precisione della ricerca geografica può essere influenzata dalla posizione, dalla relazione dati del provider con [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester) e da altri fattori. Le connessioni di rete basate su stazioni cellulari possono essere meno precise delle connessioni cablate o Wi-Fi. Inoltre, l’indirizzo IP di un visitatore potrebbe essere mappato sulla posizione dell’ISP del visitatore, che potrebbe non essere la stessa della posizione effettiva del visitatore. Alcuni problemi di geolocalizzazione mobile possono essere risolti utilizzando [API di geolocalizzazione](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API).

Nella seguente tabella viene mostrata la precisione delle informazioni geografiche basate su IP da [DigitalEnvoy](https://www.digitalelement.com/solutions/) per connessioni internet cablate o Wi-Fi. DigitalEnvoy fornisce i dati più precisi del settore. La precisione globale è superiore al 99,9% a livello di paese e fino al 97% a livello di città. Le informazioni di precisione non si applicano alle reti basate su stazioni cellulari.

| Paese | Stato | Città | Area geografica |
|--- |--- |--- |--- |
| Stati Uniti | 99,99% | 96% | 94% |
| Canada | 99,99% | 96% | 94% |
| Europa | 99,99% |  |  |
| Regno Unito | 99,99% |  | 87% |
| Germania | 99,99% | 95% | 93% |
| Scandinavia | 99% | Circa 90-93% | Circa 84-86% |
| Spagna | 99,99% | Circa 90% | Circa 95-99% |
| Asia | 99% | Circa 94-96% | Circa 90-93% |
| Giappone | 99,99% | Circa 94-96% | Circa 90-93% |
| Australia | 99,99% | 94% | 91% |

## Utilizzare il geotargeting negli script di profilo {#section_92C93138542C4A94997E3F4BE3F5DA28}

Puoi utilizzare le informazioni geografiche per gli script di profilo.

Ad esempio, utilizza:

* `profile.geolocation.country`
* `profile.geolocation.state`
* `profile.geolocation.city`
* `profile.geolocation.zip`
* `profile.geolocation.dma`
* `profile.geolocation.domainName`
* `profile.geolocation.ispName`
* `profile.geolocation.connectionSpeed`
* `profile.geolocation.mobileCarrier`

Pertanto, è possibile scrivere un&#39;espressione di targeting denominata “Proveniente da America del Nord” con il codice seguente:

`return profile.geolocation.country == 'united states' || profile.geolocation.country == 'canada' || profile.geolocation.country == 'mexico';`

## Utilizzare i valori di geotargeting come token {#section_E7F7FDF62C3B4934A6565D04B24655F6}

È possibile utilizzare i valori `profile.geolocation` direttamente come token in offerte, plug-in e così via.

Ad esempio, utilizza:

* `${profile.geolocation.country}`
* `${profile.geolocation.state}`
* `${profile.geolocation.city}`
* `${profile.geolocation.zip}`
* `${profile.geolocation.dma}`
* `${profile.geolocation.domainName}`
* `${profile.geolocation.ispName}`
* `${profile.geolocation.connectionSpeed}`
* `${profile.geolocation.mobileCarrier}`
* `${profile.geolocation.latitude}`
* `${profile.geolocation.longitude}`

## Domande frequenti sul geotargeting {#section_DD308A53AF0F48FA8C81423580561FE7}

Di seguito sono riportate le domande frequenti sul geotargeting:

### Come si specificano latitudine e longitudine?

+++Consulta i dettagli
* I valori di latitudine e longitudine devono essere un valore numerico espresso in gradi.
* I valori di latitudine e longitudine possono avere una precisione massima di cinque cifre decimali.
* Il valore della latitudine deve essere compreso tra -90 e 90.
* Il valore della longitudine deve essere compreso tra -180 e 180.

+++

### Come funziona il geotargeting per i dispositivi mobili?

+++Vedi i dettagli
La maggior parte degli utenti di dispositivi mobili accede ai contenuti tramite WiFi, il che significa che il geotargeting basato su IP di [!DNL Target] è accurato come su un desktop. Le connessioni basate su stazioni cellulari possono essere meno precise in quanto l&#39;indirizzo IP del visitatore si basa sulla stazione dalla quale viene prelevato il segnale. Alcuni problemi di geolocalizzazione mobile possono essere risolti utilizzando [API di geolocalizzazione](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API).

+++

### In che modo la funzione Geo gestisce i visitatori provenienti da AOL?

+++Vedi i dettagli
A causa del modo in cui AOL esegue il proxy del traffico, [!DNL Target] può eseguire il targeting solo a livello di paese. Ad esempio, una campagna indirizzata alla Francia ha come target gli utenti AOL in Francia. Tuttavia, una campagna indirizzata a Parigi non ha come obiettivo gli utenti AOL a Parigi. Se l&#39;intento è quello di eseguire il targeting specifico degli utenti di AOL, puoi impostare il campo regione su “AOL”. Invero, puoi eseguire il targeting degli utenti di AOL degli Stati Uniti specificando due condizioni di targeting: corrispondenza esatta di paese con “Stati Uniti” e corrispondenza esatta di regione con “AOL”.

+++

### Qual è il livello di dettaglio sulla posizione fornito dal geotargeting?

+++Consulta i dettagli
* Paese: globale
* Stato/provincia/regione: globale
* Città: globale
* Codice postale: Stati Uniti, Germania, Canada
* DMA/ITV (Regno Unito): Stati Uniti, Regno Unito
* Gestore di telefonia mobile: globale

+++

### Come posso testare le mie attività simulando di essere un utente proveniente da una posizione diversa?

+++Consulta i dettagli
* **at.js 1.*x***: è possibile sostituire l&#39;indirizzo IP con un indirizzo IP di una posizione diversa e utilizzare il parametro `mboxOverride.browserIp url`. Ad esempio, se la tua azienda è nel Regno Unito ma la campagna globale è indirizzata a visitatori di Auckland in Nuova Zelanda, utilizza questo stile di URL supponendo che `60.234.0.39` sia un indirizzo IP di Auckland:

  `https://www.mycompany.com?mboxOverride.browserIp=60.234.0.39`

  Cancella i cookie prima di eseguire il test dell’attività.

  >[!NOTE]
  >
  >`mboxOverride.browserIp` è supportato in at.js 1.*x*. Questa funzionalità non è supportata in at.js 2.*x*.

* **Equivalente in at.js 2.*x***: per sostituire il tuo indirizzo IP con at.js 2.*x*, installa un&#39;estensione/plug-in del browser (ad esempio X-Forwarded-For Header per Chrome o Firefox). Questa estensione ti consente di trasmettere l’intestazione x-inoltrato-per nelle richieste della pagina.

+++

### In che modo territori, come ad esempio Porto Rico e Hong Kong, vengono mappati nella struttura del geotargeting?

+++Vedi i dettagli
Porto Rico, Hong Kong e altri territori sono trattati come valori &quot;Paese&quot; separati.

+++

### [!DNL Target] acquisisce (e archivia) informazioni come il codice postale quando l&#39;attività è mirata con funzionalità di targeting di geolocalizzazione?

+++Vedi i dettagli
No, [!DNL Target] utilizza i dati geografici solo durante la sessione, quindi i dati vengono eliminati.

+++

## Video di formazione: Creazione di tipi di pubblico ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video contiene informazioni sull&#39;utilizzo delle categorie di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392)
