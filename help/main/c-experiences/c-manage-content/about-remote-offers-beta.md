---
keywords: offerta remota;contenuto memorizzato nella cache;contenuto dinamico;tipo url
description: Scopri come utilizzare le offerte remote in [!DNL Target] per ospitare contenuti esterni (contenuti in un CMS o altro sistema).
title: Come si creano le offerte remote?
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#beta newtab=true" tooltip="Cosa sono le funzioni beta in [!DNL Adobe Target]."
hide: true
hidefromtoc: true
source-git-commit: 26cb9d6a2359714f41acaf91c6e26a7e0ac93238
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 21%

---

# Creare offerte remote

Utilizza le offerte remote per l’hosting di contenuti esterni a [!DNL Adobe Target] a cui [!DNL Target] può fare riferimento per consegnarli ai siti web degli utenti. Questi contenuti possono trovarsi in un sistema di gestione dei contenuti (CMS) o in un altro sistema, per motivi di facilità d’uso o di sicurezza.

>[!NOTE]
>
>Questo articolo contiene informazioni sugli aggiornamenti di [!DNL Target] che fa attualmente parte di un programma beta. Il [!DNL Adobe Target] team abilita spesso nuove funzioni per determinati clienti a scopo di test e feedback. Al termine del periodo di test, queste funzioni saranno abilitate per tutti i clienti in futuro [!DNL Target Standard/Premium] e annunciate nelle note sulla versione.

Le offerte remote possono essere create su [!UICONTROL Offers] > [!UICONTROL Code Offers] pagina o in [Compositore esperienza basato su Forms](/help/main/c-experiences/form-experience-composer.md). Non è possibile creare o applicare offerte remote in [!UICONTROL Visual Experience Composer] (VEC). Il contenuto viene iniettato nel [!DNL Target] richiedono posizioni, pertanto è molto probabile che queste non siano appropriate per una [!DNL Target] richiesta.

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

* Se l&#39;offerta risiede nello stesso dominio del [!DNL Target] richieste, utilizzando [!UICONTROL Cached] Questa opzione ti consente di utilizzare URL relativi per descrivere la posizione dell’offerta.

  Ciò significa che quando si sposta l’attività dai server di staging alla produzione, il contenuto è automaticamente accessibile senza dover modificare manualmente l’URL.

