---
keywords: analytics for target;a4t;analytics come origine per la generazione di rapporti;analytics
description: Scopri come utilizzare Analytics per [!DNL Target] (A4T). A4T consente di accedere ai rapporti di Analytics per [!DNL Target] attività che utilizzano metriche di Analytics e segmenti di pubblico.
title: Come si utilizza il reporting in A4T?
feature: Analytics for Target (A4T)
exl-id: cab5dc5f-166a-468e-8382-ae734684afdd
source-git-commit: 493ecd762b5228d33377ac8263b90a0f9c73127e
workflow-type: tm+mt
source-wordcount: '1300'
ht-degree: 47%

---

# Generazione di rapporti per A4T

Utilizzo [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Adobe Target] (A4T) consente di accedere a [!DNL Analytics] rapporti per [!DNL Target] attività.

Puoi visualizzare i rapporti per le attività in entrambi [!DNL Analytics] e [!DNL Target].

Per le best practice di reporting che utilizzano [!DNL Analytics] per [!DNL Target], [visita Adobe Spark Page](https://spark.adobe.com/page/Lo3Spm4oBOvwF/).

## Panoramica {#section_035A62D65608423285D8A5A54731E2C5}

Entrambi [!DNL Analytics] e [!DNL Target] i rapporti misurano i partecipanti (le persone incluse nei test), anziché i visitatori del sito.

Ogni volta che un visitatore visualizza il contenuto dell’attività sulla pagina, [!DNL Target] effettua una chiamata diretta da server a server a [!DNL Analytics], tra cui quale attività ed esperienza ha visto il visitatore. [!DNL Target] anche le chiamate [!DNL Analytics] ogni volta che viene effettuata la conversione. [!DNL Analytics] aggiunge la conversione come nuova specifica [!DNL Analytics] evento denominato &quot;Conversione attività&quot;, tracciato insieme ad altri dati raccolti da [!DNL Analytics].

Quando il [!UICONTROL Seleziona] viene utilizzata e viene eseguito l&#39;ordinamento *Partecipanti*, nei rapporti vengono quindi visualizzate solo le esperienze che hanno ricevuto partecipanti durante il periodo di tempo selezionato.

>[!NOTE]
>
>Rapporti forniti da [!DNL Target] hanno una latenza di quattro minuti. Per le attività basate su A4T, sia nella [!DNL Target] e [!DNL Analytics] nei rapporti, potrebbero essere necessarie fino a 24 ore dopo il salvataggio iniziale dell’attività prima che i dati del rapporto possano essere suddivisi per esperienze. I dati raccolti nelle prime 24 ore sono comunque precisi e vengono attribuiti all’esperienza corretta.

## Rapporti in Analytics {#analytics}

In [!DNL Analytics], dopo l’abilitazione dell’integrazione A4T sono disponibili diverse dimensioni e metriche.

### Dimensioni

* [!UICONTROL Analytics for Target] - L&#39;ID principale trasmesso tramite l&#39;integrazione. Il formato di questa dimensione è `Activity ID:Experience ID:3rd ID`. Le dimensioni seguenti sono classificazioni di questa dimensione.
* [!UICONTROL Attività di Target]
* [!UICONTROL Esperienze Target]
* [!UICONTROL Attività Target] > [!UICONTROL Esperienza]
* [!UICONTROL 3o ID] - può essere ignorato

### Metrics (Metriche)

* [!UICONTROL Impression attività] - Corrisponde al [!UICONTROL Partecipanti] nel [!DNL Target] rapporto.
* [!UICONTROL Conversioni attività] - Corrisponde al [!UICONTROL Conversioni personalizzate] nel [!DNL Target] rapporto.

In [!DNL Analysis Workspace], utilizza [!UICONTROL Analytics for Target] pannello per analizzare [!DNL Target] attività ed esperienze con incremento e affidabilità. Per ulteriori informazioni, consulta [Pannello Analytics for Target (A4T)](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=it) in *Guida agli strumenti di Analytics*.

>[!IMPORTANT]
>
>Se [!UICONTROL Attività di Target] in [!DNL Analytics] elenca &quot;non specificato&quot; invece di elencare le attività, è necessario un aggiornamento al tuo account predisposto. Contatta il servizio clienti per risolvere il problema.

Per informazioni ed esempi dettagliati, apri la [Analytics e Target: Best practice per l’analisi](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) esercitazione, fornita da Adobe Experience League.

## Rapporti in [!DNL Target] {#section_C0D1F17F88374B6690BF904D7B83B42E}

Quando [!DNL Analytics] viene utilizzato come origine per la generazione di rapporti, nei [!DNL Target] mostra i dati raccolti da [!DNL Analytics]. La relazione è in qualche modo diversa dalle altre [!DNL Target] rapporti:

* La [!UICONTROL Tipi di pubblico] mostra i tipi di pubblico disponibili per le [!DNL Analytics] suite di rapporti.
* La [!UICONTROL Metrica] elenco mostra ogni metrica disponibile attraverso [!DNL Analytics].

   Ogni metrica è disponibile, comprese quelle personalizzate o calcolate che sono integrate in [!DNL Analytics].

   Eventuali numeri che aumentano vengono visualizzati come positivi nel rapporto, anche quando un aumento è indesiderato. Ad esempio, anche se si desidera una percentuale di mancato recapito più bassa, la percentuale più elevata viene visualizzata come vincitore con l’incremento più alto. Considera queste metriche e ad altre simili, e se preferisci aumentare o diminuire i numeri, quando prendi decisioni in base ai rapporti.

Puoi applicare la metrica o il pubblico al rapporto in [!DNL Target] dopo l’avvio dell’attività, o anche dopo il completamento del test. Non devi sapere preventivamente con precisione che cosa vuoi misurare.

Fai clic per visualizzare il testo completo [!DNL Analytics] rapporti direttamente dalla pagina del rapporto di attività.

## Creazione di attività {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

Durante la creazione di attività, devi specificare un obiettivo per l’attività nella pagina [!UICONTROL Impostazioni]. Questo obiettivo diventa la metrica predefinita per il rapporto e viene sempre indicato come prima opzione nel selettore delle metriche. Non puoi selezionare i segmenti per il rapporto come faresti per una normale attività di Target. Un test con [!DNL Analytics] utilizza [!DNL Adobe Analytics] segmenti anziché [!DNL Target] pubblico.

## Esecuzione di calcoli offline per Analytics for Adobe Target (A4T) {#section_B34BD016C8274C97AC9564F426B9607E}

Puoi eseguire calcoli offline per A4T, ma è necessario un ulteriore passaggio di esportazione dei dati di [!DNL Analytics].

Per A4T utilizziamo un [Test t di Welch](https://en.wikipedia.org/wiki/Welch%27s_t-test)Calcolo di {target=_blank} per le variabili continue (anziché metriche binarie). In Analytics, un visitatore viene sempre tracciato e ogni azione intrapresa viene conteggiata. Pertanto, se il visitatore effettua più acquisti o visita una metrica di successo più volte, tali hit aggiuntivi vengono conteggiati. Questo rende la metrica una variabile continua. Per eseguire il calcolo della prova t del Welch, è necessaria la &quot;somma dei quadrati&quot; per calcolare la varianza, che viene utilizzata nel denominatore della statistica t. [Calcoli statistici nei test A/Bn](/help/main/c-reports/statistical-methodology/statistical-calculations.md) spiega i dettagli delle formule matematiche utilizzate. La somma dei quadrati può essere recuperata da [!DNL Analytics]. Per ottenere la somma dei quadrati è necessario eseguire un’esportazione a livello del visitatore per la metrica che desideri ottimizzare, per un periodo di tempo campione.

Ad esempio, se esegui l’ottimizzazione per le visualizzazioni di pagina per visitatore, esporta un campione del numero totale di visualizzazioni di pagina per visitatore per un intervallo di tempo specificato, forse per un paio di giorni (solo poche migliaia di punti di dati sono necessari). Dovresti poi quadrare ogni valore e sommare i totali (è importante eseguire le operazioni in questo ordine). Questo valore di “somma dei quadrati” viene quindi utilizzato nel Calcolatore di affidabilità completo. Per questi valori consulta la sezione “ricavi” del foglio di calcolo.

**Per eseguire la funzione di esportazione dei dati di [!DNL Analytics]:**

1. Accedi a [!DNL Adobe Analytics].
1. Fai clic su **[!UICONTROL Strumenti]** > **[!UICONTROL Data Warehouse]**.
1. Compila i campi nella scheda di **[!UICONTROL Richiesta Data Warehouse]**.

   Per ulteriori informazioni su ogni campo, consulta “Descrizioni di Data Warehouse” in [Data Warehouse](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse.html).

   | Campo | Istruzioni |
   |--- |--- |
   | Request Name (Nome richiesta) | Specifica un nome per la richiesta. |
   | Reporting Date (Data rapporto) | Specifica un periodo di tempo e una granularità.<br>Per la prima richiesta si consiglia di scegliere non più di un’ora o un giorno di dati.  L’elaborazione dei file di Data Warehouse richiede più tempo per periodo di tempo più lunghi, pertanto è sempre consigliabile richiedere prima dati per un periodo di tempo breve, per assicurarsi che il file restituisca il risultato atteso. Quindi, passa a Request Manager (Gestione richieste), duplica la richiesta e richiedi più dati la seconda volta. Inoltre, se si imposta la granularità su qualcosa di diverso da Nessuno, la dimensione del file aumenterà drasticamente.<br>![Data Warehouse](/help/main/c-reports/assets/datawarehouse.png) |
   | Available Segments (Segmenti disponibili) | Applica un segmento, se necessario. |
   | Breakdowns (Suddivisioni) | Seleziona le dimensioni desiderate: le dimensioni standard sono pronte all’uso, mentre quelle personalizzate includono eVar e prop. Si consiglia di utilizzare &quot;ID visitatore&quot; se sono necessarie informazioni a livello di ID visitatore, anziché &quot;ID visitatore Experience Cloud&quot;.<ul><li>ID visitatore è l’ID finale utilizzato da Analytics. Si tratterà di AID (se il cliente è un’azienda) o MID (se il cliente è nuovo o se ha cancellato i cookie da quando è stato avviato il servizio ID visitatore di MC).</li><li>L’ID visitatore di Experience Cloud sarà impostato solo per i clienti che sono nuovi o che hanno cancellato i cookie da quando è stato avviato il servizio ID visitatore di MC.</li></ul> |
   | Metrics (Metriche) | Seleziona la metrica desiderata. La metrica standard è OOTB, mentre quella personalizzata include eventi personalizzati. |
   | Report Preview (Anteprima rapporto) | Rivedi le impostazioni prima di pianificare il rapporto.<br>![Data Warehouse 2](/help/main/c-reports/assets/datawarehouse2.png) |
   | Schedule Delivery (Pianifica consegna) | Immetti l’indirizzo email a cui deve essere consegnato il file, assegna un nome al file, quindi seleziona [!UICONTROL Send Immediately] (Invia subito).<br>Nota: il file può essere consegnato via FTP da [!UICONTROL Opzioni di consegna avanzate]<br>![Pianifica consegna](/help/main/c-reports/assets/datawarehouse3.png). |

1. Fai clic su **[!UICONTROL Richiedi questo rapporto]**.

   La consegna dei file può richiedere fino a 72 ore, a seconda della quantità di dati richiesti. Puoi controllare l’avanzamento della richiesta in qualsiasi momento facendo clic su [!UICONTROL Tools] > [!UICONTROL Data Warehouse] > [!UICONTROL Request Manager] (Strumenti > Data Warehouse > Gestione richieste).

   Se desideri richiedere nuovamente i dati richiesti in passato, puoi duplicare una richiesta precedente da [!UICONTROL Request Manager] se necessario.

Per ulteriori informazioni su [!DNL Data Warehouse], consulta i seguenti collegamenti nella documentazione di [!DNL Analytics]:

* [Creare una richiesta di Data Warehouse](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/t-dw-create-request.html)
* [Best practice per la Data Warehouse](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-bp.html)
