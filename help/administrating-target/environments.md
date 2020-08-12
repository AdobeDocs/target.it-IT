---
keywords: environment;troubleshooting;best practices;ubox;redirects;redirect;whitelist;blacklist;blocklist;allowlist
description: Organizza siti e ambienti di preproduzione per gestirli facilmente e per generare rapporti separati.
title: Ambienti
feature: null
topic: Standard
uuid: c7682269-4ec2-4a0f-b053-7e0ec77f4604
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 68%

---


# Ambienti

Organizza siti e ambienti di preproduzione per gestirli facilmente e per generare rapporti separati.

Per facilitare la gestione, gli host sono raccolti in ambienti. Ad esempio, si potrebbero avere decine di host raggruppati in due o tre ambienti. The preset environments include [!UICONTROL Production], [!UICONTROL Staging], and [!UICONTROL Development]. È anche possibile aggiungere nuovi ambienti e rinominare gli ambienti.

One environment, the default environment, is pre-named [!UICONTROL Production]. Questo ambiente predefinito non può essere eliminato, anche se lo si rinomina. [!DNL Target] presuppone che è qui che verranno eseguiti attività e test finali e approvati.

When a [!DNL Target] request is received from new websites or domains, these new domains always appear in the [!UICONTROL Production] environment. The [!UICONTROL Production] environment cannot have its settings changed, so unknown or new sites are guaranteed to see only content that is active and ready. La gestione degli host consente inoltre di garantire facilmente la qualità di nuove attività e contenuti nei test, nella gestione temporanea (staging) e negli ambienti di sviluppo prima di attivare le attività.

Per gestire gli ambienti, fate clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Ambienti]**.

![Elenco Ambienti](/help/administrating-target/assets/environments.png)

## Aggiunta di un ambiente {#section_32097D0993724DF3A202D164D3F18674}

1. Nell&#39;elenco [!UICONTROL Ambienti] , fare clic su **[!UICONTROL Aggiungi ambiente]**.
1. Specifica un nome descrittivo per l’ambiente.
1. Specifica la modalità attiva desiderata per l’ambiente: [!UICONTROL Attività attive] o [!UICONTROL Attività attive e inattive].
1. Fai clic su **[!UICONTROL Salva]**.

## Set the default environment for reporting {#section_4F8539B07C0C45E886E8525C344D5FB0}

È possibile selezionare l’ambiente che si desidera utilizzare come impostazione predefinita per tutti i rapporti di attività.

If you use [!UICONTROL Production] as your default, all unknown hosts automatically are added here and report data from there is included in the default report view. Invece, la creazione di un ambiente “pulito” assicura che siano inclusi solo i siti e domini principali.

Per impostare l’ambiente predefinito per la segnalazione:

1. Nell&#39;elenco [!UICONTROL Ambienti] , fate clic sull&#39;icona Stella

>[!NOTE]
>
>Se gli host passano ad altri gruppi host, gli utenti che usano la funzionalità [!DNL Recommendations] devono rigenerare il database dei comportamenti e quello dei prodotti.

## Change the name of an environment {#section_9F5F94285F8E495E9CE69810CE94CA08}

1. Dall&#39;elenco [!UICONTROL Ambiente] , fate clic sull&#39;icona **[!UICONTROL Modifica]** .
1. Modifica il nome dell’ambiente.
1. Fai clic su **[!UICONTROL Salva]**.

## Delete an environment {#section_737F8869612047868D03FC755B1223D3}

Quando un ambiente non è più necessario, è possibile eliminarlo.

1. Nell&#39;elenco [!UICONTROL Ambiente] , fare clic sull&#39;icona **[!UICONTROL Elimina]** .
1. Fai clic su **[!UICONTROL Elimina]** per confermare l’eliminazione.

>[!NOTE]
>
>You cannot delete the [!UICONTROL Production] environment, but you can rename it.

## Recommendations: filtrare raccolte ed esclusioni per ambiente (gruppo di host)

![Badge Premium](/help/assets/premium.png)

Puoi visualizzare in anteprima il contenuto delle raccolte ed esclusioni di Consigli per un ambiente selezionato (gruppo di host).

>[!NOTE]
>
>Recommendations activities are available as part of the [!DNL Target] Premium solution. Non sono disponibili in [!DNL Target] Standard senza una licenza [!DNL Target] Premium.

Un ambiente può essere utilizzato per separare gli elementi disponibili nel catalogo per usi diversi. For example, you can use host groups for [!UICONTROL Development] and [!UICONTROL Production] environments, different brands, or different geographies. Per impostazione predefinita, i risultati dell&#39;anteprima in Ricerca nel catalogo, Raccolte ed Esclusioni si basano sul gruppo di host predefinito. Puoi anche selezionare un gruppo di host diverso per visualizzare in anteprima i risultati, utilizzando il filtro Ambiente. Per impostazione predefinita, gli elementi appena aggiunti sono disponibili in tutti i gruppi di host, a meno che non sia specificato un ID ambiente al momento della creazione o dell&#39;aggiornamento dell&#39;elemento. I consigli distribuiti dipendono dal gruppo di host specificato nella richiesta.

Se i prodotti non vengono visualizzati, assicurati di utilizzare il gruppo host corretto. Ad esempio, se imposti che il consiglio usi un ambiente di gestione temporanea e imposti il gruppo host su Gestione temporanea, potrebbe essere necessario ricreare le raccolte nell&#39;ambiente di gestione temporanea perché si visualizzino i prodotti. Per visualizzare i prodotti disponibili in ogni ambiente, utilizza Ricerca catalogo con ogni ambiente. Puoi anche visualizzare in anteprima il contenuto delle raccolte ed esclusioni di Recommendations per un ambiente selezionato (gruppo di host).

>[!NOTE]
>Dopo aver modificato l’ambiente selezionato, fai clic su Cerca per aggiornare i risultati restituiti.

The [!UICONTROL Environment] filter is available from the following places in the Target UI:

* Ricerca nel catalogo ([!UICONTROL Recommendations > Ricerca nel catalogo])
* Finestra di dialogo Crea raccolta ([!UICONTROL Recommendations > Raccolte > Crea nuova])
* Finestra di dialogo Aggiorna raccolta ([!UICONTROL Recommendations > Raccolte > Modifica])
* Finestra di dialogo Crea esclusione ([!UICONTROL Recommendations > Esclusioni > Crea nuova])
* Finestra di dialogo Aggiorna esclusione ([!UICONTROL Recommendations > Esclusioni > Modifica])