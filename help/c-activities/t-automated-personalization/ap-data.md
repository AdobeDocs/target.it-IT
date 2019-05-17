---
description: Target raccoglie e utilizza automaticamente una varietà di dati per creare gli algoritmi di personalizzazione nelle attività di Personalizzazione automatizzata (AP) e Targeting automatico (AT). Quando un visitatore accede a un’attività di Personalizzazione automatizzata e Targeting automatico, viene trasmessa un’istantanea di informazioni a un set di “record di apprendimento” (i dati del visitatore su cui si baseranno gli algoritmi di personalizzazione).
seo-description: Target raccoglie e utilizza automaticamente una varietà di dati per creare gli algoritmi di personalizzazione nelle attività di Personalizzazione automatizzata (AP) e Targeting automatico (AT). Quando un visitatore accede a un’attività di Personalizzazione automatizzata e Targeting automatico, viene trasmessa un’istantanea di informazioni a un set di “record di apprendimento” (i dati del visitatore su cui si baseranno gli algoritmi di personalizzazione).
seo-title: Raccolta di dati per gli algoritmi di personalizzazione di Target
solution: Target
title: Raccolta di dati per gli algoritmi di personalizzazione di Target
title-outputclass: premium
topic: Premium
uuid: f5ca2d84-0016-4af5-a139-bca567a3d0e8
badge: premium
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# ![PREMIUM](/help/assets/premium.png) Raccolta di dati per gli algoritmi di personalizzazione Target{#data-collection-for-the-target-personalization-algorithms}

Target raccoglie e utilizza automaticamente una varietà di dati per creare gli algoritmi di personalizzazione nelle attività di Personalizzazione automatizzata (AP) e Targeting automatico (AT). Quando un visitatore accede a un’attività di Personalizzazione automatizzata e Targeting automatico, viene trasmessa un’istantanea di informazioni a un set di “record di apprendimento” (i dati del visitatore su cui si baseranno gli algoritmi di personalizzazione).

Per scoprire di più sugli algoritmi di personalizzazione di Target, consulta  [Algoritmo Foresta casuale](../../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA).

La tabella seguente mostra i dati raccolti da Personalizzazione automatica per impostazione predefinita, senza la necessità di eseguire alcuna operazione, nonché la convenzione di denominazione utilizzata per indicare questi attributi nei [rapporto Approfondimenti personalizzazione](../../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767). Puoi aumentare il set di dati di input in qualsiasi momento. Per ulteriori informazioni su come caricare dati aggiuntivi, consulta  [Caricamento dei dati per gli algoritmi di personalizzazione Target](../../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6).

| Tipo di dati | Descrizione | Convenzione sulla denominazione del tipo di dati | Attributi di esempio |
|--- |--- |--- |--- |
| Parametri URL | Target esamina l’URL per estrarre i parametri URL. | `Custom - URL Parameter - [URL Parameter]` | Dati personalizzati |
| Parametri URL di provenienza | In generale, l’URL di provenienza è quello contenente il riferimento a una pagina particolare che ha avviato la chiamata mbox.<br>Questa variabile può essere influenzata dall’attività degli utenti sul sito e dall’implementazione tecnica del sito. | `Custom - [Referring URL Parameter] - [Parameter value]` | Dati personalizzati |
| Dati ambientali e di sessione | Informazioni su come e quando l’utente accede all’attività. | `Visitor Profile - [attribute name]`<br>`Browser - [browser attribute]`<br>`Operating System - [OS attribute]` | Profilo del visitatore - Inizio visita più recente<br>Profilo del visitatore - Totale visite<br>Profilo del visitatore - Durata media per visita<br>Browser - Fuso orario<br>Browser - Giorno della settimana<br>Browser - Impostazioni della lingua<br>Browser - Tipo<br>Sistema operativo - Versione |
| Informazioni geografiche | Informazioni su dove si trova il visitatore. | `Geo - [geo attribute]` | Città<br>Paese<br>Regione/Stato<br>Codice postale<br>Latitudine<br>Longitudine<br>ISP o gestore di telefonia mobile |
| Dati mobili e sul dispositivo | Informazioni sul dispositivo e specifiche per dispositivi mobili. | `Device - [device attribute]`<br>`Mobile - [mobile attribute]` | Sistema operativo del dispositivo mobile<br>Dimensioni dello schermo del dispositivo mobile |

