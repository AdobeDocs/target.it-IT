---
keywords: offerta remota;matrice di selezione offerta remota;contenuto memorizzato nella cache;contenuto dinamico;tipo url
description: Scopri come utilizzare le offerte remote in Adobe [!DNL Target] per ospitare contenuto esterno (contenuto in un CMS o in un altro sistema). Scopri perché potresti voler utilizzare le offerte remote.
title: Come si creano le offerte remote?
feature: Experiences and Offers
exl-id: 6a5283ee-c1fb-49f7-8e7f-c23ccde26ade
source-git-commit: e8201198dc6ac36e803153d5c6b345a30716204a
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 29%

---

# Creare offerte remote

Utilizza le offerte remote per l’hosting di contenuti esterni a [!DNL Adobe Target] a cui [!DNL Target] può fare riferimento per consegnarli ai siti web degli utenti. Il contenuto potrebbe trovarsi in un sistema di gestione dei contenuti (CMS) o in un altro sistema, per motivi di facilità d’uso o di sicurezza.

>[!NOTE]
>
>Le offerte remote possono essere create nella pagina [!UICONTROL Offers] > [!UICONTROL Code Offers] o nel [Compositore esperienza basato su Forms](/help/main/c-experiences/form-experience-composer.md). Non è possibile creare o applicare offerte remote nel Compositore esperienza visivo. Il contenuto verrà inserito nei percorsi di richiesta [!DNL Target], pertanto è molto probabile che non siano appropriati per una richiesta globale di [!DNL Target].
>
>[!DNL Target Classic] include funzionalità simili: [!UICONTROL Offer on Your Site] e [!UICONTROL Offer Outside Test&Target].

Alcuni esempi di offerte remote includono:

* Diverse versioni di cross-selling
* Messaggi dinamici per il carrello acquisti
* Moduli
* Calcolatori
* Aggiornamenti del tasso di interesse
* E-mail
* Chioschi
* Assistenti vocali

## Best practice per l’utilizzo delle offerte remote {#section_7718512D08E14121B6F6B8C38134F4BC}

Best practice per l’utilizzo delle offerte remote nelle attività:

* Se l&#39;offerta si trova nello stesso dominio delle richieste [!DNL Target], l&#39;utilizzo dell&#39;opzione [!UICONTROL Cached] consente di utilizzare URL relativi per descrivere la posizione dell&#39;offerta.

  Ciò significa che quando sposti l’attività dai server di gestione temporanea alla produzione, il contenuto sarà automaticamente accessibile senza dover modificare manualmente l’URL.

