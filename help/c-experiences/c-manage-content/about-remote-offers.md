---
keywords: offerta remota;matrice di selezione offerta remota;contenuto in cache;contenuto dinamico;tipo di url
description: Scopri come utilizzare le offerte remote in Adobe [!DNL Target] per ospitare contenuti esterni (contenuti in un CMS o in un altro sistema). Scopri perché utilizzare le offerte remote.
title: Come Si Creano Offerte Remote?
feature: Esperienze e offerte
exl-id: 6a5283ee-c1fb-49f7-8e7f-c23ccde26ade
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 49%

---

# Creare offerte remote

Utilizza le offerte remote per l’hosting di contenuti esterni a [!DNL Adobe Target] a cui [!DNL Target] può fare riferimento per consegnarli ai siti web degli utenti. Questo contenuto potrebbe trovarsi in un sistema di gestione dei contenuti (CMS) o in un altro sistema, per motivi di facilità d’uso o di sicurezza.

>[!NOTE]
>
>Le offerte remote possono essere create sulla pagina [!UICONTROL Offerte] > [!UICONTROL Offerte di codice] o nel [Compositore esperienza basato su Forms](/help/c-experiences/form-experience-composer.md). Non puoi creare o applicare offerte remote nel Compositore esperienza visivo. Il contenuto verrà inserito nelle posizioni di richiesta [!DNL Target], pertanto è molto probabile che queste non siano appropriate per una richiesta globale [!DNL Target].
>
>[!DNL Target Classic] includeva funzioni simili: [!UICONTROL Offerta sul tuo sito] e [!UICONTROL Offerta esterna a Test&amp;Target].

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

* Se l&#39;offerta risiede nello stesso dominio delle richieste [!DNL Target], l&#39;opzione [!UICONTROL Cache] consente di utilizzare URL relativi per descrivere la posizione dell&#39;offerta.

   Ciò significa che quando sposti l’attività dai server di gestione temporanea alla produzione, il contenuto sarà automaticamente accessibile senza dover modificare manualmente l’URL.

