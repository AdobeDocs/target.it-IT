---
keywords: offerta remota;contenuto memorizzato nella cache;contenuto dinamico;tipo url
description: Scopri come sfruttare le offerte remote in [!DNL Target] per ospitare contenuti esterni da un CMS o da altri sistemi.
title: Come si creano le offerte remote?
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#beta newtab=true" tooltip="Cosa sono le funzioni beta in [!DNL Adobe Target]."
hide: true
hidefromtoc: true
exl-id: e83ad57e-716d-4595-b5cf-3a882fcb9e37
source-git-commit: c7d6998ffb048b1a7895e4c48b557cdb16ff510c
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 19%

---

# Creare offerte remote

Utilizzare le offerte remote per l&#39;hosting di contenuto esterno a [!DNL Adobe Target], consentendo a [!DNL Target] di fare riferimento a tali contenuti e di distribuirli ai siti Web degli utenti. Questi contenuti possono trovarsi in un sistema di gestione dei contenuti (CMS) o in un altro sistema per motivi di facilità d’uso o sicurezza.

>[!NOTE]
>
>Questo articolo contiene informazioni sugli aggiornamenti dell&#39;interfaccia utente [!DNL Target] che fa attualmente parte di un programma Beta. Il team [!DNL Adobe Target] spesso abilita nuove funzionalità per determinati clienti a scopo di test e feedback. Al termine del periodo di test, queste funzioni vengono abilitate per tutti i clienti nelle prossime versioni di [!DNL Target Standard/Premium] e annunciate nelle note sulla versione.

Le offerte remote possono essere create nella pagina [!UICONTROL Offers] > [!UICONTROL Code Offers] o nel [Compositore esperienza basato su Forms](/help/main/c-experiences/form-experience-composer.md). Impossibile creare o applicare offerte remote in [!UICONTROL Visual Experience Composer] (VEC). Il contenuto viene inserito nei percorsi di richiesta [!DNL Target], pertanto è molto probabile che questi percorsi non siano appropriati per una richiesta globale di [!DNL Target].

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

  Ciò significa che quando si sposta l’attività dai server di staging alla produzione, il contenuto è automaticamente accessibile senza dover modificare manualmente l’URL.

