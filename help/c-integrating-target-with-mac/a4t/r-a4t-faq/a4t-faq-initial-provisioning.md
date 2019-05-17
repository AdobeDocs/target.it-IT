---
description: Questo argomento contiene le risposte alle domande più frequenti sull’utilizzo di Analytics come origine per la generazione di rapporti per Target (A4T).
keywords: faq;domande frequenti;analytics for target;a4t;provisioning;adobe experience cloud
seo-description: Questo argomento contiene le risposte alle domande più frequenti sull’utilizzo di Analytics come origine per la generazione di rapporti per Target (A4T).
seo-title: Provisioning iniziale - Domande frequenti su A4T
solution: Target
title: Provisioning iniziale - Domande frequenti su A4T
topic: Standard
uuid: cc80f879-ad2a-46d6-adc2-df616e8ab0b5
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Provisioning iniziale - Domande frequenti su A4T{#initial-provisioning-a-t-faq}

Questo argomento contiene le risposte alle domande più frequenti sull’utilizzo di Analytics come origine per la generazione di rapporti per Target (A4T).

## Come posso impostare un&#39;attività A 4 T con più pagine?

Per implementare un esempio di utilizzo A 4 T di base:

* Implementare le librerie javascript per Target (at. js o mbox. js) e Analytics sull&#39;URL/pagina di destinazione dell&#39;attività. L&#39;implementazione di entrambe le soluzioni unisce i dati di Target ai dati di Analytics per ogni visitatore. Questi dati rimangono in Analytics fino alla scadenza con la scadenza predefinita impostata su 90 giorni.

* Per le pagine rimanenti sul sito, dove sono state tracciate solo le metriche di Analytics, implementa Analytics su tali pagine. Non è necessario implementare Target su queste pagine. Le metriche di Analytics acquisite da queste pagine vengono automaticamente legate all&#39;attività di Target per cui l&#39;utente è inizialmente qualificato, in base alle informazioni di Target collegate al visitatore dal punto di vista precedente.

## Come posso sapere se A4T è abilitato sul mio account Target? {#section_4437D284448F4313BF953D4B6EDBACA6}

Prima di poter selezionare una suite di rapporti durante la definizione di un’attività di analisi, è necessario disporre sia di un account utente Analytics che di un account utente Target. Gli account utente devono essere configurati come descritto nella documentazione. Consulta [Requisiti delle autorizzazioni utente](../../../c-integrating-target-with-mac/a4t/account-reqs.md#concept_4BC06CAB00BF46FF9362AFE98656B083).

Se sei membro di uno o più gruppi Experience Cloud con accesso ad Analytics e Target e a tutte le suite di rapporti, dovresti vedere l’opzione per creare un test A/B con Analytics in **[!UICONTROL Crea attività]**.

Se si verificano problemi di provisioning, verifica se il provisioning di A4T è stato eseguito correttamente.

## Perché le suite di rapporti non vengono caricate?  {#section_6CC8B2B3568A46C499895EB9811FDC2E}

Controlla quanto segue se si verifica uno di questi problemi:

* Assicurati che i tuoi account Analytics e Target siano collegati in Experience Cloud.
* Se utilizzi account di accesso in Analytics per diverse società all’interno della stessa società Experience Cloud, assicurati che l’ultima società Analytics a cui ti sei connesso corrisponda a quella collegata all’account Target per l’integrazione.
* Se sei stato connesso a Experience Cloud per diverse ore, la sessione di Analytics potrebbe essere scaduta. Disconnettiti, accedi di nuovo e riprova.

## Perché non vedo le opzioni di Analytics in Target?  {#section_EDD996AFB08B4DB196DD934BE55BF48D}

Consulta “Perché le suite di rapporti non vengono caricate?” qui sopra. La causa principale di questo problema è la stessa.

## Perché non vedo i rapporti A4T in Analytics?  {#section_FEB41E7B7E4F4F78897E4D9F021DEA59}

Consulta “Perché le suite di rapporti non vengono caricate?” qui sopra. La causa principale di questo problema è la stessa.

## Perché i rapporti in Target sono vuoti?  {#section_3837104757464CB488C5A83014A669A1}

Consulta “Perché le suite di rapporti non vengono caricate?” qui sopra. La causa principale di questo problema è la stessa.
