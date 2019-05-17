---
description: Questo argomento contiene le risposte alle domande che vengono spesso poste in merito alle offerte di reindirizzamento durante l’utilizzo di Analytics come origine per la creazione di rapporti per Target (A4T).
keywords: faq;domande frequenti;analytics for target;a4T;reindirizzamento;offerte di reindirizzamento;adobe-mc-sdid;adobe_mc_ref
seo-description: Questo argomento contiene le risposte alle domande che vengono spesso poste in merito alle offerte di reindirizzamento durante l’utilizzo di Analytics come origine per la creazione di rapporti per Target (A4T).
seo-title: Offerte di reindirizzamento - Domande frequenti su A4T
solution: Target
title: Offerte di reindirizzamento - Domande frequenti su A4T
topic: Standard
uuid: a45cef89-3003-4177-bf84-3d5a486b950d
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Offerte di reindirizzamento - Domande frequenti su A4T{#redirect-offers-a-t-faq}

Questo argomento contiene le risposte alle domande che vengono spesso poste in merito alle offerte di reindirizzamento durante l’utilizzo di Analytics come origine per la creazione di rapporti per Target (A4T).

## Analytics for Target (A4T) supporta le offerte di reindirizzamento? {#section_46B8B03ED4D542C6AD875F5F61176298}

Sì, purché l’implementazione utilizzi [!DNL at.js]. Tuttavia, l’implementazione deve soddisfare i requisiti minimi elencati di seguito per utilizzare le [offerte di reindirizzamento](../../../c-experiences/c-manage-content/offer-redirect.md#task_33C80CD722564303B687948261484F94) nelle attività che utilizzano Analytics come origine per la generazione di rapporti.

## Quali sono i requisiti minimi necessari per utilizzare le offerte di reindirizzamento con A4T? {#section_FA9384C2AA9D41EDBCE263FFFD1D9B58}

L’implementazione deve soddisfare i seguenti requisiti minimi:

* Servizio ID visitatore di Experience Cloud: [!DNL visitorAPI.js] versione 2.3.0 o successiva.
* Adobe Analytics: [!DNL appMeasurement.js] versione 2.1.
* Adobe Target: [!DNL at.js] versione 1.6.2 o successiva.

   La libreria [!DNL mbox.js] non supporta le offerte di reindirizzamento con A4T. L’implementazione deve utilizzare [!DNL at.js].

Le tre librerie devono essere incluse sia nella pagina con l’offerta di reindirizzamento sia nella pagina a cui il visitatore viene reindirizzato.

## Perché a volte sono presenti discrepanze di dati tra A 4 T e Analytics?

Sono previste alcune discrepanze di dati. Per ulteriori informazioni, consultate [Varianza di dati prevista tra Target e Analytics quando utilizzate e non utilizzate A 4 T](/help/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md).

## Perché a volte vengono conteggiate le visualizzazioni di pagina nella pagina originale e nella pagina di reindirizzamento?  {#section_B8F6CC2190B84CF08D945E797C5AF07B}

È possibile che si verifichi una condizione particolare che potrebbe causare l’attivazione della chiamata di Analytics prima che il reindirizzamento venga eseguito nella prima pagina. Questo può determinare un conteggio delle visualizzazioni di pagina sia nella pagina originale sia in quella di reindirizzamento. Questa situazione si traduce in una visualizzazione di pagina in più sulla prima pagina, anche se il visitatore non ha mai effettivamente “visualizzato” questa prima pagina.

Per aumentare la velocità del reindirizzamento della pagina, è consigliabile creare un’attività di reindirizzamento con il compositore basato su moduli. Questo è dovuto al punto in cui viene eseguito il codice nella pagina. Inoltre, è consigliato creare un’offerta di reindirizzamento per ogni esperienza, anche per quella predefinita, dove il reindirizzamento riporta alla pagina originale. Ciò assicura che, se si verifica un conteggio errato, questo si verifica in tutte le esperienze, in modo che il rapporto e l’analisi siano comunque validi per il test.

>[!NOTE]
>
>Questa corsa critica interessa solo i clienti che utilizzano at.js versione 1.6.3 o precedenti. Attenzione: il team di Target gestisce solo due versioni di at.js, ovvero la versione corrente e quella immediatamente precedente. Aggiorna at.js per assicurarti di eseguire una [versione supportata](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

Per ulteriori informazioni su questo problema, consulta la colonna “Offerte di reindirizzamento” nella tabella [Problemi noti](../../../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541).

## Posso usare le offerte di reindirizzamento con A4T se utilizzo la libreria JavaScript mbox.js? {#section_D2A8B182B7254D61A8BB2BCBA0C0F64A}

La libreria [!DNL mbox.js] non supporta le offerte di reindirizzamento con A4T. L’implementazione deve utilizzare [!DNL at.js].

## Il Compositore esperienza visivo e il Compositore esperienza basato su moduli sono entrambi supportati? {#section_FDA26FE7909B48539DA770559E687677}

Sì, entrambi i compositori sono supportati purché si utilizzano le offerte di reindirizzamento integrate.

Se utilizzi un codice personalizzato per il reindirizzamento, assicurati di compilare i due nuovi parametri associati agli URL di reindirizzamento (`adobe_mc_sdid` e `adobe_mc_ref`, descritti di seguito).

## Quali sono i nuovi parametri della stringa di query aggiunti agli URL di reindirizzamento? {#section_BA73E8B3CFCC4CBEB5BE3F76B2BC8682}

I seguenti parametri di stringa di richiesta sono associati alle offerte di reindirizzamento:

| Parametro | Descrizione |
|--- |--- |
| `adobe_mc_sdid` | Il parametro `adobe_mc_sdid` passa l’ID di dati supplementari (SDID) e l’ID dell’organizzazione di Experience Cloud dalla pagina predefinita alla nuova pagina affinché A4T “unisca” la richiesta di Target nella pagina predefinita con la richiesta di Analytics nella nuova pagina. |
| `adobe_mc_ref` | Il parametro `adobe_mc_ref` passa l’URL di riferimento della pagina predefinita alla nuova pagina. Se utilizzato con AppMeasurement.js versione 2.1 (o successiva), Analytics utilizzerà questo valore di parametro come URL di riferimento nella nuova pagina. |

Questi parametri vengono aggiunti automaticamente agli URL di reindirizzamento quando si utilizzano le offerte di reindirizzamento integrate nel Compositore esperienza visivo e nel Compositore esperienza basato su modulo quando il servizio ID visitatore viene implementato nella pagina. Se utilizzi un codice di reindirizzamento personalizzato nel Compositore esperienza visivo o nel Compositore basato su moduli, assicurati di passare questi parametri con il codice personalizzato.

## I miei server web rimuovono questi parametri dai miei URL, cosa devo fare?  {#section_0C2DDB72939F4875B6D0428B8DCB38E5}

Sarà necessario lavorare con il team IT per spostare questi parametri (`adobe_mc_sdid` e `adobe_mc_ref`) nella whitelist di parametri affidabili.

## Cosa succede se non uso A4T con la mia attività di reindirizzamento e non voglio che questi parametri vengano aggiunti ai miei URL? {#section_9E608D75FF9349FE96C65FEDD7539F45}

Se non utilizzi A4T con l’attività di reindirizzamento, disponi del servizio ID visitatore implementato e questi parametri non devono essere aggiunti automaticamente agli URL, utilizza un reindirizzamento con codice personalizzato.

Tuttavia, come best practice, è possibile mantenere il parametro `adobe_mc_ref` nell’URL per segnalare correttamente le informazioni di riferimento a [!DNL Analytics].

## Perché i parametri adobe_mc_ref e adobe_mc_sdid sono codificati con doppio URL nella mia implementazione? {#section_5EFE5F012B944C40865731EA18E7E79E}

Se utilizzi A4T e le offerte di reindirizzamento, Target aggiunge i parametri `adobe_mc_ref` e `adobe_mc_sdid` all’URL. Questi valori sono già codificati nell’URL. Nella maggior parte dei casi tutto funziona come previsto, tuttavia alcuni clienti potrebbero usare bilanciatori di carico o server web che tentano di codificare nuovamente i parametri della stringa di query.

A causa di questa doppia codifica quando l’API dei visitatori tenta di decodificare il valore `adobe_mc_sdid`, non può estrarre il valore SDID e genera un nuovo SDID. Questo porta all’invio di valori SDID errati a Target e Analytics, e vedrai una suddivisione irregolare dei reindirizzamenti nei rapporti di Analytics.

Si consiglia di parlare con il proprio team IT per assicurarsi che `adobe_mc_ref` e `adobe_mc_sdid` siano inseriti nelle whitelist in modo che tali valori non vengano trasformati in alcun modo.

## Perché l’URL di riferimento deve essere passato alla nuova pagina? {#section_91AB8B0891F6416CBF7E973DCAF54EB5}

Supponiamo che un visitatore faccia clic in [!DNL `www.google.com`] su un collegamento che porta alla tua pagina principale ( [!DNL `www.mysite.com/index.html]`) sulla quale è stata pubblicata un’attività di reindirizzamento, e viene quindi reindirizzato a una nuova pagina ( [!DNL `www.mysite.com/index2.html`]).

In precedenza, la richiesta di [!DNL Analytics] della nuova pagina avrebbe segnalato l’URL di riferimento [!DNL `www.mysite.com/index.html`] anziché [!DNL `www.google.com`]. Questo causava una segnalazione inesatta in [!DNL Analytics] associata agli URL di riferimento (ad esempio nei rapporti Canale marketing, ). Nei rapporti andava perso il fatto che il visitatore era giunto al sito da [!DNL `www.google.com`].

Con [!DNL at.js] versione 0.9.6 (o successiva) e [!DNL AppMeasurement.js] 2.1 (o versioni successive), la richiesta di [!DNL Analytics] sulla nuova pagina segnalerà [!DNL `www.google.com`] come URL di riferimento.

## Posso usare le offerte di reindirizzamento personalizzate/HTML? {#section_E49F9A83A286488C8F1098A040203D7E}

No, è necessario utilizzare un’offerta di reindirizzamento integrata per attività che utilizzano [!DNL Analytics] come origine per la generazione di rapporti (A4T). Dal punto di vista di [!DNL Target], le offerte HTML sono opache: [!DNL Target] non può sapere che un particolare pezzo di HTML contiene JavaScript che crea un’istanza di un reindirizzamento.
