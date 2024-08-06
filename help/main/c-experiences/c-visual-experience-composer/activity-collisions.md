---
keywords: targeting;collisioni;conflitti
description: Impedisci conflitti nella consegna dei contenuti sulla stessa pagina configurando correttamente le attività in Adobe Target.
title: Come posso evitare le collisioni tra attività?
feature: Visual Experience Composer (VEC)
exl-id: 1af90dd1-69c9-41ec-8785-095dcc557b32
source-git-commit: 5c963e97dae11326396a5c1c5e32d19f4d463c74
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 50%

---

# Conflitti tra attività

La scheda [!UICONTROL Collisions] nella pagina [!UICONTROL Activity Overview] in [!DNL Adobe Target] elenca i conflitti di attività sul sito.

Un conflitto tra attività si verifica quando più attività sono configurate per distribuire contenuto alla stessa pagina. Se si verifica una collisione tra attività, è possibile che sulla pagina non venga visualizzato il contenuto previsto.

La scheda [!UICONTROL Collisions] è disponibile nella pagina di panoramica dell&#39;attività e può indicare se l&#39;attività contiene potenziali conflitti.

Per accedere alla scheda [!UICONTROL Collisions], fai clic su **[!UICONTROL Activities]** > fai clic sull&#39;attività desiderata dall&#39;elenco > quindi fai clic su **[!UICONTROL Collisions]** nella barra a sinistra.

Sono indicate tutte le attività che fanno riferimento allo stesso URL, indipendentemente dall&#39;eventuale targeting di un pubblico in ogni attività. Apri questa scheda per un elenco delle attività potenzialmente in conflitto. Se il conflitto altera l’esperienza prevista, modifica l’attività.

L&#39;elenco [!UICONTROL Collisions] consente di:

* Determina se un test sia già in esecuzione su una pagina prima di impostare una nuova attività
* Esegui la risoluzione dei problemi per un&#39;attività se non viene visualizzato il contenuto previsto

L&#39;elenco [!UICONTROL Collisions] mostra ogni [!DNL Target] scenario in cui viene utilizzata la mbox e che utilizza lo stesso URL. Per ogni potenziale conflitto, l’elenco mostra l’URL dell’attività, il nome della mbox in cui potrebbe verificarsi il conflitto e tutte le attività che corrispondono a entrambi i criteri. In presenza di mbox multiple, ciascuna viene visualizzata nell’elenco.

L’elenco mostra lo stato e la priorità di ogni potenziale conflitto, insieme ad altre informazioni. Puoi utilizzare lo stato e la priorità per determinare la probabilità del verificarsi di un conflitto. Considera due attività che potrebbero entrare in conflitto. Se un’attività non è attualmente attiva, non può verificarsi un conflitto. Una collisione è possibile solo se l’attività inattiva diventa attiva. Se il potenziale conflitto è tra due attività live con la stessa priorità e lo stesso pubblico, si verifica un conflitto. Per evitarlo, puoi modificare la priorità o lo stato.

Se i tipi di pubblico sono diversi, il potenziale conflitto permane, perché è possibile che un particolare visitatore appartenga a più tipi di pubblico.
