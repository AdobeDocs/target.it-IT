---
keywords: faq;domande frequenti;analytics for target;a4t;provisioning;adobe experience cloud
description: Trova le risposte alle domande più frequenti sul provisioning di Analytics per [!DNL Target] (A4T), che consente di utilizzare i rapporti di Analytics per [!DNL Target] attività.
title: Dove posso trovare informazioni sul provisioning iniziale di A4T?
feature: Analytics for Target (A4T)
exl-id: 4b098444-3e5b-45e3-b635-1857c2c8d183
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 61%

---

# Provisioning iniziale - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande più frequenti sul provisioning [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Adobe Target] (A4T).

## Come posso impostare un’attività A4T con più pagine?

Per implementare un caso di utilizzo A4T di base con più pagine:

* Implementa le librerie JavaScript sia per Target che per Analytics sull’URL/pagina di destinazione dell’attività. L’implementazione di entrambe le soluzioni unisce i dati di Target con quelli di Analytics per ogni visitatore. Questi dati rimangono in Analytics finché non raggiungeranno la scadenza predefinita impostata su 90 giorni.

* Sulle pagine rimanenti del sito, dove saranno tracciate solo le metriche Analytics, implementa Analytics. Non è necessario implementare Target sulle pagine in questione. Le metriche Analytics acquisite in queste pagine vengono automaticamente legate all’attività Target per la quale l’utente si è inizialmente qualificato, in base alle informazioni di Target collegate al visitatore del passaggio precedente.

## Come posso sapere se A4T è abilitato sul mio [!DNL Target] account? {#section_4437D284448F4313BF953D4B6EDBACA6}

Prima di poter selezionare una suite di rapporti durante la definizione di un’attività di analisi, è necessario disporre sia di un account utente Analytics che di un account utente Target. Gli account utente devono essere configurati come descritto nella documentazione. Consulta [Requisiti delle autorizzazioni utente](/help/main/c-integrating-target-with-mac/a4t/account-reqs.md#concept_4BC06CAB00BF46FF9362AFE98656B083).

Se sei membro di uno o più gruppi di Experienci Cloud con accesso ad Analytics e Target e a tutte le suite di rapporti, dovresti vedere l’opzione per creare un test A/B con Analytics in **[!UICONTROL Crea attività]**.

Se si verificano problemi di provisioning, verifica se il provisioning di A4T è stato eseguito correttamente.

## Perché le suite di rapporti non vengono caricate? {#section_6CC8B2B3568A46C499895EB9811FDC2E}

Controlla quanto segue se si verifica uno di questi problemi:

* Assicurati che i tuoi account Analytics e Target siano collegati nell&#39;Experience Cloud.
* Alcuni clienti utilizzano più accessi aziendali di Analytics nella stessa società di Experienci Cloud. Se utilizzi più accessi, assicurati che l’ultima società Analytics a cui hai effettuato l’accesso sia quella collegata all’account Target per l’integrazione.
* Se sei stato connesso a Experience Cloud per diverse ore, la sessione di Analytics potrebbe essere scaduta. Disconnettiti, accedi di nuovo e riprova.

## Perché non vedo le opzioni di Analytics in Target? {#section_EDD996AFB08B4DB196DD934BE55BF48D}

Consulta “Perché le suite di rapporti non vengono caricate?” Sopra. La causa principale di questo problema è la stessa.

## Perché non vedo i rapporti A4T in Analytics? {#section_FEB41E7B7E4F4F78897E4D9F021DEA59}

Consulta “Perché le suite di rapporti non vengono caricate?” qui sopra. La causa principale di questo problema è la stessa.

## Perché i miei report in [!DNL Target] vuoto? {#section_3837104757464CB488C5A83014A669A1}

Consulta “Perché le suite di rapporti non vengono caricate?” qui sopra. La causa principale di questo problema è la stessa.