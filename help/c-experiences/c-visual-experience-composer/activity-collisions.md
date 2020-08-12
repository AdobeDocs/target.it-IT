---
keywords: Targeting
description: Nella scheda Conflitti della pagina Panoramica attività è incluso un elenco dei conflitti tra attività all’interno del sito.
title: Conflitti tra attività
feature: null
uuid: 0e53ef60-2f71-4b34-9383-1de5cf5d3ab5
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 100%

---


# Conflitti tra attività{#activity-collisions}

Nella scheda Conflitti della pagina Panoramica attività è incluso un elenco dei conflitti tra attività all’interno del sito.

Un conflitto tra attività si verifica quando più attività sono configurate per distribuire contenuto alla stessa pagina. Se si verifica un conflitto tra attività, è possibile che nella pagina non venga visualizzato il contenuto previsto.

Se l&#39;attività include potenziali conflitti, nella pagina di panoramica dell’attività diventa disponibile la scheda [!UICONTROL Conflitti]. Sono indicate tutte le attività che fanno riferimento allo stesso URL, indipendentemente dall&#39;eventuale targeting di un pubblico in ogni attività. Apri questa scheda per un elenco delle attività potenzialmente in conflitto. Fai clic su un’attività nell’elenco per visualizzarne la pagina di panoramica. Se il conflitto altera l’esperienza prevista, modifica l’attività.

Nell’elenco Conflitti è possibile eseguire le seguenti operazioni:

* Determina se un test sia già in esecuzione su una pagina prima di impostare una nuova attività
* Esegui la risoluzione dei problemi per un&#39;attività se non viene visualizzato il contenuto previsto

Nell&#39;elenco Conflitti è incluso ogni scenario di Target Standard in cui viene utilizzata l’mbox e che utilizza lo stesso URL. Per ogni potenziale conflitto, l’elenco mostra l’URL dell’attività, il nome dell’mbox in cui potrebbe verificarsi il conflitto ed eventuali attività che corrispondono a entrambi questi criteri. In presenza di mbox multiple, ciascuna viene visualizzata nell’elenco.

L’elenco mostra lo stato e la priorità di ogni potenziale conflitto, insieme ad altre informazioni. Puoi utilizzare lo stato e la priorità per determinare la probabilità del verificarsi di un conflitto. Se, ad esempio, esiste un potenziale conflitto tra due attività e una è inattiva, il conflitto non si verificherà effettivamente se l’attività inattiva non viene attivata. Se il potenziale conflitto è tra due attività in esecuzione con la stessa priorità e lo stesso pubblico, si verifica il conflitto. Per evitarlo, puoi modificare la priorità o lo stato.

Se i tipi di pubblico sono diversi, il potenziale conflitto permane, perché è possibile che un particolare visitatore appartenga a più tipi di pubblico.
