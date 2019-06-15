---
description: Target raccoglie e utilizza automaticamente una varietà di dati per creare gli algoritmi di personalizzazione nelle attività di Personalizzazione automatizzata (AP) e Targeting automatico (AT). Quando un visitatore accede a un’attività di Personalizzazione automatizzata e Targeting automatico, viene trasmessa un’istantanea di informazioni a un set di “record di apprendimento” (i dati del visitatore su cui si baseranno gli algoritmi di personalizzazione).
seo-description: Adobe Target raccoglie e usa automaticamente una serie di dati per creare gli algoritmi di personalizzazione nelle attività di Automated Personalization (Personalizzazione automatizzata) (AP) e Auto-Target (AT). Quando un visitatore accede a un’attività di Personalizzazione automatizzata e Targeting automatico, viene trasmessa un’istantanea di informazioni a un set di “record di apprendimento” (i dati del visitatore su cui si baseranno gli algoritmi di personalizzazione).
seo-title: Raccolta di dati per gli algoritmi di personalizzazione di Adobe Target
solution: Target
title: Raccolta di dati per gli algoritmi di personalizzazione di Target
title-outputclass: premium
topic: Premium
uuid: f5ca2d84-0016-4af5-a139-bca567a3d0e8
badge: premium
translation-type: tm+mt
source-git-commit: 1662c5e83a3712626536a659e5001cd537343883

---


# ![PREMIUM](/help/assets/premium.png) Raccolta di dati per gli algoritmi di personalizzazione Target{#data-collection-for-the-target-personalization-algorithms}

Target raccoglie e utilizza automaticamente una varietà di dati per creare gli algoritmi di personalizzazione nelle attività di Personalizzazione automatizzata (AP) e Targeting automatico (AT). Quando un visitatore accede a un’attività di Personalizzazione automatizzata e Targeting automatico, viene trasmessa un’istantanea di informazioni a un set di “record di apprendimento” (i dati del visitatore su cui si baseranno gli algoritmi di personalizzazione).

Per ulteriori informazioni sugli algoritmi di personalizzazione di Target, consulta [Algoritmo Foresta casuale](../../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA).

La tabella seguente mostra i dati raccolti da Personalizzazione automatica per impostazione predefinita, senza la necessità di eseguire alcuna operazione, nonché la convenzione di denominazione utilizzata per indicare questi attributi nei [rapporti Approfondimenti personalizzazione](../../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767). Puoi aumentare il set di dati di input in qualsiasi momento. Per ulteriori informazioni su come caricare dati aggiuntivi, consulta [Caricamento dei dati per gli algoritmi di personalizzazione Target](../../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6).

| Tipo di dati | Descrizione | Convenzione sulla denominazione del tipo di dati | Attributi di esempio |
| --- | --- | --- | --- |
| Parametri URL | Target esamina l’URL per estrarre i parametri URL. | `Custom - URL Parameter - [URL Parameter]` | Dati personalizzati |
| Parametri URL di provenienza | In generale, l’URL di provenienza è quello contenente il riferimento a una pagina particolare che ha avviato la chiamata mbox.<br>Questa variabile può essere influenzata dall’attività degli utenti sul sito e dall’implementazione tecnica del sito. | `Custom - [Referring URL Parameter] - [Parameter value]` | Dati personalizzati |
| Dati ambientali e di sessione | Informazioni su come e quando l’utente accede all’attività.<br>Vedi &quot;Dati sull&#39;ambiente e sessione&quot; di seguito. | `Visitor Profile - [attribute name]`<br>`Browser - [browser attribute]`<br>`Operating System - [OS attribute]` | Profilo del visitatore - Inizio visita più recente<br>Profilo del visitatore - Totale visite<br>Profilo del visitatore - Durata media per visita<br>Browser - Fuso orario<br>Browser - Giorno della settimana<br>Browser - Impostazioni della lingua<br>Browser - Tipo<br>Sistema operativo - Versione |
| Geografico | Informazioni su dove si trova il visitatore.<br>Vedi &quot;Dati geografici&quot; di seguito. | `Geo - [geo attribute]` | Citycountryregion<br><br>/statezip<br>codelatitudelongitudeisp<br><br><br>o Mobile Carrier |
| Dati mobili e sul dispositivo | Informazioni sul dispositivo e specifiche per dispositivi mobili.<br>Consultate «Dati dispositivo e dispositivi mobili» sotto. | `Device - [device attribute]`<br>`Mobile - [mobile attribute]` | Dispositivo mobile osmobile<br>Dimensioni schermo |

Le sezioni seguenti contengono informazioni dettagliate sui vari tipi di dati, tra cui nomi di attributi, descrizioni e valori di esempio.

>[!NOTE]
>
>Alcuni dei valori delle tabelle seguenti sono stati arrotondati al numero intero più vicino o all&#39;ora.

## Dati sull&#39;ambiente e sessione

