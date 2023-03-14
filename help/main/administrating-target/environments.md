---
keywords: ambiente;risoluzione dei problemi;best practice;ubox;reindirizzamenti;reindirizzamento;whitelist;blacklist;inserisco nell'elenco Bloccati di;inserisco nell'elenco Consentiti di
description: Scopri come utilizzare gli ambienti in Adobe [!DNL Target] per organizzare siti e ambienti di preproduzione al fine di semplificarne la gestione e la creazione di rapporti separati.
title: Cosa sono gli ambienti e come li utilizzo?
feature: Administration & Configuration
role: Admin
exl-id: 820a116a-15f9-4ba0-94f3-8e35aa0f90da
source-git-commit: a2f237ba2c79528b4d18e4100f4481e4af11d26c
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 58%

---

# Ambienti

Organizza siti e ambienti di preproduzione per gestirli facilmente e per generare rapporti separati.

Per facilitare la gestione, gli host sono raccolti in ambienti. Ad esempio, si potrebbero avere decine di host raggruppati in due o tre ambienti. Gli ambienti preimpostati includono [!UICONTROL Produzione], [!UICONTROL Staging], e [!UICONTROL Sviluppo]. È anche possibile aggiungere nuovi ambienti e rinominare gli ambienti.

Un ambiente, quello predefinito, è pre-denominato [!UICONTROL Produzione]. Questo ambiente predefinito non può essere eliminato, anche se lo si rinomina. [!DNL Target] presuppone che è qui che verranno eseguiti attività e test finali e approvati.

Quando un [!DNL Target] viene ricevuta una richiesta da nuovi siti web o domini, questi nuovi domini vengono sempre visualizzati nel [!UICONTROL Produzione] ambiente. Il [!UICONTROL Produzione] Poiché le impostazioni dell’ambiente non possono essere modificate, i siti sconosciuti o nuovi visualizzano solo il contenuto attivo e pronto. La gestione degli host consente inoltre di garantire facilmente la qualità di nuove attività e contenuti nei test, nella gestione temporanea (staging) e negli ambienti di sviluppo prima di attivare le attività.

Per gestire gli ambienti, fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Ambienti]**.

![Elenco ambienti](/help/main/administrating-target/assets/environments.png)

## Aggiungere un ambiente {#section_32097D0993724DF3A202D164D3F18674}

1. Dalla sezione [!UICONTROL Ambienti] , fare clic su **[!UICONTROL Aggiungi ambiente]**.
1. Specifica un nome descrittivo per l’ambiente.
1. Specifica la modalità attiva desiderata per l’ambiente: [!UICONTROL Attività attive] o [!UICONTROL Attività attive e inattive].

   Se si specifica [!UICONTROL Attività attive e inattive], gli host di questo ambiente visualizzano anche le attività inattive.

1. Fai clic su **[!UICONTROL Salva]**.

## Impostare l’ambiente predefinito per il reporting {#section_4F8539B07C0C45E886E8525C344D5FB0}

È possibile selezionare l’ambiente che si desidera utilizzare come impostazione predefinita per tutti i rapporti di attività.

Se usa [!UICONTROL Produzione] come impostazione predefinita, tutti gli host sconosciuti vengono aggiunti automaticamente qui e i dati del rapporto da lì sono inclusi nella vista del rapporto predefinita. Invece, la creazione di un ambiente “pulito” assicura che siano inclusi solo i siti e domini principali.

Per impostare l’ambiente predefinito per la segnalazione:

1. Dalla sezione [!UICONTROL Ambienti] fare clic sull&#39;icona Stella

>[!NOTE]
>
>Se gli host passano ad altri gruppi host, gli utenti che usano la funzionalità [!DNL Recommendations] devono rigenerare il database dei comportamenti e quello dei prodotti.

## Modificare il nome di un ambiente {#section_9F5F94285F8E495E9CE69810CE94CA08}

1. Dalla sezione [!UICONTROL Ambiente] , fare clic sul pulsante **[!UICONTROL Modifica]** icona.
1. Modifica il nome dell’ambiente.
1. Fai clic su **[!UICONTROL Salva]**.

## Eliminare un ambiente {#section_737F8869612047868D03FC755B1223D3}

Quando un ambiente non è più necessario, è possibile eliminarlo.

1. Dalla sezione [!UICONTROL Ambiente] , fare clic sul pulsante **[!UICONTROL Elimina]** icona.
1. Fai clic su **[!UICONTROL Elimina]** per confermare l’eliminazione.

>[!NOTE]
>
>Impossibile eliminare [!UICONTROL Produzione] ma è possibile rinominarlo.

## [!BADGE Premium]{type=Positive url="/help/main/c-intro/intro.md#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."}

Puoi visualizzare in anteprima il contenuto delle raccolte ed esclusioni di Consigli per un ambiente selezionato (gruppo di host).

{{premium-note}}

È possibile utilizzare un ambiente per separare gli elementi disponibili nel catalogo per usi diversi. Ad esempio, puoi utilizzare i gruppi di host per [!UICONTROL Sviluppo] e [!UICONTROL Produzione] ambienti, marchi o aree geografiche diverse. Per impostazione predefinita, i risultati dell&#39;anteprima in Ricerca nel catalogo, Raccolte ed Esclusioni si basano sul gruppo di host predefinito. Puoi anche selezionare un gruppo di host diverso per visualizzare in anteprima i risultati, utilizzando il filtro Ambiente. Per impostazione predefinita, gli elementi appena aggiunti sono disponibili in tutti i gruppi di host, a meno che non sia specificato un ID ambiente al momento della creazione o dell&#39;aggiornamento dell&#39;elemento.

>[!NOTE]
>
>I consigli distribuiti dipendono dal gruppo di host o dall’ID ambiente specificato nella richiesta.


Se i prodotti non vengono visualizzati, assicurati di utilizzare il gruppo host corretto. Ad esempio, se imposti che il consiglio usi un ambiente di gestione temporanea e imposti il gruppo host su Gestione temporanea, potrebbe essere necessario ricreare le raccolte nell&#39;ambiente di gestione temporanea perché si visualizzino i prodotti. Per visualizzare i prodotti disponibili in ogni ambiente, utilizza Ricerca catalogo con ogni ambiente. Puoi anche visualizzare in anteprima il contenuto delle raccolte ed esclusioni di Recommendations per un ambiente selezionato (gruppo di host).

>[!NOTE]
>Dopo aver modificato l’ambiente selezionato, fai clic su Cerca per aggiornare i risultati restituiti.

Il [!UICONTROL Ambiente] Il filtro è disponibile nelle seguenti posizioni nell’interfaccia utente di Target:

* Ricerca nel catalogo ([!UICONTROL Recommendations > Ricerca nel catalogo])
* Finestra di dialogo Crea raccolta ([!UICONTROL Recommendations > Raccolte > Crea nuova])
* Finestra di dialogo Aggiorna raccolta ([!UICONTROL Recommendations > Raccolte > Modifica])
* Finestra di dialogo Crea esclusione ([!UICONTROL Recommendations > Esclusioni > Crea nuova])
* Finestra di dialogo Aggiorna esclusione ([!UICONTROL Recommendations > Esclusioni > Modifica])
