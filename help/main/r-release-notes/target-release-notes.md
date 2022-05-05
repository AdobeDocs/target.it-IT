---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali sono le nuove funzioni e i miglioramenti inclusi nella prossima versione?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 83a7fb03dcf334cb82eb507d2803e955a655b40a
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 23%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 5 maggio 2022**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 22.5.1 (rilascio scaglionato; (10-12 maggio 2022)

Questa versione sarà disponibile secondo la seguente pianificazione scaglionata:

* **10 maggio**: Area Europa, Medio Oriente e Africa (EMEA)
* **11 maggio**: regione Asia-Pacifico (APAC)
* **12 maggio**: Regione Nord America (NA)

Questa versione contiene i miglioramenti e le correzioni seguenti:

* È stato risolto un problema che causava un errore JavaScript e impediva ad alcuni clienti di accedere ai dettagli dell’attività per alcuni [!UICONTROL Automated Personalization] (AP) attività. (TGT-43526)
* È stato risolto un problema che impediva ad alcuni clienti di aggiungere (o modificare) un&#39;offerta specifica a un&#39;attività di Personalizzazione automatizzata. (TGT-43503)
* È stato risolto un problema in [!DNL Target] Interfaccia utente che ha visualizzato il seguente messaggio di errore: &quot;La mbox globale potrebbe non essere sincronizzata. Prova a salvarla di nuovo.” Questo problema era relativo a un’interfaccia utente e non aveva alcun impatto sulle implementazioni dei clienti. (TGT-43475)
* È stato risolto un problema che impediva a un cliente di modificare i perfezionamenti e i tipi di pubblico a livello di esperienza per un’attività se i perfezionamenti e i tipi di pubblico venivano creati prima del nuovo [!UICONTROL Tipi di pubblico] Interfaccia utente distribuita. (TGT-43433)
* È stato risolto un problema che consentiva ai clienti di selezionare un duplicato [!DNL Adobe Audience Manager] (AAM) tipi di pubblico durante la modifica dei tipi di pubblico di reporting per un’attività. (TGT-43430)
* È stato risolto un problema che impediva ai clienti di creare tipi di pubblico duplicati, ma in aree di lavoro diverse. (TGT-43423)
* È stato risolto un problema che impediva ai clienti di eliminare le posizioni con offerte ad hoc nelle attività create in [!UICONTROL Compositore esperienza basato su moduli]. (TGT-43315)
* È stato risolto un problema che impediva ai clienti di accedere alle offerte di codice dopo aver fatto clic su offerte di immagini e aver quindi aggiornato l’interfaccia utente. (TGT-43566)
* Assicurati che l’elenco delle metriche disponibili nel [!DNL Target] Interfaccia utente per la creazione di attività che utilizzano [!DNL Analytics for Target] (A4T) visualizza solo le metriche raccolte da [!DNL Adobe Analytics]. (TGT-43294)
* È stato risolto un problema che a volte causava [!UICONTROL Configurazione] richieste di pagina non riuscite. Ad esempio, se si modifica il valore &quot;[!UICONTROL Soluzione Experience Cloud di reporting]&quot; opzione da &quot;[!UICONTROL Analytics]&quot; a &quot;[!UICONTROL Target]&quot; o &quot;[!UICONTROL Seleziona per attività]&quot;. (TGT-43272)
* È stato risolto un problema che talvolta impediva l’aggiornamento corretto delle modifiche negli script di profilo. (TGT-43249)
* È stato risolto un problema che causava il seguente errore durante il tentativo di spostare un pubblico in un&#39;altra area di lavoro: &quot;Non possiamo completare la tua richiesta. Contatta l’Assistenza clienti Adobe se il problema persiste&quot;. (TGT-43212)
* È stato corretto un errore che causava un errore durante la clonazione di modifiche al codice personalizzato per le pagine app a pagina singola (SPA). (TGT-43137)
* È stato modificato il modo in cui la metrica &quot;visualizzazioni di pagina&quot; viene gestita in SPA. Invece dell’URL della pagina che viene visualizzato nel [!DNL Target] Interfaccia utente, l’interfaccia utente visualizza ora la &quot;vista&quot;. (TGT-41200)
* È stato risolto un problema che causava la modifica della promozione originale dopo la duplicazione di un’esperienza e la successiva modifica della promozione. (TGT-41775)

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche anticipate sui miglioramenti dei prodotti in arrivo a [!DNL Target] e altri [!DNL Adobe Experience Cloud] soluzioni, iscriviti al [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