| Attribute name | Descrizione attributo | Valori di esempio |
| --- | --- | --- |
| Browser - Giorno della settimana | Il giorno della settimana in cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | Da 0 a 6.<br>(0 è domenica) |
| Browser - Ora del giorno | L&#39;ora del giorno in cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | Da 0 a 23<br>(0 è mezzanotte) |
| Browser - Ora della settimana | L&#39;ora della settimana in cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | Da 0 a 168<br>(mezzanotte mezzanotte è 0) |
| Browser - Impostazioni lingua | La lingua specificata nel browser del visitatore utilizzato per accedere all&#39;attività. | Inglese<br> |
| Browser - Altezza schermo (px) | L&#39;altezza dello schermo del browser del dispositivo (in pixel) utilizzato per accedere all&#39;attività. | 1, 2, 3, ecc. |
| Browser - Ora del giorno | L&#39;ora del browser in cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | 0, 6, 12, 18<br>(0 è notte, 6 è mattina, 12 è pomeriggio, 18 è sera) |
| Browser - Fuso orario | Il fuso orario del visitatore durante l&#39;accesso all&#39;attività. | Pacific timeeastern<br>timegmt<br> |
| Browser - Tipo | Il tipo di browser utilizzato dal visitatore durante l&#39;accesso all&#39;attività. | Chromefirefoxinternet<br><br>explorersafarielse<br><br> |
| Browser - Giorno feriale/fine settimana | Lo stato del lavoro quando il visitatore accede all&#39;attività (fine settimana, orario di lavoro o giorno della settimana). | Sabato e Domenica sono weekendmonday<br>tramite venerdì da 0900 a 1800, mentre timemonday<br>e venerdì dopo il 0900 sono giorni feriali |
| Browser - Altezza finestra (px) | L&#39;altezza della finestra del browser (in pixel) utilizzato per accedere all&#39;attività. | 1, 2, 3, ecc. |
| Browser - Larghezza finestra (px) | La larghezza della finestra del browser (in pixel) utilizzato per accedere all&#39;attività. | 1, 2, 3, ecc. |
| Dispositivo - Altezza schermo | L&#39;altezza dello schermo del dispositivo utilizzata per accedere all&#39;attività. | 1, 2, 3, ecc. |
| Dispositivo - Larghezza schermo | La larghezza dello schermo del dispositivo utilizzata per accedere all&#39;attività. | 1, 2, 3, ecc. |
| Mobile &gt; Densità pixel (ppi) | La densità pixel del dispositivo mobile usata per accedere all&#39;attività. | 1, 2, 3, ecc. |
| Sistema operativo | Il sistema operativo sul dispositivo del visitatore utilizzato per accedere all&#39;attività. | Mac oswindowslinuxsearch<br><br><br>botunknown<br>OS |
| Sistema operativo - Versione | La versione del sistema operativo che il visitatore ha utilizzato per accedere all&#39;attività. | Windows 10<br>Mac OS 10 |
| Origini di traffico - URL pagina di destinazione di provenienza | La prima pagina visualizzata dal visitatore all&#39;accesso al sito. | `https://www.adobe.com/ecloud.html` |

## Dati geografici

| Attribute name | Descrizione attributo | Valori di esempio |
| --- | --- | --- |
| Geo - Città | La città da cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | San Francisco |
| Geo - Paese | Il Paese da cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | Germania |
| Geo - DMA | L&#39;Area di marketing designata (DMA) da cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | Charlottesville |
| Geo - Latitudine | Latitudine da cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | 47.269<br>Arrotondato a 3 posizioni decimali (precisione circa 100 metri) |
| Geo - Longitudine | Longitudine da cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | -122.269<br>Arrotondato a 3 posizioni decimali (precisione circa 100 metri) |
| Geo - Regione/Regione | Lo stato o l&#39;area in cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | Utahnew<br>South Wales |
| Geo - CAP | Codice Zip da cui il visitatore ha effettuato l&#39;accesso all&#39;attività. | 84004 |
| Mobile - Gestore | Il gestore mobile utilizzato dal visitatore per accedere all&#39;attività. | Vodafonet<br>-Mobile |
| Rete - Velocità di connessione | La velocità di connessione di rete del dispositivo quando il visitatore ha effettuato l&#39;accesso all&#39;attività. | Broadbandcabledslmobilewirelesssatellite<br><br><br><br><br> |
| Rete - Nome dominio | Il nome del dominio di rete dal quale il visitatore ha effettuato l&#39;accesso all&#39;attività. | `nnt.net` |
| Rete - ISP | La rete dalla quale il visitatore ha effettuato l&#39;accesso all&#39;attività. | nnt communications corporation |

## Dati dispositivo e dispositivi mobili

| Attribute name | Descrizione attributo | Valori di esempio |
| --- | --- | --- |
| Mobile - Dispositivo - Marchio | Il marchio del dispositivo mobile utilizzato per accedere all&#39;attività. | Apple |
| Mobile - Dispositivo - Nome modello | Il nome del modello del dispositivo mobile utilizzato per accedere all&#39;attività. | Iphone XS |
| Mobile - OS - OSX | Specifica se l&#39;utente utilizza un dispositivo OSX per accedere all&#39;attività. | 0 è False, 1 è True |
| Mobile - Altezza schermo (px) | L&#39;altezza dello schermo del dispositivo mobile (in pixel) utilizzato per accedere all&#39;attività. | 1, 2, 3, ecc. |
| Mobile - Larghezza schermo (px) | La larghezza dello schermo del dispositivo mobile (in pixel) utilizzato per accedere all&#39;attività. | 1, 2, 3, ecc. |