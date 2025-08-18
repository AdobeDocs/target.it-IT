---
keywords: faq;domande frequenti;analytics for target;a4T;reindirizzamento;offerte di reindirizzamento;adobe-mc-sdid;adobe_mc_ref
description: Risposte alle domande sull'utilizzo delle offerte di reindirizzamento durante l'utilizzo di Analytics for [!DNL Target] (A4T). A4T consente di utilizzare la funzione di reporting di Analytics per  [!DNL Target]  attività.
title: Dove posso trovare domande frequenti sulle offerte di reindirizzamento con A4T?
feature: Analytics for Target (A4T)
exl-id: 4706057f-bd8b-4562-94e0-be22b2e19297
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '1430'
ht-degree: 50%

---

# Offerte di reindirizzamento - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande che vengono spesso poste in merito alle offerte di reindirizzamento quando si utilizza [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Adobe Target] (A4T).

## Analytics for Adobe Target (A4T) supporta le offerte di reindirizzamento? {#section_46B8B03ED4D542C6AD875F5F61176298}

+++Risposta
Sì, se l&#39;implementazione utilizza [!DNL at.js]. Tuttavia, l’implementazione deve soddisfare i requisiti minimi elencati di seguito per utilizzare le [offerte di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md#task_33C80CD722564303B687948261484F94) nelle attività che utilizzano Analytics come origine per la generazione di rapporti.

+++

## Quali sono i requisiti minimi per utilizzare le offerte di reindirizzamento con A4T? {#section_FA9384C2AA9D41EDBCE263FFFD1D9B58}

+++Risposta
L’implementazione deve soddisfare i seguenti requisiti minimi:

* Servizio ID visitatore di Experience Cloud: [!DNL visitorAPI.js] versione 2.3.0 o successiva.
* Adobe Analytics: [!DNL appMeasurement.js] versione 2.1.
* Adobe Target: [!DNL at.js] versione 1.6.2 o successiva.

Le tre librerie devono essere incluse sia nella pagina con l’offerta di reindirizzamento sia nella pagina a cui il visitatore viene reindirizzato.

+++

## Perché a volte sono presenti discrepanze di dati tra A4T e Analytics?

+++Risposta
È possibile riscontrare alcune discrepanze di dati. Per ulteriori informazioni, consulta [Varianze di dati previste tra Target e Analytics durante l’utilizzo con e senza A4T](/help/main/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md).

+++

## Come ridurre al minimo le discrepanze nella distribuzione del traffico quando si utilizzano offerte di reindirizzamento nelle attività A4T? {#discrepancies}

+++Risposta
Un numero limitato di clienti ha segnalato maggiore varianza nella distribuzione del traffico quando si utilizzano offerte di reindirizzamento in attività configurate con [!UICONTROL Analytics for Target] (A4T).

Considera i seguenti aspetti:

* L&#39;ordine errato di [!DNL Target] e [!DNL Analytics] chiamate potrebbe essere responsabile di gradi più elevati di varianza.

  La chiamata [!DNL Target] deve precedere la chiamata [!DNL Analytics] sulla pagina di origine (dove si verifica il reindirizzamento) e sulla pagina di destinazione (dove termina il reindirizzamento).

* Assicurati di utilizzare le offerte di reindirizzamento nelle attività di reindirizzamento A4T.
* Se nella pagina di origine (dove si verifica il reindirizzamento) sono presenti più richieste di posizione [!DNL Target], [!DNL Adobe] consiglia di eseguire l&#39;attività di reindirizzamento sulla prima richiesta di posizione [!DNL Target].

  L&#39;esecuzione dell&#39;attività di reindirizzamento sulla prima richiesta di posizione [!DNL Target] riduce le possibilità che qualifiche di attività si verifichino su altre richieste di posizione [!DNL Target] e vengano conteggiate nel rapporto. I visitatori che vengono reindirizzati non devono essere conteggiati nei rapporti di altre attività in quanto non vedranno le esperienze.

+++

## Perché a volte vengono conteggiate le visualizzazioni di pagina nella pagina originale e nella pagina di reindirizzamento? {#section_B8F6CC2190B84CF08D945E797C5AF07B}

+++Risposta
Quando si utilizza at.js versione 1.6.3 o successiva, il conteggio delle visualizzazioni di pagina su entrambe le pagine non costituisce un problema. Questa situazione di tipo “race condition” interessa solo i clienti che utilizzano versioni precedenti. Il team di Target gestisce solo due versioni di at.js: la versione corrente e quella immediatamente precedente. Aggiorna at.js per assicurarti di eseguire sempre una [versione supportata](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank}.