* Se il test coinvolge dati generati dinamicamente dal server, l&#39;opzione [!UICONTROL Dynamic] potrebbe essere la scelta giusta.
* Se si intende testare solo l&#39;aspetto del contenuto dell&#39;offerta remota esistente, utilizzare [!UICONTROL Visual Experience Composer] per modificare l&#39;aspetto del contenuto restituito dal sistema di gestione dei contenuti.
* Utilizza la [matrice per la selezione delle offerte remote](#reference_B23BEDD29DDD47709A7651AFD27E776B) (di seguito) per aiutarti a scegliere l&#39;offerta più adatta al tuo caso specifico. Se hai domande, rivolgiti al rappresentante del tuo account.

## Crea un&#39;offerta remota dalla pagina [!UICONTROL Code Offers]

1. Fare clic su **[!UICONTROL Offers]**, quindi selezionare la scheda **[!UICONTROL Code Offers]**.

1. Fare clic su **[!UICONTROL Create Offer]** > **[!UICONTROL Remote Offer]**.

1. Nella finestra di dialogo [!UICONTROL Create Remote Offer], fornisci un nome descrittivo per l&#39;offerta.

   Un nome descrittivo consente a te e agli altri utenti di trovare rapidamente l&#39;offerta nella libreria [!UICONTROL Offers].

1. (Condizionale) Se disponi di un [account Target Premium](/help/main/c-intro/intro.md#premium), seleziona l&#39;[area di lavoro](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC) desiderata.

1. Specifica il tipo di URL di reindirizzamento.

   Per ulteriori informazioni, vedere [Tipo di URL di reindirizzamento: [!UICONTROL Onsite Cached] o [!UICONTROL Onsite Dynamic]](#url-type).

1. Specifica l’URL remoto assoluto per l’offerta remota.

1. Fare clic su **[!UICONTROL Create]**.

## Crea un&#39;offerta remota utilizzando [!UICONTROL Form-Based Experience Composer]

1. Durante la creazione di un&#39;attività tramite [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md), selezionare il percorso in cui visualizzare la sezione **[!UICONTROL Content]**.

1. Fare clic sull&#39;elenco a discesa **[!UICONTROL Default Content]**, quindi fare clic su **[!UICONTROL Change Remote Offer]**.

1. Fare clic su **[!UICONTROL Create]** > **[!UICONTROL Remote Offer]**.

1. Inserisci un nome descrittivo per l’offerta.

   Un nome descrittivo consente a te e agli altri utenti di trovare rapidamente l&#39;offerta nella libreria [!UICONTROL Assets].

1. Specifica il tipo di URL di reindirizzamento.

   Per ulteriori informazioni, vedere [Tipo di URL di reindirizzamento: [!UICONTROL Onsite Cached] o [!UICONTROL Onsite Dynamic]](#url-type).

1. Specifica l’URL remoto per l’offerta remota.

1. Fare clic su **[!UICONTROL Save]**.

## Tipo di URL di reindirizzamento: [!UICONTROL Onsite Cached] o [!UICONTROL Onsite Dynamic] {#url-type}

Le seguenti informazioni sono utili per comprendere le differenze tra le due opzioni:

### URL [!UICONTROL Onsite Cached]

Il contenuto di un&#39;offerta remota memorizzata nella cache è servito da [!DNL Target].

Ogni due ore, [!DNL Target] recupera il contenuto dall&#39;URL remoto e quindi lo archivia in [!DNL Target]. Quando i visitatori caricano un sito con un&#39;esperienza che include un&#39;offerta remota, [!DNL Target] consegna l&#39;offerta.

Le offerte remote memorizzate nella cache forniscono un livello di protezione maggiore perché il contenuto non può essere modificato da qualcuno che ha effettuato l&#39;accesso a [!DNL Target]. Per modificare il contenuto, è necessario accedere al sistema di gestione dei contenuti o a un altro sistema e modificare il contenuto da tale ambiente.

L’URL di un’offerta remota memorizzata nella cache può essere assoluto o relativo.

### URL [!UICONTROL Onsite Dynamic]

Un&#39;offerta remota dinamica viene distribuita dal sistema di gestione dei contenuti o da un altro sistema anziché da [!DNL Target].

È possibile che non si desideri che il contenuto venga periodicamente memorizzato nella cache e quindi consegnato da [!DNL Target] ogni volta che un visitatore carica un sito con un&#39;esperienza che include un&#39;offerta remota. Piuttosto, desideri chiamare il sistema che ospita il contenuto e possibilmente passare informazioni specifiche in modo che l’offerta restituita possa essere dinamica (o diversa) per ogni utente. Ad esempio, se un utente accede al sito web della sua carta di credito e il sito include un’esperienza con un’offerta remota dinamica, puoi passare nell’URL parametri specifici per informazioni sul conto dell’utente. Quindi il sito web potrebbe fornire informazioni specifiche per questo utente, ad esempio il saldo del conto.

È possibile fare clic su **[!UICONTROL Add Parameter]** per aggiungere una o più richieste [!DNL Target] o parametri di richiesta.

## Utilizzare le offerte remote nelle attività

È necessario applicare le offerte remote utilizzando [!UICONTROL Form-Based Experience Composer]. Al momento non è possibile applicare offerte remote utilizzando [!UICONTROL Visual Experience Composer] (VEC).

[!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] è un&#39;interfaccia non visiva per la creazione di esperienze e offerte, utile per creare le esperienze da utilizzare nelle attività [!UICONTROL A/B Tests], [!UICONTROL Experience Targeting] (XT), [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Recommendations] quando [!UICONTROL Visual Experience Composer] non è disponibile o se non risulta pratico. È ad esempio possibile utilizzare [!UICONTROL Form-Based Experience Composer] per creare esperienze che utilizzano offerte remote.

1. Crea o modifica un&#39;attività in [!UICONTROL Form-Based Experience Composer].

   Per istruzioni dettagliate, consulta [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

1. Specifica la posizione desiderata e aggiungi eventuali perfezionamenti del pubblico secondo necessità.

1. Fare clic sull&#39;elenco a discesa nella sezione **[!UICONTROL Content]**, quindi fare clic su **[!UICONTROL Change Remote Offer]**.

1. Selezionare l&#39;offerta remota desiderata dalla finestra di dialogo [!UICONTROL Select Remote Offer], quindi fare clic su **[!UICONTROL Done]**.

1. Termina la configurazione dell’attività.

## Funzionamento delle offerte remote dinamiche {#concept_CC2A969420B34364A9FA78C1CE251818}

Nelle offerte remote dinamiche, i valori necessari vengono passati all’offerta tramite la tecnologia per pagina dinamica.

L’offerta viene eseguita dopo aver effettuato il rendering della pagina. Un iFrame invisibile raccoglie i dati, li copia dal frame e li inserisce nella pagina, caricando i valori passati.

![immagine remote_offer_howitworks_2](assets/remote_offer_howitworks_2.jpeg)

1. Il browser del visitatore richiede una pagina dal server.

2. Il browser esegue il rendering della pagina, comprese le mbox.

3. La chiamata `mboxCreate` include i parametri necessari per il rendering del contenuto dinamico.

4. [!DNL Target] restituisce l&#39;URL con la posizione del contenuto dinamico e i relativi parametri. Imposta un iFrame nell&#39;area mbox.

5. Il browser richiede l’URL ed esegue il rendering nella pagina.

## Matrice per la selezione dell’offerta remota {#reference_B23BEDD29DDD47709A7651AFD27E776B}

La matrice di selezione dell&#39;offerta remota consente di scegliere il tipo di offerta remota: [!UICONTROL Onsite Cached] o [!UICONTROL Onsite Dynamic].

| Funzione | Memoria nella cache nel sito | Dinamico nel sito |
|--- |--- |--- |
| Aggiornamenti ogni volta che un visitatore effettua una richiesta | No | Sì |
| Aggiornamenti di contenuto | Memorizzazione nella cache ogni due ore | Aggiornamento immediato ad ogni richiesta |
| Tempo di caricamento | Più veloce | Più lento a causa della richiesta di elaborazione |
| Può vedere JavaScript a pagina | Sì | No, ma può passare tramite URL |
| Le offerte possono includere JavaScript | Sì | Sì |
| URL di offerta | Assoluto o relativo | Relativo |
| Richiesta computer | Server Adobe | Il computer del visitatore, che trasporta i suoi cookies |

## Video di formazione: Compositore basato su moduli ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video fornisce una demo di [!UICONTROL Form-Based Experience Composer], che puoi utilizzare per creare offerte remote.

* Crea un&#39;attività utilizzando [!UICONTROL Form-Based Experience Composer]
* Scopri quando utilizzare [!UICONTROL Form-Based Experience Composer] rispetto a [!UICONTROL Visual Experience Composer]
* Indirizzare una posizione con i perfezionamenti

>[!VIDEO](https://video.tv.adobe.com/v/17390)
