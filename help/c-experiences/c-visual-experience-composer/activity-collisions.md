---
keywords: targeting;collisioni;conflitti
description: Le collisioni si verificano quando più attività sono configurate per distribuire contenuto alla stessa pagina. Scoprite come evitare conflitti quando si utilizza  Adobe Target.
title: Come Posso Evitare Collisioni Di Attività?
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 79%

---


# Conflitti tra attività

La scheda [!UICONTROL Collisions] nella pagina [!UICONTROL Activity Overview] in [!DNL Adobe Target] elenca le collisioni tra attività sul sito.

Un conflitto tra attività si verifica quando più attività sono configurate per distribuire contenuto alla stessa pagina. Se si verifica un conflitto tra attività, è possibile che nella pagina non venga visualizzato il contenuto previsto.

Se l&#39;attività include potenziali conflitti, nella pagina di panoramica dell’attività diventa disponibile la scheda [!UICONTROL Conflitti]. Sono indicate tutte le attività che fanno riferimento allo stesso URL, indipendentemente dall&#39;eventuale targeting di un pubblico in ogni attività. Apri questa scheda per un elenco delle attività potenzialmente in conflitto. Fai clic su un’attività nell’elenco per visualizzarne la pagina di panoramica. Se il conflitto altera l’esperienza prevista, modifica l’attività.

L&#39;elenco [!UICONTROL Collisions] consente di:

* Determina se un test sia già in esecuzione su una pagina prima di impostare una nuova attività
* Esegui la risoluzione dei problemi per un&#39;attività se non viene visualizzato il contenuto previsto

L&#39;elenco [!UICONTROL Collisions] mostra ogni [!DNL Target] scenario in cui viene utilizzata la mbox e che utilizza lo stesso URL. Per ogni potenziale conflitto, l’elenco mostra l’URL dell’attività, il nome dell’mbox in cui potrebbe verificarsi il conflitto ed eventuali attività che corrispondono a entrambi questi criteri. In presenza di mbox multiple, ciascuna viene visualizzata nell’elenco.

L’elenco mostra lo stato e la priorità di ogni potenziale conflitto, insieme ad altre informazioni. Puoi utilizzare lo stato e la priorità per determinare la probabilità del verificarsi di un conflitto. Se, ad esempio, esiste un potenziale conflitto tra due attività e una è inattiva, il conflitto non si verificherà effettivamente se l’attività inattiva non viene attivata. Se il potenziale conflitto è tra due attività in esecuzione con la stessa priorità e lo stesso pubblico, si verifica il conflitto. Per evitarlo, puoi modificare la priorità o lo stato.

Se i tipi di pubblico sono diversi, il potenziale conflitto permane, perché è possibile che un particolare visitatore appartenga a più tipi di pubblico.