* Se il test coinvolge dati generati dinamicamente dal server, il [!UICONTROL Dynamic] potrebbe essere la scelta giusta.
* Se prevedi di testare solo l’aspetto del contenuto dell’offerta remota esistente, utilizza [!UICONTROL Visual Experience Composer] per modificare l&#39;aspetto del contenuto restituito dal sistema di gestione dei contenuti.
* Utilizza il [Matrice per la selezione dell’offerta remota](#reference_B23BEDD29DDD47709A7651AFD27E776B) (di seguito) per aiutarti a scegliere l’offerta più adatta al tuo caso specifico. Se hai domande, rivolgiti al rappresentante del tuo account.

## Creare un’offerta remota da [!UICONTROL Code Offers] pagina

1. Clic **[!UICONTROL Offers]**, quindi seleziona la **[!UICONTROL Code Offers]** scheda.

   ![Offerte > Offerte codice](/help/main/c-experiences/c-manage-content/assets/offers-code-offers-new.png)

1. Clic **[!UICONTROL Create Offer]** > **[!UICONTROL Remote Offer]**.

   ![Finestra di dialogo Crea offerta remota](/help/main/c-experiences/c-manage-content/assets/remote_offer_ui_new.png)

1. Inserisci un nome descrittivo per l’offerta.

   Un nome descrittivo consente a te e agli altri utenti di trovare rapidamente l’offerta nel [!UICONTROL Assets] libreria.

1. (Condizionale) Se disponi di [Account Target Premium](/help/main/c-intro/intro.md#premium), seleziona la [workspace](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC).

1. Specifica il tipo di URL di reindirizzamento.

   Consulta [Tipo di URL di reindirizzamento: memorizzato in cache o dinamico](#url-type) per ulteriori informazioni.

1. Specifica l’URL remoto assoluto per l’offerta remota.

1. Clic **[!UICONTROL Create]**.

## Creare un’offerta remota utilizzando [!UICONTROL Form-Based Experience Composer]

1. Durante la creazione di un’attività tramite [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md), selezionare la posizione in cui visualizzare **[!UICONTROL Content]** sezione.

   ![Sezione Contenuto nel Compositore esperienza basato su moduli](/help/main/c-experiences/c-manage-content/assets/form-based-content.png)

1. Fai clic su **[!UICONTROL Default Content]** , quindi fai clic su **[!UICONTROL Change Remote Offer]**.

   ![Opzione Cambia offerta remota](/help/main/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Clic **[!UICONTROL Create]** > **[!UICONTROL Remote Offer]**.

   ![Finestra di dialogo Crea offerta remota](/help/main/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Inserisci un nome descrittivo per l’offerta.

   Un nome descrittivo consente a te e agli altri utenti di trovare rapidamente l’offerta nel [!UICONTROL Assets] libreria.

1. Specifica il tipo di URL di reindirizzamento.

   Consulta [Tipo di URL di reindirizzamento: memorizzato in cache o dinamico](#url-type) per ulteriori informazioni.

1. Specifica l’URL remoto per l’offerta remota.

1. Clic **[!UICONTROL Save]**.

## Tipo di URL di reindirizzamento: memorizzato in cache o dinamico {#url-type}

Le seguenti informazioni sono utili per comprendere le differenze tra le due opzioni:

### URL nella cache

Il contenuto di un’offerta remota memorizzata nella cache viene distribuito da [!DNL Target].

Ogni due ore, [!DNL Target] recupera il contenuto dall’URL remoto e quindi lo memorizza in [!DNL Target]. Quando i visitatori caricano un sito con un’esperienza che include un’offerta remota, [!DNL Target] consegna l’offerta.

Le offerte remote memorizzate nella cache forniscono maggiore sicurezza perché qualcuno ha effettuato l’accesso a [!DNL Target] non può modificare il contenuto. Per modificare il contenuto, è necessario registrare o un altro sistema e modificare il contenuto da tale posizione.

L’URL di un’offerta remota memorizzata nella cache può essere assoluto o relativo.

### URL dinamico

Un’offerta remota dinamica viene trasmessa dal sistema di gestione dei contenuti o da un altro sistema anziché da [!DNL Target].

Potresti non volere che il contenuto venga periodicamente memorizzato nella cache e quindi consegnato da [!DNL Target] ogni volta che un visitatore carica un sito con un’esperienza che include un’offerta remota. Piuttosto, desideri chiamare il sistema che ospita il contenuto e possibilmente passare informazioni specifiche in modo che l’offerta restituita possa essere dinamica (o diversa) per ogni utente. Ad esempio, se un utente accede al sito web della sua carta di credito e il sito include un’esperienza con un’offerta remota dinamica, puoi passare nell’URL parametri specifici per informazioni sul conto dell’utente. Quindi il sito web potrebbe fornire informazioni specifiche per questo utente, ad esempio il saldo del conto.

Puoi fare clic su **[!UICONTROL Add Parameter]** per aggiungere uno o più [!DNL Target] richieste o parametri di richiesta.

## Utilizzare le offerte remote nelle attività

È necessario applicare le offerte remote utilizzando [!UICONTROL Form-Based Experience Composer]. Al momento non è possibile applicare offerte remote utilizzando [!UICONTROL Visual Experience Composer] (VEC).

Il [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] è un’interfaccia non visiva per la creazione di esperienze e offerte, utile per creare le esperienze da utilizzare in [!UICONTROL A/B Tests], [!UICONTROL Experience Targeting] XT [!UICONTROL Automated Personalization] (AP), e [!UICONTROL Recommendations] attività quando [!UICONTROL Visual Experience Composer] non è disponibile o pratica per l’uso. Ad esempio, puoi utilizzare il [!UICONTROL Form-Based Experience Composer] per creare esperienze che utilizzano offerte remote.

1. Creare o modificare un’attività in [!UICONTROL Form-Based Experience Composer].

   Consulta [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md) per istruzioni dettagliate.

1. Specifica la posizione desiderata e aggiungi eventuali perfezionamenti del pubblico secondo necessità.

1. Fai clic sull’elenco a discesa nella sezione **[!UICONTROL Content]** , quindi fai clic su **[!UICONTROL Change Remote Offer]**.

   ![Opzione Cambia offerta remota](/help/main/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Seleziona l’offerta remota desiderata da [!UICONTROL Select Remote Offer] , quindi fare clic su **[!UICONTROL Done]**.

1. Termina la configurazione dell’attività.

## Funzionamento delle offerte remote dinamiche {#concept_CC2A969420B34364A9FA78C1CE251818}

Nelle offerte remote dinamiche, i valori necessari vengono passati all’offerta tramite la tecnologia per pagina dinamica.

L’offerta viene eseguita dopo aver effettuato il rendering della pagina. Un iFrame invisibile raccoglie i dati, li copia dal frame e li inserisce nella pagina, caricando i valori passati.

![immagine remote_offer_howitworks_2](assets/remote_offer_howitworks_2.jpeg)

1. Il browser del visitatore richiede una pagina dal server.

2. Il browser esegue il rendering della pagina, comprese le mbox.

3. `mboxCreate` La chiamata include i parametri necessari per eseguire il rendering del contenuto dinamico.

4. [!DNL Target] restituisce l’URL con la posizione del contenuto dinamico e i relativi parametri. Imposta un iFrame nell&#39;area mbox.

5. Il browser richiede l’URL ed esegue il rendering nella pagina.

## Matrice per la selezione dell’offerta remota {#reference_B23BEDD29DDD47709A7651AFD27E776B}

La Matrice per la selezione delle offerte remote consente di decidere quale tipo di offerta remota scegliere: [!UICONTROL Cached] o [!UICONTROL Dynamic].

| Funzione | Memorizzato in cache | Dinamico |
|--- |--- |--- |
| Aggiornamenti ogni volta che un visitatore effettua una richiesta | No | Sì |
| Aggiornamenti di contenuto | Memorizzazione nella cache ogni due ore | Aggiornamento immediato ad ogni richiesta |
| Tempo di caricamento | Più veloce | Più lento a causa della richiesta di elaborazione |
| Può vedere JavaScript a pagina | Sì | No, ma può passare tramite URL |
| Le offerte possono includere JavaScript | Sì | Sì |
| URL di offerta | Assoluto o relativo | Relativo |
| Richiesta computer | Server Adobe | Il computer del visitatore, che trasporta i suoi cookies |

## Video di formazione: Compositore basato su moduli ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video offre una demo del [!UICONTROL Form-Based Experience Composer], che puoi utilizzare per creare offerte remote.

* Creare un’attività tramite [!UICONTROL Form-Based Experience Composer]
* Scopri quando utilizzare [!UICONTROL Form-Based Experience Composer] rispetto al [!UICONTROL Visual Experience Composer]
* Indirizzare una posizione con i perfezionamenti

>[!VIDEO](https://video.tv.adobe.com/v/17390)