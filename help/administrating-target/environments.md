---
keywords: environment;troubleshooting;best practices;ubox;redirects;redirect;whitelist;blacklist;blocklist;allowlist
description: Organizzate i siti e gli ambienti di pre-produzione per semplificare la gestione e la creazione di report separati in  Adobe Target.
title: Ambienti
feature: hosts and environments
translation-type: tm+mt
source-git-commit: c2769c0fcf7a05c10405ec855468c829aca785c0
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 65%

---


# Ambienti

Organizza siti e ambienti di preproduzione per gestirli facilmente e per generare rapporti separati.

Per facilitare la gestione, gli host sono raccolti in ambienti. Ad esempio, si potrebbero avere decine di host raggruppati in due o tre ambienti. Gli ambienti preimpostati includono [!UICONTROL Produzione], [!UICONTROL Staging] e [!UICONTROL Sviluppo]. È anche possibile aggiungere nuovi ambienti e rinominare gli ambienti.

Un ambiente, l&#39;ambiente predefinito, è denominato in precedenza [!UICONTROL Produzione]. Questo ambiente predefinito non può essere eliminato, anche se lo si rinomina. [!DNL Target] presuppone che è qui che verranno eseguiti attività e test finali e approvati.

Quando una richiesta [!DNL Target] viene ricevuta da nuovi siti Web o domini, questi nuovi domini vengono sempre visualizzati nell&#39;ambiente [!UICONTROL Produzione]. Poiché l&#39;ambiente [!UICONTROL Production] non può avere impostazioni modificate, è necessario che i siti sconosciuti o nuovi visualizzino solo il contenuto attivo e pronto. La gestione degli host consente inoltre di garantire facilmente la qualità di nuove attività e contenuti nei test, nella gestione temporanea (staging) e negli ambienti di sviluppo prima di attivare le attività.

Per gestire gli ambienti, fare clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Ambienti]**.

![Elenco Ambienti](/help/administrating-target/assets/environments.png)

## Aggiungere un ambiente {#section_32097D0993724DF3A202D164D3F18674}

1. Nell&#39;elenco [!UICONTROL Ambienti] fare clic su **[!UICONTROL Aggiungi ambiente]**.
1. Specifica un nome descrittivo per l’ambiente.
1. Specifica la modalità attiva desiderata per l’ambiente: [!UICONTROL Attività attive] o [!UICONTROL Attività attive e inattive].
1. Fai clic su **[!UICONTROL Salva]**.

## Impostare l&#39;ambiente predefinito per il reporting {#section_4F8539B07C0C45E886E8525C344D5FB0}

È possibile selezionare l’ambiente che si desidera utilizzare come impostazione predefinita per tutti i rapporti di attività.

Se utilizzi [!UICONTROL Production] come impostazione predefinita, tutti gli host sconosciuti vengono automaticamente aggiunti qui e i dati del report da tale posizione vengono inclusi nella visualizzazione rapporto predefinita. Invece, la creazione di un ambiente “pulito” assicura che siano inclusi solo i siti e domini principali.

Per impostare l’ambiente predefinito per la segnalazione:

1. Nell&#39;elenco [!UICONTROL Ambienti], fare clic sull&#39;icona Star

>[!NOTE]
>
>Se gli host passano ad altri gruppi host, gli utenti che usano la funzionalità [!DNL Recommendations] devono rigenerare il database dei comportamenti e quello dei prodotti.

## Modificare il nome di un ambiente {#section_9F5F94285F8E495E9CE69810CE94CA08}

1. Nell&#39;elenco [!UICONTROL Ambiente] fare clic sull&#39;icona **[!UICONTROL Modifica]**.
1. Modifica il nome dell’ambiente.
1. Fai clic su **[!UICONTROL Salva]**.

## Eliminare un ambiente {#section_737F8869612047868D03FC755B1223D3}

Quando un ambiente non è più necessario, è possibile eliminarlo.

1. Nell&#39;elenco [!UICONTROL Ambiente] fare clic sull&#39;icona **[!UICONTROL Elimina]**.
1. Fai clic su **[!UICONTROL Elimina]** per confermare l’eliminazione.

>[!NOTE]
>
>Non è possibile eliminare l&#39;ambiente [!UICONTROL Produzione], ma è possibile rinominarlo.

## Recommendations: filtrare raccolte ed esclusioni per ambiente (gruppo di host)

![Badge Premium](/help/assets/premium.png)

Puoi visualizzare in anteprima il contenuto delle raccolte ed esclusioni di Consigli per un ambiente selezionato (gruppo di host).

>[!NOTE]
>
>Le attività Recommendations sono disponibili come parte della soluzione [!DNL Target] Premium. Non sono disponibili in [!DNL Target] Standard senza una licenza [!DNL Target] Premium.

Un ambiente può essere utilizzato per separare gli elementi disponibili nel catalogo per usi diversi. Ad esempio, potete utilizzare i gruppi di host per gli ambienti [!UICONTROL Sviluppo] e [!UICONTROL Produzione], diversi marchi o diverse aree geografiche. Per impostazione predefinita, i risultati dell&#39;anteprima in Ricerca nel catalogo, Raccolte ed Esclusioni si basano sul gruppo di host predefinito. Puoi anche selezionare un gruppo di host diverso per visualizzare in anteprima i risultati, utilizzando il filtro Ambiente. Per impostazione predefinita, gli elementi appena aggiunti sono disponibili in tutti i gruppi di host, a meno che non sia specificato un ID ambiente al momento della creazione o dell&#39;aggiornamento dell&#39;elemento. I consigli distribuiti dipendono dal gruppo di host specificato nella richiesta.

Se i prodotti non vengono visualizzati, assicurati di utilizzare il gruppo host corretto. Ad esempio, se imposti che il consiglio usi un ambiente di gestione temporanea e imposti il gruppo host su Gestione temporanea, potrebbe essere necessario ricreare le raccolte nell&#39;ambiente di gestione temporanea perché si visualizzino i prodotti. Per visualizzare i prodotti disponibili in ogni ambiente, utilizza Ricerca catalogo con ogni ambiente. Puoi anche visualizzare in anteprima il contenuto delle raccolte ed esclusioni di Recommendations per un ambiente selezionato (gruppo di host).

>[!NOTE]
>Dopo aver modificato l’ambiente selezionato, fai clic su Cerca per aggiornare i risultati restituiti.

Il filtro [!UICONTROL Ambiente] è disponibile nelle seguenti aree dell&#39;interfaccia utente di Target:

* Ricerca nel catalogo ([!UICONTROL Recommendations > Ricerca nel catalogo])
* Finestra di dialogo Crea raccolta ([!UICONTROL Recommendations > Raccolte > Crea nuova])
* Finestra di dialogo Aggiorna raccolta ([!UICONTROL Recommendations > Raccolte > Modifica])
* Finestra di dialogo Crea esclusione ([!UICONTROL Recommendations > Esclusioni > Crea nuova])
* Finestra di dialogo Aggiorna esclusione ([!UICONTROL Recommendations > Esclusioni > Modifica])