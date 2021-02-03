---
keywords: dati ambiente;dati sessione;dati geografici;dati geo;dati dispositivo;dati mobili;attributi;attributi profilo
description: Adobe Target raccoglie e utilizza automaticamente una varietà di dati per creare gli algoritmi di personalizzazione nelle attività di Personalizzazione automatizzata e Targeting automatico. Quando un visitatore accede a un’attività di Personalizzazione automatizzata e Targeting automatico, viene trasmessa un’istantanea di informazioni a un set di “record di apprendimento” (i dati del visitatore su cui si baseranno gli algoritmi di personalizzazione).
title: Raccolta di dati per gli algoritmi di personalizzazione
feature: Automated Personalization
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '1767'
ht-degree: 92%

---


# ![PREMIUM](/help/assets/premium.png) Raccolta di dati per gli algoritmi di personalizzazione Target

[!DNL Adobe Target] raccoglie e utilizza automaticamente una varietà di dati per creare i propri algoritmi di personalizzazione nelle attività di  [!UICONTROL  Automated Personalization] (AP) e  [!UICONTROL Auto-Target] (AT). Quando un visitatore immette un&#39;attività AP o AT, uno snapshot di informazioni viene trasmesso a un set di &quot;record di formazione&quot; (i dati del visitatore sui quali gli algoritmi di personalizzazione impareranno).

Per ulteriori informazioni sugli algoritmi di personalizzazione di Target, consulta [Algoritmo Foresta casuale](/help/c-activities/t-automated-personalization/algo-random-forest.md).

La tabella seguente mostra i dati raccolti da [!UICONTROL  Automated Personalization] e [!UICONTROL Auto-Target] per impostazione predefinita, senza che l&#39;esperto di marketing debba fare nulla, nonché la convenzione di denominazione utilizzata per indicare questi attributi in [Report approfondimenti sulla personalizzazione](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767). Puoi aumentare il set di dati di input in qualsiasi momento. Per ulteriori informazioni su come caricare dati aggiuntivi, consulta [Caricamento dei dati per gli algoritmi di personalizzazione Target](/help/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