* Se il test coinvolge dati generati dinamicamente dal server, l&#39;opzione [!UICONTROL Dynamic] potrebbe essere la scelta giusta.
* Se si intende testare solo l&#39;aspetto del contenuto dell&#39;offerta remota esistente, utilizzare [!UICONTROL Visual Experience Composer] per modificare l&#39;aspetto del contenuto restituito dal sistema di gestione dei contenuti.
* Utilizza la [matrice per la selezione delle offerte remote](#reference_B23BEDD29DDD47709A7651AFD27E776B) (di seguito) per aiutarti a scegliere l&#39;offerta più adatta al tuo caso specifico. Se hai domande, rivolgiti al rappresentante del tuo account.

## Creare un’offerta remota dalla pagina Offerte di codice

1. Fare clic su **[!UICONTROL Offers]**, quindi selezionare la scheda **[!UICONTROL Code Offers]**.

   ![Offerte > Offerte codice](/help/main/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. Fare clic su **[!UICONTROL Create]** > **[!UICONTROL Remote Offer]**.

   ![Finestra di dialogo Crea offerta remota](/help/main/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Inserisci un nome descrittivo per l’offerta.

   Un nome descrittivo consente a te e agli altri utenti di trovare rapidamente l&#39;offerta nella libreria [!UICONTROL Assets].

1. Specifica il tipo di URL di reindirizzamento.

   Per ulteriori informazioni, vedi [Tipo di URL di reindirizzamento: memorizzato in cache o dinamico](#url-type) di seguito.

1. Specifica l’URL remoto per l’offerta remota.

1. Fare clic su **[!UICONTROL Save]**.

## Creare un’offerta remota utilizzando il Compositore esperienza basato su moduli

1. Durante la creazione di un&#39;attività tramite [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md), selezionare il percorso in cui visualizzare la sezione **[!UICONTROL Content]**.

   ![Sezione contenuto nel Compositore esperienza basato su moduli](/help/main/c-experiences/c-manage-content/assets/form-based-content.png)

1. Fare clic sull&#39;elenco a discesa **[!UICONTROL Default Content]**, quindi fare clic su **[!UICONTROL Change Remote Offer]**.

   ![Modifica offerta remota](/help/main/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Fare clic su **[!UICONTROL Create]** > **[!UICONTROL Remote Offer]**.

   ![Finestra di dialogo Crea offerta remota](/help/main/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Inserisci un nome descrittivo per l’offerta.

   Un nome descrittivo consente a te e agli altri utenti di trovare rapidamente l&#39;offerta nella libreria [!UICONTROL Assets].

1. Specifica il tipo di URL di reindirizzamento.

   Per ulteriori informazioni, vedi [Tipo di URL di reindirizzamento: memorizzato in cache o dinamico](#url-type) di seguito.

1. Specifica l’URL remoto per l’offerta remota.

1. Fare clic su **[!UICONTROL Save]**.

## Tipo di URL di reindirizzamento: memorizzato in cache o dinamico {#url-type}

Le seguenti informazioni sono utili per comprendere le differenze tra le due opzioni:

### URL nella cache

Il contenuto di un&#39;offerta remota memorizzata nella cache è servito da [!DNL Target].

Ogni due ore, [!DNL Target] recupera il contenuto dall&#39;URL remoto e quindi lo archivia in [!DNL Target]. Quando i visitatori caricano un sito con un&#39;esperienza che include un&#39;offerta remota, l&#39;offerta viene consegnata da [!DNL Target].

Le offerte remote memorizzate nella cache forniscono un livello di protezione maggiore perché il contenuto non può essere modificato da qualcuno che ha effettuato l&#39;accesso a [!DNL Target]. Per modificare il contenuto, è necessario accedere al sistema di gestione dei contenuti o a un altro sistema e modificare il contenuto da tale ambiente.

L’URL di un’offerta remota memorizzata nella cache può essere assoluto o relativo.

### URL dinamico

Un&#39;offerta remota dinamica viene distribuita dal sistema di gestione dei contenuti o da un altro sistema anziché da [!DNL Target].

È possibile che non si desideri che il contenuto venga periodicamente memorizzato nella cache e quindi consegnato da [!DNL Target] ogni volta che un visitatore carica un sito con un&#39;esperienza che include un&#39;offerta remota. Piuttosto, desideri chiamare il sistema che ospita il contenuto e possibilmente passare informazioni specifiche in modo che l’offerta restituita possa essere dinamica (o diversa) per ogni utente. Ad esempio, se un utente accede al sito web della sua carta di credito e il sito include un’esperienza con un’offerta remota dinamica, puoi passare nell’URL parametri specifici per informazioni sul conto dell’utente. Quindi il sito web potrebbe fornire informazioni specifiche per questo utente, ad esempio il saldo del conto.

È possibile fare clic su **[!UICONTROL Add Parameter]** per aggiungere una o più richieste [!DNL Target] o parametri di richiesta.

## Utilizzare le offerte remote nelle attività

È necessario applicare le offerte remote utilizzando [!UICONTROL Form-Based Experience Composer]. Al momento non è possibile applicare offerte remote utilizzando il Compositore esperienza visivo.

[!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] è un&#39;interfaccia non visiva per la creazione di esperienze e offerte, utile per creare le esperienze da utilizzare nelle attività [!UICONTROL A/B Tests], [!UICONTROL Experience Targeting] (XT), [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Recommendations] quando il Compositore esperienza visivo non è disponibile o se non risulta pratico. È ad esempio possibile utilizzare [!UICONTROL Form-Based Experience Composer] per creare esperienze che utilizzano offerte remote.

1. Crea o modifica un&#39;attività in [!UICONTROL Form-Based Experience Composer].

   Per istruzioni dettagliate, consulta [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

1. Specifica la posizione desiderata e aggiungi eventuali perfezionamenti del pubblico secondo necessità.

1. Fare clic sull&#39;elenco a discesa nella sezione **[!UICONTROL Content]**, quindi fare clic su **[!UICONTROL Change Remote Offer]**.

   ![Modifica offerta remota](/help/main/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Selezionare l&#39;offerta remota desiderata dalla finestra di dialogo [!UICONTROL Select Remote Offer], quindi fare clic su **[!UICONTROL Done]**.

1. Termina la configurazione dell’attività.

## Funzionamento delle offerte remote dinamiche {#concept_CC2A969420B34364A9FA78C1CE251818}

Nelle offerte remote dinamiche, i valori necessari vengono passati all’offerta tramite la tecnologia per pagina dinamica.

L’offerta viene eseguita dopo aver effettuato il rendering della pagina. Un iframe invisibile raccoglie i dati, li copia dal frame e li inserisce nella pagina, caricando i valori passati.

![immagine remote_offer_howitworks_2](assets/remote_offer_howitworks_2.jpeg)

## Matrice per la selezione dell’offerta remota {#reference_B23BEDD29DDD47709A7651AFD27E776B}

La matrice per la selezione delle offerte remote consente di decidere il tipo di offerta remota da scegliere: [!UICONTROL Cached] o [!UICONTROL Dynamic].

| Funzione | Memorizzato in cache | Dinamico |
|--- |--- |--- |
| Aggiornamenti ogni volta che un visitatore effettua una richiesta | No | Sì |
| Aggiornamenti di contenuto | Salvato nella cache ogni 2 ore | Aggiornamento immediato ad ogni richiesta |
| Tempo di caricamento | Più veloce | Più lento a causa della richiesta di elaborazione |
| Può vedere JavaScript a pagina | Sì | No, ma può passare tramite URL |
| Le offerte possono includere JavaScript | Sì | Sì |
| URL di offerta | Assoluto o relativo | Relativo |
| Richiesta computer | Server Adobe | Il computer del visitatore, che trasporta i suoi cookies |

## Video di formazione: Compositore basato su moduli ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video offre una demo del compositore basato su moduli, che puoi utilizzare per creare offerte remote.

* Creare un’attività utilizzando il Compositore esperienza basato su moduli
* Quando utilizzare il Compositore esperienza basato su moduli o il Compositore esperienza visivo
* Indirizzare una posizione con i perfezionamenti

>[!VIDEO](https://video.tv.adobe.com/v/17390)
