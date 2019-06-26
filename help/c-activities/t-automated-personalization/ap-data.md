---
description: Adobe Target raccoglie e usa automaticamente una serie di dati per creare gli algoritmi di personalizzazione nelle attività di Automated Personalization (Personalizzazione automatizzata) (AP) e Auto-Target (AT). Quando un visitatore accede a un’attività di Personalizzazione automatizzata e Targeting automatico, viene trasmessa un’istantanea di informazioni a un set di “record di apprendimento” (i dati del visitatore su cui si baseranno gli algoritmi di personalizzazione).
keywords: dati dell'ambiente; dati sessione; dati geografici; dati geografici; dati dispositivo; dati mobili; attributi; attributi profilo
seo-description: Adobe Target raccoglie e usa automaticamente una serie di dati per creare gli algoritmi di personalizzazione nelle attività di Automated Personalization (Personalizzazione automatizzata) (AP) e Auto-Target (AT). Quando un visitatore accede a un’attività di Personalizzazione automatizzata e Targeting automatico, viene trasmessa un’istantanea di informazioni a un set di “record di apprendimento” (i dati del visitatore su cui si baseranno gli algoritmi di personalizzazione).
seo-title: Raccolta di dati per gli algoritmi di personalizzazione di Adobe Target
solution: Target
title: Raccolta di dati per gli algoritmi di personalizzazione di Target
title-outputclass: premium
topic: Premium
uuid: f5ca2d84-0016-4af5-a139-bca567a3d0e8
badge: premium
translation-type: tm+mt
source-git-commit: 156587a0375fe2dbf8c461e310b2eae04b491b57

---


# ![PREMIUM](/help/assets/premium.png) Raccolta di dati per gli algoritmi di personalizzazione Target{#data-collection-for-the-target-personalization-algorithms}

Target raccoglie e utilizza automaticamente una varietà di dati per creare gli algoritmi di personalizzazione nelle attività di Personalizzazione automatizzata (AP) e Targeting automatico (AT). Quando un visitatore accede a un’attività di Personalizzazione automatizzata e Targeting automatico, viene trasmessa un’istantanea di informazioni a un set di “record di apprendimento” (i dati del visitatore su cui si baseranno gli algoritmi di personalizzazione).

Per ulteriori informazioni sugli algoritmi di personalizzazione di Target, consulta [Algoritmo Foresta casuale](../../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA).

The following table shows the data collected by Automated Personalization and Auto-Target by default, without the marketer having to do anything, as well as the naming convention used to indicate these attributes in [Personalization Insights Reports](../../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767). Puoi aumentare il set di dati di input in qualsiasi momento. Per ulteriori informazioni su come caricare dati aggiuntivi, consulta [Caricamento dei dati per gli algoritmi di personalizzazione Target](../../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6).