| Tipo di dati | Descrizione | Convenzione sulla denominazione del tipo di dati | Attributi di esempio |
| --- | --- | --- | --- |
| [Dati mobili e sul dispositivo](#device-mobile) | Informazioni sul dispositivo e specifiche per dispositivi mobili.<br>Consulta “Dati mobili e sul dispositivo”, qui sotto. | `Device - [device attribute]`<br>`Mobile - [mobile attribute]` | Sistema operativo del dispositivo<br>Dimensioni schermo |
| [Dati sull’ambiente](#env) | Informazioni sul sistema operativo del visitatore e su come e quando il visitatore accede all’attività. | `Browser - / Operating System] - [Attribute Name]` | Browser - Type |
| Segmento Experience Cloud | Tipi di pubblico creati in Audience Manager o Analytics e condivise in Experience Cloud | `Custom - Experience Cloud Audience - [Audience Name]` | Dati personalizzati |
| [Dati geografici](#geo) | Informazioni su dove si trova il visitatore.<br>Vedi “Dati geografici”, di seguito. | `Geo - [geo attribute]` | Città<br>Paese<br>Provincia/Stato<br>Codice postale<br>Latitudine<br>Longitudine<br>ISP o gestore di telefonia mobile |
| Attributi del profilo | Script di profilo o attributi direttamente caricati nel profilo di Target tramite l’API di aggiornamento | `Custom - Visitor Profile - [attribute name]` | Dati personalizzati |
| Parametri URL di riferimento | In generale, l’URL di riferimento è l’URL che fa riferimento a una pagina specifica che ha avviato la chiamata Target.<br>Questa variabile può essere influenzata dall’attività degli utenti sul sito e dall’implementazione tecnica del sito. | `Custom - [Referring URL Parameter] - [Parameter value]` | Dati personalizzati |
| Segmenti di reporting | Qualsiasi segmento configurato nella configurazione dell’attività. | `Reporting Segment -[Segment Name]` | Dati personalizzati |
| [Dati sessione](#session) | Informazioni sul comportamento del visitatore durante la sessione di accesso all’attività. | `Visitor Profile - [Attribute Name]` | Visitor Profile - Start of Most Recent Visit |
| Parametri URL | Target esamina l’URL per estrarre i parametri URL. | `Custom - URL Parameter - [URL Parameter]` | Dati personalizzati |

Le sezioni seguenti contengono informazioni dettagliate sui vari tipi di dati, tra cui nomi di attributi, descrizioni e valori di esempio.

## Dati mobili e sul dispositivo {#device-mobile}

| Nome attributo | Descrizione attributo | Valori di esempio |
| --- | --- | --- |
| Mobile - Device - Brand | Il marchio del dispositivo mobile utilizzato per accedere all’attività. | Apple |
| Mobile - Device - eReader | Specifica se il dispositivo è un eReader. | 0 = False, 1 = True |
| Mobile - Device - Game Console | Specifica se il dispositivo è una console di giochi. | 0 = False, 1 = True |
| Mobile - Device - Media Player | Specifica se il dispositivo è un lettore multimediale. | 0 = False, 1 = True |
| Mobile - Device - Mobile Phone | Specifica se il dispositivo è un telefono cellulare. | 0 = False, 1 = True |
| Mobile - Device - Model Name | Il nome del modello del dispositivo mobile utilizzato per accedere all’attività. | iPhone XS |
| Device - Set-Top Box | Specifica se il dispositivo è un decoder. | 0 = False, 1 = True |
| Mobile - Device - Tablet | Specifica se il dispositivo è un tablet. | 0 = False, 1 = True |
| Mobile - Pixel Density (ppi) | La densità pixel del marchio del dispositivo mobile utilizzato per accedere all’attività. | 1, 2, 3, ecc. |
| Mobile - OS - OSX (Android, Windows, ecc.) | Specifica se l’utente ha utilizzato un dispositivo con sistema operativo OSX (o Android, Windows, ecc.) per accedere all’attività. | 0 = False, 1 = True |
| Mobile - Screen Height (px) | L’altezza (in pixel) dello schermo del dispositivo mobile utilizzato per accedere all’attività. | 1, 2, 3, ecc. |
| Mobile - Screen Width (px) | La larghezza (in pixel) dello schermo del dispositivo mobile utilizzato per accedere all’attività. | 1, 2, 3, ecc. |

## Dati sull’ambiente {#env}

| Nome attributo | Descrizione attributo | Valori di esempio |
| --- | --- | --- |
| Browser - Day of Week | Il giorno della settimana in cui il visitatore ha effettuato l’accesso all’attività. | Da 0 a 6.<br>(0 = domenica) |
| Browser - Hour of Day | L’ora del giorno in cui il visitatore ha effettuato l’accesso all’attività. | Da 0 a 23<br>(0 = mezzanotte) |
| Browser - Hour of Week | L’ora della settimana in cui il visitatore ha effettuato l’accesso all’attività. | Da 0 a 168<br>(0 = mezzanotte di domenica) |
| Browser - Language Setting | La lingua specificata nel browser del visitatore utilizzato per accedere all’attività. | English<br>German |
| Browser - Screen Height (px) | L’altezza (in pixel) dello schermo del browser del dispositivo mobile utilizzato per accedere all’attività. | 1, 2, 3, ecc. |
| Browser - Time of Day | L’ora del giorno del browser nel momento in cui il visitatore ha effettuato l’accesso all’attività. | 0, 6, 12, 18<br>(0 = notte, 6 = mattina,<br>12 = pomeriggio, 18 = sera) |
| Browser - Timezone | Il fuso orario del visitatore durante l’accesso all’attività. | Pacific Time<br>Eastern Time<br>GMT |
| Browser - Tipo | Il tipo di browser utilizzato dal visitatore per accedere all’attività. | Chrome<br>Firefox<br>Internet Explorer<br>Safari<br>Other |
| Browser - Weekday/Weekend | Lo stato lavorativo del giorno in cui il visitatore accede all’attività (fine settimana, orario lavorativo, orario non lavorativo infrasettimanale). | weekend = sabato e domenica<br>work time = lunedì-venerdì dalle 0900 alle 1800<br>weekday free time = lunedì-venerdì dalle 1800 alle 0900 |
| Browser - Window Height (px) | L’altezza (in pixel) della finestra del browser utilizzato per accedere all’attività. | 1, 2, 3, ecc. |
| Browser - Window Width (px) | La larghezza (in pixel) della finestra del browser utilizzato per accedere all’attività. | 1, 2, 3, ecc. |
| Device - Screen Height | L’altezza (in pixel) dello schermo del dispositivo mobile utilizzato per accedere all’attività. | 1, 2, 3, ecc. |
| Device - Screen Width | La larghezza (in pixel) dello schermo del dispositivo mobile utilizzato per accedere all’attività. | 1, 2, 3, ecc. |
| Sistema operativo | Il sistema operativo del dispositivo utilizzato dal visitatore per accedere all’attività. | Mac OS<br>Windows<br>Linux<br>Search Bot<br>OS Unknown |
| Operating System - Version | La versione del sistema operativo utilizzato dal visitatore per accedere all’attività. | Windows 10<br>Mac OS 10 |
| Traffic Sources - Referring Landing Page URL | La prima pagina visualizzata dal visitatore all’accesso al sito. | `https://www.adobe.com/ecloud.html` |

## Dati geografici {#geo}

| Nome attributo | Descrizione attributo | Valori di esempio |
| --- | --- | --- |
| Geo - City | La città da cui il visitatore ha effettuato l’accesso all’attività. | San Francisco |
| Geo - Country | Il paese da cui il visitatore ha effettuato l’accesso all’attività. | Germania |
| Geo - DMA | L’area di marketing designata (DMA) da cui il visitatore ha effettuato l’accesso all’attività. | Charlottesville |
| Geo - Latitude | La latitudine da cui il visitatore ha effettuato l’accesso all’attività. | 47,269<br>Arrotondato a 3 cifre decimali (precisione di circa 100 metri) |
| Geo - Longitude | La longitudine da cui il visitatore ha effettuato l’accesso all’attività. | -122,269<br>Arrotondato a 3 cifre decimali (precisione di circa 100 metri) |
| Geo - State/Region | Lo stato o la provincia da cui il visitatore ha effettuato l’accesso all’attività. | Utah<br>New South Wales |
| Geo - Zip Code | Codice postale da cui il visitatore ha effettuato l’accesso all’attività. | 84004 |
| Mobile - Carrier | Il gestore di telefonia mobile utilizzato dal visitatore per accedere all’attività. | Vodafone<br>T-Mobile |
| Network - Connection Speed | La velocità di connessione di rete del dispositivo quando il visitatore ha effettuato l’accesso all’attività. | Broadband<br>Cable<br>DSL<br>Mobile<br>Wireless<br>Satellite |
| Network - Domain Name | Il nome del dominio della rete dalla quale il visitatore ha effettuato l’accesso all’attività. | `nnt.net` |
| Network - ISP | La rete dalla quale il visitatore ha effettuato l’accesso all’attività. | nnt communications corporation |

## Dati sessione {#session}

| Nome attributo | Descrizione attributo | Valori di esempio |
| --- | --- | --- |
| Visitor Profile - Activity Lifetime Order Value | Specifica la somma di tutti i valori degli ordini per tutte le visite/sessioni di una particolare attività. | Doppio |
| Visitor Profile - Activity Lifetime Time on Site | Specifica il tempo totale trascorso dal visitatore sul sito, esclusa la sessione corrente, e viene aggiornato al termine della sessione. | Doppio, millisecondi |
| Visitor Profile -Average Page Views per Visit during Activity | Specifica il numero medio di visualizzazioni pagina per sessione, esclusa la sessione corrente. | Doppio |
| Visitor Profile - Average Time per Visit | Specifica il tempo medio trascorso per visita/sessione. La sessione corrente non è inclusa. | Doppio, millisecondi |
| Visitor Profile - First Visit | Specifica l’ora della prima visita durante la quale il visitatore ha interagito con Target. | Doppio, millisecondi |
| Visitor Profile - Hours since Last Visit | Specifica quante ore sono trascorse dall’ultima visita a questa attività specifica. | Doppio (solo numero intero positivo) 1, 2, 3, ecc. |
| Visitor Profile - Impressions of Location/Content | Specifica il numero di impression per una particolare combinazione di posizione/contenuto in una particolare attività. | Doppio (solo numero intero positivo) 1, 2, 3, ecc. |
| Visitor Profile - Last Target Interaction | Specifica l’ora dell’ultima interazione con Target. L&#39;interazione avviene su ogni richiesta [!DNL Target] perché l&#39;implementazione corrente di [!DNL Target] aggiorna il profilo su ogni richiesta. | Doppio, millisecondi |
| Visitor Profile - Pages Seen Before Activity | Specifica il numero di visualizzazioni pagina (impression) totali, inclusa la visita/sessione corrente, fino a quando il visitatore accede all’attività. | Doppio (solo numero intero positivo) 1, 2, 3, ecc. |
| Visitor Profile - Page Views in Current Visit | Specifica il numero di visualizzazioni pagina durante la visita/sessione corrente fino a quando il visitatore accede all’attività. Più precisamente, il numero di impression. Le impression non sono visualizzazioni di pagina reali, ma piuttosto quante volte la richiesta è stata ricevuta da Target. Target non è in grado di distinguere tra timeout o altri motivi per cui l’utente potrebbe non ricevere o visualizzare effettivamente il contenuto. | Doppio (solo numero intero positivo). |
| Visitor Profile - Start of Current Visit | Specifica l’ora in cui è iniziata la visita/sessione corrente con Target. La visita con Target può essere avviata senza accedere a un’attività. Tutto ciò che è richiesto è una chiamata a qualsiasi richiesta [!DNL Target]. Potrebbe trascorrere un po’ di tempo prima che il visitatore acceda all’attività e venga acquisita l’istantanea. | Doppio, millisecondi |
| Profilo visitatore - Inizio della visita più recente | Specifica l’ora in cui è iniziata l’ultima visita/sessione con Target. Questo attributo viene aggiornato alla scadenza della sessione.<br>Se si tratta della prima sessione del visitatore, verrà generato `LAST_SESSION_START = 0.` | Doppio, millisecondi |
| Visitor Profile - Time Since Most Recent Visit When First Enter Activity | Specifica il tempo trascorso tra la sessione precedente e il momento in cui l’utente accede all’attività e viene acquisita l’istantanea. | Doppio, millisecondi |
| Visitor Profile - Time in Visit Before Enter Activity | Specifica la differenza tra l’ultima interazione con Target e l’inizio della visita corrente. Questo attributo può essere considerato come durata della visita/sessione fino al momento in cui l’utente accede all’attività e viene acquisita l’istantanea.<br>[!DNL Target]Vengono riportati valori negativi quando l’inizio della sessione e l’ultima ora di aggiornamento vengono attivati dalla stessa chiamata I valori negativi devono essere considerati 0 (zero). | Doppio, millisecondi |
| Profilo visitatore - Visite totali | Specifica il numero totale di visite/sessioni. La visita/sessione corrente non è inclusa. | Doppio (solo numero intero positivo) 1, 2, 3, ecc. |
| Visitor Profile - Total Visits to Activity | Specifica il numero di visite a una particolare attività. Se non è presente alcuna visita precedente, viene restituito 0 (zero). | Doppio (solo numero intero positivo) 1, 2, 3, ecc. |
| Visitor Profile - Total Visits to Activity with Conversion | Specifica il numero di visite/sessioni a una particolare attività nel corso delle quali si è verificata almeno una conversione. | Doppio |
| Visitor Profile - Visits to Activity with No Conversion | Numero di visite/sessioni a una particolare attività nel corso delle quali non si sono verificate conversioni. Questo valore viene reimpostato su zero dopo una conversione, o su -1 se la conversione non si è mai verificata. | Doppio (solo numero intero positivo) 1, 2, 3, ecc. |
