---
keywords: remote offer;remote offer selection matrix;cached content;dynamic content
description: 'Con le offerte remote puoi utilizzare contenuti esterni: Target farà riferimento a tali contenuti e li consegnerà ai siti web degli utenti. I contenuti esterni possono trovarsi in un sistema di gestione dei contenuti o in un altro sistema, per motivi di facilità d’uso o di sicurezza.'
title: Creare offerte remote
topic: Standard
uuid: 5aaff281-e96c-41a6-849e-2c3b0e35f161
translation-type: tm+mt
source-git-commit: c7664f9674234565a3657f453541095811fa5aa6
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 92%

---


# Creare offerte remote{#create-remote-offers}

Con le offerte remote puoi utilizzare contenuti esterni: Target farà riferimento a tali contenuti e li consegnerà ai siti web degli utenti. I contenuti esterni possono trovarsi in un sistema di gestione dei contenuti o in un altro sistema, per motivi di facilità d’uso o di sicurezza.

>[!NOTE]
>
>Le offerte remote possono essere create solo nel compositore basato su moduli. Content will be injected in the [!DNL Target] request locations, so these are most likely not appropriate for a global [!DNL Target] request.
>
>[!DNL Target Classic] includeva funzioni simili: [!UICONTROL Offerta sul tuo sito] e [!UICONTROL Offerta esterna a Test&amp;Target].

Alcuni esempi di offerte remote includono:

* Diverse versioni di cross-selling
* Messaggi dinamici per il carrello acquisti
* Moduli
* Calcolatori
* Aggiornamenti del tasso di interesse

**Per creare un’offerta remota:**

1. Fai clic su **[!UICONTROL Offerte]**, quindi seleziona la scheda **[!UICONTROL Offerte di codice]**.
1. Fai clic su **[!UICONTROL Crea]** > **[!UICONTROL Offerta remota]**.

   ![](assets/remote_offer_ui.png)

1. Inserisci un nome descrittivo per l’offerta.

   Un nome descrittivo è utile per ritrovare rapidamente l’offerta nella libreria [!UICONTROL Risorse].

1. Specifica l’URL remoto per l’offerta remota:

   | Opzione | Descrizione |
   |--- |--- |
   | Memorizzato in cache | Il contenuto di un’offerta remota con URL memorizzato nella cache viene trasmesso da Target.<br>Ogni due ore, [!DNL Target] recupera il contenuto dall’URL remoto e quindi lo archivia in Target. Quando i visitatori caricano un sito con un’esperienza che include un’offerta remota, l’offerta viene consegnata da Target.<br>Le offerte remote memorizzate nella cache forniscono un livello di protezione maggiore, perché il loro contenuto non può essere modificato da qualcuno che abbia effettuato l’accesso a Target. Per modificare il contenuto, è necessario accedere al sistema di gestione dei contenuti o a un altro sistema e modificare il contenuto da tale ambiente.<br>L’URL di un’offerta remota memorizzata nella cache può essere assoluto o relativo. |
   | Dinamico | Un’offerta remota con URL dinamico viene trasmessa dal sistema di gestione dei contenuti o da un altro sistema anziché da Target.<br>Potresti non volere che il contenuto venga periodicamente memorizzato nella cache e quindi consegnato da Target ogni volta che un visitatore carica un sito contenente un’esperienza con un’offerta remota. Al contrario, potresti preferire che venga chiamato il sistema che ospita il contenuto e che vengano eventualmente passate a tale sistema informazioni specifiche, affinché l’offerta restituita sia dinamica o diversa per ogni utente.<br>Ad esempio, se un utente accede al sito web della sua carta di credito e il sito include un’esperienza con un’offerta remota dinamica, puoi passare nell’URL parametri specifici per informazioni sul conto dell’utente. Quindi il sito web potrebbe fornire informazioni specifiche per questo utente, ad esempio il saldo del conto.<br>Fate clic su [!UICONTROL Aggiungi parametro] per aggiungere una o più [!DNL Target] richieste o parametri di richiesta. |

1. Fai clic su **[!UICONTROL Salva]**.

## Best practice per l’utilizzo delle offerte remote {#section_7718512D08E14121B6F6B8C38134F4BC}

Best practice per l’utilizzo delle offerte remote nelle attività:

* If your offer resides in the same domain as the [!DNL Target] requests, using the [!UICONTROL Cached] option lets you use relative URLs in describing your offer location.

   Ciò significa che quando sposti l’attività dai server di gestione temporanea alla produzione, il contenuto sarà automaticamente accessibile senza dover modificare manualmente l’URL.

* Se il test include dati generati dinamicamente dal server, l’opzione [!UICONTROL Dinamico] potrebbe essere la scelta giusta.
* Se si prevede di testare solo l’aspetto del contenuto dell’offerta remota esistente, utilizza il [!UICONTROL Compositore esperienza visivo] per modificare l’aspetto del contenuto restituito dal sistema di gestione dei contenuti.
* Come ausilio nella scelta dell’offerta più adatta per il tuo caso specifico, usa la Matrice per la selezione dell’offerta remota. Se hai domande, rivolgiti al rappresentante del tuo account.

## Funzionamento delle offerte remote dinamiche {#concept_CC2A969420B34364A9FA78C1CE251818}

Nelle offerte remote dinamiche, i valori necessari vengono passati all’offerta tramite la tecnologia per pagina dinamica.

L’offerta viene eseguita dopo aver effettuato il rendering della pagina. Un iframe invisibile raccoglie i dati, li copia fuori dal frame e li inserisce nella pagina, caricando i valori passati.

![](assets/remote_offer_howitworks_2.jpeg)

## Matrice per la selezione dell’offerta remota {#reference_B23BEDD29DDD47709A7651AFD27E776B}

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