---
keywords: targeting;collisioni;conflitti
description: Impedisci conflitti nella consegna dei contenuti sulla stessa pagina configurando correttamente le attività in Adobe Target.
title: Come posso evitare le collisioni tra attività?
feature: Visual Experience Composer (VEC)
exl-id: 1af90dd1-69c9-41ec-8785-095dcc557b32
TQID: 'https://experienceleague.adobe.com/R6cwp4KnoYPO9Wxr47HswtBX6jKPJ0i-UGdtA1ZHawU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 18%
---
# Conflitti tra attività {#activity-collisions}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come utilizzare la scheda **[!UICONTROL Conflitti]** per trovare attività che potrebbero fornire contenuto alla stessa pagina.

>[!ENDSHADEBOX]

Un conflitto tra attività si verifica quando più attività sono configurate per distribuire contenuto alla stessa pagina. Se si verifica un conflitto tra attività, il contenuto previsto potrebbe non essere visualizzato nella pagina.

La scheda **[!UICONTROL Conflitti]** nella pagina **[!UICONTROL Panoramica attività]** di [!DNL Adobe Target] elenca i conflitti tra attività sul sito e mostra se un&#39;attività contiene potenziali conflitti. L&#39;elenco **[!UICONTROL Conflitti]** consente di:

* Identifica se un test è già in esecuzione su una pagina prima che venga impostata una nuova attività
* Esegui la risoluzione dei problemi per un&#39;attività se non viene visualizzato il contenuto previsto

## Accedere alla scheda Conflitti {#access-collisions}

Fai clic su **[!UICONTROL Attività]**, scegli l&#39;attività desiderata dall&#39;elenco, quindi accedi al menu **[!UICONTROL Conflitti]**.

![Icona Configura](assets/collisions_1.png)

Sono indicate tutte le attività che fanno riferimento allo stesso URL, indipendentemente dall&#39;eventuale targeting di un pubblico in ogni attività. Nella scheda sono elencate le attività che potrebbero entrare in conflitto. Se il conflitto altera l’esperienza prevista, modifica l’attività.

## Leggi l&#39;elenco Conflitti {#collisions-list}

L&#39;elenco **[!UICONTROL Conflitti]** mostra ogni [!DNL Target] scenario in cui viene utilizzata la mbox e che utilizza lo stesso URL. Per ogni potenziale conflitto, l’elenco mostra l’URL dell’attività, il nome della mbox in cui potrebbe verificarsi il conflitto e tutte le attività che corrispondono a entrambi i criteri. In presenza di mbox multiple, ciascuna viene visualizzata nell’elenco.

L’elenco mostra anche lo stato e la priorità di ogni potenziale conflitto, insieme ad altre informazioni. Lo stato e la priorità consentono di determinare la probabilità che si verifichi una collisione. Per due attività che potrebbero entrare in conflitto:

* Se un’attività non è attualmente attiva, non può verificarsi un conflitto. Una collisione è possibile solo se l’attività inattiva diventa attiva.
* Se il potenziale conflitto è tra due attività live con la stessa priorità e lo stesso pubblico, si verifica un conflitto. È possibile modificare la priorità o lo stato per evitare la collisione.
* Se i tipi di pubblico sono diversi, esiste ancora un potenziale conflitto, perché un visitatore particolare potrebbe appartenere a più tipi di pubblico.
