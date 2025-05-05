---
keywords: dati ambientali;dati sessione;dati geografici;dati geografici;dati dispositivo;dati mobili;attributi;attributi profilo;algoritmi di personalizzazione;algoritmi di apprendimento automatico;algoritmi di apprendimento automatico
description: Scopri quali dati [!DNL Adobe Target] raccoglie e utilizza per creare gli algoritmi di apprendimento automatico.
title: Quali dati vengono raccolti per creare algoritmi di apprendimento automatico?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Automated Personalization
exl-id: 7114a6d6-4779-471e-9b91-646aa49e102a
source-git-commit: fe6a7addd3854c430798fc339741c9ae6a4efc7d
workflow-type: tm+mt
source-wordcount: '1958'
ht-degree: 51%

---

# Dati utilizzati da [!DNL Target] algoritmi di apprendimento automatico

[!DNL Adobe Target] raccoglie e utilizza automaticamente vari dati per generare gli algoritmi di personalizzazione nelle attività [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Auto-Target] (AT). Quando un visitatore accede a un&#39;attività [!UICONTROL Automated Personalization] o [!UICONTROL Auto-Target], viene passata un&#39;istantanea di informazioni a un set di &quot;record di formazione&quot; (i dati del visitatore su cui gli algoritmi di personalizzazione apprendono qualcosa).

