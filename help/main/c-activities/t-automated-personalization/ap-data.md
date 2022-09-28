---
keywords: dati ambientali;dati di sessione;dati geografici;dati geografici;dati dispositivo;dati mobili;attributi;attributi di profilo;algoritmi di personalizzazione;algoritmi di apprendimento automatico;algoritmi di apprendimento automatico
description: Scopri quale Adobe di dati [!DNL Target] raccoglie e utilizza per creare i suoi algoritmi di apprendimento automatico.
title: Quali dati vengono raccolti per creare algoritmi di apprendimento automatico?
feature: Automated Personalization
exl-id: 7114a6d6-4779-471e-9b91-646aa49e102a
source-git-commit: ca1f42b95399fbd136aee27ccec9ed0e38876234
workflow-type: tm+mt
source-wordcount: '2085'
ht-degree: 49%

---

# ![PREMIUM](/help/main/assets/premium.png) Dati utilizzati da [!DNL Target] algoritmi di apprendimento automatico

[!DNL Adobe Target] raccoglie e utilizza automaticamente una varietà di dati per creare gli algoritmi di personalizzazione in [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Targeting automatico] (AT) attività. Quando un visitatore accede a un’attività di Personalizzazione automatizzata o Targeting automatico, viene trasmessa un’istantanea di informazioni a un set di &quot;record di formazione&quot; (i dati del visitatore su cui gli algoritmi di personalizzazione impareranno).

