---
keywords: Consigli;impostazioni;preferenze;settore verticale;filtrare criteri incompatibili;gruppo host predefinito;URL base miniature;token API consigli
description: 'Scopri come implementare le attività Recommendations in Adobe Target. '
title: Come Si Implementano Le Attività Recommendations?
feature: Recommendations
exl-id: b6edb504-a8b6-4379-99c1-6907e71601f9
source-git-commit: 6d601c0099e9e8451571af7b75641620a94578fc
workflow-type: tm+mt
source-wordcount: '1544'
ht-degree: 30%

---

# ![PREMIUM](/help/assets/premium.png) Pianificare e implementare [!DNL Recommendations]

Prima di configurare la prima [!DNL Recommendations] attività in [!DNL Adobe Target], completa i seguenti passaggi:

1. [Implementare [!DNL Target]](#implement-target) sul web e sulle superfici dell’app mobile da utilizzare per acquisire il comportamento degli utenti e distribuire consigli.
1. [Imposta il tuo [!DNL Recommendations] catalogo](#rec-catalog) di prodotti o contenuti da consigliare agli utenti.
1. [Trasmettere informazioni comportamentali e contesto](#pass-behavioral) a [!DNL Target Recommendations] per offrire consigli personalizzati.
1. [Configurare le esclusioni globali](#exclusions).
1. [Configura [!DNL Recommendations] impostazioni](#concept_C1E1E2351413468692D6C21145EF0B84).

## Implementate [!DNL Target] {#implement-target}

[!DNL Target Recommendations] richiede di implementare [!DNL Adobe Experience Platform Web SDK] o at.js 0.9.2 (o versione successiva). Vedi [Implementare [!DNL Target]](/help/c-implementing-target/implementing-target.md) per ulteriori informazioni.

## Configurare il catalogo Recommendations {#rec-catalog}

Per fornire consigli di alta qualità, [!DNL Target] devono essere a conoscenza dei prodotti o dei contenuti da consigliare. In genere, il catalogo deve includere tre tipi di informazioni sugli elementi da consigliare. Supponiamo di consigliare i film. Includi quanto segue:

1. Dati da presentare all’utente che riceve il consiglio. Ad esempio, puoi visualizzare il nome del filmato e un URL per un’immagine in miniatura del poster del filmato.
1. Dati utili per applicare controlli di marketing e merchandising. Ad esempio, è possibile visualizzare la valutazione del filmato in modo da non consigliare i film NC-17.
1. Dati utili per determinare la somiglianza di elementi con altri elementi. Ad esempio, è possibile visualizzare il genere del filmato e il regista del filmato.

[!DNL Target] offre diverse opzioni di integrazione per compilare il catalogo. Queste opzioni possono essere utilizzate in combinazione per aggiornare diversi elementi nel catalogo o per aggiornare diversi attributi di elementi su diverse frequenze.

| Metodo | Che cosa è | Quando usarlo | Informazioni aggiuntive |
| --- | --- | --- | --- |
| Feed di catalogo | Pianificare un feed (CSV, Google Product XML, o [!DNL Analytics Product Classifications]) da caricare e acquisire su base giornaliera. | Per l’invio di informazioni su più elementi alla volta. Per l’invio di informazioni che cambiano raramente. | Vedi [Feed](/help/c-recommendations/c-products/feeds.md). |
| API per entità | Chiama un’API per inviare aggiornamenti al minuto per un singolo elemento. | Per l’invio di aggiornamenti in tempo reale su un elemento alla volta. Per l’invio di informazioni che cambiano frequentemente (ad esempio a livello di prezzo, scorte e scorte). | Consulta la sezione [Documentazione per gli sviluppatori API per entità](https://developers.adobetarget.com/api/recommendations/#tag/Entities). |
| Trasmettere gli aggiornamenti sulla pagina | Invia aggiornamenti al minuto per un singolo elemento utilizzando JavaScript nella pagina o utilizzando l’API di consegna. | Per l’invio di aggiornamenti in tempo reale su un elemento alla volta. Per l’invio di informazioni che cambiano frequentemente (ad esempio a livello di prezzo, scorte e scorte). | Vedi [Visualizzazioni di elementi/pagine di prodotti](#items-product-pages) sotto. |

La maggior parte dei clienti deve implementare almeno un feed. Puoi quindi scegliere di integrare il feed con aggiornamenti per gli attributi o gli elementi modificati di frequente utilizzando l’API Entità o il metodo on-the-page.

## Trasmettere informazioni comportamentali e contesto {#pass-behavioral}

Informazioni comportamentali e contesto a cui passare [!DNL Target] dipende dall’azione eseguita dal visitatore, spesso associata al tipo di pagina con cui il visitatore interagisce.

### Visualizzazioni di elementi/pagine di prodotti {#items-product-pages}

Sulle pagine in cui un visitatore sta visualizzando un singolo elemento, ad esempio una pagina di dettaglio del prodotto, devi trasmettere l’identità dell’elemento che il visitatore sta visualizzando. È inoltre necessario passare la categoria più granulare dell’elemento visualizzato dal visitatore, per consentire di filtrare i consigli per la categoria corrente.

Puoi anche passare alcuni attributi che cambiano rapidamente nella pagina del prodotto stessa. Ad esempio, puoi passare il prezzo (`value`) e livello scorte/scorte.

```
<script type="text/javascript">
function targetPageParams() { 
   return { 
      "entity": { 
         "id": "32323", 
         "categoryId": "running-shoes", 
         "value": 119.99, 
         "inventory": 329 
      } 
   } 
}
</script>
```

### Visualizzazioni di categoria/pagine di categoria

In una pagina categoria, è probabile che si desideri limitare i consigli a prodotti o contenuti all’interno di tale categoria. A questo scopo, accertati di trasmettere l’identità della categoria attualmente visualizzata.

```
function targetPageParams() { 
   return { 
      "entity": { 
         "categoryId": "running-shoes" 
      } 
   } 
}
```

### Aggiunte/visualizzazioni carrello/pagine di pagamento {#cart}

Su una pagina del carrello, puoi consigliare gli elementi in base al contenuto del carrello corrente del visitatore. A tal fine, trasmetti gli ID di tutti gli elementi nel carrello corrente del visitatore utilizzando il parametro speciale `cartIds`.

```
function targetPageParams() {
   return {
      "cartIds": ["352", "223", "23432", "432", "553"]
      }
}
```

La logica dei consigli basati sul carrello è simile alla &quot;[!UICONTROL Consigliato]&quot; algoritmo basato su utenti e al &quot;[!UICONTROL Chi li ha visti, li ha comprati]&quot; e &quot;[!UICONTROL Chi ha comprato questi ha acquistato quelli]&quot; algoritmi basati su elementi.

[!DNL Target] utilizza tecniche di filtro collaborativo per determinare le somiglianze per ogni elemento nel carrello del visitatore, quindi combina queste somiglianze comportamentali tra ciascun elemento per ottenere un elenco unito.

[!DNL Target] offre anche agli esperti di marketing la possibilità di osservare il comportamento dei visitatori in una singola sessione o in più sessioni:

* **All&#39;interno di una singola sessione**: In base a ciò che hanno fatto altri visitatori all’interno di una singola sessione.

   Osservare il comportamento all’interno di una singola sessione potrebbe avere senso quando si ha la sensazione che i prodotti si &quot;incontrino&quot; fortemente in base a un utilizzo, un’occasione o un evento. Ad esempio, un visitatore sta acquistando una stampante e potrebbe anche aver bisogno di inchiostro e carta. Oppure, un visitatore sta comprando burro di arachidi e potrebbe anche avere bisogno di pane e gelatina.

* **In più sessioni**: In base a ciò che altri visitatori hanno fatto in più sessioni.

   Osservare il comportamento in più sessioni potrebbe avere senso quando si ha la sensazione che i prodotti si &quot;incontrino&quot; fortemente in base alla preferenza o al gusto del visitatore. Ad esempio, a un visitatore piace Star Wars e potrebbe piacere anche Indiana Jones, anche se il visitatore non vuole necessariamente guardare entrambi i film nella stessa seduta. Oppure, a un visitatore piace il gioco della bacheca &quot;Codenames&quot; e potrebbe anche piacere il gioco della bacheca &quot;Avalon&quot;, anche se il visitatore non può giocare entrambi i giochi contemporaneamente. 

[!DNL Target] formula raccomandazioni per ogni visitatore in base agli elementi nel carrello corrente, indipendentemente dal fatto che osservi il comportamento del visitatore in una singola sessione o in più sessioni.

### Escludere gli elementi già presenti nel carrello del visitatore

Nelle pagine di tutto il sito, potete escludere alcuni elementi dai consigli. Ad esempio, potresti non voler consigliare gli elementi già presenti nel carrello corrente del visitatore. A tal fine, passa gli ID di tutti gli elementi che desideri escludere utilizzando il parametro speciale `excludedIds`.

```
function targetPageParams() {
   return {
      "excludedIds": ["352", "223", "23432", "432", "553"]
      }
}
```

### Pagine di conferma acquisti/ordini

Quando si verifica un evento di acquisto, trasmettere l&#39;identità dell&#39;articolo o degli articoli acquistati. Vedi [Tracciare le conversioni](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053) in *Implementare [!DNL Target] senza un gestore di tag*.

## Configurare le esclusioni globali {#exclusions}

Escludi gli elementi a livello globale che non vorresti consigliare a un visitatore. Consulta [Esclusioni](/help/c-recommendations/c-products/exclusions.md).

## Configura [!DNL Recommendations] impostazioni {#concept_C1E1E2351413468692D6C21145EF0B84}

Utilizza le impostazioni per gestire l’implementazione di [!DNL Recommendations].

Per accedere al [!UICONTROL Impostazioni Recommendations] opzioni, apri [!DNL Target] in [!DNL Adobe Experience Cloud], quindi fai clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Impostazioni]**.

![](assets/recs_settings.png)

Sono disponibili le seguenti opzioni:

| Impostazione | Descrizione |
|--- |--- |
| Mbox globale personalizzata | (Facoltativo) Specifica la mbox globale personalizzata utilizzata per le attività di [!DNL Target]. Per impostazione predefinita, la mbox globale utilizzata da [!DNL Target] viene utilizzato per [!DNL Recommendations].<br>Nota: Questa opzione è impostata su [!DNL Target] [!UICONTROL Amministrazione] pagina. Apri [!DNL Target], quindi fai clic su [!UICONTROL Amministrazione] > [!UICONTROL Compositore esperienza visivo]. |
| Settore verticale | Il settore verticale è utilizzato per aiutare a categorizzare i criteri per i consigli. Queste informazioni consentono ai membri del team di individuare criteri rilevanti per una pagina specifica, ad esempio i criteri più adatti per la pagina del carrello o per una pagina multimediale. |
| Filtra criteri incompatibili | Abilita questa opzione per mostrare solo i criteri per i quali la pagina selezionata trasmette i dati richiesti. Non tutti i criteri vengono eseguiti correttamente su ogni pagina. La pagina o mbox deve passare `entity.id` o `entity.categoryId` per rendere compatibili i consigli per l’elemento o la categoria corrente. In generale, è consigliabile mostrare solo i criteri compatibili. Per fare in modo che i criteri incompatibili siano disponibili per l’attività, deseleziona questa opzione.<br>È consigliabile disattivare l’opzione se utilizzi una soluzione di gestione tag.<br>Per ulteriori informazioni su questa opzione, consulta [Domande frequenti su Recommendations](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md). |
| Gruppo host predefinito | Seleziona il gruppo host predefinito.<br>Il gruppo di host può essere utilizzato per separare gli elementi disponibili nel catalogo per usi diversi. Ad esempio, puoi utilizzare i gruppi di host per ambienti di sviluppo e produzione, marchi diversi o diverse aree geografiche. Per impostazione predefinita, i risultati dell&#39;anteprima in Ricerca nel catalogo, Raccolte ed Esclusioni si basano sul gruppo di host predefinito. Puoi anche selezionare un gruppo di host diverso per visualizzare in anteprima i risultati, utilizzando il filtro Ambiente. Per impostazione predefinita, gli elementi appena aggiunti sono disponibili in tutti i gruppi di host, a meno che non sia specificato un ID ambiente al momento della creazione o dell&#39;aggiornamento dell&#39;elemento. I consigli distribuiti dipendono dal gruppo di host specificato nella richiesta.<br>Se i prodotti non vengono visualizzati, assicurati di utilizzare il gruppo host corretto. Ad esempio, se imposti che il consiglio usi un ambiente di gestione temporanea e imposti il gruppo host su Gestione temporanea, potrebbe essere necessario ricreare le raccolte nell&#39;ambiente di gestione temporanea perché si visualizzino i prodotti. Per visualizzare i prodotti disponibili in ogni ambiente, utilizza Ricerca catalogo con ogni ambiente. Puoi anche visualizzare in anteprima il contenuto delle raccolte ed esclusioni di Recommendations per un ambiente selezionato (gruppo di host).<br>**Nota:** dopo aver modificato l’ambiente selezionato, fai clic su Cerca per aggiornare i risultati restituiti.<br>Il filtro [!UICONTROL Ambiente] è disponibile nelle seguenti posizioni nell’interfaccia utente [!DNL Target]:<ul><li>Ricerca nel catalogo (Recommendations > Ricerca nel catalogo)</li><li>Finestra di dialogo Crea raccolta ([!UICONTROL Recommendations > Raccolte > Crea nuova])</li><li>Finestra di dialogo Aggiorna raccolta ([!UICONTROL Recommendations > Raccolte > Modifica])</li><li>Finestra di dialogo Crea esclusione ([!UICONTROL Recommendations > Esclusioni > Crea nuova])</li><li>Finestra di dialogo Aggiorna esclusione ([!UICONTROL Recommendations > Esclusioni > Modifica])</li></ul>Per ulteriori informazioni, consulta [Host](/help/administrating-target/hosts.md). |
| URL di base per le miniature | L&#39;impostazione di un URL di base per il catalogo dei prodotti rende possibile l’utilizzo di URL relativi quando specifichi le miniature dei prodotti fornendo l’URL della miniatura.<br>Ad esempio:<br>`"entity.thumbnailURL=/Images/Homepage/product1.jpg"`<br>imposta un URL relativo all’URL di base della miniatura. |
| Token API per consigli | Utilizza questo token nelle chiamate API per la funzione Consigli, ad esempio l’API di download. |