Per ulteriori informazioni sugli algoritmi di personalizzazione [!DNL Target], vedere [Algoritmo Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

## Categorie di attributi [!DNL Target] predefinite

Nella tabella seguente sono riportati i dati raccolti dalle attività [!UICONTROL Automated Personalization] e [!UICONTROL Auto-Target] per impostazione predefinita, senza alcuna configurazione di [!DNL Target] o altre soluzioni [!DNL Adobe]. La tabella include anche la convenzione di denominazione utilizzata per indicare questi attributi nei [rapporti Personalization Insights](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767). Puoi aumentare il set di dati di input in qualsiasi momento. Per ulteriori informazioni su come caricare dati aggiuntivi, consulta [Caricamento dei dati per gli  [!DNL Target] algoritmi di personalizzazione](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

| Categoria dati | Prefisso di sistema | Descrizione | Nome visualizzato nei report [!UICONTROL Insights] |
| --- | --- | --- | --- |
| Parametri dell’ambiente | ENV | Informazioni sull’ambiente di un utente, tra cui sistema operativo, browser e ora del giorno/giorno della settimana. | Browser - [Nome attributo]<br>Sistema operativo - [Valore] |
| Informazioni geografiche | GEO | Informazioni sulla posizione geografica di un utente, ottenute tramite ricerca IP. | Geo - [attributo geo] |
| Dispositivo mobile | FOLLA | Informazioni sul dispositivo mobile di un utente. | Dispositivo - [attributo dispositivo]<br>Dispositivo mobile - [attributo dispositivo mobile] |
| [!DNL Target] segmenti di reporting | SEG | Segmenti di reporting configurati nel reporting di [!DNL Target]. | Segmento di reporting -[Nome segmento] |
| Comportamento sessione | SES | Informazioni sul comportamento dell’utente, ad esempio il numero di pagine visualizzate. | Profilo visitatore - [Nome attributo] |

## Categorie di attributi [!DNL Target] personalizzate

La tabella seguente mostra i dati forniti dal cliente raccolti dalle attività [!UICONTROL Automated Personalization] e [!UICONTROL Auto-Target]. Questi dati vengono raccolti solo se forniti dall&#39;utente. Nomi di attributi specifici e valori di esempio sono specifici per la configurazione del sistema.

| Categoria dati | Prefisso di sistema | Descrizione | Nome visualizzato nei report [!UICONTROL Insights] |
| --- | --- | --- | --- |
| Parametri di pagina | BOX | Parametri di pagina personalizzati (&quot;parametri mbox&quot;) passati nella chiamata a [!DNL Target]. | Personalizzato - Parametro Mbox - [nome parametro] |
| Profilo [!DNL Target] | PRO | Gli attributi di profilo personalizzati vengono caricati direttamente nel profilo [!DNL Target] tramite API o parametro di pagina e [!DNL Target] script di profilo. | Personalizzato - Profilo visitatore - [nome attributo] |
| Attributi del cliente | CRS | Attributi del cliente caricati nel profilo [!DNL Target] tramite [[!DNL Adobe Experience Cloud Customer Attributes Service]](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/attributes.html?lang=it){target=_blank}. | Personalizzato - Profilo visitatore - [nome attributo] |
| Parametri URL | URL | URL ed eventuali parametri URL per la pagina visualizzata. | Personalizzato - Parametro URL - [Parametro URL] |
| URL di riferimento | RIF | URL di riferimento ed eventuali parametri URL per l’URL di riferimento. | Personalizzato - [Parametro URL di riferimento] - [Valore parametro] |
| [!DNL Adobe Experience Cloud] tipi di pubblico condivisi | AAM | Tutti i tipi di pubblico condivisi con [!DNL Target] da altre soluzioni [!DNL Adobe Experience Cloud] (ad esempio, [!DNL Adobe Audience Manager] e [!DNL Adobe Analytics], tramite [[!DNL Experience Cloud Audience Library]](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=it){target=_blank}). | Personalizzato - Pubblico Experience Cloud - [Nome pubblico] |
| [!DNL Adobe Experience Platform Real-time CDP] tipi di pubblico | UPS | Pubblico di Platform Real-time CDP condiviso con [!DNL Target] tramite [!UICONTROL Destinations]. |  |


## Blocco delle funzionalità da [!DNL Target] algoritmi di apprendimento automatico

Le funzionalità possono essere bloccate da [!DNL Target] algoritmi di apprendimento automatico, impedendo che vengano utilizzate in qualsiasi modello o attività [!UICONTROL Automated Personalization] o [!UICONTROL Auto-Target].

Per ulteriori informazioni, vedere [Panoramica di Models API (Inserisce nell&#39;elenco Bloccati di)](https://experienceleague.adobe.com/docs/target-dev/developer/api/models-api/models-api.html?lang=it){target=_blank} nella Guida per gli sviluppatori di *[!DNL Adobe Target]*.

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
| Mobile - Pixel Density (ppi) | La densità pixel del marchio del dispositivo mobile utilizzato per accedere all’attività. | 1, 2, 3 e così via. | MOB_targeting.mobile.displayPpi |
| Mobile - OS - OS X ([!DNL Android], [!DNL Windows] e così via) | Specifica se l&#39;utente ha utilizzato un dispositivo OSX (o [!DNL Android], [!DNL Windows] e così via) per accedere all&#39;attività. | 0 = False, 1 = True | MOB_targeting.mobile.os[OS]<br>Ad esempio, MOB_targeting.mobile.osOSx, MOB_targeting.mobile.osWindows, MOB_targeting.mobile.osAndroid, MOB_targeting.mobile.osLinux |
| Mobile - Screen Height (px) | L’altezza (in pixel) dello schermo del dispositivo mobile utilizzato per accedere all’attività. | 1, 2, 3 e così via. | MOB_targeting.mobile.displayHeight |
| Mobile - Screen Width (px) | La larghezza (in pixel) dello schermo del dispositivo mobile utilizzato per accedere all’attività. | 1, 2, 3 e così via. | MOB_targeting.mobile.displayWidth |

## Dati ambientali {#env}

| Nome attributo | Descrizione attributo | Valori di esempio | Nome del sistema |
| --- | --- | --- | -- |
| Browser - Day of Week | Il giorno della settimana in cui il visitatore ha effettuato l’accesso all’attività. | 0 - 6.<br>(0 = domenica) | ENV_DayOfWeek |
| Browser - Hour of Day | L’ora del giorno in cui il visitatore ha effettuato l’accesso all’attività. | 0 - 23<br>(0 = mezzanotte) | ENV_UserHour |
| Browser - Hour of Week | L’ora della settimana in cui il visitatore ha effettuato l’accesso all’attività. | 0 - 168<br>(la mezzanotte della domenica è 0) | ENV_WeekHour |
| Browser - Language Setting | La lingua specificata nel browser del visitatore utilizzato per accedere all’attività. | English<br>German | ENV_Lingua |
| Browser - Time of Day | L’ora del giorno del browser nel momento in cui il visitatore ha effettuato l’accesso all’attività. | 0, 6, 12, 18<br>(0 = notte, 6 = mattina,<br>12 = pomeriggio, 18 = sera) | ENV_LocalTimePeriod |
| Browser - Timezone | Il fuso orario del visitatore durante l’accesso all’attività. | Pacific Time<br>Eastern Time<br>GMT | ENV_BrowserTimezoneOffsetMinutes |
| Browser - Type | Il tipo di browser utilizzato dal visitatore per accedere all’attività. | [!DNL Chrome]<br>[!DNL Firefox]<br>[!DNL Internet Explorer]<br>[!DNL Safari]<br>Altro | ENV_Browser |
| Browser - Weekday/Weekend | Lo stato lavorativo del giorno in cui il visitatore accede all’attività (fine settimana, orario lavorativo, orario non lavorativo infrasettimanale). | weekend = sabato e domenica<br>work time = lunedì-venerdì 0900 - 1800<br>weekday free time = lunedì-venerdì dopo le 1800 alle 0900 | ENV_UserHourType |
| Browser - Window Height (px) | L’altezza (in pixel) della finestra del browser utilizzato per accedere all’attività. | 1, 2, 3 e così via, | ENV_BrowserHeight |
| Browser - Window Width (px) | La larghezza (in pixel) della finestra del browser utilizzato per accedere all’attività. | 1, 2, 3 e così via, | ENV_BrowserWidth |
| Device - Screen Height (px) | L’altezza (in pixel) dello schermo del dispositivo mobile utilizzato per accedere all’attività. | 1, 2, 3 e così via, | ENV_ScreenHeight |
| Device - Screen Width (px) | La larghezza (in pixel) dello schermo del dispositivo mobile utilizzato per accedere all’attività. | 1, 2, 3 e così via, | ENV_ScreenWidth |
| Sistema operativo | Il sistema operativo del dispositivo utilizzato dal visitatore per accedere all’attività. | [!DNL Mac OS]<br>[!DNL Windows]<br>[!DNL Linux]<br>Bot di ricerca<br>Sistema operativo sconosciuto | ENV_OperatingSystem |
| Operating System - Version | La versione del sistema operativo utilizzato dal visitatore per accedere all’attività. | [!DNL Windows] 10<br>[!DNL Mac OS] 10 | ENV_OperatingSystemVersion |
| Traffic Sources - Referring Landing Page URL | La prima pagina visualizzata dal visitatore all’accesso al sito. | `https://www.adobe.com/ecloud.html` | ENV_Referrer |

## Dati geografici {#geo}

| Nome attributo | Descrizione attributo | Valori di esempio | Nome del sistema |
| --- | --- | --- | --- |
| Geo - City | La città da cui il visitatore ha effettuato l’accesso all’attività. | San Francisco | Geo_City |
| Geo - Country | Il paese da cui il visitatore ha effettuato l’accesso all’attività. | Germania | Paese_Geografico |
| Geo - DMA | L’area di marketing designata (DMA) da cui il visitatore ha effettuato l’accesso all’attività. | Charlottesville | Geo_DMA |
| Geo - Latitude | La latitudine da cui il visitatore ha effettuato l’accesso all’attività. | 47.269<br>Arrotondato a 3 cifre decimali (precisione di circa 100 metri) | GEO_Latitude |
| Geo - Longitude | La longitudine da cui il visitatore ha effettuato l’accesso all’attività. | -122.269<br>Arrotondato a 3 cifre decimali (precisione di circa 100 metri) | GEO_Longitude |
| Geo - State/Region | Lo stato o la provincia da cui il visitatore ha effettuato l’accesso all’attività. | Utah<br>New South Wales | GEO_State<br>Area_GEOGRAFICA |
| Geo - Zip Code | Codice postale da cui il visitatore ha effettuato l’accesso all’attività. | 84004 | GEO_ZipCode |
| Mobile - Carrier | Il gestore di telefonia mobile utilizzato dal visitatore per accedere all’attività. | [!DNL Vodafone]<br>[!DNL T-Mobile] | GEO_mobileCarrier |
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
| Visitor Profile - First Visit | Specifica l&#39;ora della prima visita in cui l&#39;utente ha interagito con [!DNL Target]. | Doppio, millisecondi | SES_PROFILE_CREATION_TIME |
| Visitor Profile - Hours since Last Visit | Specifica quante ore sono trascorse dall’ultima visita a questa attività specifica. | Doppio (solo numero intero positivo) 1, 2, 3 e così via. | SES_HOURS_SINCE_LAST_VISIT |
| Visitor Profile - Impressions of Location/Content | Specifica il numero di impression per una particolare combinazione di posizione/contenuto in una particolare attività. | Doppio (solo numero intero positivo) 1, 2, 3 e così via. | SES_CUMULATIVE_ACTION_[LOCATION_ID]_[CONTENT_ID] |
| Profilo visitatore - Ultima interazione [!DNL Target] | Specifica l&#39;ora dell&#39;ultima interazione con [!DNL Target]. L&#39;interazione si verifica su ogni richiesta [!DNL Target] perché l&#39;implementazione corrente di [!DNL Target] aggiorna il profilo su ogni richiesta. | Doppio, millisecondi | SES_PROFILE_UPDATE_TIME |
| Visitor Profile - Pages Seen Before Activity | Specifica il numero di visualizzazioni di pagina (impression) totali, inclusa la visita/sessione corrente, fino a quando il visitatore accede all’attività. | Doppio (solo numero intero positivo) 1, 2, 3 e così via. | SES_TOTAL_PAGE_VIEWS |
| Visitor Profile - Page Views in Current Visit | Specifica il numero di visualizzazioni di pagina durante la visita/sessione corrente fino a quando il visitatore accede all’attività. Più precisamente, il numero di impression. Queste impression non sono visualizzazioni di pagina reali, ma il numero di volte in cui la richiesta ha raggiunto [!DNL Target]. [!DNL Target] non è in grado di distinguere tra timeout o altri motivi per cui l&#39;utente non ha ricevuto o visualizzato il contenuto. | Doppio (solo numero intero positivo). | SES_SESSION_POSITION |
| Visitor Profile - Start of Current Visit | Specifica l&#39;ora di inizio della visita/sessione corrente con [!DNL Target]. La visita con [!DNL Target] può essere avviata senza accedere a un&#39;attività. È sufficiente una chiamata a qualsiasi richiesta [!DNL Target]. L’accesso all’attività e l’acquisizione dell’istantanea potrebbero richiedere del tempo. | Doppio, millisecondi | SES_SESSION_START |
| Visitor Profile - Start of Most Recent Visit | Specifica l&#39;ora di inizio dell&#39;ultima visita/sessione con [!DNL Target]. Questo attributo viene aggiornato alla scadenza della sessione.<br>Se si tratta della prima sessione del visitatore, verrà generato `LAST_SESSION_START = 0.` | Doppio, millisecondi | SES_LAST_SESSION_START |
| Visitor Profile - Time Since Most Recent Visit When First Enter Activity | Specifica il tempo trascorso tra la sessione precedente e il momento in cui l’utente accede all’attività e viene acquisita l’istantanea. | Doppio, millisecondi | SES_RECENCY |
| Visitor Profile - Time in Visit Before Enter Activity | Specifica la differenza tra l&#39;ultima interazione con [!DNL Target] e l&#39;inizio della visita corrente. Questo attributo può essere considerato come durata della visita/sessione fino al momento in cui l’utente accede all’attività e viene acquisita l’istantanea.<br>Si verificano valori negativi quando l&#39;inizio della sessione e l&#39;ora dell&#39;ultimo aggiornamento vengono attivati dalla stessa chiamata [!DNL Target]. I valori negativi devono essere considerati 0 (zero). | Doppio, millisecondi | SES_SESSION_TIME |
| Profilo visitatore - Visite totali | Specifica il numero totale di visite/sessioni. La visita/sessione corrente non è inclusa. | Doppio (solo numero intero positivo) 1, 2, 3 e così via. | SES_TOTAL_SESSIONS |
| Visitor Profile - Total Visits to Activity | Specifica il numero di visite a una particolare attività. Se non è presente alcuna visita precedente, viene restituito 0 (zero). | Doppio (solo numero intero positivo) 1, 2, 3 e così via. | SES_PREVIOUS_VISIT_COUNT |
| Visitor Profile - Total Visits to Activity with Conversion | Specifica il numero di visite/sessioni a una particolare attività nel corso delle quali si è verificata almeno una conversione. | Doppio | SES_CUMULATIVE_SUCCESSES |
| Visitor Profile - Visits to Activity with No Conversion | Numero di visite/sessioni a una particolare attività nel corso delle quali non si sono verificate conversioni. Questo valore viene reimpostato su zero dopo una conversione, o su -1 se la conversione non si è mai verificata. | Doppio (solo numero intero positivo) 1, 2, 3 e così via. | SES_SUCCESS_RECENCY |