Per ulteriori informazioni sulle [!DNL Target] algoritmi di personalizzazione, vedi [Algoritmo Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

## Predefinito [!DNL Adobe Target] categorie di attributi

La tabella seguente mostra i dati raccolti da [!UICONTROL Automated Personalization] e [!UICONTROL Targeting automatico] attività per impostazione predefinita, senza alcuna configurazione [!DNL Target] o altro [!DNL Adobe] le soluzioni, nonché la convenzione di denominazione utilizzata per indicare questi attributi in [Rapporti Approfondimenti personalizzazione](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767). Puoi aumentare il set di dati di input in qualsiasi momento. Per ulteriori informazioni su come caricare dati aggiuntivi, consulta [Caricamento dei dati per la [!DNL Target] algoritmi di personalizzazione](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

| Categoria dati | Prefisso di sistema | Descrizione | Nome visualizzato in [!UICONTROL Informazioni approfondite] rapporti |
| --- | --- | --- | --- |
| Parametri ambiente | ENV | Informazioni sull’ambiente di un utente, compresi sistema operativo, browser e ora del giorno/giorno della settimana. | Browser - [Nome attributo]<br>Sistema operativo - [Valore] |
| Informazioni geografiche | GEO | Informazioni sulla posizione geografica di un utente, ottenute tramite ricerca IP. | Geo - [attributo geo] |
| Dispositivo mobile | MOB | Informazioni sul dispositivo mobile di un utente. | Dispositivo - [attributo dispositivo]<br>Mobile - [attributo mobile] |
| Segmenti di reporting di Target | SEG | Segmenti di reporting configurati in [!DNL Target] rapporti. | Segmento di reporting -[Nome segmento] |
| Comportamento della sessione | SES | Informazioni sul comportamento dell’utente, ad esempio il numero di pagine visualizzate. | Profilo visitatore - [Nome attributo] |

## Categorie di attributi Adobe Target personalizzate

La tabella seguente mostra i dati forniti dal cliente raccolti da [!UICONTROL Automated Personalization] e [!UICONTROL Targeting automatico] attività. Questi dati vengono raccolti solo se vengono forniti. Nomi di attributi specifici e valori di esempio saranno particolari per la configurazione del sistema.

| Categoria dati | Prefisso di sistema | Descrizione | Nome visualizzato in [!UICONTROL Informazioni approfondite] rapporti |
| --- | --- | --- | --- |
| Parametri di pagina | CASELLA | Parametri di pagina personalizzati (&quot;parametri mbox&quot;) trasmessi nella chiamata a [!DNL Target]. | Personalizzato - Parametro mbox - [nome parametro] |
| [!DNL Target] profilo | PRO | Attributi di profilo personalizzati caricati direttamente nel [!DNL Target] tramite API o parametro di pagina e [!DNL Target] script di profilo. | Personalizzato - Profilo visitatore - [nome attributo] |
| Attributi del cliente | CRS | Attributi del cliente caricati nel [!DNL Target] tramite [Servizio Attributi del cliente Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/attributes.html){target=_blank}. | Personalizzato - Profilo visitatore - [nome attributo] |
| Parametri URL | URL | URL ed eventuali parametri URL per la pagina attualmente visualizzata. | Personalizzato - Parametro URL - [Parametro URL] |
| URL di riferimento | REF | URL di riferimento ed eventuali parametri URL per l’URL di riferimento. | Personalizzato - [Parametro URL di riferimento] - [Valore parametro] |
| Tipi di pubblico condivisi di Adobe Experience Cloud | AAM | Tutti i tipi di pubblico condivisi con [!DNL Target] da altri [!DNL Adobe Experience Cloud] soluzioni (ad esempio, [!DNL Adobe Audience Manager] e [!DNL Adobe Analytics], tramite [[!DNL Experience Cloud Audience Library]](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html){target=_blank}). | Personalizzato - Pubblico Experience Cloud - [Nome del pubblico] |
| Tipi di pubblico CDP in tempo reale di Adobe Experience Platform | UPS | AEP Tipi di pubblico CDP in tempo reale condivisi con [!DNL Target] tramite Destinazioni. |  |
| Attributi CDP in tempo reale di Adobe Experience Platform | AEP | Attributi CDP in tempo reale AEP condivisi con [!DNL Target] tramite Destinazioni. Questa funzione è attualmente in versione beta. |  |

## Blocco delle funzioni da [!DNL Target] algoritmi di apprendimento automatico

Le funzionalità possono essere bloccate [!DNL Target] algoritmi di apprendimento automatico, che ne impediscono l’utilizzo in qualsiasi [!UICONTROL Targeting automatico] o [!UICONTROL Automated Personalization] modello o attività.

Per bloccare una categoria di feature da [!DNL Target] algoritmi di apprendimento automatico, contatto [Adobe Customer Care](/help/main/cmp-resources-and-contact-information.md#section_CC8B206F58D6495C9372D5C0D4055CF6) e specifica le categorie di funzionalità che desideri bloccare, utilizzando i prefissi di sistema forniti sopra.

Per bloccare una o più feature specifiche da [!DNL Target] algoritmi di apprendimento automatico, contatto [Adobe Customer Care](/help/main/cmp-resources-and-contact-information.md#section_CC8B206F58D6495C9372D5C0D4055CF6) e specifica i nomi di funzionalità specifici che devono essere bloccati, utilizzando i seguenti nomi di sistema forniti. Le sezioni seguenti contengono informazioni dettagliate sui vari tipi di dati, tra cui nomi di attributi, descrizioni e valori di esempio.

## Dati mobili e sul dispositivo {#device-mobile}

| Nome attributo | Descrizione attributo | Valori di esempio | Nome del sistema |
| --- | --- | --- | --- |
| Mobile - Device - Brand | Il marchio del dispositivo mobile utilizzato per accedere all’attività. | Apple | MOB_targeting.mobile.vendor |
| Mobile - Device - eReader | Specifica se il dispositivo è un eReader. | 0 = False, 1 = True | MOB_targeting.mobile.ereader |
| Mobile - Device - Game Console | Specifica se il dispositivo è una console di giochi. | 0 = False, 1 = True | MOB_targeting.mobile.gamesConsole |
| Mobile - Device - Media Player | Specifica se il dispositivo è un lettore multimediale. | 0 = False, 1 = True | MOB_targeting.mobile.mediaPlayer |
| Mobile - Device - Mobile Phone | Specifica se il dispositivo è un telefono cellulare. | 0 = False, 1 = True | MOB_targeting.mobile.mobilePhone |
| Mobile - Device - Model Name | Il nome del modello del dispositivo mobile utilizzato per accedere all’attività. | iPhone XS | MOB_targeting.mobile.model |
| Device - Set-Top Box | Specifica se il dispositivo è un decoder. | 0 = False, 1 = True | MOB_targeting.mobile.setTopBox |
| Mobile - Device - Tablet | Specifica se il dispositivo è un tablet. | 0 = False, 1 = True | MOB_targeting.mobile.tablet |
| Mobile - Pixel Density (ppi) | La densità pixel del marchio del dispositivo mobile utilizzato per accedere all’attività. | 1, 2, 3, ecc. | MOB_targeting.mobile.displayPpi |
| Mobile - OS - OSX (Android, Windows, ecc.) | Specifica se l’utente ha utilizzato un dispositivo con sistema operativo OSX (o Android, Windows, ecc.) per accedere all’attività. | 0 = False, 1 = True | MOB_targeting.mobile.os[OS]<br>Ad esempio, MOB_targeting.mobile.osOSx, MOB_targeting.mobile.osWindows, MOB_targeting.mobile.osAndroid, MOB_targeting.mobile.osLinux |
| Mobile - Screen Height (px) | L’altezza (in pixel) dello schermo del dispositivo mobile utilizzato per accedere all’attività. | 1, 2, 3, ecc. | MOB_targeting.mobile.displayHeight |
| Mobile - Screen Width (px) | La larghezza (in pixel) dello schermo del dispositivo mobile utilizzato per accedere all’attività. | 1, 2, 3, ecc. | MOB_targeting.mobile.displayWidth |

## Dati sull’ambiente {#env}

|Nome attributo|Descrizione attributo|Valori di esempio|Nome sistema| | — | — | — | — | |Browser - Day of Week|Il giorno della settimana in cui il visitatore ha effettuato l’accesso all’attività.|Da 0 a 6.<br>(0 = domenica)|ENV_DayOfWeek| |Browser - Hour of Day|L&#39;ora del giorno in cui il visitatore ha effettuato l&#39;accesso all&#39;attività.da |0 a 23<br>(0 = mezzanotte)|ENV_UserHour| |Browser - Hour of Week|L&#39;ora della settimana in cui il visitatore ha effettuato l&#39;accesso all&#39;attività.da |0 a 168<br>(0 = mezzanotte di domenica)|ENV_WeekHour| |Browser - Language Setting|La lingua specificata nel browser del visitatore utilizzato per accedere all’attività.|Inglese<br>Tedesco|ENV_Language| |Browser - Time of Day|L&#39;ora del giorno del browser in cui il visitatore ha effettuato l&#39;accesso all&#39;attività.|0, 6, 12, 18<br>(0 = notte, 6 = mattina,<br>12 è pomeriggio, 18 è sera)|ENV_LocalTimePeriod| |Browser - Timezone|Il fuso orario del visitatore durante l&#39;accesso all&#39;attività.|Ora del Pacifico<br>Ora orientale<br>GMT|ENV_BrowserTimezoneOffsetMinutes| |Browser - Type|Il tipo di browser utilizzato dal visitatore per accedere all&#39;attività.|Chrome<br>Firefox<br>Internet Explorer<br>Safari<br>Altro|ENV_Browser| |Browser - Weekday/Weekend|Lo stato lavorativo del giorno in cui il visitatore ha effettuato l&#39;accesso all&#39;attività (fine settimana, ore lavorative o orario libero nei giorni feriali).|Sabato e domenica fine settimana<br>Lunedì-Venerdì dalle 0900 alle 1800 è orario di lavoro<br>Lunedì-Venerdì dopo le 1800 fino alle 0900 è orario libero nei giorni feriali|ENV_UserHourType| |Browser - Window Height (px)|L&#39;altezza (in pixel) della finestra del browser utilizzato dal visitatore per accedere all&#39;attività.|1, 2, 3, ecc.|ENV_BrowserHeight| |Browser - Window Width (px)|La larghezza (in pixel) della finestra del browser utilizzato dal visitatore per accedere all’attività.|1, 2, 3, ecc.|ENV_BrowserWidth| |Device - Screen Height (px)|L&#39;altezza dello schermo del dispositivo utilizzato dal visitatore per accedere all&#39;attività.|1, 2, 3, ecc.|ENV_ScreenHeight| |Device - Screen Width (px)|La larghezza dello schermo del dispositivo utilizzato dal visitatore per accedere all’attività.|1, 2, 3, ecc.|ENV_ScreenWidth| |Sistema operativo|Il sistema operativo sul dispositivo del visitatore utilizzato per accedere all&#39;attività.Sistema operativo Mac<br>Windows<br>Linux<br>Punto di ricerca<br>Sistema operativo sconosciuto|ENV_OperatingSystem| |Sistema operativo - Versione|Versione del sistema operativo utilizzato dal visitatore per accedere all&#39;attività.|Windows 10<br>Mac OS 10|ENV_OperatingSystemVersion| |Origini del traffico - URL della pagina di destinazione di riferimento|La prima pagina visualizzata dal visitatore all’accesso al sito.|`https://www.adobe.com/ecloud.html`|ENV_Referrer|

## Dati geografici {#geo}

| Nome attributo | Descrizione attributo | Valori di esempio | Nome del sistema |
| --- | --- | --- | --- |
| Geo - City | La città da cui il visitatore ha effettuato l’accesso all’attività. | San Francisco | Geo_City |
| Geo - Country | Il paese da cui il visitatore ha effettuato l’accesso all’attività. | Germania | Geo_Country |
| Geo - DMA | L’area di marketing designata (DMA) da cui il visitatore ha effettuato l’accesso all’attività. | Charlottesville | Geo_DMA |
| Geo - Latitude | La latitudine da cui il visitatore ha effettuato l’accesso all’attività. | 47,269<br>Arrotondato a 3 cifre decimali (precisione di circa 100 metri) | GEO_Latitude |
| Geo - Longitude | La longitudine da cui il visitatore ha effettuato l’accesso all’attività. | -122,269<br>Arrotondato a 3 cifre decimali (precisione di circa 100 metri) | GEO_Longitude |
| Geo - State/Region | Lo stato o la provincia da cui il visitatore ha effettuato l’accesso all’attività. | Utah<br>New South Wales | GEO_State<br>GEO_Region |
| Geo - Zip Code | Codice postale da cui il visitatore ha effettuato l’accesso all’attività. | 84004 | GEO_ZipCode |
| Mobile - Carrier | Il gestore di telefonia mobile utilizzato dal visitatore per accedere all’attività. | Vodafone<br>T-Mobile | GEO_mobileCarrier |
| Network - Connection Speed | La velocità di connessione di rete del dispositivo quando il visitatore ha effettuato l’accesso all’attività. | Broadband<br>Cable<br>DSL<br>Mobile<br>Wireless<br>Satellite | GEO_ConnectionSpeed |
| Network - Domain Name | Il nome del dominio della rete dalla quale il visitatore ha effettuato l’accesso all’attività. | `nnt.net` | GEO_DomainName |
| Network - ISP | La rete dalla quale il visitatore ha effettuato l’accesso all’attività. | nnt communications corporation | GEO_IspName |

## Dati sessione {#session}

| Nome attributo | Descrizione attributo | Valori di esempio | Nome del sistema |
| --- | --- | --- | --- |
| Visitor Profile - Activity Lifetime Order Value | Specifica la somma di tutti i valori degli ordini per tutte le visite/sessioni di una particolare attività. | Doppio | SES_CUMULATIVE_ORDER_VALUE |
| Visitor Profile - Activity Lifetime Time on Site | Specifica il tempo totale trascorso dal visitatore sul sito, esclusa la sessione corrente, e viene aggiornato al termine della sessione. | Doppio, millisecondi | SES_TOTAL_TIME |
| Visitor Profile -Average Page Views per Visit during Activity | Specifica il numero medio di visualizzazioni pagina per sessione, esclusa la sessione corrente. | Doppio | SES_REQUESTS_PER_SESSION |
| Visitor Profile - Average Time per Visit | Specifica il tempo medio trascorso per visita/sessione. La sessione corrente non è inclusa. | Doppio, millisecondi | SES_TIME_PER_SESSION |
| Visitor Profile - First Visit | Specifica l’ora della prima visita durante la quale il visitatore ha interagito con [!DNL Target]. | Doppio, millisecondi | SES_PROFILE_CREATION_TIME |
| Visitor Profile - Hours since Last Visit | Specifica quante ore sono trascorse dall’ultima visita a questa attività specifica. | Doppio (solo numero intero positivo) 1, 2, 3, ecc. | SES_HOURS_SINCE_LAST_VISIT |
| Visitor Profile - Impressions of Location/Content | Specifica il numero di impression per una particolare combinazione di posizione/contenuto in una particolare attività. | Doppio (solo numero intero positivo) 1, 2, 3, ecc. | SES_CUMULATIVE_ACTION_[LOCATION_ID]_[CONTENT_ID] |
| Profilo visitatore - Ultimo [!DNL Target] Interazione | Specifica l’ora dell’ultima interazione con [!DNL Target]. L&#39;interazione si verifica a ogni [!DNL Target] perché l&#39;attuale implementazione di [!DNL Target] aggiorna il profilo su ogni richiesta. | Doppio, millisecondi | SES_PROFILE_UPDATE_TIME |
| Visitor Profile - Pages Seen Before Activity | Specifica il numero di visualizzazioni pagina (impression) totali, inclusa la visita/sessione corrente, fino a quando il visitatore accede all’attività. | Doppio (solo numero intero positivo) 1, 2, 3, ecc. | SES_TOTAL_PAGE_VIEWS |
| Visitor Profile - Page Views in Current Visit | Specifica il numero di visualizzazioni pagina durante la visita/sessione corrente fino a quando il visitatore accede all’attività. Più precisamente, il numero di impression. Le impression non sono visualizzazioni di pagina reali, ma piuttosto quante volte la richiesta è stata ricevuta da Target. Target non è in grado di distinguere tra timeout o altri motivi per cui l’utente potrebbe non ricevere o visualizzare effettivamente il contenuto. | Doppio (solo numero intero positivo). | SES_SESSION_POSITION |
| Visitor Profile - Start of Current Visit | Specifica l’ora in cui è iniziata la visita/sessione corrente con Target. La visita con Target può essere avviata senza accedere a un’attività. Tutto ciò che è necessario è una chiamata a qualsiasi [!DNL Target] richiesta. Potrebbe trascorrere un po’ di tempo prima che il visitatore acceda all’attività e venga acquisita l’istantanea. | Doppio, millisecondi | SES_SESSION_START |
| Visitor Profile - Start of Most Recent Visit | Specifica l’ora dell’ultima visita/sessione con [!DNL Target] Ho iniziato. Questo attributo viene aggiornato alla scadenza della sessione.<br>Se si tratta della prima sessione del visitatore, verrà generato `LAST_SESSION_START = 0.` | Doppio, millisecondi | SES_LAST_SESSION_START |
| Visitor Profile - Time Since Most Recent Visit When First Enter Activity | Specifica il tempo trascorso tra la sessione precedente e il momento in cui l’utente accede all’attività e viene acquisita l’istantanea. | Doppio, millisecondi | SES_RECENCY |
| Visitor Profile - Time in Visit Before Enter Activity | Specifica la differenza tra l’ultima interazione con [!DNL Target] e all&#39;inizio della visita corrente. Questo attributo può essere considerato come durata della visita/sessione fino al momento in cui l’utente accede all’attività e viene acquisita l’istantanea.<br>[!DNL Target]Vengono riportati valori negativi quando l’inizio della sessione e l’ultima ora di aggiornamento vengono attivati dalla stessa chiamata I valori negativi devono essere considerati 0 (zero). | Doppio, millisecondi | SES_SESSION_TIME |
| Profilo visitatore - Visite totali | Specifica il numero totale di visite/sessioni. La visita/sessione corrente non è inclusa. | Doppio (solo numero intero positivo) 1, 2, 3, ecc. | SES_TOTAL_SESSIONS |
| Visitor Profile - Total Visits to Activity | Specifica il numero di visite a una particolare attività. Se non è presente alcuna visita precedente, viene restituito 0 (zero). | Doppio (solo numero intero positivo) 1, 2, 3, ecc. | SES_PREVIOUS_VISIT_COUNT |
| Visitor Profile - Total Visits to Activity with Conversion | Specifica il numero di visite/sessioni a una particolare attività nel corso delle quali si è verificata almeno una conversione. | Doppio | SES_CUMULATIVE_SUCCESSES |
| Visitor Profile - Visits to Activity with No Conversion | Numero di visite/sessioni a una particolare attività nel corso delle quali non si sono verificate conversioni. Questo valore viene reimpostato su zero dopo una conversione, o su -1 se la conversione non si è mai verificata. | Doppio (solo numero intero positivo) 1, 2, 3, ecc. | SES_SUCCESS_RECENCY |
