---
keywords: ambiente;risoluzione dei problemi;best practice;ubox;reindirizzamenti;reindirizzamento;whitelist;blacklist;inserisco nell'elenco Bloccati di;inserisco nell'elenco Consentiti di
description: Scopri come utilizzare gli ambienti in Adobe [!DNL Target] per organizzare i siti e gli ambienti di pre-produzione per semplificare la gestione e creare rapporti separati.
title: Cosa sono gli ambienti e come li utilizzo?
feature: Administration & Configuration
role: Admin
exl-id: 820a116a-15f9-4ba0-94f3-8e35aa0f90da
source-git-commit: 484971ab0fcd07205935c0fef3ea1484f40c3e96
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 46%

---

# Ambienti

Organizza siti e ambienti di preproduzione per gestirli facilmente e per generare rapporti separati.

Per facilitare la gestione, gli host sono raccolti in ambienti. Ad esempio, si potrebbero avere decine di host raggruppati in due o tre ambienti. Gli ambienti predefiniti includono [!UICONTROL Production], [!UICONTROL Staging] e [!UICONTROL Development]. È anche possibile aggiungere nuovi ambienti e rinominare gli ambienti.

Un ambiente, quello predefinito, è denominato [!UICONTROL Production]. Questo ambiente predefinito non può essere eliminato, anche se lo si rinomina. [!DNL Target] presuppone che è qui che verranno eseguiti attività e test finali e approvati.

Quando si riceve una richiesta [!DNL Target] da nuovi siti Web o domini, questi nuovi domini vengono sempre visualizzati nell&#39;ambiente [!UICONTROL Production]. Impossibile modificare le impostazioni dell&#39;ambiente [!UICONTROL Production]. Per i siti sconosciuti o nuovi viene garantita la visualizzazione solo del contenuto attivo e pronto. La gestione degli host consente inoltre di garantire facilmente la qualità di nuove attività e contenuti nei test, nella gestione temporanea (staging) e negli ambienti di sviluppo prima di attivare le attività.

Per gestire gli ambienti, fare clic su **[!UICONTROL Administration]** > **[!UICONTROL Environments]**.

## Aggiungere un ambiente {#section_32097D0993724DF3A202D164D3F18674}

1. Dall&#39;elenco [!UICONTROL Environments], fare clic su **[!UICONTROL Add Environment]**.
1. Specifica un nome descrittivo per l’ambiente.
1. Specificare la modalità attiva desiderata per l&#39;ambiente: [!UICONTROL Active Activities] o [!UICONTROL Active and Inactive Activities].

   Se si specifica [!UICONTROL Active and Inactive Activities], gli host di questo ambiente visualizzano anche le attività inattive.

1. Fare clic su **[!UICONTROL Save]**.

## Impostare l’ambiente predefinito per il reporting {#section_4F8539B07C0C45E886E8525C344D5FB0}

È possibile selezionare l’ambiente che si desidera utilizzare come impostazione predefinita per tutti i rapporti di attività.

Se utilizzi [!UICONTROL Production] come impostazione predefinita, tutti gli host sconosciuti vengono aggiunti automaticamente qui e i dati del rapporto da essi provenienti vengono inclusi nella visualizzazione del rapporto predefinita. Invece, la creazione di un ambiente “pulito” assicura che siano inclusi solo i siti e domini principali.

Per impostare l’ambiente predefinito per la segnalazione:

1. Nell&#39;elenco [!UICONTROL Environments] fare clic sull&#39;icona Stella

>[!NOTE]
>
>Se gli host passano ad altri gruppi host, gli utenti che usano la funzionalità [!DNL Recommendations] devono rigenerare il database dei comportamenti e quello dei prodotti.
>
>Se si specifica un [ambiente predefinito in un [!DNL Adobe Experience Platform] flusso di dati](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=en#target){target=_blank}, questa impostazione ha la precedenza su quella in [!DNL Target].

## Modificare il nome di un ambiente {#section_9F5F94285F8E495E9CE69810CE94CA08}

1. Nell&#39;elenco [!UICONTROL Environment] fare clic sull&#39;icona **[!UICONTROL Edit]**.
1. Modifica il nome dell’ambiente.
1. Fare clic su **[!UICONTROL Save]**.

## Eliminare un ambiente {#section_737F8869612047868D03FC755B1223D3}

Quando un ambiente non è più necessario, è possibile eliminarlo.

1. Nell&#39;elenco [!UICONTROL Environment] fare clic sull&#39;icona **[!UICONTROL Delete]**.
1. Fare clic su **[!UICONTROL Delete]** per confermare l&#39;eliminazione.

>[!NOTE]
>
>Non è possibile eliminare l&#39;ambiente [!UICONTROL Production], ma è possibile rinominarlo.

## [!BADGE Premium]{type=Positive url="/help/main/c-intro/intro.md#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."}

Puoi visualizzare in anteprima il contenuto delle raccolte ed esclusioni di Consigli per un ambiente selezionato (gruppo di host).

{{premium-note}}

È possibile utilizzare un ambiente per separare gli elementi disponibili nel catalogo per usi diversi. È ad esempio possibile utilizzare gruppi di host per ambienti [!UICONTROL Development] e [!UICONTROL Production], marchi diversi o aree geografiche diverse. Per impostazione predefinita, i risultati dell&#39;anteprima in Ricerca nel catalogo, Raccolte ed Esclusioni si basano sul gruppo di host predefinito. Puoi anche selezionare un gruppo di host diverso per visualizzare in anteprima i risultati, utilizzando il filtro Ambiente. Per impostazione predefinita, gli elementi appena aggiunti sono disponibili in tutti i gruppi di host, a meno che non venga specificato un ID ambiente al momento della creazione o dell’aggiornamento dell’elemento.

>[!NOTE]
>
>I consigli distribuiti dipendono dal gruppo di host o dall’ID ambiente specificato nella richiesta.


Se i prodotti non vengono visualizzati, assicurati di utilizzare il gruppo host corretto. Ad esempio, se imposti che il consiglio usi un ambiente di gestione temporanea e imposti il gruppo host su Gestione temporanea, potrebbe essere necessario ricreare le raccolte nell&#39;ambiente di gestione temporanea perché si visualizzino i prodotti. Per visualizzare i prodotti disponibili in ogni ambiente, utilizza Ricerca catalogo con ogni ambiente. Puoi anche visualizzare in anteprima il contenuto delle raccolte ed esclusioni di Recommendations per un ambiente selezionato (gruppo di host).

>[!NOTE]
>Dopo aver modificato l’ambiente selezionato, fai clic su Cerca per aggiornare i risultati restituiti.

Il filtro [!UICONTROL Environment] è disponibile nelle seguenti posizioni nell&#39;interfaccia utente di Target:

* Ricerca nel catalogo ([!UICONTROL Recommendations > Catalog Search])
* Finestra di dialogo Crea raccolta ([!UICONTROL Recommendations > Collections > Create New])
* Finestra di dialogo Aggiorna raccolta ([!UICONTROL Recommendations > Collections > Edit])
* Finestra di dialogo Crea esclusione ([!UICONTROL Recommendations > Exclusions > Create New])
* Finestra di dialogo Aggiorna esclusione ([!UICONTROL Recommendations > Exclusions > Edit])