Se utilizzi una versione precedente e non supportata di at.js, si potrebbe verificare una situazione di tipo “race condition” a causa della quale potrebbe essere attivata una chiamata Analytics prima che sulla prima pagina sia stato eseguito il reindirizzamento. Questa situazione può causare il conteggio di tutte le visualizzazioni di pagina sulla pagina originale e sulla pagina di reindirizzamento. Questa situazione si traduce in una visualizzazione di pagina in più sulla prima pagina, anche se il visitatore non ha mai effettivamente “visualizzato” questa prima pagina.

Si consiglia di utilizzare il compositore basato su moduli per creare un’attività di reindirizzamento per aumentare la velocità del reindirizzamento della pagina a causa della posizione in cui il codice viene eseguito sulla pagina. Inoltre, è consigliato creare un’offerta di reindirizzamento per ogni esperienza, anche per quella predefinita, dove il reindirizzamento riporta alla pagina originale. La creazione di un’offerta di reindirizzamento per ogni esperienza assicura che il conteggio errato si verifichi in tutte le esperienze. I rapporti e l’analisi sono ancora validi per il test.

Potrebbe essere utile usare offerte di reindirizzamento per tutte le esperienze dell’attività, inclusa quella predefinita (esperienza di controllo), ad esempio, per inserire le stesse condizioni in tutte le esperienze. Supponiamo che sia stata impostata un’offerta di reindirizzamento per tutte le esperienze eccetto quella predefinita: la velocità dell’esperienza priva di offerta di reindirizzamento sarà avvantaggiata. Le offerte di reindirizzamento sono consigliate solo per scenari temporanei, ad esempio a scopo di test. Le offerte di reindirizzamento non sono consigliate per scenari permanenti, ad esempio a scopo di personalizzazione. Dopo aver determinato l’esperienza &quot;vincitrice&quot;, rimuovi il reindirizzamento per migliorare le prestazioni di caricamento della pagina.

+++

## Il Compositore esperienza visivo e il Compositore esperienza basato su moduli sono entrambi supportati? {#section_FDA26FE7909B48539DA770559E687677}

+++Risposta
Sì, entrambi i compositori sono supportati purché si utilizzino le offerte di reindirizzamento incorporate.

Se utilizzi un codice personalizzato per il reindirizzamento, assicurati di compilare i due nuovi parametri associati agli URL di reindirizzamento (`adobe_mc_sdid` e `adobe_mc_ref`, descritti di seguito).

+++

## Quali sono i nuovi parametri della stringa di query aggiunti agli URL di reindirizzamento? {#section_BA73E8B3CFCC4CBEB5BE3F76B2BC8682}

+++Risposta
I seguenti parametri di stringa di richiesta sono associati alle offerte di reindirizzamento:

| Parametro | Descrizione |
|--- |--- |
| `adobe_mc_sdid` | Il parametro `adobe_mc_sdid` passa l&#39;ID di dati supplementari (SDID) e l&#39;ID dell&#39;organizzazione di Experience Cloud dalla pagina predefinita alla nuova pagina. Questi ID consentono a A4T di &quot;unire&quot; la richiesta Target nella pagina predefinita con la richiesta Analytics nella nuova pagina.<br>Il formato previsto per il passaggio di sdid nell&#39;URL (per le app ibride o da un&#39;app al sito Web o da un sito Web a un altro) è `ex. adobe_mc_sdid=SDID=123|MCORGID=123456789@AdobeOrg|TS=1498569322` |
| `adobe_mc_ref` | Il parametro `adobe_mc_ref` passa l’URL di riferimento della pagina predefinita alla nuova pagina. Se utilizzato con AppMeasurement.js versione 2.1 (o successiva), Analytics utilizza questo valore di parametro come URL di riferimento nella nuova pagina. |

Questi parametri vengono aggiunti automaticamente agli URL di reindirizzamento quando si utilizzano le offerte di reindirizzamento incorporate nel Compositore esperienza visivo e nel Compositore esperienza basato su modulo quando il servizio ID visitatore viene implementato nella pagina. Se utilizzi un codice di reindirizzamento personalizzato nel Compositore esperienza visivo o nel Compositore basato su moduli, assicurati di passare questi parametri con il codice personalizzato.

+++

## I miei server web rimuovono questi parametri dai miei URL, cosa devo fare? {#section_0C2DDB72939F4875B6D0428B8DCB38E5}

+++Risposta
Rivolgiti al tuo team IT per inserire nell&#39;elenco Consentiti questi parametri ( `adobe_mc_sdid` e `adobe_mc_ref`).

+++

## Cosa succede se non uso A4T con la mia attività di reindirizzamento e non voglio che questi parametri vengano aggiunti ai miei URL? {#section_9E608D75FF9349FE96C65FEDD7539F45}