* Se il test include dati generati dinamicamente dal server, l’opzione [!UICONTROL Dinamico] potrebbe essere la scelta giusta.
* Se si prevede di testare solo l’aspetto del contenuto dell’offerta remota esistente, utilizza il [!UICONTROL Compositore esperienza visivo] per modificare l’aspetto del contenuto restituito dal sistema di gestione dei contenuti.
* Utilizza la [Matrice per la selezione dell&#39;offerta remota](#reference_B23BEDD29DDD47709A7651AFD27E776B) (sotto) per aiutarti a scegliere l&#39;offerta più adatta al tuo caso specifico. Se hai domande, rivolgiti al rappresentante del tuo account.

## Creare un’offerta remota dalla pagina Offerte di codice

1. Fai clic su **[!UICONTROL Offerte]**, quindi seleziona la scheda **[!UICONTROL Offerte di codice]**.

   ![Offerte > Offerte di codice](/help/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. Fai clic su **[!UICONTROL Crea]** > **[!UICONTROL Offerta remota]**.

   ![Finestra di dialogo Crea offerta remota](/help/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Inserisci un nome descrittivo per l’offerta.

   Un nome descrittivo è utile per ritrovare rapidamente l’offerta nella libreria [!UICONTROL Risorse].

1. Specifica il tipo di URL di reindirizzamento.

   Consulta [Tipo URL di reindirizzamento: Cache o Dynamic](#url-type) per ulteriori informazioni.

1. Specifica l’URL remoto per l’offerta remota.

1. Fai clic su **[!UICONTROL Salva]**.

## Creare un’offerta remota utilizzando il Compositore esperienza basato su moduli

1. Durante la creazione di un&#39;attività utilizzando il [Compositore esperienza basato su moduli](/help/c-experiences/form-experience-composer.md), seleziona la posizione in cui visualizzare la sezione **[!UICONTROL Contenuto]**.

   ![Sezione Contenuto nel Compositore esperienza basato su moduli](/help/c-experiences/c-manage-content/assets/form-based-content.png)

1. Fai clic sull&#39;elenco a discesa **[!UICONTROL Contenuto predefinito]** , quindi fai clic su **[!UICONTROL Cambia offerta remota]**.

   ![Opzione Cambia offerta remota](/help/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Fai clic su **[!UICONTROL Crea]** > **[!UICONTROL Offerta remota]**.

   ![Finestra di dialogo Crea offerta remota](/help/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Inserisci un nome descrittivo per l’offerta.

   Un nome descrittivo è utile per ritrovare rapidamente l’offerta nella libreria [!UICONTROL Risorse].

1. Specifica il tipo di URL di reindirizzamento.

   Consulta [Tipo URL di reindirizzamento: Cache o Dynamic](#url-type) per ulteriori informazioni.

1. Specifica l’URL remoto per l’offerta remota.

1. Fai clic su **[!UICONTROL Salva]**.

## Tipo URL di reindirizzamento: Memorizzato in cache o dinamico {#url-type}

Le informazioni seguenti sono utili per comprendere le differenze tra le due opzioni:

### URL memorizzato nella cache

Il contenuto di un’offerta remota con URL memorizzato nella cache viene trasmesso da [!DNL Target].

Ogni due ore, [!DNL Target] recupera il contenuto dall’URL remoto e quindi lo archivia in [!DNL Target]. Quando i visitatori caricano un sito con un’esperienza che include un’offerta remota, l’offerta viene consegnata da [!DNL Target].

Le offerte remote memorizzate nella cache forniscono un livello di protezione maggiore, perché non è possibile modificare il contenuto mediante l’accesso a [!DNL Target]. Per modificare il contenuto, è necessario accedere al sistema di gestione dei contenuti o a un altro sistema e modificare il contenuto da tale ambiente.

L’URL di un’offerta remota memorizzata nella cache può essere assoluto o relativo.

### URL dinamico

Un’offerta remota con URL dinamico viene trasmessa dal sistema di gestione dei contenuti o da un altro sistema anziché da [!DNL Target].

Potresti non volere che il contenuto venga periodicamente memorizzato nella cache e quindi consegnato da [!DNL Target] ogni volta che un visitatore carica un sito contenente un’esperienza con un’offerta remota. Al contrario, desideri chiamare il sistema che ospita il contenuto, possibilmente trasmetterle informazioni specifiche in modo che l’offerta restituita possa essere dinamica (o diversa) per ogni utente. Ad esempio, se un utente accede al sito web della sua carta di credito e il sito include un’esperienza con un’offerta remota dinamica, puoi passare nell’URL parametri specifici per informazioni sul conto dell’utente. Quindi il sito web potrebbe fornire informazioni specifiche per questo utente, ad esempio il saldo del conto.

Puoi fare clic su **[!UICONTROL Aggiungi parametro]** per aggiungere una o più richieste o parametri di richiesta [!DNL Target].

## Utilizzare le offerte remote nelle attività

È necessario applicare le offerte remote utilizzando il [!UICONTROL Compositore esperienza basato su moduli]. Al momento non è possibile applicare offerte remote utilizzando il Compositore esperienza visivo.

Il [!DNL Adobe Target] [!UICONTROL Compositore esperienza basato su moduli] è un&#39;interfaccia per la creazione di esperienze non visive ed offerte, utile per creare esperienze da utilizzare in [!UICONTROL Test A/B], [!UICONTROL Targeting esperienza] (XT), [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Recommendations attività a10/> quando il compositore esperienza visivo non è disponibile o se non è pratico per l’uso. ] Ad esempio, puoi utilizzare il [!UICONTROL Compositore esperienza basato su moduli] per creare esperienze che utilizzano offerte remote.

1. Crea o modifica un&#39;attività nel [!UICONTROL Compositore esperienza basato su moduli].

   Per istruzioni dettagliate, consulta [Compositore esperienza basato su moduli](/help/c-experiences/form-experience-composer.md) .

1. Specifica la posizione desiderata e aggiungi eventuali perfezionamenti al pubblico, a seconda delle necessità.

1. Fai clic sull&#39;elenco a discesa nella sezione **[!UICONTROL Contenuto]** , quindi fai clic su **[!UICONTROL Cambia offerta remota]**.

   ![Opzione Cambia offerta remota](/help/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Seleziona l’offerta remota desiderata dalla finestra di dialogo [!UICONTROL Seleziona offerta remota], quindi fai clic su **[!UICONTROL Fine]**.

1. Termina la configurazione dell’attività.

## Funzionamento delle offerte remote dinamiche {#concept_CC2A969420B34364A9FA78C1CE251818}

Nelle offerte remote dinamiche, i valori necessari vengono passati all’offerta tramite la tecnologia per pagina dinamica.

L’offerta viene eseguita dopo aver effettuato il rendering della pagina. Un iframe invisibile raccoglie i dati, li copia fuori dal frame e li inserisce nella pagina, caricando i valori passati.

![](assets/remote_offer_howitworks_2.jpeg)

## Matrice di selezione delle offerte remote {#reference_B23BEDD29DDD47709A7651AFD27E776B}

La matrice per la selezione dell’offerta remota è utile per decidere quale tipo di offerta remota scegliere: con URL remoto [!UICONTROL Memorizzato in cache] o [!UICONTROL Dinamico].

| Funzione | Memorizzato in cache | Dinamico |
|--- |--- |--- |
| Aggiornamenti ogni volta che un visitatore effettua una richiesta | No | Sì |
| Aggiornamenti di contenuto | Salvato nella cache ogni 2 ore | Aggiornamento immediato ad ogni richiesta |
| Tempo di caricamento | Più veloce | Più lento a causa della richiesta di elaborazione |
| Può vedere JavaScript a pagina | Sì | No, ma può passare tramite URL |
| Le offerte possono includere JavaScript | Sì | Sì |
| URL di offerta | Assoluto o relativo | Relativo |
| Richiesta computer | Server Adobe | Il computer del visitatore, che trasporta i suoi cookies |

## Video di formazione: Compositore basato su moduli ![Badge tutorial](/help/assets/tutorial.png)

Questo video fornisce una demo del compositore basato su moduli, che può essere utilizzato per creare offerte remote.

* Creare un’attività utilizzando il Compositore esperienza basato su moduli
* Quando utilizzare il Compositore esperienza basato su moduli o il Compositore esperienza visivo
* Indirizzare una posizione con i perfezionamenti

>[!VIDEO](https://video.tv.adobe.com/v/17390)
