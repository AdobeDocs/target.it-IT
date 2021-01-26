---
keywords: remote offer;remote offer selection matrix;cached content;dynamic content;url type
description: Posso utilizzare le offerte remote per ospitare contenuti esterni?
title: Creare offerte remote
feature: Experiences and Offers
translation-type: tm+mt
source-git-commit: f99d8a106fb0cfc88ad1beb1e5ada03550423999
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 59%

---


# Creare offerte remote

Utilizza le offerte remote per l’hosting di contenuti esterni a [!DNL Adobe Target] a cui [!DNL Target] può fare riferimento per consegnarli ai siti web degli utenti. Questo contenuto potrebbe essere in un sistema di gestione dei contenuti (CMS) o in un altro sistema, sia per semplicità di utilizzo che per motivi di sicurezza.

>[!NOTE]
>
>Le offerte remote possono essere create nella pagina Offerte > Offerte codice o in [Forms-Based Experience Composer](/help/c-experiences/form-experience-composer.md). Non potete creare offerte remote in Visual Experience Composer (VEC). Il contenuto verrà inserito nelle posizioni di richiesta [!DNL Target], pertanto è molto probabile che non siano adatte a una richiesta globale [!DNL Target].
>
>[!DNL Target Classic] includeva funzioni simili: [!UICONTROL Offerta sul tuo sito] e [!UICONTROL Offerta esterna a Test&amp;Target].

Alcuni esempi di offerte remote includono:

* Diverse versioni di cross-selling
* Messaggi dinamici per il carrello acquisti
* Moduli
* Calcolatori
* Aggiornamenti del tasso di interesse

## Creare un&#39;offerta remota dalla pagina Code Offers (Offerte codice)

1. Fai clic su **[!UICONTROL Offerte]**, quindi seleziona la scheda **[!UICONTROL Offerte di codice]**.

   ![Offerte > Offerte codice](/help/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. Fai clic su **[!UICONTROL Crea]** > **[!UICONTROL Offerta remota]**.

   ![Crea offerta remota, finestra di dialogo](/help/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Inserisci un nome descrittivo per l’offerta.

   Un nome descrittivo è utile per ritrovare rapidamente l’offerta nella libreria [!UICONTROL Risorse].

1. Specificate il tipo di URL di reindirizzamento.

   Vedere [Tipo URL di reindirizzamento: Cache o Dynamic](#url-type) per ulteriori informazioni.

1. Specifica l’URL remoto per l’offerta remota.

1. Fai clic su **[!UICONTROL Salva]**.

## Creazione di un&#39;offerta remota tramite Form-Based Experience Composer (Compositore esperienza basato su modulo)

1. Durante la creazione di un&#39;attività con [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md), selezionate il percorso in cui visualizzare la sezione **[!UICONTROL Content]**.

   ![Sezione Contenuto in Experience Composer basato su modulo](/help/c-experiences/c-manage-content/assets/form-based-content.png)

1. Fare clic sull&#39;elenco a discesa **[!UICONTROL Contenuto predefinito]**, quindi fare clic su **[!UICONTROL Modifica offerta remota]**.

   ![Cambia offerta remota, opzione](/help/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Fai clic su **[!UICONTROL Crea]** > **[!UICONTROL Offerta remota]**.

   ![Crea offerta remota, finestra di dialogo](/help/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Inserisci un nome descrittivo per l’offerta.

   Un nome descrittivo è utile per ritrovare rapidamente l’offerta nella libreria [!UICONTROL Risorse].

1. Specificate il tipo di URL di reindirizzamento.

   Vedere [Tipo URL di reindirizzamento: Cache o Dynamic](#url-type) per ulteriori informazioni.

1. Specifica l’URL remoto per l’offerta remota.

1. Fai clic su **[!UICONTROL Salva]**.

## Tipo URL di reindirizzamento: Cache o Dinamica {#url-type}

Le seguenti informazioni sono utili per comprendere le differenze tra le due opzioni:

### URL memorizzato nella cache

Il contenuto di un’offerta remota con URL memorizzato nella cache viene trasmesso da [!DNL Target].

Ogni due ore, [!DNL Target] recupera il contenuto dall’URL remoto e quindi lo archivia in [!DNL Target]. Quando i visitatori caricano un sito con un’esperienza che include un’offerta remota, l’offerta viene consegnata da [!DNL Target].

Le offerte remote memorizzate nella cache offrono una protezione avanzata perché un utente che ha eseguito l&#39;accesso a [!DNL Target] non può modificare il contenuto. Per modificare il contenuto, è necessario accedere al sistema di gestione dei contenuti o a un altro sistema e modificare il contenuto da tale ambiente.

L’URL di un’offerta remota memorizzata nella cache può essere assoluto o relativo.

### URL dinamico

Un’offerta remota con URL dinamico viene trasmessa dal sistema di gestione dei contenuti o da un altro sistema anziché da [!DNL Target].

Potresti non volere che il contenuto venga periodicamente memorizzato nella cache e quindi consegnato da [!DNL Target] ogni volta che un visitatore carica un sito contenente un’esperienza con un’offerta remota. Al contrario, desiderate chiamare il sistema che ospita il contenuto, eventualmente trasmettere informazioni specifiche in modo che l&#39;offerta restituita possa essere dinamica (o diversa) per ogni utente. Ad esempio, se un utente accede al sito web della sua carta di credito e il sito include un’esperienza con un’offerta remota dinamica, puoi passare nell’URL parametri specifici per informazioni sul conto dell’utente. Quindi il sito web potrebbe fornire informazioni specifiche per questo utente, ad esempio il saldo del conto.

Potete fare clic su **[!UICONTROL Aggiungi parametro]** per aggiungere uno o più [!DNL Target] parametri di richieste o richieste.

## Procedure ottimali per l&#39;utilizzo delle offerte remote {#section_7718512D08E14121B6F6B8C38134F4BC}

Best practice per l’utilizzo delle offerte remote nelle attività:

* Se l&#39;offerta risiede nello stesso dominio delle [!DNL Target] richieste, l&#39;opzione [!UICONTROL Cache] consente di utilizzare URL relativi per descrivere la posizione dell&#39;offerta.

   Ciò significa che quando sposti l’attività dai server di gestione temporanea alla produzione, il contenuto sarà automaticamente accessibile senza dover modificare manualmente l’URL.

* Se il test include dati generati dinamicamente dal server, l’opzione [!UICONTROL Dinamico] potrebbe essere la scelta giusta.
* Se si prevede di testare solo l’aspetto del contenuto dell’offerta remota esistente, utilizza il [!UICONTROL Compositore esperienza visivo] per modificare l’aspetto del contenuto restituito dal sistema di gestione dei contenuti.
* Utilizzate la matrice di selezione dell&#39;offerta remota (sotto) per scegliere l&#39;offerta più adatta per il caso specifico. Se hai domande, rivolgiti al rappresentante del tuo account.

## Funzionamento delle offerte remote dinamiche {#concept_CC2A969420B34364A9FA78C1CE251818}

Nelle offerte remote dinamiche, i valori necessari vengono passati all’offerta tramite la tecnologia per pagina dinamica.

L’offerta viene eseguita dopo aver effettuato il rendering della pagina. Un iframe invisibile raccoglie i dati, li copia dalla cornice e li inserisce nella pagina, caricando i valori passati.

![](assets/remote_offer_howitworks_2.jpeg)

## Matrice di selezione delle offerte remota {#reference_B23BEDD29DDD47709A7651AFD27E776B}

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