+++Risposta
Utilizza un reindirizzamento con codice personalizzato se:

* Non utilizzi A4T con l’attività di reindirizzamento
* Hai implementato il servizio ID visitatore
* Non desideri che questi parametri vengano aggiunti automaticamente agli URL

Tuttavia, come best practice, è possibile mantenere il parametro `adobe_mc_ref` nell’URL per segnalare correttamente le informazioni di riferimento a [!DNL Analytics].

+++

## Perché i parametri adobe_mc_ref e adobe_mc_sdid sono codificati con doppio URL nella mia implementazione? {#section_5EFE5F012B944C40865731EA18E7E79E}

+++Risposta
Se utilizzi A4T e le offerte di reindirizzamento, Target aggiunge i parametri `adobe_mc_ref` e `adobe_mc_sdid` all’URL. Questi valori sono già codificati nell’URL. Nella maggior parte dei casi tutto funziona come previsto, tuttavia alcuni clienti potrebbero usare bilanciatori di carico o server web che tentano di codificare nuovamente i parametri della stringa di query.

A causa di questa doppia codifica quando l’API dei visitatori tenta di decodificare il valore `adobe_mc_sdid`, non può estrarre il valore SDID e genera un nuovo SDID. Questo processo porta all’invio di valori SDID errati a Target e Analytics, e nei rapporti di Analytics viene visualizzata una suddivisione irregolare per i reindirizzamenti.

Adobe consiglia di parlare con il team IT per assicurarsi che `adobe_mc_ref` e `adobe_mc_sdid` siano inseriti nell&#39;elenco Consentiti in modo che questi valori non vengano trasformati in alcun modo.

+++

## Perché l’URL di riferimento deve essere passato alla nuova pagina? {#section_91AB8B0891F6416CBF7E973DCAF54EB5}

+++Risposta
Supponiamo che un visitatore faccia clic su un collegamento in [!DNL `www.google.com`] alla tua pagina principale (`www.mysite.com/index.html`) sulla quale è stata pubblicata un&#39;attività di reindirizzamento, e che venga quindi reindirizzato a una nuova pagina (`www.mysite.com/index2.html`).

In precedenza, la richiesta [!DNL Analytics] nella nuova pagina avrebbe segnalato un URL di riferimento di [!DNL `www.mysite.com/index.html`] invece di [!DNL `www.google.com`]. Questo causava una segnalazione inesatta in [!DNL Analytics] associata agli URL di riferimento (ad esempio nei rapporti Canale marketing,). Nei rapporti andava perso il fatto che l&#39;utente era giunto al sito da [!DNL `www.google.com`].

Con [!DNL at.js] versione 0.9.6 (o successiva) e [!DNL AppMeasurement.js] 2.1 (o successiva), la richiesta [!DNL Analytics] nella nuova pagina riporta un URL di riferimento di [!DNL `www.google.com`].

+++

## Posso usare le offerte di reindirizzamento personalizzate/HTML? {#section_E49F9A83A286488C8F1098A040203D7E}

+++Risposta
No, è necessario utilizzare un’offerta di reindirizzamento incorporata per attività che utilizzano [!DNL Analytics] come origine per la generazione di rapporti (A4T). Dal punto di vista di [!DNL Target], le offerte HTML sono opache: [!DNL Target] non può sapere che un particolare pezzo di HTML contiene JavaScript che crea un’istanza di un reindirizzamento.

+++

## ![Badge Adobe Experience Platform Web SDK](/help/main/assets/platform.png) [!DNL Adobe Experience Platform Web SDK] supporta le offerte di reindirizzamento per A4T? {#platform}

Le seguenti domande frequenti forniscono ulteriori informazioni sull&#39;utilizzo di A4T e sulle offerte di reindirizzamento con [!DNL Platform Web SDK].

### Analytics for Target (A4T) supporta le offerte di reindirizzamento?

+++Risposta
Sì, A4T tramite Platform Web SDK supporta [offerte di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md).

+++

### [!UICONTROL Visual Experience Composer] (VEC) e [!UICONTROL Form-Based Experience Composer] sono supportati?

+++Risposta
Sì, [[!UICONTROL Visual Experience Composer]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) e [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md) sono supportati se si utilizzano offerte di reindirizzamento integrate.

+++

### Posso usare le offerte di reindirizzamento personalizzate/HTML con [!DNL Platform Web SDK]?

+++Risposta
No, devi utilizzare un’offerta di reindirizzamento integrata per attività che utilizzano A4T. Dal punto di vista di [!DNL Target], le offerte HTML sono opache. [!DNL Target] non può sapere che un particolare pezzo di HTML contiene JavaScript che crea un&#39;istanza di un reindirizzamento.

+++