| Tipo di dati | Descrizione | Convenzione sulla denominazione del tipo di dati | Attributi di esempio |
| --- | --- | --- | --- |
| [Dati dispositivo e dispositivi mobili](#device-mobile) | Informazioni sul dispositivo e specifiche per dispositivi mobili.<br>Consultate «Dati dispositivo e dispositivi mobili» sotto. | `Device - [device attribute]`<br>`Mobile - [mobile attribute]` | Mobile Device OS<br>Mobile Screen Size |
| [Dati sull&#39;ambiente](#env) | Informazioni sul sistema operativo del visitatore e su come e quando il visitatore accede all&#39;attività. | `Browser - / Operating System] - [Attribute Name]` | Browser - Tipo |
| Segmento Experience Cloud | Audience create in Audience Manager o Analytics e condivise in Experience Cloud | `Custom - Experience Cloud Audience - [Audience Name]` | Dati personalizzati |
| [Dati geografici](#geo) | Informazioni su dove si trova il visitatore.<br>Vedi &quot;Dati geografici&quot; di seguito. | `Geo - [geo attribute]` | City<br>Country<br>Region/State<br>Zip Code<br>Latitude<br>Longitude<br>ISP or Mobile Carrier |
| Attributi del profilo | Script di profilo o attributi direttamente caricati nel profilo di Target tramite l&#39;API Aggiornamento | `Custom - Visitor Profile - [attribute name]` | Dati personalizzati |
| Parametri URL di provenienza | In generale, l’URL di provenienza è quello contenente il riferimento a una pagina particolare che ha avviato la chiamata mbox.<br>Questa variabile può essere influenzata dall’attività degli utenti sul sito e dall’implementazione tecnica del sito. | `Custom - [Referring URL Parameter] - [Parameter value]` | Dati personalizzati |
| Segmenti di reporting | Qualsiasi segmento configurato nella configurazione dell&#39;attività. | `Reporting Segment -[Segment Name]` | Dati personalizzati |
| [Dati sessione](#session) | Informazioni sul comportamento del visitatore nella sessione quando si accede all&#39;attività. | `Visitor Profile - [Attribute Name]` | Profilo visitatore - Inizio della visita più recente |
| parametri URL | Target esamina l’URL per estrarre i parametri URL. | `Custom - URL Parameter - [URL Parameter]` | Dati personalizzati |

Le sezioni seguenti contengono informazioni dettagliate sui vari tipi di dati, tra cui nomi di attributi, descrizioni e valori di esempio.

## Device and Mobile data {#device-mobile}

| Attribute name | Descrizione attributo | Valori di esempio |
| --- | --- | --- |
| Mobile - Dispositivo - Marchio | Il marchio del dispositivo mobile utilizzato per accedere all&#39;attività. | Apple |
| Mobile - Dispositivo - ereader | Specifica se il dispositivo è un ereader. | 0 è False, 1 è True |
| Mobile - Dispositivo - Console giochi | Specifica se il dispositivo è una console di giochi. | 0 è False, 1 è True |
| Mobile - Dispositivo - Media Player | Specifica se il dispositivo è un lettore multimediale. | 0 è False, 1 è True |
| Mobile - Dispositivo - Telefono cellulare | Specifica se il dispositivo è un cellulare. | 0 è False, 1 è True |
| Mobile - Dispositivo - Nome modello | Il nome del modello del dispositivo mobile utilizzato per accedere all&#39;attività. | Iphone XS |
| Dispositivo - Set-Top Box | Specifica se il dispositivo è un set-top box. | 0 è False, 1 è True |
| Mobile - Dispositivo - Tablet | Specifica se il dispositivo è un tablet. | 0 è False, 1 è True |
| Mobile - Densità pixel (ppi) | La densità pixel del dispositivo mobile usata per accedere all&#39;attività. | 1, 2, 3, ecc. |
| Mobile - OS - OSX (Android, Windows, ecc.) | Specifica se l&#39;utente ha utilizzato un OSX (o Android, Windows, ecc.) dispositivo per accedere all&#39;attività. | 0 è False, 1 è True |
| Mobile - Altezza schermo (px) | L&#39;altezza dello schermo del dispositivo mobile (in pixel) utilizzato per accedere all&#39;attività. | 1, 2, 3, ecc. |
| Mobile - Larghezza schermo (px) | La larghezza dello schermo del dispositivo mobile (in pixel) utilizzato per accedere all&#39;attività. | 1, 2, 3, ecc. |

## Environmental data {#env}

| Attribute name | Descrizione attributo | Valori di esempio |
| --- | --- | --- |
| Browser - Giorno della settimana | Il giorno della settimana in cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | Da 0 a 6.<br>(0 è domenica) |
| Browser - Ora del giorno | L&#39;ora del giorno in cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | 0 to 23<br>(0 is midnight) |
| Browser - Ora della settimana | L&#39;ora della settimana in cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | 0 to 168<br>(Sunday midnight is 0) |
| Browser - Impostazioni lingua | La lingua specificata nel browser del visitatore utilizzato per accedere all&#39;attività. | English<br>German |
| Browser - Altezza schermo (px) | L&#39;altezza dello schermo del browser del dispositivo (in pixel) utilizzato per accedere all&#39;attività. | 1, 2, 3, ecc. |
| Browser - Ora del giorno | L&#39;ora del browser in cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | 0, 6, 12, 18<br>(0 is night, 6 is morning,<br>12 is afternoon, 18 is evening) |
| Browser - Fuso orario | Il fuso orario del visitatore durante l&#39;accesso all&#39;attività. | Pacific Time<br>Eastern Time<br>GMT |
| Browser - Tipo | Il tipo di browser utilizzato dal visitatore durante l&#39;accesso all&#39;attività. | Chrome<br>Firefox<br>Internet Explorer<br>Safari<br>Other |
| Browser - Giorno feriale/fine settimana | Lo stato del lavoro quando il visitatore accede all&#39;attività (fine settimana, orario di lavoro o giorno della settimana). | Saturday and Sunday is weekend<br>Monday-Friday 0900 to 1800 is work time<br>Monday-Friday after 1800 until 0900 is weekday free time |
| Browser - Altezza finestra (px) | L&#39;altezza della finestra del browser (in pixel) utilizzato per accedere all&#39;attività. | 1, 2, 3, ecc. |
| Browser - Larghezza finestra (px) | La larghezza della finestra del browser (in pixel) utilizzato per accedere all&#39;attività. | 1, 2, 3, ecc. |
| Dispositivo - Altezza schermo | L&#39;altezza dello schermo del dispositivo utilizzata per accedere all&#39;attività. | 1, 2, 3, ecc. |
| Dispositivo - Larghezza schermo | La larghezza dello schermo del dispositivo utilizzata per accedere all&#39;attività. | 1, 2, 3, ecc. |
| Sistema operativo | Il sistema operativo sul dispositivo del visitatore utilizzato per accedere all&#39;attività. | Mac OS<br>Windows<br>Linux<br>Search Bot<br>Unknown OS |
| Sistema operativo - Versione | La versione del sistema operativo che il visitatore ha utilizzato per accedere all&#39;attività. | Windows 10<br>Mac OS 10 |
| Origini di traffico - URL pagina di destinazione di provenienza | La prima pagina visualizzata dal visitatore all&#39;accesso al sito. | `https://www.adobe.com/ecloud.html` |

## Geographical data {#geo}

| Attribute name | Descrizione attributo | Valori di esempio |
| --- | --- | --- |
| Geo - Città | La città da cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | San Francisco |
| Geo - Paese | Il Paese da cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | Germania |
| Geo - DMA | L&#39;Area di marketing designata (DMA) da cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | Charlottesville |
| Geo - Latitudine | Latitudine da cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | 47.269<br>Rounded to 3 decimal places (approximately 100 meters accuracy) |
| Geo - Longitudine | Longitudine da cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | -122.269<br>Rounded to 3 decimal places (approximately 100 meters accuracy) |
| Geo - Regione/Regione | Lo stato o l&#39;area in cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | Utah<br>New South Wales |
| Geo - CAP | Codice Zip da cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | 84004 |
| Mobile - Gestore | Il gestore mobile utilizzato dal visitatore per accedere all&#39;attività. | Vodafone<br>T-Mobile |
| Rete - Velocità di connessione | La velocità di connessione di rete del dispositivo quando il visitatore ha effettuato l&#39;accesso all&#39;attività. | Broadband<br>Cable<br>DSL<br>Mobile<br>Wireless<br>Satellite |
| Rete - Nome dominio | Il nome del dominio di rete dal quale il visitatore ha effettuato l&#39;accesso all&#39;attività. | `nnt.net` |
| Rete - ISP | La rete dalla quale il visitatore ha effettuato l&#39;accesso all&#39;attività. | nnt communications corporation |

## Session data {#session}

| Attribute name | Descrizione attributo | Valori di esempio |
| --- | --- | --- |
| Profilo visitatore - Valore dell&#39;ordine del ciclo di vita dell&#39;attività | Specifica la somma di tutti i valori degli ordini per tutte le visite/sessioni a una particolare attività. | Due volte |
| Profilo visitatore - Tempo dell&#39;attività sul sito | Specifica il tempo totale trascorso sul sito, escluso la sessione corrente, e viene aggiornato al termine della sessione. | Due, millisecondi |
| Profilo visitatore -visualizzazioni di pagina medio per visita durante l&#39;attività | Specifica il numero medio di visualizzazioni di pagina per sessione, escludendo la sessione corrente. | Due volte |
| Profilo visitatore - Tempo medio per percorso | Specifica il tempo medio trascorso per visita/sessione. Questa non include la sessione corrente. | Due, millisecondi |
| Profilo visitatore - Prima visita | Specifica l&#39;ora della prima visita che l&#39;utente ha interagito con Target. | Due, millisecondi |
| Profilo visitatore - Ore dall&#39;ultima visita | Specifica le ore dall&#39;ultima visita a questa attività specifica. | Due (numero intero intero) 1, 2, 3, ecc. |
| Profilo visitatore - Impression di posizione/contenuto | Specifica il numero di impression a una particolare combinazione di posizione/contenuto in una particolare attività. | Due (numero intero intero) 1, 2, 3, ecc. |
| Profilo visitatore - Interazione ultima destinazione | Specifica l&#39;ora dell&#39;ultima interazione con Target. L&#39;interazione avviene su ogni richiesta mbox perché l&#39;implementazione corrente di Target aggiorna il profilo su ogni richiesta. | Due, millisecondi |
| Profilo visitatore - Pagine visualizzate prima dell&#39;attività | Specifica il numero di visualizzazioni di pagina (impression) totali, incluse quelle correnti, fino a quando il visitatore non immette l&#39;attività. | Due (numero intero intero) 1, 2, 3, ecc. |
| Profilo visitatore - Visualizzazioni pagina in visita corrente | Specifica il numero di visualizzazioni di pagina nella visita/sessione corrente finché il visitatore non immette l&#39;attività. Con maggiore precisione, il numero di impression. Queste impression non sono visualizzazioni di pagina reali, ma si tratta del numero di volte in cui la richiesta raggiunge Target. Target non è in grado di distinguere tra timeout o altri motivi per cui l&#39;utente non ha ricevuto o visualizzato il contenuto. | Double (numero intero intero) |
| Profilo visitatore - Inizio della visita corrente | Specifica l&#39;ora in cui è iniziata la visita/sessione corrente con Target. La visita con Target può essere avviata senza immettere un&#39;attività. È richiesta una chiamata a qualsiasi mbox. Un visitatore potrebbe richiedere un po&#39; di tempo fino all&#39;immissione dell&#39;attività e l&#39;istantanea viene ripresa. | Due, millisecondi |
| Profilo visitatore - Inizio della visita più recente | Specifica l&#39;ora dell&#39;ultima visita/sessione con Target avviata. Questo attributo viene aggiornato al termine della sessione.<br>Se questa è la prima sessione per il visitatore, verrà generato `LAST_SESSION_START = 0.` | Due, millisecondi |
| Profilo visitatore: ora dalla visita più recente al primo accesso | Specifica la durata tra la sessione precedente e quella in cui l&#39;utente immette l&#39;attività e l&#39;istantanea viene eseguita. | Due, millisecondi |
| Profilo visitatore: tempo in Visita prima di entrare nell&#39;attività | Specifica la differenza tra l&#39;ultima interazione con Target e l&#39;avvio della visita corrente. Questo attributo può essere considerato come durata della visita/sessione finché l&#39;utente non immette l&#39;attività e l&#39;istantanea viene eseguita.<br>I valori negativi si verificano quando inizia la sessione e l&#39;ultimo tempo di aggiornamento viene attivato dalla stessa chiamata mbox. I valori negativi devono essere considerati 0 (zero). | Due, millisecondi |
| Profilo visitatore - Visite totali | Specifica il numero totale di visite/sessioni. Non include la visita/sessione corrente. | Due (numero intero intero) 1, 2, 3, ecc. |
| Profilo visitatore - Totale visite all&#39;attività | Specifica il numero di visite a una particolare attività. Se non è presente una visita precedente, restituisce 0 (zero). | Due (numero intero intero) 1, 2, 3, ecc. |
| Profilo visitatore - Totale visite all&#39;attività con conversione | Specifica il numero di visite/sessioni a una particolare attività in caso di almeno una conversione durante la visita. | Due volte |
| Profilo visitatore - Visite all&#39;attività senza conversione | Numero di visite/sessioni senza conversioni a una particolare attività. Questo valore viene reimpostato su zero dopo la conversione, o -1 se la conversione non è mai avvenuta. | Due (numero intero intero) 1, 2, 3, ecc. |
